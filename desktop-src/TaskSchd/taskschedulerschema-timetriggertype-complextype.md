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
ms.openlocfilehash: 8ca21464df967ff473a767e814b9ce6969a56c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672528"
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
| [**рандомделай**](taskschedulerschema-randomdelay-timetriggertype-element.md) | длительность | Указывает время задержки, которое добавляется случайным образом к времени начала триггера. Формат этой строки — P <days> DT <hours> H <minutes> <seconds> S (например, P2DT5S — 2 дня, задержка 5 секунд). <br/> |



## <a name="remarks"></a>Комментарии

Обратите внимание, что этот элемент не добавляет никаких дочерних элементов к элементам, определенным сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





