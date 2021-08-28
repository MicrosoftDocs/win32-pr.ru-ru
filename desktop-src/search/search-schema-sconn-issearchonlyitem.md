---
description: Элемент Boolean &lt; иссеарчонлитем &gt; указывает, поддерживает ли поставщик поиска режим просмотра в дополнение к режиму поиска. Этот элемент является необязательным и не имеет дочерних элементов и атрибутов.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Элемент Иссеарчонлитем (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524a69198a650e0cb995d2ff8b4fc942ebfdaddc
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883418"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>Элемент Иссеарчонлитем (схема соединителя поиска)

Элемент Boolean &lt; иссеарчонлитем &gt; указывает, поддерживает ли поставщик поиска режим просмотра в дополнение к режиму поиска. Этот элемент является необязательным и не имеет дочерних элементов и атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
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

Значение `true` указывает, что пользователи не могут просматривать расположение соединителя поиска. Значение `false` указывает, что пользователи могут просматривать расположение соединителя поиска.

## <a name="example"></a>Пример


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



