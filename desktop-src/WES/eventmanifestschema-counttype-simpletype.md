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
ms.openlocfilehash: 63476d70a9bb5b336449a65707664c05c56a20b4c2c9fa4888c0c3125f129d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863624"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





