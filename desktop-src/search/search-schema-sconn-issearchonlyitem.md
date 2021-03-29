---
description: Элемент логического типа <isSearchOnlyItem> определяет, поддерживает ли поставщик поиска режим просмотра в дополнение к режиму поиска. Этот элемент является необязательным и не имеет дочерних элементов и атрибутов.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Элемент Иссеарчонлитем (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540631"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>Элемент Иссеарчонлитем (схема соединителя поиска)

Элемент логического типа <isSearchOnlyItem> определяет, поддерживает ли поставщик поиска режим просмотра в дополнение к режиму поиска. Этот элемент является необязательным и не имеет дочерних элементов и атрибутов.

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



 

 



