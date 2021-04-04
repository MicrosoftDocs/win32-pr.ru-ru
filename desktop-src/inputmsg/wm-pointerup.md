---
title: Сообщение WM_POINTERUP
description: Публикуется, когда указатель, который подключается через клиентскую область окна, прерывает контакт.
ms.assetid: 3bdc38da-227c-4be1-bf0b-99704b8a0111
keywords:
- WM_POINTERUP сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f6c23b810b7ec5a7f60ae7e52ddbb5b535ab0503
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "103999811"
---
# <a name="wm_pointerup-message"></a><span data-ttu-id="ed1c8-104">Сообщение WM_POINTERUP</span><span class="sxs-lookup"><span data-stu-id="ed1c8-104">WM_POINTERUP message</span></span>

<span data-ttu-id="ed1c8-105">Публикуется, когда указатель, который подключается через клиентскую область окна, прерывает контакт.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-105">Posted when a pointer that made contact over the client area of a window breaks contact.</span></span> <span data-ttu-id="ed1c8-106">Это входное сообщение предназначено для окна, над которым указатель устанавливает контакт, и указатель на этот момент неявно записывается в окно, чтобы окно продолжало принимать входные сообщения, включая **WM_POINTERUP** уведомления для указателя, пока не будет прервано Контактное лицо.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-106">This input message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input messages including the **WM_POINTERUP** notification for the pointer until it breaks contact.</span></span>

