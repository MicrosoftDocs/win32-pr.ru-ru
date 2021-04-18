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
# <a name="filter-element"></a><span data-ttu-id="a894d-104">Элемент Filter</span><span class="sxs-lookup"><span data-stu-id="a894d-104">filter Element</span></span>

<span data-ttu-id="a894d-105">Элемент **Filter** содержит элементы, ограничивающие размер списка воспроизведения, длительность списка воспроизведения или число элементов мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a894d-105">The **filter** element contains elements that limit the size of a playlist, duration of a playlist, or number of media items in a playlist.</span></span>

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a><span data-ttu-id="a894d-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a894d-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="a894d-107"><span id="type"></span><span id="TYPE"></span>**Тип**</span><span class="sxs-lookup"><span data-stu-id="a894d-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="a894d-108">Тип объекта фильтра.</span><span class="sxs-lookup"><span data-stu-id="a894d-108">The type of filter object.</span></span> <span data-ttu-id="a894d-109">Для этого атрибута нет предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="a894d-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="a894d-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**идентификатор** (обязательный)</span><span class="sxs-lookup"><span data-stu-id="a894d-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="a894d-111">Идентификатор GUID, однозначно определяющий объект фильтра.</span><span class="sxs-lookup"><span data-stu-id="a894d-111">The GUID that uniquely identifies a filter object.</span></span> <span data-ttu-id="a894d-112">Методы объекта Filter вызываются для интерпретации элементов **фрагмента** , содержащихся в элементе **Filter** .</span><span class="sxs-lookup"><span data-stu-id="a894d-112">The filter object's methods are invoked to interpret the **fragment** elements contained in the **filter** element.</span></span>



| <span data-ttu-id="a894d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a894d-113">Value</span></span>                                  | <span data-ttu-id="a894d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a894d-114">Description</span></span>                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a894d-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span><span class="sxs-lookup"><span data-stu-id="a894d-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span></span> | <span data-ttu-id="a894d-116">Идентификатор для фильтра автоматического списка воспроизведения (Майкрософт) — ограничивается фильтром автовоспроизведения по количеству, размеру или длительности.</span><span class="sxs-lookup"><span data-stu-id="a894d-116">The id for the "Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration" filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a894d-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**имя** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="a894d-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="a894d-118">Имя объекта фильтра.</span><span class="sxs-lookup"><span data-stu-id="a894d-118">The name of the filter object.</span></span>



| <span data-ttu-id="a894d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a894d-119">Value</span></span>                                                                              | <span data-ttu-id="a894d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a894d-120">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="a894d-121">Фильтр автоматического воспроизведения (Майкрософт) — ограничивает автоматические списки воспроизведения по количеству, размеру или длительности</span><span class="sxs-lookup"><span data-stu-id="a894d-121">Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration</span></span> | <span data-ttu-id="a894d-122">Ограничивает автоматические списки воспроизведения по количеству, размеру или длительности.</span><span class="sxs-lookup"><span data-stu-id="a894d-122">Limits auto playlists by count, size, or duration.</span></span> |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="a894d-123">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a894d-123">Parent/Child Elements</span></span>



| <span data-ttu-id="a894d-124">Иерархия</span><span class="sxs-lookup"><span data-stu-id="a894d-124">Hierarchy</span></span> | <span data-ttu-id="a894d-125">Элементы</span><span class="sxs-lookup"><span data-stu-id="a894d-125">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="a894d-126">Parent</span><span class="sxs-lookup"><span data-stu-id="a894d-126">Parent</span></span>    | [<span data-ttu-id="a894d-127">смартплайлист</span><span class="sxs-lookup"><span data-stu-id="a894d-127">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="a894d-128">Дочерний</span><span class="sxs-lookup"><span data-stu-id="a894d-128">Child</span></span>     | [<span data-ttu-id="a894d-129">экстент</span><span class="sxs-lookup"><span data-stu-id="a894d-129">fragment</span></span>](fragment-element.md)           |



 

## <a name="remarks"></a><span data-ttu-id="a894d-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a894d-130">Remarks</span></span>

<span data-ttu-id="a894d-131">Элемент **Filter** не добавляет элементы мультимедиа в список воспроизведения; Он просто удаляет или отфильтровывает содержимое, выбранное элементом **саурцефилтер** .</span><span class="sxs-lookup"><span data-stu-id="a894d-131">The **filter** element does not add any media elements to a playlist; it simply removes or filters out content that was selected by the **sourceFilter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="a894d-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="a894d-132">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a894d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a894d-133">Requirements</span></span>



| <span data-ttu-id="a894d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a894d-134">Requirement</span></span> | <span data-ttu-id="a894d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a894d-135">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="a894d-136">Версия</span><span class="sxs-lookup"><span data-stu-id="a894d-136">Version</span></span><br/> | <span data-ttu-id="a894d-137">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a894d-137">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a894d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a894d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a894d-139">**Элемент Argument**</span><span class="sxs-lookup"><span data-stu-id="a894d-139">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="a894d-140">**Элемент Fragment**</span><span class="sxs-lookup"><span data-stu-id="a894d-140">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="a894d-141">**Смартплайлист, элемент**</span><span class="sxs-lookup"><span data-stu-id="a894d-141">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="a894d-142">**Саурцефилтер, элемент**</span><span class="sxs-lookup"><span data-stu-id="a894d-142">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="a894d-143">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a894d-143">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





