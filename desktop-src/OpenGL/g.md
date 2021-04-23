---
title: G (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы G.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 588df117-d03c-4a1f-9666-84004cb3d97b
keywords:
- гамма-коррекция
- геометрическая модель
- геометрические объекты
- геометрические примитивы
- Заливка по методу Гуро
- groups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c369c5c2af949bed221d1afd5fb0c05aebf14849
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105672445"
---
# <a name="g-opengl"></a><span data-ttu-id="bd107-109">G (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="bd107-109">G (OpenGL)</span></span>

<span data-ttu-id="bd107-110">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) G [р](h.md) . [](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="bd107-110">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) G [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="bd107-111"><span id="opengl_gamma_correction"></span><span id="OPENGL_GAMMA_CORRECTION"></span>**гамма-коррекция**</span><span class="sxs-lookup"><span data-stu-id="bd107-111"><span id="opengl_gamma_correction"></span><span id="OPENGL_GAMMA_CORRECTION"></span>**gamma correction**</span></span>
</dt> <dd>

<span data-ttu-id="bd107-112">Функция, применяемая к цветам, хранящимся в буфере кадров, чтобы исправить нелинейный отклик глаза (и иногда монитор) на линейные изменения значений интенсивности цветов.</span><span class="sxs-lookup"><span data-stu-id="bd107-112">A function applied to colors stored in the frame buffer to correct for the nonlinear response of the eye (and sometimes of the monitor) to linear changes in color-intensity values.</span></span>

</dd> <dt>

<span data-ttu-id="bd107-113"><span id="opengl_geometric_model"></span><span id="OPENGL_GEOMETRIC_MODEL"></span>**геометрическая модель**</span><span class="sxs-lookup"><span data-stu-id="bd107-113"><span id="opengl_geometric_model"></span><span id="OPENGL_GEOMETRIC_MODEL"></span>**geometric model**</span></span>
</dt> <dd>

<span data-ttu-id="bd107-114">Вершины координат объекта и параметры, описывающие объект.</span><span class="sxs-lookup"><span data-stu-id="bd107-114">The object-coordinate vertices and parameters that describe an object.</span></span> <span data-ttu-id="bd107-115">Обратите внимание, что OpenGL не определяет синтаксис для геометрических моделей, а является синтаксисом и семантикой для отрисовки геометрических моделей.</span><span class="sxs-lookup"><span data-stu-id="bd107-115">Note that OpenGL doesn't define a syntax for geometric models, but rather a syntax and semantics for the rendering of geometric models.</span></span>

</dd> <dt>

<span data-ttu-id="bd107-116"><span id="opengl_geometric_object"></span><span id="OPENGL_GEOMETRIC_OBJECT"></span>**геометрический объект**</span><span class="sxs-lookup"><span data-stu-id="bd107-116"><span id="opengl_geometric_object"></span><span id="OPENGL_GEOMETRIC_OBJECT"></span>**geometric object**</span></span>
</dt> <dd>

<span data-ttu-id="bd107-117">Геометрическая модель.</span><span class="sxs-lookup"><span data-stu-id="bd107-117">A geometric model.</span></span>

</dd> <dt>

<span data-ttu-id="bd107-118"><span id="opengl_geometric_primitive"></span><span id="OPENGL_GEOMETRIC_PRIMITIVE"></span>**геометрический примитив**</span><span class="sxs-lookup"><span data-stu-id="bd107-118"><span id="opengl_geometric_primitive"></span><span id="OPENGL_GEOMETRIC_PRIMITIVE"></span>**geometric primitive**</span></span>
</dt> <dd>

<span data-ttu-id="bd107-119">Точка, линия или многоугольник.</span><span class="sxs-lookup"><span data-stu-id="bd107-119">A point, line, or polygon.</span></span>

</dd> <dt>

<span data-ttu-id="bd107-120"><span id="opengl_gouraud_shading"></span><span id="OPENGL_GOURAUD_SHADING"></span>**Заливка по методу Гуро**</span><span class="sxs-lookup"><span data-stu-id="bd107-120"><span id="opengl_gouraud_shading"></span><span id="OPENGL_GOURAUD_SHADING"></span>**Gouraud shading**</span></span>
</dt> <dd>

<span data-ttu-id="bd107-121">Плавная интерполяция цветов в многоугольнике или сегменте линии.</span><span class="sxs-lookup"><span data-stu-id="bd107-121">Smooth interpolation of colors across a polygon or line segment.</span></span> <span data-ttu-id="bd107-122">Цвета присваиваются в вершинах и линейно интерполируются по примитиву для создания относительно гладких вариаций в цвете.</span><span class="sxs-lookup"><span data-stu-id="bd107-122">Colors are assigned at vertices and linearly interpolated across the primitive to produce a relatively smooth variation in color.</span></span> <span data-ttu-id="bd107-123">Также называется плавной заливкой.</span><span class="sxs-lookup"><span data-stu-id="bd107-123">Also called smooth shading.</span></span>

</dd> <dt>

<span data-ttu-id="bd107-124"><span id="opengl_group"></span><span id="OPENGL_GROUP"></span>**сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="bd107-124"><span id="opengl_group"></span><span id="OPENGL_GROUP"></span>**group**</span></span>
</dt> <dd>

<span data-ttu-id="bd107-125">Группа из одного, двух, трех или четырех элементов, представляющих каждый пиксел изображения в памяти клиента.</span><span class="sxs-lookup"><span data-stu-id="bd107-125">A group of one, two, three, or four elements that represents each pixel of an image in client memory.</span></span> <span data-ttu-id="bd107-126">Таким образом, в контексте образа памяти клиента группа и пиксель имеют одно и то же действие.</span><span class="sxs-lookup"><span data-stu-id="bd107-126">Thus, in the context of a client memory image, a group and a pixel are the same thing.</span></span>

</dd> </dl>

 

 




