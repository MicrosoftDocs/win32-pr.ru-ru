---
title: Сложный тип Тригжерстипе
description: Определяет группу (Тригжерграуп) для всех элементов Trigger.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- планировщик задач сложного типа Тригжерстипе
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682127"
---
# <a name="triggerstype-complex-type"></a>Сложный тип Тригжерстипе

Определяет группу ([**тригжерграуп**](taskschedulerschema-triggergroup-group.md)) для всех элементов Trigger. Группа [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) содержит список триггеров, которые можно использовать в задаче.

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





