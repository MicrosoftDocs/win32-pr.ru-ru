---
title: Сложный тип Тиметригжертипе
description: Определяет базовый тип для элемента Тиметригжер.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- планировщик задач сложного типа Тиметригжертипе
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c03ede1b87f3969d12256df16c0b05c109391876a12c256190966c8befc7f2fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355752"
---
# <a name="timetriggertype-complex-type"></a>Сложный тип Тиметригжертипе

Определяет базовый тип для элемента [**тиметригжер**](taskschedulerschema-timetrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                        | Тип     | Описание                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**рандомделай**](taskschedulerschema-randomdelay-timetriggertype-element.md) | длительность | Указывает время задержки, которое добавляется случайным образом к времени начала триггера. Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, P2DT5S имеет 2 дня, 5 секунд задержки). <br/> |



## <a name="remarks"></a>Remarks

Обратите внимание, что этот элемент не добавляет никаких дочерних элементов к элементам, определенным сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





