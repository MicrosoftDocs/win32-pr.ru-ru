---
title: Простой тип Приорититипе
description: Определяет минимальное и максимальное значения для элемента Priority (Сеттингстипе).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- планировщик задач простого типа Приорититипе
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071867"
---
# <a name="prioritytype-simple-type"></a>Простой тип Приорититипе

Определяет минимальное и максимальное значения для элемента [**Priority (сеттингстипе)**](taskschedulerschema-priority-settingstype-element.md) .

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Значения перечисления

Простой тип **приорититипе** определяет следующие значения.



| Значение | Описание                         |
|-------|-------------------------------------|
| 0     | Минимальное допустимое целое число.<br/> |
| 10    | Максимально допустимое целое число.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Простые типы схемы планировщик задач](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





