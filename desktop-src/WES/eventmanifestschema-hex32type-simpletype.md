---
title: Простой тип HexInt32Type (схема Евентманифест)
description: Определяет 4-байтовый шестнадцатеричный тип. | Простой тип HexInt32Type (схема Евентманифест)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
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
ms.openlocfilehash: 4630bc4d7d513a0fedad2191c63ca71571ce655a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694004"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a>Простой тип HexInt32Type (схема Евентманифест)

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



 

 





