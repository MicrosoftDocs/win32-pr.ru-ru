---
title: Сложный тип Рестарттипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Рестартонфаилуре.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- планировщик задач сложного типа Рестарттипе
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535495"
---
# <a name="restarttype-complex-type"></a>Сложный тип Рестарттипе

Определяет дочерние элементы и сведения о последовательности для элемента [рестартонфаилуре](taskschedulerschema-restartonfailure-settingstype-element.md) .

``` syntax
<xs:complexType name="restartType">
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
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                              | Тип | Описание                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [**Расчета**](taskschedulerschema-count-restarttype-element.md)       |      | Число попыток перезапуска задачи.<br/> |
| [**Пределах**](taskschedulerschema-interval-restarttype-element.md) |      | Длительность попытки запуска задачи.<br/>      |



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

 

 





