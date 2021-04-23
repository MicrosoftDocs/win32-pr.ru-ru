---
title: Сообщение WM_POINTERCAPTURECHANGED
description: Отправляется в окно, которое теряет захват входного указателя.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- WM_POINTERCAPTURECHANGED сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719211"
---
# <a name="wm_pointercapturechanged-message"></a><span data-ttu-id="64142-104">Сообщение WM_POINTERCAPTURECHANGED</span><span class="sxs-lookup"><span data-stu-id="64142-104">WM_POINTERCAPTURECHANGED message</span></span>

<span data-ttu-id="64142-105">Отправляется в окно, которое теряет захват входного указателя.</span><span class="sxs-lookup"><span data-stu-id="64142-105">Sent to a window that is losing capture of an input pointer.</span></span>

<span data-ttu-id="64142-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="64142-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a><span data-ttu-id="64142-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="64142-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64142-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64142-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64142-109">Содержит сведения о потере входного указателя.</span><span class="sxs-lookup"><span data-stu-id="64142-109">Contains information about the input pointer that is being lost.</span></span> <span data-ttu-id="64142-110">Чтобы получить идентификатор указателя, используйте [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="64142-110">Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to get the pointer ID.</span></span>

</dd> <dt>

<span data-ttu-id="64142-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64142-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64142-112">Содержит маркер окна, записывающего указатель ввода.</span><span class="sxs-lookup"><span data-stu-id="64142-112">Contains a handle to the window that is capturing the input pointer.</span></span> <span data-ttu-id="64142-113">Это значение может быть равно NULL, если это окно больше не захвачено указателем.</span><span class="sxs-lookup"><span data-stu-id="64142-113">This value can be NULL if the pointer is no longer being captured by the window.</span></span>

<span data-ttu-id="64142-114">Если это сообщение создается на основе внутренней обработки, то значением может быть маркер окна, получающего сообщение.</span><span class="sxs-lookup"><span data-stu-id="64142-114">If this message is generated from internal processing, the value can be the handle of the window receiving the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64142-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64142-115">Return value</span></span>

<span data-ttu-id="64142-116">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="64142-116">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="64142-117">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="64142-117">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="64142-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64142-118">Remarks</span></span>

<span data-ttu-id="64142-119">Окно должно использовать это уведомление для прекращения обработки последующих сообщений и инициации очистки, необходимой для потери указателя.</span><span class="sxs-lookup"><span data-stu-id="64142-119">A window should use this notification to stop processing subsequent messages and initiate any cleanup required for the pointer being lost.</span></span> <span data-ttu-id="64142-120">Обработка жестов, связанных с указателем, должна также завершаться (например, путем вызова [**стопинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)), а оставшиеся контакты повторно связаны с окном.</span><span class="sxs-lookup"><span data-stu-id="64142-120">Processing of gestures associated with the pointer should also be terminated (for example, by calling [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) and remaining contacts re-associated with the window.</span></span>

<span data-ttu-id="64142-121">Как правило, если окно получает уведомление **WM_POINTERCAPTURECHANGED** , то последующие уведомления, связанные с указателем ввода, не принимаются.</span><span class="sxs-lookup"><span data-stu-id="64142-121">Typically, if a window receives the **WM_POINTERCAPTURECHANGED** notification, no subsequent notifications related to the input pointer are received.</span></span> <span data-ttu-id="64142-122">По этой причине не следует зависеть от парных уведомлений, таких как [**WM_POINTERENTER**](wm-pointerenter.md) и [**WM_POINTERLEAVE**](wm-pointerleave.md).</span><span class="sxs-lookup"><span data-stu-id="64142-122">Because of this, do not depend on paired notifications such as [**WM_POINTERENTER**](wm-pointerenter.md) and [**WM_POINTERLEAVE**](wm-pointerleave.md).</span></span>

<span data-ttu-id="64142-123">**WM_POINTERCAPTURECHANGED** не содержит [**POINTER_INFO**](/previous-versions/windows/desktop/api) данных.</span><span class="sxs-lookup"><span data-stu-id="64142-123">**WM_POINTERCAPTURECHANGED** does not include [**POINTER_INFO**](/previous-versions/windows/desktop/api) data.</span></span> <span data-ttu-id="64142-124">В отличие от установленного флага [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) , данные, возвращаемые [**жетпоинтеринфо**](/previous-versions/windows/desktop/api) (или любым вариантом), идентичны тому, что были возвращены перед уведомлением.</span><span class="sxs-lookup"><span data-stu-id="64142-124">Other than the [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) flag being set, the data returned by [**GetPointerInfo**](/previous-versions/windows/desktop/api) (or any variant) is identical to that returned prior to the notification.</span></span>

<span data-ttu-id="64142-125">Если приложение не обрабатывает это уведомление, [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca) может создать одно или несколько [**WM_GESTURE**](../wintouch/wm-gesture.md) сообщений или, если жест не распознается, **дефвиндовпрок** может создавать ввод с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="64142-125">If the application does not process this notification, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages or, if a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="64142-126">Если приложение выборочно потребляет некоторые входные данные указателя и передает оставшуюся часть в [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca), то результирующее поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="64142-126">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="64142-127">Требования</span><span class="sxs-lookup"><span data-stu-id="64142-127">Requirements</span></span>



| <span data-ttu-id="64142-128">Требование</span><span class="sxs-lookup"><span data-stu-id="64142-128">Requirement</span></span> | <span data-ttu-id="64142-129">Значение</span><span class="sxs-lookup"><span data-stu-id="64142-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64142-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64142-130">Minimum supported client</span></span><br/> | <span data-ttu-id="64142-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="64142-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="64142-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64142-132">Minimum supported server</span></span><br/> | <span data-ttu-id="64142-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="64142-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64142-134">Header</span><span class="sxs-lookup"><span data-stu-id="64142-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="64142-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64142-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64142-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64142-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64142-137">Сообщения</span><span class="sxs-lookup"><span data-stu-id="64142-137">Messages</span></span>](messages.md)
</dt> </dl>

 

