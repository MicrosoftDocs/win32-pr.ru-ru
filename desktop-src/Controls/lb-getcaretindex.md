---
title: Сообщение LB_GETCARETINDEX (Winuser. h)
description: Извлекает индекс элемента, который находится в фокусе, в списке с множественным выбором. Элемент может быть или не выбран.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- Элементы управления Windows для LB_GETCARETINDEX сообщений
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071970"
---
# <a name="lb_getcaretindex-message"></a><span data-ttu-id="afacb-105">Сообщение жеткаретиндекс балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="afacb-105">LB\_GETCARETINDEX message</span></span>

<span data-ttu-id="afacb-106">Извлекает индекс элемента, который находится в фокусе, в списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="afacb-106">Retrieves the index of the item that has the focus in a multiple-selection list box.</span></span> <span data-ttu-id="afacb-107">Элемент может быть или не выбран.</span><span class="sxs-lookup"><span data-stu-id="afacb-107">The item may or may not be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="afacb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="afacb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afacb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afacb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afacb-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="afacb-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="afacb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afacb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afacb-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="afacb-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afacb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afacb-113">Return value</span></span>

<span data-ttu-id="afacb-114">Возвращаемое значение — это Отсчитываемый от нуля индекс элемента списка с фокусом или 0, если ни один элемент не имеет фокуса.</span><span class="sxs-lookup"><span data-stu-id="afacb-114">The return value is the zero-based index of the focused list box item, or 0 if no item has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="afacb-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afacb-115">Remarks</span></span>

<span data-ttu-id="afacb-116">Это сообщение также может использоваться для получения индекса элемента, выбранного в данный момент в списке с одним выбором.</span><span class="sxs-lookup"><span data-stu-id="afacb-116">This message can also be used to get the index of the item that is currently selected in a single-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="afacb-117">Требования</span><span class="sxs-lookup"><span data-stu-id="afacb-117">Requirements</span></span>



| <span data-ttu-id="afacb-118">Требование</span><span class="sxs-lookup"><span data-stu-id="afacb-118">Requirement</span></span> | <span data-ttu-id="afacb-119">Значение</span><span class="sxs-lookup"><span data-stu-id="afacb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afacb-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afacb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="afacb-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afacb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="afacb-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afacb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="afacb-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="afacb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="afacb-124">Header</span><span class="sxs-lookup"><span data-stu-id="afacb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="afacb-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afacb-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afacb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afacb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afacb-127">**сеткаретиндекс балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="afacb-127">**LB\_SETCARETINDEX**</span></span>](lb-setcaretindex.md)
</dt> </dl>

 

 





