---
title: Цветовые пространства CMY и CMYK
description: Цветовые пространства КМИ и CMYK часто используются в цветовой печати. КМИ цветовое пространство в качестве основного цвета использует голубой, пурпурный и желтый (КМИ). Дополнительные цвета — красный, зеленый и синий.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Цветовая система Windows (WCS), КМИ Color Spaces
- WCS (цветовая система Windows), цветовые пространства КМИ
- Управление цветом изображений, цветовые пространства КМИ
- Управление цветом, цветовые пространства КМИ
- цвета, КМИ цветовые пространства
- цветовые пространства, КМИ
- КМИ цветовые пространства
- Цветовая система Windows (WCS), цветовые пространства CMYK
- WCS (цветовая система Windows), цветовые пространства CMYK
- Управление цветом изображений, цветовые пространства CMYK
- Управление цветом, Кмикколорные пространства
- цвета, цветовые пространства CMYK
- цветовые пространства, CMYK
- Цветовые пространства CMYK
- Зеленовато-голубой
- Пурпурный
- yellow
- голубой пурпурный желтый (КМИ)
- КМИ (голубой пурпурный желтый)
- голубой пурпурный желтый черный (CMYK)
- CMYK (голубой пурпурный желтый черный)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719801"
---
# <a name="cmy-and-cmyk-color-spaces"></a><span data-ttu-id="d4ab3-126">Цветовые пространства CMY и CMYK</span><span class="sxs-lookup"><span data-stu-id="d4ab3-126">CMY and CMYK Color Spaces</span></span>

<span data-ttu-id="d4ab3-127">[Цветовые пространства](c.md) КМИ и CMYK часто используются в цветовой печати.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-127">The CMY and CMYK [color spaces](c.md) are often used in color printing.</span></span> <span data-ttu-id="d4ab3-128">КМИ цветовое пространство в качестве [основного цвета](p.md)использует голубой, пурпурный и желтый (КМИ).</span><span class="sxs-lookup"><span data-stu-id="d4ab3-128">A CMY color space uses cyan, magenta, and yellow (CMY) as its [primary colors](p.md).</span></span> <span data-ttu-id="d4ab3-129">Дополнительные цвета — красный, зеленый и синий.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-129">Red, green, and blue are the secondary colors.</span></span>

<span data-ttu-id="d4ab3-130">На следующих рисунках представлены цветовые представления цветового пространства КМИ.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-130">The following figures are color representations of the CMY color space.</span></span> <span data-ttu-id="d4ab3-131">Цветовое пространство КМИ нормализовано.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-131">The CMY color space is normalized.</span></span>

![КМИ. куб цветового пространства в максимальных значениях](images/cmyclrs1.png)

![КМИ. куб цветового пространства в минимальных значениях](images/cmyclrs2.png)

<span data-ttu-id="d4ab3-134">КМИ цветовое пространство является вычитанием.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-134">The CMY color space is subtractive.</span></span> <span data-ttu-id="d4ab3-135">Таким образом, белый цвет находится в (0,0, 0,0, 0,0), а черный — в (1,0, 1,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="d4ab3-135">Therefore, white is at (0.0, 0.0, 0.0) and black is at (1.0, 1.0, 1.0).</span></span> <span data-ttu-id="d4ab3-136">Если вы начинаете с белого и не вычитаете цвета, вы получаете белый цвет.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-136">If you start with white and subtract no colors, you get white.</span></span> <span data-ttu-id="d4ab3-137">Если начать с белого и прочесть все цвета одинаково, вы получаете черный цвет.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-137">If you start with white and subtract all colors equally, you get black.</span></span>

<span data-ttu-id="d4ab3-138">Цветовое пространство CMYK является разновидностью модели КМИ.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-138">The CMYK color space is a variation on the CMY model.</span></span> <span data-ttu-id="d4ab3-139">Он добавляет черный цвет (голубой, пурпурный, желтый и черный).</span><span class="sxs-lookup"><span data-stu-id="d4ab3-139">It adds black (Cyan, Magenta, Yellow, and blacK).</span></span> <span data-ttu-id="d4ab3-140">Цветовое пространство CMYK закрывает зазор между теории и практикой.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-140">The CMYK color space closes the gap between theory and practice.</span></span> <span data-ttu-id="d4ab3-141">Теоретически, дополнительный черный компонент не требуется.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-141">In theory, the extra black component is not needed.</span></span> <span data-ttu-id="d4ab3-142">Тем не менее, опыт работы с различными типами красок и бумаг показывает, что при смешении одинаковых компонентов голубого, пурпурного и желтого красок результат обычно является темным коричневый, а не черным.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-142">However, experience with various types of inks and papers has shown that when equal components of cyan, magenta, and yellow inks are mixed, the result is usually a dark brown, not black.</span></span> <span data-ttu-id="d4ab3-143">Добавление черной краски в набор решает эту проблему.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-143">Adding black ink to the mix solves this problem.</span></span>

<span data-ttu-id="d4ab3-144">Цветовые пространства КМИ и CMYK могут быть независимыми от устройства, но чаще всего они используются в ссылке на конкретное устройство.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-144">The CMY and CMYK colors spaces can be device independent, but most often they are used in reference to a specific device.</span></span>

 

 




