---
title: Элемент meta
description: Элемент meta указывает метаданные, которые применяются ко всему списку воспроизведения.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Проигрыватель Windows Media, элемент meta
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651816"
---
# <a name="meta-element"></a><span data-ttu-id="471c8-104">Элемент meta</span><span class="sxs-lookup"><span data-stu-id="471c8-104">meta Element</span></span>

<span data-ttu-id="471c8-105">Элемент **meta** указывает метаданные, которые применяются ко всему списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="471c8-105">The **meta** element specifies metadata that applies to the entire playlist.</span></span>

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a><span data-ttu-id="471c8-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="471c8-106">Attributes</span></span>



| <span data-ttu-id="471c8-107">Термин</span><span class="sxs-lookup"><span data-stu-id="471c8-107">Term</span></span>                                                                       | <span data-ttu-id="471c8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="471c8-108">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="471c8-109"><span id="name"></span><span id="NAME"></span>**безымян**</span><span class="sxs-lookup"><span data-stu-id="471c8-109"><span id="name"></span><span id="NAME"></span>**name**</span></span><br/>          | <span data-ttu-id="471c8-110">Имя элемента метаданных.</span><span class="sxs-lookup"><span data-stu-id="471c8-110">The name of an item of metadata.</span></span><br/>                                                                                       |
| <span data-ttu-id="471c8-111"><span id="content"></span><span id="CONTENT"></span>**содержани**</span><span class="sxs-lookup"><span data-stu-id="471c8-111"><span id="content"></span><span id="CONTENT"></span>**content**</span></span><br/> | <span data-ttu-id="471c8-112">Значение элемента метаданных.</span><span class="sxs-lookup"><span data-stu-id="471c8-112">The value of an item of metadata.</span></span> <span data-ttu-id="471c8-113">Например, если атрибут name имеет значение «жанр», атрибут содержимого может иметь значение «рок».</span><span class="sxs-lookup"><span data-stu-id="471c8-113">For example, if the name attribute is "Genre" the content attribute could be "Rock".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="471c8-114">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="471c8-114">Parent/Child Elements</span></span>



| <span data-ttu-id="471c8-115">Иерархия</span><span class="sxs-lookup"><span data-stu-id="471c8-115">Hierarchy</span></span> | <span data-ttu-id="471c8-116">Элементы</span><span class="sxs-lookup"><span data-stu-id="471c8-116">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="471c8-117">Parent</span><span class="sxs-lookup"><span data-stu-id="471c8-117">Parent</span></span>    | [<span data-ttu-id="471c8-118">Глава</span><span class="sxs-lookup"><span data-stu-id="471c8-118">head</span></span>](head-element.md) |
| <span data-ttu-id="471c8-119">Дочерний</span><span class="sxs-lookup"><span data-stu-id="471c8-119">Child</span></span>     | <span data-ttu-id="471c8-120">None</span><span class="sxs-lookup"><span data-stu-id="471c8-120">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="471c8-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="471c8-121">Remarks</span></span>

<span data-ttu-id="471c8-122">Создатель списка воспроизведения Windows Media может задать для атрибута Name элемента meta любую строку.</span><span class="sxs-lookup"><span data-stu-id="471c8-122">The creator of a Windows Media Playlist can set the name attribute of a meta element to any string.</span></span> <span data-ttu-id="471c8-123">В следующем списке показаны некоторые стандартные атрибуты имени, которые находятся в списках воспроизведения Windows Media, созданных проигрывателем Windows Media и другими компонентами Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="471c8-123">The following list shows some typical name attributes that are found in Windows Media Playlists created by Windows Media Player and other Microsoft components.</span></span>

-   <span data-ttu-id="471c8-124">Автор</span><span class="sxs-lookup"><span data-stu-id="471c8-124">Author</span></span>
-   <span data-ttu-id="471c8-125">Категория</span><span class="sxs-lookup"><span data-stu-id="471c8-125">Category</span></span>
-   <span data-ttu-id="471c8-126">Genre</span><span class="sxs-lookup"><span data-stu-id="471c8-126">Genre</span></span>
-   <span data-ttu-id="471c8-127">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="471c8-127">UserName</span></span>
-   <span data-ttu-id="471c8-128">UserRating</span><span class="sxs-lookup"><span data-stu-id="471c8-128">UserRating</span></span>
-   <span data-ttu-id="471c8-129">Generator</span><span class="sxs-lookup"><span data-stu-id="471c8-129">Generator</span></span>

## <a name="examples"></a><span data-ttu-id="471c8-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="471c8-130">Examples</span></span>


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="471c8-131">Требования</span><span class="sxs-lookup"><span data-stu-id="471c8-131">Requirements</span></span>



| <span data-ttu-id="471c8-132">Требование</span><span class="sxs-lookup"><span data-stu-id="471c8-132">Requirement</span></span> | <span data-ttu-id="471c8-133">Значение</span><span class="sxs-lookup"><span data-stu-id="471c8-133">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="471c8-134">Версия</span><span class="sxs-lookup"><span data-stu-id="471c8-134">Version</span></span><br/> | <span data-ttu-id="471c8-135">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="471c8-135">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="471c8-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="471c8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471c8-137">**Элемент head**</span><span class="sxs-lookup"><span data-stu-id="471c8-137">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="471c8-138">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="471c8-138">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





