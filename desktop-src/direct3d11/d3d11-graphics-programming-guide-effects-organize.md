---
title: Упорядочение состояния в силе (Direct3D 11)
description: При использовании Direct3D 11 состояние воздействия для определенных стадий конвейера упорядочивается по структурам.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0523dd8abdabde29a5485b8d3b1e6d13b9429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997103"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a><span data-ttu-id="bb26d-103">Упорядочение состояния в силе (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="bb26d-103">Organizing State in an Effect (Direct3D 11)</span></span>

<span data-ttu-id="bb26d-104">При использовании Direct3D 11 состояние воздействия для определенных стадий конвейера упорядочивается по структурам.</span><span class="sxs-lookup"><span data-stu-id="bb26d-104">With Direct3D 11, effect state for certain pipeline stages is organized by structures.</span></span> <span data-ttu-id="bb26d-105">Ниже приведены структуры.</span><span class="sxs-lookup"><span data-stu-id="bb26d-105">Here are the structures:</span></span>



| <span data-ttu-id="bb26d-106">Состояние конвейера</span><span class="sxs-lookup"><span data-stu-id="bb26d-106">Pipeline State</span></span> | <span data-ttu-id="bb26d-107">Структура</span><span class="sxs-lookup"><span data-stu-id="bb26d-107">Structure</span></span>                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb26d-108">Rasterization</span><span class="sxs-lookup"><span data-stu-id="bb26d-108">Rasterization</span></span>  | [<span data-ttu-id="bb26d-109">**D3D11 средство программной \_ прорисовки \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="bb26d-109">**D3D11\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| <span data-ttu-id="bb26d-110">Средство слияния выхода</span><span class="sxs-lookup"><span data-stu-id="bb26d-110">Output Merger</span></span>  | <span data-ttu-id="bb26d-111">[**D3D11 \_ Desc \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) и [ **D3D11 \_ \_ набор элементов \_ глубины**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="bb26d-111">[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) and [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span> |
| <span data-ttu-id="bb26d-112">Шейдеры</span><span class="sxs-lookup"><span data-stu-id="bb26d-112">Shaders</span></span>        | <span data-ttu-id="bb26d-113">См. ниже</span><span class="sxs-lookup"><span data-stu-id="bb26d-113">See below</span></span>                                                                                                          |



 

