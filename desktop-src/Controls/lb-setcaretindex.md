---
title: Сообщение LB_SETCARETINDEX (Winuser. h)
description: Задает прямоугольник фокуса для элемента по указанному индексу в списке с множественным выбором. Если элемент не отображается, он прокручивается в представление.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- Элементы управления Windows для LB_SETCARETINDEX сообщений
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892465"
---
# <a name="lb_setcaretindex-message"></a><span data-ttu-id="b2ea7-105">Сообщение сеткаретиндекс балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="b2ea7-105">LB\_SETCARETINDEX message</span></span>

<span data-ttu-id="b2ea7-106">Задает прямоугольник фокуса для элемента по указанному индексу в списке с множественным выбором.</span><span class="sxs-lookup"><span data-stu-id="b2ea7-106">Sets the focus rectangle to the item at the specified index in a multiple-selection list box.</span></span> <span data-ttu-id="b2ea7-107">Если элемент не отображается, он прокручивается в представление.</span><span class="sxs-lookup"><span data-stu-id="b2ea7-107">If the item is not visible, it is scrolled into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2ea7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2ea7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2ea7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2ea7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2ea7-110">Указывает отсчитываемый от нуля индекс элемента списка, который должен получать прямоугольник фокуса.</span><span class="sxs-lookup"><span data-stu-id="b2ea7-110">Specifies the zero-based index of the list box item that is to receive the focus rectangle.</span></span>

<span data-ttu-id="b2ea7-111">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="b2ea7-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="b2ea7-112">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="b2ea7-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="b2ea7-113">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="b2ea7-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="b2ea7-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2ea7-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2ea7-115">Если это значение равно **false**, элемент прокручивается до тех пор, пока он не будет полностью виден; Если значение равно **true**, элемент прокручивается, пока не будет частично видимым.</span><span class="sxs-lookup"><span data-stu-id="b2ea7-115">If this value is **FALSE**, the item is scrolled until it is fully visible; if it is **TRUE**, the item is scrolled until it is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2ea7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2ea7-116">Return value</span></span>

<span data-ttu-id="b2ea7-117">Если возникает ошибка, возвращается значение фунтов \_ Err (-1).</span><span class="sxs-lookup"><span data-stu-id="b2ea7-117">If an error occurs, the return value is LB\_ERR (-1).</span></span> <span data-ttu-id="b2ea7-118">В противном случае возвращается значение ПЛОТности \_ (0).</span><span class="sxs-lookup"><span data-stu-id="b2ea7-118">Otherwise, LB\_OKAY (0) is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2ea7-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2ea7-119">Remarks</span></span>

<span data-ttu-id="b2ea7-120">Если это сообщение отправляется в список с единственным выбором, в котором не содержится выбранный элемент, то для индекса курсора задается элемент, указанный параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="b2ea7-120">If this message is sent to a single-selection list box that does not contain a selected item, the caret index is set to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="b2ea7-121">Если список с одним выбором содержит выбранный элемент, список будет возвращать ошибку балансировки нагрузки \_ .</span><span class="sxs-lookup"><span data-stu-id="b2ea7-121">If the single-selection list box does contain a selected item, the list box returns LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ea7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b2ea7-122">Requirements</span></span>



| <span data-ttu-id="b2ea7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b2ea7-123">Requirement</span></span> | <span data-ttu-id="b2ea7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b2ea7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ea7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2ea7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b2ea7-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2ea7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b2ea7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2ea7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b2ea7-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2ea7-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b2ea7-129">Header</span><span class="sxs-lookup"><span data-stu-id="b2ea7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2ea7-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2ea7-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2ea7-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2ea7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ea7-132">**жеткаретиндекс балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="b2ea7-132">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> </dl>

 

 





