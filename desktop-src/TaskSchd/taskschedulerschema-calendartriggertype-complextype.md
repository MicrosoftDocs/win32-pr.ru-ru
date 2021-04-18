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
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672758"
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
| [**рандомделай**](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | длительность                                                                                             | Содержит время задержки, которое случайным образом добавляется к времени начала триггера. Формат этой строки — P <days> DT <hours> H <minutes> <seconds> S (например, P2DT5S — 2 дня, задержка 5 секунд).<br/> |
| [**счедулебидай**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**даилисчедулетипе**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Указывает ежедневное расписание. Например, задача запускается каждый день, каждый второй день, каждый третий день и т. д.<br/>                                                                                                               |
| [**счедулебимонс**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Указывает ежемесячное расписание. Например, задача начинается в 8:00 в определенные дни месяца в определенные месяцы. <br/>                                                                                                       |
| [**счедулебимонсдайофвик**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Указывает триггер, который запускает задание в месячном расписании недели. Например, задача запускается в определенные дни недели, недели месяца и месяцы года. <br/>                                               |
| [**счедулебивик**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Указывает еженедельное расписание. Например, задача начинается в 8:00 в конкретный день недели или в конкретный день недели, каждую неделю. <br/>                                                              |



## <a name="remarks"></a>Комментарии

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

 

 





