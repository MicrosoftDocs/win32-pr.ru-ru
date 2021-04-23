---
title: Элемент head
description: Элемент head содержит метаданные, которые применяются ко всему списку воспроизведения.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Проигрыватель Windows Media, элемент головного элемента
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695096"
---
# <a name="head-element"></a><span data-ttu-id="6bc69-104">Элемент head</span><span class="sxs-lookup"><span data-stu-id="6bc69-104">head Element</span></span>

<span data-ttu-id="6bc69-105">Элемент **head** содержит метаданные, которые применяются ко всему списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6bc69-105">The **head** element contains metadata that applies to the entire playlist.</span></span>

``` syntax
<head>
</head>
```

## <a name="attributes"></a><span data-ttu-id="6bc69-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6bc69-106">Attributes</span></span>

<span data-ttu-id="6bc69-107">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="6bc69-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="6bc69-108">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6bc69-108">Parent/Child Elements</span></span>



| <span data-ttu-id="6bc69-109">Иерархия</span><span class="sxs-lookup"><span data-stu-id="6bc69-109">Hierarchy</span></span> | <span data-ttu-id="6bc69-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="6bc69-110">Elements</span></span>                                                  |
|-----------|-----------------------------------------------------------|
| <span data-ttu-id="6bc69-111">Parent</span><span class="sxs-lookup"><span data-stu-id="6bc69-111">Parent</span></span>    | [<span data-ttu-id="6bc69-112">SMIL</span><span class="sxs-lookup"><span data-stu-id="6bc69-112">smil</span></span>](smil-element.md)                                  |
| <span data-ttu-id="6bc69-113">Дочерний</span><span class="sxs-lookup"><span data-stu-id="6bc69-113">Child</span></span>     | <span data-ttu-id="6bc69-114">[Title](title-element--wpl.md), [meta](meta-element.md)</span><span class="sxs-lookup"><span data-stu-id="6bc69-114">[title](title-element--wpl.md), [meta](meta-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6bc69-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bc69-115">Remarks</span></span>

<span data-ttu-id="6bc69-116">Обычно элемент **head** содержит элемент **Title** и один или несколько элементов **meta** , определяющих глобальные характеристики списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6bc69-116">Typically the **head** element contains a **title** element and one or more **meta** elements that define global characteristics of the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="6bc69-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="6bc69-117">Examples</span></span>


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="6bc69-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6bc69-118">Requirements</span></span>



| <span data-ttu-id="6bc69-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6bc69-119">Requirement</span></span> | <span data-ttu-id="6bc69-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6bc69-120">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="6bc69-121">Версия</span><span class="sxs-lookup"><span data-stu-id="6bc69-121">Version</span></span><br/> | <span data-ttu-id="6bc69-122">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="6bc69-122">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6bc69-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bc69-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bc69-124">**Элемент meta**</span><span class="sxs-lookup"><span data-stu-id="6bc69-124">**meta Element**</span></span>](meta-element.md)
</dt> <dt>

[<span data-ttu-id="6bc69-125">**Элемент title (WPL)**</span><span class="sxs-lookup"><span data-stu-id="6bc69-125">**title Element (WPL)**</span></span>](title-element--wpl.md)
</dt> <dt>

[<span data-ttu-id="6bc69-126">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6bc69-126">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





