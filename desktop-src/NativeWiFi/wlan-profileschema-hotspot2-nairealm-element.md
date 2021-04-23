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
# <a name="nairealm-hotspot2-element"></a><span data-ttu-id="09118-103">Наиреалм (Hotspot2), элемент</span><span class="sxs-lookup"><span data-stu-id="09118-103">NAIRealm (Hotspot2) Element</span></span>

<span data-ttu-id="09118-104">Список идентификаторов области идентификаторов доступа к сети (наи).</span><span class="sxs-lookup"><span data-stu-id="09118-104">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="09118-105">Записи в этом списке обычно имеют форму `user@domain` .</span><span class="sxs-lookup"><span data-stu-id="09118-105">Entries in this list are usually of the form `user@domain`.</span></span> <span data-ttu-id="09118-106">Список сфер наи является предпочтительным методом для определения большинства немобильных операторов, таких как MSO, операторы вирелине и общедоступные места проведения.</span><span class="sxs-lookup"><span data-stu-id="09118-106">The NAI Realm list is the preferred method to identify most non-mobile operators like MSOs, wireline operators, and public venues.</span></span>

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

<span data-ttu-id="09118-107">Элемент определяется элементом [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="09118-107">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="09118-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="09118-108">Child elements</span></span>



| <span data-ttu-id="09118-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="09118-109">Element</span></span> | <span data-ttu-id="09118-110">Тип</span><span class="sxs-lookup"><span data-stu-id="09118-110">Type</span></span> | <span data-ttu-id="09118-111">Описание</span><span class="sxs-lookup"><span data-stu-id="09118-111">Description</span></span>                                                   |
|---------|------|---------------------------------------------------------------|
| <span data-ttu-id="09118-112">name</span><span class="sxs-lookup"><span data-stu-id="09118-112">name</span></span>    |      | <span data-ttu-id="09118-113">Один идентификатор области.</span><span class="sxs-lookup"><span data-stu-id="09118-113">A single realm identifier.</span></span> <span data-ttu-id="09118-114">Обычно это форма `user@domain` .</span><span class="sxs-lookup"><span data-stu-id="09118-114">Usually of the form `user@domain`.</span></span> |



 

 



