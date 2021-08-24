---
description: необязательный логический <isIndexed> элемент указывает, индексируется ли расположение, описываемое соединителем поиска (локально или удаленно с помощью Windows поиска 4 или выше).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Элемент с индексом (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afcd1a95ec14b3bbea80374d8925a88231feb0110a421c2c850a297672d0c1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711054"
---
# <a name="isindexed-element-search-connector-schema"></a>Элемент с индексом (схема соединителя поиска)

необязательный логический <isIndexed> элемент указывает, индексируется ли расположение, описываемое соединителем поиска (локально или удаленно с помощью Windows поиска 4 или выше). Значение по умолчанию — true для локальных папок. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
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



 

## <a name="example"></a>Пример


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



