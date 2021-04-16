---
description: Список уникальных идентификаторов (OUI), назначенных IEEE.
ms.assetid: 4a9885b6-2e57-4a16-8e1d-b5b0797e09db
title: Роамингконсортиум (Hotspot2), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RoamingConsortium
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5e53fa274cbc56de6be026ef0e466ec501cf9124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683036"
---
# <a name="roamingconsortium-hotspot2-element"></a>Роамингконсортиум (Hotspot2), элемент

Список уникальных идентификаторов (OUI), назначенных IEEE.

``` syntax
<xs:element name="RoamingConsortium"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:minLength
                            value="3"
                         />
                        <xs:maxLength
                            value="5"
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



| Элемент | Тип | Описание                                                               |
|---------|------|---------------------------------------------------------------------------|
| КОДОМ     |      | Один OUI, отформатированный как шестнадцатеричное число с переменным размером.<br/> |



 

 




