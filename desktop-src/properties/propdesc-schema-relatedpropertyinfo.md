---
description: Новые для Windows 7. Элемент container для элементов relatedProperty.
ms.assetid: F8BAAE5C-A7EA-487a-B829-91A27E24B58D
title: релатедпропертинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 442de657bed7e97f74064c39cc0934c65a6f520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662759"
---
# <a name="relatedpropertyinfo"></a><span data-ttu-id="6e682-104">релатедпропертинфо</span><span class="sxs-lookup"><span data-stu-id="6e682-104">relatedPropertyInfo</span></span>

<span data-ttu-id="6e682-105">Новые для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6e682-105">New for Windows 7.</span></span> <span data-ttu-id="6e682-106">Элемент container для элементов [relatedProperty](./propdesc-schema-relatedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="6e682-106">Container element for [relatedProperty](./propdesc-schema-relatedproperty.md) elements.</span></span> <span data-ttu-id="6e682-107">Для каждого элемента [пропертидескриптион](./propdesc-schema-propertydescription.md) должен быть только один элемент [релатедпропертинфо]() .</span><span class="sxs-lookup"><span data-stu-id="6e682-107">There should be only one [relatedPropertyInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e682-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e682-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedPropertyInfo">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
                    <xs:attribute name="propertyName" type="canonical-name" use="required"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:unique name="No_two_relatedProperties_can_have_the_same_relationship_name">
        <xs:selector xpath="s:relatedProperty"/>
        <xs:field    xpath="@relationshipName"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="6e682-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6e682-109">Element Information</span></span>



| <span data-ttu-id="6e682-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="6e682-110">Parent Element</span></span>                                                   | <span data-ttu-id="6e682-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6e682-111">Child Elements</span></span>                                           |
|------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="6e682-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="6e682-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="6e682-113">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="6e682-113">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md) |



 

## <a name="attributes"></a><span data-ttu-id="6e682-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6e682-114">Attributes</span></span>

<span data-ttu-id="6e682-115">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="6e682-115">This element has no attributes.</span></span>

 

 
