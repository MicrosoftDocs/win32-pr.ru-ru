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
ms.openlocfilehash: 6c78a101ec9854b8820b7c9170ea43f06258528de9fdc9d4b02bb41945ba3a7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248104"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





