---
description: '&lt;Элемент пропертисторе &gt; указывает набор из одного или нескольких свойств, используемых этой библиотекой. Этот элемент является необязательным и не имеет атрибутов.'
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Элемент Пропертисторе (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089e87e6e7bdfa568ffa2e8903f6347cb6dc7b3d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880430"
---
# <a name="propertystore-element-library-schema"></a>Элемент Пропертисторе (схема библиотеки)

&lt;Элемент пропертисторе &gt; указывает набор из одного или нескольких свойств, используемых этой библиотекой. Этот элемент является необязательным и не имеет атрибутов.

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



 

## <a name="remarks"></a>Комментарии

&lt;Элемент пропертисторе &gt; может иметь один или несколько &lt; &gt; дочерних элементов свойства.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Схема описания библиотеки](library-schema-entry.md)
</dt> <dt>

[Схема описания соединителя поиска](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
