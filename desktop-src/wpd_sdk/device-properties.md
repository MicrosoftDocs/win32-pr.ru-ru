---
description: Windows Портативные устройства поддерживают следующие свойства устройства.
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
ms.openlocfilehash: 5490323e60d353fade6dfb7f517533ecb5fa26ca9e78ae221b9ff584d8c13a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430988"
---
# <a name="device-properties-portabledeviceh"></a>Свойства устройства (Портабледевице. h)

Windows Портативные устройства поддерживают следующие свойства устройства.



<table>
<thead>
<tr class="header">
<th>Свойство.</th>
<th>VarType</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></td>
<td><strong>VT_DATE</strong></td>
<td>Текущая дата и время на устройстве.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Версия встроенного по устройства.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Уникальный 16-байтовый идентификатор, который является общим для нескольких транспортов, поддерживаемых устройством. Если одно устройство поддерживает несколько транспортов, это свойство можно использовать для связи различных драйверов транспорта WPD с этим устройством.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Имя производителя устройства, читаемое человеком.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Модель устройства.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Уникальный 16-байтовый идентификатор, используемый для различения различных моделей устройства.</td>
</tr>
<tr class="odd">
<td><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></td>
<td><strong>VT_UI8</strong></td>
<td>Значение, указывающее сетевой идентификатор EUI-64 устройства; Это свойство используется для сетевых операций по внешнему каналу. Если устройство имеет физические сетевые адреса MAC-48 (типичные сети IPv4), адрес MAC-48 кодируется в адрес EUI-64 как две половины адреса MAC-48, разделенные FF-FF. Значение EUI-64 хранится в &quot; сети или в &quot; &quot; порядке с обратным порядком байтов &quot; , где адрес EUI-64 из 01-02-03-ff-FF-04-05-06 будет помещен в VT_UI8, чтобы десятичное значение было равно 72624942021346566. Это свойство является обязательным для любого устройства, поддерживающего номинальную или безопасную проверку подлинности. Это свойство рекомендуется использовать на устройствах, поддерживающих только нулевую проверку подлинности. Значение может использоваться узлом для автоматического установления доступа к устройству без вмешательства пользователя.<br/></td>
</tr>
<tr class="even">
<td><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Значение от 0 до 100, указывающее уровень питания батареи устройства, 0 — нет, а 100 — с полной оплатой.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></td>
<td>VT_UI4</td>
<td>Перечисление <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> , указывающее источник питания устройства.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Используемый протокол устройства.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Серийный номер устройства.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></td>
<td><strong>VT_UNKNOWN</strong></td>
<td>Значение типа, указывающее, являются ли Поддерживаемые форматы, возвращенные с устройства, предпочтительным порядком. Первый формат в списке является наиболее предпочтительным для устройства, а последний является наименее предпочтительным. Приложения могут использовать это свойство, чтобы определить, перечислены ли Поддерживаемые форматы устройства в предпочтительном порядке.<br/></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Логическое значение, указывающее, являются ли Поддерживаемые форматы, возвращенные с устройства, предпочтительным порядком. то есть первый возвращаемый формат наиболее предпочтителен, а последний возвращенный формат является наименьшим предпочтительным.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Логическое значение, указывающее, поддерживает ли устройство неподдерживающие объекты. Это объекты, которые устройство предназначено только для хранения, а не для воспроизведения или использования каким-либо образом.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Понятное описание <em>участника синхронизации</em>устройства. Это устройство, приложение или сервер, с которым взаимодействует устройство для поддержания общего состояния или группы файлов между обоими партнерами. К примерам относятся программы электронной почты и библиотеки музыки.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Значение, представляющее понятное имя, заданное пользователем на устройстве.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Транспорт, поддерживаемый устройством, например USB, IP или Bluetooth. Допустимые значения относятся к типу перечисления <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> .</td>
</tr>
<tr class="even">
<td><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Значение типа, указывающее тип устройства; приложения используют это свойство только в целях представления. Функциональные характеристики устройства определяются с помощью функциональных объектов. Устройства, которые не предоставляют значок устройства, например <strong>WPD_RESOURCE_ICON</strong> для объекта устройства, будут представлены в пространстве имен WPD с помощью общего значка. Этот значок будет зависеть от указанного типа устройства. Например, если тип устройства — мобильный, используется универсальный значок телефона. При первой установке устройства Установщик класса WPD запрашивает это значение свойства и сохраняет его в реестре устройства в параметре PORTABLE_DEVICE_TYPE в качестве REG_DWORD.<br/> Возможные значения этого параметра относятся к перечислению <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> , определенному в портабледевице. h. Возможны следующие значения.<br/> <dl> <strong>WPD_DEVICE_TYPE_GENERIC</strong><br />
<strong>WPD_DEVICE_TYPE_CAMERA</strong><br />
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong><br />
<strong>WPD_DEVICE_TYPE_PHONE</strong><br />
<strong>WPD_DEVICE_TYPE_VIDEO</strong><br />
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong><br />
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Если это свойство существует и имеет значение <strong>true</strong>, устройство можно использовать с Device Stage. Это предназначено для устройств, которые не могут хранить метаданные с помощью <strong>службы метаданных устройства</strong>, но будут предоставлять метаданные на серверах Майкрософт.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства и атрибуты WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




