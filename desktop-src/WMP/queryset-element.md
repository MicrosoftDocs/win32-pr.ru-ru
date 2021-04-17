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
# <a name="queryset-element"></a><span data-ttu-id="26c83-104">Элемент запроса</span><span class="sxs-lookup"><span data-stu-id="26c83-104">querySet Element</span></span>

<span data-ttu-id="26c83-105">Элемент «выданный **запрос** » содержит элементы, которые определяют, какие элементы мультимедиа будут выбраны из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="26c83-105">The **querySet** element contains elements that define which media items will be selected from the library.</span></span>

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a><span data-ttu-id="26c83-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="26c83-106">Attributes</span></span>

<span data-ttu-id="26c83-107">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="26c83-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="26c83-108">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="26c83-108">Parent/Child Elements</span></span>



| <span data-ttu-id="26c83-109">Иерархия</span><span class="sxs-lookup"><span data-stu-id="26c83-109">Hierarchy</span></span> | <span data-ttu-id="26c83-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="26c83-110">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="26c83-111">Parent</span><span class="sxs-lookup"><span data-stu-id="26c83-111">Parent</span></span>    | [<span data-ttu-id="26c83-112">смартплайлист</span><span class="sxs-lookup"><span data-stu-id="26c83-112">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="26c83-113">Дочерний</span><span class="sxs-lookup"><span data-stu-id="26c83-113">Child</span></span>     | [<span data-ttu-id="26c83-114">саурцефилтер</span><span class="sxs-lookup"><span data-stu-id="26c83-114">sourceFilter</span></span>](sourcefilter-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="26c83-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26c83-115">Remarks</span></span>

<span data-ttu-id="26c83-116">Элемент набора **запроса** указывает, какие элементы мультимедиа следует выбрать из библиотеки, не учитывая размер результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="26c83-116">The **querySet** element specifies which media items should be selected from the library, without regard for the size of the result set.</span></span> <span data-ttu-id="26c83-117">Элемент **Filter** , с другой стороны, ограничивает размер результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="26c83-117">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="26c83-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="26c83-118">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="26c83-119">Требования</span><span class="sxs-lookup"><span data-stu-id="26c83-119">Requirements</span></span>



| <span data-ttu-id="26c83-120">Требование</span><span class="sxs-lookup"><span data-stu-id="26c83-120">Requirement</span></span> | <span data-ttu-id="26c83-121">Значение</span><span class="sxs-lookup"><span data-stu-id="26c83-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="26c83-122">Версия</span><span class="sxs-lookup"><span data-stu-id="26c83-122">Version</span></span><br/> | <span data-ttu-id="26c83-123">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="26c83-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26c83-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26c83-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c83-125">**Элемент Argument**</span><span class="sxs-lookup"><span data-stu-id="26c83-125">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="26c83-126">**Элемент Filter**</span><span class="sxs-lookup"><span data-stu-id="26c83-126">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="26c83-127">**Элемент Fragment**</span><span class="sxs-lookup"><span data-stu-id="26c83-127">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="26c83-128">**Смартплайлист, элемент**</span><span class="sxs-lookup"><span data-stu-id="26c83-128">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="26c83-129">**Саурцефилтер, элемент**</span><span class="sxs-lookup"><span data-stu-id="26c83-129">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="26c83-130">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="26c83-130">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





