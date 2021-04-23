---
title: D (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- cueing глубины
- списки вывода
- сглаживания
- двойная буферизация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb068f06135c6ba29e8a61f472d98907090a78
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800773"
---
# <a name="d-opengl"></a><span data-ttu-id="38af9-108">D (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="38af9-108">D (OpenGL)</span></span>

<span data-ttu-id="38af9-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [р](h.md) . [](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="38af9-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="38af9-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**Длина**</span><span class="sxs-lookup"><span data-stu-id="38af9-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**depth**</span></span>
</dt> <dd>

<span data-ttu-id="38af9-111">Обычно относится к координатам окна z.</span><span class="sxs-lookup"><span data-stu-id="38af9-111">Generally refers to the z window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="38af9-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**cueing глубины**</span><span class="sxs-lookup"><span data-stu-id="38af9-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**depth cueing**</span></span>
</dt> <dd>

<span data-ttu-id="38af9-113">Метод подготовки к просмотру, который назначает цвет на основе расстояния от точки зрения.</span><span class="sxs-lookup"><span data-stu-id="38af9-113">A rendering technique that assigns color based on distance from the viewpoint.</span></span>

</dd> <dt>

<span data-ttu-id="38af9-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**список отображаемых**</span><span class="sxs-lookup"><span data-stu-id="38af9-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**display list**</span></span>
</dt> <dd>

<span data-ttu-id="38af9-115">Именованный список команд OpenGL.</span><span class="sxs-lookup"><span data-stu-id="38af9-115">A named list of OpenGL commands.</span></span> <span data-ttu-id="38af9-116">Списки дисплеев всегда хранятся на сервере, поэтому списки для уменьшения сетевого трафика в средах клиента и сервера можно использовать.</span><span class="sxs-lookup"><span data-stu-id="38af9-116">Display lists are always stored on the server, so display lists can be used to reduce the network traffic in client/server environments.</span></span> <span data-ttu-id="38af9-117">Содержимое списка отображений может быть предварительно обработано, поэтому оно может выполняться более эффективно, чем тот же набор команд OpenGL, который выполняется в режиме интерпретации.</span><span class="sxs-lookup"><span data-stu-id="38af9-117">The contents of a display list may be preprocessed, and might therefore execute more efficiently than the same set of OpenGL commands executed in immediate mode.</span></span> <span data-ttu-id="38af9-118">Такая предварительная обработка особенно важна для ресурсоемких команд, таких как [**глтексимаже**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="38af9-118">Such preprocessing is especially important for computing intensive commands such as [**glTexImage**](glteximage1d.md).</span></span>

</dd> <dt>

<span data-ttu-id="38af9-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**сглаживания**</span><span class="sxs-lookup"><span data-stu-id="38af9-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**dithering**</span></span>
</dt> <dd>

<span data-ttu-id="38af9-120">Метод для увеличения воспринимаемого диапазона цветов в изображении за счет использования пространственного разрешения.</span><span class="sxs-lookup"><span data-stu-id="38af9-120">A technique for increasing the perceived range of colors in an image at the cost of spatial resolution.</span></span> <span data-ttu-id="38af9-121">Смежным пикселам присваиваются разные значения цвета.</span><span class="sxs-lookup"><span data-stu-id="38af9-121">Adjacent pixels are assigned differing color values.</span></span> <span data-ttu-id="38af9-122">При просмотре с расстояния эти цвета по-видимому смешиваются с одним промежуточным цветом.</span><span class="sxs-lookup"><span data-stu-id="38af9-122">When viewed from a distance, these colors seem to blend into a single intermediate color.</span></span> <span data-ttu-id="38af9-123">Эта методика похожа на половину Тонинг, используемую в публикациях черно-белых, для получения оттенков серого.</span><span class="sxs-lookup"><span data-stu-id="38af9-123">The technique is similar to the half-toning used in black-and-white publications to achieve shades of gray.</span></span>

</dd> <dt>

<span data-ttu-id="38af9-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**Двойная буферизация**</span><span class="sxs-lookup"><span data-stu-id="38af9-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**double buffering**</span></span>
</dt> <dd>

<span data-ttu-id="38af9-125">Использование контекстов OpenGL, в которых буферы фона и фона имеют двойную буферизацию.</span><span class="sxs-lookup"><span data-stu-id="38af9-125">Using OpenGL contexts in which both front and back color buffers are double-buffered.</span></span> <span data-ttu-id="38af9-126">Гладкая анимация достигается за счет отрисовки только заднего буфера (который не отображается), что приводит к замене передних и задних буферов.</span><span class="sxs-lookup"><span data-stu-id="38af9-126">Smooth animation is accomplished by rendering into only the back buffer (which isn't displayed), then causing the front and back buffers to be swapped.</span></span>

</dd> </dl>

 

 




