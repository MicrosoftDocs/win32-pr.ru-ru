---
title: Элемент Body
description: Элемент Body содержит элементы, определяющие содержимое списка воспроизведения.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Проигрыватель Windows Media, элемент Body
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698867"
---
# <a name="body-element"></a>Элемент Body

Элемент **Body** содержит элементы, определяющие содержимое списка воспроизведения.

``` syntax
<body>
</body>
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                 |
|-----------|--------------------------|
| Parent    | [SMIL](smil-element.md) |
| Дочерний     | [порядк](seq-element.md)   |



 

## <a name="remarks"></a>Комментарии

Содержимое списка воспроизведения упорядочено внутри элемента **Seq** , который содержится в элементе **Body** . Обычно существует либо один элемент **Seq** , который определяет статический набор элементов мультимедиа и содержит элементы **мультимедиа** , либо один, который определяет динамический набор элементов мультимедиа и содержит элемент **смартплайлист** .

## <a name="examples"></a>Примеры


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент Media**](media-element.md)
</dt> <dt>

[**Seq, элемент**](seq-element.md)
</dt> <dt>

[**Смартплайлист, элемент**](smartplaylist-element.md)
</dt> <dt>

[**SMIL, элемент**](smil-element.md)
</dt> <dt>

[**Справочник по элементам списка воспроизведения Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





