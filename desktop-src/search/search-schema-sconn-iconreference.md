---
description: Необязательный <iconReference> элемент указывает пользовательский значок для этого расположения. Этот элемент не имеет атрибутов и не содержит дочерних элементов.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Элемент Иконреференце (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76391eb7079414abe13c4e45696ee3eacb3b968eb93b342b1b9e67825fac85c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862592"
---
# <a name="iconreference-element-search-connector-schema"></a>Элемент Иконреференце (схема соединителя поиска)

Необязательный <iconReference> элемент указывает пользовательский значок для этого расположения. Этот элемент не имеет атрибутов и не содержит дочерних элементов.

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



 

## <a name="remarks"></a>Remarks

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



 

 
