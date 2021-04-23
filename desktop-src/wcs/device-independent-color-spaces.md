---
title: Аппаратно-независимые цветовые пространства
description: При распознавании потребности в стандартных, аппаратно-независимых цветовых измерениях, Комиссии International de Л'еклаираже (Международная комиссия по освещения) или ЦИЕ создано цветовое пространство на основе \ 0034; мнимой \ 0034; Основные цвета.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Цветовая система Windows (WCS), аппаратно-независимые цветовые пространства
- WCS (цветовая система Windows), аппаратно-независимые цветовые пространства
- Управление цветом изображений, аппаратно-независимые цветовые пространства
- Управление цветом, аппаратно-независимые цветовые пространства
- цвета, независимые от устройства цветовые пространства
- цветовые пространства, независимые от устройства
- аппаратно-независимые цветовые пространства
- Комиссии International de Л'еклаираже (ЦИЕ)
- Международная комиссия по освещения (ЦИЕ)
- ЦИЕ (Комиссия International de Л'еклаираже)
- ЦИЕ (Международная комиссия по освещения)
- Цветовое пространство ЦИЕКСИЗ
- Цветовое пространство XYZ
- цветовое пространство sRGB
- цветовые пространства, ЦИЕКСИЗ
- цветовые пространства, sRGB
- цветовые пространства, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719822"
---
# <a name="device-independent-color-spaces"></a><span data-ttu-id="4ece1-120">Аппаратно-независимые цветовые пространства</span><span class="sxs-lookup"><span data-stu-id="4ece1-120">Device-Independent Color Spaces</span></span>

<span data-ttu-id="4ece1-121">Учитывая потребность в стандартном, независимом от устройства цветовых измерениях, комиссная кол'еклаираже (Международная комиссия по освещения) или ЦИЕ, создала [цветовое пространство](c.md) на основе «мнимой» [основных цветов](p.md).</span><span class="sxs-lookup"><span data-stu-id="4ece1-121">Recognizing the need for standard, device-independent color measurements, the Commission International de l'Eclairage (International Commission on Illumination), or CIE, created a [color space](c.md) based on "imaginary" [primary colors](p.md).</span></span> <span data-ttu-id="4ece1-122">Фактическое устройство для создания цветов в этом цветовом пространстве не ожидается.</span><span class="sxs-lookup"><span data-stu-id="4ece1-122">No actual device is expected to produce colors in this color space.</span></span> <span data-ttu-id="4ece1-123">Он используется как средство преобразования цветов из одного цветового пространства в другое.</span><span class="sxs-lookup"><span data-stu-id="4ece1-123">It is used as a means of converting colors from one color space to another.</span></span> <span data-ttu-id="4ece1-124">Основные цвета в этом цветовом пространстве — это абстрактные цвета X, Y и Z.</span><span class="sxs-lookup"><span data-stu-id="4ece1-124">The primary colors in this color space are the abstract colors X, Y, and Z.</span></span>

<span data-ttu-id="4ece1-125">Цветовое пространство 1931 ЦИЕКСИЗ широко используется в качестве основания для преобразования цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="4ece1-125">The 1931 CIEXYZ color space is widely used as the basis for color space conversion.</span></span> <span data-ttu-id="4ece1-126">Тем не менее, при подъеме Интернета пропускная способность не слишком громоздким.</span><span class="sxs-lookup"><span data-stu-id="4ece1-126">With the rise of the Internet, however, bandwidth considerations have made the XYZ color space unwieldy.</span></span> <span data-ttu-id="4ece1-127">Обмен изображениями по ограниченной пропускной способности Интернета требует более компактной [цветовой модели](c.md).</span><span class="sxs-lookup"><span data-stu-id="4ece1-127">The exchange of images over the limited bandwidth of the Internet necessitates a more compact [color model](c.md).</span></span>

<span data-ttu-id="4ece1-128">В результате Hewlett-Packard и Майкрософт предложили внедрение стандартного предопределенного цветового пространства RGB, известного как sRGB, чтобы обеспечить точное управление цветом с очень малой нагрузкой данных.</span><span class="sxs-lookup"><span data-stu-id="4ece1-128">As a result, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined RGB color space known as sRGB, so as to allow accurate color management with very little data overhead.</span></span> <span data-ttu-id="4ece1-129">Этот стандарт утвержден в качестве формального международного стандарта IEC (IEC) как IEC 61966-2-1: мультимедийные системы и измерения Екуипментколаур и Манажементпарт 2-1: цвет Манажементдефаулт RGB.</span><span class="sxs-lookup"><span data-stu-id="4ece1-129">This standard has been approved as a formal international standard by the International Electrotechnical Commission (IEC) as IEC 61966-2-1: Multimedia Systems and EquipmentColour Measurement and ManagementPart 2-1: Colour ManagementDefault RGB Colour Space.</span></span> <span data-ttu-id="4ece1-130">Он доступен непосредственно из IEC по адресу <https://www.iec.ch/> .</span><span class="sxs-lookup"><span data-stu-id="4ece1-130">It is available directly from the IEC at <https://www.iec.ch/>.</span></span> <span data-ttu-id="4ece1-131">Сведения, обсуждающие технические проблемы, связанные с sRGB, доступны в Интернете по адресу:</span><span class="sxs-lookup"><span data-stu-id="4ece1-131">Information discussing the technical issues involved in sRGB is available on the Internet at:</span></span>

[<span data-ttu-id="4ece1-132">Стандартное цветовое пространство по умолчанию для Internet-sRGB</span><span class="sxs-lookup"><span data-stu-id="4ece1-132">A Standard Default Color Space for the Internet - sRGB</span></span>](https://www.w3.org/Graphics/Color/sRGB.html)

<span data-ttu-id="4ece1-133">Техническая документация по техническим вопросам, связанным с sRGB, sRGB. HLP, доступна в \\ папке справки в справочнике по программированию WCS 1,0 в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="4ece1-133">A help-file version of a white paper discussing the technical issues involved in sRGB, sRGB.HLP, is available in the \\Help folder of the WCS 1.0 Programmer's Reference in the Platform SDK.</span></span>

<span data-ttu-id="4ece1-134">В различных форматах файлов может использоваться или добавляться флаг, указывающий, что изображение находится в цветовом пространстве sRGB.</span><span class="sxs-lookup"><span data-stu-id="4ece1-134">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="4ece1-135">В формате, не зависящем от устройства Windows (DIB), установка для элемента **bV5CSType** структуры [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) значение LCS \_ sRGB указывает, что цвета DIB находятся в цветовом пространстве sRGB.</span><span class="sxs-lookup"><span data-stu-id="4ece1-135">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) structure to LCS\_sRGB specifies that the DIB colors are in the sRGB color space.</span></span>

 

 




