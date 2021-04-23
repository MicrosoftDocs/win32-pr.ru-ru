---
title: Сообщение LVM_GETITEMSTATE (Коммктрл. h)
description: Возвращает состояние элемента представления списка. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемстате ListView.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- Элементы управления Windows для LVM_GETITEMSTATE сообщений
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492411"
---
# <a name="lvm_getitemstate-message"></a><span data-ttu-id="e5c85-105">\_Сообщение LVM жетитемстате</span><span class="sxs-lookup"><span data-stu-id="e5c85-105">LVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="e5c85-106">Возвращает состояние элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="e5c85-106">Retrieves the state of a list-view item.</span></span> <span data-ttu-id="e5c85-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемстате ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="e5c85-107">You can send this message explicitly or by using the [**ListView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5c85-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5c85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5c85-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c85-110">Индекс элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="e5c85-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="e5c85-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5c85-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c85-112">Сведения о состоянии для извлечения.</span><span class="sxs-lookup"><span data-stu-id="e5c85-112">State information to retrieve.</span></span> <span data-ttu-id="e5c85-113">Этот параметр может быть сочетанием следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e5c85-113">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="e5c85-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e5c85-114">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="e5c85-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e5c85-115">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="e5c85-116"><dt>**ЛВИС \_ Вырезать**</dt></span><span class="sxs-lookup"><span data-stu-id="e5c85-116"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="e5c85-117">Элемент помечен для операции вырезания и вставки.</span><span class="sxs-lookup"><span data-stu-id="e5c85-117">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="e5c85-118"><dt>**ЛВИС \_ дрофилитед**</dt></span><span class="sxs-lookup"><span data-stu-id="e5c85-118"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="e5c85-119">Элемент выделяется как цель перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="e5c85-119">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="e5c85-120"><dt>**ЛВИС \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e5c85-120"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="e5c85-121">Элемент имеет фокус, поэтому он окружается стандартным прямоугольником фокуса.</span><span class="sxs-lookup"><span data-stu-id="e5c85-121">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="e5c85-122">Хотя можно выбрать несколько элементов, фокус может быть только одного элемента.</span><span class="sxs-lookup"><span data-stu-id="e5c85-122">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="e5c85-123"><dt>**ЛВИС \_ выбрано**</dt></span><span class="sxs-lookup"><span data-stu-id="e5c85-123"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="e5c85-124">Элемент выбран.</span><span class="sxs-lookup"><span data-stu-id="e5c85-124">The item is selected.</span></span> <span data-ttu-id="e5c85-125">Внешний вид выбранного элемента зависит от того, имеет ли он фокус, а также от системных цветов, используемых для выбора.</span><span class="sxs-lookup"><span data-stu-id="e5c85-125">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="e5c85-126"><dt>**ЛВИС \_ оверлаймаск**</dt></span><span class="sxs-lookup"><span data-stu-id="e5c85-126"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="e5c85-127">Используйте эту маску для получения индекса изображения оверлея элемента.</span><span class="sxs-lookup"><span data-stu-id="e5c85-127">Use this mask to retrieve the item's overlay image index.</span></span><br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="e5c85-128"><dt>**ЛВИС \_ статеимажемаск**</dt></span><span class="sxs-lookup"><span data-stu-id="e5c85-128"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="e5c85-129">Используйте эту маску для получения индекса изображения состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e5c85-129">Use this mask to retrieve the item's state image index.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c85-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5c85-130">Return value</span></span>

<span data-ttu-id="e5c85-131">Возвращает текущее состояние указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="e5c85-131">Returns the current state for the specified item.</span></span> <span data-ttu-id="e5c85-132">Единственными допустимыми битами в возвращаемом значении являются те, которые соответствуют битам, заданным в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e5c85-132">The only valid bits in the return value are those that correspond to the bits set in the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c85-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5c85-133">Remarks</span></span>

<span data-ttu-id="e5c85-134">Сведения о состоянии элемента включают набор битовых флагов, а также индексы списка изображений, которые указывают изображение состояния элемента и изображение оверлея.</span><span class="sxs-lookup"><span data-stu-id="e5c85-134">An item's state information includes a set of bit flags as well as image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c85-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e5c85-135">Requirements</span></span>



| <span data-ttu-id="e5c85-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e5c85-136">Requirement</span></span> | <span data-ttu-id="e5c85-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e5c85-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c85-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5c85-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c85-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5c85-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e5c85-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5c85-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c85-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5c85-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5c85-142">Header</span><span class="sxs-lookup"><span data-stu-id="e5c85-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5c85-143"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c85-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c85-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5c85-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c85-145">**LVM \_ сетитемстате**</span><span class="sxs-lookup"><span data-stu-id="e5c85-145">**LVM\_SETITEMSTATE**</span></span>](lvm-setitemstate.md)
</dt> </dl>

 

 





