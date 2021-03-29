---
description: 'При использовании Direct3D 10 состояние воздействия для определенных стадий конвейера организовано по следующим структурам:'
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Упорядочение состояния в силе (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79cbea90c4d42d0a24ec7e35815616bf6698f72f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141199"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a>Упорядочение состояния в силе (Direct3D 10)

При использовании Direct3D 10 состояние воздействия для определенных стадий конвейера организовано по следующим структурам:



| Состояние конвейера  | Структура                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| Сборщик входных данных | [**\_Элемент ввода D3D10, \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| Rasterization   | [**D3D10 средство программной \_ прорисовки \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| Средство слияния выхода   | [**D3D10 \_ Desc \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) и [ **D3D10 \_ \_ набор элементов \_ глубины**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |



 

Для этапов шейдера, где число изменений состояния должно быть более управляемым приложением, состояние делится на постоянное состояние буфера, состояние образца и состояние ресурса шейдера. Это позволяет приложению, которое тщательно спроектировано для обновления только изменяемого состояния, что повышает производительность за счет уменьшения объема данных, которые необходимо передать в GPU.

Так как же вы организуете состояние конвейера в результате?

Ответ заключается в том, что порядок не имеет значения. В верхней части не нужно размещать глобальные переменные. Тем не менее, все примеры в пакете SDK выполняются в том же порядке, что и оптимальный способ организации данных. Это краткое описание порядка данных в примерах пакета SDK для DirectX.

-   [Глобальные переменные](#global-variables)
-   [Шейдеры](#shaders)
-   [Методы и проходы](#techniques-and-passes)

## <a name="global-variables"></a>Глобальные переменные

Как и в случае со стандартной практикой C, глобальные переменные объявляются первыми в начале файла. Чаще всего это переменные, которые будут инициализированы приложением, а затем используются в результате. Иногда они инициализируются и никогда не изменяются. в других случаях они обновляются в каждом кадре. Как и в случае с областью видимости функции C, переменные эффектов, объявленные за пределами области функций эффектов, видимы по всему результату. Любая переменная, объявленная внутри функции Effect, видна только внутри этой функции.

Ниже приведен пример переменных, объявленных в BasicHLSL10. FX.


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix


// Texture samplers
SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};
```



Синтаксис переменных эффектов более подробно описан в [синтаксисе переменных эффектов (Direct3D 10)](d3d10-effect-variable-syntax.md). Синтаксис для выборок текстурной текстуры более подробно описан в [типе образца (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="shaders"></a>Шейдеры

Шейдеры — это небольшие исполняемые программы. Шейдеры можно представить как инкапсулированное состояние шейдера, так как код HLSL реализует функцию шейдера. В конвейере используются три различных типа шейдеров.

-   Шейдеры вершин — работают с данными вершин. Одна вершина в выдает одну вершину.
-   Шейдеры Geometry — работают с примитивными данными. Один примитив в может возвращать 0, 1 или многие примитивы.
-   Шейдеры пикселей — работают с данными пикселей. Один пиксель в выдает 1 пиксель (если только пиксел не исключается из отрисовки).

Шейдеры являются локальными функциями и следуют правилам функций в стиле языка C. При компиляции результата каждый из них компилируется, а указатель на каждую функцию шейдера хранится внутренним образом. При успешном завершении компиляции возвращается интерфейс ID3D10Effect. На этом этапе скомпилированный результат имеет промежуточный формат.

Чтобы получить дополнительные сведения о скомпилированных шейдерах, необходимо использовать отражение шейдера. Это, по сути, запрос среды выполнения декомпиляции шейдеров и возвращения информации о коде шейдера.


```
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
 
    ....    
    
    return Output;    
}


struct PS_OUTPUT
{
    float4 RGBColor : SV_Target;  // Pixel color
};

PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    ....

    return Output;
}
```



Синтаксис для шейдеров эффектов более подробно описан в [синтаксисе функции Effect (Direct3D 10)](d3d10-effect-function-syntax.md).

## <a name="techniques-and-passes"></a>Методы и проходы

Метод — это набор этапов отрисовки (должен быть хотя бы один проход). Каждый пройденный результат (аналогичный в области до одного прохода в цикле подготовки к просмотру) определяет состояние шейдера и любое другое состояние конвейера, необходимое для визуализации геометрии.

Ниже приведен пример одного метода (который включает один проход) из BasicHLSL10. FX.


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



Синтаксис шейдеров эффектов более подробно описан в [синтаксисе методики влияния (Direct3D 10)](d3d10-effect-technique-syntax.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Эффекты (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
