---
title: Простой тип Виктипе
description: Определяет значения, которые могут использоваться в элементе Week.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- планировщик задач простого типа Виктипе
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 923d5a5d672407f9d15fed62bd554853f23ce5b31debd6a7c331e4b1217f15fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757937"
---
# <a name="weektype-simple-type"></a>Простой тип Виктипе

Определяет значения, которые могут использоваться в элементе [**Week**](taskschedulerschema-week-weekstype-element.md) .

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **виктипе** — это **строка** , которая ограничена следующим шаблоном:

-   `[1-4]|Last`

    Указывает первую за четвертую неделю месяца (1-4) или всегда за последнюю неделю месяца.

## <a name="requirements"></a>Требования



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

 

 





