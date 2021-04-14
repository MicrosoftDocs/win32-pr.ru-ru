---
title: Простой тип HexInt64Type
description: Определяет 8-байтовый шестнадцатеричный тип. | Простой тип HexInt64Type
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
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
ms.openlocfilehash: 8947e594bb067140510b0b5d2046a898018a291e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424209"
---
# <a name="hexint64type-simple-type"></a>Простой тип HexInt64Type

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

Простой тип **HexInt64Type** — это [строка](/dotnet/api/system.string) , которая ограничена следующим шаблоном:

-   `0[xX][0-9A-Fa-f]{1,16}`

    Значение может содержать от одного до шестнадцати шестнадцатеричных символов (например, 0xA или 0xac7bd361004fe190).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

