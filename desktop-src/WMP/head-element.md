---
title: Элемент head
description: Элемент head содержит метаданные, которые применяются ко всему списку воспроизведения.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- проигрыватель Windows Media головного элемента
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a865419a005927cd85ea6b03d4fabad2e2ac3ef15a840b3bd01209a4df00c075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339174"
---
# <a name="head-element"></a>Элемент head

Элемент **head** содержит метаданные, которые применяются ко всему списку воспроизведения.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                                                  |
|-----------|-----------------------------------------------------------|
| Parent    | [SMIL](smil-element.md)                                  |
| Дочерний     | [Title](title-element--wpl.md), [meta](meta-element.md) |



 

## <a name="remarks"></a>Remarks

Обычно элемент **head** содержит элемент **Title** и один или несколько элементов **meta** , определяющих глобальные характеристики списка воспроизведения.

## <a name="examples"></a>Примеры


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент meta**](meta-element.md)
</dt> <dt>

[**Элемент title (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Windows Справочник по элементам списка воспроизведения мультимедиа**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





