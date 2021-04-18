---
title: Элемент Filter
description: Элемент Filter содержит элементы, ограничивающие размер списка воспроизведения, длительность списка воспроизведения или число элементов мультимедиа в списке воспроизведения.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- Элемент фильтра Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694870"
---
# <a name="filter-element"></a>Элемент Filter

Элемент **Filter** содержит элементы, ограничивающие размер списка воспроизведения, длительность списка воспроизведения или число элементов мультимедиа в списке воспроизведения.

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a>Атрибуты

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**Тип**
</dt> <dd>

Тип объекта фильтра. Для этого атрибута нет предопределенных значений.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**идентификатор** (обязательный) 
</dt> <dd>

Идентификатор GUID, однозначно определяющий объект фильтра. Методы объекта Filter вызываются для интерпретации элементов **фрагмента** , содержащихся в элементе **Filter** .



| Значение                                  | Описание                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | Идентификатор для фильтра автоматического списка воспроизведения (Майкрософт) — ограничивается фильтром автовоспроизведения по количеству, размеру или длительности. |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**имя** (обязательно) 
</dt> <dd>

Имя объекта фильтра.



| Значение                                                                              | Описание                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Фильтр автоматического воспроизведения (Майкрософт) — ограничивает автоматические списки воспроизведения по количеству, размеру или длительности | Ограничивает автоматические списки воспроизведения по количеству, размеру или длительности. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                                   |
|-----------|--------------------------------------------|
| Parent    | [смартплайлист](smartplaylist-element.md) |
| Дочерний     | [экстент](fragment-element.md)           |



 

## <a name="remarks"></a>Комментарии

Элемент **Filter** не добавляет элементы мультимедиа в список воспроизведения; Он просто удаляет или отфильтровывает содержимое, выбранное элементом **саурцефилтер** .

## <a name="examples"></a>Примеры


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент Argument**](argument-element.md)
</dt> <dt>

[**Элемент Fragment**](fragment-element.md)
</dt> <dt>

[**Смартплайлист, элемент**](smartplaylist-element.md)
</dt> <dt>

[**Саурцефилтер, элемент**](sourcefilter-element.md)
</dt> <dt>

[**Справочник по элементам списка воспроизведения Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





