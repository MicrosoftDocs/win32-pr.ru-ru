---
title: Простой тип Каунттипе
description: Определяет тип счетчика, который используется для указания количества элементов в массиве.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Журнал событий простого типа Каунттипе
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804030"
---
# <a name="counttype-simple-type"></a>Простой тип Каунттипе

Определяет тип счетчика, который используется для указания количества элементов в массиве. Значение может быть указано в виде значения xs: Унсигнедшорт или в виде строки, которая ссылается на имя узла элемента данных, содержащего короткое значение унсижед.

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





