---
description: '&lt;Элемент сеарчконнектордескриптионтипе &gt; является контейнером верхнего уровня для определения соединителя поиска.'
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f89621ab34f65fb3c3b1f8e88bbdc8dca246b8d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885077"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a>Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)

&lt;Элемент сеарчконнектордескриптионтипе &gt; является контейнером верхнего уровня для определения соединителя поиска.

-   [Синтаксис](#syntax)
-   [Сведения об элементе](#element-information)
-   [Атрибуты](#attributes)
-   [Замечания](#remarks)
-   [Пример файла описания соединителя поиска](#example-of-a-search-connector-description-file)
-   [См. также](#related-topics)

## <a name="syntax"></a>Синтаксис


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



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент | Дочерние элементы                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [Элемент Иссеарчонлитем (схема соединителя поиска)](search-schema-sconn-issearchonlyitem.md)                           |
|                | [Элемент Исдефаултсавелокатион (схема соединителя поиска)](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [Элемент Исдефаултноновнерсавелокатион (схема соединителя поиска)](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [Элемент Description (схема соединителя поиска)](search-schema-sconn-description.md)                                     |
|                | [Элемент Иконреференце (схема соединителя поиска)](search-schema-sconn-iconreference.md)                                 |
|                | [Элемент Имажелинк (схема соединителя поиска)](search-schema-sconn-imagelink.md)                                         |
|                | [Элемент Author (схема соединителя поиска)](search-schema-sconn-author.md)                                               |
|                | [Элемент dateCreated (схема соединителя поиска)](search-schema-sconn-datecreated.md)                                     |
|                | [Элемент Темплатеинфо (схема соединителя поиска)](search-schema-sconn-templateinfo.md)                                   |
|                | [Элемент Локатионпровидер (схема соединителя поиска)](search-schema-sconn-locationprovider.md)                           |
|                | [Элемент Scope (схема соединителя поиска)](search-schema-sconn-scope.md)                                                 |
|                | [Элемент Пропертисторе (схема соединителя поиска)](search-schema-sconn-propertystore.md)                                 |
|                | [Элемент Инклудеинстартменускопе (схема соединителя поиска)](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [Элемент domain (схема соединителя поиска)](search-schema-sconn-domain.md)                                               |
|                | [Элемент Суппортсадванцедкуерисинтакс (схема соединителя поиска)](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [Элемент с индексом (схема соединителя поиска)](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a>Атрибуты



| Атрибут | Описание                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | Необязательный элемент. Отображаемое имя издателя, предоставляющего соединитель поиска.      |
| product   | Необязательный элемент. Отображаемое имя продукта, к которому применяется соединитель поиска. |



 

## <a name="remarks"></a>Комментарии

Соединители поиска для федеративного поиска нельзя использовать в библиотеках. Схема соединителей поиска библиотек является расширением схемы, описанной здесь, и содержит сведения, относящиеся к библиотекам.

## <a name="example-of-a-search-connector-description-file"></a>Пример файла описания соединителя поиска

Ниже приведен пример файла описания соединителя поиска для федеративной веб-службы поиска.


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



Ниже приведен пример файла описания соединителя поиска для обработчика протокола MAPI.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Обзор схемы описания соединителя поиска](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Федеративный поиск в Windows](-search-federated-search-overview.md)
</dt> </dl>

 

 



