---
title: Список воспроизведения. getNextCheckedItem2
description: Метод getNextCheckedItem2 извлекает индекс следующего отмеченного элемента списка воспроизведения после указанного индекса.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- Проигрыватель Windows Media Player. getNextCheckedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704138"
---
# <a name="playlistgetnextcheckeditem2"></a><span data-ttu-id="8e0c8-104">Список воспроизведения. getNextCheckedItem2</span><span class="sxs-lookup"><span data-stu-id="8e0c8-104">PLAYLIST.getNextCheckedItem2</span></span>

<span data-ttu-id="8e0c8-105">Метод **getNextCheckedItem2** извлекает индекс следующего отмеченного элемента списка воспроизведения после указанного индекса.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-105">The **getNextCheckedItem2** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="8e0c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e0c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e0c8-107"><span id="item"></span><span id="ITEM"></span>*детализирован*</span><span class="sxs-lookup"><span data-stu-id="8e0c8-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="8e0c8-108">**Число** (**Long**), указывающее индекс элемента для поиска после.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e0c8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e0c8-109">Return Value</span></span>

<span data-ttu-id="8e0c8-110">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="8e0c8-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e0c8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e0c8-111">Remarks</span></span>

<span data-ttu-id="8e0c8-112">Этот метод может работать с вложенными списками воспроизведения и заменять метод **жетнекстчеккедитем** , который не может.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-112">This method can work with nested playlists and replaces the **getNextCheckedItem** method, which cannot.</span></span> <span data-ttu-id="8e0c8-113">Передайте 1 в параметре *Item* , чтобы найти первый отмеченный элемент.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-113">Pass  1 in the *item* parameter to find the first checked item.</span></span> <span data-ttu-id="8e0c8-114">Если элементы, помеченные флажками, отсутствуют, этот метод возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="8e0c8-114">When there are no further checked items, this method returns  1.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e0c8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8e0c8-115">Requirements</span></span>



| <span data-ttu-id="8e0c8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8e0c8-116">Requirement</span></span> | <span data-ttu-id="8e0c8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8e0c8-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8e0c8-118">Версия</span><span class="sxs-lookup"><span data-stu-id="8e0c8-118">Version</span></span><br/> | <span data-ttu-id="8e0c8-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8e0c8-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e0c8-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e0c8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e0c8-121">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="8e0c8-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="8e0c8-122">**Список воспроизведения. Жетнекстчеккедитем**</span><span class="sxs-lookup"><span data-stu-id="8e0c8-122">**PLAYLIST.getNextCheckedItem**</span></span>](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





