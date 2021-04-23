---
title: Этап растеризации
description: На этапе средства программной прорисовки векторные данные (состоящие из фигур или примитивов) преобразуются в растровое изображение (состоящее из пикселей) для отображения трехмерной графики в режиме реального времени.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988017"
---
# <a name="rasterizer-stage"></a><span data-ttu-id="bfbb0-103">Этап растеризации</span><span class="sxs-lookup"><span data-stu-id="bfbb0-103">Rasterizer Stage</span></span>

<span data-ttu-id="bfbb0-104">На этапе средства программной прорисовки векторные данные (состоящие из фигур или примитивов) преобразуются в растровое изображение (состоящее из пикселей) для отображения трехмерной графики в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-104">The rasterization stage converts vector information (composed of shapes or primitives) into a raster image (composed of pixels) for the purpose of displaying real-time 3D graphics.</span></span>

<span data-ttu-id="bfbb0-105">Во время растеризации каждый примитив преобразуется в пиксели, а значения для вершин интерполируются для каждого примитива.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-105">During rasterization, each primitive is converted into pixels, while interpolating per-vertex values across each primitive.</span></span> <span data-ttu-id="bfbb0-106">Растеризация заключается в обрезке вершин в усеченной пирамиде обзора за счет деления на z для получения перспективы, сопоставления примитивов с двухмерным окном просмотра и определением способа вызова шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-106">Rasterization includes clipping vertices to the view frustum, performing a divide by z to provide perspective, mapping primitives to a 2D viewport, and determining how to invoke the pixel shader.</span></span> <span data-ttu-id="bfbb0-107">Хотя использовать шейдер пикселей необязательно, на этапе средства программной прорисовки всегда выполняется обрезка, деление перспективы для преобразования точек в однородное пространство и сопоставление вершин с окном просмотра.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-107">While using a pixel shader is optional, the rasterizer stage always performs clipping, a perspective divide to transform the points into homogeneous space, and maps the vertices to the viewport.</span></span>

<span data-ttu-id="bfbb0-108">Вершины (x, y, z, w), поступающие на стадию средства прорисовки, предполагаются в однородном пространстве.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-108">Vertices (x,y,z,w), coming into the rasterizer stage are assumed to be in homogeneous clip-space.</span></span> <span data-ttu-id="bfbb0-109">В этом пространстве координат точки оси X указывают вправо, точки Y — вверх, а точки Z — по направлению от камеры.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-109">In this coordinate space the X axis points right, Y points up and Z points away from camera.</span></span>

<span data-ttu-id="bfbb0-110">Вы можете отключить растрирование, указав конвейеру, что он не имеет построителя текстуры (задайте для этапа шейдера пикселей **значение NULL** с помощью [**ссылку ID3D11DeviceContext::P ссетшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) и отключите тестирование глубины и трафарета (установите **Депсенабле** и **стенЦиленабле** в **значение false** в [**\_ \_ наборе элементов \_ глубины D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span><span class="sxs-lookup"><span data-stu-id="bfbb0-110">You may disable rasterization by telling the pipeline there is no pixel shader (set the pixel shader stage to **NULL** with [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)), and disabling depth and stencil testing (set **DepthEnable** and **StencilEnable** to **FALSE** in [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span> <span data-ttu-id="bfbb0-111">После отключения не будут обновляться связанные с растеризацией счетчики конвейера.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-111">While disabled, rasterization-related pipeline counters will not update.</span></span> <span data-ttu-id="bfbb0-112">Также имеется полное описание [правил растрирования](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span><span class="sxs-lookup"><span data-stu-id="bfbb0-112">There is also a complete description of the [rasterization rules](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span></span>

<span data-ttu-id="bfbb0-113">На оборудовании, реализующем иерархическую оптимизацию Z-буферов, можно включить предварительную загрузку z-буфера, установив для этапа шейдера пикселей **значение NULL** при включенном тестировании глубины и трафарета.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-113">On hardware that implements hierarchical Z-buffer optimizations, you may enable preloading the z-buffer by setting the pixel shader stage to **NULL** while enabling depth and stencil testing.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="bfbb0-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="bfbb0-114">In this section</span></span>



| <span data-ttu-id="bfbb0-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="bfbb0-115">Topic</span></span>                                                                                                                         | <span data-ttu-id="bfbb0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="bfbb0-116">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfbb0-117">начало работы с этапом средства прорисовки</span><span class="sxs-lookup"><span data-stu-id="bfbb0-117">Getting Started with the Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | <span data-ttu-id="bfbb0-118">В этом разделе описывается настройка окна просмотра, прямоугольника ножниц, состояния средства прорисовки и множественная выборка.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-118">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="bfbb0-119">Правила растрирования</span><span class="sxs-lookup"><span data-stu-id="bfbb0-119">Rasterization Rules</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | <span data-ttu-id="bfbb0-120">Правила растеризации определяют, как векторные данные сопоставляются с растровыми.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-120">Rasterization rules define how vector data is mapped into raster data.</span></span> <span data-ttu-id="bfbb0-121">Растровые данные прикрепляются в целочисленные расположения, которые затем сортируются и обрезаются (так, чтобы рисовать минимальное число пикселей), а атрибуты отдельных пикселей интерполируются (от атрибутов отдельных вершин), прежде чем будут переданы в построитель текстуры.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-121">The raster data is snapped to integer locations that are then culled and clipped (to draw the minimum number of pixels), and per-pixel attributes are interpolated (from per-vertex attributes) before being passed to a pixel shader.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="bfbb0-122">См. также</span><span class="sxs-lookup"><span data-stu-id="bfbb0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfbb0-123">Графический конвейер</span><span class="sxs-lookup"><span data-stu-id="bfbb0-123">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="bfbb0-124">Этапы конвейера (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bfbb0-124">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

