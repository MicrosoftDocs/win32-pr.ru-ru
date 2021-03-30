---
title: Простой тип UInt32Type (журнал событий Windows)
description: Определяет целочисленный тип без знака.
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- Журнал событий простого типа UInt32Type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2a24326197c72b08032f5144fea1a69fbe68089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988605"
---
# <a name="uint32type-simple-type-windows-event-log"></a>Простой тип UInt32Type (журнал событий Windows)

Определяет целочисленный тип без знака. Значение может быть указано в виде 4-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 4 294 967 295.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





