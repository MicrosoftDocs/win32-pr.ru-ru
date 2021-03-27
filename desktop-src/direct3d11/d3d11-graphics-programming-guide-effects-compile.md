---
title: Компиляция результата (Direct3D 11)
description: После создания результата необходимо скомпилировать код для проверки синтаксических ошибок.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987627"
---
# <a name="compile-an-effect-direct3d-11"></a>Компиляция результата (Direct3D 11)

После создания результата необходимо скомпилировать код для проверки синтаксических ошибок.

Это можно сделать, вызвав один из API-интерфейсов компиляции ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)или [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ). Эти API вызывают компилятор эффектов fxc.exe, который компилирует код HLSL. Именно поэтому синтаксис кода в результате выглядит очень похожим на код HLSL. (Существует несколько исключений, которые будут обработаны позже). Компилятор компилятора HLSL, fxc.exe, доступен в пакете SDK в папке Служебные программы, чтобы шейдеры (или эффекты) можно было компилировать в автономном режиме при выборе. См. документацию по запуску компилятора из командной строки.

-   [Пример](#example)
-   [Том](#includes)
-   [Поиск включаемых файлов](#searching-for-include-files)
-   [Макросы](#macros)
-   [Флаги шейдера HLSL](#hlsl-shader-flags)
-   [Флаги FX](#fx-flags)
-   [Проверка ошибок](#checking-errors)
-   [См. также](#related-topics)

## <a name="example"></a>Например, .

Ниже приведен пример компиляции файла эффектов.


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a>Includes

Одним из параметров API-интерфейсов компиляции является интерфейс include. Создайте один из них, если необходимо включить настраиваемое поведение, когда компилятор считывает включаемый файл. Компилятор выполняет это пользовательское поведение каждый раз при создании или компиляции влияния (которое использует указатель include). Чтобы реализовать пользовательское поведение включения, создайте класс, производный от интерфейса [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) . Это предоставляет классу два метода: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) и [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close). Реализуйте пользовательское поведение в этих методах.

## <a name="searching-for-include-files"></a>Поиск включаемых файлов

Указатель, переданный компилятором в параметр *ппарентдата* в метод [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) обработчика include, может не указывать на контейнер, включающий \# включаемый файл, который компилятору необходимо скомпилировать в код шейдера. То есть компилятор может передать **значение NULL** в *ппарентдата*. Поэтому рекомендуется выполнять поиск по своему собственному списку включаемых расположений для содержимого. Обработчик include может динамически добавлять новые расположения для включения, так как они получают эти расположения в вызовах метода **Open** .

В следующем примере предположим, что включаемые файлы кода шейдера хранятся в каталоге *сомевхерилсе* . Когда компилятор вызывает метод [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) обработчика include для открытия и чтения содержимого *сомевхерилсе \\ foo. h*, обработчик include может сохранить расположение каталога **сомевхерилсе** . Позже, когда компилятор вызывает метод **Open** обработчика include для открытия и чтения содержимого файла *Bar. h*, обработчик include может автоматически искать в каталоге *сомевхерилсе* для *Bar. h*.


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a>Макросы

Компиляция эффектов также может принимать указатель на макросы, определенные в других местах. Например, предположим, что вы хотите изменить результат в BasicHLSL10, чтобы использовать два макроса: ноль и один. Здесь показан код влияния, использующий два макроса.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Ниже приведено объявление для двух макросов.


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Макросы — это массив макросов, заканчивающийся нулем; где каждый макрос определяется с помощью структуры [**\_ \_ макроса D3D10 шейдера**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Измените вызов действия Compile, чтобы получить указатель на макросы.


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a>Флаги шейдера HLSL

Флаги шейдера определяют ограничения шейдера компилятором HLSL. Эти флаги влияют на код, создаваемый компилятором шейдера следующими способами.

-   Оптимизируйте размер кода.
-   Включая отладочную информацию, которая предотвращает управление потоком.
-   Влияет на цель компиляции и возможность запуска шейдера на устаревшем оборудовании.

Эти флаги могут быть логически объединены, если не указаны две конфликтующие характеристики. Список флагов см. в разделе [ \_ константы шейдера D3D10](/windows/desktop/direct3d10/d3d10-shader).

## <a name="fx-flags"></a>Флаги FX

Используйте эти флаги при создании эффектов для определения поведения компиляции или поведения воздействия на среду выполнения. Список флагов см. в разделе [ \_ константы D3D10 Effect](/windows/desktop/direct3d10/d3d10-effect).

## <a name="checking-errors"></a>Проверка ошибок

Если во время компиляции возникает ошибка, API возвращает интерфейс, который содержит ошибки от компилятора эффектов. Этот интерфейс называется [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)). Он не читается напрямую; Однако, возвращая указатель на буфер, содержащий данные (которые являются строкой), можно увидеть ошибки компиляции.

Этот пример содержит ошибку в Басичлсл. FX, первое объявление переменной возникает дважды.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Эта ошибка приводит к тому, что компилятор возвращает следующую ошибку, как показано на следующем снимке экрана окно контрольных значений в Microsoft Visual Studio.

![снимок экрана окна "контрольные значения Visual Studio" с ошибкой 0x01997fb8](images/effect-compile-errors-2.jpg)

Так как компилятор возвращает ошибку в ЛПВОИД указателе, приведите его к символьной строке в окно контрольных значений.

Ниже приведен код, который возвращает ошибку из-за неудачной компиляции.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Отрисовка результата (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 