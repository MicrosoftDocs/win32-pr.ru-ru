---
title: Преобразование и сопоставление цветов
description: Процесс преобразования цветов из одного цветового пространства в другое называется преобразованием цветов.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Цветовая система Windows (WCS), преобразование цветов
- WCS (цветовая система Windows), преобразование цветов
- Управление цветом изображений, преобразование цветов
- Управление цветом, преобразование цветов
- цвета, преобразование цветов
- Преобразование цветов
- Цветовая система Windows (WCS), сопоставление цветов
- WCS (цветовая система Windows), сопоставление цветов
- Управление цветом изображений, сопоставление цветов
- Управление цветом, сопоставление цветов
- цвета, сопоставление цветов
- Сопоставление цветов
- Цветовая система Windows (WCS), сопоставление цветов
- WCS (цветовая система Windows), сопоставление цветов
- Управление цветом изображений, сопоставление цветов
- Управление цветом, сопоставление цветов
- цвета, сопоставление цветов
- Сопоставление цветов
- Белая точка
- колорантс
- гамма-коррекция
- спектр
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719824"
---
# <a name="color-conversion-and-color-matching"></a><span data-ttu-id="06532-125">Преобразование и сопоставление цветов</span><span class="sxs-lookup"><span data-stu-id="06532-125">Color Conversion and Color Matching</span></span>

<span data-ttu-id="06532-126">Процесс преобразования цветов из одного [цветового пространства](c.md) в другое называется *преобразованием цветов*.</span><span class="sxs-lookup"><span data-stu-id="06532-126">The process of converting colors from one [color space](c.md) to another is called *color conversion*.</span></span> <span data-ttu-id="06532-127">Все цвета в цветовом пространстве фиксированы относительно [белой точки](w.md)цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="06532-127">All colors in a color space are fixed relative to the color space's [white point](w.md).</span></span> <span data-ttu-id="06532-128">Так как белая точка цветового пространства отличается от устройства к устройству, преобразованный цвет должен соответствовать его визуально ближайшему цвету в целевом пространстве цветов.</span><span class="sxs-lookup"><span data-stu-id="06532-128">Since the white point of a color space varies from device to device, a converted color must then be matched to its visually closest color in the destination color space.</span></span> <span data-ttu-id="06532-129">Этот процесс называется *сопоставлением цветов*.</span><span class="sxs-lookup"><span data-stu-id="06532-129">This process is called *color mapping*.</span></span>

<span data-ttu-id="06532-130">Например, при наличии цифрового изображения, созданного на экране, оно может находиться в цветовом пространстве RGB, зависящем от устройства.</span><span class="sxs-lookup"><span data-stu-id="06532-130">For example, if you have a digital image that you created on your display, it may be in a device-dependent RGB color space.</span></span> <span data-ttu-id="06532-131">Если вы хотите распечатать его на принтере, его необходимо преобразовать в цветовое пространство принтера.</span><span class="sxs-lookup"><span data-stu-id="06532-131">If you want to print it on a printer, it must be converted to the printer's color space.</span></span> <span data-ttu-id="06532-132">Так как принтер, вероятно, использует цветовое пространство CMYK, зависящее от устройства, все значения RGB необходимо преобразовать в ЦИМК.</span><span class="sxs-lookup"><span data-stu-id="06532-132">Since the printer probably uses a device-dependent CMYK color space, all RGB values must be converted to CYMK.</span></span> <span data-ttu-id="06532-133">Это [преобразование цвета](c.md).</span><span class="sxs-lookup"><span data-stu-id="06532-133">This is [color conversion](c.md).</span></span> <span data-ttu-id="06532-134">Когда значения задаются с точки зрения ЦИМК пространства, они должны соответствовать ближайшему цвету, который может создать принтер.</span><span class="sxs-lookup"><span data-stu-id="06532-134">Once the values are specified in terms of the CYMK space, they need to be matched to the closest color that the printer can produce.</span></span> <span data-ttu-id="06532-135">Это называется сопоставлением цветов или сопоставлениями [цветов](c.md).</span><span class="sxs-lookup"><span data-stu-id="06532-135">This is called color mapping or [color matching](c.md).</span></span>

<span data-ttu-id="06532-136">Как при преобразовании цветов, так и при сопоставлении цветов необходимо учитывать ряд факторов для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="06532-136">Both color conversion and color mapping must take into account a number of device-specific factors.</span></span> <span data-ttu-id="06532-137">Например, стандартные блоки изображений экрана — это пикселы.</span><span class="sxs-lookup"><span data-stu-id="06532-137">For instance, the building blocks of screen images are pixels.</span></span> <span data-ttu-id="06532-138">Каждый пиксель имеет заданное число битов для хранения значения индекса цвета или цвета.</span><span class="sxs-lookup"><span data-stu-id="06532-138">Each pixel has a set number of bits to store its color or color index value.</span></span> <span data-ttu-id="06532-139">Число бит на пиксель зависит от типа используемого интерфейса дисплея и видеоадаптера, а также от режима, в котором установлен адаптер.</span><span class="sxs-lookup"><span data-stu-id="06532-139">The number of bits per pixel depends on the type of display and display adapter being used, and the mode to which that the adapter is set.</span></span> <span data-ttu-id="06532-140">Большинство типов принтеров использует разные [колорантс](c.md) и печать с определенными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="06532-140">Most every printer type uses different [colorants](c.md) and prints at particular resolutions.</span></span>

<span data-ttu-id="06532-141">Кроме того, характеристики физического тона устройства часто отличаются на разных устройствах.</span><span class="sxs-lookup"><span data-stu-id="06532-141">In addition, the physical tone characteristics of a device are often different on different devices.</span></span> <span data-ttu-id="06532-142">Например, когда мониторы компьютеров получают цвета, они могут отличаться от них, если они были созданы при печати нажатия.</span><span class="sxs-lookup"><span data-stu-id="06532-142">For instance, when colors are produced by computer monitors, they can appear different than they would if they were produced on a printing press.</span></span> <span data-ttu-id="06532-143">Фактор коррекции, называемый *гамма-коррекцией*, часто используется для компенсации таких различий.</span><span class="sxs-lookup"><span data-stu-id="06532-143">A correction factor, called *gamma correction*, is frequently used to compensate for such differences.</span></span>

<span data-ttu-id="06532-144">Результатом этих факторов, зависящих от устройства, является то, что каждое цветовое устройство имеет определенный набор цветов, которые он может создать.</span><span class="sxs-lookup"><span data-stu-id="06532-144">The result of these device-dependent factors is that each color device has a particular set of colors that it can produce.</span></span> <span data-ttu-id="06532-145">Этот набор цветов называется его *охватом*.</span><span class="sxs-lookup"><span data-stu-id="06532-145">This color set is known as its *gamut*.</span></span> <span data-ttu-id="06532-146">Чтобы выполнить преобразование цвета и сопоставление цветов, цвета изображения должны быть преобразованы из цветового пространства исходного устройства в цветовое пространство целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="06532-146">To perform color conversion and color mapping, the colors in an image must be converted from the color space and gamut of the source device into the color space of the destination device.</span></span> <span data-ttu-id="06532-147">Затем они сопоставляются с охватом целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="06532-147">They are then matched into the gamut of the destination device.</span></span>

 

 




