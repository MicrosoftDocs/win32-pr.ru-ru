---
description: <propertyStore>Элемент указывает набор из одного или нескольких свойств, используемых этой библиотекой. Этот элемент является необязательным и не имеет атрибутов.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Элемент Пропертисторе (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985820"
---
# <a name="propertystore-element-library-schema"></a>Элемент Пропертисторе (схема библиотеки)

<propertyStore>Элемент указывает набор из одного или нескольких свойств, используемых этой библиотекой. Этот элемент является необязательным и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                               | Дочерние элементы                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md) | [Элемент Property (схема библиотеки)](schema-library-property.md) |



 

## <a name="remarks"></a>Примечания

<propertyStore>Элемент может иметь один или несколько <property> дочерних элементов.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Схема описания библиотеки](library-schema-entry.md)
</dt> <dt>

[Схема описания соединителя поиска](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
