---
description: Необязательный <propertyStore> элемент указывает расположение ипропертисторе на основе XML для хранения открытых метаданных для этого соединителя поиска. Этот элемент не имеет атрибутов и только одного дочернего элемента.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Элемент Пропертисторе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f8cda6457de764b00519a81a1134e7eecc8638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808897"
---
# <a name="propertystore-element-search-connector-schema"></a><span data-ttu-id="e3f4e-104">Элемент Пропертисторе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="e3f4e-104">propertyStore Element (Search Connector Schema)</span></span>

<span data-ttu-id="e3f4e-105">Необязательный <propertyStore> элемент указывает расположение ипропертисторе на основе XML для хранения открытых метаданных для этого соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="e3f4e-105">The optional <propertyStore> element specifies the location of an XML-based IPropertyStore to store open metadata for this search connector.</span></span> <span data-ttu-id="e3f4e-106">Этот элемент не имеет атрибутов и только одного дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="e3f4e-106">This element has no attributes and only one child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f4e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3f4e-107">Syntax</span></span>


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="e3f4e-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e3f4e-108">Element Information</span></span>



| <span data-ttu-id="e3f4e-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e3f4e-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="e3f4e-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e3f4e-110">Child Elements</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3f4e-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="e3f4e-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="e3f4e-112">Элемент Property элемента Пропертисторе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="e3f4e-112">property Element of propertyStore (Search Connector Schema)</span></span>](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a><span data-ttu-id="e3f4e-113">Пример</span><span class="sxs-lookup"><span data-stu-id="e3f4e-113">Example</span></span>

<span data-ttu-id="e3f4e-114">В следующем примере показан <propertyStore> элемент с двумя <property> элементами.</span><span class="sxs-lookup"><span data-stu-id="e3f4e-114">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



