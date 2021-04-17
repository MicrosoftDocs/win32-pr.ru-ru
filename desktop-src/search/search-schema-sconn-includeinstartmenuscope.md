---
description: Необязательный логический <includeInStartMenuScope> элемент указывает, следует ли включать этот соединитель поиска в область поиска меню "Пуск".
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Элемент Инклудеинстартменускопе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692173"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>Элемент Инклудеинстартменускопе (схема соединителя поиска)

Необязательный логический <includeInStartMenuScope> элемент указывает, следует ли включать этот соединитель поиска в область поиска меню "Пуск". Значение по умолчанию — true для соединителей поиска, использующих файловую систему в качестве источника данных, и false для соединителей поиска, используемых обработчиками свойств. Этот элемент не имеет дочерних элементов и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
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

Если включить соединитель поиска в область меню "Пуск", пользователи смогут выполнять поиск в вашем расположении из поля поиска в меню "Пуск".

## <a name="example"></a>Пример


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



