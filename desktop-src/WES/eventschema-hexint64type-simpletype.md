---
title: Простой тип HexInt64Type (схема события)
description: Определяет 8-байтовый шестнадцатеричный тип. | Простой тип HexInt64Type (схема события)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- Журнал событий простого типа HexInt64Type
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694044"
---
# <a name="hexint64type-simple-type-event-schema"></a>Простой тип HexInt64Type (схема события)

Определяет 8-байтовый шестнадцатеричный тип.

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **HexInt64Type** — это **строка** , которая ограничена следующим шаблоном:

-   `0[xX][0-9A-Fa-f]{1,16}`

    Значение может содержать от одного до шестнадцати шестнадцатеричных символов (например, 0xA или 0xac7bd361004fe190).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





