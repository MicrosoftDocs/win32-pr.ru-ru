---
title: Элемент запроса
description: Элемент «выданный запрос» содержит элементы, которые определяют, какие элементы мультимедиа будут выбраны из библиотеки.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Проигрыватель Windows Media, элемент запроса
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708421"
---
# <a name="queryset-element"></a>Элемент запроса

Элемент «выданный **запрос** » содержит элементы, которые определяют, какие элементы мультимедиа будут выбраны из библиотеки.

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                                   |
|-----------|--------------------------------------------|
| Parent    | [смартплайлист](smartplaylist-element.md) |
| Дочерний     | [саурцефилтер](sourcefilter-element.md)   |



 

## <a name="remarks"></a>Комментарии

Элемент набора **запроса** указывает, какие элементы мультимедиа следует выбрать из библиотеки, не учитывая размер результирующего набора. Элемент **Filter** , с другой стороны, ограничивает размер результирующего набора.

## <a name="examples"></a>Примеры


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
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

[**Смартплайлист, элемент**](smartplaylist-element.md)
</dt> <dt>

[**Саурцефилтер, элемент**](sourcefilter-element.md)
</dt> <dt>

[**Справочник по элементам списка воспроизведения Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





