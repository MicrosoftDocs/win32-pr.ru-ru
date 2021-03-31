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
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071578"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





