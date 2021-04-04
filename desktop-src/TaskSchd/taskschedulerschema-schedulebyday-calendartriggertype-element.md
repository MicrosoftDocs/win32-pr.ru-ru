---
title: Счедулебидай (Календартригжертипе), элемент
description: Указывает ежедневное расписание.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- планировщик задач ежедневного триггера, XML-элемент
- планировщик задач элемента Счедулебидай
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989145"
---
# <a name="schedulebyday-calendartriggertype-element"></a>Счедулебидай (Календартригжертипе), элемент

Указывает ежедневное расписание. Например, задача начинается в 8:00 раз в день, каждые-каждый день, каждый третий день и т. д.

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

Элемент **счедулебидай** определяется сложным типом [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                             | Унаследован от                                                                       | Описание                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) | Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                            | Тип             | Описание                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**дайсинтервал**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | Указывает интервал между днями в расписании.<br/> |



## <a name="remarks"></a>Комментарии

Перечисленный выше дочерний элемент определяется сложными типами элементов [**даилисчедулетипе**](taskschedulerschema-dailyscheduletype-complextype.md) .

Время дня, когда начинается задача, задается элементом [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Для разработки сценариев ежедневный триггер указывается с помощью объекта [**даилитригжер**](weeklytrigger.md) .

Для разработки на C++ ежедневный триггер указывается с помощью интерфейса [**идаилитригжер**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет ежедневный триггер календаря, который запускает задачу каждый день.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Полный пример кода XML для задачи, в котором указано ежедневное расписание, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).

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

 

 





