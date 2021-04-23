---
description: Довольно часто точки, заданные для вершин, не имеют точного соответствия с пикселями на экране. В этом случае Direct3D применяет правила растеризации по треугольнику, чтобы определить, какие пиксели относятся к определенному треугольнику.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Правила растрирования (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104273174"
---
# <a name="rasterization-rules-direct3d-9"></a><span data-ttu-id="8eac9-104">Правила растрирования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8eac9-104">Rasterization Rules (Direct3D 9)</span></span>

<span data-ttu-id="8eac9-105">Довольно часто точки, заданные для вершин, не имеют точного соответствия с пикселями на экране.</span><span class="sxs-lookup"><span data-stu-id="8eac9-105">Often, the points specified for vertices do not precisely match the pixels on the screen.</span></span> <span data-ttu-id="8eac9-106">В этом случае Direct3D применяет правила растеризации по треугольнику, чтобы определить, какие пиксели относятся к определенному треугольнику.</span><span class="sxs-lookup"><span data-stu-id="8eac9-106">When this happens, Direct3D applies triangle rasterization rules to decide which pixels apply to a given triangle.</span></span>

-   [<span data-ttu-id="8eac9-107">Правила растрирования треугольников</span><span class="sxs-lookup"><span data-stu-id="8eac9-107">Triangle Rasterization Rules</span></span>](#triangle-rasterization-rules)
-   [<span data-ttu-id="8eac9-108">Правила для точек и линий</span><span class="sxs-lookup"><span data-stu-id="8eac9-108">Point and Line Rules</span></span>](#point-and-line-rules)
-   [<span data-ttu-id="8eac9-109">Правила для точки спрайтов</span><span class="sxs-lookup"><span data-stu-id="8eac9-109">Point Sprite Rules</span></span>](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a><span data-ttu-id="8eac9-110">Правила растеризации по треугольнику</span><span class="sxs-lookup"><span data-stu-id="8eac9-110">Triangle Rasterization Rules</span></span>

<span data-ttu-id="8eac9-111">Direct3D использует общепринятый подход с началом отсчета в левом верхнему углу для размещения геометрических элементов.</span><span class="sxs-lookup"><span data-stu-id="8eac9-111">Direct3D uses a top-left filling convention for filling geometry.</span></span> <span data-ttu-id="8eac9-112">Этот же подход используется для прямоугольников в GDI и OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8eac9-112">This is the same convention that is used for rectangles in GDI and OpenGL.</span></span> <span data-ttu-id="8eac9-113">В Direct3D центр пикселя является решающей точкой.</span><span class="sxs-lookup"><span data-stu-id="8eac9-113">In Direct3D, the center of the pixel is the decisive point.</span></span> <span data-ttu-id="8eac9-114">Если центр находится внутри треугольника, этот пиксель является частью такого треугольника.</span><span class="sxs-lookup"><span data-stu-id="8eac9-114">If the center is inside a triangle, the pixel is part of the triangle.</span></span> <span data-ttu-id="8eac9-115">Центрам пикселей соответствуют целочисленные координаты.</span><span class="sxs-lookup"><span data-stu-id="8eac9-115">Pixel centers are at integer coordinates.</span></span>

<span data-ttu-id="8eac9-116">Это описание правил растеризации по треугольнику, используемых Direct3D, не обязательно распространяется на все доступное оборудование.</span><span class="sxs-lookup"><span data-stu-id="8eac9-116">This description of triangle-rasterization rules used by Direct3D does not necessarily apply to all available hardware.</span></span> <span data-ttu-id="8eac9-117">Во время тестирования вы можете обнаружить небольшие расхождения в реализации этих правил.</span><span class="sxs-lookup"><span data-stu-id="8eac9-117">Your testing may uncover minor variations in the implementation of these rules.</span></span>

<span data-ttu-id="8eac9-118">На следующем рисунке показан прямоугольник, левый верхний угол которого находится в точке (0, 0), а правый нижний угол — в точке (5, 5).</span><span class="sxs-lookup"><span data-stu-id="8eac9-118">The following illustration shows a rectangle whose upper-left corner is at (0, 0) and whose lower-right corner is at (5, 5).</span></span> <span data-ttu-id="8eac9-119">Этот прямоугольник заполняет 25 пикселей, как и следовало ожидать.</span><span class="sxs-lookup"><span data-stu-id="8eac9-119">This rectangle fills 25 pixels, just as you would expect.</span></span> <span data-ttu-id="8eac9-120">Ширина прямоугольника определяется как значение правой координаты минус значение левой координаты.</span><span class="sxs-lookup"><span data-stu-id="8eac9-120">The width of the rectangle is defined as right minus left.</span></span> <span data-ttu-id="8eac9-121">Высота определяется как значение нижней координаты минус значение верхней координаты.</span><span class="sxs-lookup"><span data-stu-id="8eac9-121">The height is defined as bottom minus top.</span></span>

![Иллюстрация нумерованного квадрата, разделенного на шесть строк и столбцов](images/pixmap.png)

<span data-ttu-id="8eac9-123">В подходе с заполнением от верхнего левого угла термин *верхний* указывает на расположение горизонтальных отрезков по вертикали, а термин *левый* указывает на расположение пикселей в отрезке по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="8eac9-123">In the top-left filling convention, *top* refers to the vertical location of horizontal spans, and *left* refers to the horizontal location of pixels within a span.</span></span> <span data-ttu-id="8eac9-124">Сторона фигуры не может быть верхней, если она не является горизонтальной.</span><span class="sxs-lookup"><span data-stu-id="8eac9-124">An edge cannot be a top edge unless it is horizontal.</span></span> <span data-ttu-id="8eac9-125">Чаще всего у большинства треугольников есть только левая и правая стороны.</span><span class="sxs-lookup"><span data-stu-id="8eac9-125">In general, most triangles have only left and right edges.</span></span> <span data-ttu-id="8eac9-126">На следующем рисунке показаны верхняя и правая стороны.</span><span class="sxs-lookup"><span data-stu-id="8eac9-126">The following illustration shows a top edge and a right edge.</span></span>

![Иллюстрация нумерованного квадрата, содержащего два треугольника](images/triedge.png)

<span data-ttu-id="8eac9-128">Подход с заполнением от левого верхнего угла определяет действие, предпринимаемое Direct3D, когда треугольник проходит через центр пикселя.</span><span class="sxs-lookup"><span data-stu-id="8eac9-128">The top-left filling convention determines the action taken by Direct3D when a triangle passes through the center of a pixel.</span></span> <span data-ttu-id="8eac9-129">На следующем рисунке показаны два треугольника, один с координатами вершин (0, 0), (5, 0) и (5, 5) и второй с координатами вершин (0, 5) (0, 0) и (5, 5).</span><span class="sxs-lookup"><span data-stu-id="8eac9-129">The following illustration shows two triangles, one at (0, 0), (5, 0), and (5, 5), and the other at (0, 5), (0, 0), and (5, 5).</span></span> <span data-ttu-id="8eac9-130">К первому треугольнику в этом случае относятся 15 пикселей (показаны черным цветом), тогда как ко второму только 10 пикселей (отображаются серым цветом), поскольку их общая сторона — левая сторона первого треугольника.</span><span class="sxs-lookup"><span data-stu-id="8eac9-130">The first triangle in this case gets 15 pixels (shown in black), whereas the second gets only 10 pixels (shown in gray) because the shared edge is the left edge of the first triangle.</span></span>

![Иллюстрация нумерованного квадрата, показывающего два треугольника](images/twotris.png)

<span data-ttu-id="8eac9-132">Если определить прямоугольник с верхним левым углом в точке (0,5, 0,5) и нижним правым углом в точке (2,5, 4,5), центральной точкой этого прямоугольника будет (1,5, 2,5).</span><span class="sxs-lookup"><span data-stu-id="8eac9-132">If you define a rectangle with its upper-left corner at (0.5, 0.5) and its lower-right corner at (2.5, 4.5), the center point of this rectangle is at (1.5, 2.5).</span></span> <span data-ttu-id="8eac9-133">При растеризации Direct3D раскладывает этот прямоугольник, центр каждого пикселя однозначно находится внутри каждого из четырех треугольников и подход с заполнением от левого верхнего угла не требуется.</span><span class="sxs-lookup"><span data-stu-id="8eac9-133">When the Direct3D rasterizer tessellates this rectangle, the center of each pixel is unambiguously inside each of the four triangles, and the top-left filling convention is not needed.</span></span> <span data-ttu-id="8eac9-134">На следующем рисунке показана такая ситуация.</span><span class="sxs-lookup"><span data-stu-id="8eac9-134">The following illustration shows this.</span></span> <span data-ttu-id="8eac9-135">Пиксели в прямоугольнике помечены согласно треугольнику, в который Direct3D их включает.</span><span class="sxs-lookup"><span data-stu-id="8eac9-135">The pixels in the rectangle are labeled according to the triangle in which Direct3D includes them.</span></span>

![Показывает нумерованный квадрат, который содержит прямоугольник, разделенный на четыре треугольника.](images/noambig.png)

<span data-ttu-id="8eac9-137">При перемещении прямоугольника с предыдущего рисунка таким образом, чтобы его верхний левый угол оказался в точке (1,0, 1,0), его правый нижний угол — в точке (3,0, 5,0), а центр — в точке (2,0, 3,0), Direct3D применяет подход с заполнением от левого верхнего угла.</span><span class="sxs-lookup"><span data-stu-id="8eac9-137">If you move the rectangle in the preceding illustration so that its upper-left corner is at (1.0, 1.0), its lower-right corner at (3.0, 5.0), and its center point at (2.0, 3.0), Direct3D applies the top-left filling convention.</span></span> <span data-ttu-id="8eac9-138">Большинство пикселей в этом прямоугольнике попадают на границу между двумя или более треугольниками, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="8eac9-138">Most pixels in this rectangle straddle the border between two or more triangles, as the following illustration shows.</span></span>

![Иллюстрация нумерованного квадрата, содержащего прямоугольник, разделенный на четыре треугольника](images/fillrule.png)

<span data-ttu-id="8eac9-140">Для обоих прямоугольников задействуются те же пиксели, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="8eac9-140">For both rectangles, the same pixels are affected, as shown in the following illustration.</span></span>

![Иллюстрация пикселей, затрагиваемых предыдущими двумя пронумерованными квадратами](images/samepix.png)

## <a name="point-and-line-rules"></a><span data-ttu-id="8eac9-142">Правила линий и точек</span><span class="sxs-lookup"><span data-stu-id="8eac9-142">Point and Line Rules</span></span>

<span data-ttu-id="8eac9-143">Точки отрисовываются так же, как и точечные спрайты, то есть оба эти вида элементов отрисовываются как выровненные по экрану четырехгранники, и, соответственно, на них распространяются те же правила, что и на отрисовку многоугольников.</span><span class="sxs-lookup"><span data-stu-id="8eac9-143">Points are rendered the same as point sprites, which are both rendered as screen-aligned quadrilaterals and thus adhere to the same rules as polygon rendering.</span></span>

<span data-ttu-id="8eac9-144">Правила отрисовки линий без сглаживания являются точно такими же, что и для [линий GDI](../gdi/lines.md).</span><span class="sxs-lookup"><span data-stu-id="8eac9-144">Non-antialiased line rendering rules are exactly the same as those for [GDI lines](../gdi/lines.md).</span></span>

<span data-ttu-id="8eac9-145">Дополнительные сведения о визуализации линий со сглаженными псевдонимами см. в разделе [**ID3DXLine**](id3dxline.md).</span><span class="sxs-lookup"><span data-stu-id="8eac9-145">For information about antialiased line rendering, see [**ID3DXLine**](id3dxline.md).</span></span>

## <a name="point-sprite-rules"></a><span data-ttu-id="8eac9-146">Правила точечных спрайтов</span><span class="sxs-lookup"><span data-stu-id="8eac9-146">Point Sprite Rules</span></span>

<span data-ttu-id="8eac9-147">Точечные спрайты и фрагментарные примитивы подвергаются растеризации таким образом, как если бы эти примитивы сначала рассекались на треугольники и затем проводилась бы растеризация полученных треугольников.</span><span class="sxs-lookup"><span data-stu-id="8eac9-147">Point sprites and patch primitives are rasterized as if the primitives were first tessellated into triangles and the resulting triangles rasterized.</span></span> <span data-ttu-id="8eac9-148">Дополнительные сведения см. в разделе [Point Sprites (Direct3D 9)](point-sprites.md).</span><span class="sxs-lookup"><span data-stu-id="8eac9-148">For more information, see [Point Sprites (Direct3D 9)](point-sprites.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8eac9-149">См. также</span><span class="sxs-lookup"><span data-stu-id="8eac9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eac9-150">Системы координат и геометрия</span><span class="sxs-lookup"><span data-stu-id="8eac9-150">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
