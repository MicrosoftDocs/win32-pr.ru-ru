---
title: Простой тип HexInt32Type (схема события)
description: Определяет 4-байтовый шестнадцатеричный тип. | Простой тип HexInt32Type (схема события)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
keywords:
- Журнал событий простого типа HexInt32Type
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000132"
---
# <a name="hexint32type-simple-type-event-schema"></a>Простой тип HexInt32Type (схема события)

Определяет 4-байтовый шестнадцатеричный тип.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Шаблоны

Простой тип **HexInt32Type** — это **строка** , которая ограничена следующим шаблоном:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Значение может содержать от одного до восьми шестнадцатеричных символов (например, 0xA или 0xac7bd361).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





