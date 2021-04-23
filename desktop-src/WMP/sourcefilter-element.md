---
title: Саурцефилтер, элемент
description: Элемент Саурцефилтер содержит элементы, которые выбирают элементы из библиотеки.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Проигрыватель Windows Media, элемент Саурцефилтер
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652140"
---
# <a name="sourcefilter-element"></a><span data-ttu-id="a6cbc-104">Саурцефилтер, элемент</span><span class="sxs-lookup"><span data-stu-id="a6cbc-104">sourceFilter Element</span></span>

<span data-ttu-id="a6cbc-105">Элемент **саурцефилтер** содержит элементы, которые выбирают элементы из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-105">The **sourceFilter** element contains elements that select items from a library.</span></span>

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a><span data-ttu-id="a6cbc-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a6cbc-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="a6cbc-107"><span id="type"></span><span id="TYPE"></span>**Тип**</span><span class="sxs-lookup"><span data-stu-id="a6cbc-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="a6cbc-108">Тип объекта фильтра.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-108">The type of filter object.</span></span> <span data-ttu-id="a6cbc-109">Для этого атрибута нет предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="a6cbc-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**идентификатор** (обязательный)</span><span class="sxs-lookup"><span data-stu-id="a6cbc-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="a6cbc-111">Идентификатор GUID, однозначно определяющий объект фильтра источника.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-111">The GUID that uniquely identifies the source filter object.</span></span> <span data-ttu-id="a6cbc-112">Методы объекта фильтра источника вызываются для интерпретации элементов **фрагмента** , содержащихся в элементе **саурцефилтер** .</span><span class="sxs-lookup"><span data-stu-id="a6cbc-112">The source filter object's methods are invoked to interpret the **fragment** elements contained in the **sourceFilter** element.</span></span>



| <span data-ttu-id="a6cbc-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a6cbc-113">Value</span></span>                                  | <span data-ttu-id="a6cbc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a6cbc-114">Description</span></span>                                              |
|----------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="a6cbc-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span><span class="sxs-lookup"><span data-stu-id="a6cbc-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span></span> | <span data-ttu-id="a6cbc-116">Идентификатор GUID для фильтра источников "музыка в библиотеке".</span><span class="sxs-lookup"><span data-stu-id="a6cbc-116">The GUID for the "Music in my library" source filter.</span></span>    |
| <span data-ttu-id="a6cbc-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span><span class="sxs-lookup"><span data-stu-id="a6cbc-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span></span> | <span data-ttu-id="a6cbc-118">Идентификатор GUID для фильтра источников "видео в библиотеке".</span><span class="sxs-lookup"><span data-stu-id="a6cbc-118">The GUID for the "Video in my library" source filter.</span></span>    |
| <span data-ttu-id="a6cbc-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span><span class="sxs-lookup"><span data-stu-id="a6cbc-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span></span> | <span data-ttu-id="a6cbc-120">Идентификатор GUID для фильтра источников "изображения в библиотеке".</span><span class="sxs-lookup"><span data-stu-id="a6cbc-120">The GUID for the "Pictures in my library" source filter.</span></span> |
| <span data-ttu-id="a6cbc-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span><span class="sxs-lookup"><span data-stu-id="a6cbc-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span></span> | <span data-ttu-id="a6cbc-122">Идентификатор GUID для фильтра источника "ТВ-передачи в библиотеке".</span><span class="sxs-lookup"><span data-stu-id="a6cbc-122">The GUID for the "TV shows in my library" source filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a6cbc-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**имя** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="a6cbc-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="a6cbc-124">Имя объекта фильтра.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-124">The name of the filter object.</span></span>



