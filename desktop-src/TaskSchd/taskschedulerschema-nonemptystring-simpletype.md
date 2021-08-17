---
title: Простой тип Нонемптистрингтипе
description: Определяет значения, используемые для непустой строки текста.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- планировщик задач простого типа Нонемптистринг
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6359240c2baba14460ab4478c31c490725646130ea2181efdcb8e92a94090d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758420"
---
# <a name="nonemptystringtype-simple-type"></a>Простой тип Нонемптистрингтипе

Определяет значения, используемые для непустой строки текста.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Значения перечисления

Простой тип **нонемптистринг** определяет следующее значение.



| Значение | Описание                                            |
|-------|--------------------------------------------------------|
| 1     | Строка содержит по крайней мере один символ.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





