---
description: Необязательный &lt; &gt; элемент пропертисторе указывает расположение ипропертисторе на основе XML для хранения открытых метаданных для этого соединителя поиска. Этот элемент не имеет атрибутов и только одного дочернего элемента.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Элемент Пропертисторе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c617f560e0471062064bcec8020dd5e6efa026
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886801"
---
# <a name="propertystore-element-search-connector-schema"></a>Элемент Пропертисторе (схема соединителя поиска)

Необязательный &lt; &gt; элемент пропертисторе указывает расположение ипропертисторе на основе XML для хранения открытых метаданных для этого соединителя поиска. Этот элемент не имеет атрибутов и только одного дочернего элемента.

## <a name="syntax"></a>Синтаксис


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



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                                                   | Дочерние элементы                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)](search-schema-searchconnectordescription.md) | [Элемент Property элемента Пропертисторе (схема соединителя поиска)](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>Пример

В следующем примере показан &lt; элемент пропертисторе &gt; с двумя &lt; элементами свойств &gt; .


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



