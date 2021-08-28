---
description: Необязательный &lt; &gt; элемент домена указывает URL-адрес службы поиска, используемой этим соединителем поиска. Он отображается в области сведений. Этот элемент не имеет дочерних элементов и не имеет атрибутов.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Элемент domain (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd84ffa2ee5bcc5f5f6dcdb93c9abbd12c57bd96
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882479"
---
# <a name="domain-element-search-connector-schema"></a>Элемент domain (схема соединителя поиска)

Необязательный &lt; &gt; элемент домена указывает URL-адрес службы поиска, используемой этим соединителем поиска. Он отображается в области сведений. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                                                   | Дочерние элементы |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Комментарии

URL-адрес должен быть доменом верхнего уровня для поставщика поиска. Например, https://www.example.com.

## <a name="example"></a>Пример


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



