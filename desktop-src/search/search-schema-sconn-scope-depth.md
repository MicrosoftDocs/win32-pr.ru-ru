---
description: '<depth>Элемент указывает, должен ли диапазон соединителя поиска включать дочерние URL-адреса. Допустимые значения: глубокий и поверхностный. Этот элемент не имеет дочерних элементов и не имеет атрибутов.'
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Элемент Depth (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245156088cd68fcf67103c18b987a9b459b0b760b3a04a1ced817badd25aada8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862529"
---
# <a name="depth-element-search-connector-schema"></a>Элемент Depth (схема соединителя поиска)

<depth>Элемент указывает, должен ли диапазон соединителя поиска включать дочерние URL-адреса. Допустимые значения: `Deep` и `Shallow`. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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



 

## <a name="remarks"></a>Remarks

Если глубина имеет глубину, пользователи могут просматривать или искать элементы на уровне URL-адреса Скопеитем или в любых дочерних URL-адресах.

## <a name="example"></a>Пример

В следующем примере показана область поиска, включающая в себя C: \\ Folder а и все ее дочерние папки и C: \\ фолдерб, но не все ее дочерние папки.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



