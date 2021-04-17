---
description: Определяет строковый тип для имени или описания профиля политики беспроводной локальной сети.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Простой тип Наметипе (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674297"
---
# <a name="nametype-simple-type-lan_policy"></a>Простой тип Наметипе (LAN_policy)

Простой тип Наметипе определяет строковый тип для имени или описания профиля политики беспроводной локальной сети. Имена и описания — это строки длиной не менее одного символа и не более 255 символов.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




