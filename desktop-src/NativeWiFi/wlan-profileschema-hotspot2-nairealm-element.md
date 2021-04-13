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
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543746"
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



 

 



