---
title: Календартригжер (Тригжерграуп), элемент
description: Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- планировщик задач триггера календаря, XML-элемент
- планировщик задач элемента Календартригжер
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d02b14fa056940a8139e87d9b471f6eaef84c311eb095073f274a9b4adf3c6dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516974"
---
# <a name="calendartrigger-triggergroup-element"></a>Календартригжер (Тригжерграуп), элемент

Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

Элемент **календартригжер** определяется сложным типом [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                           | Унаследован от                                                         | Описание                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**План**](taskschedulerschema-triggers-tasktype-element.md) | [**тригжерстипе**](taskschedulerschema-triggerstype-complextype.md) | Задает триггеры, которые запускают задачу.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                                            | Тип                                                                                                 | Описание                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Включено (Тригжербасетипе)**](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | Логическое                                                                                              | Указывает, что триггер включен.<br/>                                                                                  |
| [**Ендбаундари (Тригжербасетипе)**](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | dateTime                                                                                             | Указывает дату и время деактивации триггера. Триггер не может запустить задачу после ее деактивации.<br/> |
| [**Ексекутионтимелимит (Тригжербасетипе)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | длительность                                                                                             | Указывает максимальное время, в течение которого задача может запускаться триггером.<br/>                                   |
| [**Повторение (Тригжербасетипе)**](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md)                             | Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.<br/>          |
| [**Счедулебидай (Календартригжертипе)**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**даилисчедулетипе**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Указывает ежедневное расписание.<br/>                                                                                             |
| [**Счедулебимонс (Календартригжертипе)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Указывает ежемесячное расписание.<br/>                                                                                           |
| [**Счедулебимонсдайофвик (Календартригжертипе)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Указывает триггер, который запускает задание в месячном расписании недели.<br/>                                                |
| [**Счедулебивик (Календартригжертипе)**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Указывает еженедельное расписание.<br/>                                                                                            |
| [**Стартбаундари (Тригжербасетипе)**](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | dateTime                                                                                             | Указывает дату и время активации триггера. Этот элемент является обязательным.<br/>                                    |



## <a name="attributes"></a>Атрибуты



| Имя | Тип | Описание                               |
|------|------|-------------------------------------------|
| Идентификатор   | ID   | Идентификатор триггера.<br/> |



## <a name="remarks"></a>Remarks

Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров времени и календаря ([**тиметригжер**](taskschedulerschema-timetrigger-triggergroup-element.md) и **календартригжер**).

Перечисленные выше дочерние элементы определяются сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) и [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .

Для разработки скриптов триггеры календаря указываются с помощью одного из следующих объектов.

-   [**даилитригжер**](dailytrigger.md)
-   [**виклитригжер**](weeklytrigger.md)
-   [**монслитригжер**](monthlytrigger.md)
-   [**монслидовтригжер**](monthlydowtrigger.md)

Для разработки на C++ триггеры календаря указываются с помощью одного из следующих интерфейсов.

-   [**идаилитригжер**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**ивиклитригжер**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [**имонслитригжер**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**имонслидовтригжер**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, указывающей триггер календаря, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





