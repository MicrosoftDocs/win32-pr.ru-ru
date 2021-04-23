---
title: F (OpenGL)
description: Определения терминов OpenGL, начинающихся с буквы F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- faces
- Плоская заливка
- туман
- шрифты
- fragments
- фрамебуфферс
- Передняя сторона
- фрустум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105672447"
---
# <a name="f-opengl"></a><span data-ttu-id="0c6bf-111">F (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="0c6bf-111">F (OpenGL)</span></span>

<span data-ttu-id="0c6bf-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [р](h.md) . [](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="0c6bf-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="0c6bf-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**личным**</span><span class="sxs-lookup"><span data-stu-id="0c6bf-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**face**</span></span>
</dt> <dd>

<span data-ttu-id="0c6bf-114">Одна сторона многоугольника.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-114">One side of a polygon.</span></span> <span data-ttu-id="0c6bf-115">Каждый многоугольник имеет два лица: лицевой и задней стороной.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-115">Each polygon has two faces: a front face and a back face.</span></span> <span data-ttu-id="0c6bf-116">В окне всегда отображается только одна из сторон.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-116">Only one face is ever visible in the window.</span></span> <span data-ttu-id="0c6bf-117">Является ли видимым задний или передний вид, фактически определяется после проецирования многоугольника на окно.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-117">Whether the back or front face is visible is effectively determined after the polygon is projected onto the window.</span></span> <span data-ttu-id="0c6bf-118">Если после этой проекции края многоугольника направлены по часовой стрелке, отображается один из граней. Если экран направлен против часовой стрелки, отображается другая грань.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-118">After this projection, if the polygon's edges are directed clockwise, one of the faces is visible; if directed counterclockwise, the other face is visible.</span></span> <span data-ttu-id="0c6bf-119">Независимо от того, соответствует ли часовой стрелки спереди или назад (и против часовой стрелки соответствует Back или Front), определяется программистом OpenGL.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-119">Whether clockwise corresponds to front or back (and counterclockwise corresponds to back or front) is determined by the OpenGL programmer.</span></span>

</dd> <dt>

<span data-ttu-id="0c6bf-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**Плоская заливка**</span><span class="sxs-lookup"><span data-stu-id="0c6bf-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**flat shading**</span></span>
</dt> <dd>

<span data-ttu-id="0c6bf-121">Относится к цвету примитива с одним, постоянным цветом в его экстенте, а не плавной интерполяцией цветов по примитиву.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-121">Refers to coloring a primitive with a single, constant color across its extent, rather than smoothly interpolating colors across the primitive.</span></span> <span data-ttu-id="0c6bf-122">См. раздел [Заливка Гуро](g.md).</span><span class="sxs-lookup"><span data-stu-id="0c6bf-122">See [Gouraud shading](g.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c6bf-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**туман**</span><span class="sxs-lookup"><span data-stu-id="0c6bf-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**fog**</span></span>
</dt> <dd>

<span data-ttu-id="0c6bf-124">Метод подготовки к просмотру, который можно использовать для имитации атмосферных эффектов, таких как Хазе, туман и смог, путем исчезновения цветов объектов в цвет фона на основе расстояния от средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-124">A rendering technique that can be used to simulate atmospheric effects such as haze, fog, and smog by fading object colors to a background color based on distance from the viewer.</span></span> <span data-ttu-id="0c6bf-125">Туман также помогает восприятию расстояния от средства просмотра, давая более глубокое подсказку.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-125">Fog also aids in the perception of distance from the viewer, giving a depth cue.</span></span> <span data-ttu-id="0c6bf-126">См. также [Depth-cueing](d.md).</span><span class="sxs-lookup"><span data-stu-id="0c6bf-126">See also [depth-cueing](d.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c6bf-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**шрифтов**</span><span class="sxs-lookup"><span data-stu-id="0c6bf-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**font**</span></span>
</dt> <dd>

<span data-ttu-id="0c6bf-128">Группа графических представлений символов, обычно используемых для отображения строк текста.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-128">A group of graphical character representations usually used to display strings of text.</span></span> <span data-ttu-id="0c6bf-129">Символами могут быть римские буквы, математические символы, азиатские идеограмс, Египет хиероглифс и т. д.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-129">The characters may be roman letters, mathematical symbols, Asian ideograms, Egyptian hieroglyphs, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="0c6bf-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**экстент**</span><span class="sxs-lookup"><span data-stu-id="0c6bf-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="0c6bf-131">Графические данные, созданные путем растрирования примитивов.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-131">Graphic data generated by the rasterization of primitives.</span></span> <span data-ttu-id="0c6bf-132">Каждый фрагмент соответствует одному пикселю и включает цвет, глубину и иногда значения координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-132">Each fragment corresponds to a single pixel and includes color, depth, and sometimes texture-coordinate values.</span></span>

</dd> <dt>

<span data-ttu-id="0c6bf-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**буфера кадров**</span><span class="sxs-lookup"><span data-stu-id="0c6bf-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**framebuffer**</span></span>
</dt> <dd>

<span data-ttu-id="0c6bf-134">Стек битпланес.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-134">A stack of bitplanes.</span></span> <span data-ttu-id="0c6bf-135">Все буферы заданного окна или контекста.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-135">All the buffers of a given window or context.</span></span> <span data-ttu-id="0c6bf-136">Иногда включает всю пиксельную память графического ускорителя графики.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-136">Sometimes includes all the pixel memory of the graphics hardware accelerator.</span></span> <span data-ttu-id="0c6bf-137">См. также [битплане](b.md).</span><span class="sxs-lookup"><span data-stu-id="0c6bf-137">See also [bitplane](b.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c6bf-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**Передняя сторона**</span><span class="sxs-lookup"><span data-stu-id="0c6bf-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front face**</span></span>
</dt> <dd>

<span data-ttu-id="0c6bf-139">Ознакомьтесь с лицом.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-139">See face.</span></span>

</dd> <dt>

<span data-ttu-id="0c6bf-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**фрустум**</span><span class="sxs-lookup"><span data-stu-id="0c6bf-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span></span>
</dt> <dd>

<span data-ttu-id="0c6bf-141">Представление тома, искривленное делением перспективы.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-141">The view volume warped by perspective division.</span></span>

</dd> </dl>

 

 




