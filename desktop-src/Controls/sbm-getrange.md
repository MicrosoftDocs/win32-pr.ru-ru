---
title: Сообщение SBM_GETRANGE (Winuser. h)
description: Сообщение СБМ \_ -Range отправляется для получения минимального и максимального значений позиционирования для элемента управления "полоса прокрутки".
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- Элементы управления Windows для SBM_GETRANGE сообщений
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989067"
---
# <a name="sbm_getrange-message"></a><span data-ttu-id="ad17e-104">Сообщение СБМного \_ диапазона</span><span class="sxs-lookup"><span data-stu-id="ad17e-104">SBM\_GETRANGE message</span></span>

<span data-ttu-id="ad17e-105">Сообщение **СБМ- \_ Range** отправляется для получения минимального и максимального значений позиционирования для элемента управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="ad17e-105">The **SBM\_GETRANGE** message is sent to retrieve the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="ad17e-106">Приложения не должны отсылать это сообщение напрямую.</span><span class="sxs-lookup"><span data-stu-id="ad17e-106">Applications should not send this message directly.</span></span> <span data-ttu-id="ad17e-107">Вместо этого они должны использовать функцию [**жетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="ad17e-107">Instead, they should use the [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) function.</span></span> <span data-ttu-id="ad17e-108">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ad17e-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="ad17e-109">Приложения, которые реализуют пользовательский элемент управления "полоса прокрутки", должны отвечать на эти сообщения, чтобы функция **жетскроллранже** работала правильно.</span><span class="sxs-lookup"><span data-stu-id="ad17e-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad17e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad17e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad17e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad17e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad17e-112">Указатель на переменную, которая получает минимальное расположение прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ad17e-112">Pointer to a variable that receives the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="ad17e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad17e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad17e-114">Указатель на переменную, которая получает максимальное значение позиции прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ad17e-114">Pointer to a variable that receives the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad17e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad17e-115">Return value</span></span>

<span data-ttu-id="ad17e-116">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ad17e-116">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad17e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ad17e-117">Requirements</span></span>



| <span data-ttu-id="ad17e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ad17e-118">Requirement</span></span> | <span data-ttu-id="ad17e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ad17e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad17e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad17e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ad17e-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad17e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ad17e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad17e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ad17e-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad17e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad17e-124">Header</span><span class="sxs-lookup"><span data-stu-id="ad17e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad17e-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad17e-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad17e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad17e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad17e-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ad17e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad17e-128">**СБМ \_ жетпос**</span><span class="sxs-lookup"><span data-stu-id="ad17e-128">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="ad17e-129">**СБМ \_ сетпос**</span><span class="sxs-lookup"><span data-stu-id="ad17e-129">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="ad17e-130">**СБМ \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="ad17e-130">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="ad17e-131">**СБМ \_ сетранжередрав**</span><span class="sxs-lookup"><span data-stu-id="ad17e-131">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

