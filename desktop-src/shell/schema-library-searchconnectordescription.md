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
# <a name="searchconnectordescription-element-library-schema"></a>Элемент Сеарчконнектордескриптион (схема библиотеки)

<searchConnectorDescription>Элемент является элементом контейнера верхнего уровня определения соединителя поиска. <searchConnectorDescription>Элемент является расширением <searchConnectorDescriptionType> типа элемента, связанного с соединителями федеративного поиска Windows, однако в библиотеке нельзя включать соединители поиска для федеративного поиска Windows или обработчиков протоколов.

## <a name="syntax"></a>Синтаксис

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

## <a name="element-information"></a>Сведения об элементе

См. документацию по схеме в [Windows Search](/previous-versions/bb268030(v=msdn.10)) .



| Родительский элемент                                                                                               | Дочерние элементы                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [Элемент Сеарчконнектордескриптионлист (схема библиотеки)](schema-library-searchconnectordescriptionlist.md) | <Иссеарчонли. TEM>             |
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



 

## <a name="attributes"></a>Атрибуты



| Атрибут | Описание                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | Необязательный параметр. Отображаемое имя издателя, предоставляющего соединитель поиска.      |
| product   | Необязательный параметр. Отображаемое имя продукта, к которому применяется соединитель поиска. |



 

## <a name="remarks"></a>Примечания

<searchConnectorDescription>Элемент библиотеки использует то же определение схемы, что и <searchConnectorDescription> для федеративного поиска Windows. Несмотря на то что они используют одни и те же схемы, соединители поиска для федеративного поиска Windows не могут быть добавлены в библиотеку.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Схема описания библиотеки](library-schema-entry.md)
</dt> <dt>

[Схема описания соединителя поиска](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
