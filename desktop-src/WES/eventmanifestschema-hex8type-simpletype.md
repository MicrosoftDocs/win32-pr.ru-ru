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
ms.openlocfilehash: 9d2d70b7258317f16ac4e134f011a85218fa1b63aa768136f68b1d21c901856e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121010"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

