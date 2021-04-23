---
title: Список воспроизведения. setSelectedState2
description: Метод setSelectedState2 задает выбранное состояние элемента с указанным индексом в элементе списка воспроизведения.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- Проигрыватель Windows Media Player. setSelectedState2
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658135"
---
# <a name="playlistsetselectedstate2"></a><span data-ttu-id="6428f-104">Список воспроизведения. setSelectedState2</span><span class="sxs-lookup"><span data-stu-id="6428f-104">PLAYLIST.setSelectedState2</span></span>

<span data-ttu-id="6428f-105">Метод **setSelectedState2** задает выбранное состояние элемента с указанным индексом в элементе **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="6428f-105">The **setSelectedState2** method sets the selected state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a><span data-ttu-id="6428f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6428f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6428f-107"><span id="item"></span><span id="ITEM"></span>*детализирован*</span><span class="sxs-lookup"><span data-stu-id="6428f-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="6428f-108">**Число** (**длинное**), указывающее индекс элемента в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6428f-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="6428f-109"><span id="selected"></span><span id="SELECTED"></span>*выбрать*</span><span class="sxs-lookup"><span data-stu-id="6428f-109"><span id="selected"></span><span id="SELECTED"></span>*selected*</span></span>
</dt> <dd>

<span data-ttu-id="6428f-110">**Логическое значение** , указывающее, должен ли заданный элемент быть выбран (true) или невыбранным (false).</span><span class="sxs-lookup"><span data-stu-id="6428f-110">**Boolean** indicating whether the specified item is to be selected (true) or unselected (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6428f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6428f-111">Return Value</span></span>

<span data-ttu-id="6428f-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6428f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6428f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6428f-113">Remarks</span></span>

<span data-ttu-id="6428f-114">Этот метод может работать с вложенными списками воспроизведения и заменять метод **сетселектедстате** , который не может.</span><span class="sxs-lookup"><span data-stu-id="6428f-114">This method can work with nested playlists and replaces the **setSelectedState** method which cannot.</span></span> <span data-ttu-id="6428f-115">Вы можете задать для всех элементов запрошенное состояние, указав значение 1 в параметре *Item* .</span><span class="sxs-lookup"><span data-stu-id="6428f-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6428f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6428f-116">Requirements</span></span>



| <span data-ttu-id="6428f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6428f-117">Requirement</span></span> | <span data-ttu-id="6428f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6428f-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6428f-119">Версия</span><span class="sxs-lookup"><span data-stu-id="6428f-119">Version</span></span><br/> | <span data-ttu-id="6428f-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6428f-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6428f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6428f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6428f-122">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="6428f-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="6428f-123">**Список воспроизведения. Сетселектедстате**</span><span class="sxs-lookup"><span data-stu-id="6428f-123">**PLAYLIST.setSelectedState**</span></span>](playlist-setselectedstate.md)
</dt> </dl>

 

 





