---
title: R (OpenGL)
description: Определения терминов OpenGL, начинающихся с буквы R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ab0286f5-cad2-4537-aa98-be0fce55ff53
keywords:
- Растрирование
- прямоугольники
- rendering
- RGBA
- Режим RGBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b82a2db1bade12a0ff844006a1572cdc3b977dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103891322"
---
# <a name="r-opengl"></a><span data-ttu-id="534b1-108">R (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="534b1-108">R (OpenGL)</span></span>

<span data-ttu-id="534b1-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [р](h.md) [](i.md) . [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="534b1-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="534b1-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**растрирования**</span><span class="sxs-lookup"><span data-stu-id="534b1-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**rasterize**</span></span>
</dt> <dd>

<span data-ttu-id="534b1-111">Преобразование проецируемой точки, линии, многоугольника или пикселов точечного рисунка или изображения в фрагменты, каждый из которых соответствует пикселу в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="534b1-111">To convert a projected point, line, or polygon, or the pixels of a bitmap or image, to fragments, each corresponding to a pixel in the framebuffer.</span></span> <span data-ttu-id="534b1-112">Обратите внимание, что все примитивы растрируются, а не только точки, линии и многоугольники.</span><span class="sxs-lookup"><span data-stu-id="534b1-112">Note that all primitives are rasterized, not just points, lines, and polygons</span></span>

</dd> <dt>

<span data-ttu-id="534b1-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**углами**</span><span class="sxs-lookup"><span data-stu-id="534b1-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="534b1-114">Объект грани четырехсторонней, в котором альтернативные грани находятся параллельно друг с другом в координатах объекта.</span><span class="sxs-lookup"><span data-stu-id="534b1-114">A quadrilateral whose alternate edges are parallel to each other in object coordinates.</span></span> <span data-ttu-id="534b1-115">Многоугольники, указанные с помощью Глрект \* (), всегда являются прямоугольниками; другие куадрилатералс могут быть прямоугольниками.</span><span class="sxs-lookup"><span data-stu-id="534b1-115">Polygons specified with glRect\*( ) are always rectangles; other quadrilaterals might be rectangles.</span></span>

</dd> <dt>

<span data-ttu-id="534b1-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**отчета**</span><span class="sxs-lookup"><span data-stu-id="534b1-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**rendering**</span></span>
</dt> <dd>

<span data-ttu-id="534b1-117">Преобразование примитивов, указанных в координатах объекта, в изображение в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="534b1-117">Conversion of primitives specified in object coordinates to an image in the framebuffer.</span></span> <span data-ttu-id="534b1-118">Подготовка к просмотру является основной операцией OpenGL.</span><span class="sxs-lookup"><span data-stu-id="534b1-118">Rendering is the primary operation of OpenGL.</span></span>

</dd> <dt>

<span data-ttu-id="534b1-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span><span class="sxs-lookup"><span data-stu-id="534b1-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span></span>
</dt> <dd>

<span data-ttu-id="534b1-120">Цветовые компоненты красного, зеленого, синего и альфа-цветов в режиме RGBA.</span><span class="sxs-lookup"><span data-stu-id="534b1-120">The red, green, blue, and alpha color components of the RGBA mode.</span></span>

</dd> <dt>

<span data-ttu-id="534b1-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**Режим RGBA**</span><span class="sxs-lookup"><span data-stu-id="534b1-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**RGBA mode**</span></span>
</dt> <dd>

<span data-ttu-id="534b1-122">Контекст OpenGL, в котором буферы цветов хранят цветовые компоненты красного, зеленого, синего и альфа-цветов, а не индексы цвета.</span><span class="sxs-lookup"><span data-stu-id="534b1-122">An OpenGL context in which its color buffers store red, green, blue, and alpha color components, rather than color indexes.</span></span>

</dd> </dl>

 

 




