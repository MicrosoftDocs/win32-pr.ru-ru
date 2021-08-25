---
title: Сложный тип Логонтригжертипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Логонтригжер.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- планировщик задач сложного типа Логонтригжертипе
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85cbbeaa5d911b1ef9677c79980167a66cdf410c7aa63597b02b007795dfbd81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991215"
---
# <a name="logontriggertype-complex-type"></a>Сложный тип Логонтригжертипе

Определяет дочерние элементы и сведения о последовательности для элемента [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
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



| Элемент                                                               | Тип                                                                    | Описание                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Задержка**](taskschedulerschema-delay-logontriggertype-element.md)   | длительность                                                                | Промежуток времени между входом пользователя в систему и запуском задачи.<br/>         |
| [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md) | Идентификатор пользователя. Задача запускается, когда пользователь входит в систему на компьютере.<br/> |



## <a name="remarks"></a>Remarks

Помимо дочерних элементов, определенных здесь, элемент [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="requirements"></a>Требования



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

 

 





