---
description: Следующие константы указывают допустимый набор свойств элемента сканера для получения образа Windows (WIA).
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Константы свойства элемента сканера WIA (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aa3b1cc4ae14a9460a24f652a9599035cacca2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701585"
---
# <a name="scanner-wia-item-property-constants"></a><span data-ttu-id="b62b3-103">Константы свойства элемента сканера WIA</span><span class="sxs-lookup"><span data-stu-id="b62b3-103">Scanner WIA Item Property Constants</span></span>

<span data-ttu-id="b62b3-104">Следующие константы указывают допустимый набор свойств элемента сканера для получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="b62b3-104">The following constants specify the valid set of Windows Image Acquisition (WIA) scanner item properties.</span></span>

<span data-ttu-id="b62b3-105">Префикс "WIA- \_ адреса \_ " указывает свойство элемента для устройств сканера и является соглашением об именовании, используемым в C/C++.</span><span class="sxs-lookup"><span data-stu-id="b62b3-105">The prefix "WIA\_IPS\_" indicates an Item Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="b62b3-106">Для сценариев эти константы используют префикс "Сканнерпиктуре" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="b62b3-106">For scripting purposes these constants use the prefix "ScannerPicture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="b62b3-107">Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="b62b3-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b62b3-108">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="b62b3-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b62b3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <span data-ttu-id="b62b3-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>сканнерпиктуреаутодескев</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-111">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-111">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="b62b3-112">Включает или выключает автоматический декоса.</span><span class="sxs-lookup"><span data-stu-id="b62b3-112">Turns automatic deskew on or off.</span></span><br/> <span data-ttu-id="b62b3-113">Необязательно только для WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="b62b3-113">Optional for WIA_CATEGORY_FEEDER only.</span></span><br/> <span data-ttu-id="b62b3-114">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-114">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="b62b3-115">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-115">The following table has the constants that are valid with this property.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-116">Константа</span><span class="sxs-lookup"><span data-stu-id="b62b3-116">Constant</span></span></th>
<th><span data-ttu-id="b62b3-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-118">WIA_AUTO_DESKEW_ON</span><span class="sxs-lookup"><span data-stu-id="b62b3-118">WIA_AUTO_DESKEW_ON</span></span></td>
<td><span data-ttu-id="b62b3-119">Включите автоматический декоса.</span><span class="sxs-lookup"><span data-stu-id="b62b3-119">Turn on automatic deskew.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-120">WIA_AUTO_DESKEW_OFF</span><span class="sxs-lookup"><span data-stu-id="b62b3-120">WIA_AUTO_DESKEW_OFF</span></span></td>
<td><span data-ttu-id="b62b3-121">Отключите автоматический декоса.</span><span class="sxs-lookup"><span data-stu-id="b62b3-121">Turn off automatic deskew.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <span data-ttu-id="b62b3-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>сканнерпиктуребригхтнесс</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-123">Значения яркости изображения, доступные в сканере.</span><span class="sxs-lookup"><span data-stu-id="b62b3-123">The image brightness values available within the scanner.</span></span></p>
<p><span data-ttu-id="b62b3-124">Содержит текущую настройку яркости оборудования для устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-124">Contains the current hardware brightness setting for the device.</span></span> <span data-ttu-id="b62b3-125">Приложение задает для этого свойства значение яркости оборудования.</span><span class="sxs-lookup"><span data-stu-id="b62b3-125">An application sets this property to the hardware's brightness value.</span></span> <span data-ttu-id="b62b3-126">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-126">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-127">Значения должны сопоставляться в диапазоне от-1000 до 1000, где 1000 соответствует максимальной яркости, 0 соответствует стандартной яркости, а-1000 соответствует минимальной яркости.</span><span class="sxs-lookup"><span data-stu-id="b62b3-127">Values should be mapped in a range from -1000 through 1000, where 1000 corresponds to the maximum brightness, 0 corresponds to normal brightness, and -1000 corresponds to the minimum brightness.</span></span></p>
<p><span data-ttu-id="b62b3-128">Требуется для всех элементов в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-128">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="b62b3-129">Необязательно, но рекомендуется для WIA_CATEGORY_FINISHED_FILE элементов, поддерживающих предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="b62b3-129">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="b62b3-130">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-130">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <span data-ttu-id="b62b3-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>сканнерпиктуреконтраст</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-132">Содержит текущую настройку аппаратной контрастности для устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-132">Contains the current hardware contrast setting for a device.</span></span> <span data-ttu-id="b62b3-133">Приложение задает для этого свойства значение контрастности оборудования.</span><span class="sxs-lookup"><span data-stu-id="b62b3-133">An application sets this property to the hardware's contrast value.</span></span> <span data-ttu-id="b62b3-134">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-134">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-135">Значения должны сопоставляться в диапазоне от-1000 до 1000, где-1000 соответствует минимальному контрасту, 0 соответствует нормальным контрастам, а 1000 соответствует максимальной контрастности.</span><span class="sxs-lookup"><span data-stu-id="b62b3-135">Values should be mapped in a range from -1000 through 1000, where -1000 corresponds to the minimum contrast, 0 corresponds to normal contrast, and 1000 corresponds to the maximum contrast.</span></span></p>
<p><span data-ttu-id="b62b3-136">Требуется для всех элементов в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-136">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="b62b3-137">Необязательно, но рекомендуется для WIA_CATEGORY_FINISHED_FILE элементов, поддерживающих предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="b62b3-137">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="b62b3-138">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-138">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <span data-ttu-id="b62b3-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>сканнерпиктурекуринтент</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-140">Содержит текущие параметры намерения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-140">Contains the current intent settings.</span></span> <span data-ttu-id="b62b3-141">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-141">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-142">Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-142">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="b62b3-143">Он не поддерживается для WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FOLDER элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-143">It is not supported for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="b62b3-144">Тип: <strong>VT_I4</strong> доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-144">Type: <strong>VT_I4</strong> Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span></span></p>
<p><span data-ttu-id="b62b3-145">Драйвер использует их для предустановки свойств элемента на основе предполагаемого использования образа приложением.</span><span class="sxs-lookup"><span data-stu-id="b62b3-145">The driver uses these to preset item properties based on an application's intended use of the image.</span></span> <span data-ttu-id="b62b3-146">Это может быть, например, максимальное качество, минимальный размер и т. д.</span><span class="sxs-lookup"><span data-stu-id="b62b3-146">This might include, for example, maximum quality, minimum size, and so on.</span></span></p>
<p><span data-ttu-id="b62b3-147">Драйвер выбирает битовую глубину в точках на дюйм, а другие параметры, которые он определяет, подходят для выбранной цели.</span><span class="sxs-lookup"><span data-stu-id="b62b3-147">The driver chooses the bit depth, in dots per inch, and other settings that it determines are appropriate for the selected intent.</span></span> <span data-ttu-id="b62b3-148">Приложение может считать текущие параметры, чтобы определить, какие свойства были изменены.</span><span class="sxs-lookup"><span data-stu-id="b62b3-148">It is up to the application to read the current settings to determine which properties were changed.</span></span> <span data-ttu-id="b62b3-149">Приложение задает это свойство для автоматической установки свойств WIA для конкретной цели приобретения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-149">An application sets this property to auto-set the WIA properties for specific acquisition intent.</span></span> <span data-ttu-id="b62b3-150">Это свойство является обязательным для всех сканеров.</span><span class="sxs-lookup"><span data-stu-id="b62b3-150">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="b62b3-151">Приложение задает это свойство для автоматического задания свойств WIA для конкретной цели приобретения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-151">An application sets this property to auto-set the WIA properties for specific acquisition intent</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-152">Флаги можно сочетать с оператором побитового <strong>или</strong> , но изображение не может одновременно быть в оттенках серого и Color.</span><span class="sxs-lookup"><span data-stu-id="b62b3-152">The flags can be combined with a bitwise <strong>OR</strong> operator, but an image cannot be both grayscale and color.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-153">Это свойство является обязательным для всех сканеров.</span><span class="sxs-lookup"><span data-stu-id="b62b3-153">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="b62b3-154">В следующей таблице содержатся флаги типа Image и их определения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-154">The following table contains the image-type flags and their definitions.</span></span> <span data-ttu-id="b62b3-155">Эти флаги используются для задания того, какой тип изображения предназначен: цвет, оттенки серого и т. д.</span><span class="sxs-lookup"><span data-stu-id="b62b3-155">These flags are used to set which type of image is intended: color, grayscale, and so on.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-156">Предназначенные флаги типа образа</span><span class="sxs-lookup"><span data-stu-id="b62b3-156">Intended image type flags</span></span></th>
<th><span data-ttu-id="b62b3-157">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-158">WIA_INTENT_NONE</span><span class="sxs-lookup"><span data-stu-id="b62b3-158">WIA_INTENT_NONE</span></span></td>
<td><span data-ttu-id="b62b3-159">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b62b3-159">Default value.</span></span> <span data-ttu-id="b62b3-160">Намерение не указано.</span><span class="sxs-lookup"><span data-stu-id="b62b3-160">No intent is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-161">WIA_INTENT_IMAGE_TYPE_COLOR</span><span class="sxs-lookup"><span data-stu-id="b62b3-161">WIA_INTENT_IMAGE_TYPE_COLOR</span></span></td>
<td><span data-ttu-id="b62b3-162">Приложение планирует подготовить устройство для цветной проверки.</span><span class="sxs-lookup"><span data-stu-id="b62b3-162">The application intends to prepare the device for a color scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="b62b3-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span></span></td>
<td><span data-ttu-id="b62b3-164">Приложение планирует подготовить устройство для сканирования в градациях серого.</span><span class="sxs-lookup"><span data-stu-id="b62b3-164">The application intends to prepare the device for a grayscale scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-165">WIA_INTENT_IMAGE_TYPE_TEXT</span><span class="sxs-lookup"><span data-stu-id="b62b3-165">WIA_INTENT_IMAGE_TYPE_TEXT</span></span></td>
<td><span data-ttu-id="b62b3-166">Приложение планирует подготовить устройство для сканирования текста.</span><span class="sxs-lookup"><span data-stu-id="b62b3-166">The application intends to prepare the device for scanning text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-167">WIA_INTENT_IMAGE_TYPE_MASK</span><span class="sxs-lookup"><span data-stu-id="b62b3-167">WIA_INTENT_IMAGE_TYPE_MASK</span></span></td>
<td><span data-ttu-id="b62b3-168">Маска для всех флагов типа изображения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-168">Mask for all of the image-type flags.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b62b3-169">В следующей таблице содержатся флаги качества и размера, а также их определения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-169">The following table contains the quality and size flags and their definitions.</span></span> <span data-ttu-id="b62b3-170">Эти флаги используются для настройки требуемого уровня качества.</span><span class="sxs-lookup"><span data-stu-id="b62b3-170">These flags are used to set which level of quality is intended.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-171">Предполагаемый размер изображения/флаги качества</span><span class="sxs-lookup"><span data-stu-id="b62b3-171">Intended image size/quality flags</span></span></th>
<th><span data-ttu-id="b62b3-172">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-172">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-173">WIA_INTENT_MINIMIZE_SIZE</span><span class="sxs-lookup"><span data-stu-id="b62b3-173">WIA_INTENT_MINIMIZE_SIZE</span></span></td>
<td><span data-ttu-id="b62b3-174">Приложение планирует подготовить устройство к сканированию образа, который является незначительным сканированием.</span><span class="sxs-lookup"><span data-stu-id="b62b3-174">The application intends to prepare the device for scanning an image that result's in a small scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-175">WIA_INTENT_MAXIMIZE_QUALITY</span><span class="sxs-lookup"><span data-stu-id="b62b3-175">WIA_INTENT_MAXIMIZE_QUALITY</span></span></td>
<td><span data-ttu-id="b62b3-176">Приложение планирует подготовить устройство для сканирования высококачественного изображения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-176">The application intends to prepare the device for scanning a high-quality image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-177">WIA_INTENT_SIZE_MASK</span><span class="sxs-lookup"><span data-stu-id="b62b3-177">WIA_INTENT_SIZE_MASK</span></span></td>
<td><span data-ttu-id="b62b3-178">Этот флаг является маской для всех флагов размера и качества.</span><span class="sxs-lookup"><span data-stu-id="b62b3-178">This flag is a mask for all of the size/quality flags.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-179">WIA_INTENT_BEST_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="b62b3-179">WIA_INTENT_BEST_PREVIEW</span></span></td>
<td><span data-ttu-id="b62b3-180">Приложение планирует подготовить устройство для сканирования предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="b62b3-180">The application intends to prepare the device for scanning a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <span data-ttu-id="b62b3-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>сканнерпиктуредескевкс</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-182">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-182">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-183">Содержит число пикселей в направлении по оси x от WIA_IPS_XPOS до координат по оси x верхнего угла изображения, которое необходимо вычислить.</span><span class="sxs-lookup"><span data-stu-id="b62b3-183">Contains the number of pixels in the x-direction from WIA_IPS_XPOS to the x-coordinate of the uppermost corner of the image to be deskewed.</span></span> <span data-ttu-id="b62b3-184">Таким образом, в сочетании с WIA_IPS_DESKEW_Y, где два верхних угла наклоненного изображения расположены в ограничивающем прямоугольнике, определяемом WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT и WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="b62b3-184">Hence, it describes, in conjunction with WIA_IPS_DESKEW_Y, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="b62b3-185">его свойство реализуется драйвером сканера, если он поддерживает деравномерность.</span><span class="sxs-lookup"><span data-stu-id="b62b3-185">his property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="b62b3-186">Допустимые значения для WIA_IPS_DESKEW_X должны находиться в диапазоне от 0 до (WIA_IPS_XEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="b62b3-186">The valid values for WIA_IPS_DESKEW_X must be between 0 and (WIA_IPS_XEXTENT - 1).</span></span> <span data-ttu-id="b62b3-187">Значение 0 означает, что не следует выполнять декосая.</span><span class="sxs-lookup"><span data-stu-id="b62b3-187">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="b62b3-188">Это свойство является необязательным для элементов категорий WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER и WIA_CATEGORY_FILM; он недоступен для элементов WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="b62b3-188">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="b62b3-189">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="b62b3-189">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <span data-ttu-id="b62b3-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>сканнерпиктуредескеви</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-191">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-191">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-192">Содержит количество пикселей в направлении по оси y от WIA_IPS_YPOS до координат по оси y левого угла изображения, которое нужно деравномерное раскрывающий.</span><span class="sxs-lookup"><span data-stu-id="b62b3-192">Contains the number of pixels in the y-direction from WIA_IPS_YPOS to the y-coordinate of the leftmost corner of the image to be deskewed.</span></span> <span data-ttu-id="b62b3-193">Таким образом, в сочетании с WIA_IPS_DESKEW_X, где два верхних угла наклоненного изображения расположены в ограничивающем прямоугольнике, определяемом WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT и WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="b62b3-193">Hence, it describes, in conjunction with WIA_IPS_DESKEW_X, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="b62b3-194">Это свойство реализуется драйвером сканера, если он поддерживает деравномерность.</span><span class="sxs-lookup"><span data-stu-id="b62b3-194">This property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="b62b3-195">Допустимые значения для WIA_IPS_DESKEW_Y должны находиться в диапазоне от 0 до (WIA_IPS_YEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="b62b3-195">The valid values for WIA_IPS_DESKEW_Y must be between 0 and (WIA_IPS_YEXTENT - 1).</span></span> <span data-ttu-id="b62b3-196">Значение 0 означает, что не следует выполнять декосая.</span><span class="sxs-lookup"><span data-stu-id="b62b3-196">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="b62b3-197">Это свойство является необязательным для элементов категорий WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER и WIA_CATEGORY_FILM; он недоступен для элементов WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="b62b3-197">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="b62b3-198">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="b62b3-198">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <span data-ttu-id="b62b3-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>сканнерпиктуредокуменсандлингселект</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-200">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-200">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-201">Содержит текущий источник и режим получения сканера.</span><span class="sxs-lookup"><span data-stu-id="b62b3-201">Contains the current scanner acquisition source and mode.</span></span> <span data-ttu-id="b62b3-202">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-202">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-203">Приложение считывает это свойство, чтобы определить текущий источник получения сканера или записать это свойство, чтобы задать источник и режим сканера.</span><span class="sxs-lookup"><span data-stu-id="b62b3-203">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="b62b3-204">Кроме того, приложения используют это свойство для включения и отключения функции дуплексного режима.</span><span class="sxs-lookup"><span data-stu-id="b62b3-204">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="b62b3-205">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-205">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="b62b3-206">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-206">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-207">Флаги</span><span class="sxs-lookup"><span data-stu-id="b62b3-207">Flags</span></span></th>
<th><span data-ttu-id="b62b3-208">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-209">УСТРОЙСТВА</span><span class="sxs-lookup"><span data-stu-id="b62b3-209">DUPLEX</span></span></td>
<td><span data-ttu-id="b62b3-210">Сканирование с помощью операций дуплексного устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-210">Scan using duplexer operations.</span></span> <span data-ttu-id="b62b3-211">Сканирование обеих сторон документа с помощью общих параметров, настроенных для элемента-податчика (WIA_CATEGORY_FEEDER).</span><span class="sxs-lookup"><span data-stu-id="b62b3-211">Scan both document sides using common settings configured for the feeder item (WIA_CATEGORY_FEEDER).</span></span> <span data-ttu-id="b62b3-212">ДУПЛЕКСные и ADVANCE_DUPLEX не могут быть заданы одновременно.</span><span class="sxs-lookup"><span data-stu-id="b62b3-212">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-213">ADVANCED_DUPLEX</span><span class="sxs-lookup"><span data-stu-id="b62b3-213">ADVANCED_DUPLEX</span></span></td>
<td><span data-ttu-id="b62b3-214">Сканирование с использованием отдельных параметров, настроенных для каждого элемента дочернего веб-канала (WIA_CATEGORY_FEEDER_FRONT и WIA_CATEGORY_FEEDER_BACK).</span><span class="sxs-lookup"><span data-stu-id="b62b3-214">Scan using individual settings configured for each child feeder item (WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK).</span></span> <span data-ttu-id="b62b3-215">ДУПЛЕКСные и ADVANCE_DUPLEX не могут быть заданы одновременно.</span><span class="sxs-lookup"><span data-stu-id="b62b3-215">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-216">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="b62b3-216">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="b62b3-217">Сначала просканируйте передний план документа.</span><span class="sxs-lookup"><span data-stu-id="b62b3-217">Scan the front of the document first.</span></span> <span data-ttu-id="b62b3-218">Это значение допустимо, если задан ДУПЛЕКСный или ADVANCED_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="b62b3-218">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-219">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="b62b3-219">BACK_FIRST</span></span></td>
<td><span data-ttu-id="b62b3-220">Сначала просканируйте задний план документа.</span><span class="sxs-lookup"><span data-stu-id="b62b3-220">Scan the back of the document first.</span></span> <span data-ttu-id="b62b3-221">Это значение допустимо, если задан ДУПЛЕКСный или ADVANCED_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="b62b3-221">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-222">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="b62b3-222">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="b62b3-223">Сканирование только на передней панели.</span><span class="sxs-lookup"><span data-stu-id="b62b3-223">Scan the front only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-224">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="b62b3-224">BACK_ONLY</span></span></td>
<td><span data-ttu-id="b62b3-225">Проверка только обратного просмотра.</span><span class="sxs-lookup"><span data-stu-id="b62b3-225">Scan the back only.</span></span> <span data-ttu-id="b62b3-226">Это значение допустимо, если задан ДУПЛЕКСный или ADVANCED_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="b62b3-226">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <span data-ttu-id="b62b3-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>сканнерпиктурефилмноденаме</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-228">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-228">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-229">Включает спецификацию конкретного вложения для сканирования пленки при наличии более одного.</span><span class="sxs-lookup"><span data-stu-id="b62b3-229">Enables specification of a particular film scanning attachment when there is more than one.</span></span></p>
<p><span data-ttu-id="b62b3-230">Это свойство требуется для элементов WIA_CATEGORY_FILM, если имеется несколько элементов для сканирования на пленке.</span><span class="sxs-lookup"><span data-stu-id="b62b3-230">This property is required for the WIA_CATEGORY_FILM items when there are multiple film scan items.</span></span> <span data-ttu-id="b62b3-231">Если устройство поддерживает только один элемент фотопленки, это свойство является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b62b3-231">If the device supports only one root scanner film item then this property is optional.</span></span></p>
<p><span data-ttu-id="b62b3-232">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-232">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b62b3-233">Допустимые значения: BSTR должен иметь вид @ResourceBinary ,- <ResourceID> чтобы разрешить локализацию, так как эта строка будет предоставляться пользователю через пользовательский интерфейс сканирования пленки.</span><span class="sxs-lookup"><span data-stu-id="b62b3-233">Allowed values: The BSTR should be in the form of @ResourceBinary,-<ResourceID> to allow localization as this string would be exposed to the user through the film scanning UI.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <span data-ttu-id="b62b3-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>сканнерпиктурефилмсканмоде</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-235">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-235">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-236">Включает настройку текущей проверки пленки.</span><span class="sxs-lookup"><span data-stu-id="b62b3-236">Enables configuration of the current film scan.</span></span></p>
<p><span data-ttu-id="b62b3-237">Это свойство является обязательным для элемента WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-237">This property is required for the WIA_CATEGORY_FILM item.</span></span></p>
<p><span data-ttu-id="b62b3-238">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-238">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="b62b3-239">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-239">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-240">Константа</span><span class="sxs-lookup"><span data-stu-id="b62b3-240">Constant</span></span></th>
<th><span data-ttu-id="b62b3-241">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-241">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-242">WIA_FILM_COLOR_SLIDE</span><span class="sxs-lookup"><span data-stu-id="b62b3-242">WIA_FILM_COLOR_SLIDE</span></span></td>
<td><span data-ttu-id="b62b3-243">Сканирование для цветного слайда.</span><span class="sxs-lookup"><span data-stu-id="b62b3-243">Scan for a color slide.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-244">WIA_FILM_COLOR_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="b62b3-244">WIA_FILM_COLOR_NEGATIVE</span></span></td>
<td><span data-ttu-id="b62b3-245">Сканировать для отрицательного цвета.</span><span class="sxs-lookup"><span data-stu-id="b62b3-245">Scan for a color negative.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-246">WIA_FILM_BW_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="b62b3-246">WIA_FILM_BW_NEGATIVE</span></span></td>
<td><span data-ttu-id="b62b3-247">Проверка на наличие черного и белого отрицательных результатов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-247">Scan for a black and white negative.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <span data-ttu-id="b62b3-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>сканнерпиктуреинверт</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-249">Зарезервировано для будущего использования и в настоящее время не реализовано.</span><span class="sxs-lookup"><span data-stu-id="b62b3-249">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="b62b3-250">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-250">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="b62b3-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>сканнерпиктуреинверт</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-252">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-252">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-253">Указывает, сколько элементов хранится в элементе WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="b62b3-253">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="b62b3-254">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-254">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <span data-ttu-id="b62b3-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>сканнерпиктуреламп</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-256">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-256">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-257">Включает или выключает лампу сканера.</span><span class="sxs-lookup"><span data-stu-id="b62b3-257">Turns the scanner lamp on or off.</span></span></p>
<p><span data-ttu-id="b62b3-258">Необязательно для элементов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER и WIA_CATEGORY_FILM и рекомендуется для WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-258">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="b62b3-259">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-259">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="b62b3-260">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-260">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-261">Константа</span><span class="sxs-lookup"><span data-stu-id="b62b3-261">Constant</span></span></th>
<th><span data-ttu-id="b62b3-262">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-263">WIA_LAMP_ON</span><span class="sxs-lookup"><span data-stu-id="b62b3-263">WIA_LAMP_ON</span></span></td>
<td><span data-ttu-id="b62b3-264">Включите лампу.</span><span class="sxs-lookup"><span data-stu-id="b62b3-264">Turn on the lamp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-265">WIA_LAMP_OFF</span><span class="sxs-lookup"><span data-stu-id="b62b3-265">WIA_LAMP_OFF</span></span></td>
<td><span data-ttu-id="b62b3-266">Выключите лампу.</span><span class="sxs-lookup"><span data-stu-id="b62b3-266">Turn off the lamp.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <span data-ttu-id="b62b3-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>сканнерпиктурелампаутуфф</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-268">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-268">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-269">Задает максимальное время, в течение которого должна удерживаться лампа, если сканер не используется.</span><span class="sxs-lookup"><span data-stu-id="b62b3-269">Sets the maximum time to keep the lamp on when the scanner is not being used.</span></span></p>
<p><span data-ttu-id="b62b3-270">Необязательно для элементов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER и WIA_CATEGORY_FILM и рекомендуется для WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-270">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="b62b3-271">Тип: <strong>VT_UI4</strong>, доступ: чтение и запись, допустимые значения: 0 — 0xfff секунд</span><span class="sxs-lookup"><span data-stu-id="b62b3-271">Type: <strong>VT_UI4</strong>, Access: Read/Write, Valid Values: 0 - 0xFFF seconds</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <span data-ttu-id="b62b3-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>сканнерпиктуремаксхоризонталсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-273">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-273">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-274">Задает максимальную ширину в тысячах дюйма, которая просматривается на горизонтальной оси (X) при текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="b62b3-274">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span> <span data-ttu-id="b62b3-275">В зависимости от типа элемента это может быть ширина податчика листа или сканера.</span><span class="sxs-lookup"><span data-stu-id="b62b3-275">This may be the width of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="b62b3-276">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <span data-ttu-id="b62b3-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>сканнерпиктуремаксвертикалсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-278">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-278">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-279">Задает максимальную высоту в тысячах дюйма, которая просматривается на вертикальной оси (Y) при текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="b62b3-279">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span> <span data-ttu-id="b62b3-280">Это может быть высота податчика листа или сканера в соответствии с типом элемента.</span><span class="sxs-lookup"><span data-stu-id="b62b3-280">This may be the height of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="b62b3-281">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-281">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <span data-ttu-id="b62b3-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>сканнерпиктуреминхоризонталсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-283">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-283">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-284">Задает минимальную ширину в тысячах дюйма, которая просматривается на горизонтальной оси (X) при текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="b62b3-284">Specifies the minimum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="b62b3-285">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-285">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <span data-ttu-id="b62b3-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>сканнерпиктуреминвертикалсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-287">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-287">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-288">Задает минимальную высоту (в тысячах) дюйма, которая просматривается по вертикальной оси (Y) при текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="b62b3-288">Specifies the minimum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="b62b3-289">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-289">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <span data-ttu-id="b62b3-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>сканнерпиктуремиррор</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-291">Зарезервировано для будущего использования и в настоящее время не реализовано.</span><span class="sxs-lookup"><span data-stu-id="b62b3-291">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="b62b3-292">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-292">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <span data-ttu-id="b62b3-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>сканнерпиктуреоптикалксрес</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-294">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-294">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-295">Горизонтальное разрешение оптического экрана.</span><span class="sxs-lookup"><span data-stu-id="b62b3-295">Horizontal Optical Resolution.</span></span> <span data-ttu-id="b62b3-296">Самое высокое поддерживаемое оптическое разрешение по горизонтали в DPI.</span><span class="sxs-lookup"><span data-stu-id="b62b3-296">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="b62b3-297">Это свойство имеет одно значение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-297">This property is a single value.</span></span> <span data-ttu-id="b62b3-298">Это не список всех разрешений, которые могут быть созданы устройством.</span><span class="sxs-lookup"><span data-stu-id="b62b3-298">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="b62b3-299">Вместо этого это разрешение оптики устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-299">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="b62b3-300">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-300">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="b62b3-301">Это свойство является обязательным для всех элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-301">This property is required for all items.</span></span></p>
<p><span data-ttu-id="b62b3-302">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-302">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <span data-ttu-id="b62b3-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>сканнерпиктуреоптикалирес</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-304">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-304">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-305">Вертикальное оптическое разрешение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-305">Vertical Optical Resolution.</span></span> <span data-ttu-id="b62b3-306">Максимальное поддерживаемое вертикальное оптическое разрешение в DPI.</span><span class="sxs-lookup"><span data-stu-id="b62b3-306">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="b62b3-307">Это свойство имеет одно значение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-307">This property is a single value.</span></span> <span data-ttu-id="b62b3-308">Это не список всех разрешений, создаваемых устройством.</span><span class="sxs-lookup"><span data-stu-id="b62b3-308">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="b62b3-309">Вместо этого это разрешение оптики устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-309">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="b62b3-310">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-310">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="b62b3-311">Это свойство является обязательным для всех элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-311">This property is required for all items.</span></span></p>
<p><span data-ttu-id="b62b3-312">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <span data-ttu-id="b62b3-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>сканнерпиктуреориентатион</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-314">Указывает текущую ориентацию сканируемых документов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-314">Specifies the current orientation of the documents to be scanned.</span></span> <span data-ttu-id="b62b3-315">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-315">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-316">Приложение задает это свойство, чтобы определить исходную ориентацию страницы или изображения, которые должны быть получены.</span><span class="sxs-lookup"><span data-stu-id="b62b3-316">An application sets this property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="b62b3-317">Сведения об использовании WIA_IPS_ORIENTATION см. в разделе <strong>WIA_IPS_PAGE_SIZE</strong>.</span><span class="sxs-lookup"><span data-stu-id="b62b3-317">For information on how to use WIA_IPS_ORIENTATION, see <strong>WIA_IPS_PAGE_SIZE</strong>.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-318">WIA_IPS_ORIENTATION указывает на расположение документа, который будет проверяться на сканере или в податчике.</span><span class="sxs-lookup"><span data-stu-id="b62b3-318">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="b62b3-319">Это ориентация документа относительно направления сканирования.</span><span class="sxs-lookup"><span data-stu-id="b62b3-319">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="b62b3-320">WIA_IPS_ROTATION относится к повороту, который применяется к изображению после его сканирования, непосредственно перед передачей изображения в приложение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-320">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-321">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-321">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="b62b3-322">В следующей таблице приведены четыре константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-322">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-323">Значение</span><span class="sxs-lookup"><span data-stu-id="b62b3-323">Value</span></span></th>
<th><span data-ttu-id="b62b3-324">Определение</span><span class="sxs-lookup"><span data-stu-id="b62b3-324">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-325">КНИЖНОЙ ориентации</span><span class="sxs-lookup"><span data-stu-id="b62b3-325">PORTRAIT</span></span></td>
<td><span data-ttu-id="b62b3-326">0 градусов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-326">0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-327">СВЕРХУ</span><span class="sxs-lookup"><span data-stu-id="b62b3-327">LANDSCAPE</span></span></td>
<td><span data-ttu-id="b62b3-328">коэффициент в 90 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</span><span class="sxs-lookup"><span data-stu-id="b62b3-328">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-329">ROT180</span><span class="sxs-lookup"><span data-stu-id="b62b3-329">ROT180</span></span></td>
<td><span data-ttu-id="b62b3-330">коэффициент в 180 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</span><span class="sxs-lookup"><span data-stu-id="b62b3-330">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-331">ROT270</span><span class="sxs-lookup"><span data-stu-id="b62b3-331">ROT270</span></span></td>
<td><span data-ttu-id="b62b3-332">коэффициент в 270 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</span><span class="sxs-lookup"><span data-stu-id="b62b3-332">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <span data-ttu-id="b62b3-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>сканнерпиктурепажесизе</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-334">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-334">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-335">Содержит размер страницы, для которой в настоящий момент выбрана проверка.</span><span class="sxs-lookup"><span data-stu-id="b62b3-335">Contains the size of the page that is currently set to be scanned.</span></span> <span data-ttu-id="b62b3-336">Приложение задает это свойство, чтобы выбрать размеры сканируемой страницы.</span><span class="sxs-lookup"><span data-stu-id="b62b3-336">An application sets this property to select the dimensions of the page to scan.</span></span> <span data-ttu-id="b62b3-337">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-337">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-338">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-338">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="b62b3-339">Константы, которые можно использовать с этим свойством, см. в разделе <a href="-wia-wia2-pagesizeconstants.md"><strong>константы размера страницы WIA 2,0</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b62b3-339">For the constants that can be used with this property, see <a href="-wia-wia2-pagesizeconstants.md"><strong>WIA 2.0 Page Size Constants</strong></a>.</span></span> <span data-ttu-id="b62b3-340">Обратите внимание на следующие нефиксированные размеры, в частности:</span><span class="sxs-lookup"><span data-stu-id="b62b3-340">Note these non-fixed sizes, in particular:</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-341">Значение</span><span class="sxs-lookup"><span data-stu-id="b62b3-341">Value</span></span></th>
<th><span data-ttu-id="b62b3-342">Определение</span><span class="sxs-lookup"><span data-stu-id="b62b3-342">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-343">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="b62b3-343">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="b62b3-344">Определяется значениями свойств <strong>WIA_IPS_PAGE_HEIGHT</strong> и <strong>WIA_IPS_PAGE_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="b62b3-344">Defined by the values of the <strong>WIA_IPS_PAGE_HEIGHT</strong> and <strong>WIA_IPS_PAGE_WIDTH</strong> properties.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-345">WIA_PAGE_AUTO</span><span class="sxs-lookup"><span data-stu-id="b62b3-345">WIA_PAGE_AUTO</span></span></td>
<td><span data-ttu-id="b62b3-346">Размер страницы определяется устройством автоматически.</span><span class="sxs-lookup"><span data-stu-id="b62b3-346">Page size is automatically determined by the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-347">WIA_PAGE_CUSTOM_BASE</span><span class="sxs-lookup"><span data-stu-id="b62b3-347">WIA_PAGE_CUSTOM_BASE</span></span></td>
<td><span data-ttu-id="b62b3-348">Пользовательский размер страницы, размеры которого уже известны приложению и драйверу устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-348">A custom page size whose dimensions are already known to the application and the device driver.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b62b3-349">Значение свойства <strong>WIA_IPS_ORIENTATION</strong> определяет ориентацию текущей выбранной страницы.</span><span class="sxs-lookup"><span data-stu-id="b62b3-349">The value of the <strong>WIA_IPS_ORIENTATION</strong> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="b62b3-350">Свойства <strong>WIA_IPS_PAGE_WIDTH</strong> и <strong>WIA_IPS_PAGE_HEIGHT</strong> сообщают о размерах страницы в тысячах дюйма.</span><span class="sxs-lookup"><span data-stu-id="b62b3-350">The <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="b62b3-351">Эти свойства должны быть согласованы с <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong>, которые содержат размеры страницы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-351">These properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-352">Допустимые значения типа WIA_PROP_LIST зависят от допустимых параметров свойства <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="b62b3-352">Valid values of type WIA_PROP_LIST depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="b62b3-353">Если, например, устройство не может сканировать альбомные документы с помощью параметра WIA_PAGE_A4, WIA_PAGE_A4 не является допустимым значением свойства <strong>WIA_IPS_PAGE_SIZE</strong> , если <strong>WIA_IPS_ORIENTATION</strong> установлен в альбомную ориентацию.</span><span class="sxs-lookup"><span data-stu-id="b62b3-353">If, for example, the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 is not a valid value for the <strong>WIA_IPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-354">Если приложение устанавливает <strong>WIA_IPS_PAGE_SIZE</strong> любое значение, отличное от трех в таблице выше, минидривер должен скорректировать значения <strong>WIA_IPS_PAGE_WIDTH</strong> и <strong>WIA_IPS_PAGE_HEIGHT</strong> в размерах страницы в тысячах дюйма.</span><span class="sxs-lookup"><span data-stu-id="b62b3-354">If an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to any value other than the three in the table above, the minidriver should adjust the values of <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="b62b3-355">Он также должен скорректировать значения <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong> к размерам страницы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-355">It should also adjust the values of <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="b62b3-356">Если параметр экстента (<strong>WIA_IPS_XEXTENT</strong> или <strong>WIA_IPS_YEXTENT</strong>) изменяется на значение, не совпадающее с текущим параметром размера страницы, минидривер должен изменить значение свойства <strong>WIA_IPS_PAGE_SIZE</strong> на WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-356">If an extent setting (<strong>WIA_IPS_XEXTENT</strong> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page size setting, the minidriver should change the value of the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="b62b3-357">Минидривер также должен изменить <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> или <strong>WIA_IPS_PAGE_HEIGHT</strong> в соответствии с новым параметром экстента.</span><span class="sxs-lookup"><span data-stu-id="b62b3-357">The minidriver should also modify <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> or <strong>WIA_IPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="b62b3-358">Если параметр <strong>WIA_IPS_ORIENTATION</strong> имеет значение альбомная, параметры экстента будут передаваться относительно их обычных значений.</span><span class="sxs-lookup"><span data-stu-id="b62b3-358">If <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE, the extent settings will be exchanged relative to their usual values.</span></span> <span data-ttu-id="b62b3-359">Например, если приложение устанавливает <strong>WIA_IPS_PAGE_SIZE</strong> в WIA_PAGE_A4, минидривер устанавливает для <strong>WIA_IPS_PAGE_WIDTH</strong> значение 11692, а <strong>WIA_IPS_PAGE_HEIGHT</strong> — 8267.</span><span class="sxs-lookup"><span data-stu-id="b62b3-359">For example, if an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver sets <strong>WIA_IPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_IPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="b62b3-360">(Минидривер также должен соответствующим образом скорректировать <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong> .)</span><span class="sxs-lookup"><span data-stu-id="b62b3-360">(The minidriver should also adjust <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.)</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-361">Если <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> имеет значение WIA_PAGE_CUSTOM, параметр ориентации не используется для определения размеров сканируемой страницы.</span><span class="sxs-lookup"><span data-stu-id="b62b3-361">If <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-362">Минидривер отвечает за обеспечение соответствия свойства <strong>WIA_IPS_ORIENTATION</strong> с текущей областью выбора.</span><span class="sxs-lookup"><span data-stu-id="b62b3-362">The minidriver is responsible for ensuring that the <strong>WIA_IPS_ORIENTATION</strong> property is in agreement with the current selection area.</span></span> <span data-ttu-id="b62b3-363">Если приложение изменяет значение <strong>WIA_IPS_ORIENTATION</strong> на другое, недопустимое для текущего выбранного размера страницы, минидривер должен изменить значение <strong>WIA_IPS_PAGE_SIZE</strong> на размер страницы, поддерживаемый новым значением ориентации.</span><span class="sxs-lookup"><span data-stu-id="b62b3-363">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_IPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="b62b3-364">Если приложение задает для свойства <strong>WIA_IPS_PAGE_SIZE</strong> значение WIA_PAGE_CUSTOM, то область текущего выбора не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b62b3-364">If an application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="b62b3-365">WIA минидривер должен получить текущий макет изображения, начиная с текущих параметров свойств <strong>WIA_IPS_XPOS</strong> и <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="b62b3-365">The WIA minidriver should obtain the current image layout, starting from the current settings of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="b62b3-366">Если параметр размера страницы приводит к выделению области выделения, находящегося за пределами испытательного сканера, минидривер должен автоматически скорректировать значения <strong>WIA_IPS_XPOS</strong> и <strong>WIA_IPS_YPOS</strong> свойства на допустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="b62b3-366">If the page size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="b62b3-367">Если свойства <strong>WIA_IPS_PAGE_SIZE</strong> и <strong>WIA_IPS_ORIENTATION</strong> задаются одновременно и являются недопустимыми при их применении в сочетании, минидривер не должен возвращать параметры приложения, возвращая ошибку в <a href="https://msdn.microsoft.com/library/ms794145.aspx">ивиаминидрв::d рввалидатеитемпропертиес</a>.</span><span class="sxs-lookup"><span data-stu-id="b62b3-367">If the <strong>WIA_IPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span></p>
<p><span data-ttu-id="b62b3-368">В следующих четырех примерах показаны различные сценарии <strong>WIA_IPS_PAGE_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="b62b3-368">The following four examples show different <strong>WIA_IPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="b62b3-369">Драйвер сообщает о параметрах.</span><span class="sxs-lookup"><span data-stu-id="b62b3-369">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="b62b3-370">Приложение задает для свойства <strong>WIA_IPS_PAGE_SIZE</strong> значение WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="b62b3-370">An application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="b62b3-371">Приложение устанавливает для свойства <strong>WIA_IPS_ORIENTATION</strong> значение альбомная ориентация.</span><span class="sxs-lookup"><span data-stu-id="b62b3-371">An application sets the <strong>WIA_IPS_ORIENTATION</strong> property to LANDSCAPE.</span></span></li>
<li><span data-ttu-id="b62b3-372">Приложение изменяет свойство <strong>WIA_IPS_XEXTENT</strong> на меньшее значение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-372">An application changes the <strong>WIA_IPS_XEXTENT</strong> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="b62b3-373"><strong>Пример 1. минидривер сообщает о параметрах</strong></span><span class="sxs-lookup"><span data-stu-id="b62b3-373"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="b62b3-374">В следующем примере минидривер задает настраиваемую область выбора до того, как приложение установит все свойства WIA.</span><span class="sxs-lookup"><span data-stu-id="b62b3-374">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="b62b3-375">В этом случае область выбора представляет все стекло.</span><span class="sxs-lookup"><span data-stu-id="b62b3-375">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="b62b3-376"><strong>Пример 2. приложение задает</strong> <strong></strong><strong>для свойства</strong> WIA_IPS_PAGE_SIZE значение WIA_PAGE_LETTER  </span><span class="sxs-lookup"><span data-stu-id="b62b3-376"><strong>Example 2: An application sets the</strong> <strong>WIA_IPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="b62b3-377"><strong>Пример 3. приложение задает</strong> <strong></strong><strong>для свойства WIA_IPS_ORIENTATION значение альбомная</strong>  </span><span class="sxs-lookup"><span data-stu-id="b62b3-377"><strong>Example 3: An application sets the</strong> <strong>WIA_IPS_ORIENTATION</strong>  <strong>property to LANDSCAPE</strong></span></span></p>
<p><span data-ttu-id="b62b3-378">Физическая среда должна иметь возможность получить страницу, которая изначально была в альбомной ориентации.</span><span class="sxs-lookup"><span data-stu-id="b62b3-378">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="b62b3-379"><strong>Пример 4. приложение изменяет</strong> свойство <strong>WIA_IPS_XEXTENT</strong> <strong>на меньшее значение</strong></span><span class="sxs-lookup"><span data-stu-id="b62b3-379"><strong>Example 4: An application changes the</strong> <strong>WIA_IPS_XEXTENT</strong> <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="b62b3-380">В следующем примере приложение изменяет свойство <strong>WIA_IPS_XEXTENT</strong> на 1000.</span><span class="sxs-lookup"><span data-stu-id="b62b3-380">In the following example, an application changes the <strong>WIA_IPS_XEXTENT</strong> property to 1000.</span></span> <span data-ttu-id="b62b3-381">Минидривер должен предположить, что новое значение, содержащееся в <strong>WIA_IPS_XEXTENT</strong> , больше не является допустимым для свойства <strong>WIA_IPS_PAGE_SIZE</strong> и, таким образом, изменит <strong>WIA_IPS_PAGE_SIZE</strong> на WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-381">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_IPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="b62b3-382">Минидривер также должен корректировать <strong>WIA_IPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="b62b3-382">The minidriver must also adjust <strong>WIA_IPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <span data-ttu-id="b62b3-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>сканнерпиктурепажехеигхт</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-384">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-384">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-385">Содержит высоту (в тысячах дюйма) текущей выбранной страницы.</span><span class="sxs-lookup"><span data-stu-id="b62b3-385">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="b62b3-386">Минидривер создает и поддерживает свойство <strong>WIA_IPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="b62b3-386">The minidriver creates and maintains the <strong>WIA_IPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="b62b3-387">Приложение считывает это свойство, чтобы определить физические размеры сканируемой страницы.</span><span class="sxs-lookup"><span data-stu-id="b62b3-387">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="b62b3-388">Если параметры экстента отличаются от размеров известных страниц, это свойство сообщает высоту страницы, для которой свойство <strong>WIA_IPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM (которое является значением свойства <strong>WIA_IPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="b62b3-388">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_IPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="b62b3-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> должны быть синхронизированы с <strong>WIA_IPS_XEXTENT</strong>, которая сообщает высоту сканируемой страницы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> must be in sync with <strong>WIA_IPS_XEXTENT</strong>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="b62b3-390">Это свойство является обязательным для WIA_CATEGORY_FEEDER элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-390">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="b62b3-391">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <span data-ttu-id="b62b3-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>сканнерпиктурепажевидс</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-393">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-393">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-394">Содержит ширину текущей выбранной страницы в тысячах дюйма.</span><span class="sxs-lookup"><span data-stu-id="b62b3-394">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="b62b3-395">Приложение считывает это свойство, чтобы определить физические размеры сканируемой страницы.</span><span class="sxs-lookup"><span data-stu-id="b62b3-395">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="b62b3-396">Если параметры экстента отличаются от размеров известных страниц, это свойство сообщает ширину страницы, для которой свойство <strong>WIA_IPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-396">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="b62b3-397"><strong>WIA_IPS_PAGE_WIDTH</strong> должны быть синхронизированы со значением <strong>WIA_IPS_XEXTENT</strong>, которое показывает ширину сканируемой страницы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-397"><strong>WIA_IPS_PAGE_WIDTH</strong> must be in sync with the value of <strong>WIA_IPS_XEXTENT</strong>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="b62b3-398">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-398">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-399">Это свойство является обязательным для WIA_CATEGORY_FEEDER элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-399">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="b62b3-400">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-400">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <span data-ttu-id="b62b3-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>сканнерпиктурепажес</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-402">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-402">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-403">Содержит текущее число страниц, получаемых из автоматического устройства подачи документов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-403">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="b62b3-404">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-404">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-405">Тип: <strong>VT_I4</strong>; Доступ: чтение и запись; Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> это ноль до максимального количества страниц, которое может сканировать сканер.</span><span class="sxs-lookup"><span data-stu-id="b62b3-405">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> This is zero through the maximum number of pages that the scanner can scan.</span></span> <span data-ttu-id="b62b3-406">Значение ALL_PAGES (= 0), если сканер может сканироваться непрерывно.</span><span class="sxs-lookup"><span data-stu-id="b62b3-406">The value is ALL_PAGES (= 0) if the scanner can scan continuously.</span></span></p>
<p><span data-ttu-id="b62b3-407">Приложение считывает это свойство для определения емкости страницы устройства подачи документов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-407">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="b62b3-408">Приложение также задает для этого свойства число страниц, которое он будет сканировать.</span><span class="sxs-lookup"><span data-stu-id="b62b3-408">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-409">Если включен дуплексный режим (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> установлен в "Feed" | ДУПЛЕКС | ADVANCED_DUPLEX) <strong>WIA_IPS_PAGES</strong> по-прежнему равно числу сканируемых страниц.</span><span class="sxs-lookup"><span data-stu-id="b62b3-409">If duplex mode is enabled (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-410">Один лист бумаги автоматически будет содержать две страницы, если ДУПЛЕКСный режим включен, даже если обратная сторона страницы пуста.</span><span class="sxs-lookup"><span data-stu-id="b62b3-410">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="b62b3-411">Если задать для <strong>WIA_IPS_PAGES</strong> значение 1, то сканер будет обрабатывать одну сторону страницы.</span><span class="sxs-lookup"><span data-stu-id="b62b3-411">Setting <strong>WIA_IPS_PAGES</strong> to 1 causes a scanner to process one side of the page.</span></span> <span data-ttu-id="b62b3-412">Рекомендуется, если сканер не может сканировать только одну сторону страницы в режиме дуплекса, вы изменяете значение <strong>WIA_IPS_PAGES</strong> для элемента Inc элемента Range структуры WIA_PROPERTY_INFO на 2.</span><span class="sxs-lookup"><span data-stu-id="b62b3-412">We recommend that, if a scanner is unable to scan only one side of a page while in duplex mode, you change the <strong>WIA_IPS_PAGES</strong> value for the Inc member of the Range member of the WIA_PROPERTY_INFO structure to 2.</span></span> <span data-ttu-id="b62b3-413">Это значение сигнализирует приложению, что оно должно запрашивать страницы, кратные двум.</span><span class="sxs-lookup"><span data-stu-id="b62b3-413">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="b62b3-414">Значение ALL_PAGES (= 0) означает, что будут проверяться <em>все</em> страницы, загруженные в данный момент в устройство подачи документов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-414">A value of ALL_PAGES (= 0) means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <span data-ttu-id="b62b3-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>сканнерпиктурефотометриЦинтерп</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-416">Содержит текущее значение для белых и черных пикселей.</span><span class="sxs-lookup"><span data-stu-id="b62b3-416">Contains the current setting for white and black pixels.</span></span> <span data-ttu-id="b62b3-417">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-417">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-418">Приложение считывает это значение, чтобы определить значение белого или черного (в зависимости от того, что делает приложение).</span><span class="sxs-lookup"><span data-stu-id="b62b3-418">An application reads this value to determine the value of WHITE or BLACK (depending on what the application is doing).</span></span></p>
<p><span data-ttu-id="b62b3-419">Требуется для всех включенных приобретений или сохраненных элементов; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-419">Required for all acquisition enabled or stored items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="b62b3-420">Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-420">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="b62b3-421">Тип: <strong>VT_I4</strong>; Доступ: чтение и запись; Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="b62b3-421">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="b62b3-422">Если для устройства можно задать только одно значение, создайте тип WIA_PROP_LIST и поместите в него допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-422">If the device can be set to only a single value, create a WIA_PROP_LIST type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="b62b3-423">В следующей таблице приведены две константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-423">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-424">Значение</span><span class="sxs-lookup"><span data-stu-id="b62b3-424">Value</span></span></th>
<th><span data-ttu-id="b62b3-425">Определение</span><span class="sxs-lookup"><span data-stu-id="b62b3-425">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-426">WIA_PHOTO_WHITE_0</span><span class="sxs-lookup"><span data-stu-id="b62b3-426">WIA_PHOTO_WHITE_0</span></span></td>
<td><span data-ttu-id="b62b3-427">БЕЛЫЙ цвет равен 0, а черный — 1.</span><span class="sxs-lookup"><span data-stu-id="b62b3-427">WHITE is 0, and BLACK is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-428">WIA_PHOTO_WHITE_1</span><span class="sxs-lookup"><span data-stu-id="b62b3-428">WIA_PHOTO_WHITE_1</span></span></td>
<td><span data-ttu-id="b62b3-429">БЕЛЫЙ цвет равен 1, а черный — 0.</span><span class="sxs-lookup"><span data-stu-id="b62b3-429">WHITE is 1, and BLACK is 0.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <span data-ttu-id="b62b3-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>сканнерпиктурепревиев</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-431">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-431">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-432">Указывает режим предварительного просмотра для устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-432">Indicates the preview mode for a device.</span></span> <span data-ttu-id="b62b3-433">Приложение задает это свойство, чтобы перевести устройство в режим предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="b62b3-433">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="b62b3-434">Это свойство является обязательным для элементов WIA_CATEGORY_FLATBED и WIA_CATEGORY_FILM, необязательно для элемента WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="b62b3-434">This property is required for the WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items, optional for the WIA_CATEGORY_FEEDER item.</span></span></p>
<p><span data-ttu-id="b62b3-435">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-435">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="b62b3-436">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-436">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-437">Значение</span><span class="sxs-lookup"><span data-stu-id="b62b3-437">Value</span></span></th>
<th><span data-ttu-id="b62b3-438">Определение</span><span class="sxs-lookup"><span data-stu-id="b62b3-438">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-439">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="b62b3-439">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="b62b3-440">Приложение выполнит окончательную проверку.</span><span class="sxs-lookup"><span data-stu-id="b62b3-440">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-441">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="b62b3-441">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="b62b3-442">Приложение будет выполнять предварительную проверку.</span><span class="sxs-lookup"><span data-stu-id="b62b3-442">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <span data-ttu-id="b62b3-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>сканнерпиктурепревиевтипе</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-444">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-444">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-445">Указывает, можно ли обновить существующее изображение предварительного просмотра во время просмотра изображения (в ответ на изменение свойств WIA_IPA_DATATYPE или WIA_IPA_DEPTH).</span><span class="sxs-lookup"><span data-stu-id="b62b3-445">Specifies whether the existing preview image can be updated during an image preview (in response to a change in the WIA_IPA_DATATYPE or WIA_IPA_DEPTH properties).</span></span></p>
<p><span data-ttu-id="b62b3-446">Это свойство является необязательным для всех элементов с включенным приобретением, поддерживающих предварительные проверки. то есть WIA_IPS_PREVIEW поддерживается с WIA_PREVIEW_SCAN.</span><span class="sxs-lookup"><span data-stu-id="b62b3-446">This property is optional for all acquisition enabled items that support preview scans; that is, WIA_IPS_PREVIEW is supported with WIA_PREVIEW_SCAN.</span></span> <span data-ttu-id="b62b3-447">К ним относятся элементы типов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-447">This includes items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="b62b3-448">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-448">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b62b3-449">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-449">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-450">Константа</span><span class="sxs-lookup"><span data-stu-id="b62b3-450">Constant</span></span></th>
<th><span data-ttu-id="b62b3-451">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-451">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-452">WIA_ADVANCED_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="b62b3-452">WIA_ADVANCED_PREVIEW</span></span></td>
<td><span data-ttu-id="b62b3-453">Возможно обновление существующего образа.</span><span class="sxs-lookup"><span data-stu-id="b62b3-453">Updating the existing image is possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-454">WIA_BASIC_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="b62b3-454">WIA_BASIC_PREVIEW</span></span></td>
<td><span data-ttu-id="b62b3-455">Необходимо выполнить еще одну предварительную проверку, так как обновление существующего образа невозможно.</span><span class="sxs-lookup"><span data-stu-id="b62b3-455">Another preview scan must be executed because updating the existing image is not possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <span data-ttu-id="b62b3-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>сканнерпиктуреротатион</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-457">Содержит текущий параметр вращения, если он реализован.</span><span class="sxs-lookup"><span data-stu-id="b62b3-457">Contains the current rotation setting, if it is implemented.</span></span> <span data-ttu-id="b62b3-458">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-458">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-459">Приложение задает это свойство, чтобы сообщить драйверу, какой объем (если вообще) нужно повернуть изображение, прежде чем драйвер вернет его в приложение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-459">An application sets this property to inform the driver how much (if at all) to rotate the image before the driver returns it to the application.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-460">WIA_IPS_ORIENTATION указывает на расположение документа, который будет проверяться на сканере или в податчике.</span><span class="sxs-lookup"><span data-stu-id="b62b3-460">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="b62b3-461">Это ориентация документа относительно направления сканирования.</span><span class="sxs-lookup"><span data-stu-id="b62b3-461">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="b62b3-462">WIA_IPS_ROTATION относится к повороту, который применяется к изображению после его сканирования, непосредственно перед передачей изображения в приложение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-462">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-463">WIA-минидривер отвечает за вращение данных изображения перед их отправкой обратно в приложение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-463">The WIA minidriver is responsible for rotating the image data before sending it back to the application.</span></span> <span data-ttu-id="b62b3-464">Приложение несет ответственность за проверку заголовков изображений, чтобы увидеть только что повернутые значения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-464">The application is responsible for checking the image headers to see the newly rotated values.</span></span></p>
<p><span data-ttu-id="b62b3-465">Существует значительная путаница, связанная с разрешением воздействия вращения на область выбора текущего изображения (которая определяется свойствами <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong> ).</span><span class="sxs-lookup"><span data-stu-id="b62b3-465">Considerable confusion exists about resolving the effect of rotation on the current image's selection area (which is defined by the <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> properties).</span></span></p>
<p><span data-ttu-id="b62b3-466"><em>Область выбора</em> относится к выбранной области физической сканера, из которой запрашивается изображение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-466"><em>Selection area</em> refers to the selected area on the physical scanner bed that an image is be acquired from.</span></span> <span data-ttu-id="b62b3-467"><strong>WIA_IPS_ROTATION</strong> не изменяет область выбора.</span><span class="sxs-lookup"><span data-stu-id="b62b3-467"><strong>WIA_IPS_ROTATION</strong> does not modify the selection area.</span></span> <span data-ttu-id="b62b3-468">Драйвер применяет поворот против часовой стрелки в соответствии с <strong>WIA_IPS_ROTATION</strong> только после того, как драйвер приобрел соответствующую область выбора.</span><span class="sxs-lookup"><span data-stu-id="b62b3-468">The driver applies a counterclockwise rotation according to <strong>WIA_IPS_ROTATION</strong> only after the driver has acquired the appropriate selection area.</span></span> <span data-ttu-id="b62b3-469"><strong>WIA_IPS_ROTATION</strong> влияет на размеры выходного изображения, поэтому эти измерения должны быть отражены в заголовке данных полученного изображения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-469"><strong>WIA_IPS_ROTATION</strong> does affect the dimensions of the output image, so these dimensions must be reflected in the resulting image's data header.</span></span></p>
<p><span data-ttu-id="b62b3-470">Необязательно для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-470">Optional for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="b62b3-471">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-471">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="b62b3-472">Определены следующие константы вращения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-472">The following rotation constants are defined.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-473">Константа</span><span class="sxs-lookup"><span data-stu-id="b62b3-473">Constant</span></span></th>
<th><span data-ttu-id="b62b3-474">Определение</span><span class="sxs-lookup"><span data-stu-id="b62b3-474">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-475">КНИЖНОЙ ориентации</span><span class="sxs-lookup"><span data-stu-id="b62b3-475">PORTRAIT</span></span></td>
<td><span data-ttu-id="b62b3-476">Драйвер не будет поворачивать образ.</span><span class="sxs-lookup"><span data-stu-id="b62b3-476">The driver will not rotate the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-477">СВЕРХУ</span><span class="sxs-lookup"><span data-stu-id="b62b3-477">LANDSCAPE</span></span></td>
<td><span data-ttu-id="b62b3-478">Драйвер Tне поворачивает изображение 90 градусов против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="b62b3-478">TThe driver rotates the image 90 degrees counterclockwise.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-479">ROT180</span><span class="sxs-lookup"><span data-stu-id="b62b3-479">ROT180</span></span></td>
<td><span data-ttu-id="b62b3-480">Драйвер поворачивает изображение 180 градусов против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="b62b3-480">The driver rotates the image 180 degrees counterclockwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-481">ROT270</span><span class="sxs-lookup"><span data-stu-id="b62b3-481">ROT270</span></span></td>
<td><span data-ttu-id="b62b3-482">Драйвер поворачивает изображение 270 градусов против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="b62b3-482">The driver rotates the image 270 degrees counterclockwise.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <span data-ttu-id="b62b3-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>сканнерпиктуресегментатион</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-484">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-484">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-485">Указывает, должен ли приложение использовать фильтр сегментации драйвера для сканирования в нескольких регионах.</span><span class="sxs-lookup"><span data-stu-id="b62b3-485">Specifies whether the application should use the driver's segmentation filter for multi-region scanning.</span></span> <span data-ttu-id="b62b3-486">WIA_IPS_SEGMENTATION должны быть реализованы для WIA_CATEGORY_FLATBED и WIA_CATEGORY_FILM элементов, если они поддерживают создание дочерних элементов с фильтром сегментации или если сам драйвер создает дочерние элементы для фиксированных кадров.</span><span class="sxs-lookup"><span data-stu-id="b62b3-486">WIA_IPS_SEGMENTATION must be implemented for WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items if they support either the creation of child items with a segmentation filter or if the driver itself creates child items for fixed frames.</span></span></p>
<p><span data-ttu-id="b62b3-487">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-487">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b62b3-488">В следующей таблице приведены две константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-488">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-489">Значение</span><span class="sxs-lookup"><span data-stu-id="b62b3-489">Value</span></span></th>
<th><span data-ttu-id="b62b3-490">Определение</span><span class="sxs-lookup"><span data-stu-id="b62b3-490">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-491">WIA_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="b62b3-491">WIA_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="b62b3-492">Приложение должно использовать фильтр сегментации для сканирования в нескольких регионах.</span><span class="sxs-lookup"><span data-stu-id="b62b3-492">The application should use the segmentation filter for multi-region scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-493">WIA_DONT_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="b62b3-493">WIA_DONT_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="b62b3-494">Драйвер создает дочерние элементы для поиска в нескольких регионах.</span><span class="sxs-lookup"><span data-stu-id="b62b3-494">The driver creates the child items itself for multi-region scanning.</span></span> <span data-ttu-id="b62b3-495">Обычно это происходит, если сканер использует для этой цели фиксированные кадры.</span><span class="sxs-lookup"><span data-stu-id="b62b3-495">This is usually the case if the scanner uses fixed frames for this purpose.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-496">Драйвер может поступать с фильтром сегментации, но по-прежнему имеет WIA_IPS_SEGMENTATION WIA_DONT_USE_SEGMENTATION_FILTER для одного из его элементов (например, элемент WIA_CATEGORY_FILM).</span><span class="sxs-lookup"><span data-stu-id="b62b3-496">It is possible for a driver to come with a segmentation filter, but still have WIA_IPS_SEGMENTATION set to WIA_DONT_USE_SEGMENTATION_FILTER for one of its items (such as, the WIA_CATEGORY_FILM item).</span></span> <span data-ttu-id="b62b3-497">Это может быть так, если сканер использует фиксированные кадры для сканирования пленки, но не для обычного сканирования из WIA_CATEGORY_FLATBED элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-497">This could be the case if the scanner uses fixed frames for film scanning, but not for regular scanning from WIA_CATEGORY_FLATBED items.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <span data-ttu-id="b62b3-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>сканнерпиктурешитфидеррегистратион</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-499">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-499">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-500">Содержит регистрацию, выравнивание и обнаружение краев для документов, размещенных на планшете.</span><span class="sxs-lookup"><span data-stu-id="b62b3-500">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="b62b3-501">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-501">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="b62b3-502">Это свойство указывает, как располагается лист горизонтально в заголовке сканирования карманного компьютера или сканера с листовой подачи.</span><span class="sxs-lookup"><span data-stu-id="b62b3-502">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="b62b3-503">Свойство используется для прогнозирования места размещения документа по заголовку сканирования.</span><span class="sxs-lookup"><span data-stu-id="b62b3-503">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="b62b3-504">Для сканеров, поддерживающих несколько заголовков сканирования, это свойство задается относительно самого верхнего заголовка сканирования.</span><span class="sxs-lookup"><span data-stu-id="b62b3-504">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="b62b3-505">Это свойство является обязательным для сканеров подачи листов, прокрутки и карманных устройств.</span><span class="sxs-lookup"><span data-stu-id="b62b3-505">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="b62b3-506">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-506">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b62b3-507">В следующей таблице приведены три константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-507">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-508">Константа</span><span class="sxs-lookup"><span data-stu-id="b62b3-508">Constant</span></span></th>
<th><span data-ttu-id="b62b3-509">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-509">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-510">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="b62b3-510">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="b62b3-511">Лист располагается слева относительно заголовка сканирования.</span><span class="sxs-lookup"><span data-stu-id="b62b3-511">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-512">ПО центру</span><span class="sxs-lookup"><span data-stu-id="b62b3-512">CENTERED</span></span></td>
<td><span data-ttu-id="b62b3-513">Лист выравнивается по заголовку сканирования.</span><span class="sxs-lookup"><span data-stu-id="b62b3-513">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62b3-514">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="b62b3-514">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="b62b3-515">Лист располагается вправо относительно головного поиска.</span><span class="sxs-lookup"><span data-stu-id="b62b3-515">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <span data-ttu-id="b62b3-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>сканнерпиктурешовпревиевконтрол</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-517">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-517">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-518">Указывает, должен ли элемент отображаться в элементе управления предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="b62b3-518">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="b62b3-519">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-519">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-520">Необязательно для всех элементов с поддержкой перемещения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-520">Optional for all transfer enabled items.</span></span> <span data-ttu-id="b62b3-521">Обычно это просто элементы категорий WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM и WIA_CATEGORY_FINISHED_FILE.</span><span class="sxs-lookup"><span data-stu-id="b62b3-521">This is usually just items of the categories WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM, and WIA_CATEGORY_FINISHED_FILE.</span></span></p>
<p><span data-ttu-id="b62b3-522">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-522">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b62b3-523">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-523">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b62b3-524">Константа</span><span class="sxs-lookup"><span data-stu-id="b62b3-524">Constant</span></span></th>
<th><span data-ttu-id="b62b3-525">Описание</span><span class="sxs-lookup"><span data-stu-id="b62b3-525">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62b3-526">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="b62b3-526">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="b62b3-527">Отображение элемента управления предварительным просмотром для пользователя, так как это устройство может выполнять предварительную версию.</span><span class="sxs-lookup"><span data-stu-id="b62b3-527">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62b3-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="b62b3-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="b62b3-529">Не показывать пользователю элемент управления предварительной версии, так как это устройство не может выполнить предварительную версию.</span><span class="sxs-lookup"><span data-stu-id="b62b3-529">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <span data-ttu-id="b62b3-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>сканнерпиктуресуппортсчилдитемкреатион</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-531">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-531">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-532">Указывает, могут ли приложение (или фильтры) создавать дочерние элементы в текущем элементе.</span><span class="sxs-lookup"><span data-stu-id="b62b3-532">Specifies whether the application (or the filters) can create child items under the current item.</span></span></p>
<p><span data-ttu-id="b62b3-533">Необязательно для всех категорий элементов с поддержкой перемещения: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM и даже WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="b62b3-533">Optional for all transfer enabled item categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM and even WIA_CATEGORY_FOLDER.</span></span> <span data-ttu-id="b62b3-534">(Если хранилище не поддерживает отправку новых элементов, это свойство должно быть неподдерживаемым или не поддерживаться со значением <strong>false</strong> .)</span><span class="sxs-lookup"><span data-stu-id="b62b3-534">(If the storage won't support upload of new items then this property should be either unsupported or supported with the <strong>FALSE</strong> value.)</span></span></p>
<p><span data-ttu-id="b62b3-535">Элементы, поддерживающие WIA_IPS_SEGMENTATION и WIA_USE_SEGMENTATION_FILTER, также должны поддерживать WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION и иметь значение <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="b62b3-535">Items supporting WIA_IPS_SEGMENTATION and WIA_USE_SEGMENTATION_FILTER must also support WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION and have it set to <strong>TRUE</strong>.</span></span></p>
<p><span data-ttu-id="b62b3-536">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <strong>true</strong> и <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="b62b3-536">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <strong>TRUE</strong> and <strong>FALSE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <span data-ttu-id="b62b3-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>сканнерпиктуресрешолд</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-538">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-538">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-539">Задает значение градации серого, которое определяет, будет ли при преобразовании изображения в монохромное изображение преобразовано в белый или черный цвет.</span><span class="sxs-lookup"><span data-stu-id="b62b3-539">Specifies the grayscale value that determines whether a pixel will be converted to white or black when an image is converted to monochromatic.</span></span> <span data-ttu-id="b62b3-540">Пиксели выше порогового значения становятся белыми.</span><span class="sxs-lookup"><span data-stu-id="b62b3-540">Pixels above the threshold become white.</span></span> <span data-ttu-id="b62b3-541">Пиксели ниже порогового значения становятся белым.</span><span class="sxs-lookup"><span data-stu-id="b62b3-541">Pixels below the threshold become white.</span></span></p>
<p><span data-ttu-id="b62b3-542">Это свойство требуется для элементов сбора, поддерживающих сканирование 1 бит и имеющее для свойства WIA_IPA_DATATYPE значение WIA_DATA_THRESHOLD.</span><span class="sxs-lookup"><span data-stu-id="b62b3-542">This property is required for acquisition items that support 1-bpp scans and that have the WIA_IPA_DATATYPE property set to WIA_DATA_THRESHOLD.</span></span></p>
<p><span data-ttu-id="b62b3-543">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-543">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <span data-ttu-id="b62b3-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>сканнерпиктуретрансферкапабилитиес</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-545">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-545">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-546">Указывает, способен ли драйвер передавать несколько дочерних элементов в одном вызове передачи.</span><span class="sxs-lookup"><span data-stu-id="b62b3-546">Specifies whether the driver is capable of transferring multiple child items in single transfer call.</span></span></p>
<p><span data-ttu-id="b62b3-547">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-547">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="b62b3-548">Единственное возможное значение для этого свойства — WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span><span class="sxs-lookup"><span data-stu-id="b62b3-548">The only possible value for this property is WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span></span> <span data-ttu-id="b62b3-549">Если этот флаг установлен, драйвер способен передавать несколько дочерних элементов в одном вызове функции перемещения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-549">If this flag is set, then the driver is capable of transfering multiple child items in single transfer call.</span></span> <span data-ttu-id="b62b3-550">Если флаг не установлен, служба WIA будет рекурсивно проходить по дочерним элементам, а затем переносить каждый из этих элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-550">If the flag is not set, the WIA Service will walk through the child items recursively and then transfer each of those items.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="b62b3-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>сканнерпиктуреинверт</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-552">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-552">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-553">Указывает число байтов для отправки для элемента.</span><span class="sxs-lookup"><span data-stu-id="b62b3-553">Specifies the number of bytes to upload for the item.</span></span></p>
<p><span data-ttu-id="b62b3-554">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-554">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <span data-ttu-id="b62b3-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>сканнерпиктуревармуптиме</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-556">Указывает максимальное время прогрева (в миллисекундах), необходимое устройству перед запуском операции сканирования.</span><span class="sxs-lookup"><span data-stu-id="b62b3-556">Specifies the maximum warm-up time, in milliseconds, that the device needs before starting the scanning operation.</span></span> <span data-ttu-id="b62b3-557">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-557">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-558">Приложение может прочитать это свойство, чтобы определить максимальное время прогрева для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-558">An application can read this property to determine the maximum warm-up time for this device.</span></span> <span data-ttu-id="b62b3-559">Затем он может предоставить &quot; диалоговое окно ожидание прогрева устройства &quot; , чтобы сообщить пользователю о том, что ожидание или пауза может произойти до чего-либо.</span><span class="sxs-lookup"><span data-stu-id="b62b3-559">It can then present a &quot;waiting for the device to warm up&quot; dialog box, to let the user know that a wait or pause might occur before anything happens.</span></span></p>
<p><span data-ttu-id="b62b3-560">Это свойство является обязательным для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-560">This property is required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="b62b3-561">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <span data-ttu-id="b62b3-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>сканнерпиктурексекстент</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-563">Содержит текущую ширину (в пикселях) выбранного изображения для получения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-563">Contains the current width, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="b62b3-564">Приложение задает это свойство, чтобы пометить ширину области выбора для получения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-564">An application sets this property to mark the width of a selection area to acquire.</span></span> <span data-ttu-id="b62b3-565">Это свойство должно быть согласовано со свойством <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b62b3-565">This property must agree with the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="b62b3-566">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-566">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-567">Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-567">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="b62b3-568">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-568">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <span data-ttu-id="b62b3-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>сканнерпиктурекспос</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-570">Содержит координату x (в пикселях) верхнего левого угла выбранного изображения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-570">Contains the x coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="b62b3-571">Приложение задает это свойство, чтобы пометить левый верхний угол области выделения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-571">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="b62b3-572">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-572">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-573">Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-573">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="b62b3-574">Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-574">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="b62b3-575">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-575">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <span data-ttu-id="b62b3-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>сканнерпиктурексрес</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-577">Содержит текущее разрешение по горизонтали (в пикселях на дюйм) для устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-577">Contains the current horizontal resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="b62b3-578">Приложение задает это свойство для установки разрешения по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="b62b3-578">An application sets this property to set the horizontal resolution.</span></span> <span data-ttu-id="b62b3-579">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-579">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-580">Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-580">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="b62b3-581">Это также случай, когда один параметр разрешения зависит от другого разрешения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-581">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="b62b3-582">(Разрешение по вертикали может зависеть от разрешения по горизонтали.)</span><span class="sxs-lookup"><span data-stu-id="b62b3-582">(The vertical resolution can depend on the horizontal resolution.)</span></span></p>
<p><span data-ttu-id="b62b3-583">Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-583">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="b62b3-584">Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-584">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="b62b3-585">Тип: <strong>VT_I4</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> или WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="b62b3-585">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <span data-ttu-id="b62b3-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>сканнерпиктурексскалинг</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-587">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-587">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-588">Задает горизонтальное масштабирование в процентах, которое может быть применено к отсканированным изображениям в устройстве сканера или его драйвере.</span><span class="sxs-lookup"><span data-stu-id="b62b3-588">Sets the horizontal scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="b62b3-589">Это свойство является необязательным для всех элементов с включенным приобретением. то есть элементы типов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-589">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="b62b3-590">Тип: <strong>VT_I4</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="b62b3-590">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="b62b3-591">Значения могут быть от 1 до максимального VT_I4 (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="b62b3-591">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="b62b3-592">Например, 100 означает отсутствие масштабирования, 050 означает масштабирование до 50% от размера Оригнал, а 200 означает масштабирование до 200% исходного размера.</span><span class="sxs-lookup"><span data-stu-id="b62b3-592">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <span data-ttu-id="b62b3-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>сканнерпиктурэйекстент</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-594">Содержит текущую высоту (в пикселях) выбранного изображения для получения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-594">Contains the current height, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="b62b3-595">Приложение задает это свойство, чтобы пометить высоту области выделения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-595">An application sets this property to mark the height of a selection area.</span></span> <span data-ttu-id="b62b3-596">Это свойство должно быть согласовано со значением свойства <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b62b3-596">This property must be agree with the value of the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="b62b3-597">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-597">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-598">Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-598">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="b62b3-599">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-599">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <span data-ttu-id="b62b3-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>сканнерпиктурэйпос</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-601">Текущая координата y (в пикселях) верхнего левого угла выбранного изображения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-601">Current y coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="b62b3-602">Приложение задает это свойство, чтобы пометить левый верхний угол области выделения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-602">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="b62b3-603">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-603">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-604">Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-604">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="b62b3-605">Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-605">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="b62b3-606">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="b62b3-606">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <span data-ttu-id="b62b3-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>сканнерпиктурэйрес</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b62b3-608">Содержит текущее разрешение по вертикали (в пикселях на дюйм) для устройства.</span><span class="sxs-lookup"><span data-stu-id="b62b3-608">Contains the current vertical resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="b62b3-609">Приложение задает это свойство для установки разрешения по вертикали.</span><span class="sxs-lookup"><span data-stu-id="b62b3-609">An application sets this property to set the vertical resolution.</span></span> <span data-ttu-id="b62b3-610">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b62b3-610">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b62b3-611">Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="b62b3-611">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="b62b3-612">Это также случай, когда один параметр разрешения зависит от другого разрешения.</span><span class="sxs-lookup"><span data-stu-id="b62b3-612">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="b62b3-613">(Разрешение по горизонтали может зависеть от вертикального разрешения.)</span><span class="sxs-lookup"><span data-stu-id="b62b3-613">(The horizontal resolution can depend on the vertical resolution.)</span></span></p>
<p><span data-ttu-id="b62b3-614">Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-614">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="b62b3-615">Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</span><span class="sxs-lookup"><span data-stu-id="b62b3-615">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="b62b3-616">Тип: <strong>VT_I4</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> или WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="b62b3-616">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <span data-ttu-id="b62b3-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>сканнерпиктурэйскалинг</dt> </span><span class="sxs-lookup"><span data-stu-id="b62b3-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b62b3-618">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="b62b3-618">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b62b3-619">Задает вертикальное масштабирование в процентах, которое может быть применено к отсканированным изображениям в устройстве сканера или его драйвере.</span><span class="sxs-lookup"><span data-stu-id="b62b3-619">Sets the vertical scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="b62b3-620">Это свойство является необязательным для всех элементов с включенным приобретением. то есть элементы типов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="b62b3-620">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="b62b3-621">Тип: <strong>VT_I4</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="b62b3-621">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="b62b3-622">Значения могут быть от 1 до максимального VT_I4 (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="b62b3-622">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="b62b3-623">Например, 100 означает отсутствие масштабирования, 050 означает масштабирование до 50% от размера Оригнал, а 200 означает масштабирование до 200% исходного размера.</span><span class="sxs-lookup"><span data-stu-id="b62b3-623">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="b62b3-624">Требования</span><span class="sxs-lookup"><span data-stu-id="b62b3-624">Requirements</span></span>



| <span data-ttu-id="b62b3-625">Требование</span><span class="sxs-lookup"><span data-stu-id="b62b3-625">Requirement</span></span> | <span data-ttu-id="b62b3-626">Значение</span><span class="sxs-lookup"><span data-stu-id="b62b3-626">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b62b3-627">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b62b3-627">Minimum supported client</span></span><br/> | <span data-ttu-id="b62b3-628">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b62b3-628">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b62b3-629">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b62b3-629">Minimum supported server</span></span><br/> | <span data-ttu-id="b62b3-630">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b62b3-630">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b62b3-631">Header</span><span class="sxs-lookup"><span data-stu-id="b62b3-631">Header</span></span><br/>                   | <dl> <span data-ttu-id="b62b3-632"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="b62b3-632"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




