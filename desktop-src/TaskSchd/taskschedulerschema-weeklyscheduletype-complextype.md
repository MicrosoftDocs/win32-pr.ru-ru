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
ms.openlocfilehash: 5f886b2901a5cf1ff1c9db0c8ec761a796b8e68a0f3bdc746afa13a9d8e32ee6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099784"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





