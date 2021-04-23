---
title: Список воспроизведения. Жетнекстселектедитем
description: Метод Жетнекстселектедитем извлекает индекс следующего выбранного элемента списка воспроизведения после указанного индекса.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- Проигрыватель Windows Media Player. Жетнекстселектедитем
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704136"
---
# <a name="playlistgetnextselecteditem"></a><span data-ttu-id="4926a-104">Список воспроизведения. Жетнекстселектедитем</span><span class="sxs-lookup"><span data-stu-id="4926a-104">PLAYLIST.getNextSelectedItem</span></span>

<span data-ttu-id="4926a-105">Метод **жетнекстселектедитем** извлекает индекс следующего выбранного элемента списка воспроизведения после указанного индекса.</span><span class="sxs-lookup"><span data-stu-id="4926a-105">The **getNextSelectedItem** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="4926a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4926a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4926a-107"><span id="item"></span><span id="ITEM"></span>*детализирован*</span><span class="sxs-lookup"><span data-stu-id="4926a-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="4926a-108">**Число** (**Long**), указывающее индекс элемента для поиска после.</span><span class="sxs-lookup"><span data-stu-id="4926a-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4926a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4926a-109">Return Value</span></span>

<span data-ttu-id="4926a-110">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="4926a-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="4926a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4926a-111">Remarks</span></span>

<span data-ttu-id="4926a-112">Если другие элементы не выбраны, этот метод возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="4926a-112">When there are no further selected items, this method returns  1.</span></span>

<span data-ttu-id="4926a-113">Этот метод был заменен **getNextSelectedItem2**, который поддерживает вложенные списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4926a-113">This method has been replaced by **getNextSelectedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="4926a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4926a-114">Requirements</span></span>



| <span data-ttu-id="4926a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4926a-115">Requirement</span></span> | <span data-ttu-id="4926a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4926a-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4926a-117">Версия</span><span class="sxs-lookup"><span data-stu-id="4926a-117">Version</span></span><br/> | <span data-ttu-id="4926a-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="4926a-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4926a-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4926a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4926a-120">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="4926a-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="4926a-121">**Список воспроизведения. getNextSelectedItem2**</span><span class="sxs-lookup"><span data-stu-id="4926a-121">**PLAYLIST.getNextSelectedItem2**</span></span>](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





