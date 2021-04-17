---
title: Смартплайлист, элемент
description: Элемент Смартплайлист содержит динамически определенную часть списка воспроизведения.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- Проигрыватель Windows Media, элемент Смартплайлист
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708476"
---
# <a name="smartplaylist-element"></a>Смартплайлист, элемент

Элемент **смартплайлист** содержит динамически определенную часть списка воспроизведения.

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a>Атрибуты



| Термин                                                                                                                                   | Описание                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**версия** (обязательно) <br/> | Десятичное число, представляющее номер версии схемы смарт-списка воспроизведения. Задайте значение 1.0.0.0.<br/> |



 

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                                                       |
|-----------|----------------------------------------------------------------|
| Parent    | [порядк](seq-element.md)                                         |
| Дочерний     | [запрос](queryset-element.md), [Фильтр](filter-element.md) |



 

## <a name="remarks"></a>Комментарии

Элемент **смартплайлист** обычно содержит элемент с набором **запроса** , который также может содержать элемент **Filter** .

## <a name="examples"></a>Примеры


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
            name = "Music in my library">
                <fragment name = "Genre">
                    <argument name = "condition">Is</argument>
                    <argument name = "value">Rock</argument>
                </fragment>
                <fragment name = "Album Artist">
                    <argument name = "condition">Is Not</argument>
                    <argument name = "value">Brenda Diaz</argument>
                </fragment>
        </sourceFilter>
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент Argument**](argument-element.md)
</dt> <dt>

[**Элемент Filter**](filter-element.md)
</dt> <dt>

[**Элемент Fragment**](fragment-element.md)
</dt> <dt>

[**Элемент запроса**](queryset-element.md)
</dt> <dt>

[**Seq, элемент**](seq-element.md)
</dt> <dt>

[**Справочник по элементам списка воспроизведения Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





