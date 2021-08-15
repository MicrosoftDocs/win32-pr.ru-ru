---
description: <simpleLocation>Элемент указывает расположение соединителей поиска, основанных на файловой системе или обработчике протоколов. Этот элемент имеет два дочерних элемента и не имеет атрибутов.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Элемент Симплелокатион (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82731c5a230f8dd12b9d73cafd75dfc7d3cdd66bf1e57120701ed3ca0ba54b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862465"
---
# <a name="simplelocation-element-search-connector-schema"></a>Элемент Симплелокатион (схема соединителя поиска)

<simpleLocation>Элемент указывает расположение соединителей поиска, основанных на файловой системе или обработчике протоколов. Этот элемент имеет два дочерних элемента и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                                                   | Дочерние элементы                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)](search-schema-searchconnectordescription.md) | [Элемент URL-адреса Симплелокатион (схема соединителя поиска)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | сериализовано: этот элемент содержит Шелллинк в кодировке Base64, указывающий на расположение, определенное в <url> элементе. Windows 7 создает шелллинк из значения <url> элемента и соответствующим образом обновляет это поле при первой загрузке этой библиотеки, поэтому автор должен оставить его пустым. |



 

## <a name="remarks"></a>Remarks

Этот элемент можно использовать вместо, <locationProvider> Если расположение находится в файловой системе или если соединитель является известным обработчиком протокола (например, MAPI:). Если <simpleLocation> присутствует, то не должен быть <locationProvider> элементом. Для соединителей поиска поставщика веб-служб используйте [<locationProvider>](search-schema-sconn-locationprovider.md) элемент.

## <a name="examples"></a>Примеры


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



