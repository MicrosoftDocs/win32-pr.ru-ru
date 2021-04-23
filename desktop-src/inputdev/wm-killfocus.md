---
title: Сообщение WM_KILLFOCUS (Winuser. h)
description: Посылается окну непосредственно перед тем, как оно теряет фокус клавиатуры.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- WM_KILLFOCUS ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071487"
---
# <a name="wm_killfocus-message"></a><span data-ttu-id="87f11-104">\_Сообщение КИЛЛФОКУС WM</span><span class="sxs-lookup"><span data-stu-id="87f11-104">WM\_KILLFOCUS message</span></span>

<span data-ttu-id="87f11-105">Посылается окну непосредственно перед тем, как оно теряет фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="87f11-105">Sent to a window immediately before it loses the keyboard focus.</span></span>


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a><span data-ttu-id="87f11-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87f11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f11-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87f11-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87f11-108">Маркер окна, получающего фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="87f11-108">A handle to the window that receives the keyboard focus.</span></span> <span data-ttu-id="87f11-109">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="87f11-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87f11-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87f11-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87f11-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="87f11-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f11-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87f11-112">Return value</span></span>

<span data-ttu-id="87f11-113">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="87f11-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="87f11-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87f11-114">Remarks</span></span>

<span data-ttu-id="87f11-115">Если приложение отображает курсор, в этот момент курсор должен быть разрушен.</span><span class="sxs-lookup"><span data-stu-id="87f11-115">If an application is displaying a caret, the caret should be destroyed at this point.</span></span>

<span data-ttu-id="87f11-116">При обработке этого сообщения не следует выполнять вызовы функций, которые отображают или активируют окно.</span><span class="sxs-lookup"><span data-stu-id="87f11-116">While processing this message, do not make any function calls that display or activate a window.</span></span> <span data-ttu-id="87f11-117">Это приводит к тому, что поток получает управление и может привести к тому, что приложение перестает отвечать на сообщения.</span><span class="sxs-lookup"><span data-stu-id="87f11-117">This causes the thread to yield control and can cause the application to stop responding to messages.</span></span> <span data-ttu-id="87f11-118">Дополнительные сведения см. в разделе [взаимоблокировки сообщений](/windows/desktop/winmsg/about-messages-and-message-queues).</span><span class="sxs-lookup"><span data-stu-id="87f11-118">For more information, see [Message Deadlocks](/windows/desktop/winmsg/about-messages-and-message-queues).</span></span>

## <a name="requirements"></a><span data-ttu-id="87f11-119">Требования</span><span class="sxs-lookup"><span data-stu-id="87f11-119">Requirements</span></span>



| <span data-ttu-id="87f11-120">Требование</span><span class="sxs-lookup"><span data-stu-id="87f11-120">Requirement</span></span> | <span data-ttu-id="87f11-121">Значение</span><span class="sxs-lookup"><span data-stu-id="87f11-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f11-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87f11-122">Minimum supported client</span></span><br/> | <span data-ttu-id="87f11-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87f11-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="87f11-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87f11-124">Minimum supported server</span></span><br/> | <span data-ttu-id="87f11-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87f11-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87f11-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="87f11-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f11-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87f11-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f11-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87f11-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="87f11-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="87f11-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="87f11-130">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="87f11-130">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="87f11-131">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="87f11-131">**WM\_SETFOCUS**</span></span>](wm-setfocus.md)
</dt> <dt>

<span data-ttu-id="87f11-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="87f11-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="87f11-133">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="87f11-133">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

