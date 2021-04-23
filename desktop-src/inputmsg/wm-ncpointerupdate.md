---
title: Сообщение WM_NCPOINTERUPDATE
description: Опубликовано для предоставления обновления указателя, который подключается к неклиентской области окна, или когда незахваченный контакт перемещается по неклиентской области окна.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUPDATE сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_NCPOINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 09ef5fd6f3b7378a963be4278f1fabdf0f6ab351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415288"
---
# <a name="wm_ncpointerupdate-message"></a><span data-ttu-id="f3be4-104">Сообщение WM_NCPOINTERUPDATE</span><span class="sxs-lookup"><span data-stu-id="f3be4-104">WM_NCPOINTERUPDATE message</span></span>

<span data-ttu-id="f3be4-105">Опубликовано для предоставления обновления указателя, который подключается к неклиентской области окна, или когда незахваченный контакт перемещается по неклиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="f3be4-105">Posted to provide an update on a pointer that made contact over the non-client area of a window or when a hovering uncaptured contact moves over the non-client area of a window.</span></span> <span data-ttu-id="f3be4-106">При наведении указателя мыши сообщение предназначено для любого окна, над которым происходит указатель.</span><span class="sxs-lookup"><span data-stu-id="f3be4-106">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="f3be4-107">Пока указатель находится в контакте с поверхностью, указатель неявно записывается в окно, над которым указатель сделал контакт, и это окно по---получит входные данные для указателя до тех пор, пока не будет прервано соединение.</span><span class="sxs-lookup"><span data-stu-id="f3be4-107">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="f3be4-108">Если окно захватило этот указатель, это сообщение не будет отправлено.</span><span class="sxs-lookup"><span data-stu-id="f3be4-108">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="f3be4-109">Вместо этого в окно, которое захватило этот указатель, отправляется [**WM_POINTERUPDATE**](wm-pointerupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="f3be4-109">Instead, a [**WM_POINTERUPDATE**](wm-pointerupdate.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="f3be4-110">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="f3be4-110">\[!Important\]</span></span>  
> <span data-ttu-id="f3be4-111">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="f3be4-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="f3be4-112">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="f3be4-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="f3be4-113">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="f3be4-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="f3be4-114">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3be4-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## <a name="parameters"></a><span data-ttu-id="f3be4-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3be4-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3be4-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3be4-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3be4-117">Содержит идентификатор указателя и дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f3be4-117">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="f3be4-118">Используйте следующие макросы для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="f3be4-118">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="f3be4-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): идентификатор указателя</span><span class="sxs-lookup"><span data-stu-id="f3be4-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="f3be4-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): значение проверки попадания, возвращаемое при обработке сообщения [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="f3be4-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="f3be4-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3be4-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3be4-122">Содержит расположение точки указателя.</span><span class="sxs-lookup"><span data-stu-id="f3be4-122">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="f3be4-123">Так как указатель может установить связь с устройством в нетривиальной области, это расположение может быть упрощено более сложной областью указателя.</span><span class="sxs-lookup"><span data-stu-id="f3be4-123">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="f3be4-124">Когда это возможно, приложение должно использовать полные сведения об области указателя, а не расположение точки.</span><span class="sxs-lookup"><span data-stu-id="f3be4-124">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="f3be4-125">Используйте следующие макросы, чтобы получить физические экранные координаты точки.</span><span class="sxs-lookup"><span data-stu-id="f3be4-125">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="f3be4-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): координата X (горизонтальная точка).</span><span class="sxs-lookup"><span data-stu-id="f3be4-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="f3be4-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): координата Y (вертикальная точка).</span><span class="sxs-lookup"><span data-stu-id="f3be4-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3be4-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3be4-128">Return value</span></span>

<span data-ttu-id="f3be4-129">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="f3be4-129">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="f3be4-130">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="f3be4-130">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3be4-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3be4-131">Remarks</span></span>

<span data-ttu-id="f3be4-132">Если приложение не обрабатывает это сообщение, [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca) может выполнить одно или несколько системных действий в зависимости от результата проверки попадания, включенного в сообщение.</span><span class="sxs-lookup"><span data-stu-id="f3be4-132">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="f3be4-133">Как правило, приложениям не нужно выполнять обработку этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="f3be4-133">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3be4-134">Требования</span><span class="sxs-lookup"><span data-stu-id="f3be4-134">Requirements</span></span>



| <span data-ttu-id="f3be4-135">Требование</span><span class="sxs-lookup"><span data-stu-id="f3be4-135">Requirement</span></span> | <span data-ttu-id="f3be4-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f3be4-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3be4-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3be4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f3be4-138">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f3be4-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="f3be4-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3be4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f3be4-140">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f3be4-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f3be4-141">Header</span><span class="sxs-lookup"><span data-stu-id="f3be4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3be4-142"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3be4-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3be4-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3be4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3be4-144">Сообщения</span><span class="sxs-lookup"><span data-stu-id="f3be4-144">Messages</span></span>](messages.md)
</dt> </dl>

 

