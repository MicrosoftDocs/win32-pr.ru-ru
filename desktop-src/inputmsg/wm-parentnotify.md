---
title: Сообщение WM_PARENTNOTIFY
description: Отправляется в окно при возникновении значительных действий в окне-потомке.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- WM_PARENTNOTIFY сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534706"
---
# <a name="wm_parentnotify-message"></a><span data-ttu-id="8b1cf-104">Сообщение WM_PARENTNOTIFY</span><span class="sxs-lookup"><span data-stu-id="8b1cf-104">WM_PARENTNOTIFY message</span></span>

<span data-ttu-id="8b1cf-105">Отправляется в окно при возникновении значительных действий в окне-потомке.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-105">Sent to a window when a significant action occurs on a descendant window.</span></span> <span data-ttu-id="8b1cf-106">Теперь это сообщение расширено для включения события [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="8b1cf-106">This message is now extended to include the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span> <span data-ttu-id="8b1cf-107">При создании дочернего окна система отправляет [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) непосредственно перед функцией [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , которая создает окно.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-107">When the child window is being created, the system sends [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) just before the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function that creates the window returns.</span></span> <span data-ttu-id="8b1cf-108">При уничтожении дочернего окна система отправляет сообщение перед любой обработкой, чтобы уничтожить окно.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-108">When the child window is being destroyed, the system sends the message before any processing to destroy the window takes place.</span></span>

