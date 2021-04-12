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
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415784"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





