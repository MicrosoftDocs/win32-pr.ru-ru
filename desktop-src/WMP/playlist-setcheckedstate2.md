---
title: Список воспроизведения. setCheckedState2
description: Метод setCheckedState2 устанавливает состояние Checked элемента с указанным индексом в элементе списка воспроизведения.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- Проигрыватель Windows Media Player. setCheckedState2
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704119"
---
# <a name="playlistsetcheckedstate2"></a><span data-ttu-id="9fa05-104">Список воспроизведения. setCheckedState2</span><span class="sxs-lookup"><span data-stu-id="9fa05-104">PLAYLIST.setCheckedState2</span></span>

<span data-ttu-id="9fa05-105">Метод **setCheckedState2** устанавливает состояние Checked элемента с указанным индексом в элементе **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="9fa05-105">The **setCheckedState2** method sets the checked state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a><span data-ttu-id="9fa05-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fa05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fa05-107"><span id="item"></span><span id="ITEM"></span>*детализирован*</span><span class="sxs-lookup"><span data-stu-id="9fa05-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="9fa05-108">**Число** (**длинное**), указывающее индекс элемента списка воспроизведения, который должен быть установлен или снят.</span><span class="sxs-lookup"><span data-stu-id="9fa05-108">**Number** (**long**) indicating the index of the playlist item to be checked or unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="9fa05-109"><span id="checked"></span><span id="CHECKED"></span>*отмечен*</span><span class="sxs-lookup"><span data-stu-id="9fa05-109"><span id="checked"></span><span id="CHECKED"></span>*checked*</span></span>
</dt> <dd>

<span data-ttu-id="9fa05-110">**Логическое значение** , указывающее, должен ли заданный элемент проверяться (true) или неустановленным (false).</span><span class="sxs-lookup"><span data-stu-id="9fa05-110">**Boolean** indicating whether the specified item is to be checked (true) or unchecked (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fa05-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fa05-111">Return Value</span></span>

<span data-ttu-id="9fa05-112">Этот метод возвращает **логическое значение**.</span><span class="sxs-lookup"><span data-stu-id="9fa05-112">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fa05-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fa05-113">Remarks</span></span>

<span data-ttu-id="9fa05-114">Этот метод может работать с вложенными списками воспроизведения и заменять метод **сетчеккедстате** , который не может.</span><span class="sxs-lookup"><span data-stu-id="9fa05-114">This method can work with nested playlists and replaces the **setCheckedState** method, which cannot.</span></span> <span data-ttu-id="9fa05-115">Вы можете задать для всех элементов запрошенное состояние, указав значение 1 в параметре *Item* .</span><span class="sxs-lookup"><span data-stu-id="9fa05-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa05-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9fa05-116">Requirements</span></span>



| <span data-ttu-id="9fa05-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9fa05-117">Requirement</span></span> | <span data-ttu-id="9fa05-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9fa05-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="9fa05-119">Версия</span><span class="sxs-lookup"><span data-stu-id="9fa05-119">Version</span></span><br/> | <span data-ttu-id="9fa05-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9fa05-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fa05-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fa05-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa05-122">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="9fa05-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="9fa05-123">**Список воспроизведения. Сетчеккедстате**</span><span class="sxs-lookup"><span data-stu-id="9fa05-123">**PLAYLIST.setCheckedState**</span></span>](playlist-setcheckedstate.md)
</dt> </dl>

 

 





