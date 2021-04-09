---
title: Сообщение LB_SETHORIZONTALEXTENT (Winuser. h)
description: Задает ширину (в пикселях), на которую окно списка можно прокручивать горизонтально (прокручиваемую ширину).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- Элементы управления Windows для LB_SETHORIZONTALEXTENT сообщений
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892462"
---
# <a name="lb_sethorizontalextent-message"></a><span data-ttu-id="8852a-104">Сообщение сесоризонталекстент балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="8852a-104">LB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="8852a-105">Задает ширину (в пикселях), на которую окно списка можно прокручивать горизонтально (прокручиваемую ширину).</span><span class="sxs-lookup"><span data-stu-id="8852a-105">Sets the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="8852a-106">Если ширина списка меньше этого значения, горизонтальная полоса прокрутки горизонтально прокручивает элементы списка.</span><span class="sxs-lookup"><span data-stu-id="8852a-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="8852a-107">Если ширина окна списка равна или больше этого значения, то горизонтальная полоса прокрутки скрыта.</span><span class="sxs-lookup"><span data-stu-id="8852a-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="8852a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8852a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8852a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8852a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8852a-110">Указывает число пикселей, на которое можно прокручивать список.</span><span class="sxs-lookup"><span data-stu-id="8852a-110">Specifies the number of pixels by which the list box can be scrolled.</span></span>

<span data-ttu-id="8852a-111">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="8852a-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span>

</dd> <dt>

<span data-ttu-id="8852a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8852a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8852a-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="8852a-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8852a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8852a-114">Return value</span></span>

<span data-ttu-id="8852a-115">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8852a-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8852a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8852a-116">Remarks</span></span>

<span data-ttu-id="8852a-117">Чтобы ответить на сообщение **\_ сесоризонталекстент балансировки нагрузки** , список должен быть определен с помощью стиля [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="8852a-117">To respond to the **LB\_SETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="8852a-118">Обратите внимание, что окно списка не обновляет горизонтальный экстент динамически.</span><span class="sxs-lookup"><span data-stu-id="8852a-118">Note that a list box does not update its horizontal extent dynamically.</span></span>

<span data-ttu-id="8852a-119">Это сообщение не влияет на список с несколькими столбцами.</span><span class="sxs-lookup"><span data-stu-id="8852a-119">This message has no effect on a multiple-column list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="8852a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8852a-120">Requirements</span></span>



| <span data-ttu-id="8852a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8852a-121">Requirement</span></span> | <span data-ttu-id="8852a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8852a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8852a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8852a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8852a-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8852a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8852a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8852a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8852a-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8852a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8852a-127">Header</span><span class="sxs-lookup"><span data-stu-id="8852a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8852a-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8852a-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8852a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8852a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8852a-130">**жесоризонталекстент балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="8852a-130">**LB\_GETHORIZONTALEXTENT**</span></span>](lb-gethorizontalextent.md)
</dt> </dl>

 

