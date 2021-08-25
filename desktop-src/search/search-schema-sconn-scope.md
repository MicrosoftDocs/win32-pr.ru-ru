---
description: Необязательный <scope> элемент указывает коллекцию <scopeItem> элементов, определяющих включаемые и исключаемые области для этого конкретного соединителя поиска.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Элемент Scope (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d5fcdb3908f495d07199c61a2005a4f97ba5a01c641fb4e854961489e7abe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944304"
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



 

## <a name="remarks"></a>Remarks

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



 

 



