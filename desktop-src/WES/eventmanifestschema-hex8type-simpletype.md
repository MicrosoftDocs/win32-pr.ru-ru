---
title: Простой тип HexInt8Type
description: Определяет 1-байтовый шестнадцатеричный тип.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Журнал событий простого типа HexInt8Type
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493095"
---
# <a name="hexint8type-simple-type"></a>Простой тип HexInt8Type

Определяет 1-байтовый шестнадцатеричный тип.

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **HexInt8Type** — это [строка](/dotnet/api/system.string) , которая ограничена следующим шаблоном:

-   `0[xX][0-9A-Fa-f]{1,2}`

    Значение может содержать от одного до двух шестнадцатеричных символов (например, 0xA или 0xac).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