<span data-ttu-id="ed1c8-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ed1c8-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="ed1c8-108">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="ed1c8-108">\[!Important\]</span></span>  
> <span data-ttu-id="ed1c8-109">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="ed1c8-110">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="ed1c8-111">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="ed1c8-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="ed1c8-112">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ed1c8-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERUP                  0x0247
```



## <a name="parameters"></a><span data-ttu-id="ed1c8-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed1c8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed1c8-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed1c8-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed1c8-115">Содержит сведения об указателе.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-115">Contains information about the pointer.</span></span> <span data-ttu-id="ed1c8-116">Используйте следующие макросы для получения сведений из параметра wParam.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="ed1c8-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): идентификатор указателя.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="ed1c8-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, представляет ли данное сообщение первый вход, созданный новым указателем.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="ed1c8-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, было ли это сообщение создано указателем в течение его времени существования.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="ed1c8-120">Этот флаг не установлен для сообщений, указывающих на то, что указатель имеет диапазон обнаружения слева</span><span class="sxs-lookup"><span data-stu-id="ed1c8-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="ed1c8-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, было ли это сообщение создано указателем, который находится в связи с областью окна.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="ed1c8-122">Этот флаг не задан для сообщений, указывающих на наведение указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="ed1c8-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): указывает, что этот указатель был обозначен как первичный.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="ed1c8-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, имеется ли первичное действие.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="ed1c8-125">Это аналогично левой кнопке мыши.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="ed1c8-126">В связи с поверхностью дигитайзера этот набор будет иметь сенсорный указатель.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="ed1c8-127">Этот набор будет иметь указатель пера, если он находится в контакте с поверхностью дигитайзера без нажатия кнопок.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="ed1c8-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, есть ли вторичное действие.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="ed1c8-129">Это аналогично нажатию кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="ed1c8-130">Этот набор будет иметь указатель пера, если он в связи с поверхностью дигитайзера нажата кнопка пера.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="ed1c8-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий на наличие одного или нескольких третичных действий на основе типа указателя; приложения, которые хотят реагировать на третичные действия, должны получить информацию, относящуюся к типу указателя, чтобы определить, какие из них нажаты.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="ed1c8-132">Например, приложение может определить состояния кнопок пера, вызвав [**жетпоинтерпенинфо**](/previous-versions/windows/desktop/api) и изучив флаги, указывающие состояния кнопок.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="ed1c8-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, принял ли указанный указатель четвертое действие.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="ed1c8-134">Приложения, которые хотят реагировать на четвертые действия, должны получить сведения, относящиеся к типу указателя, чтобы определить, нажата ли первая расширенная кнопка мыши (XButton1).</span><span class="sxs-lookup"><span data-stu-id="ed1c8-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="ed1c8-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**флаг**](pointer-flags-contants.md) , указывающий, принял ли указанный указатель пятое действие.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="ed1c8-136">Приложения, которые хотят отвечать на пятое действие, должны получить информацию, относящуюся к типу указателя, чтобы определить, нажата ли вторая кнопка расширенной мыши (XButton2).</span><span class="sxs-lookup"><span data-stu-id="ed1c8-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="ed1c8-137">Дополнительные сведения см. в разделе [**Флаги указателя**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1c8-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="ed1c8-138">Указатель мыши не имеет установленного флага кнопки.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="ed1c8-139">Это аналогично перемещению мыши без кнопок мыши.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="ed1c8-140">Приложение может определить состояния кнопок для наведения указателя мыши, например путем вызова [**жетпоинтерпенинфо**](/previous-versions/windows/desktop/api) и проверки флагов, указывающих на состояния кнопок.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="ed1c8-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed1c8-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed1c8-142">Содержит расположение точки указателя.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="ed1c8-143">Так как указатель может установить связь с устройством в нетривиальной области, это расположение может быть упрощено более сложной областью указателя.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="ed1c8-144">Когда это возможно, приложение должно использовать полные сведения об области указателя, а не расположение точки.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="ed1c8-145">Используйте следующие макросы, чтобы получить физические экранные координаты точки.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="ed1c8-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): координата X (горизонтальная точка).</span><span class="sxs-lookup"><span data-stu-id="ed1c8-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="ed1c8-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): координата Y (вертикальная точка).</span><span class="sxs-lookup"><span data-stu-id="ed1c8-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed1c8-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed1c8-148">Return value</span></span>

<span data-ttu-id="ed1c8-149">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="ed1c8-150">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="ed1c8-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed1c8-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed1c8-151">Remarks</span></span>

> <span data-ttu-id="ed1c8-152">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="ed1c8-152">\[!Important\]</span></span>  
> <span data-ttu-id="ed1c8-153">Когда окно теряет указатель и получает уведомление [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , он обычно не будет получать дальнейшие уведомления.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-153">When a window loses capture of a pointer and it receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it typically will not receive any further notifications.</span></span> <span data-ttu-id="ed1c8-154">По этой причине важно не делать никаких предположений на основе равномерно связанных [**WM_POINTERDOWN**](wm-pointerdown.md) / **WM_POINTERUP** или [**WM_POINTERENTER**](wm-pointerenter.md) / уведомлений [**WM_POINTERLEAVE**](wm-pointerleave.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1c8-154">For this reason, it is important that you not make any assumptions based on evenly paired [**WM_POINTERDOWN**](wm-pointerdown.md)/**WM_POINTERUP** or [**WM_POINTERENTER**](wm-pointerenter.md)/[**WM_POINTERLEAVE**](wm-pointerleave.md) notifications.</span></span>

 

<span data-ttu-id="ed1c8-155">Каждый указатель имеет уникальный идентификатор указателя в течение своего времени существования.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-155">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="ed1c8-156">Время существования указателя начинается при первом обнаружении.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-156">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="ed1c8-157">При обнаружении указателя мыши создается [**WM_POINTERENTER**](wm-pointerenter.md) сообщение.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-157">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="ed1c8-158">При обнаружении указателя, не являющегося указателем, создается [**WM_POINTERDOWN**](wm-pointerdown.md) сообщение, за которым следует сообщение **WM_POINTERENTER** .</span><span class="sxs-lookup"><span data-stu-id="ed1c8-158">A [**WM_POINTERDOWN**](wm-pointerdown.md) message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="ed1c8-159">Во время его существования указатель может формировать ряд [**WM_POINTERUPDATE**](wm-pointerupdate.md) сообщений при наведении указателя мыши или в контакте.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-159">During its lifetime, a pointer may generate a series of [**WM_POINTERUPDATE**](wm-pointerupdate.md) messages while it is hovering or in contact.</span></span>

<span data-ttu-id="ed1c8-160">Время существования указателя заканчивается, когда он больше не обнаруживается.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-160">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="ed1c8-161">При этом создается [**WM_POINTERLEAVE**](wm-pointerleave.md) сообщение.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-161">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="ed1c8-162">При прерывании указателя задается [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1c8-162">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="ed1c8-163">Сообщение [**WM_POINTERLEAVE**](wm-pointerleave.md) также может быть создано, когда незахваченный указатель перемещается за пределы окна.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-163">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="ed1c8-164">Для получения горизонтального и вертикального расположения указателя используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ed1c8-164">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>

<span data-ttu-id="ed1c8-165">Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="ed1c8-165">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="ed1c8-166">Макрос [**макепоинтс**](/windows/win32/api/wingdi/nf-wingdi-makepoints) также можно использовать для преобразования параметра lParam в структуру [**points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ed1c8-166">The [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro can also be used to convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="ed1c8-167">Функцию [**жеткэйстате**](/windows/win32/api/winuser/nf-winuser-getkeystate) можно использовать для определения состояний клавиши модификатора клавиатуры, связанных с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-167">The [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function can be used to determine the keyboard modifier key states associated with this message.</span></span> <span data-ttu-id="ed1c8-168">Например, чтобы обнаружить, что нажата клавиша ALT, проверьте, не **жеткэйстате** ли значение 0 (VK_MENU) &lt; .</span><span class="sxs-lookup"><span data-stu-id="ed1c8-168">For example, to detect that the ALT key was pressed, check whether **GetKeyState**(VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="ed1c8-169">Если приложение не обрабатывает это сообщение, [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca) может создать одно или несколько [**WM_GESTURE**](../wintouch/wm-gesture.md)сообщений, если последовательность входных данных из этого и, возможно, других указателей распознается как жест.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-169">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md)messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="ed1c8-170">Если жест не распознан, **дефвиндовпрок** может создавать ввод с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-170">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="ed1c8-171">Если приложение выборочно потребляет некоторые входные данные указателя и передает оставшуюся часть в [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca), то результирующее поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-171">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="ed1c8-172">Используйте функцию [**жетпоинтеринфо**](/previous-versions/windows/desktop/api) для получения дополнительных сведений, относящихся к этому сообщению.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-172">Use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function to retrieve further information related to this message.</span></span>

## <a name="examples"></a><span data-ttu-id="ed1c8-173">Примеры</span><span class="sxs-lookup"><span data-stu-id="ed1c8-173">Examples</span></span>

<span data-ttu-id="ed1c8-174">В следующем примере кода показано, как получить позиции x и y указателя, связанного с данным сообщением.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-174">The following code example shows how to retrieve the x and y position of the pointer associated witht this message.</span></span>


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

// process pointer up, similar to mouse button up
```



