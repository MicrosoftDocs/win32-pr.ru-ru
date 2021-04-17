---
title: Элемент Media
description: Элемент Media указывает один из элементов мультимедиа в списке воспроизведения.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Проигрыватель Windows Media, элемент мультимедиа
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651573"
---
# <a name="media-element"></a><span data-ttu-id="11a33-104">Элемент Media</span><span class="sxs-lookup"><span data-stu-id="11a33-104">media Element</span></span>

<span data-ttu-id="11a33-105">Элемент **Media** указывает один из элементов мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="11a33-105">The **media** element specifies one of the media items in a playlist.</span></span>

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a><span data-ttu-id="11a33-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="11a33-106">Attributes</span></span>



| <span data-ttu-id="11a33-107">Термин</span><span class="sxs-lookup"><span data-stu-id="11a33-107">Term</span></span>                                                                                                                       | <span data-ttu-id="11a33-108">Описание</span><span class="sxs-lookup"><span data-stu-id="11a33-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a33-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="11a33-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (required)</span></span> <br/> | <span data-ttu-id="11a33-110">URL-адрес элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="11a33-110">The URL of a media item.</span></span><br/>                                                              |
| <span data-ttu-id="11a33-111"><span id="cid"></span><span id="CID"></span>**согласуется**</span><span class="sxs-lookup"><span data-stu-id="11a33-111"><span id="cid"></span><span id="CID"></span>**cid**</span></span><br/>                                                             | <span data-ttu-id="11a33-112">ИДЕНТИФИКАТОР содержимого, уникальный для этого элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="11a33-112">The content ID that is unique to this media item.</span></span><br/>                                     |
| <span data-ttu-id="11a33-113"><span id="tid"></span><span id="TID"></span>**TID**</span><span class="sxs-lookup"><span data-stu-id="11a33-113"><span id="tid"></span><span id="TID"></span>**tid**</span></span><br/>                                                             | <span data-ttu-id="11a33-114">ИДЕНТИФИКАТОР отслеживания, который можно использовать для отслеживания объекта файловой системы для этого элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="11a33-114">The tracking ID that can be used to track the File System Object for this media item.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="11a33-115">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="11a33-115">Parent/Child Elements</span></span>



| <span data-ttu-id="11a33-116">Иерархия</span><span class="sxs-lookup"><span data-stu-id="11a33-116">Hierarchy</span></span> | <span data-ttu-id="11a33-117">Элементы</span><span class="sxs-lookup"><span data-stu-id="11a33-117">Elements</span></span>               |
|-----------|------------------------|
| <span data-ttu-id="11a33-118">Parent</span><span class="sxs-lookup"><span data-stu-id="11a33-118">Parent</span></span>    | [<span data-ttu-id="11a33-119">порядк</span><span class="sxs-lookup"><span data-stu-id="11a33-119">seq</span></span>](seq-element.md) |
| <span data-ttu-id="11a33-120">Дочерний</span><span class="sxs-lookup"><span data-stu-id="11a33-120">Child</span></span>     | <span data-ttu-id="11a33-121">None</span><span class="sxs-lookup"><span data-stu-id="11a33-121">None</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="11a33-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="11a33-122">Remarks</span></span>

<span data-ttu-id="11a33-123">Атрибут **CID** (идентификатор содержимого) заполняется проигрывателем Windows Media как способ уникальной идентификации фрагмента мультимедийного содержимого, даже если его атрибуты метаданных были изменены.</span><span class="sxs-lookup"><span data-stu-id="11a33-123">The **cid** attribute (the content ID) is populated by the Windows Media Player as a way to uniquely identify a piece of media content even if its metadata attributes have been changed.</span></span> <span data-ttu-id="11a33-124">Это позволяет предоставлять общий доступ к спискам воспроизведения на разных компьютерах, так как содержимое можно идентифицировать на другом компьютере, а путь к нему можно восстановить с помощью списка воспроизведения Windows Media.</span><span class="sxs-lookup"><span data-stu-id="11a33-124">This allows the sharing of playlists across computers, because the content can be identified on another computer, and the path to it can be "auto-repaired" by the Windows Media Playlist.</span></span> <span data-ttu-id="11a33-125">Атрибут **tid** (идентификатор отслеживания) использует файловую систему Windows для автоматического восстановления пути к носителю при изменении имени или расположения файла.</span><span class="sxs-lookup"><span data-stu-id="11a33-125">The **tid** attribute (the tracking ID) uses the Windows file system to auto-repair the path to the media if the name or location of the file is changed.</span></span>

## <a name="examples"></a><span data-ttu-id="11a33-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="11a33-126">Examples</span></span>


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a><span data-ttu-id="11a33-127">Требования</span><span class="sxs-lookup"><span data-stu-id="11a33-127">Requirements</span></span>



| <span data-ttu-id="11a33-128">Требование</span><span class="sxs-lookup"><span data-stu-id="11a33-128">Requirement</span></span> | <span data-ttu-id="11a33-129">Значение</span><span class="sxs-lookup"><span data-stu-id="11a33-129">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="11a33-130">Версия</span><span class="sxs-lookup"><span data-stu-id="11a33-130">Version</span></span><br/> | <span data-ttu-id="11a33-131">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="11a33-131">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11a33-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11a33-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a33-133">**Seq, элемент**</span><span class="sxs-lookup"><span data-stu-id="11a33-133">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="11a33-134">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="11a33-134">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





