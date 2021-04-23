---
title: I (OpenGL)
description: Определения терминов OpenGL, начинающихся с буквы I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2c78efce-9aed-4bcd-a254-7bff053b0acd
keywords:
- images
- примитивы изображений
- режим интерпретации
- index
- IRI GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe340cfbd7dbef3d93cc68ba310d863717225c0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533650"
---
# <a name="i-opengl"></a><span data-ttu-id="dd7b2-108">I (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="dd7b2-108">I (OpenGL)</span></span>

<span data-ttu-id="dd7b2-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [р](h.md) . [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="dd7b2-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="dd7b2-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**Эскиз**</span><span class="sxs-lookup"><span data-stu-id="dd7b2-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**image**</span></span>
</dt> <dd>

<span data-ttu-id="dd7b2-111">Прямоугольный массив пикселей в памяти клиента или в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="dd7b2-111">A rectangular array of pixels, either in client memory or in the framebuffer.</span></span>

</dd> <dt>

<span data-ttu-id="dd7b2-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**примитив изображения**</span><span class="sxs-lookup"><span data-stu-id="dd7b2-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**image primitive**</span></span> 
</dt> <dd>

<span data-ttu-id="dd7b2-113">Точечный рисунок или изображение.</span><span class="sxs-lookup"><span data-stu-id="dd7b2-113">A bitmap or an image.</span></span>

</dd> <dt>

<span data-ttu-id="dd7b2-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**режим интерпретации**</span><span class="sxs-lookup"><span data-stu-id="dd7b2-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**immediate mode**</span></span>
</dt> <dd>

<span data-ttu-id="dd7b2-115">Режим, в котором команда OpenGL вызывается напрямую, а не из списка просмотра.</span><span class="sxs-lookup"><span data-stu-id="dd7b2-115">Mode in which an OpenGL command is called directly, rather than from a display list.</span></span> <span data-ttu-id="dd7b2-116">Бит немедленного режима не существует; режим в режиме интерпретации относится к использованию OpenGL, а не к определенному биту состояния OpenGL.</span><span class="sxs-lookup"><span data-stu-id="dd7b2-116">No immediate-mode bit exists; the mode in immediate mode refers to usage of OpenGL, rather than to a specific bit of OpenGL state.</span></span>

</dd> <dt>

<span data-ttu-id="dd7b2-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**номер**</span><span class="sxs-lookup"><span data-stu-id="dd7b2-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**index**</span></span>
</dt> <dd>

<span data-ttu-id="dd7b2-118">Одиночное значение, которое интерпретируется как абсолютное значение, а не как нормализованное значение в указанном диапазоне (как и компонент).</span><span class="sxs-lookup"><span data-stu-id="dd7b2-118">A single value that is interpreted as an absolute value, rather than as a normalized value in a specified range (as is a component).</span></span> <span data-ttu-id="dd7b2-119">Цветовые индексы — это имена цветов, которые отменяются на устройстве отображения с помощью цветовой гиперкарты.</span><span class="sxs-lookup"><span data-stu-id="dd7b2-119">Color indexes are the names of colors, which are dereferenced by the display hardware using the color map.</span></span> <span data-ttu-id="dd7b2-120">Индексы обычно маскируются, а не обрабатываются, если они выходят за пределы диапазона.</span><span class="sxs-lookup"><span data-stu-id="dd7b2-120">Indexes are typically masked, rather than clamped, when out of range.</span></span> <span data-ttu-id="dd7b2-121">Например, индекс 0xF7 маскируется к 0x7 при написании в 4-разрядном буфере (цвет или набор элементов).</span><span class="sxs-lookup"><span data-stu-id="dd7b2-121">For example, the index 0xf7 is masked to 0x7 when written to a 4-bit buffer (color or stencil).</span></span> <span data-ttu-id="dd7b2-122">Цветовые индексы и индексы наборов элементов всегда обрабатываются как индексы, а не как компоненты.</span><span class="sxs-lookup"><span data-stu-id="dd7b2-122">Color indexes and stencil indexes are always treated as indexes, never as components.</span></span>

</dd> <dt>

<span data-ttu-id="dd7b2-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRI GL**</span><span class="sxs-lookup"><span data-stu-id="dd7b2-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span></span>
</dt> <dd>

<span data-ttu-id="dd7b2-124">Собственная графическая библиотека Silicon Graphics, разработанная от 1982 до 1992.</span><span class="sxs-lookup"><span data-stu-id="dd7b2-124">Silicon Graphics' proprietary graphics library, developed from 1982 through 1992.</span></span> <span data-ttu-id="dd7b2-125">OpenGL был разработан с использованием IRI GL в качестве отправной точки.</span><span class="sxs-lookup"><span data-stu-id="dd7b2-125">OpenGL was designed with IRIS GL as a starting point.</span></span>

</dd> </dl>

 

 




