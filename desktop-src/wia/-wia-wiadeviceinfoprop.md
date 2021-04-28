---
description: Константы свойств сведений об устройстве — свойства сведений об устройстве — это свойства, описывающие установку и установку устройства.
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
ms.openlocfilehash: aec37ae84eed6b15bc10a4e979a5d95d21be3423
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097242"
---
# <a name="device-information-property-constants"></a>Константы свойств сведений об устройстве

Свойства сведений об устройстве — это свойства, описывающие установку и установку устройства. Эти свойства доступны через интерфейсы [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) , а также через корневой элемент. Свойства сведений об устройстве имеют префикс "WIA \_ DIP \_ " (свойство сведений об устройстве) и предоставляются службой "получение образа Windows" (WIA). В целях написания сценариев эти константы используют префикс «DeviceInfo» и являются частью перечислимого типа [виадевицеинфопропертид](-wia-wiadeviceinfopropertyid.md) . Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>девицеинфодевид</dt> </dl></td>
<td style="text-align: left;">Строка идентификатора устройства для WIA минидривер. Служба WIA создает и поддерживает это свойство.<br/> Тип: VT_BSTR, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>девицеинфовенддеск</dt> </dl></td>
<td style="text-align: left;">Строка описания поставщика для минидривер WIA. Описание поставщика получено из INF-файла. Приложение считывает это свойство, чтобы получить описание поставщика устройства. Служба WIA создает и поддерживает это свойство.<br/> Тип: VT_BSTR, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>девицеинфодевдеск</dt> </dl></td>
<td style="text-align: left;">Строка описания устройства для WIA минидривер. Служба WIA создает и поддерживает это свойство. Строка описания устройства, которое содержит это свойство, получено из INF-файла. Приложение считывает это свойство, чтобы получить описание устройства.<br/> Тип: VT_BSTR, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>девицеинфодевтипе</dt> </dl></td>
<td style="text-align: left;">Тип устройства и подтип устройства. Служба WIA создает и поддерживает это свойство. Используйте макрос GET_STIDEVICE_TYPE, чтобы получить тип устройства. Тип и подтип устройства получаются из INF-файла. Приложение считывает это свойство, чтобы определить, использует ли оно сканер, камеру или видеоустройство.<br/> Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> В настоящее время типы устройств определяются следующим образом. Звездочка * указывает, что тип устройства не поддерживается в Windows Vista и более поздних версиях. Двойная звездочка * * указывает, что тип устройства не поддерживается Windows Server 2003, Windows Vista или более поздней версии. <br/> 
<table>
<thead>
<tr class="header">
<th>Тип</th>
<th>Значение</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>стидевицетипедефаулт</td>
<td>0x0000</td>
<td>Устройство по умолчанию</td>
</tr>
<tr class="even">
<td>стидевицетипесканнер</td>
<td>0x0001</td>
<td>Устройство сканера (см. <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> , чтобы определить, является ли сканер устройством подачи или подачи листов.)</td>
</tr>
<tr class="odd">
<td>Стидевицетипедигиталкамера *</td>
<td>0x0002</td>
<td>Устройство камеры</td>
</tr>
<tr class="even">
<td>Стидевицетипестреамингвидео * *</td>
<td>0x0003</td>
<td>Видеоустройство</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>девицеинфопортнаме</dt> </dl></td>
<td style="text-align: left;"><p>Имя порта установленного устройства, которое назначается драйвером режима ядра, работающим с устройством. Служба WIA создает и поддерживает это свойство. Приложение считывает это свойство для определения имени порта.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>девицеинфодевнаме</dt> </dl></td>
<td style="text-align: left;"><p>Название устройства. Служба WIA создает и поддерживает это свойство. Имя устройства, содержащееся в этом свойстве, получено из INF-файла. Приложение считывает это свойство для получения имени устройства.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>девицеинфосервернаме</dt> </dl></td>
<td style="text-align: left;"><p>Имя сервера, на котором работает WIA-минидривер. Это свойство является необязательным для Windows XP и более поздних версий.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>девицеинфоремотедевид</dt> </dl></td>
<td style="text-align: left;"><p>ИДЕНТИФИКАТОР устройства WIA, установленного на удаленном компьютере. Служба WIA создает и поддерживает это свойство. Он используется только внутри службы WIA.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>девицеинфауиклсид</dt> </dl></td>
<td style="text-align: left;"><p>Предоставленный поставщиком идентификатор CLSID для любого COM-объекта расширения пользовательского интерфейса, устанавливаемого с помощью WIA минидривер. Служба WIA создает и поддерживает это свойство. Значение CLSID пользовательского интерфейса, содержащееся в этом свойстве, получено из INF-файла. Если CLSID пользовательского интерфейса не указан, служба WIA предоставляет значение по умолчанию. Это свойство используется только внутри службы WIA при отображении пользовательского интерфейса.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>девицеинфохвконфиг</dt> </dl></td>
<td style="text-align: left;"><p>Тип соединения, который используется устройством. Служба WIA создает и поддерживает это свойство, и только служба WIA может изменить ее.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Свойство может иметь следующие возможные значения.</p>

<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Универсальное устройство WDM</td>
</tr>
<tr class="even">
<td>2</td>
<td>Устройство SCSI</td>
</tr>
<tr class="odd">
<td>4</td>
<td>USB-устройство</td>
</tr>
<tr class="even">
<td>8</td>
<td>Последовательное устройство</td>
</tr>
<tr class="odd">
<td>16</td>
<td>Параллельное устройство</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>девицеинфобаудрате</dt> </dl></td>
<td style="text-align: left;"><p>Текущая настройка скорости передачи для устройства. Служба WIA создает и поддерживает это свойство. &quot; &quot; Если устройство не подключено с помощью последовательного кабеля, оно должно быть пустым.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>девицеинфостиженкапабилитиес</dt> </dl></td>
<td style="text-align: left;"><p>Универсальные возможности сти для устройства, полученные из INF-файла. Служба WIA создает и поддерживает это свойство. Приложение считывает это свойство для определения универсальных возможностей сти устройства.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>девицеинфовиаверсион</dt> </dl></td>
<td style="text-align: left;"><p>Число (в виде строки) текущей версии WIA, установленной в системе. Приложение считывает это свойство для определения версии WIA, установленной в системе. Служба WIA создает и поддерживает это свойство. Это свойство доступно в Windows XP и более поздних версиях.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>девицеинфодриверверсион</dt> </dl></td>
<td style="text-align: left;"><p>Текущая версия DLL минидривер WIA. Служба WIA создает и поддерживает это свойство. Это свойство доступно в Windows XP и более поздних версиях.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>девицеинфопнпид</dt> </dl></td>
<td style="text-align: left;"><p>Текущий идентификатор PnP для устройства. Служба WIA создает и поддерживает это свойство. Это свойство доступно в Windows Vista и более поздних версиях.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>девицеинфостидриверверсион</dt> </dl></td>
<td style="text-align: left;"><p>Универсальная версия драйвера сти. Служба WIA создает и поддерживает это свойство. Приложение считывает это свойство для определения универсальной версии драйвера сти. Это свойство доступно в Windows Vista и более поздних версиях.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Header<br/>                   | <dl> <dt>Виадеф. h</dt> </dl> |



 

 




