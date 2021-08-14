---
title: Сложный тип Даилисчедулетипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Счедулебидай.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- планировщик задач сложного типа Даилисчедулетипе
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 881442d4aa6d6b22fb443a2670aac379b39bfed064089b95dd1bd07ba80a1f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357184"
---
# <a name="dailyscheduletype-complex-type"></a>Сложный тип Даилисчедулетипе

Определяет дочерние элементы и сведения о последовательности для элемента [**счедулебидай**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) .

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                            | Тип | Описание                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [**дайсинтервал**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | Указывает интервал между днями в расписании. <br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





