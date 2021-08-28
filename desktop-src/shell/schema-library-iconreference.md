---
description: '&lt;Элемент иконреференце &gt; указывает пользовательский значок для этой библиотеки. Этот элемент является необязательным и не имеет атрибутов или дочерних элементов.'
title: Элемент Иконреференце (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: db34a387200f3078da08747191242ae7414be410
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884270"
---
# <a name="iconreference-element-library-schema"></a>Элемент Иконреференце (схема библиотеки)

&lt;Элемент иконреференце &gt; указывает пользовательский значок для этой библиотеки. Этот элемент является необязательным и не имеет атрибутов или дочерних элементов.

## <a name="syntax"></a>Синтаксис


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент                                                               | Дочерние элементы |
|------------------------------------------------------------------------------|----------------|
| [Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Комментарии

Ссылка на значок должна быть указана в форме, подходящей для функции [**паспарсеиконлокатион**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) . Например, так: `ModuleFileName,IconResourceIndex`.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Элемент Фолдертипе (схема библиотеки)](schema-library-foldertype.md)
</dt> <dt>

[Элемент Ислибрарипиннед (схема библиотеки)](schema-library-islibrarypinned.md)
</dt> <dt>

[Элемент Либраридескриптион (схема библиотеки)](schema-librarydescription.md)
</dt> <dt>

[Элемент Name (схема библиотеки)](schema-library-name.md)
</dt> <dt>

[Элемент ownerSID (схема библиотеки)](schema-library-ownersid.md)
</dt> <dt>

[Элемент Пропертисторе (схема библиотеки)](schema-library-propertystore.md)
</dt> <dt>

[Элемент Сеарчконнектордескриптион (схема библиотеки)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Элемент Сеарчконнектордескриптионлист (схема библиотеки)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Элемент Темплатеинфо (схема библиотеки)](schema-library-templateinfo.md)
</dt> <dt>

[Элемент Version (схема библиотеки)](schema-library-version.md)
</dt> </dl>

 

 



