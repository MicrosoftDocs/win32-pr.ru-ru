---
title: Простой тип HexInt16Type
description: Определяет 2-байтовый шестнадцатеричный тип.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- Журнал событий простого типа HexInt16Type
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492555"
---
# <a name="hexint16type-simple-type"></a>Простой тип HexInt16Type

Определяет 2-байтовый шестнадцатеричный тип.

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **HexInt16Type** — это **строка** , которая ограничена следующим шаблоном:

-   `0[xX][0-9A-Fa-f]{1,4}`

    Значение может содержать от одного до четырех шестнадцатеричных символов (например, 0xA или 0xac7b).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