| <span data-ttu-id="a6cbc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a6cbc-125">Value</span></span>                  | <span data-ttu-id="a6cbc-126">Описание</span><span class="sxs-lookup"><span data-stu-id="a6cbc-126">Description</span></span>                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cbc-127">Музыка в библиотеке</span><span class="sxs-lookup"><span data-stu-id="a6cbc-127">Music in my library</span></span>    | <span data-ttu-id="a6cbc-128">Объект Filter, выбирающий указанные элементы из набора музыкальных элементов в библиотеке пользователя.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-128">A filter object that selects specified items from the set of music items in the user's library.</span></span> |
| <span data-ttu-id="a6cbc-129">Видео в библиотеке</span><span class="sxs-lookup"><span data-stu-id="a6cbc-129">Video in my library</span></span>    | <span data-ttu-id="a6cbc-130">Объект Filter, выбирающий указанные элементы из набора видеозаписей в библиотеке пользователя.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-130">A filter object that selects specified items from the set of video items in the user's library.</span></span> |
| <span data-ttu-id="a6cbc-131">Изображения в библиотеке</span><span class="sxs-lookup"><span data-stu-id="a6cbc-131">Pictures in my library</span></span> | <span data-ttu-id="a6cbc-132">Объект Filter, выбирающий указанные элементы из набора элементов Photo в библиотеке пользователя.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-132">A filter object that selects specified items from the set of photo items in the user's library.</span></span> |
| <span data-ttu-id="a6cbc-133">ТВ-передачи в библиотеке</span><span class="sxs-lookup"><span data-stu-id="a6cbc-133">TV shows in my library</span></span> | <span data-ttu-id="a6cbc-134">Объект фильтра, выбирающий указанные элементы из набора ТВ-элементов в библиотеке пользователя.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-134">A filter object that selects specified items from the set of TV items in the user's library.</span></span>    |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="a6cbc-135">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a6cbc-135">Parent/Child Elements</span></span>



| <span data-ttu-id="a6cbc-136">Иерархия</span><span class="sxs-lookup"><span data-stu-id="a6cbc-136">Hierarchy</span></span> | <span data-ttu-id="a6cbc-137">Элементы</span><span class="sxs-lookup"><span data-stu-id="a6cbc-137">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="a6cbc-138">Parent</span><span class="sxs-lookup"><span data-stu-id="a6cbc-138">Parent</span></span>    | [<span data-ttu-id="a6cbc-139">запрос</span><span class="sxs-lookup"><span data-stu-id="a6cbc-139">querySet</span></span>](queryset-element.md) |
| <span data-ttu-id="a6cbc-140">Дочерний</span><span class="sxs-lookup"><span data-stu-id="a6cbc-140">Child</span></span>     | [<span data-ttu-id="a6cbc-141">экстент</span><span class="sxs-lookup"><span data-stu-id="a6cbc-141">fragment</span></span>](fragment-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="a6cbc-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6cbc-142">Remarks</span></span>

<span data-ttu-id="a6cbc-143">Элемент **саурцефилтер** выбирает элементы из библиотеки без учета размера результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-143">The **sourceFilter** element selects items from the library without regard for the size of the result set.</span></span> <span data-ttu-id="a6cbc-144">Элемент **Filter** , с другой стороны, ограничивает размер результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-144">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="a6cbc-145">Примеры</span><span class="sxs-lookup"><span data-stu-id="a6cbc-145">Examples</span></span>


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
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
```



## <a name="requirements"></a><span data-ttu-id="a6cbc-146">Требования</span><span class="sxs-lookup"><span data-stu-id="a6cbc-146">Requirements</span></span>



| <span data-ttu-id="a6cbc-147">Требование</span><span class="sxs-lookup"><span data-stu-id="a6cbc-147">Requirement</span></span> | <span data-ttu-id="a6cbc-148">Значение</span><span class="sxs-lookup"><span data-stu-id="a6cbc-148">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="a6cbc-149">Версия</span><span class="sxs-lookup"><span data-stu-id="a6cbc-149">Version</span></span><br/> | <span data-ttu-id="a6cbc-150">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a6cbc-150">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6cbc-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6cbc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6cbc-152">**Элемент Filter**</span><span class="sxs-lookup"><span data-stu-id="a6cbc-152">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="a6cbc-153">**Элемент Fragment**</span><span class="sxs-lookup"><span data-stu-id="a6cbc-153">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="a6cbc-154">**Элемент запроса**</span><span class="sxs-lookup"><span data-stu-id="a6cbc-154">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="a6cbc-155">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a6cbc-155">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





