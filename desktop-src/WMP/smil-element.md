---
title: SMIL, элемент
description: элемент smil всегда является элементом верхнего уровня в файле списка воспроизведения Windows Media (WPL). Он указывает, что в файле используется SMIL (синхронизированный язык интеграции мультимедиа) синтаксис и грамматика.
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- элемент smil проигрыватель Windows Media
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15ed9c3d70b0af65019cd384bc68ab9c26f8d01673481b9ced3595730379bf1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763464"
---
# <a name="smil-element"></a>SMIL, элемент

элемент **smil** всегда является элементом верхнего уровня в файле списка воспроизведения Windows Media (WPL). Он указывает, что в файле используется SMIL (синхронизированный язык интеграции мультимедиа) синтаксис и грамматика.

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                                           |
|-----------|----------------------------------------------------|
| Parent    | Нет                                               |
| Дочерний     | [головной](head-element.md), [основной текст](body-element.md) |



 

## <a name="remarks"></a>Remarks

каждый Windows списка воспроизведения мультимедиа должен иметь элемент **smil** в его корне.

## <a name="examples"></a>Примеры


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент Body**](body-element.md)
</dt> <dt>

[**Элемент head**](head-element.md)
</dt> <dt>

[**Windows Справочник по элементам списка воспроизведения мультимедиа**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





