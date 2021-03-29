---
title: Сложный тип Буттригжертипе
description: Определяет дочерний элемент и сведения о последовательности для элемента Буттригжер.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- планировщик задач сложного типа Буттригжертипе
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492084"
---
# <a name="boottriggertype-complex-type"></a>Сложный тип Буттригжертипе

Определяет дочерний элемент и сведения о последовательности для элемента [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="bootTriggerType">
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



| Элемент                                                            | Тип     | Описание                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [**Задержка**](taskschedulerschema-delay-boottriggertype-element.md) | длительность | Промежуток времени между загрузкой системы и срабатыванием триггера. <br/> |



## <a name="remarks"></a>Комментарии

Помимо дочернего элемента, определенного здесь, элемент [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





