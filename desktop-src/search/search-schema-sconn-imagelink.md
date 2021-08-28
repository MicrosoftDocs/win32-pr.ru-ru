---
description: Необязательный &lt; &gt; элемент имажелинк указывает эскиз для этого соединителя поиска. Этот элемент имеет один обязательный дочерний элемент и не имеет атрибутов.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Элемент Имажелинк (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6030f44e74f8f8441b3a6cd0835df9c5969619
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882398"
---
# <a name="imagelink-element-search-connector-schema"></a>Элемент Имажелинк (схема соединителя поиска)

Необязательный &lt; &gt; элемент имажелинк указывает эскиз для этого соединителя поиска. Этот элемент имеет один обязательный дочерний элемент и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис


```
<!-- imageLink -->
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



| Родительский элемент                                                                                                   | Дочерние элементы                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)](search-schema-searchconnectordescription.md) | [Элемент URL-адреса Имажелинк (схема соединителя поиска)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Комментарии

Значение Имажелинк может быть локальным путем файловой системы или URL-адресом. файл изображения может быть любым из базовых типов образов, поддерживаемых Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Пример элемента Имажелинк


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



