---
title: Сложный тип Монсстипе
description: Определяет дочерние элементы и сведения о последовательности для элементов month (Монслидайофвиксчедулетипе) и months (Монслисчедулетипе).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- планировщик задач сложного типа Монсстипе
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801480"
---
# <a name="monthstype-complex-type"></a>Сложный тип Монсстипе

Определяет дочерние элементы и сведения о последовательности для элементов [**Month (монслидайофвиксчедулетипе)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) и [**months (монслисчедулетипе)**](taskschedulerschema-months-monthlyscheduletype-element.md) .

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Тип | Описание                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [**Апрель**](taskschedulerschema-april-monthstype-element.md)         | Н/Д  | Указывает, что задача выполняется в апреле. <br/>     |
| [**Августа**](taskschedulerschema-august-monthstype-element.md)       | Н/Д  | Указывает, что задача выполняется в августе. <br/>    |
| [**Декабрь**](taskschedulerschema-december-monthstype-element.md)   | Н/Д  | Указывает, что задача выполняется в декабре. <br/>  |
| [**Февраль**](taskschedulerschema-february-monthstype-element.md)   | Н/Д  | Указывает, что задача выполняется в феврале. <br/>  |
| [**Января**](taskschedulerschema-january-monthstype-element.md)     | Н/Д  | Указывает, что задача выполняется в январе. <br/>   |
| [**Июле**](taskschedulerschema-july-monthstype-element.md)           | Н/Д  | Указывает, что задача выполняется в июле. <br/>      |
| [**Июнь**](taskschedulerschema-june-monthstype-element.md)           | Н/Д  | Указывает, что задача выполняется в июне. <br/>      |
| [**Март**](taskschedulerschema-march-monthstype-element.md)         | Н/Д  | Указывает, что задача выполняется в марте. <br/>     |
| [**Мая**](taskschedulerschema-may-monthstype-element.md)             | Н/Д  | Указывает, что задача выполняется в Май. <br/>       |
| [**Ноября**](taskschedulerschema-november-monthstype-element.md)   | Н/Д  | Указывает, что задача выполняется в ноябре. <br/>  |
| [**Октябре**](taskschedulerschema-october-monthstype-element.md)     | Н/Д  | Указывает, что задача выполняется в октябре. <br/>   |
| [**Сентябрь**](taskschedulerschema-september-monthstype-element.md) | Н/Д  | Указывает, что задача выполняется в сентябре. <br/> |



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

 

 





