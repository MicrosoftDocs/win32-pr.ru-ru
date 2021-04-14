---
title: Months (Монслидайофвиксчедулетипе), элемент
description: Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Элемент months планировщик задач
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415097"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>Months (Монслидайофвиксчедулетипе), элемент

Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

Элемент **months** определяется сложным типом [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                                            | Унаследован от                                                                                         | Описание                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**Счедулебимонсдайофвик (Календартригжертипе)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Указывает триггер, который запускает задание для ежемесячного расписания недели.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Тип | Описание                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Апрель**](taskschedulerschema-april-monthstype-element.md)         |      | Указывает, что задача выполняется в апреле.<br/>     |
| [**Августа**](taskschedulerschema-august-monthstype-element.md)       |      | Указывает, что задача выполняется в августе.<br/>    |
| [**Декабрь**](taskschedulerschema-december-monthstype-element.md)   |      | Указывает, что задача выполняется в декабре.<br/>  |
| [**Февраль**](taskschedulerschema-february-monthstype-element.md)   |      | Указывает, что задача выполняется в феврале.<br/>  |
| [**Января**](taskschedulerschema-january-monthstype-element.md)     |      | Указывает, что задача выполняется в январе.<br/>   |
| [**Июле**](taskschedulerschema-july-monthstype-element.md)           |      | Указывает, что задача выполняется в июле.<br/>      |
| [**Июнь**](taskschedulerschema-june-monthstype-element.md)           |      | Указывает, что задача выполняется в июне.<br/>      |
| [**Март**](taskschedulerschema-march-monthstype-element.md)         |      | Указывает, что задача выполняется в марте.<br/>     |
| [**Мая**](taskschedulerschema-may-monthstype-element.md)             |      | Указывает, что задача выполняется в Май.<br/>       |
| [**Ноября**](taskschedulerschema-november-monthstype-element.md)   |      | Указывает, что задача выполняется в ноябре.<br/>  |
| [**Октябре**](taskschedulerschema-october-monthstype-element.md)     |      | Указывает, что задача выполняется в октябре.<br/>   |
| [**Сентябрь**](taskschedulerschema-september-monthstype-element.md) |      | Указывает, что задача выполняется в сентябре.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки со сценариями месяцы года для расписания месячного дня недели задаются с помощью свойства [**монслидовтригжер. монссофеар**](monthlydowtrigger-monthsofyear.md) .

Для разработки на C++ месяцы месяца года для расписания ежемесячного дня задаются с помощью свойства [**имонслидовтригжер:: монссофеар**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) .

Приведенные выше дочерние элементы определяются сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .

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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





