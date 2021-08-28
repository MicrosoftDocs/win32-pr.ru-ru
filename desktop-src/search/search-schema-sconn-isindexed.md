---
description: необязательный логический элемент с индексом "Boolean" &lt; указывает, &gt; индексируется ли расположение, описываемое соединителем поиска (локально или удаленно с помощью Windows поиска 4 или выше).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Элемент с индексом (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3588d451631ab8d0bb8313092b5b1ee7bb5c9dc4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881847"
---
# <a name="isindexed-element-search-connector-schema"></a>Элемент с индексом (схема соединителя поиска)

необязательный логический элемент с индексом "Boolean" &lt; указывает, &gt; индексируется ли расположение, описываемое соединителем поиска (локально или удаленно с помощью Windows поиска 4 или выше). Значение по умолчанию — true для локальных папок. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

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



 

 



