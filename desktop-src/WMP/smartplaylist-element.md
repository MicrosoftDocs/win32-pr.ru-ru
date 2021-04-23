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
# <a name="smartplaylist-element"></a><span data-ttu-id="82fbd-104">Смартплайлист, элемент</span><span class="sxs-lookup"><span data-stu-id="82fbd-104">smartPlaylist Element</span></span>

<span data-ttu-id="82fbd-105">Элемент **смартплайлист** содержит динамически определенную часть списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="82fbd-105">The **smartPlaylist** element contains the dynamically defined portion of a playlist.</span></span>

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a><span data-ttu-id="82fbd-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="82fbd-106">Attributes</span></span>



| <span data-ttu-id="82fbd-107">Термин</span><span class="sxs-lookup"><span data-stu-id="82fbd-107">Term</span></span>                                                                                                                                   | <span data-ttu-id="82fbd-108">Описание</span><span class="sxs-lookup"><span data-stu-id="82fbd-108">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82fbd-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**версия** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="82fbd-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (required)</span></span> <br/> | <span data-ttu-id="82fbd-110">Десятичное число, представляющее номер версии схемы смарт-списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="82fbd-110">The decimal number representing the version number of the smart playlist schema.</span></span> <span data-ttu-id="82fbd-111">Задайте значение 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="82fbd-111">Set to 1.0.0.0.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="82fbd-112">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="82fbd-112">Parent/Child Elements</span></span>



| <span data-ttu-id="82fbd-113">Иерархия</span><span class="sxs-lookup"><span data-stu-id="82fbd-113">Hierarchy</span></span> | <span data-ttu-id="82fbd-114">Элементы</span><span class="sxs-lookup"><span data-stu-id="82fbd-114">Elements</span></span>                                                       |
|-----------|----------------------------------------------------------------|
| <span data-ttu-id="82fbd-115">Parent</span><span class="sxs-lookup"><span data-stu-id="82fbd-115">Parent</span></span>    | [<span data-ttu-id="82fbd-116">порядк</span><span class="sxs-lookup"><span data-stu-id="82fbd-116">seq</span></span>](seq-element.md)                                         |
| <span data-ttu-id="82fbd-117">Дочерний</span><span class="sxs-lookup"><span data-stu-id="82fbd-117">Child</span></span>     | <span data-ttu-id="82fbd-118">[запрос](queryset-element.md), [Фильтр](filter-element.md)</span><span class="sxs-lookup"><span data-stu-id="82fbd-118">[querySet](queryset-element.md), [filter](filter-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="82fbd-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82fbd-119">Remarks</span></span>

<span data-ttu-id="82fbd-120">Элемент **смартплайлист** обычно содержит элемент с набором **запроса** , который также может содержать элемент **Filter** .</span><span class="sxs-lookup"><span data-stu-id="82fbd-120">A **smartPlaylist** element typically contains a **querySet** element and can also contain a **filter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="82fbd-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="82fbd-121">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="82fbd-122">Требования</span><span class="sxs-lookup"><span data-stu-id="82fbd-122">Requirements</span></span>



| <span data-ttu-id="82fbd-123">Требование</span><span class="sxs-lookup"><span data-stu-id="82fbd-123">Requirement</span></span> | <span data-ttu-id="82fbd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="82fbd-124">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="82fbd-125">Версия</span><span class="sxs-lookup"><span data-stu-id="82fbd-125">Version</span></span><br/> | <span data-ttu-id="82fbd-126">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="82fbd-126">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82fbd-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82fbd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82fbd-128">**Элемент Argument**</span><span class="sxs-lookup"><span data-stu-id="82fbd-128">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="82fbd-129">**Элемент Filter**</span><span class="sxs-lookup"><span data-stu-id="82fbd-129">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="82fbd-130">**Элемент Fragment**</span><span class="sxs-lookup"><span data-stu-id="82fbd-130">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="82fbd-131">**Элемент запроса**</span><span class="sxs-lookup"><span data-stu-id="82fbd-131">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="82fbd-132">**Seq, элемент**</span><span class="sxs-lookup"><span data-stu-id="82fbd-132">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="82fbd-133">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="82fbd-133">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





