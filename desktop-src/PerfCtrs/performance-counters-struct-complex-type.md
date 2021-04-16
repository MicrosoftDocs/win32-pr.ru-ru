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
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663178"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




