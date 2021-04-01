---
title: W (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы W.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7f8235a3-ea48-40eb-8957-e7a55a5778af
keywords:
- Windows
- с выровняйтем окон
- координаты окна
- каркасной модели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f6f1897af46c85ed48171d251ebe1b2de8c5e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800605"
---
# <a name="w-opengl"></a><span data-ttu-id="a7c82-107">W (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="a7c82-107">W (OpenGL)</span></span>

<span data-ttu-id="a7c82-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [р](h.md) [](i.md) . [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="a7c82-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="a7c82-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**окно**</span><span class="sxs-lookup"><span data-stu-id="a7c82-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**window**</span></span>
</dt> <dd>

<span data-ttu-id="a7c82-110">Подобласть буфера кадров, обычно прямоугольная, у которой все пиксели имеют одинаковую конфигурацию буфера.</span><span class="sxs-lookup"><span data-stu-id="a7c82-110">A subregion of the framebuffer, usually rectangular, whose pixels all have the same buffer configuration.</span></span> <span data-ttu-id="a7c82-111">Контекст OpenGL подготавливается к просмотру по одному окну за раз.</span><span class="sxs-lookup"><span data-stu-id="a7c82-111">An OpenGL context renders to one window at a time.</span></span>

</dd> <dt>

<span data-ttu-id="a7c82-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**с выровняйтем окон**</span><span class="sxs-lookup"><span data-stu-id="a7c82-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**window-aligned**</span></span>
</dt> <dd>

<span data-ttu-id="a7c82-113">При ссылке на сегменты линии или границы многоугольника подразумевает, что они являются параллельными границами окна.</span><span class="sxs-lookup"><span data-stu-id="a7c82-113">When referring to line segments or polygon edges, implies that these are parallel to the window boundaries.</span></span> <span data-ttu-id="a7c82-114">(В OpenGL окно прямоугольное, с горизонтальными и вертикальными краями).</span><span class="sxs-lookup"><span data-stu-id="a7c82-114">(In OpenGL, the window is rectangular, with horizontal and vertical edges).</span></span> <span data-ttu-id="a7c82-115">При ссылке на шаблон многоугольника подразумевает, что шаблон фиксирован относительно исходного окна.</span><span class="sxs-lookup"><span data-stu-id="a7c82-115">When referring to a polygon pattern, implies that the pattern is fixed relative to the window origin.</span></span>

</dd> <dt>

<span data-ttu-id="a7c82-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**координаты окна**</span><span class="sxs-lookup"><span data-stu-id="a7c82-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**window coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="a7c82-117">Система координат окна.</span><span class="sxs-lookup"><span data-stu-id="a7c82-117">The coordinate system of a window.</span></span> <span data-ttu-id="a7c82-118">Важно различать имена пикселей, которые являются дискретными, и систему координат окна, которая является непрерывной.</span><span class="sxs-lookup"><span data-stu-id="a7c82-118">It's important to distinguish between the names of pixels, which are discrete, and the window-coordinate system, which is continuous.</span></span> <span data-ttu-id="a7c82-119">Например, пиксель в левом нижнем углу окна — пиксель (0, 0); координаты окна центра этого пикселя: (0,5, 0,5, z).</span><span class="sxs-lookup"><span data-stu-id="a7c82-119">For example, the pixel at the lower-left corner of a window is pixel (0, 0); the window coordinates of the center of this pixel are (0.5, 0.5, z).</span></span> <span data-ttu-id="a7c82-120">Обратите внимание, что координаты окон включают глубину, z, компонент и то, что этот компонент также является непрерывным.</span><span class="sxs-lookup"><span data-stu-id="a7c82-120">Note that window coordinates include a depth, or z, component, and that this component is continuous as well.</span></span>

</dd> <dt>

<span data-ttu-id="a7c82-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**каркасной модели**</span><span class="sxs-lookup"><span data-stu-id="a7c82-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**wireframe**</span></span>
</dt> <dd>

<span data-ttu-id="a7c82-122">Представление объекта, содержащего только сегменты линий.</span><span class="sxs-lookup"><span data-stu-id="a7c82-122">A representation of an object that contains line segments only.</span></span> <span data-ttu-id="a7c82-123">Как правило, сегменты линии обозначают границы многоугольников.</span><span class="sxs-lookup"><span data-stu-id="a7c82-123">Typically, the line segments indicate polygon edges.</span></span>

</dd> </dl>

 

 




