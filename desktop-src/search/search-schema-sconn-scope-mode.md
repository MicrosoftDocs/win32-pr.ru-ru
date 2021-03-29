---
description: '<mode>Элемент указывает, следует ли включать или исключать URL-адрес из области соединителя поиска. Допустимые значения: include и Exclude. Этот элемент не имеет дочерних элементов и не имеет атрибутов.'
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Элемент Mode (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808896"
---
# <a name="mode-element-search-connector-schema"></a>Элемент Mode (схема соединителя поиска)

<mode>Элемент указывает, следует ли включать или исключать URL-адрес из области соединителя поиска. Допустимые значения: `Include` и `Exclude`. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
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



| Родительский элемент                                                                   | Дочерние элементы |
|----------------------------------------------------------------------------------|----------------|
| [Элемент Скопеитем (схема соединителя поиска)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Комментарии

Невозможно выполнить поиск или просмотр исключенной области. URL-адреса Скопеитем можно вкладывать. Например, можно включить родительскую область и все ее дочерние элементы, кроме одной, добавив родительский URL-адрес как включенный, со значением глубины Deep и исключая дочерний URL-адрес.

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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



