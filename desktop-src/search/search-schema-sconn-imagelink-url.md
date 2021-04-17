---
description: <url>Элемент указывает URL-адрес эскиза для соединителя поиска. Если <imageLink> существует, этот элемент является обязательным. У него нет дочерних элементов и атрибутов.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: Элемент URL-адреса Имажелинк (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692175"
---
# <a name="imagelink-url-element-search-connector-schema"></a>Элемент URL-адреса Имажелинк (схема соединителя поиска)

<url>Элемент указывает URL-адрес эскиза для соединителя поиска. Если <imageLink> существует, этот элемент является обязательным. У него нет дочерних элементов и атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                                   | Дочерние элементы |
|----------------------------------------------------------------------------------|----------------|
| [Элемент Имажелинк (схема соединителя поиска)](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a>Комментарии

Значением может быть путь к локальной файловой системе или URL-адрес. Файл образа может быть любым из базовых типов образов, поддерживаемых Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelinkurl-element"></a>Пример элемента Имажелинкурл


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



