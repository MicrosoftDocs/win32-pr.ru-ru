---
title: Сложный тип Регистратионтригжертипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Регистратионтригжер.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- планировщик задач сложного типа Регистратионтригжертипе
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415873"
---
# <a name="registrationtriggertype-complex-type"></a>Сложный тип Регистратионтригжертипе

Определяет дочерние элементы и сведения о последовательности для элемента [**регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="registrationTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                    | Тип     | Описание                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [**Задержка**](taskschedulerschema-delay-registrationtriggertype-element.md) | длительность | Указывает промежуток времени между регистрацией задачи и началом задачи.<br/> |



## <a name="remarks"></a>Комментарии

Помимо дочерних элементов, определенных здесь, элемент [**регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





