---
description: Портативные устройства Windows поддерживают следующие свойства устройства.
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: Свойства устройства (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Device
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 696d5fefd65d194f9bb451b0095ed87b90f8a22c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668685"
---
# <a name="device-properties-portabledeviceh"></a><span data-ttu-id="ec6e1-103">Свойства устройства (Портабледевице. h)</span><span class="sxs-lookup"><span data-stu-id="ec6e1-103">Device Properties (PortableDevice.h)</span></span>

<span data-ttu-id="ec6e1-104">Портативные устройства Windows поддерживают следующие свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-104">Windows Portable Devices supports the following device properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ec6e1-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="ec6e1-105">Property</span></span></th>
<th><span data-ttu-id="ec6e1-106">VarType</span><span class="sxs-lookup"><span data-stu-id="ec6e1-106">VarType</span></span></th>
<th><span data-ttu-id="ec6e1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ec6e1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec6e1-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span></span></td>
<td><span data-ttu-id="ec6e1-109"><strong>VT_DATE</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-109"><strong>VT_DATE</strong></span></span></td>
<td><span data-ttu-id="ec6e1-110">Текущая дата и время на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-110">The current date and time on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6e1-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span></span></td>
<td><span data-ttu-id="ec6e1-112"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-112"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="ec6e1-113">Версия встроенного по устройства.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-113">The device's firmware version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6e1-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="ec6e1-115"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-115"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="ec6e1-116">Уникальный 16-байтовый идентификатор, который является общим для нескольких транспортов, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-116">A unique 16-byte identifier that is common across multiple transports supported by the device.</span></span> <span data-ttu-id="ec6e1-117">Если одно устройство поддерживает несколько транспортов, это свойство можно использовать для связи различных драйверов транспорта WPD с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-117">If a single device supports multiple transports, this property may be used to associate the various transport WPD drivers with that device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6e1-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span></span></td>
<td><span data-ttu-id="ec6e1-119"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-119"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="ec6e1-120">Имя производителя устройства, читаемое человеком.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-120">A human-readable device manufacturer name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6e1-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span></span></td>
<td><span data-ttu-id="ec6e1-122"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-122"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="ec6e1-123">Модель устройства.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-123">The device model.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6e1-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="ec6e1-125"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-125"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="ec6e1-126">Уникальный 16-байтовый идентификатор, используемый для различения различных моделей устройства.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-126">A unique 16-byte identifier used to differentiate among different models of a device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6e1-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span></span></td>
<td><span data-ttu-id="ec6e1-128"><strong>VT_UI8</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-128"><strong>VT_UI8</strong></span></span></td>
<td><span data-ttu-id="ec6e1-129">Значение, указывающее сетевой идентификатор EUI-64 устройства; Это свойство используется для сетевых операций по внешнему каналу. Если устройство имеет физические сетевые адреса MAC-48 (типичные сети IPv4), адрес MAC-48 кодируется в адрес EUI-64 как две половины адреса MAC-48, разделенные FF-FF.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-129">A value that specifies the EUI-64 network identifier of the device; this property is used for out-of-band network operations.If the device has MAC-48 physical network addresses (typical of IPv4 networks), the MAC-48 address is encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span> <span data-ttu-id="ec6e1-130">Значение EUI-64 хранится в &quot; сети или в &quot; &quot; порядке с обратным порядком байтов &quot; , где адрес EUI-64 из 01-02-03-ff-FF-04-05-06 будет помещен в VT_UI8, чтобы десятичное значение было равно 72624942021346566.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-130">The EUI-64 value is stored in &quot;network&quot; or &quot;big-endian&quot; order, where an EUI-64 address of 01-02-03-FF-FF-04-05-06 would be placed in the VT_UI8 such that the decimal value is 72624942021346566.</span></span> <span data-ttu-id="ec6e1-131">Это свойство является обязательным для любого устройства, поддерживающего номинальную или безопасную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-131">This property is required on any device that supports Nominal or Secure Authentication.</span></span> <span data-ttu-id="ec6e1-132">Это свойство рекомендуется использовать на устройствах, поддерживающих только нулевую проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-132">This property is recommended on devices that support only Zero Authentication.</span></span> <span data-ttu-id="ec6e1-133">Значение может использоваться узлом для автоматического установления доступа к устройству без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-133">The value can be used by the host to automatically establish access to the device without user intervention.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6e1-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span></span></td>
<td><span data-ttu-id="ec6e1-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="ec6e1-136">Значение от 0 до 100, указывающее уровень питания батареи устройства, 0 — нет, а 100 — с полной оплатой.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-136">A value from 0 to 100 that specifies the power level of the device's battery, with 0 being none, and 100 being fully charged.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6e1-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span></span></td>
<td><span data-ttu-id="ec6e1-138">VT_UI4</span><span class="sxs-lookup"><span data-stu-id="ec6e1-138">VT_UI4</span></span></td>
<td><span data-ttu-id="ec6e1-139">Перечисление <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> , указывающее источник питания устройства.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-139">A <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> enumeration that specifies the power source of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6e1-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span></span></td>
<td><span data-ttu-id="ec6e1-141"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-141"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="ec6e1-142">Используемый протокол устройства.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-142">The device protocol that is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6e1-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span></span></td>
<td><span data-ttu-id="ec6e1-144"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-144"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="ec6e1-145">Серийный номер устройства.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-145">The device's serial number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6e1-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span></span></td>
<td><span data-ttu-id="ec6e1-147"><strong>VT_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-147"><strong>VT_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="ec6e1-148">Значение типа, указывающее, являются ли Поддерживаемые форматы, возвращенные с устройства, предпочтительным порядком.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-148">A value that specifies whether the supported formats returned from the device are in a preferred order.</span></span> <span data-ttu-id="ec6e1-149">Первый формат в списке является наиболее предпочтительным для устройства, а последний является наименее предпочтительным. Приложения могут использовать это свойство, чтобы определить, перечислены ли Поддерживаемые форматы устройства в предпочтительном порядке.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-149">The first format in the list is most preferred by the device, while the last is the least preferred.Applications may use this property to determine whether a device's supported formats are listed in a preferred order.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6e1-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span></span></td>
<td><span data-ttu-id="ec6e1-151"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-151"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="ec6e1-152">Логическое значение, указывающее, являются ли Поддерживаемые форматы, возвращенные с устройства, предпочтительным порядком. то есть первый возвращаемый формат наиболее предпочтителен, а последний возвращенный формат является наименьшим предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-152">A Boolean value that specifies whether the supported formats returned from the device are in a preferred order; that is, the first returned format is most preferred while the last returned format is least preferred.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6e1-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span></span></td>
<td><span data-ttu-id="ec6e1-154"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-154"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="ec6e1-155">Логическое значение, указывающее, поддерживает ли устройство неподдерживающие объекты.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-155">A Boolean value that specifies whether the device supports non-consumable objects.</span></span> <span data-ttu-id="ec6e1-156">Это объекты, которые устройство предназначено только для хранения, а не для воспроизведения или использования каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-156">These are objects that the device is only meant to store, not play or use in any way.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6e1-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span></span></td>
<td><span data-ttu-id="ec6e1-158"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-158"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="ec6e1-159">Понятное описание <em>участника синхронизации</em>устройства.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-159">A human-readable description of a device's <em>synchronization partner</em>.</span></span> <span data-ttu-id="ec6e1-160">Это устройство, приложение или сервер, с которым взаимодействует устройство для поддержания общего состояния или группы файлов между обоими партнерами.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-160">This is a device, application, or server that the device communicates with to maintain a common state or group of files between both partners.</span></span> <span data-ttu-id="ec6e1-161">К примерам относятся программы электронной почты и библиотеки музыки.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-161">Examples include e-mail programs and music libraries.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6e1-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span></span></td>
<td><span data-ttu-id="ec6e1-163"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-163"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="ec6e1-164">Значение, представляющее понятное имя, заданное пользователем на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-164">A value that represents the friendly name set by the user on the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6e1-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span></span></td>
<td><span data-ttu-id="ec6e1-166"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-166"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="ec6e1-167">Транспорт, поддерживаемый устройством, например USB, IP или Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-167">the transport supported by the device, such as USB, IP, or Bluetooth.</span></span> <span data-ttu-id="ec6e1-168">Допустимые значения относятся к типу перечисления <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ec6e1-168">Valid values are of the <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> enumeration type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6e1-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span></span></td>
<td><span data-ttu-id="ec6e1-170"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-170"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="ec6e1-171">Значение типа, указывающее тип устройства; приложения используют это свойство только в целях представления.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-171">A value that specifies the device type; applications use this property for representation purposes only.</span></span> <span data-ttu-id="ec6e1-172">Функциональные характеристики устройства определяются с помощью функциональных объектов. Устройства, которые не предоставляют значок устройства, например <strong>WPD_RESOURCE_ICON</strong> для объекта устройства, будут представлены в пространстве имен WPD с помощью общего значка.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-172">Functional characteristics of the device are decided through functional objects.Devices that do not supply a device icon, for example, a <strong>WPD_RESOURCE_ICON</strong> for the device object, will be represented in the WPD Namespace with a generic icon.</span></span> <span data-ttu-id="ec6e1-173">Этот значок будет зависеть от указанного типа устройства. Например, если тип устройства — мобильный, используется универсальный значок телефона.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-173">This icon will depend on the specified device type, for example, if the device type is a mobile phone, the generic phone icon is used.</span></span> <span data-ttu-id="ec6e1-174">При первой установке устройства Установщик класса WPD запрашивает это значение свойства и сохраняет его в реестре устройства в параметре PORTABLE_DEVICE_TYPE в качестве REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-174">On first install of the device, the WPD Class Installer will query this property value and store it in the device registry under the PORTABLE_DEVICE_TYPE value as a REG_DWORD.</span></span><br/> <span data-ttu-id="ec6e1-175">Возможные значения этого параметра относятся к перечислению <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> , определенному в портабледевице. h.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-175">This parameter's possible values are from the <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="ec6e1-176">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ec6e1-176">Values are:</span></span><br/> <dl> <span data-ttu-id="ec6e1-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span></span><br /><span data-ttu-id="ec6e1-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span></span><br /><span data-ttu-id="ec6e1-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span></span><br /><span data-ttu-id="ec6e1-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span></span><br /><span data-ttu-id="ec6e1-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span></span><br /><span data-ttu-id="ec6e1-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span></span><br /><span data-ttu-id="ec6e1-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6e1-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span></span></td>
<td><span data-ttu-id="ec6e1-185"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="ec6e1-185"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="ec6e1-186">Если это свойство существует и имеет значение <strong>true</strong>, устройство можно использовать с Device Stage.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-186">If this property exists and is set to <strong>TRUE</strong>, the device can be used with Device Stage .</span></span> <span data-ttu-id="ec6e1-187">Это предназначено для устройств, которые не могут хранить метаданные с помощью <strong>службы метаданных устройства</strong>, но будут предоставлять метаданные на серверах Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ec6e1-187">This is meant for devices that cannot store metadata using the <strong>Device Metadata Service</strong>, but will provide metadata on the Microsoft servers.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="ec6e1-188">Требования</span><span class="sxs-lookup"><span data-stu-id="ec6e1-188">Requirements</span></span>



| <span data-ttu-id="ec6e1-189">Требование</span><span class="sxs-lookup"><span data-stu-id="ec6e1-189">Requirement</span></span> | <span data-ttu-id="ec6e1-190">Значение</span><span class="sxs-lookup"><span data-stu-id="ec6e1-190">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6e1-191">Header</span><span class="sxs-lookup"><span data-stu-id="ec6e1-191">Header</span></span><br/> | <dl> <span data-ttu-id="ec6e1-192"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec6e1-192"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec6e1-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec6e1-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec6e1-194">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="ec6e1-194">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




