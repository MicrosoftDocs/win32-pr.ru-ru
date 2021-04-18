---
title: Основные функции для использования в контексте устройства
description: Следующие функции WCS предоставляют базовые возможности сопоставления цветов в контекстах устройств. Они полезны для всех приложений, которым требуется реализовать управление цветом с низкой нагрузкой и минимальным вмешательством пользователя.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Цветовая система Windows (WCS), функции
- WCS (цветовая система Windows), функции
- Управление цветом изображений, функции
- Управление цветом, функции
- цвета, функции
- Справочник по WCS, функции
- Справочник по WCS, функциям
- Цветовая система Windows (WCS), контексты устройств
- WCS (цветовая система Windows), контексты устройств
- Управление цветом изображений, контексты устройств
- Управление цветом, контексты устройств
- цвета, контексты устройств
- Справочник по WCS, контексты устройств
- Справочник по контексту WCS и устройствам
- контексты устройств
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "105719861"
---
# <a name="basic-functions-for-use-within-a-device-context"></a><span data-ttu-id="17ae7-119">Основные функции для использования в контексте устройства</span><span class="sxs-lookup"><span data-stu-id="17ae7-119">Basic Functions for Use Within a Device Context</span></span>

<span data-ttu-id="17ae7-120">Следующие функции WCS предоставляют базовые возможности [сопоставления цветов](c.md) в контекстах устройств.</span><span class="sxs-lookup"><span data-stu-id="17ae7-120">The following WCS functions deliver basic [color mapping](c.md) capabilities within device contexts.</span></span> <span data-ttu-id="17ae7-121">Они полезны для всех приложений, которым требуется реализовать управление цветом с низкой нагрузкой и минимальным вмешательством пользователя.</span><span class="sxs-lookup"><span data-stu-id="17ae7-121">They are useful to all applications that need to implement color management with low overhead and minimal user intervention.</span></span>



| <span data-ttu-id="17ae7-122">Функция</span><span class="sxs-lookup"><span data-stu-id="17ae7-122">Function</span></span>                                                           | <span data-ttu-id="17ae7-123">Описание</span><span class="sxs-lookup"><span data-stu-id="17ae7-123">Description</span></span>                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17ae7-124">**чеккколорсингамут**</span><span class="sxs-lookup"><span data-stu-id="17ae7-124">**CheckColorsInGamut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | <span data-ttu-id="17ae7-125">Проверяет, находятся ли заданные цвета в цветовой гамме устройства.</span><span class="sxs-lookup"><span data-stu-id="17ae7-125">Checks if given colors are in a device's gamut.</span></span>                                                                                                     |
| [<span data-ttu-id="17ae7-126">**колоркорректпалетте**</span><span class="sxs-lookup"><span data-stu-id="17ae7-126">**ColorCorrectPalette**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | <span data-ttu-id="17ae7-127">Исправление записей в палитре для контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="17ae7-127">Corrects the entries in a palette for a device context.</span></span>                                                                                             |
| [<span data-ttu-id="17ae7-128">**колорматчтотаржет**</span><span class="sxs-lookup"><span data-stu-id="17ae7-128">**ColorMatchToTarget**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | <span data-ttu-id="17ae7-129">Выполняет сопоставление цветов в целях предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="17ae7-129">Performs color mapping for preview purposes.</span></span>                                                                                                        |
| [<span data-ttu-id="17ae7-130">**креатеколорспаце**</span><span class="sxs-lookup"><span data-stu-id="17ae7-130">**CreateColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | <span data-ttu-id="17ae7-131">Создает цветовое пространство.</span><span class="sxs-lookup"><span data-stu-id="17ae7-131">Creates a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="17ae7-132">**делетеколорспаце**</span><span class="sxs-lookup"><span data-stu-id="17ae7-132">**DeleteColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | <span data-ttu-id="17ae7-133">Удаляет цветовое пространство.</span><span class="sxs-lookup"><span data-stu-id="17ae7-133">Deletes a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="17ae7-134">**енумикмпрофилес**</span><span class="sxs-lookup"><span data-stu-id="17ae7-134">**EnumICMProfiles**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | <span data-ttu-id="17ae7-135">Перечисляет цветовые профили вывода, доступные для данного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="17ae7-135">Enumerates output color profiles available for a given device context.</span></span>                                                                              |
| [<span data-ttu-id="17ae7-136">**енумикмпрофилеспроккаллбакк**</span><span class="sxs-lookup"><span data-stu-id="17ae7-136">**EnumICMProfilesProcCallback**</span></span>](/windows/desktop/api/Wingdi/) | <span data-ttu-id="17ae7-137">Определяемая приложением функция обратного вызова для [**енумикмпрофилес**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span><span class="sxs-lookup"><span data-stu-id="17ae7-137">Application-defined callback function for [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span></span> <span data-ttu-id="17ae7-138">Имя этой функции также определяется приложением.</span><span class="sxs-lookup"><span data-stu-id="17ae7-138">The name of this function is also defined by the application.</span></span> |
| [<span data-ttu-id="17ae7-139">**жетколорспаце**</span><span class="sxs-lookup"><span data-stu-id="17ae7-139">**GetColorSpace**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | <span data-ttu-id="17ae7-140">Возвращает текущее входное Цветное пространство в контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="17ae7-140">Gets the current input color space in a device context.</span></span> |
| [<span data-ttu-id="17ae7-141">**жетикмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="17ae7-141">**GetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | <span data-ttu-id="17ae7-142">Возвращает текущий выходной цветовой профиль контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="17ae7-142">Gets the current output color profile of a device context.</span></span>                                                                                          |
| [<span data-ttu-id="17ae7-143">**жетлогколорспаце**</span><span class="sxs-lookup"><span data-stu-id="17ae7-143">**GetLogColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | <span data-ttu-id="17ae7-144">Возвращает структуру [**логколорспаце**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="17ae7-144">Gets the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure of a device context.</span></span>                                                                      |
| [<span data-ttu-id="17ae7-145">**сетколорспаце**</span><span class="sxs-lookup"><span data-stu-id="17ae7-145">**SetColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | <span data-ttu-id="17ae7-146">Задает цветовое пространство ввода контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="17ae7-146">Sets a device context's input color space.</span></span>                                                                                                          |
| [<span data-ttu-id="17ae7-147">**сетикммоде**</span><span class="sxs-lookup"><span data-stu-id="17ae7-147">**SetICMMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | <span data-ttu-id="17ae7-148">Включает или выключает управление цветом в контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="17ae7-148">Turns color management on or off in a device context.</span></span>                                                                                               |
| [<span data-ttu-id="17ae7-149">**сетикмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="17ae7-149">**SetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | <span data-ttu-id="17ae7-150">Задает выходной профиль цвета для заданного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="17ae7-150">Sets the output color profile for a given device context.</span></span>                                                                                           |
| [<span data-ttu-id="17ae7-151">**вксенумколорпрофилес**</span><span class="sxs-lookup"><span data-stu-id="17ae7-151">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | <span data-ttu-id="17ae7-152">Перечисляет все цветовые профили, удовлетворяющие критериям перечисления в указанной области управления профилями.</span><span class="sxs-lookup"><span data-stu-id="17ae7-152">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                      |



 

 

 




