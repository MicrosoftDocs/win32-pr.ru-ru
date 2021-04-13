---
title: T (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы T.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: effb170b-fea3-4954-9f9c-3bc1aa829bc0
keywords:
- тесселяции
- шаг текселя
- текстура
- Сопоставление текстур
- Матрица текстур
- преобразования
- треугольники
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1cb324179137dbf9f9046c0c19acfffdf7394e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134890"
---
# <a name="t-opengl"></a><span data-ttu-id="fa4b7-110">T (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="fa4b7-110">T (OpenGL)</span></span>

<span data-ttu-id="fa4b7-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [р](h.md) [.](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="fa4b7-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="fa4b7-112"><span id="opengl_tessellation"></span><span id="OPENGL_TESSELLATION"></span>**тесселяции**</span><span class="sxs-lookup"><span data-stu-id="fa4b7-112"><span id="opengl_tessellation"></span><span id="OPENGL_TESSELLATION"></span>**tessellation**</span></span>
</dt> <dd>

<span data-ttu-id="fa4b7-113">Уменьшение части аналитической поверхности до сетки многоугольников или части аналитической кривой до последовательности строк.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-113">Reduction of a portion of an analytic surface to a mesh of polygons, or of a portion of an analytic curve to a sequence of lines.</span></span>

</dd> <dt>

<span data-ttu-id="fa4b7-114"><span id="opengl_texel"></span><span id="OPENGL_TEXEL"></span>**шаг текселя**</span><span class="sxs-lookup"><span data-stu-id="fa4b7-114"><span id="opengl_texel"></span><span id="OPENGL_TEXEL"></span>**texel**</span></span>
</dt> <dd>

<span data-ttu-id="fa4b7-115">Элемент текстуры.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-115">A texture element.</span></span> <span data-ttu-id="fa4b7-116">Шаг текселя получается из памяти текстуры и представляет цвет текстуры, применяемой к соответствующему фрагменту.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-116">A texel is obtained from texture memory and represents the color of the texture to be applied to a corresponding fragment.</span></span> <span data-ttu-id="fa4b7-117">См. также [фрагмент](f.md).</span><span class="sxs-lookup"><span data-stu-id="fa4b7-117">See also [fragment](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa4b7-118"><span id="opengl_texture"></span><span id="OPENGL_TEXTURE"></span>**поддержки**</span><span class="sxs-lookup"><span data-stu-id="fa4b7-118"><span id="opengl_texture"></span><span id="OPENGL_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="fa4b7-119">Одномерный или двухмерный рисунок, используемый для изменения цвета фрагментов, созданных с помощью растрирования.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-119">A one- or two-dimensional image used to modify the color of fragments produced by rasterization.</span></span> <span data-ttu-id="fa4b7-120">См. также [растрирование](r.md).</span><span class="sxs-lookup"><span data-stu-id="fa4b7-120">See also [rasterize](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa4b7-121"><span id="opengl_texture_mapping"></span><span id="OPENGL_TEXTURE_MAPPING"></span>**Сопоставление текстур**</span><span class="sxs-lookup"><span data-stu-id="fa4b7-121"><span id="opengl_texture_mapping"></span><span id="OPENGL_TEXTURE_MAPPING"></span>**texture mapping**</span></span>
</dt> <dd>

<span data-ttu-id="fa4b7-122">Процесс применения изображения (текстуры) к примитиву.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-122">The process of applying an image (the texture) to a primitive.</span></span> <span data-ttu-id="fa4b7-123">Сопоставление текстур часто используется для добавления в сцену реальной реальности.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-123">Texture mapping is often used to add realism to a scene.</span></span> <span data-ttu-id="fa4b7-124">Например, можно применить рисунок здания фасадной к многоугольнику, представляющему стену.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-124">For example, you could apply a picture of a building facade to a polygon representing a wall.</span></span> <span data-ttu-id="fa4b7-125">См. также текстура.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-125">See also texture.</span></span>

</dd> <dt>

<span data-ttu-id="fa4b7-126"><span id="opengl_texture_matrix"></span><span id="OPENGL_TEXTURE_MATRIX"></span>**Матрица текстур**</span><span class="sxs-lookup"><span data-stu-id="fa4b7-126"><span id="opengl_texture_matrix"></span><span id="OPENGL_TEXTURE_MATRIX"></span>**texture matrix**</span></span>
</dt> <dd>

<span data-ttu-id="fa4b7-127">Матрица 4x4, которая преобразует координаты текстуры из координат, которые они задают в, в координаты, используемые для интерполяции и поиска текстур.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-127">The 4x4 matrix that transforms texture coordinates from the coordinates that they're specified in to the coordinates that are used for interpolation and texture lookup.</span></span>

</dd> <dt>

<span data-ttu-id="fa4b7-128"><span id="opengl_transformation"></span><span id="OPENGL_TRANSFORMATION"></span>**преобразования**</span><span class="sxs-lookup"><span data-stu-id="fa4b7-128"><span id="opengl_transformation"></span><span id="OPENGL_TRANSFORMATION"></span>**transformation**</span></span>
</dt> <dd>

<span data-ttu-id="fa4b7-129">Деформацию пространства.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-129">A warping of space.</span></span> <span data-ttu-id="fa4b7-130">В OpenGL преобразования ограничены с помощью проецированных преобразований, включающих все, что может быть представлено матрицей 4x4.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-130">In OpenGL, transformations are limited to projective transformations that include anything that can be represented by a 4x4 matrix.</span></span> <span data-ttu-id="fa4b7-131">К таким преобразованиям относятся вращение, переводы, масштабирование (неоднородным доступом) по осям координат, преобразования перспективы и их сочетания.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-131">Such transformations include rotations, translations, (nonuniform) scalings along the coordinate axes, perspective transformations, and combinations of these.</span></span>

</dd> <dt>

<span data-ttu-id="fa4b7-132"><span id="opengl_triangle"></span><span id="OPENGL_TRIANGLE"></span>**значок**</span><span class="sxs-lookup"><span data-stu-id="fa4b7-132"><span id="opengl_triangle"></span><span id="OPENGL_TRIANGLE"></span>**triangle**</span></span>
</dt> <dd>

<span data-ttu-id="fa4b7-133">Многоугольник с тремя краями.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-133">A polygon with three edges.</span></span> <span data-ttu-id="fa4b7-134">Треугольники всегда выпуклой.</span><span class="sxs-lookup"><span data-stu-id="fa4b7-134">Triangles are always convex.</span></span>

</dd> </dl>

 

 




