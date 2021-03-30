---
title: Day (Дайсофмонстипе), элемент
description: Указывает день месяца, в который выполняется задача.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Элемент Day планировщик задач
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071352"
---
# <a name="day-daysofmonthtype-element"></a>Day (Дайсофмонстипе), элемент

Указывает день месяца, в который выполняется задача.

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

Элемент **Day** определяется сложным типом [**дайсофмонстипе**](taskschedulerschema-daysofmonthtype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                            | Унаследован от                                                               | Описание                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**дайсофмонстипе**](taskschedulerschema-daysofmonthtype-complextype.md) | Указывает дни месяца, в которые выполняется задача.<br/> |



## <a name="examples"></a>Примеры

Следующий XML-код определяет дни ежемесячного календаря, в которых задача выполняется в первый и 15-й день месяца.


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





