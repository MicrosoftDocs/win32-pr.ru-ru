---
title: Системмонитор DataSourceType, свойство
description: Возвращает или задает источник данных счетчика производительности.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Сисмон свойство DataSourceType
- Свойство DataSourceType Сисмон, интерфейс Системмонитор
- Интерфейс Системмонитор Сисмон, свойство DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071839"
---
# <a name="systemmonitordatasourcetype-property"></a>Системмонитор: свойство Атасаурцетипе:D

Возвращает или задает источник данных счетчика производительности.

## <a name="syntax"></a>Синтаксис


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a>Значение свойства

Источник данных счетчика производительности. Возможные значения см. в разделе [**датасаурцетипеконстантс**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).

## <a name="exceptions"></a>Исключения



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип исключения</th>
<th>Условие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System. ArgumentException</strong></td>
<td>Это исключение может быть получено по одной из следующих причин:
<ul>
<li>Указано недопустимое значение источника данных.</li>
<li>Если источником данных является файл журнала, СИСМОН не может найти один из указанных файлов. Значение Err. Number — 0xC0000BD1.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

**До Windows Vista:** Невозможно добавить или удалить файлы журнала из [**коллекции файлов журнала**](systemmonitor-logfiles.md) , если для этого свойства задано значение сисмонлогфилес. Присвойте этому свойству значение Сисмонлогфилес после создания или изменения коллекции файлов журнала.

Кроме того, нельзя изменить свойства [**склдсннаме**](systemmonitor-sqldsnname.md) и [**скллогсетнаме**](systemmonitor-sqllogsetname.md) , если для этого свойства не должно быть задано значение сисмонскллог. Присвойте этому свойству значение Сисмонскллог после изменения имен сервера и базы данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системмонитор**](systemmonitor.md)
</dt> </dl>

 

 





