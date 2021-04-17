---
description: <templateInfo>Элемент является контейнером для элемента фолдертипе, который указывает тип папки для отображения результатов запроса к этой библиотеке. Этот элемент является необязательным и не имеет атрибутов.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Элемент Темплатеинфо (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543098"
---
# <a name="templateinfo-element-library-schema"></a>Элемент Темплатеинфо (схема библиотеки)

<templateInfo>Элемент является контейнером для элемента [фолдертипе](schema-library-foldertype.md) , который указывает тип папки для отображения результатов запроса к этой библиотеке. Этот элемент является необязательным и не имеет атрибутов.

## <a name="syntax"></a>Синтаксис

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                               | Дочерние элементы                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md) | [Элемент Фолдертипе (схема библиотеки)](schema-library-foldertype.md)       |
|                                                                              | [Элемент Пропертисторе (схема библиотеки)](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Схема описания библиотеки](library-schema-entry.md)
</dt> <dt>

[Схема описания соединителя поиска](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
