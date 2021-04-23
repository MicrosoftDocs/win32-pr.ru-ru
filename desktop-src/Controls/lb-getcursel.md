---
title: Сообщение LB_GETCURSEL (Winuser. h)
description: Возвращает индекс выбранного в данный момент элемента, если он имеется, в списке с единственным выбором.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- Элементы управления Windows для LB_GETCURSEL сообщений
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071969"
---
# <a name="lb_getcursel-message"></a><span data-ttu-id="fd3e8-104">\_Сообщение с НЕрекурсивной балансировкой нагрузки</span><span class="sxs-lookup"><span data-stu-id="fd3e8-104">LB\_GETCURSEL message</span></span>

<span data-ttu-id="fd3e8-105">Возвращает индекс выбранного в данный момент элемента, если он имеется, в списке с единственным выбором.</span><span class="sxs-lookup"><span data-stu-id="fd3e8-105">Gets the index of the currently selected item, if any, in a single-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd3e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd3e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd3e8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd3e8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd3e8-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fd3e8-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fd3e8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd3e8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd3e8-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fd3e8-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd3e8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd3e8-111">Return value</span></span>

<span data-ttu-id="fd3e8-112">В списке с единственным выбором возвращаемое значение — это Отсчитываемый от нуля индекс текущего выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="fd3e8-112">In a single-selection list box, the return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="fd3e8-113">Если выбор отсутствует, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="fd3e8-113">If there is no selection, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd3e8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd3e8-114">Remarks</span></span>

<span data-ttu-id="fd3e8-115">Чтобы получить индексы выбранных элементов в списке с множественным выбором, используйте сообщение [**\_ жетселитемс балансировки нагрузки**](lb-getselitems.md) .</span><span class="sxs-lookup"><span data-stu-id="fd3e8-115">To retrieve the indexes of the selected items in a multiple-selection list box, use the [**LB\_GETSELITEMS**](lb-getselitems.md) message.</span></span> <span data-ttu-id="fd3e8-116">Чтобы определить, выбран ли элемент, имеющий прямоугольник фокуса в списке множественного выбора, используйте сообщение [**\_ жетсел балансировки нагрузки**](lb-getsel.md) .</span><span class="sxs-lookup"><span data-stu-id="fd3e8-116">To determine whether the item that has the focus rectangle in a multiple selection list box is selected, use the [**LB\_GETSEL**](lb-getsel.md) message.</span></span>

<span data-ttu-id="fd3e8-117">При отправке в список с множественным выбором метод **балансировки нагрузки \_** возвращает индекс элемента, имеющего прямоугольник фокуса.</span><span class="sxs-lookup"><span data-stu-id="fd3e8-117">If sent to a multiple-selection list box, **LB\_GETCURSEL** returns the index of the item that has the focus rectangle.</span></span> <span data-ttu-id="fd3e8-118">Если элементы не выбраны, возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="fd3e8-118">If no items are selected, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3e8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fd3e8-119">Requirements</span></span>



| <span data-ttu-id="fd3e8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fd3e8-120">Requirement</span></span> | <span data-ttu-id="fd3e8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fd3e8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3e8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd3e8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3e8-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd3e8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fd3e8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd3e8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3e8-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd3e8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fd3e8-126">Header</span><span class="sxs-lookup"><span data-stu-id="fd3e8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd3e8-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd3e8-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd3e8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd3e8-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd3e8-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fd3e8-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fd3e8-130">**жеткаретиндекс балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="fd3e8-130">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> <dt>

[<span data-ttu-id="fd3e8-131">**жетсел балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="fd3e8-131">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="fd3e8-132">**жетселитемс балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="fd3e8-132">**LB\_GETSELITEMS**</span></span>](lb-getselitems.md)
</dt> <dt>

[<span data-ttu-id="fd3e8-133">**сеткурсел балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="fd3e8-133">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> </dl>

 

 





