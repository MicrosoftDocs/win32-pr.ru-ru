---
title: Сложный тип Дайсофвиктипе
description: Определяет дочерние элементы и сведения о последовательности для элементов DaysOfWeek (Виклисчедулетипе) и DaysOfWeek (Монслидайофвиксчедулетипе).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- планировщик задач сложного типа Дайсофвиктипе
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341335"
---
# <a name="daysofweektype-complex-type"></a>Сложный тип Дайсофвиктипе

Определяет дочерние элементы и сведения о последовательности для элементов [**DaysOfWeek (виклисчедулетипе)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) и [**DaysOfWeek (монслидайофвиксчедулетипе)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                   | Тип | Описание                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [**Пятница**](taskschedulerschema-friday-daysofweektype-element.md)       | Н/Д  | Задача выполняется в пятницу. <br/>    |
| [**Понедельник**](taskschedulerschema-monday-daysofweektype-element.md)       | Н/Д  | Задача выполняется в понедельник.<br/>     |
| [**Суббота**](taskschedulerschema-saturday-daysofweektype-element.md)   | Н/Д  | Задача выполняется в субботу. <br/>  |
| [**Воскресенье**](taskschedulerschema-sunday-daysofweektype-element.md)       | Н/Д  | Задача выполняется в воскресенье. <br/>    |
| [**Четверг**](taskschedulerschema-thursday-daysofweektype-element.md)   | Н/Д  | Задача выполняется в четверг <br/>   |
| [**Вторник**](taskschedulerschema-tuesday-daysofweektype-element.md)     | Н/Д  | Задача выполняется во вторник. <br/>   |
| [**Среда**](taskschedulerschema-wednesday-daysofweektype-element.md) | Н/Д  | Задача выполняется в среду. <br/> |



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

 

 





