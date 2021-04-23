---
title: Список воспроизведения. Жетнекстчеккедитем
description: Метод Жетнекстчеккедитем извлекает индекс следующего отмеченного элемента списка воспроизведения после указанного индекса.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- Проигрыватель Windows Media Player. Жетнекстчеккедитем
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704139"
---
# <a name="playlistgetnextcheckeditem"></a><span data-ttu-id="3e673-104">Список воспроизведения. Жетнекстчеккедитем</span><span class="sxs-lookup"><span data-stu-id="3e673-104">PLAYLIST.getNextCheckedItem</span></span>

<span data-ttu-id="3e673-105">Метод **жетнекстчеккедитем** извлекает индекс следующего отмеченного элемента списка воспроизведения после указанного индекса.</span><span class="sxs-lookup"><span data-stu-id="3e673-105">The **getNextCheckedItem** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="3e673-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e673-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e673-107"><span id="item"></span><span id="ITEM"></span>*детализирован*</span><span class="sxs-lookup"><span data-stu-id="3e673-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="3e673-108">**Число** (**Long**), указывающее индекс элемента для поиска после.</span><span class="sxs-lookup"><span data-stu-id="3e673-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e673-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e673-109">Return Value</span></span>

<span data-ttu-id="3e673-110">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="3e673-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e673-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e673-111">Remarks</span></span>

<span data-ttu-id="3e673-112">Если элементы, помеченные флажками, отсутствуют, этот метод возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="3e673-112">When there are no further checked items, this method returns  1.</span></span>

<span data-ttu-id="3e673-113">Этот метод был заменен **getNextCheckedItem2**, который поддерживает вложенные списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3e673-113">This method has been replaced by **getNextCheckedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e673-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3e673-114">Requirements</span></span>



| <span data-ttu-id="3e673-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3e673-115">Requirement</span></span> | <span data-ttu-id="3e673-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3e673-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3e673-117">Версия</span><span class="sxs-lookup"><span data-stu-id="3e673-117">Version</span></span><br/> | <span data-ttu-id="3e673-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3e673-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e673-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e673-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e673-120">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="3e673-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="3e673-121">**Список воспроизведения. getNextCheckedItem2**</span><span class="sxs-lookup"><span data-stu-id="3e673-121">**PLAYLIST.getNextCheckedItem2**</span></span>](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





