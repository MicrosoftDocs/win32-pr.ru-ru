---
title: Счедулебимонсдайофвик (Календартригжертипе), элемент
description: Задает ежемесячное расписание для дня недели.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- планировщик задач элемента Счедулебимонсдайофвик
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803317"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>Счедулебимонсдайофвик (Календартригжертипе), элемент

Задает ежемесячное расписание для дня недели. Например, задача запускается в определенные дни недели, недели месяца и месяцы года.

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

Элемент **счедулебимонсдайофвик** определяется сложным типом [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                             | Унаследован от                                                                       | Описание                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) | Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                   | Тип                                                                     | Описание                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) | Указывает дни недели, в которые выполняется задача.<br/>       |
| [**Месяц**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**монсстипе**](taskschedulerschema-monthstype-complextype.md)         | Указывает месяцы года, в течение которых выполняется задача.<br/> |
| [**Недели**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | Указывает интервал между неделями в расписании.<br/>    |



## <a name="remarks"></a>Комментарии

Время дня, когда начинается задача, задается элементом [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Для разработки сценариев месячный триггер дня недели указывается с помощью объекта [**монслидовтригжер**](monthlydowtrigger.md) .

Для разработки на C++ триггер месячного дня недели указывается с помощью интерфейса [**имонслидовтригжер**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) .

Перечисленные выше дочерние элементы определяются сложными типами элементов [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет месячный день недели в календаре, который запускает задачу (в 8:00 AM) в понедельник первой недели для каждого месяца года.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
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
</CalendarTrigger>
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

 

 





