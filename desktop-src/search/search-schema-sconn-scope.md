---
description: Необязательный <scope> элемент указывает коллекцию <scopeItem> элементов, определяющих включаемые и исключаемые области для этого конкретного соединителя поиска.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Элемент Scope (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692167"
---
# <a name="scope-element-search-connector-schema"></a><span data-ttu-id="3a03e-103">Элемент Scope (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="3a03e-103">scope Element (Search Connector Schema)</span></span>

<span data-ttu-id="3a03e-104">Необязательный <scope> элемент указывает коллекцию <scopeItem> элементов, определяющих включаемые и исключаемые области для этого конкретного соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="3a03e-104">The optional <scope> element specifies a collection of <scopeItem> elements that define the scope inclusions and exclusions for this particular search connector.</span></span> <span data-ttu-id="3a03e-105">Если имеется <scope> , то он должен содержать хотя бы один <scopeItem> элемент.</span><span class="sxs-lookup"><span data-stu-id="3a03e-105">If <scope> is present, it MUST contain at least one <scopeItem> element.</span></span> <span data-ttu-id="3a03e-106">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="3a03e-106">This element has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a03e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a03e-107">Syntax</span></span>


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="3a03e-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3a03e-108">Element Information</span></span>



| <span data-ttu-id="3a03e-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="3a03e-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="3a03e-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3a03e-110">Child Elements</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="3a03e-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="3a03e-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | <span data-ttu-id="3a03e-112">[элемент скопеитем (схема соединителя поиска)](search-schema-sconn-scopeitem.md).</span><span class="sxs-lookup"><span data-stu-id="3a03e-112">[scopeItem Element (Search Connector Schema)](search-schema-sconn-scopeitem.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3a03e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a03e-113">Remarks</span></span>

<span data-ttu-id="3a03e-114">Используйте <scope> элементы и, <scopeItem> чтобы указать, какие расположения следует искать, и какие расположения следует исключить из поиска.</span><span class="sxs-lookup"><span data-stu-id="3a03e-114">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="3a03e-115">Пример</span><span class="sxs-lookup"><span data-stu-id="3a03e-115">Example</span></span>

<span data-ttu-id="3a03e-116">В следующем примере показана область поиска, включающая в себя C: \\ ексамплефолдер и все ее дочерние папки, кроме c: \\ ексамплефолдер \\ ексклудеме.</span><span class="sxs-lookup"><span data-stu-id="3a03e-116">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



