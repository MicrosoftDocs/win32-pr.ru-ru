---
description: Режим заливки, используемый для отрисовки многоугольника, имеет более глубокое воздействие на его внешний вид. Режимы заливки определяют интенсивность цвета и освещения в любой точке многоугольника. Direct3D поддерживает два режима заливки.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Режимы заливки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566504"
---
# <a name="shading-modes-direct3d-9"></a><span data-ttu-id="dd819-105">Режимы заливки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dd819-105">Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="dd819-106">Режим заливки, используемый для отрисовки многоугольника, имеет более глубокое воздействие на его внешний вид.</span><span class="sxs-lookup"><span data-stu-id="dd819-106">The shading mode used to render a polygon has a profound effect on its appearance.</span></span> <span data-ttu-id="dd819-107">Режимы заливки определяют интенсивность цвета и освещения в любой точке многоугольника.</span><span class="sxs-lookup"><span data-stu-id="dd819-107">Shading modes determine the intensity of color and lighting at any point on a polygon face.</span></span> <span data-ttu-id="dd819-108">Direct3D поддерживает два режима заливки.</span><span class="sxs-lookup"><span data-stu-id="dd819-108">Direct3D supports two shading modes.</span></span>

-   [<span data-ttu-id="dd819-109">Плоская заливка</span><span class="sxs-lookup"><span data-stu-id="dd819-109">Flat Shading</span></span>](#flat-shading)
-   [<span data-ttu-id="dd819-110">Заливка по методу Гуро</span><span class="sxs-lookup"><span data-stu-id="dd819-110">Gouraud Shading</span></span>](#gouraud-shading)

## <a name="flat-shading"></a><span data-ttu-id="dd819-111">Плоская заливка</span><span class="sxs-lookup"><span data-stu-id="dd819-111">Flat Shading</span></span>

<span data-ttu-id="dd819-112">В режиме плоской заливки конвейер визуализации Direct3D Визуализирует многоугольник, используя цвет материала многоугольника на первой вершине в качестве цвета для всего многоугольника.</span><span class="sxs-lookup"><span data-stu-id="dd819-112">In the flat shading mode, the Direct3D rendering pipeline renders a polygon, using the color of the polygon material at its first vertex as the color for the entire polygon.</span></span> <span data-ttu-id="dd819-113">Трехмерные объекты, отображаемые с плоской заливкой, имеют четкие края многоугольников, если они не копланар.</span><span class="sxs-lookup"><span data-stu-id="dd819-113">3D objects that are rendered with flat shading have visibly sharp edges between polygons if they are not coplanar.</span></span>

<span data-ttu-id="dd819-114">На следующем рисунке показан чайник, отображаемый с плоской заливкой.</span><span class="sxs-lookup"><span data-stu-id="dd819-114">The following illustration shows a teapot rendered with flat shading.</span></span> <span data-ttu-id="dd819-115">Контур каждого многоугольника четко виден.</span><span class="sxs-lookup"><span data-stu-id="dd819-115">The outline of each polygon is clearly visible.</span></span> <span data-ttu-id="dd819-116">Плоская заливка — это самая быстрая форма заливки.</span><span class="sxs-lookup"><span data-stu-id="dd819-116">Flat shading is the fastest form of shading.</span></span>

![Иллюстрация чайник с помощью плоской заливки](images/flattea.png)

## <a name="gouraud-shading"></a><span data-ttu-id="dd819-118">Заливка по методу Гуро</span><span class="sxs-lookup"><span data-stu-id="dd819-118">Gouraud Shading</span></span>

<span data-ttu-id="dd819-119">Когда Direct3D Визуализирует многоугольник с помощью заливки по методу Гуро, он выдает цвет для каждой вершины с помощью параметров нормали и освещения вершин.</span><span class="sxs-lookup"><span data-stu-id="dd819-119">When Direct3D renders a polygon using Gouraud shading, it computes a color for each vertex by using the vertex normal and lighting parameters.</span></span> <span data-ttu-id="dd819-120">Затем выполняется интерполяция цвета по грани многоугольников, которые выполняются линейно.</span><span class="sxs-lookup"><span data-stu-id="dd819-120">Then, it interpolates the color across the face of the polygons The interpolation is done linearly.</span></span> <span data-ttu-id="dd819-121">Например, если красный компонент цвета вершины 1 — 0,8, а красный компонент вершины 2 — 0,4 с использованием режима заливки Гуро и цветовой модели RGB, модуль освещения Direct3D присваивает красному компоненту 0,6 точку в средней точке линии между этими вершинами.</span><span class="sxs-lookup"><span data-stu-id="dd819-121">For example, if the red component of the color of vertex 1 is 0.8 and the red component of vertex 2 is 0.4, using the Gouraud shading mode and the RGB color model, the Direct3D lighting module assigns a red component of 0.6 to the pixel at the midpoint of the line between these vertices.</span></span>

<span data-ttu-id="dd819-122">На следующем рисунке показана заливка по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="dd819-122">The following illustration demonstrates Gouraud shading.</span></span> <span data-ttu-id="dd819-123">Этот чайник состоит из множества плоских треугольных многоугольников.</span><span class="sxs-lookup"><span data-stu-id="dd819-123">This teapot is composed of many flat, triangular polygons.</span></span> <span data-ttu-id="dd819-124">Однако заливка по методу Гуро делает поверхность объекта изогнутой и гладкой.</span><span class="sxs-lookup"><span data-stu-id="dd819-124">However, Gouraud shading makes the surface of the object appear curved and smooth.</span></span>

![Иллюстрация чайник с помощью заливки по методу Гуро](images/gourtea.png)

<span data-ttu-id="dd819-126">Заливка по методу Гуро также может использоваться для вывода объектов с четкими краями.</span><span class="sxs-lookup"><span data-stu-id="dd819-126">Gouraud shading can also be used to display objects with sharp edges.</span></span>

<span data-ttu-id="dd819-127">Дополнительные сведения см. в разделе [векторы нормали граней и вершин (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="dd819-127">For more information, see [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd819-128">См. также</span><span class="sxs-lookup"><span data-stu-id="dd819-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd819-129">Заливка</span><span class="sxs-lookup"><span data-stu-id="dd819-129">Shading</span></span>](shading.md)
</dt> </dl>

 

 



