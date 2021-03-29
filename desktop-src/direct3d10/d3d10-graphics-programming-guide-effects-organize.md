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
# <a name="organizing-state-in-an-effect-direct3d-10"></a><span data-ttu-id="1a4ad-103">Упорядочение состояния в силе (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1a4ad-103">Organizing State in an Effect (Direct3D 10)</span></span>

<span data-ttu-id="1a4ad-104">При использовании Direct3D 10 состояние воздействия для определенных стадий конвейера организовано по следующим структурам:</span><span class="sxs-lookup"><span data-stu-id="1a4ad-104">With Direct3D 10, effect state for certain pipeline stages is organized by the following structures:</span></span>



| <span data-ttu-id="1a4ad-105">Состояние конвейера</span><span class="sxs-lookup"><span data-stu-id="1a4ad-105">Pipeline State</span></span>  | <span data-ttu-id="1a4ad-106">Структура</span><span class="sxs-lookup"><span data-stu-id="1a4ad-106">Structure</span></span>                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4ad-107">Сборщик входных данных</span><span class="sxs-lookup"><span data-stu-id="1a4ad-107">Input Assembler</span></span> | [<span data-ttu-id="1a4ad-108">**\_Элемент ввода D3D10, \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1a4ad-108">**D3D10\_INPUT\_ELEMENT\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| <span data-ttu-id="1a4ad-109">Rasterization</span><span class="sxs-lookup"><span data-stu-id="1a4ad-109">Rasterization</span></span>   | [<span data-ttu-id="1a4ad-110">**D3D10 средство программной \_ прорисовки \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1a4ad-110">**D3D10\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| <span data-ttu-id="1a4ad-111">Средство слияния выхода</span><span class="sxs-lookup"><span data-stu-id="1a4ad-111">Output Merger</span></span>   | <span data-ttu-id="1a4ad-112">[**D3D10 \_ Desc \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) и [ **D3D10 \_ \_ набор элементов \_ глубины**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="1a4ad-112">[**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) and [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |



 

<span data-ttu-id="1a4ad-113">Для этапов шейдера, где число изменений состояния должно быть более управляемым приложением, состояние делится на постоянное состояние буфера, состояние образца и состояние ресурса шейдера.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-113">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, and shader resource state.</span></span> <span data-ttu-id="1a4ad-114">Это позволяет приложению, которое тщательно спроектировано для обновления только изменяемого состояния, что повышает производительность за счет уменьшения объема данных, которые необходимо передать в GPU.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-114">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="1a4ad-115">Так как же вы организуете состояние конвейера в результате?</span><span class="sxs-lookup"><span data-stu-id="1a4ad-115">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="1a4ad-116">Ответ заключается в том, что порядок не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-116">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="1a4ad-117">В верхней части не нужно размещать глобальные переменные.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-117">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="1a4ad-118">Тем не менее, все примеры в пакете SDK выполняются в том же порядке, что и оптимальный способ организации данных.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-118">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="1a4ad-119">Это краткое описание порядка данных в примерах пакета SDK для DirectX.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-119">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="1a4ad-120">Глобальные переменные</span><span class="sxs-lookup"><span data-stu-id="1a4ad-120">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="1a4ad-121">Шейдеры</span><span class="sxs-lookup"><span data-stu-id="1a4ad-121">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="1a4ad-122">Методы и проходы</span><span class="sxs-lookup"><span data-stu-id="1a4ad-122">Techniques and Passes</span></span>](#techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="1a4ad-123">Глобальные переменные</span><span class="sxs-lookup"><span data-stu-id="1a4ad-123">Global Variables</span></span>

<span data-ttu-id="1a4ad-124">Как и в случае со стандартной практикой C, глобальные переменные объявляются первыми в начале файла.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-124">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="1a4ad-125">Чаще всего это переменные, которые будут инициализированы приложением, а затем используются в результате.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-125">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="1a4ad-126">Иногда они инициализируются и никогда не изменяются. в других случаях они обновляются в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-126">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="1a4ad-127">Как и в случае с областью видимости функции C, переменные эффектов, объявленные за пределами области функций эффектов, видимы по всему результату. Любая переменная, объявленная внутри функции Effect, видна только внутри этой функции.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-127">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="1a4ad-128">Ниже приведен пример переменных, объявленных в BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-128">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


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



<span data-ttu-id="1a4ad-129">Синтаксис переменных эффектов более подробно описан в [синтаксисе переменных эффектов (Direct3D 10)](d3d10-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="1a4ad-129">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 10)](d3d10-effect-variable-syntax.md).</span></span> <span data-ttu-id="1a4ad-130">Синтаксис для выборок текстурной текстуры более подробно описан в [типе образца (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1a4ad-130">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="shaders"></a><span data-ttu-id="1a4ad-131">Шейдеры</span><span class="sxs-lookup"><span data-stu-id="1a4ad-131">Shaders</span></span>

<span data-ttu-id="1a4ad-132">Шейдеры — это небольшие исполняемые программы.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-132">Shaders are small executable programs.</span></span> <span data-ttu-id="1a4ad-133">Шейдеры можно представить как инкапсулированное состояние шейдера, так как код HLSL реализует функцию шейдера.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-133">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="1a4ad-134">В конвейере используются три различных типа шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-134">The pipeline uses three different kinds of shaders.</span></span>

-   <span data-ttu-id="1a4ad-135">Шейдеры вершин — работают с данными вершин.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-135">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="1a4ad-136">Одна вершина в выдает одну вершину.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-136">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="1a4ad-137">Шейдеры Geometry — работают с примитивными данными.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-137">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="1a4ad-138">Один примитив в может возвращать 0, 1 или многие примитивы.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-138">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="1a4ad-139">Шейдеры пикселей — работают с данными пикселей.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-139">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="1a4ad-140">Один пиксель в выдает 1 пиксель (если только пиксел не исключается из отрисовки).</span><span class="sxs-lookup"><span data-stu-id="1a4ad-140">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="1a4ad-141">Шейдеры являются локальными функциями и следуют правилам функций в стиле языка C.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-141">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="1a4ad-142">При компиляции результата каждый из них компилируется, а указатель на каждую функцию шейдера хранится внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-142">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="1a4ad-143">При успешном завершении компиляции возвращается интерфейс ID3D10Effect.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-143">An ID3D10Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="1a4ad-144">На этом этапе скомпилированный результат имеет промежуточный формат.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-144">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="1a4ad-145">Чтобы получить дополнительные сведения о скомпилированных шейдерах, необходимо использовать отражение шейдера.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-145">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="1a4ad-146">Это, по сути, запрос среды выполнения декомпиляции шейдеров и возвращения информации о коде шейдера.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-146">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


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



<span data-ttu-id="1a4ad-147">Синтаксис для шейдеров эффектов более подробно описан в [синтаксисе функции Effect (Direct3D 10)](d3d10-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="1a4ad-147">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 10)](d3d10-effect-function-syntax.md).</span></span>

## <a name="techniques-and-passes"></a><span data-ttu-id="1a4ad-148">Методы и проходы</span><span class="sxs-lookup"><span data-stu-id="1a4ad-148">Techniques and Passes</span></span>

<span data-ttu-id="1a4ad-149">Метод — это набор этапов отрисовки (должен быть хотя бы один проход).</span><span class="sxs-lookup"><span data-stu-id="1a4ad-149">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="1a4ad-150">Каждый пройденный результат (аналогичный в области до одного прохода в цикле подготовки к просмотру) определяет состояние шейдера и любое другое состояние конвейера, необходимое для визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-150">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="1a4ad-151">Ниже приведен пример одного метода (который включает один проход) из BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="1a4ad-151">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


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



<span data-ttu-id="1a4ad-152">Синтаксис шейдеров эффектов более подробно описан в [синтаксисе методики влияния (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="1a4ad-152">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a4ad-153">См. также</span><span class="sxs-lookup"><span data-stu-id="1a4ad-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a4ad-154">Эффекты (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1a4ad-154">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
