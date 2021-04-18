---
title: DaysOfMonth (Монслисчедулетипе), элемент
description: Указывает дни месяца, в которые выполняется задача.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- планировщик задач элемента DaysOfMonth
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682140"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a>DaysOfMonth (Монслисчедулетипе), элемент

Указывает дни месяца, в которые выполняется задача.

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

Элемент **DaysOfMonth** определяется сложным типом [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                    | Унаследован от                                                                                         | Описание                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**счедулебимонс**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Указывает триггер, который запускает задание для ежемесячного расписания недели.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                        | Тип                                                                    | Описание                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**День**](taskschedulerschema-day-daysofmonthtype-element.md) | [**дайофмонстипе**](taskschedulerschema-dayofmonthtype-simpletype.md) | Указывает день месяца, в который выполняется задача.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки скриптов дни месяца для расписания задаются с помощью свойства [**монслитригжер. DaysOfMonth**](monthlytrigger-daysofmonth.md) .

Для разработки на C++ дни месяца для расписания задаются с помощью свойства [**имонслитригжер::D айсофмонс**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .

Дочерний элемент должен повторяться для каждого дня месяца, который будет выполняться задачей.

## <a name="examples"></a>Примеры

Следующий XML-код определяет месячный триггер календаря, который запускает задачу (в 8:30 AM) в 1-й день каждого месяца.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
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

 

 





