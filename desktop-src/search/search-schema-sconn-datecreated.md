---
description: Необязательный <dateCreated> элемент определяет дату и время создания соединителя поиска, используя стандарт ISO 8601. У него нет дочерних элементов и атрибутов.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Элемент dateCreated (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808908"
---
# <a name="datecreated-element-search-connector-schema"></a>Элемент dateCreated (схема соединителя поиска)

Необязательный <dateCreated> элемент определяет дату и время создания соединителя поиска, используя стандарт ISO 8601. У него нет дочерних элементов и атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
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

Формат значения этого элемента соответствует стандарту ISO 8601. Обычно используется один из следующих типов:

-   \[Гггг \] - \[ мм \] - \[ дд \] T \[ чч \] : \[ мм \] : \[ СС \] ± \[ чч \] : \[ мм \] ("1981-04-05T14:30:30-05:00")
-   \[ГГГГ \] \[ мм \] \[ дд \] T \[ чч \] \[ mm \] \[ SS \] Z ("19810405T193030Z")

## <a name="example"></a>Пример


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



