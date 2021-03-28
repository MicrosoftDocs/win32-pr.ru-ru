---
title: Примитивные топологии
description: Direct3D 10 и более поздние версии поддерживают несколько типов-примитивов (или топологий), которые представлены \_ \_ перечисляемым типом топологии примитивов D3D. Эти типы определяют, как вершины обрабатываются и визуализируются в конвейере.
ms.assetid: 357ad085-fd91-4420-abc3-1c57e8cbb517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e83f901d4d91d01a3cffedddb343fde7b50c20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337585"
---
# <a name="primitive-topologies"></a><span data-ttu-id="bd8fb-104">Примитивные топологии</span><span class="sxs-lookup"><span data-stu-id="bd8fb-104">Primitive Topologies</span></span>

<span data-ttu-id="bd8fb-105">Direct3D 10 и более поздние версии поддерживают несколько типов-примитивов (или топологий), которые представлены перечисляемым типом [**\_ \_ топологии примитивов D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) .</span><span class="sxs-lookup"><span data-stu-id="bd8fb-105">Direct3D 10 and higher supports several primitive types (or topologies) that are represented by the [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) enumerated type.</span></span> <span data-ttu-id="bd8fb-106">Эти типы определяют, как вершины обрабатываются и визуализируются в конвейере.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-106">These types define how vertices are interpreted and rendered by the pipeline.</span></span>

