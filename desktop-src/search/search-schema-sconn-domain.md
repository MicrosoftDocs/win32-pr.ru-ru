---
description: Необязательный <domain> элемент указывает URL-адрес службы поиска, используемой этим соединителем поиска. Он отображается в области сведений. Этот элемент не имеет дочерних элементов и не имеет атрибутов.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Элемент domain (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896914"
---
# <a name="domain-element-search-connector-schema"></a><span data-ttu-id="80ee4-105">Элемент domain (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="80ee4-105">domain Element (Search Connector Schema)</span></span>

<span data-ttu-id="80ee4-106">Необязательный <domain> элемент указывает URL-адрес службы поиска, используемой этим соединителем поиска.</span><span class="sxs-lookup"><span data-stu-id="80ee4-106">The optional <domain> element specifies the URL of the search service used by this search connector.</span></span> <span data-ttu-id="80ee4-107">Он отображается в области сведений.</span><span class="sxs-lookup"><span data-stu-id="80ee4-107">It is displayed in the details pane.</span></span> <span data-ttu-id="80ee4-108">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="80ee4-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="80ee4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80ee4-109">Syntax</span></span>


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="80ee4-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="80ee4-110">Element Information</span></span>



| <span data-ttu-id="80ee4-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="80ee4-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="80ee4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="80ee4-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="80ee4-113">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="80ee4-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="80ee4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80ee4-114">Remarks</span></span>

<span data-ttu-id="80ee4-115">URL-адрес должен быть доменом верхнего уровня для поставщика поиска.</span><span class="sxs-lookup"><span data-stu-id="80ee4-115">The URL should be the top-level domain for the search provider.</span></span> <span data-ttu-id="80ee4-116">Например, https://www.example.com.</span><span class="sxs-lookup"><span data-stu-id="80ee4-116">For example, https://www.example.com.</span></span>

## <a name="example"></a><span data-ttu-id="80ee4-117">Пример</span><span class="sxs-lookup"><span data-stu-id="80ee4-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



