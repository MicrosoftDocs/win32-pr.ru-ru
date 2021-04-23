---
description: Необязательный <locationProvider> элемент указывает поставщика поиска, который будет использоваться соединителем поиска поставщика веб-службы. Этот элемент содержит один обязательный атрибут и необязательный дочерний элемент.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Элемент Локатионпровидер (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701379"
---
# <a name="locationprovider-element-search-connector-schema"></a><span data-ttu-id="00377-104">Элемент Локатионпровидер (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="00377-104">locationProvider Element (Search Connector Schema)</span></span>

<span data-ttu-id="00377-105">Необязательный <locationProvider> элемент указывает поставщика поиска, который будет использоваться соединителем поиска поставщика веб-службы.</span><span class="sxs-lookup"><span data-stu-id="00377-105">The optional <locationProvider> element specifies the search provider to be used by the web service provider search connector.</span></span> <span data-ttu-id="00377-106">Этот элемент содержит один обязательный атрибут и необязательный дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="00377-106">This element contains one mandatory attribute and an optional child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="00377-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00377-107">Syntax</span></span>


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="00377-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="00377-108">Element Information</span></span>



| <span data-ttu-id="00377-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="00377-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="00377-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="00377-110">Child Elements</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="00377-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="00377-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="00377-112">Элемент propertyBag (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="00377-112">propertyBag Element (Search Connector Schema)</span></span>](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a><span data-ttu-id="00377-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="00377-113">Attributes</span></span>



| <span data-ttu-id="00377-114">Атрибут</span><span class="sxs-lookup"><span data-stu-id="00377-114">Attribute</span></span> | <span data-ttu-id="00377-115">Описание</span><span class="sxs-lookup"><span data-stu-id="00377-115">Description</span></span>                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | <span data-ttu-id="00377-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="00377-116">Required.</span></span> <span data-ttu-id="00377-117">Идентификатор класса (CLSID) поставщика поиска.</span><span class="sxs-lookup"><span data-stu-id="00377-117">The class identifier (CLSID) of the search provider.</span></span> |
| <span data-ttu-id="00377-118">codebase</span><span class="sxs-lookup"><span data-stu-id="00377-118">codebase</span></span>  | <span data-ttu-id="00377-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00377-119">Optional.</span></span>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="00377-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00377-120">Remarks</span></span>

<span data-ttu-id="00377-121">@clsidЗначение атрибута для поставщика OpenSearch — {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span><span class="sxs-lookup"><span data-stu-id="00377-121">The @clsid attribute value for the OpenSearch provider is {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span></span>

<span data-ttu-id="00377-122">Соединители поиска на основе файловой системы и обработчика протокола могут использовать [<simpleLocation>](search-schema-sconn-simplelocation.md) элемент.</span><span class="sxs-lookup"><span data-stu-id="00377-122">File system and protocol handler based search connectors can use the [<simpleLocation>](search-schema-sconn-simplelocation.md) element instead.</span></span> <span data-ttu-id="00377-123">Если <locationProvider> присутствует, <simpleLocation> в описании СОЕДИНИТЕЛЯ поиска не должен быть элемент.</span><span class="sxs-lookup"><span data-stu-id="00377-123">If <locationProvider> is present, there MUST NOT be a <simpleLocation> element in the Search Connector description.</span></span>

## <a name="example-of-a-locationprovider-element"></a><span data-ttu-id="00377-124">Пример элемента Локатионпровидер</span><span class="sxs-lookup"><span data-stu-id="00377-124">Example of a locationProvider Element</span></span>


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



