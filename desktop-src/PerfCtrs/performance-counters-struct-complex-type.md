---
description: Определяет структуру, содержащую один или несколько значений счетчиков.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Сложный тип struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29796a259810cd03739c45338709966bd765f0c1fd9026777f435acb2c5de253
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978854"
---
# <a name="struct-complex-type"></a>Сложный тип struct

Определяет структуру, содержащую один или несколько значений счетчиков.

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



| Имя | Тип                                                                    | Описание                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| name | [**мужчина: Ксимболтипе**](performance-counters-csymboltype-simple-type.md) | Имя структуры.<br/>                                                                                                            |
| тип | [**мужчина: Ксимболтипе**](performance-counters-csymboltype-simple-type.md) | Символьное имя, идентифицирующее структуру. Средство [КТРПП](ctrpp.md) создает переменную структуры с таким именем, которую можно использовать.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




