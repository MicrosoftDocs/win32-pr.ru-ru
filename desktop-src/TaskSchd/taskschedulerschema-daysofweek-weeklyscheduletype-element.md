---
title: DaysOfWeek (Виклисчедулетипе), элемент
description: Указывает дни недели, в которые выполняется задача. | DaysOfWeek (Виклисчедулетипе), элемент
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
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
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684946"
---
# <a name="daysofweek-weeklyscheduletype-element"></a>DaysOfWeek (Виклисчедулетипе), элемент

Указывает дни недели, в которые выполняется задача.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

Элемент **DaysOfWeek** определяется сложным типом [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                  | Унаследован от                                                                     | Описание                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**счедулебивик**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md) | Указывает еженедельное расписание.<br/> |



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



## <a name="remarks"></a>Комментарии

Предыдущие дочерние элементы определяются сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .

Для разработки сценариев еженедельный интервал указывается с помощью свойства [**виклитригжер. виксинтервал**](weeklytrigger-weeksinterval.md) .

Для разработки на C++ еженедельный интервал задается с помощью свойства [**ивиклитригжер:: виксинтервал**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет ежедневный триггер календаря, который запускает задачу с понедельника по пятницу (в 8:00 AM) каждую неделю.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



Полный пример XML-кода для задачи, использующей еженедельный триггер, см. в разделе [Пример еженедельного триггера (XML)](weekly-trigger-example--xml-.md).

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

 

 





