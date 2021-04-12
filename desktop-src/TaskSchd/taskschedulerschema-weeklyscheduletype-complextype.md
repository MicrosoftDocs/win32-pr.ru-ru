---
title: Сложный тип Виклисчедулетипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Счедулебивик.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- планировщик задач сложного типа Виклисчедулетипе
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 797e01c20e749593d64bad12f017af8be613992e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415224"
---
# <a name="weeklyscheduletype-complex-type"></a>Сложный тип Виклисчедулетипе

Определяет дочерние элементы и сведения о последовательности для элемента [**счедулебивик**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) .

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
        <xs:element name="WeeksInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="52"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                               | Тип                                                                     | Описание                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) | Указывает дни недели, в которые выполняется задача.<br/>    |
| [**виксинтервал**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | Указывает интервал между неделями в расписании.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





