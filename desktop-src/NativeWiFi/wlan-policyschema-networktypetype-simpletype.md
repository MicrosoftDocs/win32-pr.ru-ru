---
description: Определяет типы беспроводных сетей.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: Простой тип Нетворктипетипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684230"
---
# <a name="networktypetype-simple-type"></a>Простой тип Нетворктипетипе

Простой тип Нетворктипетипе определяет типы беспроводных сетей. Существует два типа сетей: сети инфраструктуры (ESS) и ad-hoc Network (ИБСС).

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Значения перечисления

Простой тип **нетворктипетипе** определяет следующие значения.



| Значение | Описание |
|-------|-------------|
| ибсс  |             |
| ДИСТАНЦИОН   |             |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




