---
title: Сложный тип Репетитионтипе
description: Определяет дочерние элементы и сведения о последовательности для элемента повторения (Тригжербасетипе).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- планировщик задач сложного типа Репетитионтипе
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa9ee8c08a79f5db053b772c86929f98a72f011c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415872"
---
# <a name="repetitiontype-complex-type"></a>Сложный тип Репетитионтипе

Определяет дочерние элементы и сведения о последовательности для элемента [**повторения (тригжербасетипе)**](taskschedulerschema-repetition-triggerbasetype-element.md) .

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Duration"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                   | Тип    | Описание                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [**Длительность**](taskschedulerschema-duration-repetitiontype-element.md)                   |         | Указывает, как долго шаблон повторяется. Если значение не указано, шаблон повторяется бесконечно.<br/> |
| [**Пределах**](taskschedulerschema-interval-repetitiontype-element.md)                   |         | Задает интервал времени между перезапусками задачи.<br/>                                              |
| [**стопатдуратионенд**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | Логическое | Указывает, что выполняющийся экземпляр задачи останавливается в конце срока действия шаблона повторения.<br/>     |



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

 

 





