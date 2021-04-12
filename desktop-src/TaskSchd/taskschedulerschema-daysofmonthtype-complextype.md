---
title: Сложный тип Дайсофмонстипе
description: Определяет дочерний элемент и сведения о последовательности для элемента DaysOfMonth (Монслисчедулетипе).
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- планировщик задач сложного типа Дайсофмонстипе
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1459528b47bf01a9e336b758b739c3f5751ee1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415948"
---
# <a name="daysofmonthtype-complex-type"></a>Сложный тип Дайсофмонстипе

Определяет дочерний элемент и сведения о последовательности для элемента [**DaysOfMonth (монслисчедулетипе)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) .

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                        | Тип                                                                    | Описание                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**День**](taskschedulerschema-day-daysofmonthtype-element.md) | [**дайофмонстипе**](taskschedulerschema-dayofmonthtype-simpletype.md) | Указывает день месяца, в который выполняется задача. <br/> |



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

 

 





