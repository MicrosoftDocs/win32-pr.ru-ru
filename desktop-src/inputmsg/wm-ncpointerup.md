---
title: Сообщение WM_NCPOINTERUP
description: Передается, когда указатель, который был направлен через неклиентскую область окна, прерывает контакт.
ms.assetid: 4bdc11da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUP сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_NCPOINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a875814b51558c20de47eeee525f6dd35f716fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803082"
---
# <a name="wm_ncpointerup-message"></a><span data-ttu-id="a7399-104">Сообщение WM_NCPOINTERUP</span><span class="sxs-lookup"><span data-stu-id="a7399-104">WM_NCPOINTERUP message</span></span>

<span data-ttu-id="a7399-105">Передается, когда указатель, который был направлен через неклиентскую область окна, прерывает контакт.</span><span class="sxs-lookup"><span data-stu-id="a7399-105">Posted when a pointer that made contact over the non-client area of a window breaks contact.</span></span> <span data-ttu-id="a7399-106">Сообщение предназначено для окна, на которое указатель устанавливает контакт, и указатель на этот момент неявно записывается в окно, чтобы окно продолжало принимать входные данные для указателя до тех пор, пока не будет прерывать контакт, включая уведомление **WM_NCPOINTERUP** .</span><span class="sxs-lookup"><span data-stu-id="a7399-106">The message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact, including the **WM_NCPOINTERUP** notification.</span></span>

<span data-ttu-id="a7399-107">Если окно захватило этот указатель, это сообщение не будет отправлено.</span><span class="sxs-lookup"><span data-stu-id="a7399-107">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="a7399-108">Вместо этого в окно, которое захватило этот указатель, отправляется [**WM_POINTERUP**](wm-pointerup.md) .</span><span class="sxs-lookup"><span data-stu-id="a7399-108">Instead, a [**WM_POINTERUP**](wm-pointerup.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="a7399-109">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="a7399-109">\[!Important\]</span></span>  
> <span data-ttu-id="a7399-110">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="a7399-110">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="a7399-111">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="a7399-111">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="a7399-112">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="a7399-112">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="a7399-113">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a7399-113">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUP               0x0243
```



## <a name="parameters"></a><span data-ttu-id="a7399-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7399-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7399-115">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7399-115">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7399-116">Содержит идентификатор указателя и дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a7399-116">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="a7399-117">Используйте следующие макросы для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="a7399-117">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="a7399-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): идентификатор указателя</span><span class="sxs-lookup"><span data-stu-id="a7399-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="a7399-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): значение проверки попадания, возвращаемое при обработке сообщения [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="a7399-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="a7399-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7399-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7399-121">Содержит расположение точки указателя.</span><span class="sxs-lookup"><span data-stu-id="a7399-121">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="a7399-122">Так как указатель может установить связь с устройством в нетривиальной области, это расположение может быть упрощено более сложной областью указателя.</span><span class="sxs-lookup"><span data-stu-id="a7399-122">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="a7399-123">Когда это возможно, приложение должно использовать полные сведения об области указателя, а не расположение точки.</span><span class="sxs-lookup"><span data-stu-id="a7399-123">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="a7399-124">Используйте следующие макросы, чтобы получить физические экранные координаты точки.</span><span class="sxs-lookup"><span data-stu-id="a7399-124">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="a7399-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): координата X (горизонтальная точка).</span><span class="sxs-lookup"><span data-stu-id="a7399-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="a7399-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): координата Y (вертикальная точка).</span><span class="sxs-lookup"><span data-stu-id="a7399-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7399-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7399-127">Return value</span></span>

<span data-ttu-id="a7399-128">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="a7399-128">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="a7399-129">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="a7399-129">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7399-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7399-130">Remarks</span></span>

<span data-ttu-id="a7399-131">Если приложение не обрабатывает это сообщение, [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca) может выполнить одно или несколько системных действий в зависимости от результата проверки попадания, включенного в сообщение.</span><span class="sxs-lookup"><span data-stu-id="a7399-131">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="a7399-132">Как правило, приложениям не нужно выполнять обработку этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="a7399-132">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7399-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a7399-133">Requirements</span></span>



| <span data-ttu-id="a7399-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a7399-134">Requirement</span></span> | <span data-ttu-id="a7399-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a7399-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7399-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7399-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a7399-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a7399-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a7399-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7399-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a7399-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a7399-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a7399-140">Header</span><span class="sxs-lookup"><span data-stu-id="a7399-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7399-141"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7399-141"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7399-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7399-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7399-143">Сообщения</span><span class="sxs-lookup"><span data-stu-id="a7399-143">Messages</span></span>](messages.md)
</dt> </dl>

 

