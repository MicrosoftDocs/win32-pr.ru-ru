---
description: Необязательный &lt; &gt; элемент scope указывает коллекцию &lt; элементов скопеитем &gt; , которые определяют включаемые и исключаемые области для этого конкретного соединителя поиска.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Элемент Scope (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c011eee8def80a7f1d395a7a52a72d30fb4935
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886700"
---
# <a name="scope-element-search-connector-schema"></a>Элемент Scope (схема соединителя поиска)

Необязательный &lt; &gt; элемент scope указывает коллекцию &lt; элементов скопеитем &gt; , которые определяют включаемые и исключаемые области для этого конкретного соединителя поиска. Если указана &lt; область &gt; , она должна содержать по крайней мере один &lt; &gt; элемент скопеитем. Этот элемент не содержит атрибуты.

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

Используйте &lt; элементы scope &gt; и &lt; скопеитем, &gt; чтобы определить, какие расположения следует искать, и какие расположения следует исключить из поиска.

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



 

 



