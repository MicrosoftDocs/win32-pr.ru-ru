---
description: Необязательный логический <isDefaultSaveLocation> элемент указывает, следует ли использовать расположение, описанное в соединителе поиска, в качестве расположения для сохранения по умолчанию. Этот элемент не имеет дочерних элементов и не имеет атрибутов.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Элемент Исдефаултсавелокатион (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b664e4cd6f7c88f1dfbeb44ba23faee5d24a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342912"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a>Элемент Исдефаултсавелокатион (схема соединителя поиска)

Необязательный логический <isDefaultSaveLocation> элемент указывает, следует ли использовать расположение, описанное в соединителе поиска, в качестве расположения для сохранения по умолчанию. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
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

Когда пользователь выбирает сохранение элемента, проводник Windows сохраняет его в расположении, указанном в <simpleLocation> элементе. Пользователи могут изменить этот параметр, используя диалоговое окно свойств соединителя поиска.

## <a name="example"></a>Пример


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