-   [<span data-ttu-id="bd8fb-107">Основные простые типы</span><span class="sxs-lookup"><span data-stu-id="bd8fb-107">Basic Primitive Types</span></span>](#basic-primitive-types)
-   [<span data-ttu-id="bd8fb-108">Элементарное соседство</span><span class="sxs-lookup"><span data-stu-id="bd8fb-108">Primitive Adjacency</span></span>](#primitive-adjacency)
-   [<span data-ttu-id="bd8fb-109">Направление поворота и начальные положения вершины</span><span class="sxs-lookup"><span data-stu-id="bd8fb-109">Winding Direction and Leading Vertex Positions</span></span>](#winding-direction-and-leading-vertex-positions)
-   [<span data-ttu-id="bd8fb-110">Создание нескольких полос</span><span class="sxs-lookup"><span data-stu-id="bd8fb-110">Generating Multiple Strips</span></span>](#generating-multiple-strips)
-   [<span data-ttu-id="bd8fb-111">См. также</span><span class="sxs-lookup"><span data-stu-id="bd8fb-111">Related topics</span></span>](#related-topics)

## <a name="basic-primitive-types"></a><span data-ttu-id="bd8fb-112">Основные простые типы</span><span class="sxs-lookup"><span data-stu-id="bd8fb-112">Basic Primitive Types</span></span>

<span data-ttu-id="bd8fb-113">Поддерживаются следующие базовые типы-примитивы:</span><span class="sxs-lookup"><span data-stu-id="bd8fb-113">The following basic primitive types are supported:</span></span>

-   [<span data-ttu-id="bd8fb-114">Список точек</span><span class="sxs-lookup"><span data-stu-id="bd8fb-114">Point List</span></span>](/windows/desktop/direct3d9/point-lists)
-   [<span data-ttu-id="bd8fb-115">Список строк</span><span class="sxs-lookup"><span data-stu-id="bd8fb-115">Line List</span></span>](/windows/desktop/direct3d9/line-lists)
-   [<span data-ttu-id="bd8fb-116">Полоса строк</span><span class="sxs-lookup"><span data-stu-id="bd8fb-116">Line Strip</span></span>](/windows/desktop/direct3d9/line-strips)
-   [<span data-ttu-id="bd8fb-117">Список треугольников</span><span class="sxs-lookup"><span data-stu-id="bd8fb-117">Triangle List</span></span>](/windows/desktop/direct3d9/triangle-lists)
-   [<span data-ttu-id="bd8fb-118">Полоса трианже</span><span class="sxs-lookup"><span data-stu-id="bd8fb-118">Triange Strip</span></span>](/windows/desktop/direct3d9/triangle-strips)

<span data-ttu-id="bd8fb-119">Для визуализации каждого типа-примитива см. схему далее в этом разделе в [направлении поворота и начальных позициях вершин](#winding-direction-and-leading-vertex-positions).</span><span class="sxs-lookup"><span data-stu-id="bd8fb-119">For a visualization of each primitive type, see the diagram later in this topic in [Winding Direction and Leading Vertex Positions](#winding-direction-and-leading-vertex-positions).</span></span>

<span data-ttu-id="bd8fb-120">Этап входного ассемблера считывает данные из буферов вершин и индексов, собирает данные в эти примитивы, а затем отправляет данные на остальные этапы конвейера.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-120">The input-assembler stage reads data from vertex and index buffers, assembles the data into these primitives, and then sends the data to the remaining pipeline stages.</span></span> <span data-ttu-id="bd8fb-121">(Можно использовать метод [**ссылку ID3D11DeviceContext:: иасетпримитиветопологи**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) , чтобы указать тип-примитив для этапа входного ассемблера.)</span><span class="sxs-lookup"><span data-stu-id="bd8fb-121">(You can use the [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) method to specify the primitive type for the input-assembler stage.)</span></span>

## <a name="primitive-adjacency"></a><span data-ttu-id="bd8fb-122">Элементарное соседство</span><span class="sxs-lookup"><span data-stu-id="bd8fb-122">Primitive Adjacency</span></span>

<span data-ttu-id="bd8fb-123">Все типы-примитивы Direct3D 10 и выше (за исключением списка точек) доступны в двух версиях: один примитивный тип с соседией и один примитивный тип без соседства.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-123">All Direct3D 10 and higher primitive types (except the point list) are available in two versions: one primitive type with adjacency and one primitive type without adjacency.</span></span> <span data-ttu-id="bd8fb-124">Примитивы с соседством содержат некоторые окружающие вершин, а примитивы без соседство содержат только вершины целевого примитива.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-124">Primitives with adjacency contain some of the surrounding vertices, while primitives without adjacency contain only the vertices of the target primitive.</span></span> <span data-ttu-id="bd8fb-125">Например, примитив списка линий (представленный значением линелист для **\_ топологии- \_ \_ примитива D3D** ) имеет соответствующий примитив списка линий, включающий соседство (представленное **значением \_ \_ \_ \_ года линелистной топологии D3D** ).</span><span class="sxs-lookup"><span data-stu-id="bd8fb-125">For example, the line list primitive (represented by the **D3D\_PRIMITIVE\_TOPOLOGY\_LINELIST** value) has a corresponding line list primitive that includes adjacency (represented by the **D3D\_PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ** value.)</span></span>

<span data-ttu-id="bd8fb-126">Соседние примитивы предоставляют дополнительные сведения о геометрии и видны только через шейдер геометрии.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-126">Adjacent primitives are intended to provide more information about your geometry and are only visible through a geometry shader.</span></span> <span data-ttu-id="bd8fb-127">Соседство полезно для шейдеров геометрии, которые используются обнаружение силуэтов, экструзию теневых объемов и т. д.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-127">Adjacency is useful for geometry shaders that use silhouette detection, shadow volume extrusion, and so on.</span></span>

<span data-ttu-id="bd8fb-128">Например, предположим, что вы хотите нарисовать список треугольников с соседством.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-128">For example, suppose you want to draw a triangle list with adjacency.</span></span> <span data-ttu-id="bd8fb-129">Список треугольников, содержащий 36 вершин (с соседством), даст 6 завершенных примитивов.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-129">A triangle list that contains 36 vertices (with adjacency) will yield 6 completed primitives.</span></span> <span data-ttu-id="bd8fb-130">Примитивы с соседством (за исключением ломаных) содержат ровно два раза больше вершин, чем эквивалентный примитив без соседства, где каждая дополнительная вершина является соседней.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-130">Primitives with adjacency (except line strips) contain exactly twice as many vertices as the equivalent primitive without adjacency, where each additional vertex is an adjacent vertex.</span></span>

## <a name="winding-direction-and-leading-vertex-positions"></a><span data-ttu-id="bd8fb-131">Направление поворота и начальные положения вершины</span><span class="sxs-lookup"><span data-stu-id="bd8fb-131">Winding Direction and Leading Vertex Positions</span></span>

<span data-ttu-id="bd8fb-132">Как показано на следующем рисунке, передняя вершина — это первая несмежная вершина в примитиве.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-132">As shown in the following illustration, a leading vertex is the first non-adjacent vertex in a primitive.</span></span> <span data-ttu-id="bd8fb-133">Для типа примитива может быть задано несколько начальных вершин, если каждая из них используется для различных примитивов.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-133">A primitive type can have multiple leading vertices defined, as long as each one is used for a different primitive.</span></span> <span data-ttu-id="bd8fb-134">Для полосы треугольников с соседством передние вершины — это 0, 2, 4, 6 и т. д.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-134">For a triangle strip with adjacency, the leading vertices are 0, 2, 4, 6, and so on.</span></span> <span data-ttu-id="bd8fb-135">Для ломаной с соседством передние вершины — 1, 2, 3 и т. д.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-135">For a line strip with adjacency, the leading vertices are 1, 2, 3, and so on.</span></span> <span data-ttu-id="bd8fb-136">С другой стороны у соседнего примитива нет передних вершин.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-136">An adjacent primitive, on the other hand, has no leading vertex.</span></span>

<span data-ttu-id="bd8fb-137">На следующем рисунке показан порядок вершин для всех типов примитивов, которые может получить сборщик входных данных.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-137">The following illustration shows the vertex ordering for all of the primitive types that the input assembler can produce.</span></span>

![схема порядка вершин для типов примитивов](images/d3d10-primitive-topologies.png)

<span data-ttu-id="bd8fb-139">В следующей таблице описаны символы, использованные в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-139">The symbols in the preceding illustration are described in the following table.</span></span>



| <span data-ttu-id="bd8fb-140">Символ</span><span class="sxs-lookup"><span data-stu-id="bd8fb-140">Symbol</span></span>                                                                                   | <span data-ttu-id="bd8fb-141">name</span><span class="sxs-lookup"><span data-stu-id="bd8fb-141">Name</span></span>              | <span data-ttu-id="bd8fb-142">Описание</span><span class="sxs-lookup"><span data-stu-id="bd8fb-142">Description</span></span>                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![символ вершины](images/d3d10-primitive-topologies-vertex.png)                     | <span data-ttu-id="bd8fb-144">Вершина</span><span class="sxs-lookup"><span data-stu-id="bd8fb-144">Vertex</span></span>            | <span data-ttu-id="bd8fb-145">Точка в трехмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-145">A point in 3D space.</span></span>                                                                                                                                                                               |
| ![символ направления поворота](images/d3d10-primitive-topologies-winding-direction.png) | <span data-ttu-id="bd8fb-147">Направление поворота</span><span class="sxs-lookup"><span data-stu-id="bd8fb-147">Winding Direction</span></span> | <span data-ttu-id="bd8fb-148">Порядок вершин при сборке примитива.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-148">The vertex order when assembling a primitive.</span></span> <span data-ttu-id="bd8fb-149">Может быть по часовой стрелке или против часовой стрелки; Укажите это путем вызова [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1).</span><span class="sxs-lookup"><span data-stu-id="bd8fb-149">Can be clockwise or counterclockwise; specify this by calling [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1).</span></span> |
| ![символ передней вершины](images/d3d10-primitive-topologies-leading-vertex.png)       | <span data-ttu-id="bd8fb-151">Передняя вершина</span><span class="sxs-lookup"><span data-stu-id="bd8fb-151">Leading Vertex</span></span>    | <span data-ttu-id="bd8fb-152">Первая несмежная вершина в примитиве, содержащем данные констант.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-152">The first non-adjacent vertex in a primitive that contains per-constant data.</span></span>                                                                                                                      |



 

## <a name="generating-multiple-strips"></a><span data-ttu-id="bd8fb-153">Создание нескольких полос</span><span class="sxs-lookup"><span data-stu-id="bd8fb-153">Generating Multiple Strips</span></span>

<span data-ttu-id="bd8fb-154">Вы можете создать несколько полос с помощью вырезания полос.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-154">You can generate multiple strips through strip cutting.</span></span> <span data-ttu-id="bd8fb-155">Вы можете вырезать полосы, явно вызвав HLSL-функцию [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) или вставив специальное значение индекса в буфер индексов.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-155">You can perform a strip cut by explicitly calling the [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL function, or by inserting a special index value into the index buffer.</span></span> <span data-ttu-id="bd8fb-156">Это значение –1, т. е. 0xffffffff для 32-разрядных индексы или 0xffff для 16-разрядные индексов.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-156">This value is –1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices.</span></span> <span data-ttu-id="bd8fb-157">Индекс –1 указывает на явное «вырезание» или «перезапуск» текущей полосы.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-157">An index of –1 indicates an explicit 'cut' or 'restart' of the current strip.</span></span> <span data-ttu-id="bd8fb-158">Предыдущий индекс завершает предыдущий примитив или полосу, а следующий индекс начинает новый примитив или полосу.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-158">The previous index completes the previous primitive or strip and the next index starts a new primitive or strip.</span></span> <span data-ttu-id="bd8fb-159">Дополнительные сведения о создании нескольких полос см. в разделе [этап шейдера Geometry](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bd8fb-159">For more info about generating multiple strips, see [Geometry-Shader Stage](/previous-versions//bb205146(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="bd8fb-160">Требуется [уровень компонентов](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 или выше, так как не все 10level9 оборудование реализует эту функцию.</span><span class="sxs-lookup"><span data-stu-id="bd8fb-160">You need [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 or higher hardware because not all 10level9 hardware implements this functionality.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bd8fb-161">См. также</span><span class="sxs-lookup"><span data-stu-id="bd8fb-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd8fb-162">Начало работы с этапом Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="bd8fb-162">Getting Started with the Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> <dt>

[<span data-ttu-id="bd8fb-163">Этапы конвейера (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bd8fb-163">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 