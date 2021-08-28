---
description: Необязательный &lt; элемент логического исдефаултноновнерсавелокатион &gt; указывает, следует ли использовать расположение, описанное в соединителе поиска, в качестве расположения для сохранения по умолчанию, когда пользователь с другого компьютера в домашней группе выбирает сохранение элемента.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Элемент Исдефаултноновнерсавелокатион (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2a20912b10864d856bd4513e31a37eeee5c2a0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881934"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>Элемент Исдефаултноновнерсавелокатион (схема соединителя поиска)

Необязательный &lt; элемент логического исдефаултноновнерсавелокатион &gt; указывает, следует ли использовать расположение, описанное в соединителе поиска, в качестве расположения для сохранения по умолчанию, когда пользователь с другого компьютера в домашней группе выбирает сохранение элемента. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
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

если задано значение true, то когда пользователь из другого компьютера в домашней группе выбирает сохранение элемента, Windows Explorer сохраняет его в расположении, указанном &lt; в &gt; элементе симплелокатион.

## <a name="example"></a>Пример


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



