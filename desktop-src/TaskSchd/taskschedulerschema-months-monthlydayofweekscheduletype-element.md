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
ms.openlocfilehash: a963032a2d33f13158af249f2b867037cf50082be005efa579148031c8e30585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959604"
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
| [**Август**](taskschedulerschema-august-monthstype-element.md)       |      | Указывает, что задача выполняется в августе.<br/>    |
| [**Декабрь**](taskschedulerschema-december-monthstype-element.md)   |      | Указывает, что задача выполняется в декабре.<br/>  |
| [**Февраль**](taskschedulerschema-february-monthstype-element.md)   |      | Указывает, что задача выполняется в феврале.<br/>  |
| [**Январь**](taskschedulerschema-january-monthstype-element.md)     |      | Указывает, что задача выполняется в январе.<br/>   |
| [**Июль**](taskschedulerschema-july-monthstype-element.md)           |      | Указывает, что задача выполняется в июле.<br/>      |
| [**Июнь**](taskschedulerschema-june-monthstype-element.md)           |      | Указывает, что задача выполняется в июне.<br/>      |
| [**Март**](taskschedulerschema-march-monthstype-element.md)         |      | Указывает, что задача выполняется в марте.<br/>     |
| [**Май**](taskschedulerschema-may-monthstype-element.md)             |      | Указывает, что задача выполняется в Май.<br/>       |
| [**Ноябрь**](taskschedulerschema-november-monthstype-element.md)   |      | Указывает, что задача выполняется в ноябре.<br/>  |
| [**Октябрь**](taskschedulerschema-october-monthstype-element.md)     |      | Указывает, что задача выполняется в октябре.<br/>   |
| [**Сентябрь**](taskschedulerschema-september-monthstype-element.md) |      | Указывает, что задача выполняется в сентябре.<br/> |



## <a name="remarks"></a>Remarks

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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





