---
title: Список воспроизведения. getNextSelectedItem2
description: Метод getNextSelectedItem2 извлекает индекс следующего выбранного элемента списка воспроизведения после указанного индекса.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- Проигрыватель Windows Media Player. getNextSelectedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704133"
---
# <a name="playlistgetnextselecteditem2"></a><span data-ttu-id="96387-104">Список воспроизведения. getNextSelectedItem2</span><span class="sxs-lookup"><span data-stu-id="96387-104">PLAYLIST.getNextSelectedItem2</span></span>

<span data-ttu-id="96387-105">Метод **getNextSelectedItem2** извлекает индекс следующего выбранного элемента списка воспроизведения после указанного индекса.</span><span class="sxs-lookup"><span data-stu-id="96387-105">The **getNextSelectedItem2** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="96387-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96387-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96387-107"><span id="item"></span><span id="ITEM"></span>*детализирован*</span><span class="sxs-lookup"><span data-stu-id="96387-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="96387-108">**Число** (**Long**), указывающее индекс элемента для поиска после.</span><span class="sxs-lookup"><span data-stu-id="96387-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96387-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96387-109">Return Value</span></span>

<span data-ttu-id="96387-110">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="96387-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="96387-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96387-111">Remarks</span></span>

<span data-ttu-id="96387-112">Этот метод может работать с вложенными списками воспроизведения и заменять метод **жетнекстселектедитем** , который не может.</span><span class="sxs-lookup"><span data-stu-id="96387-112">This method can work with nested playlists and replaces the **getNextSelectedItem** method, which cannot.</span></span> <span data-ttu-id="96387-113">Передайте 1 в параметре *Item* , чтобы найти первый выбранный элемент.</span><span class="sxs-lookup"><span data-stu-id="96387-113">Pass  1 in the *item* parameter to find the first selected item.</span></span> <span data-ttu-id="96387-114">Если другие элементы не выбраны, возвращается-1.</span><span class="sxs-lookup"><span data-stu-id="96387-114">When there are no further selected items, -1 is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="96387-115">Требования</span><span class="sxs-lookup"><span data-stu-id="96387-115">Requirements</span></span>



| <span data-ttu-id="96387-116">Требование</span><span class="sxs-lookup"><span data-stu-id="96387-116">Requirement</span></span> | <span data-ttu-id="96387-117">Значение</span><span class="sxs-lookup"><span data-stu-id="96387-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="96387-118">Версия</span><span class="sxs-lookup"><span data-stu-id="96387-118">Version</span></span><br/> | <span data-ttu-id="96387-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="96387-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96387-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96387-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96387-121">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="96387-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="96387-122">**Список воспроизведения. Жетнекстселектедитем**</span><span class="sxs-lookup"><span data-stu-id="96387-122">**PLAYLIST.getNextSelectedItem**</span></span>](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





