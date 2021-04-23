---
title: Seq, элемент
description: Элемент seq содержит элементы, которые определяют статический список воспроизведения или элементы, определяющие интеллектуальный список воспроизведения.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Seq, элемент Windows Media Player
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648047"
---
# <a name="seq-element"></a><span data-ttu-id="a96ef-104">Seq, элемент</span><span class="sxs-lookup"><span data-stu-id="a96ef-104">seq Element</span></span>

<span data-ttu-id="a96ef-105">Элемент **Seq** содержит элементы, которые определяют статический список воспроизведения или элементы, определяющие интеллектуальный список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a96ef-105">The **seq** element contains elements that define a static playlist or elements that define a smart playlist.</span></span>

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a><span data-ttu-id="a96ef-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a96ef-106">Attributes</span></span>

<span data-ttu-id="a96ef-107">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="a96ef-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="a96ef-108">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a96ef-108">Parent/Child Elements</span></span>



| <span data-ttu-id="a96ef-109">Иерархия</span><span class="sxs-lookup"><span data-stu-id="a96ef-109">Hierarchy</span></span> | <span data-ttu-id="a96ef-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="a96ef-110">Elements</span></span>                                                               |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="a96ef-111">Parent</span><span class="sxs-lookup"><span data-stu-id="a96ef-111">Parent</span></span>    | [<span data-ttu-id="a96ef-112">body</span><span class="sxs-lookup"><span data-stu-id="a96ef-112">body</span></span>](body-element.md)                                               |
| <span data-ttu-id="a96ef-113">Дочерний</span><span class="sxs-lookup"><span data-stu-id="a96ef-113">Child</span></span>     | <span data-ttu-id="a96ef-114">[носитель](media-element.md), [смартплайлист](smartplaylist-element.md)</span><span class="sxs-lookup"><span data-stu-id="a96ef-114">[media](media-element.md), [smartPlaylist](smartplaylist-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a96ef-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a96ef-115">Remarks</span></span>

<span data-ttu-id="a96ef-116">Если элемент **Seq** содержит только элементы **мультимедиа** , которые ссылаются на определенные элементы мультимедиа, список воспроизведения считается статическим.</span><span class="sxs-lookup"><span data-stu-id="a96ef-116">When a **seq** element only contains **media** elements that reference specific media items, the playlist is considered to be static.</span></span> <span data-ttu-id="a96ef-117">Если элемент **Seq** содержит элемент **смартплайлист** , он считается динамическим «интеллектуальным» списком воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a96ef-117">When a **seq** element contains a **smartPlaylist** element, it is considered to be a dynamic "smart" playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="a96ef-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="a96ef-118">Examples</span></span>


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a><span data-ttu-id="a96ef-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a96ef-119">Requirements</span></span>



| <span data-ttu-id="a96ef-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a96ef-120">Requirement</span></span> | <span data-ttu-id="a96ef-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a96ef-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="a96ef-122">Версия</span><span class="sxs-lookup"><span data-stu-id="a96ef-122">Version</span></span><br/> | <span data-ttu-id="a96ef-123">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a96ef-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a96ef-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a96ef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a96ef-125">**Элемент Body**</span><span class="sxs-lookup"><span data-stu-id="a96ef-125">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="a96ef-126">**Элемент Media**</span><span class="sxs-lookup"><span data-stu-id="a96ef-126">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="a96ef-127">**Смартплайлист, элемент**</span><span class="sxs-lookup"><span data-stu-id="a96ef-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="a96ef-128">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a96ef-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





