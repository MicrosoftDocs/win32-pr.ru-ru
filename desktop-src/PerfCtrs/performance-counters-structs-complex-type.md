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
ms.openlocfilehash: 0dfa7f72ee537d857f19301aa4df906d94b0bf7ba9e3f7a76bdb6ab82c84dfd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314424"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




