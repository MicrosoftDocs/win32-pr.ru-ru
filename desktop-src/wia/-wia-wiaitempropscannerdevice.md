---
description: Аппаратные устройства для получения образа Windows (WIA) имеют значения свойств, которые хранятся в реестре Windows.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Константы свойств устройства сканера (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701586"
---
# <a name="scanner-device-property-constants"></a><span data-ttu-id="595e0-103">Константы свойств устройства сканера</span><span class="sxs-lookup"><span data-stu-id="595e0-103">Scanner Device Property Constants</span></span>

<span data-ttu-id="595e0-104">Аппаратные устройства для получения образа Windows (WIA) имеют значения свойств, которые хранятся в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="595e0-104">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="595e0-105">Дополнительные сведения см. в разделе [**общие константы свойств устройства**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="595e0-105">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span> <span data-ttu-id="595e0-106">Следующие константы свойств устройства со связанными строками относятся к сканерам цифровых изображений.</span><span class="sxs-lookup"><span data-stu-id="595e0-106">The following device property constants, with their associated strings, are specific to digital image scanners.</span></span>

<span data-ttu-id="595e0-107">Префикс "WIA \_ DPS \_ " указывает на свойство устройства для устройств сканера и является соглашением об именовании, используемым в C/C++.</span><span class="sxs-lookup"><span data-stu-id="595e0-107">The prefix "WIA\_DPS\_" indicates a Device Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="595e0-108">Для сценариев эти константы используют префикс "Сканнердевице" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="595e0-108">For scripting purposes these constants use the prefix "ScannerDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="595e0-109">Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="595e0-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="595e0-110">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="595e0-110">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="595e0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <span data-ttu-id="595e0-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>сканнердевицедевицеид</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="595e0-113">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-113">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="595e0-114">Содержит уникальный идентификатор экземпляра функции для устройства сканера веб-служб.</span><span class="sxs-lookup"><span data-stu-id="595e0-114">Contains a unique function instance identifier for a web services scanner device.</span></span> <span data-ttu-id="595e0-115">Этот идентификатор представляет веб-службу на устройстве сканера, с которой взаимодействует мини-драйвер WIA.</span><span class="sxs-lookup"><span data-stu-id="595e0-115">This identifier represents the web service on the scanner device with which the WIA mini-driver is communicating.</span></span> <span data-ttu-id="595e0-116">Никаких предположений о форме этого идентификатора не должно быть.</span><span class="sxs-lookup"><span data-stu-id="595e0-116">No assumptions about the form of this identifier should be made.</span></span> <span data-ttu-id="595e0-117">Мини-драйвер WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-117">The WIA mini-driver creates and maintains this property.</span></span> <br/> <span data-ttu-id="595e0-118">Приложения WIA могут использовать значение WIA_DPS_DEVICE_ID для поиска, используя API обнаружения функций, объект экземпляра функции, представляющий устройство сканера веб-служб, используемое в текущем сеансе WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="595e0-118">WIA applications can use the value of WIA_DPS_DEVICE_ID to find, using the Function Discovery API, the function instance object representing the web services scanner device used in the current WIA 2.0 session.</span></span><br/> <span data-ttu-id="595e0-119">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-119">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <span data-ttu-id="595e0-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="595e0-121">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="595e0-121">Reserved, do not use.</span></span><br/> <span data-ttu-id="595e0-122">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-122">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <span data-ttu-id="595e0-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="595e0-124">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="595e0-124">Reserved, do not use.</span></span><br/> <span data-ttu-id="595e0-125">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-125">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <span data-ttu-id="595e0-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>сканнердевицедокуменсандлингкапабилитиес</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="595e0-127">Содержит возможности сканера.</span><span class="sxs-lookup"><span data-stu-id="595e0-127">Contains the capabilities of the scanner.</span></span> <span data-ttu-id="595e0-128">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-128">The minidriver creates and maintains this property.</span></span> <br/> <span data-ttu-id="595e0-129">Приложение считывает это свойство, чтобы определить, есть ли у сканера планшетный, веб-устройство подачи документов или установленный дуплекс.</span><span class="sxs-lookup"><span data-stu-id="595e0-129">An application reads this property to determine whether the scanner has a flatbed, document feeder, or duplexer installed.</span></span> <span data-ttu-id="595e0-130">Это свойство также используется для дальнейшего определения установленных компонентов.</span><span class="sxs-lookup"><span data-stu-id="595e0-130">This property is also used to further define the installed features.</span></span><br/> <span data-ttu-id="595e0-131">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-131">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="595e0-132">В следующей таблице описаны константы, допустимые только в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="595e0-132">The following table describes the constants that are valid with Windows 7 only.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-133">Флаги</span><span class="sxs-lookup"><span data-stu-id="595e0-133">Flags</span></span></th>
<th><span data-ttu-id="595e0-134">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-135">AUTO_SOURCE</span><span class="sxs-lookup"><span data-stu-id="595e0-135">AUTO_SOURCE</span></span></td>
<td><span data-ttu-id="595e0-136">В сканере установлен автоматический обработчик документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-136">The scanner has an automatic document handler installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="595e0-137">В следующей таблице описаны константы, допустимые только в Windows 7 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="595e0-137">The following table describes the constants that are valid with Windows 7 and Windows Vista only.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-138">Флаги</span><span class="sxs-lookup"><span data-stu-id="595e0-138">Flags</span></span></th>
<th><span data-ttu-id="595e0-139">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-140">ADVANCED_DUP</span><span class="sxs-lookup"><span data-stu-id="595e0-140">ADVANCED_DUP</span></span></td>
<td><span data-ttu-id="595e0-141">Устройство поддерживает расширенную конфигурацию дуплексного сканирования.</span><span class="sxs-lookup"><span data-stu-id="595e0-141">The device supports advanced duplex scan configuration.</span></span> <span data-ttu-id="595e0-142">Используйте WIA_IPS_DUPLEX_SETTINGS, чтобы переключаться между использованием базовой и расширенной дуплексных конфигураций.</span><span class="sxs-lookup"><span data-stu-id="595e0-142">Use WIA_IPS_DUPLEX_SETTINGS to switch between using basic and advanced duplex configurations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-143">DETECT_FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="595e0-143">DETECT_FILM_TPA</span></span></td>
<td><span data-ttu-id="595e0-144">Сканер может определить, когда адаптер прозрачности или пленки готов к сканированию.</span><span class="sxs-lookup"><span data-stu-id="595e0-144">The scanner can detect when the transparency/film adapter is ready to scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-145">DETECT_STOR</span><span class="sxs-lookup"><span data-stu-id="595e0-145">DETECT_STOR</span></span></td>
<td><span data-ttu-id="595e0-146">Средство проверки может обнаруживать наличие документов во внутреннем хранилище.</span><span class="sxs-lookup"><span data-stu-id="595e0-146">The scanner can detect when there are documents in the internal storage.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-147">FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="595e0-147">FILM_TPA</span></span></td>
<td><span data-ttu-id="595e0-148">Сканер оснащен адаптером сканирования прозрачности или пленки.</span><span class="sxs-lookup"><span data-stu-id="595e0-148">The scanner is equipped with a transparency/film scanning adapter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-149">стор</span><span class="sxs-lookup"><span data-stu-id="595e0-149">STOR</span></span></td>
<td><span data-ttu-id="595e0-150">Сканер оснащен внутренним устройством хранения изображений.</span><span class="sxs-lookup"><span data-stu-id="595e0-150">The scanner is equipped with an internal image storage device.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="595e0-151">В следующей таблице описаны константы, допустимые в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-151">The following table describes the constants that are valid with Windows XP or later.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-152">Флаги</span><span class="sxs-lookup"><span data-stu-id="595e0-152">Flags</span></span></th>
<th><span data-ttu-id="595e0-153">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-154">DETECT_FEED</span><span class="sxs-lookup"><span data-stu-id="595e0-154">DETECT_FEED</span></span></td>
<td><span data-ttu-id="595e0-155">Средство проверки может обнаружить документ в веб-канале.</span><span class="sxs-lookup"><span data-stu-id="595e0-155">The scanner can detect a document in the feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-156">DETECT_FLAT</span><span class="sxs-lookup"><span data-stu-id="595e0-156">DETECT_FLAT</span></span></td>
<td><span data-ttu-id="595e0-157">Сканер может обнаружить документ на планшетном Платен.</span><span class="sxs-lookup"><span data-stu-id="595e0-157">The scanner can detect a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-158">DETECT_SCAN</span><span class="sxs-lookup"><span data-stu-id="595e0-158">DETECT_SCAN</span></span></td>
<td><span data-ttu-id="595e0-159">Средство проверки может обнаружить документ в веб-канале только при сканировании.</span><span class="sxs-lookup"><span data-stu-id="595e0-159">The scanner can detect a document in the feeder only by scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-160">DUP</span><span class="sxs-lookup"><span data-stu-id="595e0-160">DUP</span></span></td>
<td><span data-ttu-id="595e0-161">Сканер имеет дуплексный модуль.</span><span class="sxs-lookup"><span data-stu-id="595e0-161">The scanner has a duplexer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-162">КАНАЛ</span><span class="sxs-lookup"><span data-stu-id="595e0-162">FEED</span></span></td>
<td><span data-ttu-id="595e0-163">В сканере установлен автоматический обработчик документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-163">The scanner has an automatic document handler installed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-164">ВЫПУКЛАЯ</span><span class="sxs-lookup"><span data-stu-id="595e0-164">FLAT</span></span></td>
<td><span data-ttu-id="595e0-165">Сканер имеет планшетный Платен.</span><span class="sxs-lookup"><span data-stu-id="595e0-165">The scanner has a flatbed platen.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="595e0-166">В следующей таблице описаны константы, допустимые только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="595e0-166">The following table describes the constants that are valid with Windows XP only.</span></span> <span data-ttu-id="595e0-167">Эти значения являются устаревшими для Windows 7 и Windows Vista и не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="595e0-167">These values have been deprecated for Windows 7 and Windows Vista and should not be used.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-168">Флаги</span><span class="sxs-lookup"><span data-stu-id="595e0-168">Flags</span></span></th>
<th><span data-ttu-id="595e0-169">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-170">DETECT_DUP</span><span class="sxs-lookup"><span data-stu-id="595e0-170">DETECT_DUP</span></span></td>
<td><span data-ttu-id="595e0-171">Сканер может обнаружить запрос на дуплексное сканирование от пользователя.</span><span class="sxs-lookup"><span data-stu-id="595e0-171">The scanner can detect a duplex scan request from the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-172">DETECT_DUP_AVAIL</span><span class="sxs-lookup"><span data-stu-id="595e0-172">DETECT_DUP_AVAIL</span></span></td>
<td><span data-ttu-id="595e0-173">Сканер может определить, когда был установлен дуплекс.</span><span class="sxs-lookup"><span data-stu-id="595e0-173">The scanner can tell when the duplexer is installed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-174">DETECT_FEED_AVAIL</span><span class="sxs-lookup"><span data-stu-id="595e0-174">DETECT_FEED_AVAIL</span></span></td>
<td><span data-ttu-id="595e0-175">Сканер может определить, когда установлен автоматический веб-канал документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-175">The scanner can tell when the automatic document feeder is installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <span data-ttu-id="595e0-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>сканнердевицедокуменсандлингселект</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-177">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-177">This property is not supported in Windows Vista and later.</span></span> <span data-ttu-id="595e0-178">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-178">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-179">Содержит текущий источник и режим получения сканера. Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-179">Contains the current scanner acquisition source and mode.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-180">Приложение считывает это свойство, чтобы определить текущий источник получения сканера или записать это свойство, чтобы задать источник и режим сканера.</span><span class="sxs-lookup"><span data-stu-id="595e0-180">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="595e0-181">Кроме того, приложения используют это свойство для включения и отключения функции дуплексного режима.</span><span class="sxs-lookup"><span data-stu-id="595e0-181">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="595e0-182">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="595e0-182">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="595e0-183">В следующей таблице содержится десять констант, допустимых для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="595e0-183">The following table has the ten constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-184">Флаги</span><span class="sxs-lookup"><span data-stu-id="595e0-184">Flags</span></span></th>
<th><span data-ttu-id="595e0-185">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-186">ФЕЙЕРВЕРК</span><span class="sxs-lookup"><span data-stu-id="595e0-186">FEEDER</span></span></td>
<td><span data-ttu-id="595e0-187">Сканирование с помощью устройства подачи документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-187">Scan using the document feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-188">СТЕКЛО</span><span class="sxs-lookup"><span data-stu-id="595e0-188">FLATBED</span></span></td>
<td><span data-ttu-id="595e0-189">Сканирование с помощью планшета.</span><span class="sxs-lookup"><span data-stu-id="595e0-189">Scan using the flatbed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-190">УСТРОЙСТВА</span><span class="sxs-lookup"><span data-stu-id="595e0-190">DUPLEX</span></span></td>
<td><span data-ttu-id="595e0-191">Сканирование с помощью операций дуплексного устройства.</span><span class="sxs-lookup"><span data-stu-id="595e0-191">Scan using duplexer operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-192">AUTO_ADVANCE</span><span class="sxs-lookup"><span data-stu-id="595e0-192">AUTO_ADVANCE</span></span></td>
<td><span data-ttu-id="595e0-193">Включает автоматическое подача следующего документа после проверки.</span><span class="sxs-lookup"><span data-stu-id="595e0-193">Enables automatic feeding of the next document after a scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-194">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="595e0-194">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="595e0-195">Сначала просканируйте передний план документа.</span><span class="sxs-lookup"><span data-stu-id="595e0-195">Scan the front of the document first.</span></span> <span data-ttu-id="595e0-196">Это значение допустимо, если задан дуплекс.</span><span class="sxs-lookup"><span data-stu-id="595e0-196">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-197">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="595e0-197">BACK_FIRST</span></span></td>
<td><span data-ttu-id="595e0-198">Сначала просканируйте задний план документа.</span><span class="sxs-lookup"><span data-stu-id="595e0-198">Scan the back of the document first.</span></span> <span data-ttu-id="595e0-199">Это значение допустимо, если задан дуплекс.</span><span class="sxs-lookup"><span data-stu-id="595e0-199">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-200">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="595e0-200">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="595e0-201">Сканирование только на передней панели.</span><span class="sxs-lookup"><span data-stu-id="595e0-201">Scan the front only.</span></span> <span data-ttu-id="595e0-202">Это значение допустимо, если задан дуплекс.</span><span class="sxs-lookup"><span data-stu-id="595e0-202">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-203">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="595e0-203">BACK_ONLY</span></span></td>
<td><span data-ttu-id="595e0-204">Проверка только обратного просмотра.</span><span class="sxs-lookup"><span data-stu-id="595e0-204">Scan the back only.</span></span> <span data-ttu-id="595e0-205">Это значение допустимо, если задан дуплекс.</span><span class="sxs-lookup"><span data-stu-id="595e0-205">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-206">NEXT_PAGE</span><span class="sxs-lookup"><span data-stu-id="595e0-206">NEXT_PAGE</span></span></td>
<td><span data-ttu-id="595e0-207">Сканирование следующей страницы документа.</span><span class="sxs-lookup"><span data-stu-id="595e0-207">Scan the next page of the document.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-208">Предподача</span><span class="sxs-lookup"><span data-stu-id="595e0-208">PREFEED</span></span></td>
<td><span data-ttu-id="595e0-209">Включить режим предварительного перевода.</span><span class="sxs-lookup"><span data-stu-id="595e0-209">Enable pre-feed mode.</span></span> <span data-ttu-id="595e0-210">Предварительное размещение следующего документа во время сканирования.</span><span class="sxs-lookup"><span data-stu-id="595e0-210">Pre-position next document while scanning.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <span data-ttu-id="595e0-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>сканнердевицедокуменсандлингстатус</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="595e0-212">Содержит текущее состояние установленного сканера, устройства подачи документов или дуплексного устройства.</span><span class="sxs-lookup"><span data-stu-id="595e0-212">Contains current state of the scanner's installed flatbed, document feeder, or duplexer.</span></span> <span data-ttu-id="595e0-213">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-213">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-214">Приложение считывает это свойство, чтобы определить, готово ли устройство сканера к использованию.</span><span class="sxs-lookup"><span data-stu-id="595e0-214">An application reads this property to determine whether the scanner device is ready to be used.</span></span> <span data-ttu-id="595e0-215">Это идеальный способ проверить, находится ли бумага в податчике перед получением изображения.</span><span class="sxs-lookup"><span data-stu-id="595e0-215">This is an ideal way to check whether paper is in the feeder prior to acquiring an image.</span></span></p>
<p><span data-ttu-id="595e0-216">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-216">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-217">В следующей таблице приведены константы, допустимые для этого свойства. Звездочка \* означает, что флаг не поддерживается в Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="595e0-217">The following table has the constants that are valid with this property.An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="595e0-218">Символ <strong>V</strong> означает, что флаг поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-218">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-219">Флаги</span><span class="sxs-lookup"><span data-stu-id="595e0-219">Flags</span></span></th>
<th><span data-ttu-id="595e0-220">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-220">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-221">FEED_READY</span><span class="sxs-lookup"><span data-stu-id="595e0-221">FEED_READY</span></span></td>
<td><span data-ttu-id="595e0-222">Планшетный объект готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="595e0-222">The flatbed is ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-223">FLAT_READY</span><span class="sxs-lookup"><span data-stu-id="595e0-223">FLAT_READY</span></span></td>
<td><span data-ttu-id="595e0-224">Сканер содержит документ на планшетном Платен.</span><span class="sxs-lookup"><span data-stu-id="595e0-224">The scanner has a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-225">DUP_READY</span><span class="sxs-lookup"><span data-stu-id="595e0-225">DUP_READY</span></span></td>
<td><span data-ttu-id="595e0-226">Дуплексный модуль включен и готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="595e0-226">The duplexer is enabled and ready to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-227">FLAT_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="595e0-227">FLAT_COVER_UP</span></span></td>
<td><span data-ttu-id="595e0-228">Плоский испытательный картон.</span><span class="sxs-lookup"><span data-stu-id="595e0-228">The flat bed cover is up.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-229">PATH_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="595e0-229">PATH_COVER_UP</span></span></td>
<td><span data-ttu-id="595e0-230">Путь к документу охватывается и препятствует правильной работе.</span><span class="sxs-lookup"><span data-stu-id="595e0-230">The paper path is covered up and is preventing proper operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-231">PAPER_JAM</span><span class="sxs-lookup"><span data-stu-id="595e0-231">PAPER_JAM</span></span></td>
<td><span data-ttu-id="595e0-232">Документ застрял в податчике документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-232">A document is jammed in the document feeder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-233">FILM_TPA_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-233">FILM_TPA_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="595e0-234">Адаптер прозрачности установлен и готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="595e0-234">The transparency adapter is installed and ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-235">STORAGE_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-235">STORAGE_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="595e0-236">Внутреннее запоминающее устройство готово.</span><span class="sxs-lookup"><span data-stu-id="595e0-236">The internal storage device is ready.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-237">STORAGE_FULL<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-237">STORAGE_FULL<strong>V</strong></span></span></td>
<td><span data-ttu-id="595e0-238">Хранилище заполнено, операции отправки невозможно.</span><span class="sxs-lookup"><span data-stu-id="595e0-238">The storage is full, no upload operations possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-239">MULTIPLE_FEED<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-239">MULTIPLE_FEED<strong>V</strong></span></span></td>
<td><span data-ttu-id="595e0-240">Произошло условие множественного веб-канала (обычно с PAPER_JAM).</span><span class="sxs-lookup"><span data-stu-id="595e0-240">A multiple feed condition occurred (usually with a PAPER_JAM).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-241">DEVICE_ATTENTION<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-241">DEVICE_ATTENTION<strong>V</strong></span></span></td>
<td><span data-ttu-id="595e0-242">Ошибка, требующая вмешательства пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="595e0-242">There is an error that requires user intervention on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-243">LAMP_ERR<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-243">LAMP_ERR<strong>V</strong></span></span></td>
<td><span data-ttu-id="595e0-244">Сканер не готов из-за проблемы лампы.</span><span class="sxs-lookup"><span data-stu-id="595e0-244">The scanner is not ready due to a lamp problem.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <span data-ttu-id="595e0-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>сканнердевицеендорсерчарактерс</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="595e0-246">Содержит все допустимые символы, которые приложение может использовать для создания допустимых строк подтверждения.</span><span class="sxs-lookup"><span data-stu-id="595e0-246">Contains all the valid characters that an application can use to create valid endorser strings.</span></span> <span data-ttu-id="595e0-247">Заверение — это принтер, установленный на сканере, который печатает текстовое сообщение на каждой сканируемой странице.</span><span class="sxs-lookup"><span data-stu-id="595e0-247">An endorser is a printer installed on a scanner that imprints a text message on every page scanned.</span></span> <span data-ttu-id="595e0-248">Минидривер должен проверять значение свойства <strong>WIA_DPS_ENDORSER_STRING</strong> по отношению к допустимой кодировке в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="595e0-248">The minidriver should validate the setting of the <strong>WIA_DPS_ENDORSER_STRING</strong> property against the valid character set in this property.</span></span> <span data-ttu-id="595e0-249">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-249">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-250">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-250">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <span data-ttu-id="595e0-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>сканнердевицеендорсерстринг</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="595e0-252">Содержит строку, которая должна быть одобрена (иными словами, напечатана) на каждой странице, которую минидривер просматривает.</span><span class="sxs-lookup"><span data-stu-id="595e0-252">Contains a string that is to be endorsed (in other words, printed) on each page that the minidriver scans.</span></span> <span data-ttu-id="595e0-253">Приложение задает это свойство, используя допустимую кодировку, сообщаемую в свойстве <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> .</span><span class="sxs-lookup"><span data-stu-id="595e0-253">An application sets this property using the valid character set that is reported in the <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> property.</span></span> <span data-ttu-id="595e0-254">Минидривер должен заменять документы только в том случае, если в этом свойстве задана строка.</span><span class="sxs-lookup"><span data-stu-id="595e0-254">The minidriver should endorse documents only if a string is set in this property.</span></span> <span data-ttu-id="595e0-255">Пустая строка означает, что функция подтверждения отключена.</span><span class="sxs-lookup"><span data-stu-id="595e0-255">An empty string means that the endorser functionality is disabled.</span></span></p>
<p><span data-ttu-id="595e0-256">Так как это обязанность драйвера для интерпретации строки подтверждения, драйвер может использовать специальные символы в <strong>WIA_DPS_ENDORSER_STRING</strong>.</span><span class="sxs-lookup"><span data-stu-id="595e0-256">Because it is the driver's responsibility to interpret the endorser string, your driver can use special characters in <strong>WIA_DPS_ENDORSER_STRING</strong>.</span></span> <span data-ttu-id="595e0-257">Однако эти символы будут понятны только вашим приложениям.</span><span class="sxs-lookup"><span data-stu-id="595e0-257">However, only your applications would understand these characters.</span></span></p>
<p><span data-ttu-id="595e0-258">Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-258">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-259">Драйвер, поддерживающий свойство <strong>WIA_DPS_ENDORSER_STRING</strong> , должен поддерживать следующий список токенов.</span><span class="sxs-lookup"><span data-stu-id="595e0-259">A driver supporting the <strong>WIA_DPS_ENDORSER_STRING</strong> property must support the following list of tokens.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-260">Токен</span><span class="sxs-lookup"><span data-stu-id="595e0-260">Token</span></span></th>
<th><span data-ttu-id="595e0-261">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-262">$DATE $</span><span class="sxs-lookup"><span data-stu-id="595e0-262">$DATE$</span></span></td>
<td><span data-ttu-id="595e0-263">Дата в формате гггг/мм/дд.</span><span class="sxs-lookup"><span data-stu-id="595e0-263">The date in the form YYYY/MM/DD.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-264">$DAY $</span><span class="sxs-lookup"><span data-stu-id="595e0-264">$DAY$</span></span></td>
<td><span data-ttu-id="595e0-265">День в формате DD.</span><span class="sxs-lookup"><span data-stu-id="595e0-265">The day in the form DD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-266">$MONTH $</span><span class="sxs-lookup"><span data-stu-id="595e0-266">$MONTH$</span></span></td>
<td><span data-ttu-id="595e0-267">Месяц года в формате MM.</span><span class="sxs-lookup"><span data-stu-id="595e0-267">The month of the year in the form MM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-268">$PAGE _COUNT $</span><span class="sxs-lookup"><span data-stu-id="595e0-268">$PAGE_COUNT$</span></span></td>
<td><span data-ttu-id="595e0-269">Число передаваемых страниц.</span><span class="sxs-lookup"><span data-stu-id="595e0-269">The number of pages transferred.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-270">$TIME $</span><span class="sxs-lookup"><span data-stu-id="595e0-270">$TIME$</span></span></td>
<td><span data-ttu-id="595e0-271">Время суток в формате чч: мм: СС.</span><span class="sxs-lookup"><span data-stu-id="595e0-271">The time of day in the form HH:MM:SS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-272">$YEAR $</span><span class="sxs-lookup"><span data-stu-id="595e0-272">$YEAR$</span></span></td>
<td><span data-ttu-id="595e0-273">Год в формате гггг.</span><span class="sxs-lookup"><span data-stu-id="595e0-273">The year in the form YYYY.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <span data-ttu-id="595e0-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="595e0-275">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="595e0-275">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="595e0-276">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <span data-ttu-id="595e0-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>сканнердевицеглобалидентити</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-278">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-278">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-279">Содержит адрес SOAP устройства со сканером веб-служб.</span><span class="sxs-lookup"><span data-stu-id="595e0-279">Contains the SOAP address of a web services scanner device.</span></span> <span data-ttu-id="595e0-280">Мини-драйвер WIA 2,0 создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-280">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-281">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-281">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <span data-ttu-id="595e0-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>сканнердевицехоризонталбедрегистратион</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-283">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-283">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-284">Содержит регистрацию или выравнивание по горизонтали для документов, размещенных на планшете.</span><span class="sxs-lookup"><span data-stu-id="595e0-284">Contains the registration, or horizontal alignment, for documents placed on the flatbed.</span></span> <span data-ttu-id="595e0-285">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-285">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-286">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-286">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-287">В следующей таблице приведены три константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="595e0-287">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-288">Константа</span><span class="sxs-lookup"><span data-stu-id="595e0-288">Constant</span></span></th>
<th><span data-ttu-id="595e0-289">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-289">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-290">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="595e0-290">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="595e0-291">Документ выравнивается по левому краю.</span><span class="sxs-lookup"><span data-stu-id="595e0-291">The paper is left justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-292">ПО центру</span><span class="sxs-lookup"><span data-stu-id="595e0-292">CENTERED</span></span></td>
<td><span data-ttu-id="595e0-293">Документ выравнивается по центру.</span><span class="sxs-lookup"><span data-stu-id="595e0-293">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-294">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="595e0-294">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="595e0-295">Документ выровнен по правому краю.</span><span class="sxs-lookup"><span data-stu-id="595e0-295">The paper is right justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="595e0-296"><strong>См. также:</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-296"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="595e0-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <span data-ttu-id="595e0-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>сканнердевицехоризонталбедсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-299">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-299">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="595e0-300">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-300">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-301">Задает максимальную ширину (в тысячах) дюйма, которая сканируется по горизонтальной оси (X) от Платен сканера в текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="595e0-301">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="595e0-302">Это свойство также применяется к автоматическим податчикам документов, которые перемещают листы в Платен сканера для сканирования.</span><span class="sxs-lookup"><span data-stu-id="595e0-302">This property also applies to automatic document feeders that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="595e0-303">Это свойство является обязательным для сканеров, имеющих Платен.</span><span class="sxs-lookup"><span data-stu-id="595e0-303">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="595e0-304">Для других типов сканера вместо этого будет реализовано свойство <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="595e0-304">Other scanner types will instead implement the <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="595e0-305">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-305">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="595e0-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>сканнердевицехоризонталшитфидсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-307">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-307">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="595e0-308">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-308">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-309">Задает максимальную ширину в тысячах дюйма, которая просматривается на горизонтальной оси (X) при текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="595e0-309">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="595e0-310">Это свойство также применяется к автоматическим податчикам документов, которые просматриваются без перемещения листов в Платен сканера для планшетов.</span><span class="sxs-lookup"><span data-stu-id="595e0-310">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="595e0-311">Это свойство является обязательным для сканеров подачи листов, прокрутки и ручной проверки.</span><span class="sxs-lookup"><span data-stu-id="595e0-311">This property is mandatory for sheet-fed, scroll-fed, and hand-held scanners.</span></span></p>
<p><span data-ttu-id="595e0-312">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <span data-ttu-id="595e0-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>сканнердевицемаксскантиме</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="595e0-314">Содержит максимальное время сканирования одной страницы с текущими настройками свойств (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="595e0-314">Contains the maximum time to scan a single page with the current property settings, in milliseconds.</span></span> <span data-ttu-id="595e0-315">Приложение считывает это свойство, чтобы оценить время, которое займет сканирование страницы.</span><span class="sxs-lookup"><span data-stu-id="595e0-315">An application reads this property to estimate the time it will take to scan a page.</span></span> <span data-ttu-id="595e0-316">Это полезно при определении условий устройства, которое перестало отвечать.</span><span class="sxs-lookup"><span data-stu-id="595e0-316">This is helpful when determining the conditions of a device that has stopped responding.</span></span> <span data-ttu-id="595e0-317">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-317">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="595e0-318">Это свойство является обязательным для всех сканеров.</span><span class="sxs-lookup"><span data-stu-id="595e0-318">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="595e0-319">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-319">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="595e0-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>сканнердевицеминхоризонталшитфидсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-321">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-321">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="595e0-322">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-322">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-323">Содержит физические горизонтальные размеры наименьшей страницы, которую может сканировать устройство подачи документов сканера, в тысячах дюйма.</span><span class="sxs-lookup"><span data-stu-id="595e0-323">Contains the physical horizontal dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="595e0-324">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-324">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-325">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-325">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-326"><strong>См. также:</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-326"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="595e0-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="595e0-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>сканнердевицеминвертикалшитфидсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-329">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-329">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="595e0-330">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-330">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-331">Содержит физические вертикальные размеры наименьшей страницы, которую может сканировать устройство подачи документов сканера, в тысячах дюйма.</span><span class="sxs-lookup"><span data-stu-id="595e0-331">Contains the physical vertical dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="595e0-332">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-332">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-333">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-333">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-334"><strong>См. также:</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-334"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="595e0-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <span data-ttu-id="595e0-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>сканнердевицеоптикалксрес</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-337">Это свойство не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="595e0-337">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="595e0-338">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-338">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-339">Горизонтальное разрешение оптического экрана.</span><span class="sxs-lookup"><span data-stu-id="595e0-339">Horizontal Optical Resolution.</span></span> <span data-ttu-id="595e0-340">Самое высокое поддерживаемое оптическое разрешение по горизонтали в DPI.</span><span class="sxs-lookup"><span data-stu-id="595e0-340">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="595e0-341">Это свойство имеет одно значение.</span><span class="sxs-lookup"><span data-stu-id="595e0-341">This property is a single value.</span></span> <span data-ttu-id="595e0-342">Это не список всех разрешений, которые могут быть созданы устройством.</span><span class="sxs-lookup"><span data-stu-id="595e0-342">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="595e0-343">Вместо этого это разрешение оптики устройства.</span><span class="sxs-lookup"><span data-stu-id="595e0-343">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="595e0-344">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-344">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="595e0-345">Это свойство является обязательным для всех сканеров.</span><span class="sxs-lookup"><span data-stu-id="595e0-345">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="595e0-346">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-346">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <span data-ttu-id="595e0-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>сканнердевицеоптикалирес</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-348">Это свойство не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="595e0-348">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="595e0-349">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-349">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-350">Вертикальное оптическое разрешение.</span><span class="sxs-lookup"><span data-stu-id="595e0-350">Vertical Optical Resolution.</span></span> <span data-ttu-id="595e0-351">Максимальное поддерживаемое вертикальное оптическое разрешение в DPI.</span><span class="sxs-lookup"><span data-stu-id="595e0-351">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="595e0-352">Это свойство имеет одно значение.</span><span class="sxs-lookup"><span data-stu-id="595e0-352">This property is a single value.</span></span> <span data-ttu-id="595e0-353">Это не список всех разрешений, создаваемых устройством.</span><span class="sxs-lookup"><span data-stu-id="595e0-353">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="595e0-354">Вместо этого это разрешение оптики устройства.</span><span class="sxs-lookup"><span data-stu-id="595e0-354">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="595e0-355">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-355">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="595e0-356">Это свойство является обязательным для всех сканеров.</span><span class="sxs-lookup"><span data-stu-id="595e0-356">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="595e0-357">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-357">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <span data-ttu-id="595e0-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>сканнердевицеориентатион</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="595e0-359">Содержит текущую настройку ориентации. Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-359">Contains the current orientation setting.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-360">Приложение задает свойство <strong>WIA_DPS_ORIENTATION</strong> , чтобы определить исходную ориентацию страницы или изображения, которые должны быть получены.</span><span class="sxs-lookup"><span data-stu-id="595e0-360">An application sets the <strong>WIA_DPS_ORIENTATION</strong> property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="595e0-361">Сведения об использовании WIA_DPS_ORIENTATION см. в разделе <strong>WIA_DPS_PAGE_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-361">For information on how to use WIA_DPS_ORIENTATION, see <strong>WIA_DPS_PAGE_SIZE</strong></span></span></p>
<p><span data-ttu-id="595e0-362">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="595e0-362">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="595e0-363">В следующей таблице приведены четыре константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="595e0-363">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-364">Значение</span><span class="sxs-lookup"><span data-stu-id="595e0-364">Value</span></span></th>
<th><span data-ttu-id="595e0-365">дефинатион</span><span class="sxs-lookup"><span data-stu-id="595e0-365">Defination</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-366">СВЕРХУ</span><span class="sxs-lookup"><span data-stu-id="595e0-366">LANDSCAPE</span></span></td>
<td><span data-ttu-id="595e0-367">коэффициент в 90 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</span><span class="sxs-lookup"><span data-stu-id="595e0-367">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-368">КНИЖНОЙ ориентации</span><span class="sxs-lookup"><span data-stu-id="595e0-368">PORTRAIT</span></span></td>
<td><span data-ttu-id="595e0-369">0 градусов.</span><span class="sxs-lookup"><span data-stu-id="595e0-369">0 degrees.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-370">ROT180</span><span class="sxs-lookup"><span data-stu-id="595e0-370">ROT180</span></span></td>
<td><span data-ttu-id="595e0-371">коэффициент в 180 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</span><span class="sxs-lookup"><span data-stu-id="595e0-371">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-372">ROT270</span><span class="sxs-lookup"><span data-stu-id="595e0-372">ROT270</span></span></td>
<td><span data-ttu-id="595e0-373">коэффициент в 270 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</span><span class="sxs-lookup"><span data-stu-id="595e0-373">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="595e0-374"><strong>См. также:</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-374"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="595e0-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="595e0-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <span data-ttu-id="595e0-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>сканнердевицепадколор</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="595e0-377">Цвет, используемый для заполнения при недостаточном объеме данных изображения, чтобы заполнить запрошенный буфер.</span><span class="sxs-lookup"><span data-stu-id="595e0-377">Color used to pad when there is not enough image data to fill a requested buffer.</span></span> <span data-ttu-id="595e0-378">Это свойство реализуется для сканеров, которые заполняют буфер.</span><span class="sxs-lookup"><span data-stu-id="595e0-378">This property is implemented for scanners that pad the buffer.</span></span> <span data-ttu-id="595e0-379">Это свойство является необязательным для всех сканеров.</span><span class="sxs-lookup"><span data-stu-id="595e0-379">This property is optional for all scanners.</span></span> <span data-ttu-id="595e0-380">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-380">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-381">Тип: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-381">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-382">Формат сведений о цвете — <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">ргбкуад</a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-382">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <span data-ttu-id="595e0-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>сканнердевицепажехеигхт</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-384">Это свойство не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="595e0-384">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="595e0-385">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-385">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-386">Содержит высоту (в тысячах дюйма) текущей выбранной страницы.</span><span class="sxs-lookup"><span data-stu-id="595e0-386">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="595e0-387">Минидривер создает и поддерживает свойство <strong>WIA_DPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="595e0-387">The minidriver creates and maintains the <strong>WIA_DPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="595e0-388">Приложение считывает это свойство, чтобы определить физические размеры сканируемой страницы.</span><span class="sxs-lookup"><span data-stu-id="595e0-388">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="595e0-389">Если параметры экстента отличаются от размеров известных страниц, это свойство сообщает высоту страницы, для которой свойство <strong>WIA_DPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM (которое является значением свойства <strong>WIA_DPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="595e0-389">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_DPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="595e0-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> должны быть синхронизированы с <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, которая сообщает высоту сканируемой страницы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="595e0-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> must be in sync with <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="595e0-391">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <span data-ttu-id="595e0-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>сканнердевицепажесизе</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-393">Это свойство не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="595e0-393">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="595e0-394">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-394">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-395">Содержит размер страницы, которая в настоящий момент выбрана для сканирования.</span><span class="sxs-lookup"><span data-stu-id="595e0-395">Contains the size of the page that is currently selected to be scanned.</span></span> <span data-ttu-id="595e0-396">Чтобы выбрать размеры сканируемой страницы, приложение задает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-396">To select the dimensions of the page to scan, an application sets this property.</span></span> <span data-ttu-id="595e0-397">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-397">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-398">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="595e0-398">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="595e0-399">В следующей таблице приведены три константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="595e0-399">The following table has the three constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-400">Значение</span><span class="sxs-lookup"><span data-stu-id="595e0-400">Value</span></span></th>
<th><span data-ttu-id="595e0-401">Определение</span><span class="sxs-lookup"><span data-stu-id="595e0-401">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-402">WIA_PAGE_A4</span><span class="sxs-lookup"><span data-stu-id="595e0-402">WIA_PAGE_A4</span></span></td>
<td><span data-ttu-id="595e0-403">8267 X 11692 (КНИЖная ориентация)</span><span class="sxs-lookup"><span data-stu-id="595e0-403">8267 X 11692 (PORTRAIT orientation)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-404">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="595e0-404">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="595e0-405">Определяется значениями свойств <strong>WIA_DPS_PAGE_HEIGHT</strong> и <strong>WIA_DPS_PAGE_WIDTH</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-405">Defined by the values of the <strong>WIA_DPS_PAGE_HEIGHT</strong> and <strong>WIA_DPS_PAGE_WIDTH</strong> properties</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-406">WIA_PAGE_LETTER</span><span class="sxs-lookup"><span data-stu-id="595e0-406">WIA_PAGE_LETTER</span></span></td>
<td><span data-ttu-id="595e0-407">8500 X 11000 (КНИЖная ориентация)</span><span class="sxs-lookup"><span data-stu-id="595e0-407">8500 X 11000 (PORTRAIT orientation)</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="595e0-408">Значение свойства <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> определяет ориентацию текущей выбранной страницы.</span><span class="sxs-lookup"><span data-stu-id="595e0-408">The value of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="595e0-409">Свойства <strong>WIA_DPS_PAGE_WIDTH</strong> и <strong>WIA_DPS_PAGE_HEIGHT</strong> сообщают о размерах страницы в тысячах дюйма.</span><span class="sxs-lookup"><span data-stu-id="595e0-409">The <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="595e0-410">Обратите внимание, что эти свойства должны быть согласованы с <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong>, которые содержат размеры страницы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="595e0-410">Note that these properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span> <span data-ttu-id="595e0-411">Допустимые значения типа WIA_PROP_LIST должны зависеть от допустимых настроек свойства <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="595e0-411">Valid values of type WIA_PROP_LIST should depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="595e0-412">Если устройство не может сканировать документы, ориентированные на альбомную ориентацию, с параметром WIA_PAGE_A4, WIA_PAGE_A4 не должны отображаться в списке допустимых значений для свойства <strong>WIA_DPS_PAGE_SIZE</strong> , если <strong>WIA_IPS_ORIENTATION</strong> имеет значение ланскапе.</span><span class="sxs-lookup"><span data-stu-id="595e0-412">If the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 should not appear in the list of valid values for the <strong>WIA_DPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANSCAPE.</span></span></p>
<p><span data-ttu-id="595e0-413">Если приложение устанавливает <strong>WIA_DPS_PAGE_SIZE</strong> любое значение, отличное от WIA_PAGE_CUSTOM, минидривер должен изменить значения <strong>WIA_DPS_PAGE_WIDTH</strong> и <strong>WIA_DPS_PAGE_HEIGHT</strong> на размеры страницы в тысячах дюйма.</span><span class="sxs-lookup"><span data-stu-id="595e0-413">If an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to any value other than WIA_PAGE_CUSTOM, the minidriver should adjust the values of <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="595e0-414">Он также должен скорректировать значения <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> и <strong>WIA_IPS_YEXTENT</strong> к размерам страницы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="595e0-414">It should also adjust the values of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="595e0-415">Если параметр экстента (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> или <strong>WIA_IPS_YEXTENT</strong>) изменяется на значение, не совпадающее с текущим параметром размера страницы, минидривер должен изменить значение свойства <strong>WIA_DPS_PAGE_SIZE</strong> на WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="595e0-415">If an extent setting (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page-size setting, the minidriver should change the value of the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="595e0-416">Минидривер также должен изменить <strong>WIA_DPS_PAGE_WIDTH</strong> или <strong>WIA_DPS_PAGE_HEIGHT</strong> в соответствии с новым параметром экстента.</span><span class="sxs-lookup"><span data-stu-id="595e0-416">The minidriver should also modify <strong>WIA_DPS_PAGE_WIDTH</strong> or <strong>WIA_DPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="595e0-417">Если для <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> задано значение ланскапе, то параметры экстента будут &quot; отражены. &quot; Например, если приложение задает <strong>WIA_DPS_PAGE_SIZE</strong> для WIA_PAGE_A4, минидривер должен установить для параметра <strong>WIA_DPS_PAGE_WIDTH</strong> значение 11692, а для <strong>WIA_DPS_PAGE_HEIGHT</strong> — 8267.</span><span class="sxs-lookup"><span data-stu-id="595e0-417">If <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> is set to LANSCAPE, the extent settings will be &quot;flipped.&quot; For example, if an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver should set <strong>WIA_DPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_DPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="595e0-418">(Минидривер также должен задавать <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong> соответственно.) Обратите внимание, что если <strong>WIA_DPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM, Настройка ориентации не используется для определения размеров сканируемой страницы.</span><span class="sxs-lookup"><span data-stu-id="595e0-418">(The minidriver should also set <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.) Note that if <strong>WIA_DPS_PAGE_SIZE</strong> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span></p>
<p><span data-ttu-id="595e0-419">Минидривер отвечает за обеспечение соответствия свойства <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> с текущей областью выбора.</span><span class="sxs-lookup"><span data-stu-id="595e0-419">The minidriver is responsible for ensuring that the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property is in agreement with the current selection area.</span></span> <span data-ttu-id="595e0-420">Если приложение изменяет значение <strong>WIA_IPS_ORIENTATION</strong> на другое, недопустимое для текущего выбранного размера страницы, минидривер должен изменить значение <strong>WIA_DPS_PAGE_SIZE</strong> на размер страницы, поддерживаемый новым значением ориентации.</span><span class="sxs-lookup"><span data-stu-id="595e0-420">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_DPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="595e0-421">Если приложение задает для свойства <strong>WIA_DPS_PAGE_SIZE</strong> значение WIA_PAGE_CUSTOM, то область текущего выбора не изменяется.</span><span class="sxs-lookup"><span data-stu-id="595e0-421">If an application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="595e0-422">WIA минидривер должен получить текущий макет изображения, начиная с текущих параметров свойств <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> и <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="595e0-422">The WIA minidriver should obtain the current image layout, starting from the current settings of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="595e0-423">Если параметр размера страницы приводит к выделению области выделения, находящегося за пределами испытательного сканера, минидривер должен автоматически скорректировать значения <strong>WIA_IPS_XPOS</strong> и <strong>WIA_IPS_YPOS</strong> свойства на допустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="595e0-423">If the page-size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="595e0-424">Если свойства <strong>WIA_DPS_PAGE_SIZE</strong> и <strong>WIA_IPS_ORIENTATION</strong> задаются одновременно и являются недопустимыми при их применении в сочетании, минидривер не должен возвращать параметры приложения, возвращая ошибку в <a href="https://msdn.microsoft.com/library/ms794145.aspx">ивиаминидрв::d рввалидатеитемпропертиес</a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-424">If the <strong>WIA_DPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span> <span data-ttu-id="595e0-425">.</span><span class="sxs-lookup"><span data-stu-id="595e0-425">.</span></span></p>
<p><span data-ttu-id="595e0-426">В следующих четырех примерах показаны различные сценарии <strong>WIA_DPS_PAGE_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="595e0-426">The following four examples show different <strong>WIA_DPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="595e0-427">Драйвер сообщает о параметрах.</span><span class="sxs-lookup"><span data-stu-id="595e0-427">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="595e0-428">Приложение задает для свойства <strong>WIA_DPS_PAGE_SIZE</strong> значение WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="595e0-428">An application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="595e0-429">Приложение задает для свойства <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> значение ланскапе.</span><span class="sxs-lookup"><span data-stu-id="595e0-429">An application sets the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property to LANSCAPE.</span></span></li>
<li><span data-ttu-id="595e0-430">Приложение изменяет свойство <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> на меньшее значение.</span><span class="sxs-lookup"><span data-stu-id="595e0-430">An application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="595e0-431"><strong>Пример 1. минидривер сообщает о параметрах</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-431"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="595e0-432">В следующем примере минидривер задает настраиваемую область выбора до того, как приложение установит все свойства WIA.</span><span class="sxs-lookup"><span data-stu-id="595e0-432">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="595e0-433">В этом случае область выбора представляет все стекло.</span><span class="sxs-lookup"><span data-stu-id="595e0-433">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
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
<p><span data-ttu-id="595e0-434"><strong>Пример 2. приложение задает</strong> <strong></strong><strong>для свойства</strong> WIA_DPS_PAGE_SIZE значение WIA_PAGE_LETTER  </span><span class="sxs-lookup"><span data-stu-id="595e0-434"><strong>Example 2: An application sets the</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
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
<p><span data-ttu-id="595e0-435"><strong>Пример 3. приложение задает</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>для свойства</strong> WIA_IPS_ORIENTATION значение ланскапе  </span><span class="sxs-lookup"><span data-stu-id="595e0-435"><strong>Example 3: An application sets the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>property to LANSCAPE</strong></span></span></p>
<p><span data-ttu-id="595e0-436">Физическая среда должна иметь возможность получить страницу, которая изначально была в альбомной ориентации.</span><span class="sxs-lookup"><span data-stu-id="595e0-436">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<p><span data-ttu-id="595e0-437"><strong>Пример 4. приложение изменяет</strong> свойство <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>на меньшее значение</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-437"><strong>Example 4: An application changes the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="595e0-438">В следующем примере приложение изменяет свойство <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> на 1000.</span><span class="sxs-lookup"><span data-stu-id="595e0-438">In the following example, an application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to 1000.</span></span> <span data-ttu-id="595e0-439">Минидривер должен предположить, что новое значение, содержащееся в <strong>WIA_IPS_XEXTENT</strong> , больше не является допустимым для свойства <strong>WIA_DPS_PAGE_SIZE</strong> и, таким образом, изменит <strong>WIA_DPS_PAGE_SIZE</strong> на WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="595e0-439">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_DPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="595e0-440">Минидривер также должен корректировать <strong>WIA_DPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="595e0-440">The minidriver must also adjust <strong>WIA_DPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <span data-ttu-id="595e0-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>сканнердевицепажевидс</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-442">Это свойство не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="595e0-442">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="595e0-443">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-443">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-444">Содержит ширину текущей выбранной страницы в тысячах дюйма.</span><span class="sxs-lookup"><span data-stu-id="595e0-444">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="595e0-445">Приложение считывает это свойство, чтобы определить физические размеры сканируемой страницы.</span><span class="sxs-lookup"><span data-stu-id="595e0-445">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="595e0-446">Если параметры экстента отличаются от размеров известных страниц, это свойство сообщает ширину страницы, для которой свойство <strong>WIA_DPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="595e0-446">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="595e0-447"><strong>WIA_DPS_PAGE_WIDTH</strong> должны быть синхронизированы со значением <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, которое показывает ширину сканируемой страницы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="595e0-447"><strong>WIA_DPS_PAGE_WIDTH</strong> must be in sync with the value of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="595e0-448">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-448">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-449">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-449">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <span data-ttu-id="595e0-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>сканнердевицепажес</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-451">Это свойство не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="595e0-451">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="595e0-452">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-452">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-453">Содержит текущее число страниц, получаемых из автоматического устройства подачи документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-453">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="595e0-454">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-454">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-455">Тип: <strong>VT_I4</strong>; Доступ: чтение и запись; Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (от нуля до максимального количества страниц, которое может храниться в податчике документов)</span><span class="sxs-lookup"><span data-stu-id="595e0-455">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero through the maximum number of pages that the document feeder can hold)</span></span></p>
<p><span data-ttu-id="595e0-456">Приложение считывает это свойство для определения емкости страницы устройства подачи документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-456">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="595e0-457">Приложение также задает для этого свойства число страниц, которое он будет сканировать.</span><span class="sxs-lookup"><span data-stu-id="595e0-457">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-458">Если включен дуплексный режим (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> установлен в "Feed" | ДУПЛЕКСная), <strong>WIA_DPS_PAGES</strong> по-прежнему равно числу сканируемых страниц.</span><span class="sxs-lookup"><span data-stu-id="595e0-458">If duplex mode is enabled (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-459">Один лист бумаги автоматически будет содержать две страницы, если ДУПЛЕКСный режим включен, даже если обратная сторона страницы пуста.</span><span class="sxs-lookup"><span data-stu-id="595e0-459">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="595e0-460">Установка <strong>WIA_DPS_PAGES</strong> в значение 1 приводит к тому, что сканер обрабатывает одну из сторон страницы.</span><span class="sxs-lookup"><span data-stu-id="595e0-460">Setting <strong>WIA_DPS_PAGES</strong> to 1 causes a scanner to process one of the sides of the page.</span></span> <span data-ttu-id="595e0-461">Если сканер не может сканировать только одну сторону страницы в режиме дуплекса, <strong>WIA_DPS_PAGES</strong> допустимое значение для элемента Inc в структуре WIA_PROPERTY_INFO необходимо изменить на 2.</span><span class="sxs-lookup"><span data-stu-id="595e0-461">It is recommended that if a scanner is unable to scan only one side of a page while in duplex mode, the <strong>WIA_DPS_PAGES</strong> valid value for the Inc member of the WIA_PROPERTY_INFO structure should be changed to 2.</span></span> <span data-ttu-id="595e0-462">Это значение сигнализирует приложению, что оно должно запрашивать страницы, кратные двум.</span><span class="sxs-lookup"><span data-stu-id="595e0-462">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="595e0-463">Нулевое значение означает, что проверяются <em>все</em> страницы, загруженные в устройство подачи документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-463">A value of zero means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <span data-ttu-id="595e0-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>сканнердевицеплатенколор</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="595e0-465">Задает цвет платена в обратной стороне сканируемой страницы.</span><span class="sxs-lookup"><span data-stu-id="595e0-465">Specifies the color of the platen in back of the sheet to be scanned.</span></span> <span data-ttu-id="595e0-466">Это свойство является необязательным для сканеров, имеющих Платен.</span><span class="sxs-lookup"><span data-stu-id="595e0-466">This property is optional for scanners that have a platen.</span></span> <span data-ttu-id="595e0-467">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-467">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-468">Тип: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-468">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-469">Формат сведений о цвете — <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">ргбкуад</a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-469">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <span data-ttu-id="595e0-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>сканнердевицепревиев</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-471">Это свойство не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="595e0-471">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="595e0-472">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-472">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-473">Указывает режим предварительного просмотра для устройства.</span><span class="sxs-lookup"><span data-stu-id="595e0-473">Indicates the preview mode for a device.</span></span> <span data-ttu-id="595e0-474">Приложение задает это свойство, чтобы перевести устройство в режим предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="595e0-474">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="595e0-475">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="595e0-475">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="595e0-476">В следующей таблице приведены две константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="595e0-476">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-477">Значение</span><span class="sxs-lookup"><span data-stu-id="595e0-477">Value</span></span></th>
<th><span data-ttu-id="595e0-478">Определение</span><span class="sxs-lookup"><span data-stu-id="595e0-478">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-479">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="595e0-479">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="595e0-480">Приложение выполнит окончательную проверку.</span><span class="sxs-lookup"><span data-stu-id="595e0-480">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-481">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="595e0-481">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="595e0-482">Приложение будет выполнять предварительную проверку.</span><span class="sxs-lookup"><span data-stu-id="595e0-482">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <span data-ttu-id="595e0-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>сканнердевицесканахеадпажес</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="595e0-484">Содержит значение, указывающее, будет ли сканер кэшировать страницы в буфере сканера перед их отправкой в приложение.</span><span class="sxs-lookup"><span data-stu-id="595e0-484">Contains a value that indicates whether the scanner will cache pages in a scanner buffer before sending them to the application.</span></span></p>
<p><span data-ttu-id="595e0-485">Нулевое значение отключает сканирование, и страницы не просматриваются заранее.</span><span class="sxs-lookup"><span data-stu-id="595e0-485">A value of zero disables scan ahead and no pages will be scanned ahead.</span></span> <span data-ttu-id="595e0-486">При обычной передаче данных в буферизованный элемент с упреждающим просмотром получает буферизованные страницы.</span><span class="sxs-lookup"><span data-stu-id="595e0-486">Doing normal data transfers on the buffered scan-ahead item retrieves the buffered pages.</span></span> <span data-ttu-id="595e0-487">Свойства WIA не могут быть изменены во время операции предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="595e0-487">WIA properties cannot be changed during a scan-ahead operation.</span></span> <span data-ttu-id="595e0-488">Это необязательное свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-488">This property is optional.</span></span></p>
<p><span data-ttu-id="595e0-489">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> от нуля до максимального количества страниц, которое может храниться в податчике документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-489">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <span data-ttu-id="595e0-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>сканнердевицесканаваилаблеитем</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-491">Это свойство поддерживается только в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-491">This property is supported only by Windows 7 and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-492">Указывает источник входных данных (планшетный, автоматический веб-устройство подачи документов или адаптер сканирования файлов) для сканирования или место хранения, из которого следует передавать данные.</span><span class="sxs-lookup"><span data-stu-id="595e0-492">Indicates the input source (flatbed, automatic document feeder, or fil-scanning adapter) to scan from, or the storage location to transfer data from.</span></span></p>
<p><span data-ttu-id="595e0-493">Событие Scan уведомляет приложение о том, что пользователь инициировал сканирование, но событие не предоставляет имя элемента WIA, представляющего источник входных данных.</span><span class="sxs-lookup"><span data-stu-id="595e0-493">A scan event notifies the application that the user has initiated a scan, but the event does not supply the name of the WIA item that represents the input source.</span></span> <span data-ttu-id="595e0-494">Обработчик событий приложения может запросить свойство WIA_DPS_SCAN_AVAILABLE_ITEM корневого элемента, чтобы получить имя входного элемента источника.</span><span class="sxs-lookup"><span data-stu-id="595e0-494">The application's event handler can query the root item's WIA_DPS_SCAN_AVAILABLE_ITEM property to get the name of the input source item.</span></span></p>
<p><span data-ttu-id="595e0-495">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> от нуля до максимального количества страниц, которое может храниться в податчике документов.</span><span class="sxs-lookup"><span data-stu-id="595e0-495">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <span data-ttu-id="595e0-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>сканнердевицесервицеид</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-497">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-497">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-498">Содержит идентификатор службы сканера веб-служб.</span><span class="sxs-lookup"><span data-stu-id="595e0-498">Contains the Service ID of a Web Services scanner device.</span></span> <span data-ttu-id="595e0-499">Мини-драйвер WIA 2,0 создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-499">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-500">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-500">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <span data-ttu-id="595e0-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>сканнердевицешитфидеррегистратион</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-502">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-502">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="595e0-503">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-503">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-504">Содержит регистрацию, выравнивание и обнаружение краев для документов, размещенных на планшете.</span><span class="sxs-lookup"><span data-stu-id="595e0-504">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="595e0-505">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-505">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="595e0-506">Это свойство указывает, как располагается лист горизонтально в заголовке сканирования карманного компьютера или сканера с листовой подачи.</span><span class="sxs-lookup"><span data-stu-id="595e0-506">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="595e0-507">Свойство используется для прогнозирования места размещения документа по заголовку сканирования.</span><span class="sxs-lookup"><span data-stu-id="595e0-507">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="595e0-508">Для сканеров, поддерживающих несколько заголовков сканирования, это свойство задается относительно самого верхнего заголовка сканирования.</span><span class="sxs-lookup"><span data-stu-id="595e0-508">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="595e0-509">Это свойство является обязательным для сканеров подачи листов, прокрутки и карманных устройств.</span><span class="sxs-lookup"><span data-stu-id="595e0-509">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="595e0-510">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-510">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-511">В следующей таблице приведены три константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="595e0-511">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-512">Константа</span><span class="sxs-lookup"><span data-stu-id="595e0-512">Constant</span></span></th>
<th><span data-ttu-id="595e0-513">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-513">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-514">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="595e0-514">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="595e0-515">Лист располагается слева относительно заголовка сканирования.</span><span class="sxs-lookup"><span data-stu-id="595e0-515">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-516">ПО центру</span><span class="sxs-lookup"><span data-stu-id="595e0-516">CENTERED</span></span></td>
<td><span data-ttu-id="595e0-517">Лист выравнивается по заголовку сканирования.</span><span class="sxs-lookup"><span data-stu-id="595e0-517">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-518">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="595e0-518">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="595e0-519">Лист располагается вправо относительно головного поиска.</span><span class="sxs-lookup"><span data-stu-id="595e0-519">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <span data-ttu-id="595e0-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>сканнердевицешовпревиевконтрол</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-521">Это свойство не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="595e0-521">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="595e0-522">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-522">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-523">Указывает, должен ли элемент отображаться в элементе управления предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="595e0-523">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="595e0-524">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-524">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-525">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-525">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-526">В следующей таблице приведены две константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="595e0-526">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-527">Константа</span><span class="sxs-lookup"><span data-stu-id="595e0-527">Constant</span></span></th>
<th><span data-ttu-id="595e0-528">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-528">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-529">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="595e0-529">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="595e0-530">Отображение элемента управления предварительным просмотром для пользователя, так как это устройство может выполнять предварительную версию.</span><span class="sxs-lookup"><span data-stu-id="595e0-530">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="595e0-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="595e0-532">Не показывать пользователю элемент управления предварительной версии, так как это устройство не может выполнить предварительную версию.</span><span class="sxs-lookup"><span data-stu-id="595e0-532">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <span data-ttu-id="595e0-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>сканнердевицеусернаме</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-534">Это свойство поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-534">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-535">Используется службой WIA для информирования мини-драйвера о имени учетной записи пользователя (включая имя сетевого домена, если применимо) сеанса, в котором выполняется текущее приложение WIA.</span><span class="sxs-lookup"><span data-stu-id="595e0-535">Used by the WIA service to inform the mini-driver about the user account name (including the network domain name when applicable) of the session in which the current WIA application is running.</span></span></p>
<p><span data-ttu-id="595e0-536">Это свойство корневого элемента, управляемое службой WIA.</span><span class="sxs-lookup"><span data-stu-id="595e0-536">This is a root item property, managed by the WIA service.</span></span></p>
<p><span data-ttu-id="595e0-537">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-537">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <span data-ttu-id="595e0-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>сканнердевицевертикалбедрегистратион</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-539">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-539">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-540">Содержит регистрацию или вертикальное выравнивание и обнаружение краев для документов, размещенных на планшете.</span><span class="sxs-lookup"><span data-stu-id="595e0-540">Contains the registration, or vertical alignment and edge detection, for documents placed on the flatbed.</span></span> <span data-ttu-id="595e0-541">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-541">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="595e0-542">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-542">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="595e0-543">В следующей таблице приведены три константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="595e0-543">The following table has the three constants that are valid with this property..</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="595e0-544">Константа</span><span class="sxs-lookup"><span data-stu-id="595e0-544">Constant</span></span></th>
<th><span data-ttu-id="595e0-545">Описание</span><span class="sxs-lookup"><span data-stu-id="595e0-545">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="595e0-546">TOP_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="595e0-546">TOP_JUSTIFIED</span></span></td>
<td><span data-ttu-id="595e0-547">Документ выровнен по верхнему краю.</span><span class="sxs-lookup"><span data-stu-id="595e0-547">The paper is top justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="595e0-548">ПО центру</span><span class="sxs-lookup"><span data-stu-id="595e0-548">CENTERED</span></span></td>
<td><span data-ttu-id="595e0-549">Документ выравнивается по центру.</span><span class="sxs-lookup"><span data-stu-id="595e0-549">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="595e0-550">BOTTOM_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="595e0-550">BOTTOM_JUSTIFIED</span></span></td>
<td><span data-ttu-id="595e0-551">Документ выровнен по нижнему краю.</span><span class="sxs-lookup"><span data-stu-id="595e0-551">The paper is bottom justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="595e0-552"><strong>См. также</strong>.</span><span class="sxs-lookup"><span data-stu-id="595e0-552"><strong>See Also</strong>.</span></span></p>
<p><span data-ttu-id="595e0-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="595e0-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <span data-ttu-id="595e0-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>сканнердевицевертикалбедсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-555">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-555">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="595e0-556">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-556">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-557">Задает максимальную высоту в тысячах дюйма, которая просматривается по вертикальной оси (Y) от Платен сканера для планшетов с текущим разрешением.</span><span class="sxs-lookup"><span data-stu-id="595e0-557">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="595e0-558">Это свойство также применяется к автоматическим податчикам документов, которые перемещают листы в Платен сканера для сканирования.</span><span class="sxs-lookup"><span data-stu-id="595e0-558">This property also applies to automatic document feeders, that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="595e0-559">Это свойство является обязательным для сканеров, имеющих Платен.</span><span class="sxs-lookup"><span data-stu-id="595e0-559">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="595e0-560">Для других типов сканера вместо этого будет реализовано свойство <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="595e0-560">Other scanner types will instead implement the <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="595e0-561">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="595e0-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>сканнердевицевертикалшитфидсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="595e0-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="595e0-563">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="595e0-563">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="595e0-564">Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="595e0-564">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="595e0-565">Задает максимальную высоту в тысячах дюйма, которая просматривается по вертикальной оси (Y) из сканера карманного или электронного канала при текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="595e0-565">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="595e0-566">Это свойство также применяется к автоматическим податчикам документов, которые просматриваются без перемещения листов в Платен сканера для планшетов.</span><span class="sxs-lookup"><span data-stu-id="595e0-566">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="595e0-567">Это свойство является обязательным для сканеров подачи листов.</span><span class="sxs-lookup"><span data-stu-id="595e0-567">This property is mandatory for sheet-fed scanners.</span></span> <span data-ttu-id="595e0-568">Сканеры с прокруткой и ручной поддержкой не должны реализовывать это свойство.</span><span class="sxs-lookup"><span data-stu-id="595e0-568">Scroll-fed and hand-held scanners should not implement this property.</span></span></p>
<p><span data-ttu-id="595e0-569">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="595e0-569">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="595e0-570">Требования</span><span class="sxs-lookup"><span data-stu-id="595e0-570">Requirements</span></span>



| <span data-ttu-id="595e0-571">Требование</span><span class="sxs-lookup"><span data-stu-id="595e0-571">Requirement</span></span> | <span data-ttu-id="595e0-572">Значение</span><span class="sxs-lookup"><span data-stu-id="595e0-572">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="595e0-573">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="595e0-573">Minimum supported client</span></span><br/> | <span data-ttu-id="595e0-574">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="595e0-574">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="595e0-575">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="595e0-575">Minimum supported server</span></span><br/> | <span data-ttu-id="595e0-576">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="595e0-576">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="595e0-577">Header</span><span class="sxs-lookup"><span data-stu-id="595e0-577">Header</span></span><br/>                   | <dl> <span data-ttu-id="595e0-578"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="595e0-578"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
