---
description: Следующие константы формируют набор допустимых команд аппаратного устройства для получения образа Windows (WIA).
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Команды устройства WIA (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897434"
---
# <a name="wia-device-commands"></a>Команды устройства WIA

Следующие константы формируют набор допустимых команд аппаратного устройства для получения образа Windows (WIA).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </dl></td>
<td style="text-align: left;">Приводит к тому, что минидривер устройства синхронизируют кэшированные элементы с аппаратным устройством. Если устройство поддерживает метод <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>ивиаитем:: анализеитем</strong></a> , выполнив эту команду, минидривер отклоняет результаты анализа и сбрасывает элемент в исходное состояние. Все драйверы должны поддерживать эту команду.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </dl></td>
<td style="text-align: left;">Заставляет устройство WIA получить изображение.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </dl></td>
<td style="text-align: left;">Указывает устройству удалить все элементы, которые могут быть удалены из дерева объектов <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> , представляющих устройство. Удаление элемента запрещено путем задания свойств элемента. Дополнительные сведения см. в разделе <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>ивиапропертистораже:: сетпропертистреам</strong></a> и <a href="-wia-property-attributes.md">атрибуты свойств</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Используется для сканеров документов. Заставляет средство проверки загружать следующую страницу в обработчике документов.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Используется для сканеров документов. Указывает устройству выгружать все оставшиеся страницы в обработчике документа. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <dt><strong>WIA_CMD_START_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Используется для сканеров документов с податчиком страниц. Указывает устройству запустить двигатель устройства подачи. Эта функция доступна начиная с Windows 8.<br/>
<blockquote>
[!Note]<br />
Минидривер WIA должен отклонить эту команду и вернуть <strong>WIA_ERROR_INVALID_COMMAND</strong> , если свойство <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> не поддерживается или имеет значение WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Используется для сканеров документов с податчиком страниц. Указывает устройству на необходимость отключить двигатель устройства подачи. Эта функция доступна начиная с Windows 8.<br/>
<blockquote>
[!Note]<br />
Минидривер WIA должен отклонить эту команду и вернуть <strong>WIA_ERROR_INVALID_COMMAND</strong> , если свойство <strong>WIA_IPS_FEEDER_CONTROL</strong> не поддерживается или имеет значение WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Используется для сканеров документов с податчиком страниц. Указывает устройству приостановить мотор. Эта функция доступна начиная с Windows 8.<br/>
<blockquote>
[!Note]<br />
Минидривер WIA должен отклонить эту команду и вернуть <strong>WIA_ERROR_INVALID_COMMAND</strong> , если свойство <strong>WIA_IPS_FEEDER_CONTROL</strong> не поддерживается или имеет значение WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Header<br/>                   | <dl> <dt>Виадеф. h</dt> </dl> |



 

 
