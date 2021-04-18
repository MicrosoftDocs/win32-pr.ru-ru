---
description: <searchConnectorDescriptionType>Элемент является контейнером верхнего уровня для определения соединителя поиска.
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7edb69647567b7e18e25e11dcd0fc773d0be7902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692162"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a><span data-ttu-id="692f4-103">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-103">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>

<span data-ttu-id="692f4-104"><searchConnectorDescriptionType>Элемент является контейнером верхнего уровня для определения соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="692f4-104">The <searchConnectorDescriptionType> element is the top level container for the search connector definition.</span></span>

-   [<span data-ttu-id="692f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="692f4-105">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="692f4-106">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="692f4-106">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="692f4-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="692f4-107">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="692f4-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="692f4-108">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="692f4-109">Пример файла описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="692f4-109">Example of a Search Connector Description File</span></span>](#example-of-a-search-connector-description-file)
-   [<span data-ttu-id="692f4-110">См. также</span><span class="sxs-lookup"><span data-stu-id="692f4-110">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="692f4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="692f4-111">Syntax</span></span>


```
<!-- searchConnectorDescriptionType -->
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



## <a name="element-information"></a><span data-ttu-id="692f4-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="692f4-112">Element Information</span></span>



| <span data-ttu-id="692f4-113">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="692f4-113">Parent Element</span></span> | <span data-ttu-id="692f4-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="692f4-114">Child Elements</span></span>                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [<span data-ttu-id="692f4-115">Элемент Иссеарчонлитем (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-115">isSearchOnlyItem Element (Search Connector Schema)</span></span>](search-schema-sconn-issearchonlyitem.md)                           |
|                | [<span data-ttu-id="692f4-116">Элемент Исдефаултсавелокатион (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-116">isDefaultSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [<span data-ttu-id="692f4-117">Элемент Исдефаултноновнерсавелокатион (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-117">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [<span data-ttu-id="692f4-118">Элемент Description (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-118">description Element (Search Connector Schema)</span></span>](search-schema-sconn-description.md)                                     |
|                | [<span data-ttu-id="692f4-119">Элемент Иконреференце (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-119">iconReference Element (Search Connector Schema)</span></span>](search-schema-sconn-iconreference.md)                                 |
|                | [<span data-ttu-id="692f4-120">Элемент Имажелинк (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-120">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md)                                         |
|                | [<span data-ttu-id="692f4-121">Элемент Author (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-121">author Element (Search Connector Schema)</span></span>](search-schema-sconn-author.md)                                               |
|                | [<span data-ttu-id="692f4-122">Элемент dateCreated (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-122">dateCreated Element (Search Connector Schema)</span></span>](search-schema-sconn-datecreated.md)                                     |
|                | [<span data-ttu-id="692f4-123">Элемент Темплатеинфо (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-123">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md)                                   |
|                | [<span data-ttu-id="692f4-124">Элемент Локатионпровидер (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-124">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md)                           |
|                | [<span data-ttu-id="692f4-125">Элемент Scope (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-125">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md)                                                 |
|                | [<span data-ttu-id="692f4-126">Элемент Пропертисторе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-126">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md)                                 |
|                | [<span data-ttu-id="692f4-127">Элемент Инклудеинстартменускопе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-127">includeInStartMenuScope Element (Search Connector Schema)</span></span>](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [<span data-ttu-id="692f4-128">Элемент domain (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-128">domain Element (Search Connector Schema)</span></span>](search-schema-sconn-domain.md)                                               |
|                | [<span data-ttu-id="692f4-129">Элемент Суппортсадванцедкуерисинтакс (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-129">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [<span data-ttu-id="692f4-130">Элемент с индексом (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="692f4-130">isIndexed Element (Search Connector Schema)</span></span>](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a><span data-ttu-id="692f4-131">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="692f4-131">Attributes</span></span>



| <span data-ttu-id="692f4-132">Атрибут</span><span class="sxs-lookup"><span data-stu-id="692f4-132">Attribute</span></span> | <span data-ttu-id="692f4-133">Описание</span><span class="sxs-lookup"><span data-stu-id="692f4-133">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="692f4-134">publisher</span><span class="sxs-lookup"><span data-stu-id="692f4-134">publisher</span></span> | <span data-ttu-id="692f4-135">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="692f4-135">Optional.</span></span> <span data-ttu-id="692f4-136">Отображаемое имя издателя, предоставляющего соединитель поиска.</span><span class="sxs-lookup"><span data-stu-id="692f4-136">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="692f4-137">product</span><span class="sxs-lookup"><span data-stu-id="692f4-137">product</span></span>   | <span data-ttu-id="692f4-138">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="692f4-138">Optional.</span></span> <span data-ttu-id="692f4-139">Отображаемое имя продукта, к которому применяется соединитель поиска.</span><span class="sxs-lookup"><span data-stu-id="692f4-139">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="692f4-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="692f4-140">Remarks</span></span>

<span data-ttu-id="692f4-141">Соединители поиска для федеративного поиска нельзя использовать в библиотеках.</span><span class="sxs-lookup"><span data-stu-id="692f4-141">Search connectors for federated search cannot be used in libraries.</span></span> <span data-ttu-id="692f4-142">Схема соединителей поиска библиотек является расширением схемы, описанной здесь, и содержит сведения, относящиеся к библиотекам.</span><span class="sxs-lookup"><span data-stu-id="692f4-142">The schema for library search connectors is an extension of the schema described here and includes information specific to libraries.</span></span>

## <a name="example-of-a-search-connector-description-file"></a><span data-ttu-id="692f4-143">Пример файла описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="692f4-143">Example of a Search Connector Description File</span></span>

<span data-ttu-id="692f4-144">Ниже приведен пример файла описания соединителя поиска для федеративной веб-службы поиска.</span><span class="sxs-lookup"><span data-stu-id="692f4-144">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



<span data-ttu-id="692f4-145">Ниже приведен пример файла описания соединителя поиска для обработчика протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="692f4-145">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="related-topics"></a><span data-ttu-id="692f4-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="692f4-146">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="692f4-147">**Reference**</span><span class="sxs-lookup"><span data-stu-id="692f4-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="692f4-148">Обзор схемы описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="692f4-148">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="692f4-149">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="692f4-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="692f4-150">Федеративный поиск в Windows</span><span class="sxs-lookup"><span data-stu-id="692f4-150">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> </dl>

 

 



