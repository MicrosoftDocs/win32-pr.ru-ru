---
title: Счедулебимонс (Календартригжертипе), элемент
description: Указывает ежемесячное расписание.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- планировщик задач элемента Счедулебимонс
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137019"
---
# <a name="schedulebymonth-calendartriggertype-element"></a>Счедулебимонс (Календартригжертипе), элемент

Указывает ежемесячное расписание. Например, задача начинается в 8:00 в определенные дни месяца в определенные месяцы.

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

Элемент **счедулебимонс** определяется сложным типом [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                             | Унаследован от                                                                       | Описание                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) | Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                  | Тип                                                                       | Описание                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfMonth (Монслисчедулетипе)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**дайсофмонстипе**](taskschedulerschema-daysofmonthtype-complextype.md) | Указывает дни месяца, в которые выполняется задача.<br/>  |
| [**Месяцы (Монслисчедулетипе)**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**монсстипе**](taskschedulerschema-monthstype-complextype.md)           | Указывает месяцы года, в течение которых выполняется задача.<br/> |



## <a name="remarks"></a>Комментарии

Время дня, когда начинается задача, задается элементом [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Для разработки скриптов ежемесячный триггер указывается с помощью объекта [**монслитригжер**](monthlytrigger.md) .

Для разработки на C++ ежемесячный триггер указывается с помощью интерфейса [**имонслитригжер**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) .

Перечисленные ниже дочерние элементы определяются сложными типами элементов [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет месячный триггер календаря, который запускает задачу (в 8:00 AM) на первый и 15-й день каждого месяца года.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
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

 

 





