---
description: <searchConnectorDescription>Элемент является элементом контейнера верхнего уровня определения соединителя поиска.
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: Элемент Сеарчконнектордескриптион (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa6c213d43a648ebea51b58b4c3103a0ee42f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985896"
---
# <a name="searchconnectordescription-element-library-schema"></a><span data-ttu-id="a88a3-103">Элемент Сеарчконнектордескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="a88a3-103">searchConnectorDescription Element (Library Schema)</span></span>

<span data-ttu-id="a88a3-104"><searchConnectorDescription>Элемент является элементом контейнера верхнего уровня определения соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="a88a3-104">The <searchConnectorDescription> element is the top level container element of a search connector definition.</span></span> <span data-ttu-id="a88a3-105"><searchConnectorDescription>Элемент является расширением <searchConnectorDescriptionType> типа элемента, связанного с соединителями федеративного поиска Windows, однако в библиотеке нельзя включать соединители поиска для федеративного поиска Windows или обработчиков протоколов.</span><span class="sxs-lookup"><span data-stu-id="a88a3-105">The <searchConnectorDescription> element is an extension of the <searchConnectorDescriptionType> element type associated with Windows Federated Search connectors; however, you cannot include search connectors for Windows Federated Search or protocol handlers in a library.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88a3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a88a3-106">Syntax</span></span>

``` syntax
<!-- searchConnectorDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
   <xs:complexType name="searchConnectorDescriptionType">
      <xs:all>
         <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
         <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/
         <xs:element name="description" type="xs:string" minOccurs="0"/>
         <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
         <xs:element name="imageLink" minOccurs="0">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="url" type="xs:anyURI"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="author" type="xs:string" minOccurs="0"/>
         <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
         <xs:element name="templateInfo" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="folderType" minOccurs="0"/>
               </xs:all>
            </xs:complexType>
         </xs:element>
         <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0"/>
         <xs:element name="locationProvider" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
               </xs:all>
               <xs:attribute name="clsid" use="required"/>
               <xs:attribute name="codebase" type="xs:string"/>
            </xs:complexType>
         </xs:element>
         <xs:element name="scope" minOccurs="0">
            <xs:complexType>
               <xs:sequence minOccurs="0">
                  <xs:element name="scopeItem" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:all>
                           <xs:element name="mode" default="Include">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Include"/>
                                    <xs:enumeration value="Exclude"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="depth" default="Shallow" minOccurs="0">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Shallow"/>
                                    <xs:enumeration value="Deep"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="url" type="xs:anyURI"/>
                        </xs:all>
                     </xs:complexType>
                  </xs:element>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0"/>
         <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="domain" type="xs:string" minOccurs="0"/>
         <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isIndexed" type="xs:boolean" minOccurs="0"/>
      </xs:all>
      <xs:attribute name="publisher" type="xs:string"/>
      <xs:attribute name="product" type="xs:string"/>
   </xs:complexType>
</xs:schema>
```

## <a name="element-information"></a><span data-ttu-id="a88a3-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a88a3-107">Element Information</span></span>

<span data-ttu-id="a88a3-108">См. документацию по схеме в [Windows Search](/previous-versions/bb268030(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a88a3-108">Refer to the schema documentation in [Windows Search](/previous-versions/bb268030(v=msdn.10))</span></span>



| <span data-ttu-id="a88a3-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a88a3-109">Parent Element</span></span>                                                                                               | <span data-ttu-id="a88a3-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a88a3-110">Child Elements</span></span>                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="a88a3-111">Элемент Сеарчконнектордескриптионлист (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="a88a3-111">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md) | <span data-ttu-id="a88a3-112"><Иссеарчонли. TEM></span><span class="sxs-lookup"><span data-stu-id="a88a3-112"><isSearchOnlyI.tem></span></span>             |
|                                                                                                              | <description>                   |
|                                                                                                              | <iconReference>                 |
|                                                                                                              | <imageLink>                     |
|                                                                                                              | <author>                        |
|                                                                                                              | <dateCreated>                   |
|                                                                                                              | <templateInfo>                  |
|                                                                                                              | <locationProvider>              |
|                                                                                                              | <scope>                         |
|                                                                                                              | <propertyStore>                 |
|                                                                                                              | <domain>                        |
|                                                                                                              | <supportsAdvancedQuerySyntax>   |
|                                                                                                              | <isDefaultSaveLocation>         |
|                                                                                                              | <isDefaultNonOwnerSaveLocation> |
|                                                                                                              | <isIndexed>                     |
|                                                                                                              | <simpleLocation>                |
|                                                                                                              | <includeInStartMenu>            |



 

## <a name="attributes"></a><span data-ttu-id="a88a3-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a88a3-113">Attributes</span></span>



| <span data-ttu-id="a88a3-114">Атрибут</span><span class="sxs-lookup"><span data-stu-id="a88a3-114">Attribute</span></span> | <span data-ttu-id="a88a3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a88a3-115">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a88a3-116">publisher</span><span class="sxs-lookup"><span data-stu-id="a88a3-116">publisher</span></span> | <span data-ttu-id="a88a3-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a88a3-117">Optional.</span></span> <span data-ttu-id="a88a3-118">Отображаемое имя издателя, предоставляющего соединитель поиска.</span><span class="sxs-lookup"><span data-stu-id="a88a3-118">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="a88a3-119">product</span><span class="sxs-lookup"><span data-stu-id="a88a3-119">product</span></span>   | <span data-ttu-id="a88a3-120">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a88a3-120">Optional.</span></span> <span data-ttu-id="a88a3-121">Отображаемое имя продукта, к которому применяется соединитель поиска.</span><span class="sxs-lookup"><span data-stu-id="a88a3-121">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a88a3-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="a88a3-122">Remarks</span></span>

<span data-ttu-id="a88a3-123"><searchConnectorDescription>Элемент библиотеки использует то же определение схемы, что и <searchConnectorDescription> для федеративного поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="a88a3-123">The <searchConnectorDescription> element of a library uses the same schema definition as the <searchConnectorDescription> for Windows Federated Search.</span></span> <span data-ttu-id="a88a3-124">Несмотря на то что они используют одни и те же схемы, соединители поиска для федеративного поиска Windows не могут быть добавлены в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="a88a3-124">Although they use the same schemas, search connectors for Windows Federated search cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a88a3-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a88a3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a88a3-126">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="a88a3-126">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="a88a3-127">Схема описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="a88a3-127">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
