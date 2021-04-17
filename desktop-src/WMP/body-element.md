---
title: Элемент Body
description: Элемент Body содержит элементы, определяющие содержимое списка воспроизведения.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Проигрыватель Windows Media, элемент Body
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698867"
---
# <a name="body-element"></a><span data-ttu-id="0fefa-104">Элемент Body</span><span class="sxs-lookup"><span data-stu-id="0fefa-104">body Element</span></span>

<span data-ttu-id="0fefa-105">Элемент **Body** содержит элементы, определяющие содержимое списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0fefa-105">The **body** element contains the elements that define the contents of a playlist.</span></span>

``` syntax
<body>
</body>
```

## <a name="attributes"></a><span data-ttu-id="0fefa-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0fefa-106">Attributes</span></span>

<span data-ttu-id="0fefa-107">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0fefa-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="0fefa-108">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0fefa-108">Parent/Child Elements</span></span>



| <span data-ttu-id="0fefa-109">Иерархия</span><span class="sxs-lookup"><span data-stu-id="0fefa-109">Hierarchy</span></span> | <span data-ttu-id="0fefa-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="0fefa-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="0fefa-111">Parent</span><span class="sxs-lookup"><span data-stu-id="0fefa-111">Parent</span></span>    | [<span data-ttu-id="0fefa-112">SMIL</span><span class="sxs-lookup"><span data-stu-id="0fefa-112">smil</span></span>](smil-element.md) |
| <span data-ttu-id="0fefa-113">Дочерний</span><span class="sxs-lookup"><span data-stu-id="0fefa-113">Child</span></span>     | [<span data-ttu-id="0fefa-114">порядк</span><span class="sxs-lookup"><span data-stu-id="0fefa-114">seq</span></span>](seq-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="0fefa-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fefa-115">Remarks</span></span>

<span data-ttu-id="0fefa-116">Содержимое списка воспроизведения упорядочено внутри элемента **Seq** , который содержится в элементе **Body** .</span><span class="sxs-lookup"><span data-stu-id="0fefa-116">The contents of a playlist are organized within a **seq** element that is contained within the **body** element.</span></span> <span data-ttu-id="0fefa-117">Обычно существует либо один элемент **Seq** , который определяет статический набор элементов мультимедиа и содержит элементы **мультимедиа** , либо один, который определяет динамический набор элементов мультимедиа и содержит элемент **смартплайлист** .</span><span class="sxs-lookup"><span data-stu-id="0fefa-117">Typically there is either one **seq** element that defines a static set of media items and contains **media** elements, or there is one that defines a dynamic set of media items and contains a **smartPlaylist** element.</span></span>

## <a name="examples"></a><span data-ttu-id="0fefa-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="0fefa-118">Examples</span></span>


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a><span data-ttu-id="0fefa-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0fefa-119">Requirements</span></span>



| <span data-ttu-id="0fefa-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0fefa-120">Requirement</span></span> | <span data-ttu-id="0fefa-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0fefa-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="0fefa-122">Версия</span><span class="sxs-lookup"><span data-stu-id="0fefa-122">Version</span></span><br/> | <span data-ttu-id="0fefa-123">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0fefa-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fefa-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fefa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fefa-125">**Элемент Media**</span><span class="sxs-lookup"><span data-stu-id="0fefa-125">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="0fefa-126">**Seq, элемент**</span><span class="sxs-lookup"><span data-stu-id="0fefa-126">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="0fefa-127">**Смартплайлист, элемент**</span><span class="sxs-lookup"><span data-stu-id="0fefa-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="0fefa-128">**SMIL, элемент**</span><span class="sxs-lookup"><span data-stu-id="0fefa-128">**smil Element**</span></span>](smil-element.md)
</dt> <dt>

[<span data-ttu-id="0fefa-129">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0fefa-129">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





