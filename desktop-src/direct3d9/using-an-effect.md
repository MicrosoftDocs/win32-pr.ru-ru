---
description: На этой странице будет показано, как создать и использовать результат.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Использование влияния (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d240148c8817a3e480099a3ad1acb81bbff60803b0d0a8327e3a77cba681b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856104"
---
# <a name="using-an-effect-direct3d-9"></a>Использование влияния (Direct3D 9)

На этой странице будет показано, как создать и использовать результат. В этом разделе рассматриваются следующие темы:

-   [Создание результата](#create-an-effect)
-   [Отрисовка результата](#render-an-effect)
-   [Использование семантики для поиска параметров эффектов](#use-semantics-to-find-effect-parameters)
-   [Использование дескрипторов для эффективного получения и задания параметров](#use-handles-to-get-and-set-parameters-efficiently)
-   [Добавление сведений о параметрах с заметками](#add-parameter-information-with-annotations)
-   [Общие параметры эффектов](#share-effect-parameters)
-   [Компиляция влияния в автономный режим](#compile-an-effect-offline)
-   [Повышение производительности с помощью предтеней](#improve-performance-with-preshaders)
-   [Использование блоков параметров для управления параметрами эффектов](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a>Создание результата

Ниже приведен пример создания действия, взятого из [примера басичлсл](../directx-sdk--august-2009-.md). Код создания результатов для создания шейдера отладки — из **онкреатедевице**:


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



Эта функция принимает следующие аргументы:

-   Устройство.
-   Имя файла действия.
-   Указатель на список определений, заканчивающийся НУЛЕМ \# , для использования при синтаксическом анализе шейдера.
-   Необязательный указатель на обработчик include, написанный пользователем. Обработчик вызывается процессором каждый раз, когда ему требуется разрешить \# Включение.
-   Флаг компиляции шейдера, который предоставляет указания компилятора о том, как будет использоваться шейдер. Эти способы могут быть следующими:
    -   Пропуск проверки, если компилируются известные хорошие шейдеры.
    -   Пропуск оптимизации (иногда используется, когда оптимизация усложняет отладку).
    -   Запрос сведений об отладке для включения в шейдер, чтобы их можно было отлаживать.
-   Пул эффектов. Если один и тот же указатель пула памяти используется несколькими эффектами, то глобальные переменные в эффектах совместно используются друг с другом. Если нет необходимости совместно использовать переменные влияния, пул памяти может иметь значение **null**.
-   Указатель на новый результат.
-   Указатель на буфер, в который могут отправляться ошибки проверки. В этом примере параметр был установлен в **значение NULL** и не используется.

> [!Note]  
> Начиная с пакета SDK 2006 декабря, компилятор HLSL DirectX 10 теперь является компилятором по умолчанию как в DirectX 9, так и в DirectX 10. Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .

 

## <a name="render-an-effect"></a>Отрисовка результата

Последовательность вызовов для применения состояния эффектов к устройству:

-   [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) задает активный метод.
-   [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) задает активный проход.
-   [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) обновляет изменения любых вызовов набора в ходе передачи. Он должен вызываться перед любым вызовом Draw.
-   [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md) завершает проход.
-   [**ID3DXEffect:: end**](id3dxeffect--end.md) завершает активный метод.

Код рендеринга эффектов также проще, чем соответствующий код отрисовки без влияния. Вот как выглядит код отрисовки:


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



Цикл рендеринга состоит из запроса к результату, чтобы увидеть, сколько их содержит, а затем вызывает все проходы для приемки. Цикл рендеринга можно расширить для вызова нескольких методов, каждый из которых имеет несколько проходов.

## <a name="use-semantics-to-find-effect-parameters"></a>Использование семантики для поиска параметров эффектов

Семантика — это идентификатор, прикрепленный к параметру Effect, позволяющий приложению искать параметр. Параметр может иметь не более одной семантики. Семантика находится после двоеточия (:) после имени параметра. Например:


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



Если вы объявили глобальную переменную Effect без использования семантической семантики, она будет выглядеть следующим образом:


```
float4x4 matWorldViewProj;
```



Интерфейс Effect может использовать семантику для получения маркера для конкретного параметра effect. Например, следующий метод возвращает маркер матрицы:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



Помимо поиска по семантическому имени, интерфейс Effect имеет много других методов для поиска параметров.

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a>Использование дескрипторов для эффективного получения и задания параметров

Дескрипторы предоставляют эффективные средства для создания ссылок на параметры, методы, проходы и аннотации с применением эффектов. Дескрипторы (которые имеют тип D3DXHANDLE) являются строковыми указателями. Дескрипторы, передаваемые в функции, такие как Жетпараметеркскскс или Жетаннотатионкскскс, могут быть представлены в одной из трех форм:

-   Маркер, возвращаемый функцией, например Жетпараметеркскскс.
-   Строка, содержащая имя параметра, метода, прохода или заметки.
-   **Значение параметра handle.**

В этом примере возвращается маркер для параметра, к которому прикреплена семантика ВОРЛДВИЕВПРОЖ:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a>Добавление сведений о параметрах с заметками

Заметки представляют собой определяемые пользователем данные, которые могут быть присоединены к любому методу, параметру Pass или. Заметка — это гибкий способ добавления сведений к отдельным параметрам. Эти сведения можно считать и использовать любым способом, выбранным приложением. Аннотация может иметь любой тип данных и может быть динамически добавлена. Объявления заметок разделяются угловыми скобками. Аннотация содержит:

-   Тип данных.
-   Имя переменной.
-   Знак равенства (=).
-   Значение данных.
-   Конечная точка с запятой (;).

Например, оба приведенных выше примера в этом документе содержат следующую аннотацию:


```
texture Tex0 < string name = "tiger.bmp"; >;
```



Заметка присоединена к объекту текстуры и задает файл текстуры, который должен использоваться для инициализации объекта текстуры. Заметка не инициализирует объект текстуры, это просто часть сведений о пользователе, которая присоединяется к переменной. Приложение может прочитать заметку с помощью [**ID3DXBaseEffect::**](id3dxbaseeffect--getannotation.md) GetString или [**ID3DXBaseEffect:: жетаннотатионбинаме**](id3dxbaseeffect--getannotationbyname.md) , чтобы получить строку. Заметки также могут добавляться приложением.

Каждая аннотация:

-   Должен быть либо числовым, либо строкой.
-   Всегда должно быть инициализировано значением по умолчанию.
-   Может быть связан с [методами и передается (Direct3D 9)](techniques-and-passes.md) и [параметрами эффектов](/previous-versions/windows/desktop/ee417539(v=vs.85))верхнего уровня.
-   Можно записывать и считывать с помощью [**ID3DXEffect**](id3dxeffect.md) или [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).
-   Можно добавить с помощью [**ID3DXEffect**](id3dxeffect.md).
-   Не может ссылаться внутри этого результата.
-   Не может иметь подсемантику или поданнотации.

## <a name="share-effect-parameters"></a>Общие параметры эффектов

Параметры эффектов — это все нестатические переменные, объявленные в результате. Это могут быть глобальные переменные и заметки. Параметры эффектов могут совместно использоваться различными эффектами путем объявления параметров с ключевым словом "Shared" и последующего создания эффекта с пулом эффектов.

Пул эффектов содержит общие параметры эффектов. Пул создается путем вызова [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), который возвращает интерфейс [**ID3DXEffectPool**](id3dxeffectpool.md) . Интерфейс может быть указан в качестве входных данных для любой функции D3DXCreateEffectxxx при создании результата. Чтобы параметр был совместно использоваться несколькими эффектами, параметр должен иметь одинаковое имя, тип и семантику в каждом из общих эффектов.


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



Эффекты, которые совместно используют параметры, должны использовать одно и то же устройство. Это применяется для предотвращения совместного использования зависимых от устройства параметров (таких как шейдеры или текстуры) на разных устройствах. Параметры удаляются из пула при выпуске эффектов, содержащих общие параметры. Если общий доступ к параметрам не требуется, при создании результата укажите **значение NULL** для пула эффектов.

Клонированные эффекты используют тот же пул эффектов, что и результат клонирования. При клонировании действия создается точная копия результата, включая глобальные переменные, методы, проходы и заметки.

## <a name="compile-an-effect-offline"></a>Компиляция влияния в автономный режим

Вы можете компилировать эффекты во время выполнения с помощью [**D3DXCreateEffect**](d3dxcreateeffect.md), а также компилировать эффекты в автономном режиме, используя средство компилятора командной строки fxc.exe. Результат в [примере компиледеффект](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) содержит Вершинный шейдер, шейдер пикселей и один прием:


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



Использование [средства компилятора Effect](../direct3dtools/fxc.md) для компиляции шейдера для VS 1 \_ \_ 1 создало следующие инструкции шейдера сборки:


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a>Повышение производительности с помощью предтеней

Предварительный шейдер — это метод повышения эффективности шейдера путем предварительного вычисления выражений шейдеров констант. Компилятор результатов автоматически извлекает вычисления шейдера из тела шейдера и выполняет их на ЦП до запуска шейдера. Следовательно, предшейдеры работают только с эффектами. Например, эти два выражения можно вычислить за пределами шейдера перед его запуском.


```
mul(World,mul(View, Projection));
sin(time)
```



Вычисления шейдеров, которые могут быть перемещены, связаны с равномерными параметрами; то есть вычисления не изменяются для каждой вершины или пикселя. При использовании эффектов компилятор автоматически создает и выполняет предшейдер. нет флагов для включения. Предшейдеры могут уменьшить количество инструкций на шейдер, а также сократить количество постоянных регистров, используемых шейдером.

Компилятор эффектов следует рассматривать как тип многопроцессорного компилятора, поскольку он компилирует код шейдера для двух типов процессоров: ЦП и GPU. Кроме того, компилятор эффектов предназначен для перемещения кода из GPU в ЦП и, следовательно, для повышения производительности шейдера. Это очень похоже на извлечение статического выражения из цикла. Шейдер, который преобразует расположение из мира в пространство проекции и копирует координаты текстуры, будет выглядеть следующим образом в HLSL:


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



Использование [средства компилятора Effect](../direct3dtools/fxc.md) для компиляции шейдера для VS \_ 1 \_ 1 приводит к следующим инструкциям по сборке:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Это занимает около 14 слотов и использует 9 постоянных регистров. При использовании предшейдера компилятор перемещает статические выражения из шейдера и в предшейдер. Один и тот же шейдер будет выглядеть следующим образом с помощью предшейдера:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Перед выполнением шейдера он выполняет предварительный построитель. Результат — это те же функциональные возможности, что и повышение производительности шейдера, поскольку было уменьшено количество инструкций, которые необходимо выполнить (для каждой вершины или пикселя в зависимости от типа шейдера). Кроме того, шейдер использует меньше регистров констант в результате того, как статические выражения перемещаются в предшейдер. Это означает, что шейдеры, ранее ограниченные количеством постоянных регистров, которые они требуют, теперь могут компилироваться, так как для них требуется меньше постоянных регистров. Разумно рассчитывать на 5-процентный и 20-процентное улучшение производительности от предтеней.

Помните, что входные константы отличаются от выходных констант в предшейдере. Выходные данные C1 не совпадают с входным регистром C1. Запись в регистр константы в предшейдере фактически записывает в соответствующий входной слот шейдера (константа).


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



Приведенная выше инструкция CMP будет считать значение C1, а инструкция mul будет записывать в реестры аппаратного шейдера для использования шейдером вершин.

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a>Использование блоков параметров для управления параметрами эффектов

Блоки параметров — это блоки изменений состояния эффектов. Блок параметров может записывать изменения состояния, чтобы их можно было применить позже с помощью одного вызова. Создайте блок параметров, вызвав [**ID3DXEffect:: бегинпараметерблокк**](id3dxeffect--beginparameterblock.md):


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



Блок параметров сохраняет четыре изменения, примененные вызовами API. Вызов [**ID3DXEffect:: бегинпараметерблокк**](id3dxeffect--beginparameterblock.md) начинает запись изменений состояния. [**ID3DXEffect:: ендпараметерблокк**](id3dxeffect--endparameterblock.md) останавливает Добавление изменений в блок параметров и возвращает маркер. Этот маркер будет использоваться при вызове [**ID3DXEffect:: апплипараметерблокк**](id3dxeffect--applyparameterblock.md).

В [примере еффектпарам](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx)в последовательности прорисовки применяется блок параметров:


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



Блок параметров задает значения всех четырех изменений состояния непосредственно перед вызовом [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) . Блоки параметров — это удобный способ установки нескольких изменений состояния с помощью одного вызова API.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Эффекты](effects.md)
</dt> </dl>

 

 
