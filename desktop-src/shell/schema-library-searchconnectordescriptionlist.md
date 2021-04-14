---
description: Этот <searchConnectorDescriptionList> элемент содержит список соединителей поиска, которые сопоставляются с расположениями, входящими в эту библиотеку. Каждый соединитель поиска определяется <searchConnectorDescription> элементом. Этот элемент является необязательным и не имеет атрибутов.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Элемент Сеарчконнектордескриптионлист (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985892"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>Элемент Сеарчконнектордескриптионлист (схема библиотеки)

Этот <searchConnectorDescriptionList> элемент содержит список соединителей поиска, которые сопоставляются с расположениями, входящими в эту библиотеку. Каждый соединитель поиска определяется <searchConnectorDescription> элементом. Этот элемент является необязательным и не имеет атрибутов.

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



 

## <a name="remarks"></a>Примечания

Соединители поиска для федеративного поиска Windows и области обработчика протокола не могут быть добавлены в библиотеку.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Схема описания библиотеки](library-schema-entry.md)
</dt> <dt>

[Схема описания соединителя поиска](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
