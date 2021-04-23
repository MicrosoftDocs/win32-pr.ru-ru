---
description: Следующие константы свойств устройств должны поддерживаться всеми интерфейсами интерфейса Ивиаитем, IWiaItem2 и Ивиадрвитем, если в их описаниях не указано иное.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Стандартные константы свойств элементов WIA (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701588"
---
# <a name="common-wia-item-property-constants"></a><span data-ttu-id="64619-103">Стандартные константы свойств элементов WIA</span><span class="sxs-lookup"><span data-stu-id="64619-103">Common WIA Item Property Constants</span></span>

<span data-ttu-id="64619-104">Следующие константы свойств устройств должны поддерживаться всеми интерфейсами интерфейса [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) и [ивиадрвитем](https://msdn.microsoft.com/library/ms793976.aspx) , если в их описаниях не указано иное.</span><span class="sxs-lookup"><span data-stu-id="64619-104">The following device property constants must be supported by all [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) and [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) interfaces unless otherwise noted in their descriptions.</span></span>

<span data-ttu-id="64619-105">Префикс "WIA \_ IPA \_ " указывает свойство элемента для всех устройств и является соглашением об именовании, используемым в C/C++.</span><span class="sxs-lookup"><span data-stu-id="64619-105">The prefix "WIA\_IPA\_" indicates an item property for all devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="64619-106">Для сценариев эти константы используют префикс "Picture" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="64619-106">For scripting purposes these constants use the prefix "Picture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="64619-107">Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="64619-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="64619-108">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="64619-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="64619-109">Описание</span><span class="sxs-lookup"><span data-stu-id="64619-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <span data-ttu-id="64619-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>пиктуреакцессригхтс</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64619-111">Этот флаг управляет доступом к элементу, а также тем, удаляется ли элемент.</span><span class="sxs-lookup"><span data-stu-id="64619-111">This flag controls access to the item as well as whether the item is deleted.</span></span><br/> <span data-ttu-id="64619-112">Требуется для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-112">Required for all WIA 2.0 items.</span></span><br/> <span data-ttu-id="64619-113">Тип: <strong>VT_I4</strong>; Чтение, запись или чтение (только для чтения) в зависимости от способности элемента изменять права доступа; Допустимые значения: WIA_PROP_FLAG</span><span class="sxs-lookup"><span data-stu-id="64619-113">Type: <strong>VT_I4</strong>; Read/Write or Read Only, depending on the item's ability to have its access rights changed; Valid values: WIA_PROP_FLAG</span></span><br/> <span data-ttu-id="64619-114">В следующей таблице приведены пять флагов, допустимых для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="64619-114">The following table has the five flags that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-115">Право доступа</span><span class="sxs-lookup"><span data-stu-id="64619-115">Access Right</span></span></th>
<th><span data-ttu-id="64619-116">Описание</span><span class="sxs-lookup"><span data-stu-id="64619-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-117">WIA_ITEM_READ</span><span class="sxs-lookup"><span data-stu-id="64619-117">WIA_ITEM_READ</span></span></td>
<td><span data-ttu-id="64619-118">Элемент имеет доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="64619-118">Item has read-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-119">WIA_ITEM_WRITE</span><span class="sxs-lookup"><span data-stu-id="64619-119">WIA_ITEM_WRITE</span></span></td>
<td><span data-ttu-id="64619-120">Элемент имеет доступ только на запись.</span><span class="sxs-lookup"><span data-stu-id="64619-120">Item has write-only access.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-121">WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="64619-121">WIA_ITEM_CAN_BE_DELETED</span></span></td>
<td><span data-ttu-id="64619-122">Элемент имеет доступ только на удаление.</span><span class="sxs-lookup"><span data-stu-id="64619-122">Item has delete-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-123">WIA_ITEM_RD</span><span class="sxs-lookup"><span data-stu-id="64619-123">WIA_ITEM_RD</span></span></td>
<td><span data-ttu-id="64619-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="64619-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-125">WIA_ITEM_RWD</span><span class="sxs-lookup"><span data-stu-id="64619-125">WIA_ITEM_RWD</span></span></td>
<td><span data-ttu-id="64619-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="64619-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <span data-ttu-id="64619-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>пиктуреаппколормаппинг</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-128">Это свойство зарезервировано для будущего использования и не реализовано в данный момент.</span><span class="sxs-lookup"><span data-stu-id="64619-128">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="64619-129">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-129">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <span data-ttu-id="64619-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>пиктуребитсперчаннел</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-131">Содержит количество бит на канал для образа.</span><span class="sxs-lookup"><span data-stu-id="64619-131">Contains the number of bits per channel for the image.</span></span> <span data-ttu-id="64619-132">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-132">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-133">Требуется для всех элементов изображений, доступных для получения или сохранения в WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-133">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="64619-134">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-134">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <span data-ttu-id="64619-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>пиктуребуфферсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-136">Содержит размер буфера (в байтах), используемого при переносе данных.</span><span class="sxs-lookup"><span data-stu-id="64619-136">Contains the size of the buffer, in bytes, used during a data transfer.</span></span> <span data-ttu-id="64619-137">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-137">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-138">Приложение может прочитать это свойство, чтобы определить размер буфера, заданный драйвером для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="64619-138">An application can read this property to determine the driver-specified buffer size for data transfers.</span></span> <span data-ttu-id="64619-139">Служба WIA также считывает это свойство для выделения памяти для минидривер во время обмена данными.</span><span class="sxs-lookup"><span data-stu-id="64619-139">The WIA service also reads this property to allocate memory for the minidriver during the data transfer</span></span></p>
<p><span data-ttu-id="64619-140">Необязательно для всех элементов WIA 2,0, поддерживающих перемещение.</span><span class="sxs-lookup"><span data-stu-id="64619-140">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-141">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-141">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="64619-142">Свойство <strong>WIA_IPA_BUFFER_SIZE</strong> содержит минимальный объем данных, которые приложение может запросить в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="64619-142">The <strong>WIA_IPA_BUFFER_SIZE</strong> property contains is the minimum amount of data an application can request at any given time.</span></span> <span data-ttu-id="64619-143">Чем больше размер буфера, тем больше будет запросов к устройству.</span><span class="sxs-lookup"><span data-stu-id="64619-143">The larger the buffer size, the larger the requests to the device will be.</span></span> <span data-ttu-id="64619-144">Это может заставить устройство работать медленнее и не реагировать, может снизить общую производительность системы и может потреблять чрезмерные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="64619-144">This can make the device seem slow and unresponsive, can slow the overall system performance, and can consume excessive resources.</span></span> <span data-ttu-id="64619-145">Слишком малые размеры буфера могут снизить производительность при переносе данных, так как они требуют большого количества небольших запросов.</span><span class="sxs-lookup"><span data-stu-id="64619-145">Buffer sizes that are too small can slow performance of the data transfer by requiring many smaller requests.</span></span> <span data-ttu-id="64619-146">Выберите приемлемый размер буфера, учитывая типичный размер запроса данных на устройстве и балансировку количества запросов по размеру этих запросов.</span><span class="sxs-lookup"><span data-stu-id="64619-146">Choose a reasonable buffer size by considering the typical size of a data request to your device and balancing the number of requests against the size of those requests.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <span data-ttu-id="64619-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>пиктуребитесперлине</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-148">Содержит число байтов в одной строке просмотра изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-148">Contains the number of bytes in one scan line of the image.</span></span> <span data-ttu-id="64619-149">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-149">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-150">Необязательно для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-150">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-151">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-151">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <span data-ttu-id="64619-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>пиктуречаннелсперпиксел</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-153">Содержит число каналов на пиксель для образа.</span><span class="sxs-lookup"><span data-stu-id="64619-153">Contains the number of channels per pixel for the image.</span></span> <span data-ttu-id="64619-154">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-154">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-155">Требуется для всех элементов изображений, доступных для получения или сохранения в WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-155">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="64619-156">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-156">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <span data-ttu-id="64619-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>пиктуреколорпрофиле</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-158">Это свойство зарезервировано для будущего использования и не реализовано в данный момент.</span><span class="sxs-lookup"><span data-stu-id="64619-158">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="64619-159">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-159">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <span data-ttu-id="64619-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>пиктурекомпрессион</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-161">Содержит текущий используемый тип сжатия.</span><span class="sxs-lookup"><span data-stu-id="64619-161">Contains the current compression type used.</span></span> <span data-ttu-id="64619-162">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-162">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-163">Приложение считывает это свойство для определения типа сжатия изображения или задает это свойство для настройки параметра сжатия.</span><span class="sxs-lookup"><span data-stu-id="64619-163">An application reads this property to determine the image compression type or sets this property to configure the compression setting.</span></span></p>
<p><span data-ttu-id="64619-164">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="64619-164">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="64619-165">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="64619-165">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="64619-166">Символ <strong>V</strong> указывает, что константа поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-166">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="64619-167">(Он доступен только через интерфейс <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="64619-167">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-168">Тип сжатия</span><span class="sxs-lookup"><span data-stu-id="64619-168">Compression Type</span></span></th>
<th><span data-ttu-id="64619-169">Описание</span><span class="sxs-lookup"><span data-stu-id="64619-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-170">WIA_COMPRESSION_NONE</span><span class="sxs-lookup"><span data-stu-id="64619-170">WIA_COMPRESSION_NONE</span></span></td>
<td><span data-ttu-id="64619-171">Без сжатия.</span><span class="sxs-lookup"><span data-stu-id="64619-171">No compression.</span></span> <span data-ttu-id="64619-172">Дополнительные сведения см. в разделе <strong>Примечание</strong> .</span><span class="sxs-lookup"><span data-stu-id="64619-172">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-173">WIA_COMPRESSION_AUTO</span><span class="sxs-lookup"><span data-stu-id="64619-173">WIA_COMPRESSION_AUTO</span></span></td>
<td><span data-ttu-id="64619-174">Режим автоматического сжатия.</span><span class="sxs-lookup"><span data-stu-id="64619-174">Automatic compression mode.</span></span> <span data-ttu-id="64619-175">Дополнительные сведения см. в разделе <strong>Примечание</strong> .</span><span class="sxs-lookup"><span data-stu-id="64619-175">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-176">WIA_COMPRESSION_BI_RLE4</span><span class="sxs-lookup"><span data-stu-id="64619-176">WIA_COMPRESSION_BI_RLE4</span></span></td>
<td><span data-ttu-id="64619-177">Сжатие RLE4</span><span class="sxs-lookup"><span data-stu-id="64619-177">RLE4 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-178">WIA_COMPRESSION_BI_RLE8</span><span class="sxs-lookup"><span data-stu-id="64619-178">WIA_COMPRESSION_BI_RLE8</span></span></td>
<td><span data-ttu-id="64619-179">Сжатие RLE8</span><span class="sxs-lookup"><span data-stu-id="64619-179">RLE8 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-180">WIA_COMPRESSION_G3</span><span class="sxs-lookup"><span data-stu-id="64619-180">WIA_COMPRESSION_G3</span></span></td>
<td><span data-ttu-id="64619-181">Сжатие группы 3</span><span class="sxs-lookup"><span data-stu-id="64619-181">Group 3 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-182">WIA_COMPRESSION_G4</span><span class="sxs-lookup"><span data-stu-id="64619-182">WIA_COMPRESSION_G4</span></span></td>
<td><span data-ttu-id="64619-183">Сжатие группы 4</span><span class="sxs-lookup"><span data-stu-id="64619-183">Group 4 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-184">WIA_COMPRESSION_JPEG</span><span class="sxs-lookup"><span data-stu-id="64619-184">WIA_COMPRESSION_JPEG</span></span></td>
<td><span data-ttu-id="64619-185">Сжатие JPEG.</span><span class="sxs-lookup"><span data-stu-id="64619-185">JPEG compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-186">WIA_COMPRESSION_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="64619-186">WIA_COMPRESSION_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="64619-187">Сжатие ЖБИГ.</span><span class="sxs-lookup"><span data-stu-id="64619-187">JBIG compression.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="64619-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span></span></td>
<td><span data-ttu-id="64619-189">Сжатие JPEG 2000.</span><span class="sxs-lookup"><span data-stu-id="64619-189">JPEG 2000 compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-190">WIA_COMPRESSION_PNG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="64619-190">WIA_COMPRESSION_PNG<strong>V</strong></span></span></td>
<td><span data-ttu-id="64619-191">Сжатие PNG.</span><span class="sxs-lookup"><span data-stu-id="64619-191">PNG compression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="64619-192">Если это свойство имеет значение WIA_COMPRESSION_NONE, а WIA_IPA_FORMAT — либо WiaImgFmt_PDFA, либо WiaImgFmt_XPS; затем WIA_COMPRESSION_NONE означает, что режим сжатия не определен, и сканер должен выбрать режим.</span><span class="sxs-lookup"><span data-stu-id="64619-192">When this property is WIA_COMPRESSION_NONE, and WIA_IPA_FORMAT is either WiaImgFmt_PDFA or WiaImgFmt_XPS; then WIA_COMPRESSION_NONE means that the compression mode is undefined and the scanner must decide on a mode.</span></span></p>
<p><span data-ttu-id="64619-193">WIA_COMPRESSION_AUTO — это новое значение свойства, определенное для свойства WIA_IPA_COMPRESSION.</span><span class="sxs-lookup"><span data-stu-id="64619-193">WIA_COMPRESSION_AUTO is a new property value defined for the WIA_IPA_COMPRESSION property.</span></span> <span data-ttu-id="64619-194">Это значение допустимо для всех программируемых элементов источника данных образа, включая планшет и устройство подачи.</span><span class="sxs-lookup"><span data-stu-id="64619-194">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="64619-195">Если это значение поддерживается мини-драйвером WIA, клиент приложения WIA может задать WIA_IPA_COMPRESSION, чтобы включить автоматическое обнаружение режима сжатия на устройстве.</span><span class="sxs-lookup"><span data-stu-id="64619-195">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_COMPRESSION in order to enable automatic compression mode detection at the device.</span></span> <span data-ttu-id="64619-196">WIA_COMPRESSION_AUTO могут работать с и без полного автоцвета (WIA_DATA_AUTO и WIA_DEPTH_AUTO).</span><span class="sxs-lookup"><span data-stu-id="64619-196">WIA_COMPRESSION_AUTO can work with and without full auto-color being supported or enabled (WIA_DATA_AUTO and WIA_DEPTH_AUTO).</span></span></p>
<p><span data-ttu-id="64619-197">WIA_COMPRESSION_AUTO наиболее полезна при переносе форматов файлов, поддерживающих несколько типов данных и битовых глубин, таких как WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="64619-197">WIA_COMPRESSION_AUTO is most useful with transfer file formats that support multiple data types and bit depths, such as WiaImgFmt_RAW.</span></span> <span data-ttu-id="64619-198">Дополнительные сведения о переносе форматов файлов см. в разделе WIA_IPA_FORMAT в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="64619-198">For more information about transfer file formats, see WIA_IPA_FORMAT in this table.</span></span></p>
<p><span data-ttu-id="64619-199">Опитонал поддержка WIA_COMPRESSION_AUTO для мини-драйвера WIA.</span><span class="sxs-lookup"><span data-stu-id="64619-199">It is opitonal for the WIA mini-driver to suport WIA_COMPRESSION_AUTO.</span></span> <span data-ttu-id="64619-200">Если он поддерживается, Мини-драйвер WIA не должен задавать его в качестве значения по умолчанию для WIA_IPA_COMPRESSION; Это значение может быть задано только для приложения WIA.</span><span class="sxs-lookup"><span data-stu-id="64619-200">When it is supported, the WIA mini-driver must never set it as the default value for WIA_IPA_COMPRESSION; only the WIA application can set this value.</span></span></p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <span data-ttu-id="64619-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>пиктуредататипе</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-202">Содержит текущий параметр типа данных для устройства.</span><span class="sxs-lookup"><span data-stu-id="64619-202">Contains the current data type setting for the device.</span></span> <span data-ttu-id="64619-203">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-203">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-204">Приложение считывает это свойство для определения типа данных изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-204">An application reads this property to determine the data type of the image.</span></span> <span data-ttu-id="64619-205">Приложение записывает это свойство, чтобы задать текущий тип данных изображения, которое будет передано.</span><span class="sxs-lookup"><span data-stu-id="64619-205">An application writes this property to set the current data type of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="64619-206">Это свойство является обязательным для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-206">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="64619-207">Он должен быть доступен для чтения и записи для всех элементов с включенным приобретением WIA 2,0 и доступен только для чтения для элементов хранилища WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-207">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="64619-208">Тип: <strong>VT_I4</strong>; Доступ для операционных систем, предшествующих Windows Vista: это свойство доступно только для чтения для камер и чтения и записи для сканеров. Доступ для Windows Vista и более поздних версий: это свойство предназначено только для чтения для WIA_CATEGORY_FOLDER и WIA_CATEGORY_FINISHED_FILE элементов, а для чтения и записи для всех остальных категорий элементов WIA 2,0. Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="64619-208">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: This property is Read Only for cameras and Read/Write for scanners; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="64619-209">Следующая таблица содержит шесть констант, допустимых с параметром, если <strong>WIA_IPA_FORMAT</strong> не имеет значение WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="64619-209">The following table has the six constants that are valid with when <strong>WIA_IPA_FORMAT</strong> is not set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-210">Тип данных</span><span class="sxs-lookup"><span data-stu-id="64619-210">Data Type</span></span></th>
<th><span data-ttu-id="64619-211">Описание</span><span class="sxs-lookup"><span data-stu-id="64619-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-212">WIA_DATA_AUTO</span><span class="sxs-lookup"><span data-stu-id="64619-212">WIA_DATA_AUTO</span></span></td>
<td><span data-ttu-id="64619-213">Допустимы для всех программируемых элементов источника данных образа, включая планшет и устройство подачи.</span><span class="sxs-lookup"><span data-stu-id="64619-213">Valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="64619-214">Если это значение поддерживается мини-драйвером WIA, клиент приложения WIA может задать WIA_IPA_DATATYPE, чтобы включить автоматическое обнаружение цветов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="64619-214">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DATATYPE in order to enable automatic color detection at the device.</span></span> <span data-ttu-id="64619-215">Если задан параметр WIA_DATA_AUTO, Мини-драйвер WIA должен обновить WIA_IPA_DEPTH того же элемента на WIA_DEPTH_AUTO (это значение должно быть поддерживаемым, если устройство поддерживает автоматический цвет).</span><span class="sxs-lookup"><span data-stu-id="64619-215">When WIA_DATA_AUTO is set, the WIA mini-driver must update WIA_IPA_DEPTH on the same item to WIA_DEPTH_AUTO (which must be a supported value if the device supports automatic color).</span></span><br/> <span data-ttu-id="64619-216">Это необязательное значение, но оно требуется, если для WIA_IPA_DEPTH поддерживается WIA_DEPTH_AUTO.</span><span class="sxs-lookup"><span data-stu-id="64619-216">This is an optional value, but it is required when WIA_DEPTH_AUTO is supported for WIA_IPA_DEPTH.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-217">WIA_DATA_COLOR</span><span class="sxs-lookup"><span data-stu-id="64619-217">WIA_DATA_COLOR</span></span></td>
<td><span data-ttu-id="64619-218">Данные сканирования имеют цвет красного, зеленого, синего (RGB).</span><span class="sxs-lookup"><span data-stu-id="64619-218">Scan data is red, green, blue (RGB) color.</span></span> <span data-ttu-id="64619-219">Полный формат цвета описывается с помощью следующих свойств WIA: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span><span class="sxs-lookup"><span data-stu-id="64619-219">The full color format is described using the following WIA properties: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span></span><br/> <span data-ttu-id="64619-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span><span class="sxs-lookup"><span data-stu-id="64619-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span></span><br/> <span data-ttu-id="64619-221"><strong>WIA_IPA_PLANAR</strong></span><span class="sxs-lookup"><span data-stu-id="64619-221"><strong>WIA_IPA_PLANAR</strong></span></span><br/> <span data-ttu-id="64619-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="64619-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span></span><br/> <span data-ttu-id="64619-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="64619-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span></span><br/> <span data-ttu-id="64619-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span><span class="sxs-lookup"><span data-stu-id="64619-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-225">WIA_DATA_COLOR_DITHER</span><span class="sxs-lookup"><span data-stu-id="64619-225">WIA_DATA_COLOR_DITHER</span></span></td>
<td><span data-ttu-id="64619-226">То же, что и WIA_DATA_COLOR за исключением того, что данные отменяются с помощью выбранного шаблона сглаживания.</span><span class="sxs-lookup"><span data-stu-id="64619-226">Same as WIA_DATA_COLOR except that the data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-227">WIA_DATA_COLOR_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="64619-227">WIA_DATA_COLOR_THRESHOLD</span></span></td>
<td><span data-ttu-id="64619-228">То же, что и WIA_DATA_COLOR за исключением того, что при сканировании данных используется пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="64619-228">Same as WIA_DATA_COLOR except that the threshold value is used when scanning the data.</span></span> <span data-ttu-id="64619-229">Значения цвета в <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> значения преобразуются в полную яркость; цвета под этим значением преобразуются в черный.</span><span class="sxs-lookup"><span data-stu-id="64619-229">Color values over the <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> value are converted to full brightness; colors under this value are converted to black.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-230">WIA_DATA_DITHER</span><span class="sxs-lookup"><span data-stu-id="64619-230">WIA_DATA_DITHER</span></span></td>
<td><span data-ttu-id="64619-231">Данные сканирования отменяются с помощью выбранного шаблона сглаживания.</span><span class="sxs-lookup"><span data-stu-id="64619-231">Scan data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-232">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="64619-232">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="64619-233">Данные сканирования представляют интенсивность.</span><span class="sxs-lookup"><span data-stu-id="64619-233">Scan data represents intensity.</span></span> <span data-ttu-id="64619-234">Палитра представляет собой фиксированную серую шкалу с одинаковыми пробелами с глубиной, заданной свойством <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> .</span><span class="sxs-lookup"><span data-stu-id="64619-234">The palette is a fixed, equally-spaced gray scale with a depth specified by <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-235">WIA_DATA_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="64619-235">WIA_DATA_THRESHOLD</span></span></td>
<td><span data-ttu-id="64619-236">Пороговое значение — один бит на пиксель с черно-белыми данными.</span><span class="sxs-lookup"><span data-stu-id="64619-236">The threshold is one bit per pixel of black-and-white data.</span></span> <span data-ttu-id="64619-237">Данные из текущего значения <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> преобразуются в белые; данные с этим значением преобразуются в черный.</span><span class="sxs-lookup"><span data-stu-id="64619-237">Data over the current value of <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> is converted to white; data under this value is converted to black.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="64619-238">Свойство <strong>WIA_IPA_DATATYPE</strong> также используется для описания типа перемещения необработанных данных, который будет использоваться, когда приложение задает WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="64619-238">The <strong>WIA_IPA_DATATYPE</strong> property is also used to describe the type of RAW data transfer to be used when the application sets WiaImgFmt_RAW.</span></span> <span data-ttu-id="64619-239">Драйвер должен задать свойству <strong>WIA_IPA_DATATYPE</strong> список допустимых значений, из которых приложение может выбрать один из них.</span><span class="sxs-lookup"><span data-stu-id="64619-239">The driver should set the <strong>WIA_IPA_DATATYPE</strong> property to a list of allowed values from which the application can pick one.</span></span></p>
<p><span data-ttu-id="64619-240">Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="64619-240">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="64619-241">Проверьте свойство <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> , чтобы определить битовую глубину.</span><span class="sxs-lookup"><span data-stu-id="64619-241">Check the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property to determine the bit depth.</span></span> <span data-ttu-id="64619-242">Это свойство обычно содержит одно значение для камер.</span><span class="sxs-lookup"><span data-stu-id="64619-242">This property usually contains a single value for cameras.</span></span></p>
<p><span data-ttu-id="64619-243">В следующей таблице перечислены константы, допустимые с <strong>WIA_IPA_DATATYPE</strong> , если <strong>WIA_IPA_FORMAT</strong> имеет значение WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="64619-243">The following table lists the constants that are valid with <strong>WIA_IPA_DATATYPE</strong> when <strong>WIA_IPA_FORMAT</strong> is set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-244">Тип данных</span><span class="sxs-lookup"><span data-stu-id="64619-244">Data Type</span></span></th>
<th><span data-ttu-id="64619-245">Описание</span><span class="sxs-lookup"><span data-stu-id="64619-245">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-246">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="64619-246">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="64619-247">Данные сканирования представляют интенсивность.</span><span class="sxs-lookup"><span data-stu-id="64619-247">Scan data represents intensity.</span></span> <span data-ttu-id="64619-248">Палитра представляет собой фиксированные оттенки серого с глубиной, заданной свойством <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> .</span><span class="sxs-lookup"><span data-stu-id="64619-248">The palette is a fixed, equally spaced grayscale with a depth specified by the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span> <span data-ttu-id="64619-249">Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="64619-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-250">WIA_DATA_RAW_BGR</span><span class="sxs-lookup"><span data-stu-id="64619-250">WIA_DATA_RAW_BGR</span></span></td>
<td><span data-ttu-id="64619-251">Данные сканирования находятся в BGR (синий-зеленый-красный) колорспаце.</span><span class="sxs-lookup"><span data-stu-id="64619-251">Scan data is in the BGR (blue-green-red) colorspace.</span></span> <span data-ttu-id="64619-252">Полный формат цвета описывается с помощью Фолловингвиапропертиес: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span><span class="sxs-lookup"><span data-stu-id="64619-252">The full color format is described using the followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span></span><br/> <span data-ttu-id="64619-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span><span class="sxs-lookup"><span data-stu-id="64619-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span></span><br/> <span data-ttu-id="64619-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="64619-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span></span><br/> <span data-ttu-id="64619-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="64619-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span></span><br/> <span data-ttu-id="64619-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span><span class="sxs-lookup"><span data-stu-id="64619-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span></span><br/> <span data-ttu-id="64619-257">Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 3.</span><span class="sxs-lookup"><span data-stu-id="64619-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-258">WIA_DATA_RAW_CMY</span><span class="sxs-lookup"><span data-stu-id="64619-258">WIA_DATA_RAW_CMY</span></span></td>
<td><span data-ttu-id="64619-259">Данные сканирования находятся в голубом/пурпурном цвете (КМИ) колорспаце.</span><span class="sxs-lookup"><span data-stu-id="64619-259">Scan data is in the cyan-magenta-yellow (CMY) colorspace.</span></span> <span data-ttu-id="64619-260">Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="64619-260">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="64619-261">Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 3.</span><span class="sxs-lookup"><span data-stu-id="64619-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-262">WIA_DATA_RAW_CMYK</span><span class="sxs-lookup"><span data-stu-id="64619-262">WIA_DATA_RAW_CMYK</span></span></td>
<td><span data-ttu-id="64619-263">Данные сканирования находятся в цвете голубой-пурпурный-желтый-черный (CMYK) колорспаце.</span><span class="sxs-lookup"><span data-stu-id="64619-263">Scan data is in the cyan-magenta-yellow-black (CMYK) colorspace.</span></span> <span data-ttu-id="64619-264">Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="64619-264">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="64619-265">Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 4.</span><span class="sxs-lookup"><span data-stu-id="64619-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-266">WIA_DATA_RAW_RGB</span><span class="sxs-lookup"><span data-stu-id="64619-266">WIA_DATA_RAW_RGB</span></span></td>
<td><span data-ttu-id="64619-267">Данные сканирования находятся в колорспацее красный-зеленый-синий цвет (RGB).</span><span class="sxs-lookup"><span data-stu-id="64619-267">Scan data is in the red-green-blue (RGB) colorspace.</span></span> <span data-ttu-id="64619-268">Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="64619-268">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="64619-269">Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 3.</span><span class="sxs-lookup"><span data-stu-id="64619-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-270">WIA_DATA_RAW_YUV</span><span class="sxs-lookup"><span data-stu-id="64619-270">WIA_DATA_RAW_YUV</span></span></td>
<td><span data-ttu-id="64619-271">Данные сканирования находятся в цвете «светимость» — «разница» — «Красная разница» (YUV) колорспаце.</span><span class="sxs-lookup"><span data-stu-id="64619-271">Scan data is in the luminance-blue difference-red difference (YUV) colorspace.</span></span> <span data-ttu-id="64619-272">Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="64619-272">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="64619-273">Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 3.</span><span class="sxs-lookup"><span data-stu-id="64619-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-274">WIA_DATA_RAW_YUVK</span><span class="sxs-lookup"><span data-stu-id="64619-274">WIA_DATA_RAW_YUVK</span></span></td>
<td><span data-ttu-id="64619-275">Данные сканирования находятся в цвете «светимость-синий» — «Красная разница» — «черная» (ЮВК) колорспаце.</span><span class="sxs-lookup"><span data-stu-id="64619-275">Scan data is in the luminance-blue difference-red difference-black (YUVK) colorspace.</span></span> <span data-ttu-id="64619-276">Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="64619-276">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="64619-277">Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 4.</span><span class="sxs-lookup"><span data-stu-id="64619-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <span data-ttu-id="64619-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>пиктуредепс</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-279">WIA_IPA_DEPTH содержит значение битовой глубины изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-279">WIA_IPA_DEPTH Contains the bit depth setting of an image.</span></span> <span data-ttu-id="64619-280">Минидривер создает и поддерживает это свойство. Приложение считывает это свойство, чтобы определить битовую глубину изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-280">The minidriver creates and maintains this property.An application reads this property to determine the bit depth setting of the image.</span></span> <span data-ttu-id="64619-281">Приложение может также иметь возможность задать для этого значения нужную глубину.</span><span class="sxs-lookup"><span data-stu-id="64619-281">The application might also be able to set this value to the desired bit depth.</span></span></p>
<p><span data-ttu-id="64619-282">Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="64619-282">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="64619-283">Это свойство является обязательным для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-283">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="64619-284">Он должен быть доступен для чтения и записи для всех элементов с включенным приобретением WIA 2,0 и доступен только для чтения для элементов хранилища WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-284">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="64619-285">Тип: <strong>VT_I4</strong>; Доступ для операционных систем, предшествующих Windows Vista: чтение и запись; Доступ для Windows Vista и более поздних версий: это свойство предназначено только для чтения для WIA_CATEGORY_FOLDER и WIA_CATEGORY_FINISHED_FILE элементов, а для чтения и записи для всех остальных категорий элементов WIA 2,0. Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="64619-285">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: Read/Write; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="64619-286">WIA_DEPTH_AUTO определяется как 0 бит на пиксель, а это новое значение свойства, определенное для WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="64619-286">WIA_DEPTH_AUTO is defined as 0 bits per pixel, and it is a new property value defined for the WIA_IPA_DEPTH.</span></span> <span data-ttu-id="64619-287">Это значение допустимо для всех программируемых элементов источника данных образа, включая планшет и устройство подачи.</span><span class="sxs-lookup"><span data-stu-id="64619-287">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="64619-288">Если WIA_DEPTH_AUTO поддерживается мини-драйвером WIA, клиент приложения WIA может установить WIA_IPA_DEPTH это значение, чтобы включить автоматическое обнаружение цветов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="64619-288">When WIA_DEPTH_AUTO is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DEPTH to this value, to enable automatic color detection at the device.</span></span> <span data-ttu-id="64619-289">Если WIA_DEPTH_AUTO установлен, Мини-драйвер WIA должен обновить WIA_IPA_DATATYPE на том же элементе, чтобы WIA_DATA_AUTO (это значение должно быть поддерживаемым, если устройство поддерживает автоматический цвет).</span><span class="sxs-lookup"><span data-stu-id="64619-289">When WIA_DEPTH_AUTO is set, the WIA mini-driver must update WIA_IPA_DATATYPE on the same item to WIA_DATA_AUTO (which must be a supported value, if the device supports automatic color).</span></span></p>
<p><span data-ttu-id="64619-290">WIA_DEPTH_AUTO является необязательным значением, но оно становится обязательным, если для WIA_IPA_DATATYPE поддерживается WIA_DATA_AUTO.</span><span class="sxs-lookup"><span data-stu-id="64619-290">WIA_DEPTH_AUTO is an optional value, but it becomes required when WIA_DATA_AUTO is supported for WIA_IPA_DATATYPE.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <span data-ttu-id="64619-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>пиктурефиленамикстенсион</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-292">Содержит расширение имени файла для определенного формата файла.</span><span class="sxs-lookup"><span data-stu-id="64619-292">Contains the file name extension for a particular file format.</span></span> <span data-ttu-id="64619-293">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-293">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-294">Необязательно для всех элементов WIA 2,0, поддерживающих перемещение.</span><span class="sxs-lookup"><span data-stu-id="64619-294">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-295">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-295">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="64619-296">Драйвер обновляет это свойство, чтобы отразить текущее значение свойства <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> .</span><span class="sxs-lookup"><span data-stu-id="64619-296">The driver updates this property to reflect the current value of the <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> property.</span></span></p>
<p><span data-ttu-id="64619-297">Например, если <strong>WIA_IPA_FORMAT</strong> WiaImgFmt_JPEG, <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> должен иметь значение <strong>JPG</strong>.</span><span class="sxs-lookup"><span data-stu-id="64619-297">For example, if <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_JPEG, then <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> should be <strong>jpg</strong>.</span></span> <span data-ttu-id="64619-298">Если <strong>WIA_IPA_FORMAT</strong> WiaImgFmt_BMP, то WIA_IPA_FILENAME_EXTENSION должно быть BMP.</span><span class="sxs-lookup"><span data-stu-id="64619-298">If <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_BMP, then WIA_IPA_FILENAME_EXTENSION should be BMP.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="64619-299">Расширение имени файла не включает точку.</span><span class="sxs-lookup"><span data-stu-id="64619-299">The file name extension does not include the dot.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="64619-300">Это свойство рекомендуется использовать для драйверов, которые поддерживают стандартные форматы и необходимы для драйверов, реализующих определенные пользователем форматы.</span><span class="sxs-lookup"><span data-stu-id="64619-300">This property is recommended for drivers that support standard formats and is required for drivers that implement custom-defined formats.</span></span> <span data-ttu-id="64619-301">Он информирует приложение о правильном расширении имени файла для использования во время перемещения файлов в частном формате.</span><span class="sxs-lookup"><span data-stu-id="64619-301">It informs the application of the correct file name extension to use during the transfer of privately formatted files.</span></span> <span data-ttu-id="64619-302">Например, если корпорация A. Datum создала драйвер WIA, который передавал файл в новом формате, компания может указать расширение &quot; ADC &quot; .</span><span class="sxs-lookup"><span data-stu-id="64619-302">For example, if the A. Datum Corporation created a WIA driver that transferred a file in a new format, the company could specify an extension of &quot;adc&quot;.</span></span> <span data-ttu-id="64619-303">Это позволяет приложениям передавать данные в этом формате в файл и создавать имя файла, например <em>MyFile. ADC</em>, которое полезно для других пользователей, которые понимают новое расширение.</span><span class="sxs-lookup"><span data-stu-id="64619-303">This allows applications to transfer data in that format to a file and to create a file name such as <em>myfile.adc</em>,which is useful to others who understand the new extension.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <span data-ttu-id="64619-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>пиктуреформат</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-305">Содержит текущий формат изображения, которое будет передано.</span><span class="sxs-lookup"><span data-stu-id="64619-305">Contains the current format of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="64619-306">Приложение считывает это свойство, чтобы определить формат получаемого изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-306">An application reads this property to determine the format of the image that it is about to receive.</span></span> <span data-ttu-id="64619-307">Приложение записывает это свойство для задания формата.</span><span class="sxs-lookup"><span data-stu-id="64619-307">An application writes this property to set the format.</span></span> <span data-ttu-id="64619-308">Это свойство зависит от свойства <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> .</span><span class="sxs-lookup"><span data-stu-id="64619-308">This property depends on the <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> property.</span></span> <span data-ttu-id="64619-309">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-309">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-310">Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="64619-310">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="64619-311">Тип: <strong>CLSID</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="64619-311">Type: <strong>CLSID</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="64619-312">В следующей таблице перечислены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="64619-312">The following table lists the constants that are valid with this property.</span></span> <span data-ttu-id="64619-313">Звездочка \* указывает, что константа не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="64619-313">The asterisk \* indicates that the constant is not supported in Windows Vista.</span></span> <span data-ttu-id="64619-314">(Он доступен только через интерфейс <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> .) Двойная звездочка \* \* указывает, что константа не поддерживается в Windows Server 2003 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="64619-314">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) The double asterisk \*\* indicates that the constant is not supported in either Windows Server 2003 or Windows Vista.</span></span> <span data-ttu-id="64619-315">Символ <strong>V</strong> указывает, что константа поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-315">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="64619-316">(Он доступен только через интерфейс <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="64619-316">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-317">Формат</span><span class="sxs-lookup"><span data-stu-id="64619-317">Format</span></span></th>
<th><span data-ttu-id="64619-318">Описание</span><span class="sxs-lookup"><span data-stu-id="64619-318">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-319">WiaAudFmt_AIFF</span><span class="sxs-lookup"><span data-stu-id="64619-319">WiaAudFmt_AIFF</span></span></td>
<td><span data-ttu-id="64619-320">Формат аудиозаписей в формате AIFF</span><span class="sxs-lookup"><span data-stu-id="64619-320">AIFF audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-321">WiaAudFmt_MP3</span><span class="sxs-lookup"><span data-stu-id="64619-321">WiaAudFmt_MP3</span></span></td>
<td><span data-ttu-id="64619-322">Формат аудио в формате MP3</span><span class="sxs-lookup"><span data-stu-id="64619-322">MP3 audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-323">WiaAudFmt_WAV</span><span class="sxs-lookup"><span data-stu-id="64619-323">WiaAudFmt_WAV</span></span></td>
<td><span data-ttu-id="64619-324">Звуковой формат WAV</span><span class="sxs-lookup"><span data-stu-id="64619-324">WAV audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-325">WiaAudFmt_WMA</span><span class="sxs-lookup"><span data-stu-id="64619-325">WiaAudFmt_WMA</span></span></td>
<td><span data-ttu-id="64619-326">Аудио формат WMA</span><span class="sxs-lookup"><span data-stu-id="64619-326">WMA audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-327">WiaImgFmt_ASF \* \*</span><span class="sxs-lookup"><span data-stu-id="64619-327">WiaImgFmt_ASF\*\*</span></span></td>
<td><span data-ttu-id="64619-328">Формат видео ASF</span><span class="sxs-lookup"><span data-stu-id="64619-328">ASF video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-329">WiaImgFmt_AVI \* \*</span><span class="sxs-lookup"><span data-stu-id="64619-329">WiaImgFmt_AVI\*\*</span></span></td>
<td><span data-ttu-id="64619-330">Видео в формате AVI</span><span class="sxs-lookup"><span data-stu-id="64619-330">AVI video format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-331">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="64619-331">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="64619-332">Точечный рисунок Windows с файлом заголовка</span><span class="sxs-lookup"><span data-stu-id="64619-332">Windows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-333">WiaImgFmt_CIFF \*</span><span class="sxs-lookup"><span data-stu-id="64619-333">WiaImgFmt_CIFF\*</span></span></td>
<td><span data-ttu-id="64619-334">Формат файла изображения камеры</span><span class="sxs-lookup"><span data-stu-id="64619-334">Camera Image File format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-335">WiaImgFmt_DPOF</span><span class="sxs-lookup"><span data-stu-id="64619-335">WiaImgFmt_DPOF</span></span></td>
<td><span data-ttu-id="64619-336">Формат печати ДПОФ</span><span class="sxs-lookup"><span data-stu-id="64619-336">DPOF printing format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-337">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="64619-337">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="64619-338">Расширенный метафайл Windows</span><span class="sxs-lookup"><span data-stu-id="64619-338">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-339">WiaImgFmt_EXEC</span><span class="sxs-lookup"><span data-stu-id="64619-339">WiaImgFmt_EXEC</span></span></td>
<td><span data-ttu-id="64619-340">Исполняемый файл</span><span class="sxs-lookup"><span data-stu-id="64619-340">Executable file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-341">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="64619-341">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="64619-342">Формат файла Exchange</span><span class="sxs-lookup"><span data-stu-id="64619-342">Exchangeable File Format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-343">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="64619-343">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="64619-344">Формат Флашпикс</span><span class="sxs-lookup"><span data-stu-id="64619-344">FlashPix format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-345">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="64619-345">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="64619-346">Формат изображения GIF</span><span class="sxs-lookup"><span data-stu-id="64619-346">GIF image format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-347">WiaImgFmt_HTML</span><span class="sxs-lookup"><span data-stu-id="64619-347">WiaImgFmt_HTML</span></span></td>
<td><span data-ttu-id="64619-348">Формат HTML</span><span class="sxs-lookup"><span data-stu-id="64619-348">HTML format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-349">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="64619-349">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="64619-350">Формат файла значка Windows</span><span class="sxs-lookup"><span data-stu-id="64619-350">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-351">WiaImgFmt_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="64619-351">WiaImgFmt_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="64619-352">Совместный формат группы экспертов по обработке изображений (ЖБИГ).</span><span class="sxs-lookup"><span data-stu-id="64619-352">The Joint Bi-level Image Experts Group (JBIG) format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-353">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="64619-353">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="64619-354">Сжатый формат JPEG</span><span class="sxs-lookup"><span data-stu-id="64619-354">JPEG compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-355">WiaImgFmt_JPEG2K</span><span class="sxs-lookup"><span data-stu-id="64619-355">WiaImgFmt_JPEG2K</span></span></td>
<td><span data-ttu-id="64619-356">Сжатый формат JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="64619-356">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-357">WiaImgFmt_JPEG2KX</span><span class="sxs-lookup"><span data-stu-id="64619-357">WiaImgFmt_JPEG2KX</span></span></td>
<td><span data-ttu-id="64619-358">Сжатый формат JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="64619-358">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-359">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="64619-359">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="64619-360">Точечный рисунок Windows без файла заголовка</span><span class="sxs-lookup"><span data-stu-id="64619-360">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-361">WiaImgFmt_PDFA<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="64619-361">WiaImgFmt_PDFA<strong>V</strong></span></span></td>
<td><span data-ttu-id="64619-362">Формат PDF/A (ISO/CD 19005-1).</span><span class="sxs-lookup"><span data-stu-id="64619-362">The PDF/A (ISO/CD 19005-1) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-363">WiaImgFmt_MPG \* \*</span><span class="sxs-lookup"><span data-stu-id="64619-363">WiaImgFmt_MPG\*\*</span></span></td>
<td><span data-ttu-id="64619-364">Формат видео MPEG</span><span class="sxs-lookup"><span data-stu-id="64619-364">MPEG video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-365">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="64619-365">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="64619-366">Формат файлов еастман Kodak</span><span class="sxs-lookup"><span data-stu-id="64619-366">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-367">WiaImgFmt_PICT</span><span class="sxs-lookup"><span data-stu-id="64619-367">WiaImgFmt_PICT</span></span></td>
<td><span data-ttu-id="64619-368">Формат файлов Apple</span><span class="sxs-lookup"><span data-stu-id="64619-368">Apple file format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-369">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="64619-369">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="64619-370">Формат W3C PNG</span><span class="sxs-lookup"><span data-stu-id="64619-370">W3C PNG format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-371">WiaImgFmt_RAW</span><span class="sxs-lookup"><span data-stu-id="64619-371">WiaImgFmt_RAW</span></span></td>
<td><span data-ttu-id="64619-372">Формат RAW только для передачи данных</span><span class="sxs-lookup"><span data-stu-id="64619-372">Raw format for data transfers only</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-373">WiaImgFmt_RAWRGB</span><span class="sxs-lookup"><span data-stu-id="64619-373">WiaImgFmt_RAWRGB</span></span></td>
<td><span data-ttu-id="64619-374">Необработанный формат RGB</span><span class="sxs-lookup"><span data-stu-id="64619-374">Raw RGB format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-375">WiaImgFmt_RTF</span><span class="sxs-lookup"><span data-stu-id="64619-375">WiaImgFmt_RTF</span></span></td>
<td><span data-ttu-id="64619-376">Формат форматированного текста</span><span class="sxs-lookup"><span data-stu-id="64619-376">Rich Text File format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-377">WiaImgFmt_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="64619-377">WiaImgFmt_SCRIPT</span></span></td>
<td><span data-ttu-id="64619-378">Файл скрипта</span><span class="sxs-lookup"><span data-stu-id="64619-378">Script file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-379">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="64619-379">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="64619-380">TIFF (Tag Image File Format)</span><span class="sxs-lookup"><span data-stu-id="64619-380">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-381">WiaImgFmt_TXT</span><span class="sxs-lookup"><span data-stu-id="64619-381">WiaImgFmt_TXT</span></span></td>
<td><span data-ttu-id="64619-382">текстовый файл</span><span class="sxs-lookup"><span data-stu-id="64619-382">Text file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-383">WiaImgFmt_UNICODE16</span><span class="sxs-lookup"><span data-stu-id="64619-383">WiaImgFmt_UNICODE16</span></span></td>
<td><span data-ttu-id="64619-384">16-разрядная кодировка Юникода</span><span class="sxs-lookup"><span data-stu-id="64619-384">UNICODE 16-bit encoding</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-385">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="64619-385">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="64619-386">Метафайл Windows</span><span class="sxs-lookup"><span data-stu-id="64619-386">Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-387">WiaImgFmt_XML</span><span class="sxs-lookup"><span data-stu-id="64619-387">WiaImgFmt_XML</span></span></td>
<td><span data-ttu-id="64619-388">XML-файл</span><span class="sxs-lookup"><span data-stu-id="64619-388">XML file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-389">WiaImgFmt_XPS<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="64619-389">WiaImgFmt_XPS<strong>V</strong></span></span></td>
<td><span data-ttu-id="64619-390">Формат пакета XPS</span><span class="sxs-lookup"><span data-stu-id="64619-390">XPS Package format</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="64619-391">Если это свойство имеет значение WiaImgFmt_PDFA или WiaImgFmt_XPS, а WIA_IPA_COMPRESSION — WIA_COMPRESSION_NONE; Второе значение означает, что режим сжатия не определен, и сканер должен выбрать режим.</span><span class="sxs-lookup"><span data-stu-id="64619-391">When this property is either WiaImgFmt_PDFA or WiaImgFmt_XPS, and WIA_IPA_COMPRESSION is WIA_COMPRESSION_NONE; then the latter value means that the compression mode is undefined and the scanner must decide on a mode.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <span data-ttu-id="64619-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>пиктурефуллитемнаме</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-393">Содержит полное имя элемента (имя элемента вместе со сведениями о пути).</span><span class="sxs-lookup"><span data-stu-id="64619-393">Contains the full item name (the item name together with path information).</span></span> <span data-ttu-id="64619-394">Полное имя элемента совпадает с параметром <em>бстрфуллитемнаме</em> функции служебной программы <a href="https://msdn.microsoft.com/library/ms794649.aspx">виаскреатедрвитем</a> Service.</span><span class="sxs-lookup"><span data-stu-id="64619-394">The full item name is the same as the <em>bstrFullItemName</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="64619-395">Приложение считывает это свойство, чтобы определить, какой элемент в настоящий момент используется, и где этот элемент находится в дереве элементов.</span><span class="sxs-lookup"><span data-stu-id="64619-395">An application reads this property to determine which item it is currently using and where that item is located in the item tree.</span></span> <span data-ttu-id="64619-396">Каждый элемент должен иметь уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="64619-396">Each item should have a unique name.</span></span> <span data-ttu-id="64619-397">Приложения обычно используют полное имя элемента для поиска элементов в дереве элементов.</span><span class="sxs-lookup"><span data-stu-id="64619-397">Applications commonly use the full item name to search for items in the item tree.</span></span> <span data-ttu-id="64619-398">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-398">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-399">Требуется для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-399">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-400">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-400">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <span data-ttu-id="64619-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>пиктурегаммакурвес</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-402">Это свойство зарезервировано для будущего использования и в настоящее время не реализовано.</span><span class="sxs-lookup"><span data-stu-id="64619-402">This property is reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="64619-403">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-403">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <span data-ttu-id="64619-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>пиктуреикмпрофиленаме</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-405">Содержит имя профиля ICM, необходимое для правильного декодирования изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-405">Contains the ICM profile name that is needed to properly decode the image.</span></span> <span data-ttu-id="64619-406">Приложение считывает это свойство, чтобы определить профиль ICM, используемый при обработке изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-406">An application reads this property to determine the ICM profile to use when processing the image.</span></span> <span data-ttu-id="64619-407">Служба WIA создает и поддерживает это свойство на основе записи Икмпрофилес в файле установки драйвера.</span><span class="sxs-lookup"><span data-stu-id="64619-407">The WIA service creates and maintains this property based on the ICMProfiles entry in the driver installation file.</span></span></p>
<p><span data-ttu-id="64619-408">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-408">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <span data-ttu-id="64619-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>пиктуреитемкатегори</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-410">Поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-410">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="64619-411">Элементы WIA 2,0 группируются по категориям, которые определяют способ обработки или использования <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="64619-411">WIA 2.0 items are grouped into categories that define how a <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> is to be treated or used.</span></span> <span data-ttu-id="64619-412">Например, если элемент представляет устройство подачи, то приложение должно содержать необходимые свойства устройства подачи документов и действовать как устройство подачи документов.</span><span class="sxs-lookup"><span data-stu-id="64619-412">For example, If the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="64619-413">Если элемент представляет готовый файл, то приложение WIA 2,0 должно обрабатывать его таким образом, предполагая, что данные статичны и расположены на устройстве.</span><span class="sxs-lookup"><span data-stu-id="64619-413">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="64619-414">(Правила для каждого элемента будут определены в отдельных документах спецификации.)</span><span class="sxs-lookup"><span data-stu-id="64619-414">(The rules for each item will be defined in their individual specification documents.)</span></span></p>
<p><span data-ttu-id="64619-415">Требуется для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-415">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-416">Тип: <strong>VT_CLSID</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-wia2-itemcategoryguids.md"><strong>идентификаторы GUID категорий элементов</strong></a></span><span class="sxs-lookup"><span data-stu-id="64619-416">Type: <strong>VT_CLSID</strong>, Access: Read Only, Valid values: <a href="-wia-wia2-itemcategoryguids.md"><strong>Item Category GUIDs</strong></a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <span data-ttu-id="64619-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>пиктуреитемфлагс</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-418">Содержит описательные флаги для элемента WIA.</span><span class="sxs-lookup"><span data-stu-id="64619-418">Contains the descriptive flags for a WIA item.</span></span> <span data-ttu-id="64619-419">Флаги элемента те же, что и в параметре <em>лобжектфлагс</em> функции служебной программы <a href="https://msdn.microsoft.com/library/ms794649.aspx">виаскреатедрвитем</a> Service.</span><span class="sxs-lookup"><span data-stu-id="64619-419">The item flags are the same as those in the <em>lObjectFlags</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="64619-420">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-420">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-421">Приложение считывает это свойство для определения значений флагов элемента.</span><span class="sxs-lookup"><span data-stu-id="64619-421">An application reads this property to determine the item's descriptive flag values.</span></span></p>
<p><span data-ttu-id="64619-422">Тип: <strong>VT_I4</strong> доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-422">Type: <strong>VT_I4</strong> Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="64619-423">В следующей таблице приведены флаги, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="64619-423">The following table has the flags that are valid with this property.</span></span> <span data-ttu-id="64619-424">Звездочка \* означает, что флаг не поддерживается в Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="64619-424">An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="64619-425">(Он доступен только через интерфейс <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> .) Двойная звездочка \* \* означает, что флаг не поддерживается в Windows Server 2003 или Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="64619-425">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) An double asterisk \*\* indicates that the flag is not supported in either Windows Server 2003 or Windows Vista or later.</span></span> <span data-ttu-id="64619-426">Символ <strong>V</strong> означает, что флаг поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-426">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> <span data-ttu-id="64619-427">(Он доступен только через интерфейс <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="64619-427">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-428">Flag</span><span class="sxs-lookup"><span data-stu-id="64619-428">Flag</span></span></th>
<th><span data-ttu-id="64619-429">Определение</span><span class="sxs-lookup"><span data-stu-id="64619-429">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-430">Виаитемтипеанализе \*</span><span class="sxs-lookup"><span data-stu-id="64619-430">WiaItemTypeAnalyze\*</span></span></td>
<td><span data-ttu-id="64619-431">Этот элемент поддерживает метод <strong>ивиаитем:: анализеитем</strong> (описан в документации по Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="64619-431">This item supports the <strong>IWiaItem::AnalyzeItem</strong> method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="64619-432">Этот элемент также поддерживает автоматическое создание дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="64619-432">This item also supports automatic child item generation.</span></span> <span data-ttu-id="64619-433">Эта возможность полезна для обнаружения региона или декомпозиции страниц.</span><span class="sxs-lookup"><span data-stu-id="64619-433">This capability is useful for region detection or page decomposition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-434">виаитемтипеаудио</span><span class="sxs-lookup"><span data-stu-id="64619-434">WiaItemTypeAudio</span></span></td>
<td><span data-ttu-id="64619-435">Этот элемент поддерживает аудио.</span><span class="sxs-lookup"><span data-stu-id="64619-435">This item supports audio.</span></span> <span data-ttu-id="64619-436">Этот флаг допустим только для элементов, для которых также установлен флаг <strong>виаитемтипефиле</strong> .</span><span class="sxs-lookup"><span data-stu-id="64619-436">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-437">Виаитемтипебурст \*</span><span class="sxs-lookup"><span data-stu-id="64619-437">WiaItemTypeBurst\*</span></span></td>
<td><span data-ttu-id="64619-438">Только для папок.</span><span class="sxs-lookup"><span data-stu-id="64619-438">For folders only.</span></span> <span data-ttu-id="64619-439">Этот флаг указывает, что изображения в этой папке были собраны в непрерывной последовательности времени.</span><span class="sxs-lookup"><span data-stu-id="64619-439">This flag indicates that the images in this folder were taken in a continuous time sequence.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-440">виаитемтипеделетед</span><span class="sxs-lookup"><span data-stu-id="64619-440">WiaItemTypeDeleted</span></span></td>
<td><span data-ttu-id="64619-441">Этот элемент помечен для удаления, этот элемент был удален, этот элемент не существует или содержимое этого элемента недопустимо.</span><span class="sxs-lookup"><span data-stu-id="64619-441">This item is marked for deletion, this item has been deleted, this item does not exist, or the contents of this item are invalid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-442">Виаитемтипедокумент<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="64619-442">WiaItemTypeDocument<strong>V</strong></span></span></td>
<td><span data-ttu-id="64619-443">Этот элемент является файлом документа в одном из форматов документов, содержащихся в свойстве <strong>WIA_IPA_FORMAT</strong> .</span><span class="sxs-lookup"><span data-stu-id="64619-443">This item is a document file in one of the document formats that the <strong>WIA_IPA_FORMAT</strong> property contains.</span></span> <span data-ttu-id="64619-444">(Эти форматы включают в себя файлы, не являющиеся изображениями, такие как txt, htm и doc.)</span><span class="sxs-lookup"><span data-stu-id="64619-444">(These formats include those for nonimage files, such as .txt, .htm, and .doc files.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-445">виаитемтипедевице</span><span class="sxs-lookup"><span data-stu-id="64619-445">WiaItemTypeDevice</span></span></td>
<td><span data-ttu-id="64619-446">Этот элемент представляет подключенное устройство.</span><span class="sxs-lookup"><span data-stu-id="64619-446">This item represents a connected device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-447">виаитемтипедисконнектед</span><span class="sxs-lookup"><span data-stu-id="64619-447">WiaItemTypeDisconnected</span></span></td>
<td><span data-ttu-id="64619-448">Этот элемент представляет отключенное устройство.</span><span class="sxs-lookup"><span data-stu-id="64619-448">This item represents a disconnected device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-449">виаитемтипефиле</span><span class="sxs-lookup"><span data-stu-id="64619-449">WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="64619-450">Элемент поддерживает передачу файлов.</span><span class="sxs-lookup"><span data-stu-id="64619-450">The item supports file transfers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-451">виаитемтипефолдер</span><span class="sxs-lookup"><span data-stu-id="64619-451">WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="64619-452">Элемент является папкой.</span><span class="sxs-lookup"><span data-stu-id="64619-452">The item is a folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-453">виаитемтипефри</span><span class="sxs-lookup"><span data-stu-id="64619-453">WiaItemTypeFree</span></span></td>
<td><span data-ttu-id="64619-454">Элемент не инициализирован или был удален.</span><span class="sxs-lookup"><span data-stu-id="64619-454">The item is uninitialized or has been deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-455">виаитемтипеженератед</span><span class="sxs-lookup"><span data-stu-id="64619-455">WiaItemTypeGenerated</span></span></td>
<td><span data-ttu-id="64619-456">Этот элемент был создан приложением или драйвером.</span><span class="sxs-lookup"><span data-stu-id="64619-456">This item has been generated by an application or by the driver.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-457">Виаитемтипехасаттачментс \*</span><span class="sxs-lookup"><span data-stu-id="64619-457">WiaItemTypeHasAttachments\*</span></span></td>
<td><span data-ttu-id="64619-458">Этот элемент поддерживает вложения и в настоящее время содержит вложения.</span><span class="sxs-lookup"><span data-stu-id="64619-458">This item supports attachments and currently contains attachments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-459">Виаитемтипехпанорама \*</span><span class="sxs-lookup"><span data-stu-id="64619-459">WiaItemTypeHPanorama\*</span></span></td>
<td><span data-ttu-id="64619-460">Этот элемент представляет горизонтальный панорамный рисунок.</span><span class="sxs-lookup"><span data-stu-id="64619-460">This item represents a horizontal panoramic image.</span></span> <span data-ttu-id="64619-461">Этот флаг допустим только для элементов, для которых также установлен флаг <strong>виаитемтипефолдер</strong> .</span><span class="sxs-lookup"><span data-stu-id="64619-461">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-462">виаитемтипеимаже</span><span class="sxs-lookup"><span data-stu-id="64619-462">WiaItemTypeImage</span></span></td>
<td><span data-ttu-id="64619-463">Элемент является файлом изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-463">The item is an image file.</span></span> <span data-ttu-id="64619-464">Этот флаг допустим только для элементов, для которых также установлен флаг <strong>виаитемтипефиле</strong> .</span><span class="sxs-lookup"><span data-stu-id="64619-464">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-465">Виаитемтипепрограммабледатасаурце<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="64619-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span></span></td>
<td><span data-ttu-id="64619-466">Элемент является программируемым источником данных и соответствует набору предварительно определенных правил конфигурации, которые основаны на <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span><span class="sxs-lookup"><span data-stu-id="64619-466">The item is a programmable data source and follows a set of predefined configuration rules, which are based on <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-467">Виаитемтиперут<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="64619-467">WiaItemTypeRoot<strong>V</strong></span></span></td>
<td><span data-ttu-id="64619-468">Этот элемент является корневым элементом, который является родительским для всех элементов компонента, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="64619-468">This item is the root item, which is the parent to all the feature items that the device supports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-469">виаитемтипестораже</span><span class="sxs-lookup"><span data-stu-id="64619-469">WiaItemTypeStorage</span></span></td>
<td><span data-ttu-id="64619-470">Этот флаг указывает дополнительное хранилище для элементов папок.</span><span class="sxs-lookup"><span data-stu-id="64619-470">This flag indicates additional storage for folders items.</span></span> <span data-ttu-id="64619-471">Драйверы WIA определяют свои элементы в терминах изображений и папок.</span><span class="sxs-lookup"><span data-stu-id="64619-471">WIA drivers specify their items in terms of images and folders.</span></span> <span data-ttu-id="64619-472">Не существует свойств WIA, описывающих характеристики элемента хранения (например, объем хранилища, скорость записи или тип носителя).</span><span class="sxs-lookup"><span data-stu-id="64619-472">No WIA properties exist that describe the characteristics of a storage item (such as remaining storage space, write speed, or type of media.</span></span> <span data-ttu-id="64619-473">Можно добавить свойства, относящиеся к поставщику, которые предоставляют эту информацию.</span><span class="sxs-lookup"><span data-stu-id="64619-473">Vendor-specific properties that expose this information can be added.</span></span> <span data-ttu-id="64619-474">Эти свойства доступны только для приложений или расширений, написанных для их распознавания.</span><span class="sxs-lookup"><span data-stu-id="64619-474">These properties are accessible only to applications or extensions that are written to recognize them.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-475">виаитемтипетрансфер</span><span class="sxs-lookup"><span data-stu-id="64619-475">WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="64619-476">Этот элемент можно использовать для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="64619-476">This item can be used to transfer data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-477">виаитемтипетваинкапабилитипасссраугх</span><span class="sxs-lookup"><span data-stu-id="64619-477">WiaItemTypeTwainCapabilityPassThrough</span></span></td>
<td><span data-ttu-id="64619-478">Этот тип указывает, что устройство WIA может получать данные о возможности TWAIN на уровне совместимости TWAIN.</span><span class="sxs-lookup"><span data-stu-id="64619-478">This type indicates that the WIA device is able to receive TWAIN capability data from the TWAIN compatibility layer.</span></span> <span data-ttu-id="64619-479">Если этот тип задан, то все возможности TWAIN, не распознаваемые уровнем совместимости TWAIN, передаются в драйвер Севиа.</span><span class="sxs-lookup"><span data-stu-id="64619-479">If this type is set, any TWAIN capability that is not understood by the TWAIN compatibility layer will be passed to theWIA driver.</span></span> <span data-ttu-id="64619-480">Это допустимо только для корневого элемента.</span><span class="sxs-lookup"><span data-stu-id="64619-480">This is valid only for the root item.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-481">Виаитемтипевидео \* \*</span><span class="sxs-lookup"><span data-stu-id="64619-481">WiaItemTypeVideo\*\*</span></span></td>
<td><span data-ttu-id="64619-482">Этот элемент поддерживает потоковую передачу видео.</span><span class="sxs-lookup"><span data-stu-id="64619-482">This item supports streaming video.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-483">Виаитемтипевпанорама \*</span><span class="sxs-lookup"><span data-stu-id="64619-483">WiaItemTypeVPanorama\*</span></span></td>
<td><span data-ttu-id="64619-484">Этот элемент представляет вертикальную панорамную изображение.</span><span class="sxs-lookup"><span data-stu-id="64619-484">This item represents a vertical panoramic image.</span></span> <span data-ttu-id="64619-485">Этот флаг допустим только для элементов, для которых также установлен флаг <strong>виаитемтипефолдер</strong> .</span><span class="sxs-lookup"><span data-stu-id="64619-485">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="64619-486">Некоторые из этих флагов являются обязательными или необязательными для элементов WIA 2,0 в соответствии с категорией элемента, как показано в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="64619-486">Some of these flags are required or optional for WIA 2.0 items, according to the category of the item, as shown in this table.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-487">Категория элемента</span><span class="sxs-lookup"><span data-stu-id="64619-487">Category of Item</span></span></th>
<th><span data-ttu-id="64619-488">Обязательно</span><span class="sxs-lookup"><span data-stu-id="64619-488">Required</span></span></th>
<th><span data-ttu-id="64619-489">Необязательно</span><span class="sxs-lookup"><span data-stu-id="64619-489">Optional</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-490">WIA_CATEGORY_ROOT</span><span class="sxs-lookup"><span data-stu-id="64619-490">WIA_CATEGORY_ROOT</span></span></td>
<td><span data-ttu-id="64619-491">Виаитемтиперут Виаитемтипефолдер</span><span class="sxs-lookup"><span data-stu-id="64619-491">WiaItemTypeRoot WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="64619-492">Виаитемтипедевице Виаитемтипедисконнектед</span><span class="sxs-lookup"><span data-stu-id="64619-492">WiaItemTypeDevice WiaItemTypeDisconnected</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-493">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="64619-493">WIA_CATEGORY_FLATBED</span></span></td>
<td><span data-ttu-id="64619-494">Виаитемтипепрограммабледатасаурце Виаитемтипетрансфер Виаитемтипеимаже Виаитемтипефиле</span><span class="sxs-lookup"><span data-stu-id="64619-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="64619-495">Виаитемтипефолдер (если поддерживается несколько элементов регионов сканирования, этот флаг необязателен только для корневого элемента WIA_CATEGORY_FLATBED.)</span><span class="sxs-lookup"><span data-stu-id="64619-495">WiaItemTypeFolder (If multiple scan regions items are supported, this flag is optional only for the WIA_CATEGORY_FLATBED root item.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span><span class="sxs-lookup"><span data-stu-id="64619-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span></span></td>
<td><span data-ttu-id="64619-497">Виаитемтипепрограммабледатасаурце Виаитемтипетрансфер Виаитемтипеимаже Виаитемтипефиле</span><span class="sxs-lookup"><span data-stu-id="64619-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="64619-498">Виаитемтипефолдер (если имеются WIA_CATEGORY_FEEDER_FRONT и WIA_CATEGORY_FEEDER_BACK элементы, этот флаг является необязательным только для корневого элемента WIA_CATEGORY_FEEDER.)</span><span class="sxs-lookup"><span data-stu-id="64619-498">WiaItemTypeFolder (If WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK items are present, then this flag is optional only for the WIA_CATEGORY_FEEDER root item.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-499">WIA_CATEGORY_FILM (корневой)</span><span class="sxs-lookup"><span data-stu-id="64619-499">WIA_CATEGORY_FILM (root)</span></span></td>
<td><span data-ttu-id="64619-500">Виаитемтипепрограммабледатасаурце Виаитемтипетрансфер Виаитемтипеимаже Виаитемтипефиле WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="64619-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="64619-501">Нет</span><span class="sxs-lookup"><span data-stu-id="64619-501">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-502">WIA_CATEGORY_FILM (дочерние элементы)</span><span class="sxs-lookup"><span data-stu-id="64619-502">WIA_CATEGORY_FILM (children)</span></span></td>
<td><span data-ttu-id="64619-503">Виаитемтипепрограммабледатасаурце Виаитемтипетрансфер Виаитемтипеимаже Виаитемтипефиле</span><span class="sxs-lookup"><span data-stu-id="64619-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="64619-504">Нет</span><span class="sxs-lookup"><span data-stu-id="64619-504">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-505">WIA_CATEGORY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="64619-505">WIA_CATEGORY_FOLDER</span></span></td>
<td><span data-ttu-id="64619-506">Виаитемтипестораже Виаитемтипефолдер</span><span class="sxs-lookup"><span data-stu-id="64619-506">WiaItemTypeStorage WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="64619-507">виаитемтипеделетед</span><span class="sxs-lookup"><span data-stu-id="64619-507">WiaItemTypeDeleted</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-508">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="64619-508">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><span data-ttu-id="64619-509">Виаитемтипефиле Виаитемтипетрансфер</span><span class="sxs-lookup"><span data-stu-id="64619-509">WiaItemTypeFile WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="64619-510">Виаитемтипеимаже Виаитемтипеаудио Виаитемтипеделетед</span><span class="sxs-lookup"><span data-stu-id="64619-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <span data-ttu-id="64619-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>пиктуреитемнаме</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-512">Содержит имя элемента.</span><span class="sxs-lookup"><span data-stu-id="64619-512">Contains the item name.</span></span> <span data-ttu-id="64619-513">Приложение считывает это свойство, чтобы определить, какой элемент в данный момент используется.</span><span class="sxs-lookup"><span data-stu-id="64619-513">An application reads this property to determine which item it is currently using.</span></span> <span data-ttu-id="64619-514">Каждый элемент имеет уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="64619-514">Each item has a unique name.</span></span> <span data-ttu-id="64619-515">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-515">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-516">Требуется для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-516">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-517">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-517">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <span data-ttu-id="64619-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>пиктуреитемсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-519">Содержит текущий размер (в байтах) данных, связанных с элементом.</span><span class="sxs-lookup"><span data-stu-id="64619-519">Contains the current size, in bytes, of the data that is associated with the item.</span></span> <span data-ttu-id="64619-520">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-520">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-521">Содержит общий размер передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="64619-521">Contains is the total size of the data being transferred.</span></span> <span data-ttu-id="64619-522">Если это значение равно нулю, это означает, что минидривер не содержит сведений о точном размере данных.</span><span class="sxs-lookup"><span data-stu-id="64619-522">If this value is zero, it means that the minidriver has no information about the exact size of the data.</span></span> <span data-ttu-id="64619-523">(Это распространено для сжатых данных.) Приложение считывает это значение, чтобы определить размер приобретения перед тем, как оно будет происходить.</span><span class="sxs-lookup"><span data-stu-id="64619-523">(This is common for compressed data.) An application reads this value to determine the size of the acquisition before it takes place.</span></span> <span data-ttu-id="64619-524">Служба WIA считывает это свойство для помощи при выделении памяти для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="64619-524">The WIA service reads this property to assist in allocating memory for data transfers.</span></span> <span data-ttu-id="64619-525">Дополнительные сведения см. в разделе <a href="https://msdn.microsoft.com/library/ms792198.aspx">Передача данных в приложение WIA</a> , если свойство имеет значение 0, а тимед настроен для передачи файла, служба WIA не выделяет память для WIA-минидривер.</span><span class="sxs-lookup"><span data-stu-id="64619-525">For further information, see <a href="https://msdn.microsoft.com/library/ms792198.aspx">Transferring Data to a WIA Application</a> if the property is set to zero and TYMED is configured for a file transfer, the WIA service does not allocate any memory for the WIA minidriver.</span></span></p>
<p><span data-ttu-id="64619-526">Требуется для всех элементов WIA 2,0, поддерживающих перемещение.</span><span class="sxs-lookup"><span data-stu-id="64619-526">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-527">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-527">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <span data-ttu-id="64619-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>пиктуреитемтиме</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-529">Содержит время первоначальной записи образа.</span><span class="sxs-lookup"><span data-stu-id="64619-529">Contains the time that the image was originally captured.</span></span> <span data-ttu-id="64619-530">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-530">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="64619-531">Это свойство должно быть представлено в виде вектора из восьми значений <strong>слов</strong> в виде структуры SYSTEMTIME (описывается в документации по Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="64619-531">This property should be reported as a vector of eight <strong>WORD</strong> values in the form of a SYSTEMTIME structure (described in the Platform SDK documentation).</span></span></p>
<p><span data-ttu-id="64619-532">Необязательно для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-532">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-533">Тип: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> доступ: только для чтения, записи или чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-533">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong> Access: Read/Write or Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="64619-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>пиктуреитемитемссторед</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-535">Поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-535">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="64619-536">Указывает, сколько элементов хранится в элементе WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="64619-536">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="64619-537">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-537">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <span data-ttu-id="64619-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>пиктуреминбуфферсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-539">Указывает минимальный размер буфера, используемого при передаче данных.</span><span class="sxs-lookup"><span data-stu-id="64619-539">Specifies the minimum buffer size that is used in data transfers.</span></span> <span data-ttu-id="64619-540">Если перенос данных выполняется через механизм обратного вызова, значение свойства может быть меньше 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="64619-540">If the data transfer is performed through a callback mechanism, the property value can be as small as 64KB.</span></span> <span data-ttu-id="64619-541">Однако если перемещение выполняется в файл, значение свойства равно количеству байтов, необходимых для одновременного перемещения одной страницы данных.</span><span class="sxs-lookup"><span data-stu-id="64619-541">However, if the transfer is to file, the property value is the number of bytes that are needed to transfer one page of data at a time.</span></span> <span data-ttu-id="64619-542">Минидривер создает и поддерживает это свойство WIA.</span><span class="sxs-lookup"><span data-stu-id="64619-542">The minidriver creates and maintains this WIA property.</span></span></p>
<p><span data-ttu-id="64619-543">Необязательно для всех элементов WIA 2,0, поддерживающих перемещение.</span><span class="sxs-lookup"><span data-stu-id="64619-543">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-544">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-544">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <span data-ttu-id="64619-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>пиктуренумберофлинес</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-546">Содержит число строк, содержащихся в изображении (вертикальная высота изображения в пикселях).</span><span class="sxs-lookup"><span data-stu-id="64619-546">Contains the number of lines contained in the image (the vertical height of the image in pixels).</span></span> <span data-ttu-id="64619-547">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-547">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-548">Необязательно для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-548">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-549">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-549">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <span data-ttu-id="64619-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>пиктурепикселсперлине</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-551">Содержит количество пикселей в каждой строке изображения (ширина изображения в пикселях).</span><span class="sxs-lookup"><span data-stu-id="64619-551">Contains the number of pixels in each line of the image (the width of the image in pixels).</span></span> <span data-ttu-id="64619-552">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-552">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-553">Необязательно для всех элементов WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="64619-553">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-554">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-554">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <span data-ttu-id="64619-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>пиктурепланар</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-556">Это свойство не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-556">This property is not supported in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="64619-557">Содержит параметры упаковки данных изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-557">Contains image data packing options.</span></span> <span data-ttu-id="64619-558">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-558">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-559">Приложение считывает это свойство для определения параметров упаковки изображения или задает параметры упаковки текущего изображения.</span><span class="sxs-lookup"><span data-stu-id="64619-559">An application reads this property to determine the image packing options or sets the current image packing options.</span></span></p>
<p><span data-ttu-id="64619-560">Тип: <strong>VT_I4</strong>; Доступ: чтение и запись; Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="64619-560">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="64619-561">Если для устройства можно задать только одно значение, создайте тип WIA_PROP_LIST и поместите в него допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="64619-561">If the device can be set to only a single value, create a WIA_PROP_LIST type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="64619-562">В следующей таблице приведены две константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="64619-562">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-563">Значение</span><span class="sxs-lookup"><span data-stu-id="64619-563">Value</span></span></th>
<th><span data-ttu-id="64619-564">Определение</span><span class="sxs-lookup"><span data-stu-id="64619-564">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-565">WIA_PACKED_PIXEL</span><span class="sxs-lookup"><span data-stu-id="64619-565">WIA_PACKED_PIXEL</span></span></td>
<td><span data-ttu-id="64619-566">Данные изображения находятся в формате упакованных пикселей.</span><span class="sxs-lookup"><span data-stu-id="64619-566">Image data is in packed-pixel format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-567">WIA_PLANAR</span><span class="sxs-lookup"><span data-stu-id="64619-567">WIA_PLANAR</span></span></td>
<td><span data-ttu-id="64619-568">Данные изображения имеют плоский формат.</span><span class="sxs-lookup"><span data-stu-id="64619-568">Image data is in planar format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <span data-ttu-id="64619-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>пиктурепреферредформат</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-570">Содержит предпочтительный формат для изображений, которые передает этот минидривер.</span><span class="sxs-lookup"><span data-stu-id="64619-570">Contains the preferred format for images that this minidriver transfers.</span></span> <span data-ttu-id="64619-571">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-571">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-572">Требуется для всех элементов WIA 2,0, поддерживающих перемещение.</span><span class="sxs-lookup"><span data-stu-id="64619-572">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-573">Тип: <strong>CLSID</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-573">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <span data-ttu-id="64619-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>пиктурепропстреамкомпатид</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-575">Указывает CLSID, представляющий набор значений свойств устройства.</span><span class="sxs-lookup"><span data-stu-id="64619-575">Specifies a CLSID that represents a set of device property values.</span></span> <span data-ttu-id="64619-576">Если драйвер устройства реализует эту функцию, приложения используют это свойство, чтобы определить, поддерживает ли устройство набор значений.</span><span class="sxs-lookup"><span data-stu-id="64619-576">If a device driver implements this feature, applications use this property to determine if the device supports a set of values.</span></span></p>
<p><span data-ttu-id="64619-577">Тип: <strong>CLSID</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="64619-577">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="64619-578">В следующей таблице приведены 12 констант, допустимых для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="64619-578">The following table has the 12 constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-579">Значение</span><span class="sxs-lookup"><span data-stu-id="64619-579">Value</span></span></th>
<th><span data-ttu-id="64619-580">Определение</span><span class="sxs-lookup"><span data-stu-id="64619-580">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-581">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="64619-581">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="64619-582">Точечный рисунок Микрософтвиндовс с файлом заголовка</span><span class="sxs-lookup"><span data-stu-id="64619-582">MicrosoftWindows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-583">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="64619-583">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="64619-584">Расширенный метафайл Windows</span><span class="sxs-lookup"><span data-stu-id="64619-584">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-585">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="64619-585">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="64619-586">Формат файла Exchange</span><span class="sxs-lookup"><span data-stu-id="64619-586">Exchangeable File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-587">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="64619-587">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="64619-588">Формат Флашпикс</span><span class="sxs-lookup"><span data-stu-id="64619-588">FlashPix format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-589">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="64619-589">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="64619-590">Формат изображения GIF</span><span class="sxs-lookup"><span data-stu-id="64619-590">GIF image format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-591">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="64619-591">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="64619-592">Формат файла значка Windows</span><span class="sxs-lookup"><span data-stu-id="64619-592">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-593">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="64619-593">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="64619-594">Сжатый формат JPEG</span><span class="sxs-lookup"><span data-stu-id="64619-594">JPEG compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-595">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="64619-595">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="64619-596">Формат файлов еастман Kodak</span><span class="sxs-lookup"><span data-stu-id="64619-596">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-597">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="64619-597">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="64619-598">Формат W3C PNG</span><span class="sxs-lookup"><span data-stu-id="64619-598">W3C PNG format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-599">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="64619-599">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="64619-600">Точечный рисунок Windows без файла заголовка</span><span class="sxs-lookup"><span data-stu-id="64619-600">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-601">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="64619-601">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="64619-602">TIFF (Tag Image File Format)</span><span class="sxs-lookup"><span data-stu-id="64619-602">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-603">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="64619-603">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="64619-604">Метафайл Windows</span><span class="sxs-lookup"><span data-stu-id="64619-604">Windows metafile</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <span data-ttu-id="64619-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>пиктуреравбитсперчаннел</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-606">Поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-606">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="64619-607">Содержит количество битов в каждом канале.</span><span class="sxs-lookup"><span data-stu-id="64619-607">Contains the number of bits in each channel.</span></span> <span data-ttu-id="64619-608">Это свойство должно быть представлено в виде вектора, равного количеству БАЙТОВ, так как есть каналы, где первый байт соответствует количеству битов в первом канале, второй байт — к числу битов во втором канале и т. д.</span><span class="sxs-lookup"><span data-stu-id="64619-608">This property should be reported as a vector of as many BYTE values as there are channels, where the first BYTE corresponds to the number of bits in the first channel, the second byte to the number of bits in the second channel and so on.</span></span> <span data-ttu-id="64619-609">Должно быть столько записей, сколько каналов в соответствии с WIA_IPA_CHANNELS_PER_PIXEL.</span><span class="sxs-lookup"><span data-stu-id="64619-609">There need to be as many entries as there are channels according to WIA_IPA_CHANNELS_PER_PIXEL.</span></span> <span data-ttu-id="64619-610">Драйвер задает это свойство, когда приложение переключается на WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="64619-610">The driver sets that property when the application switches to WiaImgFmt_RAW.</span></span> <span data-ttu-id="64619-611">Для хорошо известных подтипов существует столько же записей, сколько указано в таблице в разделе WIA_IPA_RAW_SUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="64619-611">For the well-known subtypes, there are as many entries as listed in the table under WIA_IPA_RAW_SUBTYPE.</span></span></p>
<p><span data-ttu-id="64619-612">Тип: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-612">Type: <strong>VT_UI1</strong>|<strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <span data-ttu-id="64619-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>пиктуререгионтипе</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-614">Это свойство зарезервировано для будущего использования и не реализовано в данный момент.</span><span class="sxs-lookup"><span data-stu-id="64619-614">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="64619-615">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-615">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <span data-ttu-id="64619-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>пиктуресуппресспропертипаже</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-617">Указывает, следует ли подавлять Общие страницы свойств для элементов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="64619-617">Specifies whether to suppress the general property pages for items on the device.</span></span></p>
<p><span data-ttu-id="64619-618">Это свойство доступно в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-618">This property is available on Windows XP and later.</span></span></p>
<p><span data-ttu-id="64619-619">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-619">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="64619-620">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="64619-620">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="64619-621">Звездочка \* указывает, что константа не является допустимой в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-621">The asterisk \* indicates that the constant is not valid with Windows Vista and later.</span></span> <span data-ttu-id="64619-622">(Он доступен только через интерфейс <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="64619-622">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-623">Константа</span><span class="sxs-lookup"><span data-stu-id="64619-623">Constant</span></span></th>
<th><span data-ttu-id="64619-624">Описание</span><span class="sxs-lookup"><span data-stu-id="64619-624">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL \*</span><span class="sxs-lookup"><span data-stu-id="64619-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL\*</span></span></td>
<td><span data-ttu-id="64619-626">Подавляет страницу свойств элемента «общие» для камеры.</span><span class="sxs-lookup"><span data-stu-id="64619-626">Suppress the general item property page for a camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span><span class="sxs-lookup"><span data-stu-id="64619-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span></span></td>
<td><span data-ttu-id="64619-628">Подавляет страницу свойств элемента "Общие" для сканера.</span><span class="sxs-lookup"><span data-stu-id="64619-628">Suppress the general item property page for a scanner.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <span data-ttu-id="64619-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>пиктуретимед</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-630">Это свойство содержит параметр метода перемещения.</span><span class="sxs-lookup"><span data-stu-id="64619-630">This property contains the transfer method setting.</span></span> <span data-ttu-id="64619-631">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="64619-631">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="64619-632">Приложение считывает это свойство для определения метода перемещения данных минидривер.</span><span class="sxs-lookup"><span data-stu-id="64619-632">An application reads this property to determine the minidriver's method of data transfer.</span></span></p>
<p><span data-ttu-id="64619-633">Требуется для всех элементов WIA 2,0, поддерживающих перемещение.</span><span class="sxs-lookup"><span data-stu-id="64619-633">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="64619-634">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="64619-634">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="64619-635">В следующей таблице приведены константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="64619-635">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="64619-636">Звездочка \* указывает константы, которые не являются допустимыми в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-636">The asterisk \* indicates constants that are not valid with Windows Vista and later.</span></span> <span data-ttu-id="64619-637">(Они доступны только через интерфейс <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="64619-637">(They are only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64619-638">Тип переноса</span><span class="sxs-lookup"><span data-stu-id="64619-638">Transfer Type</span></span></th>
<th><span data-ttu-id="64619-639">Описание</span><span class="sxs-lookup"><span data-stu-id="64619-639">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64619-640">TYMED_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="64619-640">TYMED_CALLBACK\*</span></span></td>
<td><span data-ttu-id="64619-641">Перенос изображения в память в полосах.</span><span class="sxs-lookup"><span data-stu-id="64619-641">Transfer an image to memory, in bands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-642">TYMED_MULTIPAGE_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="64619-642">TYMED_MULTIPAGE_CALLBACK\*</span></span></td>
<td><span data-ttu-id="64619-643">Перемещение нескольких образов в память в полосах.</span><span class="sxs-lookup"><span data-stu-id="64619-643">Transfer multiple images to memory, in bands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64619-644">TYMED_FILE</span><span class="sxs-lookup"><span data-stu-id="64619-644">TYMED_FILE</span></span></td>
<td><span data-ttu-id="64619-645">Перенос изображения в файл.</span><span class="sxs-lookup"><span data-stu-id="64619-645">Transfer an image to a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64619-646">TYMED_MULTIPAGE_FILE</span><span class="sxs-lookup"><span data-stu-id="64619-646">TYMED_MULTIPAGE_FILE</span></span></td>
<td><span data-ttu-id="64619-647">Перенос изображения в файл.</span><span class="sxs-lookup"><span data-stu-id="64619-647">Transfer an image to a file.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="64619-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>пиктуреитемуплоадитемсизе</dt> </span><span class="sxs-lookup"><span data-stu-id="64619-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="64619-649">Поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="64619-649">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="64619-650">Указывает число байтов для отправки для элемента.</span><span class="sxs-lookup"><span data-stu-id="64619-650">Specifies the number of bytes to upload for an item.</span></span></p>
<p><span data-ttu-id="64619-651">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="64619-651">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="64619-652">Требования</span><span class="sxs-lookup"><span data-stu-id="64619-652">Requirements</span></span>



| <span data-ttu-id="64619-653">Требование</span><span class="sxs-lookup"><span data-stu-id="64619-653">Requirement</span></span> | <span data-ttu-id="64619-654">Значение</span><span class="sxs-lookup"><span data-stu-id="64619-654">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="64619-655">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64619-655">Minimum supported client</span></span><br/> | <span data-ttu-id="64619-656">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64619-656">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="64619-657">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64619-657">Minimum supported server</span></span><br/> | <span data-ttu-id="64619-658">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64619-658">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="64619-659">Header</span><span class="sxs-lookup"><span data-stu-id="64619-659">Header</span></span><br/>                   | <dl> <span data-ttu-id="64619-660"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="64619-660"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




