---
title: Сложный тип Календартригжертипе
description: Определяет дочерние элементы и сведения о последовательности для элементов календаря.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- планировщик задач сложного типа Календартригжертипе
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a891f60d46f8826faed1cc4b95e4c55f6efa4f7f
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734169"
---
# <a name="calendartriggertype-complex-type"></a>Сложный тип Календартригжертипе

Определяет дочерние элементы и сведения о последовательности для элементов календаря.

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                      | Тип                                                                                                 | Описание                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**рандомделай**](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | длительность                                                                                             | Содержит время задержки, которое случайным образом добавляется к времени начала триггера. Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, P2DT5S имеет 2 дня, 5 секунд задержки).<br/> |
| [**счедулебидай**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**даилисчедулетипе**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Указывает ежедневное расписание. Например, задача запускается каждый день, каждый второй день, каждый третий день и т. д.<br/>                                                                                                               |
| [**счедулебимонс**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Указывает ежемесячное расписание. Например, задача начинается в 8:00 в определенные дни месяца в определенные месяцы. <br/>                                                                                                       |
| [**счедулебимонсдайофвик**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Указывает триггер, который запускает задание в месячном расписании недели. Например, задача запускается в определенные дни недели, недели месяца и месяцы года. <br/>                                               |
| [**счедулебивик**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Указывает еженедельное расписание. Например, задача начинается в 8:00 в конкретный день недели или в конкретный день недели, каждую неделю. <br/>                                                              |



## <a name="remarks"></a>Замечания

Помимо дочернего элемента, определенного здесь, элемент [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





