---
title: Функции калибровки и классификации устройств
description: Следующие функции полезны при написании калибровки устройств и средств для работы со символами, необходимых для установки и калибровки цветовых устройств, таких как мониторы и принтеры.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Цветовая система Windows (WCS), функции
- WCS (цветовая система Windows), функции
- Управление цветом изображений, функции
- Управление цветом, функции
- цвета, функции
- Справочник по WCS, функции
- Справочник по WCS, функциям
- Цветовая система Windows (WCS), калибровка устройств
- WCS (цветовая система Windows), калибровка устройств
- Управление цветом изображений, калибровка устройств
- Управление цветом, калибровка устройств
- цвета, калибровка устройств
- Справочник по WCS, калибровка устройств
- Справочник по WCS, калибровке устройств
- Цветовая система Windows (WCS), обкодировка
- WCS (цветовая система Windows), обкодировка
- Управление цветом изображений, обработка символов
- Управление цветом, обработка символов
- цвета, символы
- Справочник по WCS, символы
- Справочник по WCS, обзнаку
- Калибровка устройств
- монитора
- характеристические
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105720857"
---
# <a name="device-calibration-and-characterization-functions"></a><span data-ttu-id="ec671-127">Функции калибровки и классификации устройств</span><span class="sxs-lookup"><span data-stu-id="ec671-127">Device Calibration and Characterization Functions</span></span>

<span data-ttu-id="ec671-128">Следующие функции полезны при написании калибровки устройств и средств для работы со символами, необходимых для установки и калибровки цветовых устройств, таких как мониторы и принтеры.</span><span class="sxs-lookup"><span data-stu-id="ec671-128">The following functions are useful for writing device calibration and characterization tools needed for installing and calibrating color display devices such as monitors and printers.</span></span>