<span data-ttu-id="ed1c8-175">В следующем примере кода показано, как получить идентификатор указателя, связанный с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-175">The following code example shows how to obtain the pointer id associated with this message.</span></span>


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    
// failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}


```



<span data-ttu-id="ed1c8-176">В следующем примере кода показано, как управлять различными типами указателей, связанными с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="ed1c8-176">The following code example shows how to handle different pointer types associated with this message.</span></span>


```c++
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a><span data-ttu-id="ed1c8-177">Требования</span><span class="sxs-lookup"><span data-stu-id="ed1c8-177">Requirements</span></span>



| <span data-ttu-id="ed1c8-178">Требование</span><span class="sxs-lookup"><span data-stu-id="ed1c8-178">Requirement</span></span> | <span data-ttu-id="ed1c8-179">Значение</span><span class="sxs-lookup"><span data-stu-id="ed1c8-179">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1c8-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed1c8-180">Minimum supported client</span></span><br/> | <span data-ttu-id="ed1c8-181">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ed1c8-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="ed1c8-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed1c8-182">Minimum supported server</span></span><br/> | <span data-ttu-id="ed1c8-183">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ed1c8-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed1c8-184">Header</span><span class="sxs-lookup"><span data-stu-id="ed1c8-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed1c8-185"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c8-185"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed1c8-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed1c8-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1c8-187">Сообщения</span><span class="sxs-lookup"><span data-stu-id="ed1c8-187">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="ed1c8-188">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ed1c8-189">**Флаги указателя**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-189">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="ed1c8-190">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-190">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="ed1c8-191">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-191">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="ed1c8-192">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-192">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="ed1c8-193">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-193">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="ed1c8-194">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-194">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="ed1c8-195">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-195">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="ed1c8-196">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-196">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="ed1c8-197">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-197">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="ed1c8-198">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-198">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="ed1c8-199">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="ed1c8-199">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>
