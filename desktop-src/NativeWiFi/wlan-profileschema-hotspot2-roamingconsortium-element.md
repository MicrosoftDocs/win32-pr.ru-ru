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
# <a name="roamingconsortium-hotspot2-element"></a><span data-ttu-id="6d25e-103">Роамингконсортиум (Hotspot2), элемент</span><span class="sxs-lookup"><span data-stu-id="6d25e-103">RoamingConsortium (Hotspot2) Element</span></span>

<span data-ttu-id="6d25e-104">Список уникальных идентификаторов (OUI), назначенных IEEE.</span><span class="sxs-lookup"><span data-stu-id="6d25e-104">A list of Organizationally Unique Identifiers (OUI) assigned by IEEE.</span></span>

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

<span data-ttu-id="6d25e-105">Элемент определяется элементом [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6d25e-105">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6d25e-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6d25e-106">Child elements</span></span>



| <span data-ttu-id="6d25e-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="6d25e-107">Element</span></span> | <span data-ttu-id="6d25e-108">Тип</span><span class="sxs-lookup"><span data-stu-id="6d25e-108">Type</span></span> | <span data-ttu-id="6d25e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6d25e-109">Description</span></span>                                                               |
|---------|------|---------------------------------------------------------------------------|
| <span data-ttu-id="6d25e-110">КОДОМ</span><span class="sxs-lookup"><span data-stu-id="6d25e-110">OUI</span></span>     |      | <span data-ttu-id="6d25e-111">Один OUI, отформатированный как шестнадцатеричное число с переменным размером.</span><span class="sxs-lookup"><span data-stu-id="6d25e-111">A single OUI, formatted as a variable size hexadecimal number.</span></span><br/> |



 

 




