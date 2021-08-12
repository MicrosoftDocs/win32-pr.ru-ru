---
title: Элемент запроса
description: Элемент «выданный запрос» содержит элементы, которые определяют, какие элементы мультимедиа будут выбраны из библиотеки.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- проигрыватель Windows Media элемента запроса
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb157bb30c2e728b7840fe7021a2a4fcacc317b10eb6778b5702d7d2277c4a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570617"
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



 

## <a name="remarks"></a>Remarks

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
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



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

[**Windows Справочник по элементам списка воспроизведения мультимедиа**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





