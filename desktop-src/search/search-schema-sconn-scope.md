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
# <a name="scope-element-search-connector-schema"></a>Элемент Scope (схема соединителя поиска)

Необязательный <scope> элемент указывает коллекцию <scopeItem> элементов, определяющих включаемые и исключаемые области для этого конкретного соединителя поиска. Если имеется <scope> , то он должен содержать хотя бы один <scopeItem> элемент. Этот элемент не содержит атрибуты.

## <a name="syntax"></a>Синтаксис


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



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                                                   | Дочерние элементы                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)](search-schema-searchconnectordescription.md) | [элемент скопеитем (схема соединителя поиска)](search-schema-sconn-scopeitem.md). |



 

## <a name="remarks"></a>Комментарии

Используйте <scope> элементы и, <scopeItem> чтобы указать, какие расположения следует искать, и какие расположения следует исключить из поиска.

## <a name="example"></a>Пример

В следующем примере показана область поиска, включающая в себя C: \\ ексамплефолдер и все ее дочерние папки, кроме c: \\ ексамплефолдер \\ ексклудеме.


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



 

 



