---
title: SMIL, элемент
description: Элемент smil всегда является элементом верхнего уровня в файле списка воспроизведения Windows Media (WPL). Он указывает, что в файле используется SMIL (синхронизированный язык интеграции мультимедиа) синтаксис и грамматика.
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Элемент smil Windows Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657843"
---
# <a name="smil-element"></a><span data-ttu-id="aad4a-105">SMIL, элемент</span><span class="sxs-lookup"><span data-stu-id="aad4a-105">smil Element</span></span>

<span data-ttu-id="aad4a-106">Элемент **SMIL** всегда является элементом верхнего уровня в файле списка воспроизведения Windows Media (WPL).</span><span class="sxs-lookup"><span data-stu-id="aad4a-106">The **smil** element is always the top level element in a Windows Media Playlist (WPL) file.</span></span> <span data-ttu-id="aad4a-107">Он указывает, что в файле используется SMIL (синхронизированный язык интеграции мультимедиа) синтаксис и грамматика.</span><span class="sxs-lookup"><span data-stu-id="aad4a-107">It specifies that the file uses SMIL (Synchronized Multimedia Integration Language) syntax and grammar.</span></span>

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a><span data-ttu-id="aad4a-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="aad4a-108">Attributes</span></span>

<span data-ttu-id="aad4a-109">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="aad4a-109">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="aad4a-110">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="aad4a-110">Parent/Child Elements</span></span>



| <span data-ttu-id="aad4a-111">Иерархия</span><span class="sxs-lookup"><span data-stu-id="aad4a-111">Hierarchy</span></span> | <span data-ttu-id="aad4a-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="aad4a-112">Elements</span></span>                                           |
|-----------|----------------------------------------------------|
| <span data-ttu-id="aad4a-113">Parent</span><span class="sxs-lookup"><span data-stu-id="aad4a-113">Parent</span></span>    | <span data-ttu-id="aad4a-114">Нет</span><span class="sxs-lookup"><span data-stu-id="aad4a-114">None</span></span>                                               |
| <span data-ttu-id="aad4a-115">Дочерний</span><span class="sxs-lookup"><span data-stu-id="aad4a-115">Child</span></span>     | <span data-ttu-id="aad4a-116">[головной](head-element.md), [основной текст](body-element.md)</span><span class="sxs-lookup"><span data-stu-id="aad4a-116">[head](head-element.md), [body](body-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="aad4a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aad4a-117">Remarks</span></span>

<span data-ttu-id="aad4a-118">Каждый список воспроизведения Windows Media должен иметь элемент **SMIL** в корне.</span><span class="sxs-lookup"><span data-stu-id="aad4a-118">Every Windows Media Playlist must have the **smil** element at its root.</span></span>

## <a name="examples"></a><span data-ttu-id="aad4a-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="aad4a-119">Examples</span></span>


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a><span data-ttu-id="aad4a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="aad4a-120">Requirements</span></span>



| <span data-ttu-id="aad4a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="aad4a-121">Requirement</span></span> | <span data-ttu-id="aad4a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="aad4a-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="aad4a-123">Версия</span><span class="sxs-lookup"><span data-stu-id="aad4a-123">Version</span></span><br/> | <span data-ttu-id="aad4a-124">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="aad4a-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aad4a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aad4a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad4a-126">**Элемент Body**</span><span class="sxs-lookup"><span data-stu-id="aad4a-126">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="aad4a-127">**Элемент head**</span><span class="sxs-lookup"><span data-stu-id="aad4a-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="aad4a-128">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="aad4a-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





