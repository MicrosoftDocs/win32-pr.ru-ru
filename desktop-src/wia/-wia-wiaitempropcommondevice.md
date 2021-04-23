---
description: В дополнение к свойствам сведений об устройстве для устройств получения изображений Windows (WIA) в реестре содержатся значения свойств, которые могут быть прочитаны и записаны приложениями.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Общие константы свойств устройства (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541890"
---
# <a name="common-device-property-constants"></a><span data-ttu-id="96f21-103">Общие константы свойств устройства</span><span class="sxs-lookup"><span data-stu-id="96f21-103">Common Device Property Constants</span></span>

<span data-ttu-id="96f21-104">В дополнение к свойствам сведений об устройстве для устройств получения изображений Windows (WIA) в реестре содержатся значения свойств, которые могут быть прочитаны и записаны приложениями.</span><span class="sxs-lookup"><span data-stu-id="96f21-104">In addition to device information properties, Windows Image Acquisition (WIA) devices have property values stored in the registry that applications read and write.</span></span> <span data-ttu-id="96f21-105">Они связаны с объектом [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) или [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="96f21-105">They are associated with the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object or [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <span data-ttu-id="96f21-106">Свойства устройства представляют сведения об устройстве, такие как состояние подключения и время устройства.</span><span class="sxs-lookup"><span data-stu-id="96f21-106">Device properties represent device information such as connection status and device time.</span></span> <span data-ttu-id="96f21-107">Каждое свойство устройства имеет связанную строку свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="96f21-107">Each device property has an associated device property string.</span></span>

<span data-ttu-id="96f21-108">Указанные здесь константы свойств устройства являются общими для большинства или всех аппаратных устройств WIA.</span><span class="sxs-lookup"><span data-stu-id="96f21-108">The Device Property Constants listed here are common to most or all WIA hardware devices.</span></span>

<span data-ttu-id="96f21-109">Префикс "WIA \_ DPA \_ " указывает свойство устройства для всех устройств и является соглашением об именовании, используемым в C/C++.</span><span class="sxs-lookup"><span data-stu-id="96f21-109">The prefix "WIA\_DPA\_" indicates a Device Property for All devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="96f21-110">В целях написания сценариев эти константы используют префикс "устройство" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="96f21-110">For scripting purposes these constants use the prefix "Device" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="96f21-111">Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="96f21-111">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="96f21-112">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="96f21-112">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="96f21-113">Описание</span><span class="sxs-lookup"><span data-stu-id="96f21-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <span data-ttu-id="96f21-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>девицеконнектстатус</dt> </span><span class="sxs-lookup"><span data-stu-id="96f21-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="96f21-115">Текущее состояние подключения для устройства.</span><span class="sxs-lookup"><span data-stu-id="96f21-115">The current connection status for the device.</span></span> <span data-ttu-id="96f21-116">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="96f21-116">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="96f21-117">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="96f21-117">Type: <strong>VT_I4</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="96f21-118">Свойство может иметь следующие возможные значения.</span><span class="sxs-lookup"><span data-stu-id="96f21-118">The property can have the following possible values.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="96f21-119">Состояние подключения</span><span class="sxs-lookup"><span data-stu-id="96f21-119">Connect Status</span></span></th>
<th><span data-ttu-id="96f21-120">Определение</span><span class="sxs-lookup"><span data-stu-id="96f21-120">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96f21-121">WIA_DEVICE_NOT_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="96f21-121">WIA_DEVICE_NOT_CONNECTED</span></span></td>
<td><span data-ttu-id="96f21-122">Устройство не подключено.</span><span class="sxs-lookup"><span data-stu-id="96f21-122">Device is not connected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96f21-123">WIA_DEVICE_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="96f21-123">WIA_DEVICE_CONNECTED</span></span></td>
<td><span data-ttu-id="96f21-124">Устройство подключено и работает.</span><span class="sxs-lookup"><span data-stu-id="96f21-124">Device is connected and operational.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <span data-ttu-id="96f21-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>девицедевицетиме</dt> </span><span class="sxs-lookup"><span data-stu-id="96f21-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="96f21-126">Текущее время, хранящееся на устройстве.</span><span class="sxs-lookup"><span data-stu-id="96f21-126">The current clock time that is stored on the device.</span></span> <span data-ttu-id="96f21-127">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="96f21-127">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="96f21-128">Тип: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="96f21-128">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong>, Access: Read/Write or Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="96f21-129">Это свойство поддерживается только устройствами с внутренним временем.</span><span class="sxs-lookup"><span data-stu-id="96f21-129">This property is supported only by devices that have an internal clock.</span></span> <span data-ttu-id="96f21-130">Если можно задать часы устройства, это свойство доступно для чтения и записи; в противном случае он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="96f21-130">If the device clock can be set, this property is Read/Write; otherwise, it is Read-only.</span></span></p>
<p><span data-ttu-id="96f21-131">Устройства WIA сообщают о времени в структуре <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> .</span><span class="sxs-lookup"><span data-stu-id="96f21-131">WIA devices report time in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <span data-ttu-id="96f21-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>девицефирмвареверсион</dt> </span><span class="sxs-lookup"><span data-stu-id="96f21-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="96f21-133">Версия встроенного по устройства.</span><span class="sxs-lookup"><span data-stu-id="96f21-133">The device firmware version.</span></span> <span data-ttu-id="96f21-134">Это значение должно быть строковым значением, например &quot; 1.0.4 &quot; или &quot; 1,0 ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="96f21-134">This value must be a string value, such as &quot;1.0.4&quot; or &quot;1.0abc&quot;.</span></span> <span data-ttu-id="96f21-135">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="96f21-135">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="96f21-136">Если WIA минидривер не предоставляет ресурс версии, служба WIA предоставляет значение &quot; 0.0.0.0 в &quot; качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="96f21-136">If the WIA minidriver does not supply a version resource, the WIA service supplies the value &quot;0.0.0.0&quot; as a default.</span></span> <span data-ttu-id="96f21-137">Приложение считывает это свойство, чтобы определить версию библиотеки WIA минидривер DLL.</span><span class="sxs-lookup"><span data-stu-id="96f21-137">An application reads this property to determine the version of the WIA minidriver DLL.</span></span></p>
<p><span data-ttu-id="96f21-138">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="96f21-138">Type: <strong>VT_BSTR</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="96f21-139">Требования</span><span class="sxs-lookup"><span data-stu-id="96f21-139">Requirements</span></span>



| <span data-ttu-id="96f21-140">Требование</span><span class="sxs-lookup"><span data-stu-id="96f21-140">Requirement</span></span> | <span data-ttu-id="96f21-141">Значение</span><span class="sxs-lookup"><span data-stu-id="96f21-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="96f21-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96f21-142">Minimum supported client</span></span><br/> | <span data-ttu-id="96f21-143">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="96f21-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="96f21-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96f21-144">Minimum supported server</span></span><br/> | <span data-ttu-id="96f21-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96f21-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="96f21-146">Header</span><span class="sxs-lookup"><span data-stu-id="96f21-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="96f21-147"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="96f21-147"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
