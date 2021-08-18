---
title: Сложный тип Маинтенанцесеттингстипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Маинтенанцесеттингс.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- планировщик задач сложного типа Маинтенанцесеттингстипе
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0733d16ec929b4e67774fc436c1530b67d70392b2655525b2aaaa642c2ea346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139207"
---
# <a name="maintenancesettingstype-complex-type"></a>Сложный тип Маинтенанцесеттингстипе

Определяет дочерние элементы и сведения о последовательности для элемента [**маинтенанцесеттингс**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) .

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                        | Тип    | Описание                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Крайний срок**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | Указывает период времени, по истечении которого планировщик заданий будет пытаться запустить задачу во время аварийного автоматического обслуживания, если это не удалось завершить во время регулярного обслуживания.<br/> |
| **Монопольный доступ**                                                                  | Логическое | Если задано значение true, задача будет запускаться только в других задачах обслуживания.<br/>                                                                                                 |
| [**Период**](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | Указывает, как часто задача должна запускаться во время автоматического обслуживания.<br/>                                                                                                      |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>           |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





