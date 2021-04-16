---
description: Портативные устройства Windows поддерживают следующие свойства событий.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Свойства события (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699225"
---
# <a name="event-properties"></a>Свойства события

Портативные устройства Windows поддерживают следующие свойства событий.



<table>
<thead>
<tr class="header">
<th>Свойство</th>
<th>VarType</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Зарезервировано для последующего использования.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Логическое значение, указывающее, является ли событие широковещательным для всех клиентов. Клиенты могут получить это событие, зарегистрировав обратный вызов с помощью <strong>ипортабледевице:: Advise</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Логическое значение, указывающее, изменилась ли дочерняя иерархия объекта. Этот параметр используется для уведомления вызывающей стороны о том, что некоторые дочерние элементы для указанного объекта были добавлены или удалены. Обычно изменение иерархии инициируется на стороне устройства. Клиентам может потребоваться перечислить дочерние элементы этой папки для обновления своих представлений.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></td>
<td><strong>VT_CLSID</strong></td>
<td>Значение, идентифицирующее событие.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Файл cookie передаются обратно клиенту при запросе создания объекта путем вызова метода <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>ипортабледевицеконтент:: креатеобжектвиспропертиесанддата</strong></a> . Этот параметр добавляется в качестве удобства, чтобы вызывающий объект привязать событие, добавленное к объекту, к запросу, отправленному для создания объекта. Драйвер передает этот файл cookie обратно в качестве <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> возвращаемого значения при обработке команды <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Значение, уникально идентифицирующее родительский объект. Это свойство похоже на <strong>WPD_OBJECT_PARENT_ID</strong>, но этот идентификатор не меняется между сеансами.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Значение типа, указывающее ход выполнения выполняемой в данный момент операции. Значение этого свойства может находиться в диапазоне от 0 до 100 с 100, указывающим, что операция завершена.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Значение, указывающее текущее состояние операции, например "запущено", "запущено", "остановлено" и т. д. Возможные значения этого параметра относятся к перечислению <strong>WPD_OPERATION_STATES</strong> , определенному в портабледевице. h. Возможны следующие значения:<br/> <dl> <strong>WPD_OPERATION_STATE_UNSPECIFIED</strong><br />
<strong>WPD_OPERATION_STATE_STARTED</strong><br />
<strong>WPD_OPERATION_STATE_RUNNING</strong><br />
<strong>WPD_OPERATION_STATE_PAUSED</strong><br />
<strong>WPD_OPERATION_STATE_CANCELLED</strong><br />
<strong>WPD_OPERATION_STATE_FINISHED</strong><br />
<strong>WPD_OPERATION_STATE_ABORTED</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Значение типа, указывающее устройство, которое является источником события. Это устройство или идентификатор службы, заданные системой Plug-and-Play, и — это та же строка, которая используется в методах <strong>ипортабледевице:: Open</strong>или <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>Ипортабледевицесервице:: Open</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Строка, используемая драйвером WPD для обнаружения операций метода службы устройства. Приложения не должны использовать этот параметр напрямую.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства и атрибуты WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




