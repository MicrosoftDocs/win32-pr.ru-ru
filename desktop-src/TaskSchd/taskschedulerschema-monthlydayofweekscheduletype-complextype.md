---
title: Сложный тип Монслидайофвиксчедулетипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Счедулебимонсдайофвик.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- планировщик задач сложного типа Монслидайофвиксчедулетипе
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0e15a697c07de4df59f7762e4b6dc0d167b1fff8ab7477f77f5e59d6b654f7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575204"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a>Сложный тип Монслидайофвиксчедулетипе

Определяет дочерние элементы и сведения о последовательности для элемента [**счедулебимонсдайофвик**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) .

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                   | Тип                                                                     | Описание                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) | Указывает дни недели, в которые выполняется задача.<br/>   |
| [**Месяц**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**монсстипе**](taskschedulerschema-monthstype-complextype.md)         | Указывает месяцы года, в течение которых выполняется задача.<br/> |
| [**Недели**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [**викстипе**](taskschedulerschema-weekstype-complextype.md)           | Указывает недели месяца, в течение которых выполняется задача.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





