---
title: Сообщение LB_SELITEMRANGE (Winuser. h)
description: Выбирает или отменяет выбор одного или нескольких последовательных элементов в списке с множественным выбором.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- Элементы управления Windows для LB_SELITEMRANGE сообщений
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071912"
---
# <a name="lb_selitemrange-message"></a><span data-ttu-id="64626-104">Сообщение селитемранже балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="64626-104">LB\_SELITEMRANGE message</span></span>

<span data-ttu-id="64626-105">Выбирает или отменяет выбор одного или нескольких последовательных элементов в списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="64626-105">Selects or deselects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="64626-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="64626-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64626-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64626-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64626-108">**Значение true** , чтобы выбрать диапазон элементов, или **false** , чтобы снять его выделение.</span><span class="sxs-lookup"><span data-stu-id="64626-108">**TRUE** to select the range of items, or **FALSE** to deselect it.</span></span>

</dd> <dt>

<span data-ttu-id="64626-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64626-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64626-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) Указывает отсчитываемый от нуля индекс первого выбираемого элемента.</span><span class="sxs-lookup"><span data-stu-id="64626-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the first item to select.</span></span> <span data-ttu-id="64626-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Указывает отсчитываемый от нуля индекс последнего выбираемого элемента.</span><span class="sxs-lookup"><span data-stu-id="64626-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64626-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64626-112">Return value</span></span>

<span data-ttu-id="64626-113">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="64626-113">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="64626-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64626-114">Remarks</span></span>

<span data-ttu-id="64626-115">Это сообщение следует использовать только в списках с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="64626-115">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="64626-116">Это сообщение может выбрать диапазон только в пределах первых 65 536 элементов.</span><span class="sxs-lookup"><span data-stu-id="64626-116">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="64626-117">Требования</span><span class="sxs-lookup"><span data-stu-id="64626-117">Requirements</span></span>



| <span data-ttu-id="64626-118">Требование</span><span class="sxs-lookup"><span data-stu-id="64626-118">Requirement</span></span> | <span data-ttu-id="64626-119">Значение</span><span class="sxs-lookup"><span data-stu-id="64626-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64626-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64626-120">Minimum supported client</span></span><br/> | <span data-ttu-id="64626-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64626-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64626-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64626-122">Minimum supported server</span></span><br/> | <span data-ttu-id="64626-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64626-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64626-124">Header</span><span class="sxs-lookup"><span data-stu-id="64626-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="64626-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64626-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64626-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64626-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="64626-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="64626-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64626-128">**селитемранжеекс балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="64626-128">**LB\_SELITEMRANGEEX**</span></span>](lb-selitemrangeex.md)
</dt> <dt>

[<span data-ttu-id="64626-129">**сетсел балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="64626-129">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> <dt>

<span data-ttu-id="64626-130">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="64626-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="64626-131">**макелпарам**</span><span class="sxs-lookup"><span data-stu-id="64626-131">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

