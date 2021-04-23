---
description: Свойства сведений об устройстве — это свойства, описывающие установку и установку устройства.
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Константы свойств сведений об устройстве (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 18c44bb310c2dcee5bb227e0885a71b58f5b362e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711075"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="e9794-103">Константы свойств сведений об устройстве</span><span class="sxs-lookup"><span data-stu-id="e9794-103">Device Information Property Constants</span></span>

<span data-ttu-id="e9794-104">Свойства сведений об устройстве — это свойства, описывающие установку и установку устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="e9794-105">Эти свойства доступны через интерфейсы [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , а также через корневой элемент.</span><span class="sxs-lookup"><span data-stu-id="e9794-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="e9794-106">Свойства сведений об устройстве имеют префикс "WIA \_ DIP \_ " (свойство сведений об устройстве) и предоставляются службой "получение образа Windows" (WIA).</span><span class="sxs-lookup"><span data-stu-id="e9794-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="e9794-107">В целях написания сценариев эти константы используют префикс «DeviceInfo» и являются частью перечислимого типа [виадевицеинфопропертид](-wia-wiadeviceinfopropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="e9794-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="e9794-108">Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="e9794-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e9794-109">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="e9794-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e9794-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e9794-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="e9794-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>девицеинфодевид</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9794-112">Строка идентификатора устройства для WIA минидривер.</span><span class="sxs-lookup"><span data-stu-id="e9794-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="e9794-113">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="e9794-114">Тип: VT_BSTR, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="e9794-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>девицеинфовенддеск</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9794-116">Строка описания поставщика для минидривер WIA.</span><span class="sxs-lookup"><span data-stu-id="e9794-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="e9794-117">Описание поставщика получено из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="e9794-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="e9794-118">Приложение считывает это свойство, чтобы получить описание поставщика устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="e9794-119">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="e9794-120">Тип: VT_BSTR, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="e9794-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>девицеинфодевдеск</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9794-122">Строка описания устройства для WIA минидривер.</span><span class="sxs-lookup"><span data-stu-id="e9794-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="e9794-123">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-124">Строка описания устройства, которое содержит это свойство, получено из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="e9794-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="e9794-125">Приложение считывает это свойство, чтобы получить описание устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="e9794-126">Тип: VT_BSTR, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="e9794-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>девицеинфодевтипе</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9794-128">Тип устройства и подтип устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-128">The device type and device subtype.</span></span> <span data-ttu-id="e9794-129">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-130">Используйте макрос GET_STIDEVICE_TYPE, чтобы получить тип устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="e9794-131">Тип и подтип устройства получаются из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="e9794-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="e9794-132">Приложение считывает это свойство, чтобы определить, использует ли оно сканер, камеру или видеоустройство.</span><span class="sxs-lookup"><span data-stu-id="e9794-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="e9794-133">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="e9794-134">В настоящее время типы устройств определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e9794-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="e9794-135">Звездочка \* указывает, что тип устройства не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e9794-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="e9794-136">Двойная звездочка \* \* указывает, что тип устройства не поддерживается Windows Server 2003, Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e9794-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e9794-137">Тип</span><span class="sxs-lookup"><span data-stu-id="e9794-137">Type</span></span></th>
<th><span data-ttu-id="e9794-138">Значение</span><span class="sxs-lookup"><span data-stu-id="e9794-138">Value</span></span></th>
<th><span data-ttu-id="e9794-139">Определение</span><span class="sxs-lookup"><span data-stu-id="e9794-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9794-140">стидевицетипедефаулт</span><span class="sxs-lookup"><span data-stu-id="e9794-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="e9794-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="e9794-141">0x0000</span></span></td>
<td><span data-ttu-id="e9794-142">Устройство по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e9794-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9794-143">стидевицетипесканнер</span><span class="sxs-lookup"><span data-stu-id="e9794-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="e9794-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="e9794-144">0x0001</span></span></td>
<td><span data-ttu-id="e9794-145">Устройство сканера (см. <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> , чтобы определить, является ли сканер устройством подачи или подачи листов.)</span><span class="sxs-lookup"><span data-stu-id="e9794-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9794-146">Стидевицетипедигиталкамера \*</span><span class="sxs-lookup"><span data-stu-id="e9794-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="e9794-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="e9794-147">0x0002</span></span></td>
<td><span data-ttu-id="e9794-148">Устройство камеры</span><span class="sxs-lookup"><span data-stu-id="e9794-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9794-149">Стидевицетипестреамингвидео \* \*</span><span class="sxs-lookup"><span data-stu-id="e9794-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="e9794-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="e9794-150">0x0003</span></span></td>
<td><span data-ttu-id="e9794-151">Видеоустройство</span><span class="sxs-lookup"><span data-stu-id="e9794-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="e9794-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>девицеинфопортнаме</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-153">Имя порта установленного устройства, которое назначается драйвером режима ядра, работающим с устройством.</span><span class="sxs-lookup"><span data-stu-id="e9794-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="e9794-154">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-155">Приложение считывает это свойство для определения имени порта.</span><span class="sxs-lookup"><span data-stu-id="e9794-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="e9794-156">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="e9794-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>девицеинфодевнаме</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-158">Название устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-158">The name of the device.</span></span> <span data-ttu-id="e9794-159">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-160">Имя устройства, содержащееся в этом свойстве, получено из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="e9794-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="e9794-161">Приложение считывает это свойство для получения имени устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="e9794-162">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="e9794-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>девицеинфосервернаме</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-164">Имя сервера, на котором работает WIA-минидривер.</span><span class="sxs-lookup"><span data-stu-id="e9794-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="e9794-165">Это свойство является необязательным для Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e9794-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="e9794-166">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="e9794-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>девицеинфоремотедевид</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-168">ИДЕНТИФИКАТОР устройства WIA, установленного на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e9794-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="e9794-169">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-170">Он используется только внутри службы WIA.</span><span class="sxs-lookup"><span data-stu-id="e9794-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="e9794-171">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="e9794-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>девицеинфауиклсид</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-173">Предоставленный поставщиком идентификатор CLSID для любого COM-объекта расширения пользовательского интерфейса, устанавливаемого с помощью WIA минидривер.</span><span class="sxs-lookup"><span data-stu-id="e9794-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="e9794-174">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-175">Значение CLSID пользовательского интерфейса, содержащееся в этом свойстве, получено из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="e9794-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="e9794-176">Если CLSID пользовательского интерфейса не указан, служба WIA предоставляет значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e9794-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="e9794-177">Это свойство используется только внутри службы WIA при отображении пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e9794-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="e9794-178">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="e9794-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>девицеинфохвконфиг</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-180">Тип соединения, который используется устройством.</span><span class="sxs-lookup"><span data-stu-id="e9794-180">The type of connection that the device is using.</span></span> <span data-ttu-id="e9794-181">Служба WIA создает и поддерживает это свойство, и только служба WIA может изменить ее.</span><span class="sxs-lookup"><span data-stu-id="e9794-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="e9794-182">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="e9794-183">Свойство может иметь следующие возможные значения.</span><span class="sxs-lookup"><span data-stu-id="e9794-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e9794-184">Значение</span><span class="sxs-lookup"><span data-stu-id="e9794-184">Value</span></span></th>
<th><span data-ttu-id="e9794-185">Определение</span><span class="sxs-lookup"><span data-stu-id="e9794-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9794-186">1</span><span class="sxs-lookup"><span data-stu-id="e9794-186">1</span></span></td>
<td><span data-ttu-id="e9794-187">Универсальное устройство WDM</span><span class="sxs-lookup"><span data-stu-id="e9794-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9794-188">2</span><span class="sxs-lookup"><span data-stu-id="e9794-188">2</span></span></td>
<td><span data-ttu-id="e9794-189">Устройство SCSI</span><span class="sxs-lookup"><span data-stu-id="e9794-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9794-190">4</span><span class="sxs-lookup"><span data-stu-id="e9794-190">4</span></span></td>
<td><span data-ttu-id="e9794-191">USB-устройство</span><span class="sxs-lookup"><span data-stu-id="e9794-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9794-192">8</span><span class="sxs-lookup"><span data-stu-id="e9794-192">8</span></span></td>
<td><span data-ttu-id="e9794-193">Последовательное устройство</span><span class="sxs-lookup"><span data-stu-id="e9794-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9794-194">16</span><span class="sxs-lookup"><span data-stu-id="e9794-194">16</span></span></td>
<td><span data-ttu-id="e9794-195">Параллельное устройство</span><span class="sxs-lookup"><span data-stu-id="e9794-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="e9794-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>девицеинфобаудрате</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-197">Текущая настройка скорости передачи для устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="e9794-198">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-199">&quot; &quot; Если устройство не подключено с помощью последовательного кабеля, оно должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="e9794-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="e9794-200">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="e9794-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>девицеинфостиженкапабилитиес</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-202">Универсальные возможности сти для устройства, полученные из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="e9794-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="e9794-203">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-204">Приложение считывает это свойство для определения универсальных возможностей сти устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="e9794-205">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="e9794-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>девицеинфовиаверсион</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-207">Число (в виде строки) текущей версии WIA, установленной в системе.</span><span class="sxs-lookup"><span data-stu-id="e9794-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="e9794-208">Приложение считывает это свойство для определения версии WIA, установленной в системе.</span><span class="sxs-lookup"><span data-stu-id="e9794-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="e9794-209">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-210">Это свойство доступно в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e9794-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="e9794-211">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="e9794-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>девицеинфодриверверсион</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-213">Текущая версия DLL минидривер WIA.</span><span class="sxs-lookup"><span data-stu-id="e9794-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="e9794-214">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-215">Это свойство доступно в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e9794-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="e9794-216">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="e9794-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>девицеинфопнпид</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-218">Текущий идентификатор PnP для устройства.</span><span class="sxs-lookup"><span data-stu-id="e9794-218">The current PnP id for the device.</span></span> <span data-ttu-id="e9794-219">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-220">Это свойство доступно в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e9794-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="e9794-221">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="e9794-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>девицеинфостидриверверсион</dt> </span><span class="sxs-lookup"><span data-stu-id="e9794-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9794-223">Универсальная версия драйвера сти.</span><span class="sxs-lookup"><span data-stu-id="e9794-223">The generic STI driver version.</span></span> <span data-ttu-id="e9794-224">Служба WIA создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e9794-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9794-225">Приложение считывает это свойство для определения универсальной версии драйвера сти.</span><span class="sxs-lookup"><span data-stu-id="e9794-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="e9794-226">Это свойство доступно в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e9794-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="e9794-227">Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9794-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="e9794-228">Требования</span><span class="sxs-lookup"><span data-stu-id="e9794-228">Requirements</span></span>



| <span data-ttu-id="e9794-229">Требование</span><span class="sxs-lookup"><span data-stu-id="e9794-229">Requirement</span></span> | <span data-ttu-id="e9794-230">Значение</span><span class="sxs-lookup"><span data-stu-id="e9794-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e9794-231">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9794-231">Minimum supported client</span></span><br/> | <span data-ttu-id="e9794-232">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e9794-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e9794-233">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9794-233">Minimum supported server</span></span><br/> | <span data-ttu-id="e9794-234">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9794-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e9794-235">Header</span><span class="sxs-lookup"><span data-stu-id="e9794-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9794-236"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9794-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




