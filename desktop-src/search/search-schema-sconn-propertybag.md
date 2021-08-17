---
description: Обязательный <propertyBag> элемент указывает набор из одного или нескольких свойств, используемых этим поставщиком расположения.
ms.assetid: 63f8f2e4-3b52-4d6e-8d3a-2e133aac0e86
title: Элемент propertyBag (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a8b888ba57fd71c892c61bc8b3f29a8ebc7f9e240162d0ecf6b3bbff41d2e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226484"
---
# <a name="propertybag-element-search-connector-schema"></a>Элемент propertyBag (схема соединителя поиска)

Обязательный <propertyBag> элемент указывает набор из одного или нескольких свойств, используемых этим поставщиком расположения.

## <a name="syntax"></a>Синтаксис


```
<!-- propertyBag -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
                            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
                        </xs:element>
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



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                                 | Дочерние элементы                                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Элемент Локатионпровидер (схема соединителя поиска)](search-schema-sconn-locationprovider.md) | [Элемент Property (схема соединителя поиска)](search-schema-sconn-locationproviderproperty.md) |



 

## <a name="example-of-a-propertybag-element-and-property-elements"></a>Пример элемента PropertyBag и элементов свойств


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



