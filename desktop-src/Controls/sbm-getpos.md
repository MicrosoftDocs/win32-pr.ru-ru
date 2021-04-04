---
title: Сообщение SBM_GETPOS (Winuser. h)
description: Сообщение СБМ \_ жетпос отправляется для получения текущей позицией бегунка элемента управления "полоса прокрутки".
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- Элементы управления Windows для SBM_GETPOS сообщений
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989068"
---
# <a name="sbm_getpos-message"></a><span data-ttu-id="fa469-104">\_Сообщение СБМ жетпос</span><span class="sxs-lookup"><span data-stu-id="fa469-104">SBM\_GETPOS message</span></span>

<span data-ttu-id="fa469-105">Сообщение **СБМ \_ жетпос** отправляется для получения текущей позицией бегунка элемента управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="fa469-105">The **SBM\_GETPOS** message is sent to retrieve the current position of the scroll box of a scroll bar control.</span></span> <span data-ttu-id="fa469-106">Текущая величина — это относительное значение, которое зависит от текущего диапазона прокрутки.</span><span class="sxs-lookup"><span data-stu-id="fa469-106">The current position is a relative value that depends on the current scrolling range.</span></span> <span data-ttu-id="fa469-107">Например, если диапазон прокрутки находится в диапазоне от 0 до 100, а поле прокрутки находится в середине линейки, текущее расположение равно 50.</span><span class="sxs-lookup"><span data-stu-id="fa469-107">For example, if the scrolling range is 0 through 100 and the scroll box is in the middle of the bar, the current position is 50.</span></span>

<span data-ttu-id="fa469-108">Приложения не должны отсылать это сообщение напрямую.</span><span class="sxs-lookup"><span data-stu-id="fa469-108">Applications should not send this message directly.</span></span> <span data-ttu-id="fa469-109">Вместо этого они должны использовать функцию [**жетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="fa469-109">Instead, they should use the [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) function.</span></span> <span data-ttu-id="fa469-110">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fa469-110">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="fa469-111">Приложения, которые реализуют пользовательский элемент управления "полоса прокрутки", должны отвечать на эти сообщения, чтобы функция **жетскроллпос** работала правильно.</span><span class="sxs-lookup"><span data-stu-id="fa469-111">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollPos** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa469-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa469-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa469-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa469-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa469-114">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fa469-114">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fa469-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa469-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa469-116">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fa469-116">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa469-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa469-117">Return value</span></span>

<span data-ttu-id="fa469-118">Возвращаемое значение является текущей позицией ползунка полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="fa469-118">The return value is the current position of the scroll box in the scroll bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa469-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fa469-119">Requirements</span></span>



| <span data-ttu-id="fa469-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fa469-120">Requirement</span></span> | <span data-ttu-id="fa469-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fa469-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa469-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa469-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fa469-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa469-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa469-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa469-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fa469-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa469-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa469-126">Header</span><span class="sxs-lookup"><span data-stu-id="fa469-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa469-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa469-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa469-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa469-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa469-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fa469-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa469-130">**СБМ \_**</span><span class="sxs-lookup"><span data-stu-id="fa469-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="fa469-131">**СБМ \_ сетпос**</span><span class="sxs-lookup"><span data-stu-id="fa469-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="fa469-132">**СБМ \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="fa469-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="fa469-133">**СБМ \_ сетранжередрав**</span><span class="sxs-lookup"><span data-stu-id="fa469-133">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

