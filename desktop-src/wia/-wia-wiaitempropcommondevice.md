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
# <a name="common-device-property-constants"></a>Общие константы свойств устройства

В дополнение к свойствам сведений об устройстве для устройств получения изображений Windows (WIA) в реестре содержатся значения свойств, которые могут быть прочитаны и записаны приложениями. Они связаны с объектом [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) или [**IWiaItem2**](-wia-iwiaitem2.md) . Свойства устройства представляют сведения об устройстве, такие как состояние подключения и время устройства. Каждое свойство устройства имеет связанную строку свойства устройства.

Указанные здесь константы свойств устройства являются общими для большинства или всех аппаратных устройств WIA.

Префикс "WIA \_ DPA \_ " указывает свойство устройства для всех устройств и является соглашением об именовании, используемым в C/C++. В целях написания сценариев эти константы используют префикс "устройство" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) . Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.



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
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>девицеконнектстатус</dt> </dl></td>
<td style="text-align: left;">Текущее состояние подключения для устройства. Минидривер создает и поддерживает это свойство.<br/> Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Свойство может иметь следующие возможные значения.<br/> 
<table>
<thead>
<tr class="header">
<th>Состояние подключения</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DEVICE_NOT_CONNECTED</td>
<td>Устройство не подключено.</td>
</tr>
<tr class="even">
<td>WIA_DEVICE_CONNECTED</td>
<td>Устройство подключено и работает.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>девицедевицетиме</dt> </dl></td>
<td style="text-align: left;"><p>Текущее время, хранящееся на устройстве. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Это свойство поддерживается только устройствами с внутренним временем. Если можно задать часы устройства, это свойство доступно для чтения и записи; в противном случае он доступен только для чтения.</p>
<p>Устройства WIA сообщают о времени в структуре <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> .</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>девицефирмвареверсион</dt> </dl></td>
<td style="text-align: left;"><p>Версия встроенного по устройства. Это значение должно быть строковым значением, например &quot; 1.0.4 &quot; или &quot; 1,0 ABC &quot; . Минидривер создает и поддерживает это свойство. Если WIA минидривер не предоставляет ресурс версии, служба WIA предоставляет значение &quot; 0.0.0.0 в &quot; качестве значения по умолчанию. Приложение считывает это свойство, чтобы определить версию библиотеки WIA минидривер DLL.</p>
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



 

 