<span data-ttu-id="8b1cf-109">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8b1cf-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="8b1cf-110">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="8b1cf-110">\[!Important\]</span></span>  
> <span data-ttu-id="8b1cf-111">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="8b1cf-112">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="8b1cf-113">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="8b1cf-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="8b1cf-114">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b1cf-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a><span data-ttu-id="8b1cf-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b1cf-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b1cf-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b1cf-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b1cf-117">Младшее слово параметра *wParam* указывает событие, для которого будет уведомлен родительский объект.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-117">The low-order word of *wParam* specifies the event for which the parent is being notified.</span></span> <span data-ttu-id="8b1cf-118">Значение слова высокого порядка зависит от значения младшего слова.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-118">The value of the high-order word depends on the value of the low-order word.</span></span> <span data-ttu-id="8b1cf-119">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-119">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8b1cf-120">ЛОВОРД (*wParam*)</span><span class="sxs-lookup"><span data-stu-id="8b1cf-120">LOWORD(*wParam*)</span></span>                                                                                                                                                                                                             | <span data-ttu-id="8b1cf-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8b1cf-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <span data-ttu-id="8b1cf-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="8b1cf-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span></span> </dl>                | <span data-ttu-id="8b1cf-123">Создается дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-123">The child window is being created.</span></span><br/> <span data-ttu-id="8b1cf-124">HIWORD (*wParam*) — это идентификатор дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-124">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="8b1cf-125">*lParam* — это маркер дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-125">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <span data-ttu-id="8b1cf-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="8b1cf-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span></span> </dl>             | <span data-ttu-id="8b1cf-127">Дочернее окно уничтожается.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-127">The child window is being destroyed.</span></span><br/> <span data-ttu-id="8b1cf-128">HIWORD (*wParam*) — это идентификатор дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-128">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="8b1cf-129">*lParam* — это маркер дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-129">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <span data-ttu-id="8b1cf-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span><span class="sxs-lookup"><span data-stu-id="8b1cf-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span></span> </dl> | <span data-ttu-id="8b1cf-131">Пользователь поместил курсор над дочерним окном и щелкнул левую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-131">The user has placed the cursor over the child window and has clicked the left mouse button.</span></span><br/> <span data-ttu-id="8b1cf-132">HIWORD (*wParam*) не определен.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-132">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="8b1cf-133">*lParam* — это слово в виде нижнего порядка по оси x, а координата y курсора — это слово в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-133">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <span data-ttu-id="8b1cf-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span><span class="sxs-lookup"><span data-stu-id="8b1cf-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span></span> </dl> | <span data-ttu-id="8b1cf-135">Пользователь поместил курсор над дочерним окном и щелкнул среднюю кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-135">The user has placed the cursor over the child window and has clicked the middle mouse button.</span></span><br/> <span data-ttu-id="8b1cf-136">HIWORD (*wParam*) не определен.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-136">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="8b1cf-137">*lParam* — это слово в виде нижнего порядка по оси x, а координата y курсора — это слово в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-137">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <span data-ttu-id="8b1cf-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span><span class="sxs-lookup"><span data-stu-id="8b1cf-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span></span> </dl> | <span data-ttu-id="8b1cf-139">Пользователь поместил курсор над дочерним окном и щелкнул правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-139">The user has placed the cursor over the child window and has clicked the right mouse button.</span></span><br/> <span data-ttu-id="8b1cf-140">HIWORD (*wParam*) не определен.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-140">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="8b1cf-141">*lParam* — это слово в виде нижнего порядка по оси x, а координата y курсора — это слово в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-141">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <span data-ttu-id="8b1cf-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span><span class="sxs-lookup"><span data-stu-id="8b1cf-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span></span> </dl> | <span data-ttu-id="8b1cf-143">Пользователь поместил курсор над дочерним окном и щелкнул первую или вторую кнопку X.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-143">The user has placed the cursor over the child window and has clicked the first or second X button.</span></span><br/> <span data-ttu-id="8b1cf-144">HIWORD (*wParam*) указывает, какая кнопка была нажата.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-144">HIWORD(*wParam*) indicates which button was pressed.</span></span> <span data-ttu-id="8b1cf-145">Этот параметр может принимать одно из следующих значений: XBUTTON1 или XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-145">This parameter can be one of the following values: XBUTTON1 or XBUTTON2.</span></span><br/> <span data-ttu-id="8b1cf-146">*lParam* — это слово в виде нижнего порядка по оси x, а координата y курсора — это слово в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-146">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <span data-ttu-id="8b1cf-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span><span class="sxs-lookup"><span data-stu-id="8b1cf-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span></span> </dl> | <span data-ttu-id="8b1cf-148">Указатель сделал связь с дочерним окном.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-148">A pointer has made contact with the child window.</span></span><br/> <span data-ttu-id="8b1cf-149">HIWORD (*wParam*) содержит идентификатор указателя, создавшего событие [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="8b1cf-149">HIWORD(*wParam*) contains the identifier of the pointer that generated the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span><br/>                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="8b1cf-150">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b1cf-150">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b1cf-151">Содержит расположение точки указателя.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-151">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="8b1cf-152">Так как указатель может установить связь с устройством в нетривиальной области, это расположение может быть упрощено более сложной областью указателя.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-152">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="8b1cf-153">Когда это возможно, приложение должно использовать полные сведения об области указателя, а не расположение точки.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-153">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="8b1cf-154">Используйте следующие макросы, чтобы получить физические экранные координаты точки.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-154">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="8b1cf-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): координата X (горизонтальная точка).</span><span class="sxs-lookup"><span data-stu-id="8b1cf-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="8b1cf-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): координата Y (вертикальная точка).</span><span class="sxs-lookup"><span data-stu-id="8b1cf-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b1cf-157">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b1cf-157">Return value</span></span>

<span data-ttu-id="8b1cf-158">Если приложение обрабатывает это сообщение, оно возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-158">If the application processes this message, it returns zero.</span></span>

<span data-ttu-id="8b1cf-159">Если приложение не обрабатывает это сообщение, оно вызывает [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="8b1cf-159">If the application does not process this message, it calls [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b1cf-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b1cf-160">Remarks</span></span>

<span data-ttu-id="8b1cf-161">Это сообщение также отправляется во все окна предков дочернего окна, включая окно верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-161">This message is also sent to all ancestor windows of the child window, including the top-level window.</span></span>

<span data-ttu-id="8b1cf-162">Все дочерние окна, кроме тех, которые имеют расширенный стиль окна **WS_EX_NOPARENTNOTIFY** , отправляют это сообщение в родительские окна.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-162">All child windows, except those that have the **WS_EX_NOPARENTNOTIFY** extended window style, send this message to their parent windows.</span></span> <span data-ttu-id="8b1cf-163">По умолчанию дочерние окна в диалоговом окне имеют стиль **WS_EX_NOPARENTNOTIFY** , если только не вызвана функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) для создания дочернего окна без этого стиля.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-163">By default, child windows in a dialog box have the **WS_EX_NOPARENTNOTIFY** style, unless the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function is called to create the child window without this style.</span></span>

<span data-ttu-id="8b1cf-164">Это уведомление предоставляет в качестве предка дочернего окна возможность проверить сведения о указателе и, при необходимости, захватить указатель с помощью функций захвата указателя.</span><span class="sxs-lookup"><span data-stu-id="8b1cf-164">This notification provides the child window's ancestor windows an opportunity to examine the pointer information and, if required, capture the pointer using the pointer capture functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1cf-165">Требования</span><span class="sxs-lookup"><span data-stu-id="8b1cf-165">Requirements</span></span>



| <span data-ttu-id="8b1cf-166">Требование</span><span class="sxs-lookup"><span data-stu-id="8b1cf-166">Requirement</span></span> | <span data-ttu-id="8b1cf-167">Значение</span><span class="sxs-lookup"><span data-stu-id="8b1cf-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1cf-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b1cf-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8b1cf-169">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8b1cf-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="8b1cf-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b1cf-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8b1cf-171">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8b1cf-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b1cf-172">Header</span><span class="sxs-lookup"><span data-stu-id="8b1cf-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b1cf-173"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b1cf-173"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b1cf-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b1cf-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1cf-175">Сообщения</span><span class="sxs-lookup"><span data-stu-id="8b1cf-175">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="8b1cf-176">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="8b1cf-176">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="8b1cf-177">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="8b1cf-177">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

<span data-ttu-id="8b1cf-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b1cf-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8b1cf-179">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b1cf-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8b1cf-180">**WM_CREATE**</span><span class="sxs-lookup"><span data-stu-id="8b1cf-180">**WM_CREATE**</span></span>](../winmsg/wm-create.md)
</dt> <dt>

[<span data-ttu-id="8b1cf-181">**WM_DESTROY**</span><span class="sxs-lookup"><span data-stu-id="8b1cf-181">**WM_DESTROY**</span></span>](../winmsg/wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="8b1cf-182">**WM_LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="8b1cf-182">**WM_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="8b1cf-183">**WM_MBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="8b1cf-183">**WM_MBUTTONDOWN**</span></span>](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[<span data-ttu-id="8b1cf-184">**WM_RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="8b1cf-184">**WM_RBUTTONDOWN**</span></span>](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[<span data-ttu-id="8b1cf-185">**WM_XBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="8b1cf-185">**WM_XBUTTONDOWN**</span></span>](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

