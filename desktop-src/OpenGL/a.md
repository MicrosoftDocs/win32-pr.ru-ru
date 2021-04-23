---
title: A (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы A.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- сглаживания
- alpha
- анимация
- сглаживание
- Обрезка конкретного приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d161832eb6d81738038e10564233f26920f0d60
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414577"
---
# <a name="a-opengl"></a><span data-ttu-id="48ada-108">A (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="48ada-108">A (OpenGL)</span></span>

<span data-ttu-id="48ada-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [р](h.md) . [](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="48ada-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="48ada-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**сглаживания**</span><span class="sxs-lookup"><span data-stu-id="48ada-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**aliasing**</span></span>
</dt> <dd>

<span data-ttu-id="48ada-111">Метод подготовки к просмотру, который присваивает пикселам цвет отображаемого примитива, независимо от того, охватывает ли этот примитив все или часть области пикселя.</span><span class="sxs-lookup"><span data-stu-id="48ada-111">A rendering technique that assigns to pixels the color of the primitive being rendered, whether that primitive covers all or part of the pixel's area.</span></span> <span data-ttu-id="48ada-112">Псевдонимы приводят к неровным краям или жаггиес.</span><span class="sxs-lookup"><span data-stu-id="48ada-112">Aliasing results in jagged edges, or jaggies.</span></span> <span data-ttu-id="48ada-113">См. также [жаггиес](jk.md).</span><span class="sxs-lookup"><span data-stu-id="48ada-113">See also [jaggies](jk.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ada-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**буквы**</span><span class="sxs-lookup"><span data-stu-id="48ada-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**alpha**</span></span>
</dt> <dd>

<span data-ttu-id="48ada-115">Четвертый компонент цвета обычно используется для управления смешением цветов.</span><span class="sxs-lookup"><span data-stu-id="48ada-115">A fourth color component typically used to control color blending.</span></span> <span data-ttu-id="48ada-116">Альфа-компонент никогда не отображается напрямую.</span><span class="sxs-lookup"><span data-stu-id="48ada-116">The alpha component is never displayed directly.</span></span> <span data-ttu-id="48ada-117">По соглашению OpenGL Alpha указывает на непрозрачность и прозрачность по шкале от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="48ada-117">By convention, OpenGL alpha indicates opacity and transparency on a scale of 0.0 to 1.0.</span></span> <span data-ttu-id="48ada-118">Альфа-значение 1,0 означает полную прозрачность, альфа-значение 0,0 означает полную прозрачность.</span><span class="sxs-lookup"><span data-stu-id="48ada-118">An alpha value of 1.0 implies complete opacity, an alpha value of 0.0 implies complete transparency.</span></span>

</dd> <dt>

<span data-ttu-id="48ada-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**захоронен**</span><span class="sxs-lookup"><span data-stu-id="48ada-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animation**</span></span>
</dt> <dd>

<span data-ttu-id="48ada-120">Создание повторяющихся визуализаций сцены достаточно быстро, с плавно изменяющимися положениями или позициями объектов, что позволяет достичь иллюзии движения.</span><span class="sxs-lookup"><span data-stu-id="48ada-120">The generation of repeated renderings of a scene quickly enough, with smoothly changing viewpoint or object positions, that the illusion of motion is achieved.</span></span> <span data-ttu-id="48ada-121">Анимация OpenGL почти всегда использует двойную буферизацию.</span><span class="sxs-lookup"><span data-stu-id="48ada-121">OpenGL animation almost always uses double-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="48ada-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**сглаживания**</span><span class="sxs-lookup"><span data-stu-id="48ada-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**antialiasing**</span></span>
</dt> <dd>

<span data-ttu-id="48ada-123">Метод подготовки к просмотру, который назначает цвета пикселям в зависимости от доли области пикселя, охватываемой выводимым примитивом.</span><span class="sxs-lookup"><span data-stu-id="48ada-123">A rendering technique that assigns colors to pixels based on the fraction of the pixel area that is covered by the primitive being rendered.</span></span> <span data-ttu-id="48ada-124">При отрисовке со сглаживанием уменьшается или устраняется жаггиес, полученный в результате отрисовки с псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="48ada-124">Antialiased rendering reduces or eliminates the jaggies that result from aliased rendering.</span></span> <span data-ttu-id="48ada-125">См. также [жаггиес](jk.md), [Подготовка к просмотру](r.md).</span><span class="sxs-lookup"><span data-stu-id="48ada-125">See also [jaggies](jk.md), [rendering](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="48ada-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**Обрезка конкретного приложения**</span><span class="sxs-lookup"><span data-stu-id="48ada-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**application-specific clipping**</span></span> 
</dt> <dd>

<span data-ttu-id="48ada-127">Обрезка примитивов относительно плоскостей в координатах глаз.</span><span class="sxs-lookup"><span data-stu-id="48ada-127">Clipping of primitives against planes in eye coordinates.</span></span> <span data-ttu-id="48ada-128">Плоскости задаются приложением с помощью [**глклипплане**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="48ada-128">The planes are specified by the application using [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="48ada-129">См. также [координаты глаз](e.md).</span><span class="sxs-lookup"><span data-stu-id="48ada-129">See also [eye coordinates](e.md).</span></span>

</dd> </dl>

 

 




