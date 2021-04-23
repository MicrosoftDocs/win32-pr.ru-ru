---
title: Тесселяция многоугольников
description: Тесселяция многоугольников
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Служебная программа OpenGL (GLU), тесселяция
- GLU (служебная программа OpenGL), тесселяция
- Служебная программа OpenGL (GLU), простые многоугольники
- GLU (служебная программа OpenGL), простые многоугольники
- простые многоугольники OpenGL
- Служебная программа OpenGL (GLU), сложные многоугольники
- GLU (служебная программа OpenGL), сложные многоугольники
- сложные многоугольники OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661634"
---
# <a name="tessellating-polygons"></a><span data-ttu-id="a7fa7-111">Тесселяция многоугольников</span><span class="sxs-lookup"><span data-stu-id="a7fa7-111">Tessellating Polygons</span></span>

<span data-ttu-id="a7fa7-112">OpenGL может напрямую отображать только простые многоугольники выпуклой.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-112">OpenGL can directly display only simple convex polygons.</span></span> <span data-ttu-id="a7fa7-113">Многоугольник является простым, если:</span><span class="sxs-lookup"><span data-stu-id="a7fa7-113">A polygon is simple if:</span></span>

-   <span data-ttu-id="a7fa7-114">Грани пересекаются только в вершинах.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-114">The edges intersect only at vertices.</span></span>
-   <span data-ttu-id="a7fa7-115">Нет повторяющихся вершин.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-115">There are no duplicate vertices.</span></span>
-   <span data-ttu-id="a7fa7-116">На любой вершине встречаются ровно два края.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-116">Exactly two edges meet at any vertex.</span></span>

<span data-ttu-id="a7fa7-117">Чтобы отобразить простые многоугольники нонконвекс или простые многоугольники, содержащие отверстия, сначала необходимо выполнить триангуляцию многоугольников (разделить их на многоугольники выпуклой).</span><span class="sxs-lookup"><span data-stu-id="a7fa7-117">To display simple nonconvex polygons or simple polygons containing holes, you must first triangulate the polygons (subdivide them into convex polygons).</span></span> <span data-ttu-id="a7fa7-118">Такое подразделение называется *тесселяцией*.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-118">Such subdivision is called *tessellation*.</span></span> <span data-ttu-id="a7fa7-119">GLU предоставляет коллекцию функций, выполняющих тесселяцию.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-119">GLU provides a collection of functions that perform tessellation.</span></span> <span data-ttu-id="a7fa7-120">Обратите внимание, что функции тесселяции GLU не могут работать с непростыми многоугольниками. Стандартный метод OpenGL для управления такими многоугольниками отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-120">Note that the GLU tessellation functions can't handle nonsimple polygons; there is no standard OpenGL method to handle such polygons.</span></span>

<span data-ttu-id="a7fa7-121">Так как тесселяция часто требуется и может быть довольно непростой, в этом разделе подробно описаны функции тесселяции GLU.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-121">Because tessellation is often required and can be rather tricky, this section describes the GLU tessellation functions in detail.</span></span> <span data-ttu-id="a7fa7-122">Эти функции принимают в качестве входных произвольных многоугольников, которые могут включать отверстия, и возвращают некоторую комбинацию треугольников, сеток треугольников и вентиляторов треугольников.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-122">These functions take as input arbitrary simple polygons that might include holes, and they return some combination of triangles, triangle meshes, and triangle fans.</span></span> <span data-ttu-id="a7fa7-123">Если вы не хотите работать с сетками или вентиляторами, можно указать, что функции тесселяции возвращают только треугольники.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-123">If you don't want to deal with meshes or fans, you can specify that the tessellation functions return only triangles.</span></span> <span data-ttu-id="a7fa7-124">Однако сведения о сети и о вентиляторах повышают производительность.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-124">However, mesh and fan information improves performance.</span></span> <span data-ttu-id="a7fa7-125">Функции тесселяции многоугольника триангуляцию многоугольника вогнутых участков с одним или несколькими контурами.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-125">The polygon tessellation functions triangulate a concave polygon with one or more contours.</span></span>

<span data-ttu-id="a7fa7-126">**Использование тесселяции многоугольников**</span><span class="sxs-lookup"><span data-stu-id="a7fa7-126">**To use polygon tessellation**</span></span>

1.  <span data-ttu-id="a7fa7-127">Создайте объект тесселяции с помощью [**глуневтесс**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="a7fa7-127">Create a tessellation object with [**gluNewTess**](glunewtess.md).</span></span>
2.  <span data-ttu-id="a7fa7-128">Используйте [*глутесскаллбакк*](glutess.md) для определения функций обратного вызова, которые будут использоваться для обработки треугольников, созданных тесселяцией.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-128">Use [*gluTessCallBack*](glutess.md) to define callback functions you will use to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="a7fa7-129">С помощью [**глубегинполигон**](glubeginpolygon.md), [**глутессвертекс**](glutessvertex.md), [**глунекстконтаур**](glunextcontour.md)и [**глуендполигон**](gluendpolygon.md)укажите многоугольник с отверстиями или многоугольником вогнутых участков для тесселяции.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-129">With [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), specify the polygon with holes or the concave polygon to be tessellated.</span></span>

    <span data-ttu-id="a7fa7-130">Когда описание многоугольника будет завершено, средство тесселяции вызовет функции обратного вызова по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-130">When the polygon description is complete, the tessellation facility invokes your callback functions as necessary.</span></span>

    <span data-ttu-id="a7fa7-131">Ненужные объекты тесселяции можно уничтожить с помощью [**глуделететесс**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="a7fa7-131">You can destroy unneeded tessellation objects with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="a7fa7-132">Дополнительные сведения о сохранении данных тесселяции см. в разделе [Использование функций обратного вызова](using-callback-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a7fa7-132">For more information on saving the tessellation data, see [Using Callback Functions](using-callback-functions.md).</span></span>

 

 




