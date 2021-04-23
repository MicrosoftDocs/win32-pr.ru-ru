---
title: Макросы для значений и цветов CMYK
description: Следующие макросы полезны при управлении значениями CMYK.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Цветовая система Windows (WCS), макросы CMYK
- WCS (цветовая система Windows), макросы CMYK
- Управление цветом изображений, макросы CMYK
- Управление цветом, макросы CMYK
- цвета, макросы CMYK
- Справочник по WCS, макросы CMYK
- Справочник по макросам WCS, CMYK
- Макросы CMYK
- голубой пурпурный желтый черный (CMYK)
- CMYK (голубой пурпурный желтый черный)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719844"
---
# <a name="macros-for-cmyk-values-and-colors"></a><span data-ttu-id="b0391-113">Макросы для значений и цветов CMYK</span><span class="sxs-lookup"><span data-stu-id="b0391-113">Macros for CMYK Values and Colors</span></span>

<span data-ttu-id="b0391-114">Следующие макросы полезны при управлении значениями CMYK.</span><span class="sxs-lookup"><span data-stu-id="b0391-114">The following macros are useful in manipulating CMYK values.</span></span>



| <span data-ttu-id="b0391-115">Макрос</span><span class="sxs-lookup"><span data-stu-id="b0391-115">Macro</span></span>                          | <span data-ttu-id="b0391-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b0391-116">Description</span></span>                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="b0391-117">**ИЗОБРАЖЕНИЯ**</span><span class="sxs-lookup"><span data-stu-id="b0391-117">**CMYK**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | <span data-ttu-id="b0391-118">Формирует значение CMYK из отдельных значений голубого, пурпурного, желтого и черного.</span><span class="sxs-lookup"><span data-stu-id="b0391-118">Builds a CMYK value from individual cyan, magenta, yellow, and black values.</span></span> |
| [<span data-ttu-id="b0391-119">**жетквалуе**</span><span class="sxs-lookup"><span data-stu-id="b0391-119">**GetCValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | <span data-ttu-id="b0391-120">Извлекает значение голубого цвета из значения цвета CMYK.</span><span class="sxs-lookup"><span data-stu-id="b0391-120">Retrieves the cyan color value from a CMYK color value.</span></span>                      |
| [<span data-ttu-id="b0391-121">**жетквалуе**</span><span class="sxs-lookup"><span data-stu-id="b0391-121">**GetKValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | <span data-ttu-id="b0391-122">Извлекает значение черного цвета из значения цвета CMYK.</span><span class="sxs-lookup"><span data-stu-id="b0391-122">Retrieves the black color value from a CMYK color value.</span></span>                     |
| [<span data-ttu-id="b0391-123">**жетмвалуе**</span><span class="sxs-lookup"><span data-stu-id="b0391-123">**GetMValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | <span data-ttu-id="b0391-124">Извлекает Пурпурное значение из значения цвета CMYK.</span><span class="sxs-lookup"><span data-stu-id="b0391-124">Retrieves the magenta value from a CMYK color value.</span></span>                         |
| [<span data-ttu-id="b0391-125">**жетивалуе**</span><span class="sxs-lookup"><span data-stu-id="b0391-125">**GetYValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | <span data-ttu-id="b0391-126">Извлекает значение желтого цвета из значения цвета CMYK.</span><span class="sxs-lookup"><span data-stu-id="b0391-126">Retrieves the yellow color value from a CMYK color value.</span></span>                    |



 

<span data-ttu-id="b0391-127">В качестве цвета используются следующие макросы.</span><span class="sxs-lookup"><span data-stu-id="b0391-127">The following macros are used with color.</span></span>



| <span data-ttu-id="b0391-128">Макрос</span><span class="sxs-lookup"><span data-stu-id="b0391-128">Macro</span></span>                                | <span data-ttu-id="b0391-129">Описание</span><span class="sxs-lookup"><span data-stu-id="b0391-129">Description</span></span>                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0391-130">**жетбвалуе**</span><span class="sxs-lookup"><span data-stu-id="b0391-130">**GetBValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | <span data-ttu-id="b0391-131">Возвращает значение синего цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="b0391-131">Gets an RGB blue value.</span></span>                                                                                                                               |
| [<span data-ttu-id="b0391-132">**жетгвалуе**</span><span class="sxs-lookup"><span data-stu-id="b0391-132">**GetGValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | <span data-ttu-id="b0391-133">Возвращает зеленое значение RGB.</span><span class="sxs-lookup"><span data-stu-id="b0391-133">Gets an RGB green value.</span></span>                                                                                                                              |
| [<span data-ttu-id="b0391-134">**RValue**</span><span class="sxs-lookup"><span data-stu-id="b0391-134">**GetRValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | <span data-ttu-id="b0391-135">Возвращает значение красного цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="b0391-135">Gets an RGB red value.</span></span>                                                                                                                                |
| <span data-ttu-id="b0391-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b0391-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span></span> | <span data-ttu-id="b0391-137">Принимает индекс для записи палитры логического цвета и возвращает спецификатор записи палитры.</span><span class="sxs-lookup"><span data-stu-id="b0391-137">Accepts an index to a logical-color palette entry and returns a palette-entry specifier.</span></span>                                                              |
| [<span data-ttu-id="b0391-138">**палеттергб**</span><span class="sxs-lookup"><span data-stu-id="b0391-138">**PALETTERGB**</span></span>](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | <span data-ttu-id="b0391-139">Принимает три значения, представляющие относительный интенситиес красного, зеленого и синего, и возвращает описатель красного, зеленого, синего (RGB), относительный от палитры.</span><span class="sxs-lookup"><span data-stu-id="b0391-139">Accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier.</span></span> |
| [<span data-ttu-id="b0391-140">RGB</span><span class="sxs-lookup"><span data-stu-id="b0391-140">RGB</span></span>](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | <span data-ttu-id="b0391-141">Выбирает красный, зеленый и синий цвет (RGB) на основе заданных аргументов и цветовых возможностей выходного устройства.</span><span class="sxs-lookup"><span data-stu-id="b0391-141">Selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.</span></span>                               |



 

 

 