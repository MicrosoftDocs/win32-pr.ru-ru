---
title: Воскресенье (Дайсофвиктипе), элемент
description: Указывает, что задача выполняется в воскресенье.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Воскресенье элемента планировщик задач
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25a184d16d5239f2294f02ddb6144fa4b886d1f83e11cbbd6e481f7fda77e1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356265"
---
# <a name="sunday-daysofweektype-element"></a>Воскресенье (Дайсофвиктипе), элемент

Указывает, что задача выполняется в воскресенье.

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

Элемент **Sunday** определяется сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                                  | Унаследован от                                                             | Описание                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (Монслидайофвиксчедулетипе)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) | Указывает дни недели, в которых задача выполняется для ежемесячного расписания недели.<br/> |
| [**DaysOfWeek (Виклисчедулетипе)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) | Указывает дни недели, в которых задача выполняется для еженедельного расписания.<br/>              |



## <a name="examples"></a>Примеры

Следующий XML-код определяет календарь дня недели, который запускает задачу в воскресенье.


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





