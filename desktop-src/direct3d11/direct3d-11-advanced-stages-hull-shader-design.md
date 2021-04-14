---
title: Создание шейдера поверхности
description: В этом разделе показано, как спроектировать поверхности шейдер.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997055"
---
# <a name="how-to-design-a-hull-shader"></a><span data-ttu-id="ad7c7-103">Руководство. Проектирование шейдера поверхности</span><span class="sxs-lookup"><span data-stu-id="ad7c7-103">How To: Design a Hull Shader</span></span>

<span data-ttu-id="ad7c7-104">Шейдер поверхности — это первый из трех этапов, которые работают вместе для реализации [тесселяции](direct3d-11-advanced-stages-tessellation.md) (два других этапа — тесселяция и Шейдер доменов).</span><span class="sxs-lookup"><span data-stu-id="ad7c7-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md) (the other two stages are the tessellator and a domain shader).</span></span> <span data-ttu-id="ad7c7-105">В этом разделе показано, как спроектировать поверхности шейдер.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-105">This topics shows how to design a hull shader.</span></span>

<span data-ttu-id="ad7c7-106">Шейдер поверхности требует наличия двух функций: основного шейдера поверхности и функции константы patch.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-106">A hull shader requires two functions, the main hull shader and a patch constant function.</span></span> <span data-ttu-id="ad7c7-107">Шейдер поверхности реализует вычисления для каждой контрольной точки; Шейдер поверхности также вызывает функцию константы Patch, которая реализует вычисления для каждого исправления.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-107">The hull shader implements calculations on each control point; the hull shader also calls the patch constant function which implements calculations on each patch.</span></span>

<span data-ttu-id="ad7c7-108">После создания шейдера поверхности см. раздел [как создать поверхности шейдер](direct3d-11-advanced-stages-hull-shader-create.md) , чтобы узнать, как создать шейдер поверхности.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-108">After you have designed a hull shader, see [How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md) to learn how to create a hull shader.</span></span>

<span data-ttu-id="ad7c7-109">**Разработка шейдера поверхности**</span><span class="sxs-lookup"><span data-stu-id="ad7c7-109">**To design a hull shader**</span></span>

1.  <span data-ttu-id="ad7c7-110">Определите точки управления входными и выходными данными шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-110">Define hull shader input control and output control points.</span></span>

    ```
    // Input control point
    struct VS_CONTROL_POINT_OUTPUT
    {
        float3 vPosition : WORLDPOS;
        float2 vUV       : TEXCOORD0;
        float3 vTangent  : TANGENT;
    };

    // Output control point
    struct BEZIER_CONTROL_POINT
    {
        float3 vPosition    : BEZIERPOS;
    };
    ```

    

2.  <span data-ttu-id="ad7c7-111">Определите постоянные данные выходного исправления.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-111">Define output patch constant data.</span></span>

    ```
    // Output patch constant data.
    struct HS_CONSTANT_DATA_OUTPUT
    {
        float Edges[4]        : SV_TessFactor;
        float Inside[2]       : SV_InsideTessFactor;
        
        float3 vTangent[4]    : TANGENT;
        float2 vUV[4]         : TEXCOORD;
        float3 vTanUCorner[4] : TANUCORNER;
        float3 vTanVCorner[4] : TANVCORNER;
        float4 vCWts          : TANWEIGHTS;
    };
    ```

    

    <span data-ttu-id="ad7c7-112">Для четырехъядерного домена [ОКП \_ тессфактор](/windows/desktop/direct3dhlsl/sv-tessfactor) определяет 4 фактора тесселяции краев (для тесселяции краев), так как для тесселяции фиксированных функций необходимо иметь представление о том, сколько нужно тесселяции.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-112">For a quad domain, [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) defines 4 edge tessellation factors (to tessellate the edges), since the fixed function tessellator needs to know how much to tessellate.</span></span> <span data-ttu-id="ad7c7-113">Необходимые выходные данные отличаются для доменов треугольников и исолине.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-113">The required outputs are different for the triangle and isoline domains.</span></span>

    <span data-ttu-id="ad7c7-114">Фиксированная тесселяция функции не просматривает никакие другие выходные данные шейдера поверхности, такие как другие константы исправления или любые контрольные точки.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-114">The fixed function tessellator doesn't look at any other hull shader outputs, such as other patch constant data or any of the control points.</span></span> <span data-ttu-id="ad7c7-115">Шейдер домена, который вызывается для каждой точки, выдается с помощью предопределенной тесселяции функции, будет видеть все точки управления выходными данными шейдера поверхности и все данные константы выходного исправления. Шейдер оценивает исправление в своем расположении.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-115">The domain shader -- which is invoked for each point the fixed function tessellator generates -- will see as its input all the hull shader's output control points and all the output patch constant data; the shader evaluates the patch at its location.</span></span>

