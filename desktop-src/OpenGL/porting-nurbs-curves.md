---
title: Перенос кривых НУРБС
description: Функции OpenGL для рисования кривых НУРБС очень похожи на функции IRI GL. Релевантной последовательности и контрольные точки указываются с помощью функции Глунурбскурве, которая должна содержаться в паре Глубегинкурве/Глуендкурве.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Перенос GL в ГК, кривые НУРБС
- Перенос из IRI GL, НУРБС кривых
- перенос в OpenGL из IRI GL, НУРБС кривых
- Перенос по стандарту OpenGL из IRI GL, НУРБС кривых
- Кривые НУРБС
- кривые
- Перенос GL по IRI, кривые
- Перенос из IRI GL, кривых
- перенос в OpenGL из IRI GL, кривых
- Перенос по стандарту OpenGL из IRI GL, кривых
- НУРБС (неоднородный рациональный B-сплайн)
- Неоднородный рациональный B-сплайн (НУРБС)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411126"
---
# <a name="porting-nurbs-curves"></a><span data-ttu-id="14b1b-116">Перенос кривых НУРБС</span><span class="sxs-lookup"><span data-stu-id="14b1b-116">Porting NURBS Curves</span></span>

<span data-ttu-id="14b1b-117">Функции OpenGL для рисования кривых НУРБС очень похожи на функции IRI GL.</span><span class="sxs-lookup"><span data-stu-id="14b1b-117">The OpenGL functions for drawing NURBS curves are very similar to the IRIS GL functions.</span></span> <span data-ttu-id="14b1b-118">Релевантной последовательности и контрольные точки указываются с помощью функции [**глунурбскурве**](glunurbscurve.md) , которая должна содержаться в паре [**глубегинкурве**](glubegincurve.md)  /  [**глуендкурве**](gluendcurve.md) .</span><span class="sxs-lookup"><span data-stu-id="14b1b-118">You specify knot sequences and control points using a [**gluNurbsCurve**](glunurbscurve.md) function, which must be contained within a [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) pair.</span></span>

