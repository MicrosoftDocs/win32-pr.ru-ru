---
title: Использование процесса сопоставления цветов в WCS
description: Сопоставление цветов WCS основано на профилях устройств.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Цветовая система Windows (WCS), сопоставление цветов
- WCS (цветовая система Windows), сопоставление цветов
- Управление цветом изображений, сопоставление цветов
- Управление цветом, сопоставление цветов
- цвета, сопоставление цветов
- Сопоставление цветов
- Цветовая система Windows (WCS), профили устройств
- WCS (цветовая система Windows), профили устройств
- Управление цветом изображений, профили устройств
- Управление цветом, профили устройств
- цвета, профили устройств
- Цветовая система Windows (WCS), профили
- WCS (цветовая система Windows), профили
- Управление цветом изображений, профили
- Управление цветом, профили
- цвета, профили
- профили устройств
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719811"
---
# <a name="using-the-color-mapping-process-with-wcs"></a><span data-ttu-id="98835-120">Использование процесса сопоставления цветов в WCS</span><span class="sxs-lookup"><span data-stu-id="98835-120">Using The Color Mapping Process with WCS</span></span>

<span data-ttu-id="98835-121">Сопоставление цветов WCS основано на [профилях устройств](d.md).</span><span class="sxs-lookup"><span data-stu-id="98835-121">WCS color mapping is based on [device profiles](d.md).</span></span> <span data-ttu-id="98835-122">Они предоставляются поставщиками аппаратных устройств цвета и устанавливаются при установке устройства.</span><span class="sxs-lookup"><span data-stu-id="98835-122">These are supplied by vendors of color hardware devices and installed when a device is installed.</span></span> <span data-ttu-id="98835-123">Если сопоставление цветов используется программой приложения, WCS получает доступ к профилю устройства образа, чтобы получить сведения, необходимые для преобразования изображения на ПК.</span><span class="sxs-lookup"><span data-stu-id="98835-123">When color mapping is used by an application program, WCS accesses the device profile of the image to get the information needed to convert the image to the PCS.</span></span> <span data-ttu-id="98835-124">Преобразование выполняется модулем CMM.</span><span class="sxs-lookup"><span data-stu-id="98835-124">The conversion is done by the CMM.</span></span>

