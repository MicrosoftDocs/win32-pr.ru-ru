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
ms.openlocfilehash: 71bdf8b87a641247ce2064ccf44ee861d79aab0593229e4cd7b38035c5c7c124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424434"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Простые типы схемы планировщик задач](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