<span data-ttu-id="bb26d-114">Для этапов шейдера, где число изменений состояния должно быть более управляемым приложением, состояние делится на постоянное состояние буфера, состояние выборки, состояние ресурса шейдера и неупорядоченное состояние представления доступа (для шейдеров пикселей и вычислений).</span><span class="sxs-lookup"><span data-stu-id="bb26d-114">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, shader resource state, and unordered access view state (for pixel and compute shaders).</span></span> <span data-ttu-id="bb26d-115">Это позволяет приложению, которое тщательно спроектировано для обновления только изменяемого состояния, что повышает производительность за счет уменьшения объема данных, которые необходимо передать в GPU.</span><span class="sxs-lookup"><span data-stu-id="bb26d-115">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="bb26d-116">Так как же вы организуете состояние конвейера в результате?</span><span class="sxs-lookup"><span data-stu-id="bb26d-116">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="bb26d-117">Ответ заключается в том, что порядок не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="bb26d-117">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="bb26d-118">В верхней части не нужно размещать глобальные переменные.</span><span class="sxs-lookup"><span data-stu-id="bb26d-118">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="bb26d-119">Тем не менее, все примеры в пакете SDK выполняются в том же порядке, что и оптимальный способ организации данных.</span><span class="sxs-lookup"><span data-stu-id="bb26d-119">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="bb26d-120">Это краткое описание порядка данных в примерах пакета SDK для DirectX.</span><span class="sxs-lookup"><span data-stu-id="bb26d-120">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="bb26d-121">Глобальные переменные</span><span class="sxs-lookup"><span data-stu-id="bb26d-121">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="bb26d-122">Шейдеры</span><span class="sxs-lookup"><span data-stu-id="bb26d-122">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="bb26d-123">Группы, методики и проходы</span><span class="sxs-lookup"><span data-stu-id="bb26d-123">Groups, Techniques, and Passes</span></span>](#groups-techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="bb26d-124">Глобальные переменные</span><span class="sxs-lookup"><span data-stu-id="bb26d-124">Global Variables</span></span>

<span data-ttu-id="bb26d-125">Как и в случае со стандартной практикой C, глобальные переменные объявляются первыми в начале файла.</span><span class="sxs-lookup"><span data-stu-id="bb26d-125">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="bb26d-126">Чаще всего это переменные, которые будут инициализированы приложением, а затем используются в результате.</span><span class="sxs-lookup"><span data-stu-id="bb26d-126">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="bb26d-127">Иногда они инициализируются и никогда не изменяются. в других случаях они обновляются в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="bb26d-127">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="bb26d-128">Как и в случае с областью видимости функции C, переменные эффектов, объявленные за пределами области функций эффектов, видимы по всему результату. Любая переменная, объявленная внутри функции Effect, видна только внутри этой функции.</span><span class="sxs-lookup"><span data-stu-id="bb26d-128">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="bb26d-129">Ниже приведен пример переменных, объявленных в BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="bb26d-129">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


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



<span data-ttu-id="bb26d-130">Синтаксис переменных эффектов более подробно описан в [синтаксисе переменных эффектов (Direct3D 11)](d3d11-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="bb26d-130">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 11)](d3d11-effect-variable-syntax.md).</span></span> <span data-ttu-id="bb26d-131">Синтаксис для выборок текстурной текстуры более подробно описан в [типе образца (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="bb26d-131">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

## <a name="shaders"></a><span data-ttu-id="bb26d-132">Шейдеры</span><span class="sxs-lookup"><span data-stu-id="bb26d-132">Shaders</span></span>

<span data-ttu-id="bb26d-133">Шейдеры — это небольшие исполняемые программы.</span><span class="sxs-lookup"><span data-stu-id="bb26d-133">Shaders are small executable programs.</span></span> <span data-ttu-id="bb26d-134">Шейдеры можно представить как инкапсулированное состояние шейдера, так как код HLSL реализует функцию шейдера.</span><span class="sxs-lookup"><span data-stu-id="bb26d-134">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="bb26d-135">Графический конвейер графики до пяти различных видов шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bb26d-135">The graphics pipeline up to five different kinds of shaders.</span></span>

-   <span data-ttu-id="bb26d-136">Шейдеры вершин — работают с данными вершин.</span><span class="sxs-lookup"><span data-stu-id="bb26d-136">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="bb26d-137">Одна вершина в выдает одну вершину.</span><span class="sxs-lookup"><span data-stu-id="bb26d-137">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="bb26d-138">Шейдеры поверхности — работа с данными исправления.</span><span class="sxs-lookup"><span data-stu-id="bb26d-138">Hull shaders - Operate on patch data.</span></span> <span data-ttu-id="bb26d-139">Этап контрольной точки: один вызов дает одну контрольную точку; Для каждого этапа разветвления и объединения: одно исправление дает некоторый объем данных с постоянным исправлением.</span><span class="sxs-lookup"><span data-stu-id="bb26d-139">Control Point Phase: one invocation yields one control point; For each Fork and Join Phases: one patch yields some amount of patch constant data.</span></span>
-   <span data-ttu-id="bb26d-140">Шейдеры домена — работают с примитивными данными.</span><span class="sxs-lookup"><span data-stu-id="bb26d-140">Domain shaders - Operate on primitive data.</span></span> <span data-ttu-id="bb26d-141">Один примитив может возвращать 0, 1 или многие примитивы.</span><span class="sxs-lookup"><span data-stu-id="bb26d-141">One primitive may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="bb26d-142">Шейдеры Geometry — работают с примитивными данными.</span><span class="sxs-lookup"><span data-stu-id="bb26d-142">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="bb26d-143">Один примитив в может возвращать 0, 1 или многие примитивы.</span><span class="sxs-lookup"><span data-stu-id="bb26d-143">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="bb26d-144">Шейдеры пикселей — работают с данными пикселей.</span><span class="sxs-lookup"><span data-stu-id="bb26d-144">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="bb26d-145">Один пиксель в выдает 1 пиксель (если только пиксел не исключается из отрисовки).</span><span class="sxs-lookup"><span data-stu-id="bb26d-145">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="bb26d-146">В конвейере COMPUTE Shader используется один шейдер:</span><span class="sxs-lookup"><span data-stu-id="bb26d-146">The compute shader pipeline uses one shader:</span></span>

-   <span data-ttu-id="bb26d-147">Шейдеры вычислений — работают с любым видом данных.</span><span class="sxs-lookup"><span data-stu-id="bb26d-147">Compute shaders - Operate on any kind of data.</span></span> <span data-ttu-id="bb26d-148">Выходные данные не зависят от числа потоков.</span><span class="sxs-lookup"><span data-stu-id="bb26d-148">The output is independent of the number of threads.</span></span>

<span data-ttu-id="bb26d-149">Шейдеры являются локальными функциями и следуют правилам функций в стиле языка C.</span><span class="sxs-lookup"><span data-stu-id="bb26d-149">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="bb26d-150">При компиляции результата каждый из них компилируется, а указатель на каждую функцию шейдера хранится внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="bb26d-150">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="bb26d-151">При успешном завершении компиляции возвращается интерфейс ID3D11Effect.</span><span class="sxs-lookup"><span data-stu-id="bb26d-151">An ID3D11Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="bb26d-152">На этом этапе скомпилированный результат имеет промежуточный формат.</span><span class="sxs-lookup"><span data-stu-id="bb26d-152">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="bb26d-153">Чтобы получить дополнительные сведения о скомпилированных шейдерах, необходимо использовать отражение шейдера.</span><span class="sxs-lookup"><span data-stu-id="bb26d-153">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="bb26d-154">Это, по сути, запрос среды выполнения декомпиляции шейдеров и возвращения информации о коде шейдера.</span><span class="sxs-lookup"><span data-stu-id="bb26d-154">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


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



<span data-ttu-id="bb26d-155">Синтаксис шейдеров эффектов более подробно описан в синтаксисе функции, выполняя [функцию Effect (Direct3D 11)](d3d11-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="bb26d-155">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 11)](d3d11-effect-function-syntax.md).</span></span>

## <a name="groups-techniques-and-passes"></a><span data-ttu-id="bb26d-156">Группы, методики и проходы</span><span class="sxs-lookup"><span data-stu-id="bb26d-156">Groups, Techniques, and Passes</span></span>

<span data-ttu-id="bb26d-157">Группа — это набор методов.</span><span class="sxs-lookup"><span data-stu-id="bb26d-157">A group is a collection of techniques.</span></span> <span data-ttu-id="bb26d-158">Метод — это набор этапов отрисовки (должен быть хотя бы один проход).</span><span class="sxs-lookup"><span data-stu-id="bb26d-158">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="bb26d-159">Каждый пройденный результат (аналогичный в области до одного прохода в цикле подготовки к просмотру) определяет состояние шейдера и любое другое состояние конвейера, необходимое для визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="bb26d-159">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="bb26d-160">Группы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="bb26d-160">Groups are optional.</span></span> <span data-ttu-id="bb26d-161">Существует одна неименованная группа, охватывающая все глобальные методы.</span><span class="sxs-lookup"><span data-stu-id="bb26d-161">There is a single, unnamed group which encompasses all global techniques.</span></span> <span data-ttu-id="bb26d-162">Все остальные группы должны иметь имя.</span><span class="sxs-lookup"><span data-stu-id="bb26d-162">All other groups must be named.</span></span>

<span data-ttu-id="bb26d-163">Ниже приведен пример одного метода (который включает один проход) из BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="bb26d-163">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


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

fxgroup g0
{
    technique11 RunComputeShader
    {
        pass P0
        {
            SetComputeShader( CompileShader( cs_5_0, CS() ) );
        }
    }
}

```



<span data-ttu-id="bb26d-164">Синтаксис шейдеров эффектов более подробно описан в [синтаксисе методики влияния (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="bb26d-164">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb26d-165">См. также</span><span class="sxs-lookup"><span data-stu-id="bb26d-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb26d-166">Эффекты (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="bb26d-166">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 