<span data-ttu-id="14b1b-119">В следующей таблице перечислены функции IRI GL для рисования НУРБС кривых и их эквивалентных функций OpenGL.</span><span class="sxs-lookup"><span data-stu-id="14b1b-119">The following table lists the IRIS GL functions for drawing NURBS curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="14b1b-120">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="14b1b-120">IRIS GL function</span></span> | <span data-ttu-id="14b1b-121">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="14b1b-121">OpenGL function</span></span>                        | <span data-ttu-id="14b1b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="14b1b-122">Meaning</span></span>                     |
|------------------|----------------------------------------|-----------------------------|
| <span data-ttu-id="14b1b-123">**бгнкурве**</span><span class="sxs-lookup"><span data-stu-id="14b1b-123">**bgncurve**</span></span>     | [<span data-ttu-id="14b1b-124">**глубегинкурве**</span><span class="sxs-lookup"><span data-stu-id="14b1b-124">**gluBeginCurve**</span></span>](glubegincurve.md) | <span data-ttu-id="14b1b-125">Начинает определение кривой.</span><span class="sxs-lookup"><span data-stu-id="14b1b-125">Begins a curve definition.</span></span>  |
| <span data-ttu-id="14b1b-126">**нурбскурве**</span><span class="sxs-lookup"><span data-stu-id="14b1b-126">**nurbscurve**</span></span>   | [<span data-ttu-id="14b1b-127">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="14b1b-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="14b1b-128">Задает атрибуты кривой.</span><span class="sxs-lookup"><span data-stu-id="14b1b-128">Specifies curve attributes.</span></span> |
| <span data-ttu-id="14b1b-129">**ендкурве**</span><span class="sxs-lookup"><span data-stu-id="14b1b-129">**endcurve**</span></span>     | [<span data-ttu-id="14b1b-130">**глуендкурве**</span><span class="sxs-lookup"><span data-stu-id="14b1b-130">**gluEndCurve**</span></span>](gluendcurve.md)     | <span data-ttu-id="14b1b-131">Завершает определение кривой.</span><span class="sxs-lookup"><span data-stu-id="14b1b-131">Ends a curve definition.</span></span>    |



 

<span data-ttu-id="14b1b-132">Сопоставьте координаты положения, текстуры и цвета, выполнив каждую из них как отдельные **глунурбскурве** внутри пары начало/конец.</span><span class="sxs-lookup"><span data-stu-id="14b1b-132">Associate position, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** inside the begin/end pair.</span></span> <span data-ttu-id="14b1b-133">Можно сделать не более одного вызова **глунурбскурве** для каждого фрагмента данных цвета, расположения и текстуры в пределах одной пары **глубегинкурве/глуендкурве** .</span><span class="sxs-lookup"><span data-stu-id="14b1b-133">You can make no more than one call to **gluNurbsCurve** for each piece of color, position, and texture data within a single **gluBeginCurve/gluEndCurve** pair.</span></span> <span data-ttu-id="14b1b-134">Необходимо выполнить ровно один вызов, чтобы описать расположение кривой ( \_ Описание GL «Карта1» \_ вершиной \_ 3 или GL \_ «Карта1» \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="14b1b-134">You must make exactly one call to describe the position of the curve (a GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4 description).</span></span> <span data-ttu-id="14b1b-135">При вызове **глуендкурве** кривая разбивается на сегменты линии, а затем готовится к просмотру.</span><span class="sxs-lookup"><span data-stu-id="14b1b-135">When you call **gluEndCurve**, the curve is tessellated into line segments and then rendered.</span></span>

<span data-ttu-id="14b1b-136">В следующей таблице перечислены типы кривых IRI GL и OpenGL НУРБС.</span><span class="sxs-lookup"><span data-stu-id="14b1b-136">The following table lists IRIS GL and OpenGL NURBS curve types.</span></span>



| <span data-ttu-id="14b1b-137">Тип IRI GL</span><span class="sxs-lookup"><span data-stu-id="14b1b-137">IRIS GL type</span></span> | <span data-ttu-id="14b1b-138">Тип OpenGL</span><span class="sxs-lookup"><span data-stu-id="14b1b-138">OpenGL type</span></span>                  | <span data-ttu-id="14b1b-139">Значение</span><span class="sxs-lookup"><span data-stu-id="14b1b-139">Meaning</span></span>                                 |
|--------------|------------------------------|-----------------------------------------|
| <span data-ttu-id="14b1b-140">N \_ V3D</span><span class="sxs-lookup"><span data-stu-id="14b1b-140">N\_V3D</span></span>       | <span data-ttu-id="14b1b-141">GL \_ «Карта1», \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="14b1b-141">GL\_MAP1\_VERTEX\_3</span></span>          | <span data-ttu-id="14b1b-142">Полиномная кривая.</span><span class="sxs-lookup"><span data-stu-id="14b1b-142">Polynomial curve.</span></span>                       |
| <span data-ttu-id="14b1b-143">N \_ V3DR</span><span class="sxs-lookup"><span data-stu-id="14b1b-143">N\_V3DR</span></span>      | <span data-ttu-id="14b1b-144">\_«Карта1»ная \_ вершина GL \_ 4</span><span class="sxs-lookup"><span data-stu-id="14b1b-144">GL\_MAP1\_VERTEX\_4</span></span>          | <span data-ttu-id="14b1b-145">Рациональная кривая.</span><span class="sxs-lookup"><span data-stu-id="14b1b-145">Rational curve.</span></span>                         |
|              | <span data-ttu-id="14b1b-146">\_«Карта1» \_ текстура GL \_ курд\_\*</span><span class="sxs-lookup"><span data-stu-id="14b1b-146">GL\_MAP1\_TEXTURE\_COORD\_\*</span></span> | <span data-ttu-id="14b1b-147">Точки управления — это координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="14b1b-147">Control points are texture coordinates.</span></span> |
|              | <span data-ttu-id="14b1b-148">«Карта1» GL ( \_ \_ Обычная)</span><span class="sxs-lookup"><span data-stu-id="14b1b-148">GL\_MAP1\_NORMAL</span></span>             | <span data-ttu-id="14b1b-149">Контрольные точки являются нормальными.</span><span class="sxs-lookup"><span data-stu-id="14b1b-149">Control points are normals.</span></span>             |



 

<span data-ttu-id="14b1b-150">Дополнительные сведения о доступных типах оценщиков см. в разделе [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="14b1b-150">For more information on available evaluator types, see [**glMap1**](glmap1.md).</span></span>

<span data-ttu-id="14b1b-151">??</span><span class="sxs-lookup"><span data-stu-id="14b1b-151">??</span></span>

 

 




