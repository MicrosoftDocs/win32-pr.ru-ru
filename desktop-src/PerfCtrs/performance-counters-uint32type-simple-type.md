---
description: Простой тип UInt32Type (счетчики производительности) — определяет целочисленный тип без знака.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Простой тип UInt32Type (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114582"
---
# <a name="uint32type-simple-type-performance-counters"></a>Простой тип UInt32Type (счетчики производительности)

Определяет целочисленный тип без знака.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Remarks

Значение можно указать в виде 4-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 4 294 967 295.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




