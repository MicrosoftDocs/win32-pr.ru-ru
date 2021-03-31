---
title: Простой тип UInt16Type
description: Определяет короткий тип без знака.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- Журнал событий простого типа UInt16Type
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e687f42a43a12266267a0531ce078e8c6b5d1031
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803574"
---
# <a name="uint16type-simple-type"></a>Простой тип UInt16Type

Определяет короткий тип без знака. Значение может быть задано в виде 2-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 65 535.

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