<span data-ttu-id="98835-125">Профиль устройства можно внедрить в само изображение.</span><span class="sxs-lookup"><span data-stu-id="98835-125">A device profile can be embedded into the image itself.</span></span> <span data-ttu-id="98835-126">Поэтому профиль устройства перемещается вместе с изображением даже через Интернет.</span><span class="sxs-lookup"><span data-stu-id="98835-126">So the device profile travels with the image, even across the Internet.</span></span> <span data-ttu-id="98835-127">Пользователю не требуется исходное устройство, чтобы получить точное сопоставление цветов.</span><span class="sxs-lookup"><span data-stu-id="98835-127">A user does not need the source device to get an accurate color mapping.</span></span> <span data-ttu-id="98835-128">Если у образа нет профиля устройства, в качестве значения по умолчанию используется пространство sRGB.</span><span class="sxs-lookup"><span data-stu-id="98835-128">If an image does not have a device profile, the sRGB space is used as a default.</span></span> <span data-ttu-id="98835-129">Дополнительные сведения см. в разделе [Использование управления цветом в Интернете](using-color-management-on-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="98835-129">For more details, see [Using Color Management on the Internet](using-color-management-on-the-internet.md).</span></span>

<span data-ttu-id="98835-130">Обратите внимание, что приложения, использующие WCS, не должны внедрять профиль sRGB в изображение.</span><span class="sxs-lookup"><span data-stu-id="98835-130">Note that applications which use WCS should never embed the sRGB profile into an image.</span></span> <span data-ttu-id="98835-131">Цветовое пространство sRGB обеспечивает стандартизованное цветовое пространство, переносимое на все устройства.</span><span class="sxs-lookup"><span data-stu-id="98835-131">The sRGB color space provides a standardized color space that is portable across all devices.</span></span> <span data-ttu-id="98835-132">Она автоматически доступна для пользователей Windows 98 и более поздних версий, а также для Windows 2000 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="98835-132">It is automatically available to users of Windows 98 and later as well as Windows 2000 and later.</span></span> <span data-ttu-id="98835-133">Поэтому ему не нужно перемещаться вместе с изображением.</span><span class="sxs-lookup"><span data-stu-id="98835-133">Therefore, it does not need to travel with the image.</span></span>

<span data-ttu-id="98835-134">После того как цвета изображения будут установлены на [ПК](p.md), WCS получает доступ к профилю устройства на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="98835-134">After the image colors are in the [PCS](p.md), WCS accesses the device profile of the destination device.</span></span> <span data-ttu-id="98835-135">Он получает CMM для преобразования цветов изображения из компьютеров в цветовой охват целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="98835-135">It gets the CMM to convert the image colors from PCS to the gamut of the destination device.</span></span>

<span data-ttu-id="98835-136">Более сложное сопоставление цветов также можно выполнить с помощью WCS.</span><span class="sxs-lookup"><span data-stu-id="98835-136">More complex color mapping can also be done with WCS.</span></span> <span data-ttu-id="98835-137">Например, его можно использовать для получения представления о том, что изображение, созданное на дисплее, будет выглядеть при печати на лазерном принтере с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="98835-137">For example, it can be used to get an idea of what an image created on a video display would look like when printed on a high resolution laser printer.</span></span> <span data-ttu-id="98835-138">Пример становится более сложным, если имеется только стандартный струйный принтер, на котором необходимо выполнить предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="98835-138">The example gets more complex if there is only a standard inkjet printer on which to preview it.</span></span> <span data-ttu-id="98835-139">Изображение может быть преобразовано из гаммы экрана в цветовой охват струйного принтера.</span><span class="sxs-lookup"><span data-stu-id="98835-139">The image can be converted from the gamut of the display, into the gamut of the inkjet printer.</span></span> <span data-ttu-id="98835-140">Из него можно преобразовать в цветовой охват лазерного принтера.</span><span class="sxs-lookup"><span data-stu-id="98835-140">From there it can converted into the gamut of the laser printer.</span></span> <span data-ttu-id="98835-141">Полученный образ может быть напечатан на струйном принтере.</span><span class="sxs-lookup"><span data-stu-id="98835-141">The resulting image can be printed on the inkjet printer.</span></span> <span data-ttu-id="98835-142">Конечно, при печати на цветном лазерном принтере изображение будет иметь более высокое разрешение.</span><span class="sxs-lookup"><span data-stu-id="98835-142">Of course the image would be at a higher resolution when printed on the color laser printer.</span></span> <span data-ttu-id="98835-143">Тем не менее цвета изображения проверки подлинности, напечатанного на струйном принтере, будут близки к цветам, печатаемым лазерным принтером.</span><span class="sxs-lookup"><span data-stu-id="98835-143">However, the colors of the proofing image printed on the inkjet printer would be a close match to the colors that the laser printer would print.</span></span>

<span data-ttu-id="98835-144">Способ преобразования в этом примере — преобразование цветов изображения из цветового охвата экрана в ПК.</span><span class="sxs-lookup"><span data-stu-id="98835-144">The way the conversions in the example are accomplished is to convert the image colors from the display's gamut into the PCS.</span></span> <span data-ttu-id="98835-145">После того как цвета изображения будут преобразованы на ПК, профиль устройства струйного принтера будет использоваться для преобразования их в цветовой охват струйного принтера.</span><span class="sxs-lookup"><span data-stu-id="98835-145">After the image colors are converted into the PCS, the device profile of the inkjet printer would be used to transform them into the gamut of the inkjet printer.</span></span> <span data-ttu-id="98835-146">Далее будет использоваться преобразование «цветовой охват в ПК», чтобы переместить цвета обратно на ПК.</span><span class="sxs-lookup"><span data-stu-id="98835-146">Next, the gamut to PCS transform would be used to move the colors back to the PCS.</span></span> <span data-ttu-id="98835-147">В этом случае профиль устройства лазерного принтера используется для преобразования цветов с компьютеров в цветовой охват лазерного принтера.</span><span class="sxs-lookup"><span data-stu-id="98835-147">From there, the laser printer's device profile is used to convert the colors from PCS into the gamut of the laser printer.</span></span>

<span data-ttu-id="98835-148">Возможность легко преобразовывать цвета из цветового охвата устройства на ПК и обратно позволяет использовать цвета изображений, предназначенные для одного цветового устройства вывода, для проверки практически любой другой.</span><span class="sxs-lookup"><span data-stu-id="98835-148">The ability to easily transform colors from a device gamut to the PCS and back again enables image colors intended for one color output device to be proofed on almost any other.</span></span>

<span data-ttu-id="98835-149">В предыдущем примере описание отличается от реальной процедуры для ясности.</span><span class="sxs-lookup"><span data-stu-id="98835-149">In the preceding example, the description varies from the actual procedure somewhat for clarity.</span></span> <span data-ttu-id="98835-150">На практике все преобразования, упомянутые в предыдущем абзаце, будут объединены в одно преобразование.</span><span class="sxs-lookup"><span data-stu-id="98835-150">In reality, all of the transformations mentioned in the preceding paragraph would be concatenated into a single transformation.</span></span>

 

 




