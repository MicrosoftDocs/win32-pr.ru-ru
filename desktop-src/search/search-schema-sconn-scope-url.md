---
description: '&lt;Элемент URL &gt; задает URL-адрес, представляющий область соединителя поиска. Этот элемент не имеет дочерних элементов и не имеет атрибутов.'
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: Элемент URL-адреса Скопеитем (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a1db669f7365f04bed49c769ab695ab674b20b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886705"
---
# <a name="scopeitem-url-element-search-connector-schema"></a>Элемент URL-адреса Скопеитем (схема соединителя поиска)

&lt;Элемент URL &gt; задает URL-адрес, представляющий область соединителя поиска. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                   | Дочерние элементы |
|----------------------------------------------------------------------------------|----------------|
| [Элемент Скопеитем (схема соединителя поиска)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Комментарии

Значением может быть путь к локальной файловой системе или URL-адрес.

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



 

 