| <span data-ttu-id="ec671-129">Функция</span><span class="sxs-lookup"><span data-stu-id="ec671-129">Function</span></span> | <span data-ttu-id="ec671-130">Описание</span><span class="sxs-lookup"><span data-stu-id="ec671-130">Description</span></span> |
|-|-|
| [<span data-ttu-id="ec671-131">**клосеколорпрофиле**</span><span class="sxs-lookup"><span data-stu-id="ec671-131">**CloseColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-closecolorprofile) | <span data-ttu-id="ec671-132">Закрывает открытый обработчик профиля.</span><span class="sxs-lookup"><span data-stu-id="ec671-132">Closes an open profile handle.</span></span> |
| [<span data-ttu-id="ec671-133">**креатедевицелинкпрофиле**</span><span class="sxs-lookup"><span data-stu-id="ec671-133">**CreateDeviceLinkProfile**</span></span>](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | <span data-ttu-id="ec671-134">Создает *профиль связи устройства* (ICC) из набора цветовых профилей с использованием указанных целей.</span><span class="sxs-lookup"><span data-stu-id="ec671-134">Creates an International Color Consortium (ICC) *device link profile* from a set of color profiles, using the specified intents.</span></span> |
| [<span data-ttu-id="ec671-135">**жетколорпрофилилемент**</span><span class="sxs-lookup"><span data-stu-id="ec671-135">**GetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | <span data-ttu-id="ec671-136">Копирует данные из указанного элемента профиля с меткой указанного цветового профиля в буфер.</span><span class="sxs-lookup"><span data-stu-id="ec671-136">Copies data from a specified tagged profile element of a specified color profile into a buffer.</span></span> |
| [<span data-ttu-id="ec671-137">**жетколорпрофилилементтаг**</span><span class="sxs-lookup"><span data-stu-id="ec671-137">**GetColorProfileElementTag**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | <span data-ttu-id="ec671-138">Извлекает имя тега, заданное параметром *двиндекс* , в таблице тегов данного профиля цвета ICC, где *двиндекс* — это Отсчитываемый от единицы индекс в таблице.</span><span class="sxs-lookup"><span data-stu-id="ec671-138">Retrieves the tag name specified by *dwIndex* in the tag table of a given International Color Consortium (ICC) color profile, where *dwIndex* is a one-based index into that table.</span></span> |
| [<span data-ttu-id="ec671-139">**жетколорпрофилефромхандле**</span><span class="sxs-lookup"><span data-stu-id="ec671-139">**GetColorProfileFromHandle**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| <span data-ttu-id="ec671-140">Извлекает содержимое профиля цвета, заданное маркером, для открытого цветового профиля.</span><span class="sxs-lookup"><span data-stu-id="ec671-140">Retrieves the color profile contents given a handle to an open color profile.</span></span>     |
| [<span data-ttu-id="ec671-141">**жетколорпрофилехеадер**</span><span class="sxs-lookup"><span data-stu-id="ec671-141">**GetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | <span data-ttu-id="ec671-142">Извлекает или наследует структуру заголовка ICC из профиля цвета ICC или XML WCS.</span><span class="sxs-lookup"><span data-stu-id="ec671-142">Retrieves or derives ICC header structure from either ICC color profile or WCS XML profile.</span></span> <span data-ttu-id="ec671-143">Драйверы и приложения должны иметь **значение true** только в том случае, если возвращается правильно структурированный заголовок.</span><span class="sxs-lookup"><span data-stu-id="ec671-143">Drivers and applications should assume returning **TRUE** only indicates that a properly structured header is returned.</span></span> <span data-ttu-id="ec671-144">Каждый тег по-прежнему должен проверяться независимо с помощью устаревших API-интерфейсов ICM2 или API схемы XML.</span><span class="sxs-lookup"><span data-stu-id="ec671-144">Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.</span></span> |
| [<span data-ttu-id="ec671-145">**жеткаунтколорпрофилилементс**</span><span class="sxs-lookup"><span data-stu-id="ec671-145">**GetCountColorProfileElements**</span></span>](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | <span data-ttu-id="ec671-146">Извлекает количество элементов с тегами в заданном цвете профиля.</span><span class="sxs-lookup"><span data-stu-id="ec671-146">Retrieves the number of tagged elements in a given color profile.</span></span> |
| [<span data-ttu-id="ec671-147">**GetPS2ColorRenderingDictionary**</span><span class="sxs-lookup"><span data-stu-id="ec671-147">**GetPS2ColorRenderingDictionary**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | <span data-ttu-id="ec671-148">Извлекает словарь рендеринга цвета 2 уровня PostScript из указанного профиля цвета ICC.</span><span class="sxs-lookup"><span data-stu-id="ec671-148">Retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.</span></span> |
| [<span data-ttu-id="ec671-149">**GetPS2ColorRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="ec671-149">**GetPS2ColorRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | <span data-ttu-id="ec671-150">Получает [Цель отрисовки](r.md) цвета 2 PostScript из профиля цвета ICC.</span><span class="sxs-lookup"><span data-stu-id="ec671-150">Retrieves the PostScript Level 2 color [rendering intent](r.md) from an ICC color profile.</span></span> |
| [<span data-ttu-id="ec671-151">**GetPS2ColorSpaceArray**</span><span class="sxs-lookup"><span data-stu-id="ec671-151">**GetPS2ColorSpaceArray**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | <span data-ttu-id="ec671-152">Извлекает массив [цветового пространства](c.md) уровня 2 для PostScript из профиля цвета ICC.</span><span class="sxs-lookup"><span data-stu-id="ec671-152">Retrieves the PostScript Level 2 [color space](c.md) array from an ICC color profile.</span></span> |
| [<span data-ttu-id="ec671-153">**исколорпрофилетагпресент**</span><span class="sxs-lookup"><span data-stu-id="ec671-153">**IsColorProfileTagPresent**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | <span data-ttu-id="ec671-154">Сообщает, имеется ли в указанном цвете профиль указанный тег ICC.</span><span class="sxs-lookup"><span data-stu-id="ec671-154">Reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.</span></span> |
| [<span data-ttu-id="ec671-155">**исколорпрофилевалид**</span><span class="sxs-lookup"><span data-stu-id="ec671-155">**IsColorProfileValid**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | <span data-ttu-id="ec671-156">Позволяет определить, является ли указанный профиль допустимым профилем ICC, или допустимым маркером профиля цветовой системы Windows (WCS), который можно использовать для управления цветом.</span><span class="sxs-lookup"><span data-stu-id="ec671-156">Allows you to determine whether the specified profile is a valid International Color Consortium (ICC) profile, or a valid Windows Color System (WCS) profile handle that can be used for color management.</span></span> |
| [<span data-ttu-id="ec671-157">**опенколорпрофилев**</span><span class="sxs-lookup"><span data-stu-id="ec671-157">**OpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-opencolorprofilew) | <span data-ttu-id="ec671-158">Создает маркер для указанного цветового профиля.</span><span class="sxs-lookup"><span data-stu-id="ec671-158">Creates a handle to a specified color profile.</span></span> <span data-ttu-id="ec671-159">Затем этот маркер можно использовать в других функциях управления профилями.</span><span class="sxs-lookup"><span data-stu-id="ec671-159">The handle can then be used in other profile management functions.</span></span> |
| [<span data-ttu-id="ec671-160">**сетколорпрофилилемент**</span><span class="sxs-lookup"><span data-stu-id="ec671-160">**SetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | <span data-ttu-id="ec671-161">Задает данные элемента для элемента профиля с тегом в цветном профиле ICC.</span><span class="sxs-lookup"><span data-stu-id="ec671-161">Sets the element data for a tagged profile element in an ICC color profile.</span></span> |
| [<span data-ttu-id="ec671-162">**сетколорпрофилилементреференце**</span><span class="sxs-lookup"><span data-stu-id="ec671-162">**SetColorProfileElementReference**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | <span data-ttu-id="ec671-163">Создает в указанном цвете ICC профиль нового тега, который ссылается на те же данные, что и существующий тег.</span><span class="sxs-lookup"><span data-stu-id="ec671-163">Creates in a specified ICC color profile a new tag that references the same data as an existing tag.</span></span> |
| [<span data-ttu-id="ec671-164">**сетколорпрофилилементсизе**</span><span class="sxs-lookup"><span data-stu-id="ec671-164">**SetColorProfileElementSize**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | <span data-ttu-id="ec671-165">Задает размер элемента с тегами в цвете ICC-профиля.</span><span class="sxs-lookup"><span data-stu-id="ec671-165">Sets the size of a tagged element in an ICC color profile.</span></span> |
| [<span data-ttu-id="ec671-166">**сетколорпрофилехеадер**</span><span class="sxs-lookup"><span data-stu-id="ec671-166">**SetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | <span data-ttu-id="ec671-167">Задает данные заголовка в указанном профиле ICC.</span><span class="sxs-lookup"><span data-stu-id="ec671-167">Sets the header data in a specified ICC color profile.</span></span> |
| [<span data-ttu-id="ec671-168">**вксжеткалибратионманажементстате**</span><span class="sxs-lookup"><span data-stu-id="ec671-168">**WcsGetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | <span data-ttu-id="ec671-169">Определяет, включено ли управление системой состояния калибровки экрана.</span><span class="sxs-lookup"><span data-stu-id="ec671-169">Determines whether system management of the display calibration state is enabled.</span></span> |
| [<span data-ttu-id="ec671-170">**вкссеткалибратионманажементстате**</span><span class="sxs-lookup"><span data-stu-id="ec671-170">**WcsSetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | <span data-ttu-id="ec671-171">Определяет, включено ли управление системой состояния калибровки экрана.</span><span class="sxs-lookup"><span data-stu-id="ec671-171">Determines whether system management of the display calibration state is enabled.</span></span> |



 

 

 




