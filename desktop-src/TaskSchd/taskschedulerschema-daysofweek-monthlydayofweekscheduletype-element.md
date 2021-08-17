---
title: DaysOfWeek (Монслидайофвиксчедулетипе), элемент
description: Указывает дни недели, в которые выполняется задача. | DaysOfWeek (Монслидайофвиксчедулетипе), элемент
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
keywords:
- планировщик задач элемента DaysOfWeek
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7ed2a597c1b92245a34dae510c079a5b5aa7a4e7893a78dbb70d7bc5988d580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357147"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a>DaysOfWeek (Монслидайофвиксчедулетипе), элемент

Указывает дни недели, в которые выполняется задача.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

Элемент **DaysOfWeek** определяется сложным типом [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                      | Унаследован от                                                                                         | Описание                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**счедулебимонсдайофвик**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Указывает триггер, который запускает задание для ежемесячного расписания недели.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                   | Тип | Описание                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Пятница**](taskschedulerschema-friday-daysofweektype-element.md)       |      | Указывает, что задача выполняется в пятницу.<br/>    |
| [**Понедельник**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Указывает, что задача выполняется в понедельник.<br/>    |
| [**Суббота**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Указывает, что задача выполняется в субботу.<br/>  |
| [**Воскресенье**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Указывает, что задача выполняется в воскресенье.<br/>    |
| [**Четверг**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Указывает, что задача выполняется в четверг.<br/>  |
| [**Вторник**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Указывает, что задача выполняется во вторник.<br/>   |
| [**Среда**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Указывает, что задача выполняется в среду.<br/> |



## <a name="remarks"></a>Remarks

Для разработки сценариев дни недели для месячного дня недели задаются с помощью свойства [**монслидовтригжер. DaysOfWeek**](monthlydowtrigger-daysofweek.md) .

Для разработки на C++ дни недели для месячного дня недели задаются с помощью свойства [**имонслидовтригжер::D айсофвик**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) .

Приведенные выше дочерние элементы определяются сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет месячный календарь дня недели, который запускает задачу в понедельник первой недели для каждого месяца года.


```XML
<ScheduleByMonthDayOfWeek>
    <Weeks>
        <Week>1</Week>
    </Weeks>
    <DaysOfWeek>
        <Monday/>
    </DaysOfWeek>
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonthDayOfWeek>
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

 

 





