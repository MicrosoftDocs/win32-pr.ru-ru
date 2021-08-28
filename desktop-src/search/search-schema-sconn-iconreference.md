---
description: Необязательный &lt; &gt; элемент иконреференце указывает пользовательский значок для этого расположения. Этот элемент не имеет атрибутов и не содержит дочерних элементов.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Элемент Иконреференце (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ff41d6dfd37e5e3fe780171701886b08b195ac
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882413"
---
# <a name="iconreference-element-search-connector-schema"></a>Элемент Иконреференце (схема соединителя поиска)

Необязательный &lt; &gt; элемент иконреференце указывает пользовательский значок для этого расположения. Этот элемент не имеет атрибутов и не содержит дочерних элементов.

## <a name="syntax"></a>Синтаксис


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
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

Формат ссылки должен быть указан в форме, подходящей для функции [паспарсеиконлокатион](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) : (например, <dll file name> <icon index> ).

## <a name="example"></a>Пример


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
