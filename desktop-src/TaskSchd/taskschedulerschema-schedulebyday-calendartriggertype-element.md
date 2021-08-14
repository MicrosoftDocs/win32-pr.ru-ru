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
ms.openlocfilehash: f29cc4b702ba93aec44e3460279976f50c5563463accfb58b920ad79b757126a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131586"
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



## <a name="remarks"></a>Remarks

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

## <a name="requirements"></a>Requirements (Требования)



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

 

 





