---
description: <scopeItem>Элемент представляет отдельную запись в таблице область исключения/включения.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: Элемент Скопеитем (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144014"
---
# <a name="scopeitem-element-search-connector-schema"></a>Элемент Скопеитем (схема соединителя поиска)

<scopeItem>Элемент представляет отдельную запись в таблице область исключения/включения. <scopeItem> расширяет стандартный тип Шелллинктипе, добавляя три новых элемента, управляющих включением и исключением папок, контролируя глубину результатов и задающее расположение области. Если <scope> элемент существует, этот элемент является обязательным. Он имеет три дочерних элемента и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
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



| Родительский элемент                                                           | Дочерние элементы                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Элемент Scope (схема соединителя поиска)](search-schema-sconn-scope.md) | [элемент Scope (схема соединителя поиска)](search-schema-sconn-scope-mode.md).        |
|                                                                          | [элемент Scope (схема соединителя поиска)](search-schema-sconn-scope-depth.md).       |
|                                                                          | [элемент URL скопеитем (схема соединителя поиска)](search-schema-sconn-scope-url.md). |



 

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



 

 



