---
title: SMIL, элемент
description: Элемент smil всегда является элементом верхнего уровня в файле списка воспроизведения Windows Media (WPL). Он указывает, что в файле используется SMIL (синхронизированный язык интеграции мультимедиа) синтаксис и грамматика.
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Элемент smil Windows Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657843"
---
# <a name="smil-element"></a>SMIL, элемент

Элемент **SMIL** всегда является элементом верхнего уровня в файле списка воспроизведения Windows Media (WPL). Он указывает, что в файле используется SMIL (синхронизированный язык интеграции мультимедиа) синтаксис и грамматика.

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



 

## <a name="remarks"></a>Комментарии

Каждый список воспроизведения Windows Media должен иметь элемент **SMIL** в корне.

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент Body**](body-element.md)
</dt> <dt>

[**Элемент head**](head-element.md)
</dt> <dt>

[**Справочник по элементам списка воспроизведения Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





