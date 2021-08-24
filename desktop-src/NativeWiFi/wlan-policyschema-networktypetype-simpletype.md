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
ms.openlocfilehash: 40184bb027f80826baa3ad56090755a2cd9ec630f9eb105e402d30a6ecf2661c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800114"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




