---
title: Простой тип Дайофмонстипе
description: Определяет возможные значения для указания дня месяца.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- планировщик задач простого типа Дайофмонстипе
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c3d3d549f2d84c292ad1dbdf3c03965bd6e4265559b57c41016811834167a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309359"
---
# <a name="dayofmonthtype-simple-type"></a>Простой тип Дайофмонстипе

Определяет возможные значения для указания дня месяца.

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **дайофмонстипе** — это **строка** , которая ограничена следующим шаблоном:

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    Указывает первый из 31-дневного дня месяца или всегда последний день месяца.

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

 

 