3.  <span data-ttu-id="ad7c7-116">Определите функцию константы patch.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-116">Define a patch constant function.</span></span> <span data-ttu-id="ad7c7-117">Функция константы Patch выполняется один раз для каждого исправления, чтобы вычислить все данные, которые являются постоянными для всего исправления (в отличие от данных точки управления, которые вычисляются в шейдере поверхности).</span><span class="sxs-lookup"><span data-stu-id="ad7c7-117">A patch constant function executes once for each patch to calculate any data that is constant for the entire patch (as opposed to per-control point data, which is computed in the hull shader).</span></span>

    ```
    
    #define MAX_POINTS 32

    // Patch Constant Function
    HS_CONSTANT_DATA_OUTPUT SubDToBezierConstantsHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip,
        uint PatchID : SV_PrimitiveID )
    {   
        HS_CONSTANT_DATA_OUTPUT Output;

        // Insert code to compute Output here
        
        return Output;
    }
    ```

    

    <span data-ttu-id="ad7c7-118">В функцию константы Patch входят следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="ad7c7-118">Properties of the patch constant function include:</span></span>

    -   <span data-ttu-id="ad7c7-119">Один вход указывает переменную, содержащую идентификатор исправления, и определяется системным значением **SV \_ примитивеид** (см. [семантику](../direct3dhlsl/dx-graphics-hlsl-semantics.md) в модели шейдера 4).</span><span class="sxs-lookup"><span data-stu-id="ad7c7-119">One input specifies a variable containing a patch id, and is identified by the **SV\_PrimitiveID** system value (see [semantics](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in shader model 4).</span></span>
    -   <span data-ttu-id="ad7c7-120">Одним входным параметром являются контрольные точки ввода, объявленные в **\_ \_ \_ выходных данных точки управления VS** в этом примере.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-120">One input parameter is the input control points, declared in **VS\_CONTROL\_POINT\_OUTPUT** in this example.</span></span> <span data-ttu-id="ad7c7-121">Функция Patch может видеть все контрольные точки ввода для каждого исправления. в этом примере имеется 32 контрольных точек для каждого исправления.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-121">A patch function can see all the input control points for each patch, there are 32 control points per patch in this example.</span></span>
    -   <span data-ttu-id="ad7c7-122">Как минимум, функция должна рассчитывать факторы тесселяции для каждого исправления для этапа тесселяции, которые определяются с помощью [SV \_ тессфактор](/windows/desktop/direct3dhlsl/sv-tessfactor).</span><span class="sxs-lookup"><span data-stu-id="ad7c7-122">As a minimum, the function must calculate per-patch tessellation factors for the tessellator stage which are identified with [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span></span> <span data-ttu-id="ad7c7-123">Для четырех доменов требуется четыре фактора тесселяции для краев и два дополнительных фактора (обозначены [ОКП \_ инсидетессфактор](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) для тесселяции внутри исправления.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-123">A quad domain requires four tessellation factors for the edges and two additional factors (identified by [SV\_InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) for tessellating the inside of the patch.</span></span> <span data-ttu-id="ad7c7-124">Фиксированная тесселяция функции не просматривает никакие другие выходные данные шейдера поверхности (например, постоянные данные исправления или любые контрольные точки).</span><span class="sxs-lookup"><span data-stu-id="ad7c7-124">The fixed function tessellator doesn't look at any other hull shader outputs (such as the patch constant data or any of the control points).</span></span>
    -   <span data-ttu-id="ad7c7-125">Выходы обычно определяются структурой и определяются с помощью **\_ \_ \_ выходных данных о константах HS** в этом примере; структура зависит от типа домена и будет отличаться для доменов треугольников и исолине.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-125">The outputs are usually defined by a structure and is identified by **HS\_CONSTANT\_DATA\_OUTPUT** in this example; the structure depends on the domain type and would be different for triangle or isoline domains.</span></span>

    <span data-ttu-id="ad7c7-126">Шейдер домена с другой стороны вызывается для каждой точки, создаваемой с помощью предопределенной тесселяции функции, и необходимо просмотреть контрольные точки вывода и данные константы выходного исправления (оба из шейдера поверхности) для вычисления исправления в его расположении.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-126">A domain shader on the other hand is invoked for each point the fixed function tessellator generates and needs to see the output control points and the output patch constant data (both from the hull shader) to evaluate a patch at its location.</span></span>

4.  <span data-ttu-id="ad7c7-127">Определите шейдер поверхности.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-127">Define a hull shader.</span></span> <span data-ttu-id="ad7c7-128">Шейдер поверхности определяет свойства исправления, включая функцию константы patch.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-128">A hull shader identifies the properties of a patch including a patch constant function.</span></span> <span data-ttu-id="ad7c7-129">Шейдер поверхности вызывается один раз для каждой контрольной точки вывода.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-129">A hull shader is invoked once for each output control point.</span></span>

    ```
    [domain("quad")]
    [partitioning("integer")]
    [outputtopology("triangle_cw")]
    [outputcontrolpoints(16)]
    [patchconstantfunc("SubDToBezierConstantsHS")]
    BEZIER_CONTROL_POINT SubDToBezierHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip, 
        uint i : SV_OutputControlPointID,
        uint PatchID : SV_PrimitiveID )
    {
        VS_CONTROL_POINT_OUTPUT Output;

        // Insert code to compute Output here.
        
        return Output;
    }
    ```

    

    <span data-ttu-id="ad7c7-130">Шейдер поверхности использует следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="ad7c7-130">A hull shader uses the following attributes:</span></span>

    -   <span data-ttu-id="ad7c7-131">Атрибут [домена](/windows/desktop/direct3dhlsl/sm5-attributes-domain) .</span><span class="sxs-lookup"><span data-stu-id="ad7c7-131">A [domain](/windows/desktop/direct3dhlsl/sm5-attributes-domain) attribute.</span></span>
    -   <span data-ttu-id="ad7c7-132">Атрибут [секционирования](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) .</span><span class="sxs-lookup"><span data-stu-id="ad7c7-132">A [partitioning](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) attribute.</span></span>
    -   <span data-ttu-id="ad7c7-133">Атрибут [аутпуттопологи](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) .</span><span class="sxs-lookup"><span data-stu-id="ad7c7-133">An [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) attribute.</span></span>
    -   <span data-ttu-id="ad7c7-134">Атрибут [аутпутконтролпоинтс](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) .</span><span class="sxs-lookup"><span data-stu-id="ad7c7-134">An [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) attribute.</span></span>
    -   <span data-ttu-id="ad7c7-135">Атрибут [патчконстантфунк](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) .</span><span class="sxs-lookup"><span data-stu-id="ad7c7-135">A [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) attribute.</span></span> <span data-ttu-id="ad7c7-136">Шейдер поверхности вычисляет контрольные точки вывода, в этом примере есть 16 выходных контрольных точек Безье.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-136">A hull shader calculates output control points, there are 16 output Bezier control points in this example.</span></span>

<span data-ttu-id="ad7c7-137">Все контрольные точки ввода (определяемые **\_ \_ \_ выходными данными точки управления VS**) видимы для каждого вызова шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-137">All the input control points (identified by **VS\_CONTROL\_POINT\_OUTPUT**) are visible to each hull shader invocation.</span></span> <span data-ttu-id="ad7c7-138">В этом примере есть 32 контрольных точек ввода.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-138">In this example, there are 32 input control points.</span></span>

<span data-ttu-id="ad7c7-139">Шейдер поверхности вызывается один раз для каждой контрольной точки вывода (определяется с помощью [SV \_ аутпутконтролпоинтид](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) для каждого исправления (ОПРЕДЕЛЯЕТСЯ с помощью SV \_ примитивеид).</span><span class="sxs-lookup"><span data-stu-id="ad7c7-139">A hull shader is invoked once per output control point (identified with [SV\_OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) for each patch (identified with SV\_PrimitiveID).</span></span> <span data-ttu-id="ad7c7-140">Цель этого конкретного шейдера — вычислить вывод *i*, который был определен как контрольная точка Безье (в этом примере есть 16 контрольных точек вывода, определенных аутпутконтролпоинтс).</span><span class="sxs-lookup"><span data-stu-id="ad7c7-140">The purpose of this particular shader is to calculate output *i*, which was defined to be a BEZIER control point (this example has 16 output control points defined by outputcontrolpoints).</span></span>

<span data-ttu-id="ad7c7-141">Шейдер поверхности выполняет подпрограммы один раз для каждого исправления (функция константы Patch) для расчета данных исправления (в качестве минимального значения).</span><span class="sxs-lookup"><span data-stu-id="ad7c7-141">A hull shader runs a routine once per patch (the patch constant function) to compute patch-constant data (tessellation factors as a minimum).</span></span> <span data-ttu-id="ad7c7-142">По отдельности, шейдер поверхности запускает функцию константы patch (именуемую Субдтобезиерконстантшс) для каждого исправления, чтобы вычислить постоянные данные исправления, такие как факторы тесселяции для этапа тесселяции.</span><span class="sxs-lookup"><span data-stu-id="ad7c7-142">Separately, a hull shader runs a patch constant function (called SubDToBezierConstantsHS) on each patch to compute patch-constant data such as tessellation factors for the tessellator stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad7c7-143">См. также</span><span class="sxs-lookup"><span data-stu-id="ad7c7-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad7c7-144">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ad7c7-144">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="ad7c7-145">Общие сведения об тесселяции</span><span class="sxs-lookup"><span data-stu-id="ad7c7-145">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 