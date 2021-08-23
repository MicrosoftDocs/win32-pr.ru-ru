---
description: Список идентификаторов области идентификаторов доступа к сети (наи).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: Наиреалм (Hotspot2), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 084ee3ce04a560ce50c3ab0391f808bc09aed1bb90da6a34b86755b9b64ae772
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684214"
---
# <a name="nairealm-hotspot2-element"></a>Наиреалм (Hotspot2), элемент

Список идентификаторов области идентификаторов доступа к сети (наи). Записи в этом списке обычно имеют форму `user@domain` . Список сфер наи является предпочтительным методом для определения большинства немобильных операторов, таких как MSO, операторы вирелине и общедоступные места проведения.

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент определяется элементом [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент | Тип | Описание                                                   |
|---------|------|---------------------------------------------------------------|
| name    |      | Один идентификатор области. Обычно это форма `user@domain` . |



 

 



