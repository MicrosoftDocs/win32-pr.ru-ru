---
description: Объект Сафевиа — это &\# 0034; безопасность для скриптов&\# 0034; точка входа для всех функций создания скриптов для получения изображений Windows (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Объект Сафевиа
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711090"
---
# <a name="safewia-object"></a>Объект Сафевиа

Объект **сафевиа** — это точка входа "безопасность для скриптов" для всех функций создания скриптов для получения изображений Windows (WIA). Любое приложение, использующее модель скриптов WIA, должно создавать объект **сафевиа** или [**WIA**](-wia-wia.md) . Используйте этот объект для перечисления и создания устройств и получения уведомлений о событиях оборудования.

## <a name="members"></a>Элементы

Объект **сафевиа** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **сафевиа** содержит эти методы.



| Метод                             | Описание                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Создания**](-wia-iwia-create.md) | Метод [**CREATE**](-wia-iwia-create.md) объекта [**WIA**](-wia-wia.md) устанавливает соединение с указанным устройством WIA и возвращает объект [**Item**](-wia-item.md) , представляющий устройство.<br/> |



 

### <a name="properties"></a>Свойства

Объект **сафевиа** имеет следующие свойства.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Свойство</th>
<th style="text-align: left;">Тип доступа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>Устройства</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Коллекция объектов <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> , представляющих все устройства, установленные на компьютере. Только для чтения. <br/>
<blockquote>
[!Note]<br />
Эта коллекция основана на 0.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |
| IID<br/>                      | \_САФЕВИА CLSID<br/>                                                                                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Одно**](-wia-wia.md)
</dt> </dl>

 

 




