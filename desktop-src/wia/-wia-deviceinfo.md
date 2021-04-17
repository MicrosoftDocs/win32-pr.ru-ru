---
description: Объект DeviceInfo предоставляет доступ к свойствам аппаратного устройства для получения образа Windows (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Объект DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656607"
---
# <a name="deviceinfo-object"></a>Объект DeviceInfo

Объект **DeviceInfo** предоставляет доступ к свойствам аппаратного устройства для получения образа Windows (WIA). Кроме того, метод [**CREATE**](-wia-iwiadeviceinfo-create.md) позволяет приложению или сценарию подключиться к устройству и получить объект [**элемента**](-wia-item.md) , представляющий устройство. Используйте метод [**Devices**](-wia-iwia-devices.md) для получения коллекции объектов **DeviceInfo** .

## <a name="members"></a>Элементы

Объект **DeviceInfo** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **DeviceInfo** содержит эти методы.



| Метод                                                 | Описание                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Создания**](-wia-iwiadeviceinfo-create.md)           | Метод [**CREATE**](-wia-iwiadeviceinfo-create.md) объекта **DeviceInfo** устанавливает соединение с устройством WIA, заданным объектом **DeviceInfo** , и возвращает объект [**Item**](-wia-item.md) , представляющий устройство.<br/> |
| [**жетпропбид**](-wia-iwiadeviceinfo-getpropbyid.md) | Метод [**жетпропбид**](-wia-iwiadeviceinfo-getpropbyid.md) объекта **DeviceInfo** использует идентификатор свойства устройства для возвращения его значения.<br/>                                                                                               |



 

### <a name="properties"></a>Свойства

Объект **DeviceInfo** имеет следующие свойства.



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
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-id.md"><strong>Удостоверения</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Получает идентификатор аппаратного устройства WIA. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Производителя</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Извлекает имя производителя данного устройства.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-name.md"><strong>Имя</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Имя аппаратного устройства WIA, отображаемое в пользовательском интерфейсе.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-port.md"><strong>Порту</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Извлекает порт, к которому подключено аппаратное устройство WIA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-type.md"><strong>Тип</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Возвращает тип аппаратного устройства WIA. Возможны следующие значения: <br/>
<ul>
<li>дигиталкамера</li>
<li>Сканер</li>
<li>стреамингвидео</li>
<li>Значение по умолчанию</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>уиклсид</strong></a><br/></td>
<td style="text-align: left;">Только для чтения<br/></td>
<td style="text-align: left;">Получает идентификатор класса пользовательского интерфейса, предоставленного изготовителем для этого аппаратного устройства WIA. Значение представляет собой строковое представление GUID. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




