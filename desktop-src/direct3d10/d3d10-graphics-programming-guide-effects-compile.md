---
description: После создания результата сначала необходимо скомпилировать код для проверки синтаксических ошибок.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Компиляция эффекта (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e0c4364fab67b0e0e7c97b7478a023f6394b5515e6f1d16cf2d352172af6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128435"
---
# <a name="compile-an-effect-direct3d-10"></a>Компиляция эффекта (Direct3D 10)

После создания результата сначала необходимо скомпилировать код для проверки синтаксических ошибок. Это делается путем вызова одного из API-интерфейсов компиляции (например, D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory). Эти API вызывают компилятор эффектов, fxc.exe который является компилятором, используемым для компиляции кода HLSL. Именно поэтому синтаксис кода в результате выглядит очень похожим на код HLSL (существует несколько исключений, которые будут обработаны позже). Кстати, компилятор эффектов компилятора и HLSL (fxc.exe) находится в пакете SDK в папке служебных программ, чтобы можно было компилировать шейдер (или эффекты) в автономном режиме при выборе. См. документацию по запуску компилятора из командной строки.

-   [Том](#includes)
-   [Макросы](#macros)
-   [Флаги шейдера HLSL](#hlsl-shader-flags)
-   [Флаги FX](#fx-flags)
-   [Проверка ошибок](#checking-errors)
-   [Связанные темы](#related-topics)

Ниже приведен пример компиляции файла эффектов (из образца BasicHLSL10).


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

Один из параметров — это интерфейс include. Создайте один из них, если необходимо включить настраиваемое поведение при чтении включаемого файла. Это пользовательское поведение выполняется каждый раз при создании действия (использующего указатель включения) или при компиляции действия (которое использует указатель включения). Чтобы реализовать пользовательское поведение включения, создайте класс, производный от интерфейса include. Это предоставляет классу два метода: Open и Close. Реализуйте пользовательское поведение в методах Open и Close.

## <a name="macros"></a>Макросы

Компиляция эффектов также может принимать указатель на макросы, определенные в других местах. Например, предположим, что вы изменили воздействие на BasicHLSL10, чтобы использовать два макроса: ноль и один. Здесь показан код влияния, использующий два макроса.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Ниже приведено объявление для двух макросов.


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Макросы — это массив макросов, заканчивающийся нулем; где каждый макрос определяется структурой [**\_ \_ макроса D3D шейдера**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Наконец, измените вызов действия Compile, чтобы получить указатель на макросы.


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>Флаги шейдера HLSL

Флаги шейдера определяют ограничения шейдера компилятором HLSL. Эти флаги влияют на код, созданный компилятором шейдера, в том числе:

-   Рекомендации по размеру. Оптимизируйте код.
-   Вопросы отладки: Включение отладочной информации, запрет управления потоком.
-   Рекомендации по оборудованию: Цель компиляции и возможность запуска шейдера на устаревшем оборудовании.

Как правило, эти флаги могут быть логически объединены, предполагая, что не указаны две конфликтующие характеристики. Список флагов см. в разделе [константы эффектов (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="fx-flags"></a>Флаги FX

Эти флаги используются при создании эффектов для определения поведения компиляции или поведения воздействия на среду выполнения. Список флагов см. в разделе [константы эффектов (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="checking-errors"></a>Проверка ошибок

Если во время компиляции возникает ошибка, API возвращает интерфейс, который содержит ошибки, возвращенные компилятором влияния. Этот интерфейс называется ID3D10Blob. Однако он не читается напрямую, но возвращает указатель на буфер, содержащий данные (которые являются строкой), можно увидеть любые ошибки компиляции.

В этом примере в результат Басичлсл. FX было введено сообщение об ошибке, которое дважды копирует объявление первой переменной.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Эта ошибка привела к возвращению компилятором следующей ошибки, как показано на следующем снимке экрана окна контрольных значений в Microsoft Visual Studio.

![снимок экрана окна "контрольные значения Visual Studio"](images/effect-compile-errors-2.jpg)

Так как ошибка возвращается в указатель ЛПВОИД, приведите ее к символьной строке в окне Контрольные значения.

Ниже приведен код, который используется для возврата ошибки из-за неудачной компиляции.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отрисовка влияния (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



