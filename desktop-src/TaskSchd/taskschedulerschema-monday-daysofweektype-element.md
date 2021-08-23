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
ms.openlocfilehash: 22bd1028a36efa6e2fe96a300b221073dbf87f14e77621d8b1591f85c7f6fd6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513943"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





