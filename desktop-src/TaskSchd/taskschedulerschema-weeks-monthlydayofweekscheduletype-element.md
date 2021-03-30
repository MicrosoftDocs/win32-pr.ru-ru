---
title: Weeks (Монслидайофвиксчедулетипе), элемент
description: Указывает недели месяца, в которых выполняется задача.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Элемент weeks планировщик задач
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803634"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>Weeks (Монслидайофвиксчедулетипе), элемент

Указывает недели месяца, в которых выполняется задача.

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

Элемент **weeks** определяется сложным типом [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                                      | Унаследован от                                                                                         | Описание                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**счедулебимонсдайофвик**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Указывает триггер, который запускает задание в месячном расписании недели.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                    | Тип                                                        | Описание                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**Неделя**](taskschedulerschema-week-weekstype-element.md) | [**виктипе**](taskschedulerschema-weektype-simpletype.md) | Указывает конкретную неделю месяца.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки сценариев недели месяца указываются с помощью свойства [**монслидовтригжер. виксофмонс**](monthlydowtrigger-weeksofmonth.md) .

Для разработки на C++ недели месяца указываются с помощью свойства [**имонслидовтригжер:: виксофмонс**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) .

При указании недель месяца используйте 1-4, чтобы указать первые четыре недели месяца, или используйте строку "Last", чтобы указать последнюю неделю независимо от недели.

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

 

 





