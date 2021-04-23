---
title: P (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bc7b0c93-af06-44a4-8bb8-adc0c6fedb6e
keywords:
- parameters
- подразделение перспективы
- пиксели
- точки
- многоугольники
- Primitives
- матрицы проекции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9970b3eb84920184e693ace93b14120828573e30
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103988112"
---
# <a name="p-opengl"></a><span data-ttu-id="9d0ab-110">P (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="9d0ab-110">P (OpenGL)</span></span>

<span data-ttu-id="9d0ab-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [р.](h.md) [](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="9d0ab-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="9d0ab-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**параметр**</span><span class="sxs-lookup"><span data-stu-id="9d0ab-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ab-113">Значение, передаваемое в качестве аргумента команде OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-113">A value passed as an argument to an OpenGL command.</span></span> <span data-ttu-id="9d0ab-114">Иногда одно из значений, передаваемых по ссылке на команду OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-114">Sometimes one of the values passed by reference to an OpenGL command.</span></span>

</dd> <dt>

<span data-ttu-id="9d0ab-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**подразделение перспективы**</span><span class="sxs-lookup"><span data-stu-id="9d0ab-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**perspective division**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ab-116">Деление x, y и z на w выполняется в координатах обрезки.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-116">The division of x, y, and z by w, carried out in clip coordinates.</span></span> <span data-ttu-id="9d0ab-117">См. также [координаты клипов](c.md).</span><span class="sxs-lookup"><span data-stu-id="9d0ab-117">See also [clip coordinates](c.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d0ab-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**растров**</span><span class="sxs-lookup"><span data-stu-id="9d0ab-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**pixel**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ab-119">Элемент Picture.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-119">Picture element.</span></span> <span data-ttu-id="9d0ab-120">Биты в расположении (x, y) всех битпланес в буфера кадров составляют один пиксель (x, y).</span><span class="sxs-lookup"><span data-stu-id="9d0ab-120">The bits at location (x, y) of all the bitplanes in the framebuffer constitute the single pixel (x, y).</span></span> <span data-ttu-id="9d0ab-121">В изображении в памяти клиента пиксель — это одна группа элементов.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-121">In an image in client memory, a pixel is one group of elements.</span></span> <span data-ttu-id="9d0ab-122">В координатах окна OpenGL каждый пиксель соответствует области экрана 1,0 x 1.0.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-122">In OpenGL window coordinates, each pixel corresponds to a 1.0x1.0 screen area.</span></span> <span data-ttu-id="9d0ab-123">Координаты левого нижнего угла в именах пикселей x, y — (x, y), а правый верхний угол — (x + 1, y + 1).</span><span class="sxs-lookup"><span data-stu-id="9d0ab-123">The coordinates of the lower-left corner of the pixel names x, y are (x, y), and the upper-right corner are (x+1, y+1).</span></span>

</dd> <dt>

<span data-ttu-id="9d0ab-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**точки**</span><span class="sxs-lookup"><span data-stu-id="9d0ab-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**point**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ab-125">Точное расположение в пространстве, которое подготавливается к просмотру как точка конечного диаметра.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-125">An exact location in space, which is rendered as a finite-diameter dot.</span></span>

</dd> <dt>

<span data-ttu-id="9d0ab-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**фигуры**</span><span class="sxs-lookup"><span data-stu-id="9d0ab-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**polygon**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ab-127">Близкое к краю поверхность, ограниченная краями, заданным вершинами.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-127">A near-planar surface bounded by edges specified by vertices.</span></span> <span data-ttu-id="9d0ab-128">Каждый треугольник сетки треугольника — это многоугольник, как и каждый грани четырехсторонней сетки грани четырехсторонней.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-128">Each triangle of a triangle mesh is a polygon, as is each quadrilateral of a quadrilateral mesh.</span></span> <span data-ttu-id="9d0ab-129">Прямоугольник, заданный параметром Глрект, также является многоугольником.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-129">The rectangle specified by glRect is also a polygon.</span></span>

</dd> <dt>

<span data-ttu-id="9d0ab-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**простого**</span><span class="sxs-lookup"><span data-stu-id="9d0ab-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitive**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ab-131">Фигура (точка, линия, многоугольник, точечный рисунок или изображение), которую можно изобразить, сохранять и манипулировать как дискретными сущностями; элементы, из которых создаются крупные графические модели.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-131">A shape (such as a point, line, polygon, bitmap, or image) that can be drawn, stored, and manipulated as a discrete entity; elements from which large graphic designs are created.</span></span>

</dd> <dt>

<span data-ttu-id="9d0ab-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**матрица проекции**</span><span class="sxs-lookup"><span data-stu-id="9d0ab-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**projection matrix**</span></span>
</dt> <dd>

<span data-ttu-id="9d0ab-133">Матрица 4x4, которая преобразует точки, линии, многоугольники и растровые позиции из координат глаз в координаты отсечения.</span><span class="sxs-lookup"><span data-stu-id="9d0ab-133">The 4x4 matrix that transforms points, lines, polygons, and raster positions from eye coordinates to clip coordinates.</span></span>

</dd> </dl>

 

 




