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
ms.openlocfilehash: 92eafff1be2c1dc924a7041ad45cadfca994d03d776f61a3c866d6c3c2f6f380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033384"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




