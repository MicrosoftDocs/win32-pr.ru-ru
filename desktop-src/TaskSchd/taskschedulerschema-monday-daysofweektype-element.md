---
title: Понедельник (Дайсофвиктипе), элемент
description: Указывает, что задача выполняется в понедельник.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- планировщик задач элемента понедельник
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3967db32a6ccd536e2e389e84de4eec05b333634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492057"
---
# <a name="monday-daysofweektype-element"></a>Понедельник (Дайсофвиктипе), элемент

Указывает, что задача выполняется в понедельник.

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

Элемент **Monday** определяется сложным типом [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                                  | Унаследован от                                                             | Описание                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (Монслидайофвиксчедулетипе)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) | Указывает дни недели, в которых задача выполняется для ежемесячного расписания недели.<br/> |
| [**DaysOfWeek (Виклисчедулетипе)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) | Указывает дни недели, в которых задача выполняется для еженедельного расписания.<br/>              |



## <a name="examples"></a>Примеры

Следующий XML-код определяет календарь дня недели, который запускает задачу в понедельник.


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





