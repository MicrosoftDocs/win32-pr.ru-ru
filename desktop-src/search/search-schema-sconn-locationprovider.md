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
# <a name="locationprovider-element-search-connector-schema"></a>Элемент Локатионпровидер (схема соединителя поиска)

Необязательный <locationProvider> элемент указывает поставщика поиска, который будет использоваться соединителем поиска поставщика веб-службы. Этот элемент содержит один обязательный атрибут и необязательный дочерний элемент.

## <a name="syntax"></a>Синтаксис


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



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                                                   | Дочерние элементы                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)](search-schema-searchconnectordescription.md) | [Элемент propertyBag (схема соединителя поиска)](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>Атрибуты



| Атрибут | Описание                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | Обязательный. Идентификатор класса (CLSID) поставщика поиска. |
| codebase  | Необязательный элемент.                                                      |



 

## <a name="remarks"></a>Комментарии

@clsidЗначение атрибута для поставщика OpenSearch — {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.

Соединители поиска на основе файловой системы и обработчика протокола могут использовать [<simpleLocation>](search-schema-sconn-simplelocation.md) элемент. Если <locationProvider> присутствует, <simpleLocation> в описании СОЕДИНИТЕЛЯ поиска не должен быть элемент.

## <a name="example-of-a-locationprovider-element"></a>Пример элемента Локатионпровидер


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



