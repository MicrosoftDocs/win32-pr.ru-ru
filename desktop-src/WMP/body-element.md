---
title: Элемент Body
description: Элемент Body содержит элементы, определяющие содержимое списка воспроизведения.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- элемент body проигрыватель Windows Media
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c785b7db7b44177469596450ee75a460e2bc6224b191a2811baf95380bea25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135957"
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



 

## <a name="remarks"></a>Remarks

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
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



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

[**Windows Справочник по элементам списка воспроизведения мультимедиа**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





