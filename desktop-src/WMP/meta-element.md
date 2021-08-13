---
title: Элемент meta
description: Элемент meta указывает метаданные, которые применяются ко всему списку воспроизведения.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- элемент meta проигрыватель Windows Media
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b2e4120b3eceea6d2a664edec9b48a46d33ad19b788bb820458a8802dccd2d9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415744"
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

создатель списка воспроизведения Windows Media может задать для атрибута name элемента meta любую строку. в следующем списке показаны некоторые стандартные атрибуты имени, которые находятся в Windows списках воспроизведения мультимедиа, созданных проигрыватель Windows Media и другими компонентами майкрософт.

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент head**](head-element.md)
</dt> <dt>

[**Windows Справочник по элементам списка воспроизведения мультимедиа**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





