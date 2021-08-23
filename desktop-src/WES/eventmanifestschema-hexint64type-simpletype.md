---
title: Простой тип UInt64Type (схема Евентманифест)
description: Определяет тип long без знака.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- Журнал событий простого типа UInt64Type
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 088cdead48fb62adf816b6065e211afcc994ec618db8b7e9a0597e6f72c1780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511344"
---
# <a name="uint64type-simple-type"></a>Простой тип UInt64Type

Определяет тип long без знака. Значение может быть задано как 8-байтовое целое или шестнадцатеричное значение в диапазоне от 0 до 18446744073709551615.

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





