---
title: Элемент title (WPL)
description: Элемент Title указывает название списка воспроизведения.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Элемент title (WPL) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704503"
---
# <a name="title-element-wpl"></a><span data-ttu-id="97bb0-104">Элемент title (WPL)</span><span class="sxs-lookup"><span data-stu-id="97bb0-104">title Element (WPL)</span></span>

<span data-ttu-id="97bb0-105">Элемент **Title** указывает название списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="97bb0-105">The **title** element specifies a title for the playlist.</span></span>

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a><span data-ttu-id="97bb0-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="97bb0-106">Attributes</span></span>

<span data-ttu-id="97bb0-107">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="97bb0-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="97bb0-108">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="97bb0-108">Parent/Child Elements</span></span>



| <span data-ttu-id="97bb0-109">Иерархия</span><span class="sxs-lookup"><span data-stu-id="97bb0-109">Hierarchy</span></span> | <span data-ttu-id="97bb0-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="97bb0-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="97bb0-111">Parent</span><span class="sxs-lookup"><span data-stu-id="97bb0-111">Parent</span></span>    | [<span data-ttu-id="97bb0-112">Глава</span><span class="sxs-lookup"><span data-stu-id="97bb0-112">head</span></span>](head-element.md) |
| <span data-ttu-id="97bb0-113">Дочерний</span><span class="sxs-lookup"><span data-stu-id="97bb0-113">Child</span></span>     | <span data-ttu-id="97bb0-114">None</span><span class="sxs-lookup"><span data-stu-id="97bb0-114">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="97bb0-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="97bb0-115">Remarks</span></span>

<span data-ttu-id="97bb0-116">При выборе заголовка для списка воспроизведения Windows Media (WPL) следует учесть, что содержимое списка воспроизведения может быть динамическим.</span><span class="sxs-lookup"><span data-stu-id="97bb0-116">When choosing a title for a Windows Media Playlist (WPL), consider that the content of the playlist can be dynamic.</span></span> <span data-ttu-id="97bb0-117">Хорошим подходом является основа заголовка логики в элементах **Argument** , так как именно это определяет содержимое списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="97bb0-117">A good approach is to base the title on the logic in the **argument** elements because this is what defines the content of the playlist.</span></span> <span data-ttu-id="97bb0-118">В качестве примера можно привести «мой любимый рок — песни из 1966» или «Dance песни, которые я не воспроизводил».</span><span class="sxs-lookup"><span data-stu-id="97bb0-118">Examples of this are "My Favorite Rock Songs from 1966" or "Dance Songs That I Haven't Played Recently".</span></span>

## <a name="examples"></a><span data-ttu-id="97bb0-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="97bb0-119">Examples</span></span>


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a><span data-ttu-id="97bb0-120">Требования</span><span class="sxs-lookup"><span data-stu-id="97bb0-120">Requirements</span></span>



| <span data-ttu-id="97bb0-121">Требование</span><span class="sxs-lookup"><span data-stu-id="97bb0-121">Requirement</span></span> | <span data-ttu-id="97bb0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="97bb0-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="97bb0-123">Версия</span><span class="sxs-lookup"><span data-stu-id="97bb0-123">Version</span></span><br/> | <span data-ttu-id="97bb0-124">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="97bb0-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97bb0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97bb0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97bb0-126">**Элемент Argument**</span><span class="sxs-lookup"><span data-stu-id="97bb0-126">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="97bb0-127">**Элемент head**</span><span class="sxs-lookup"><span data-stu-id="97bb0-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="97bb0-128">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="97bb0-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





