---
description: Этот &lt; &gt; элемент сеарчконнектордескриптионлист содержит список соединителей поиска, которые сопоставляются с расположениями, входящими в эту библиотеку. Каждый соединитель поиска определяется &lt; &gt; элементом сеарчконнектордескриптион. Этот элемент является необязательным и не имеет атрибутов.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Элемент Сеарчконнектордескриптионлист (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc3a3cb7353529dccca66ffa15e1604bdd1c0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885610"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>Элемент Сеарчконнектордескриптионлист (схема библиотеки)

Этот &lt; &gt; элемент сеарчконнектордескриптионлист содержит список соединителей поиска, которые сопоставляются с расположениями, входящими в эту библиотеку. Каждый соединитель поиска определяется &lt; &gt; элементом сеарчконнектордескриптион. Этот элемент является необязательным и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                               | Дочерние элементы                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md) | [Элемент Сеарчконнектордескриптион (схема библиотеки)](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a>Комментарии

соединители поиска для Windows федеративного поиска и области обработчика протокола не могут быть добавлены в библиотеку.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Схема описания библиотеки](library-schema-entry.md)
</dt> <dt>

[Схема описания соединителя поиска](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
