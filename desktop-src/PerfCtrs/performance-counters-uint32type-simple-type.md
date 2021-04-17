---
description: Определяет целочисленный тип без знака.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Простой тип UInt32Type (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663173"
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

## <a name="remarks"></a>Комментарии

Значение можно указать в виде 4-байтового целого или шестнадцатеричного значения в диапазоне от 0 до 4 294 967 295.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




