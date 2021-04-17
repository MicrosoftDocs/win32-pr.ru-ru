---
title: Элемент meta
description: Элемент meta указывает метаданные, которые применяются ко всему списку воспроизведения.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Проигрыватель Windows Media, элемент meta
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651816"
---
# <a name="meta-element"></a>Элемент meta

Элемент **meta** указывает метаданные, которые применяются ко всему списку воспроизведения.

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>Атрибуты



| Термин                                                                       | Описание                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**безымян**<br/>          | Имя элемента метаданных.<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**содержани**<br/> | Значение элемента метаданных. Например, если атрибут name имеет значение «жанр», атрибут содержимого может иметь значение «рок».<br/> |



 

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                 |
|-----------|--------------------------|
| Parent    | [Глава](head-element.md) |
| Дочерний     | None                     |



 

## <a name="remarks"></a>Remarks

Создатель списка воспроизведения Windows Media может задать для атрибута Name элемента meta любую строку. В следующем списке показаны некоторые стандартные атрибуты имени, которые находятся в списках воспроизведения Windows Media, созданных проигрывателем Windows Media и другими компонентами Майкрософт.

-   Автор
-   Категория
-   Genre
-   Имя пользователя
-   UserRating
-   Generator

## <a name="examples"></a>Примеры


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент head**](head-element.md)
</dt> <dt>

[**Справочник по элементам списка воспроизведения Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





