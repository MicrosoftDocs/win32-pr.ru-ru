---
description: Определяет список структур, содержащих значения счетчиков.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Составной тип структур
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663175"
---
# <a name="structs-complex-type"></a>Составной тип структур

Определяет список структур, содержащих значения счетчиков.

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент    | Тип                                                           | Описание                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **struct** | [**Man: структура**](performance-counters-struct-complex-type.md) | Имя структуры, содержащей значения счетчика.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




