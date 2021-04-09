---
description: Необязательный логический <isIndexed> элемент указывает, индексируется ли расположение, описываемое соединителем поиска (локально или удаленно с помощью Windows Search 4 или более поздней версии).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Элемент с индексом (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144020"
---
# <a name="isindexed-element-search-connector-schema"></a>Элемент с индексом (схема соединителя поиска)

Необязательный логический <isIndexed> элемент указывает, индексируется ли расположение, описываемое соединителем поиска (локально или удаленно с помощью Windows Search 4 или более поздней версии). Значение по умолчанию — true для локальных папок. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

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



 

 



