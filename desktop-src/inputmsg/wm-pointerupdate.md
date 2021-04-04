---
title: Сообщение WM_POINTERUPDATE
description: Опубликовано для предоставления обновления указателя, который подключается к клиентской области окна или при наведении указателя мыши на незахваченный указатель на клиентскую область окна.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac222
keywords:
- WM_POINTERUPDATE сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 215874f4dc1b3438ae3d69b22758ced09a050f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137654"
---
# <a name="wm_pointerupdate-message"></a><span data-ttu-id="81177-104">Сообщение WM_POINTERUPDATE</span><span class="sxs-lookup"><span data-stu-id="81177-104">WM_POINTERUPDATE message</span></span>

<span data-ttu-id="81177-105">Опубликовано для предоставления обновления указателя, который подключается к клиентской области окна или при наведении указателя мыши на незахваченный указатель на клиентскую область окна.</span><span class="sxs-lookup"><span data-stu-id="81177-105">Posted to provide an update on a pointer that made contact over the client area of a window or on a hovering uncaptured pointer over the client area of a window.</span></span> <span data-ttu-id="81177-106">При наведении указателя мыши сообщение предназначено для любого окна, над которым происходит указатель.</span><span class="sxs-lookup"><span data-stu-id="81177-106">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="81177-107">Пока указатель находится в контакте с поверхностью, указатель неявно записывается в окно, над которым указатель сделал контакт, и это окно по---получит входные данные для указателя до тех пор, пока не будет прервано соединение.</span><span class="sxs-lookup"><span data-stu-id="81177-107">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span>

> <span data-ttu-id="81177-108">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="81177-108">\[!Important\]</span></span>  
> <span data-ttu-id="81177-109">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="81177-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="81177-110">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="81177-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="81177-111">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="81177-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="81177-112">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81177-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERUPDATE              0x0245
```



## <a name="parameters"></a><span data-ttu-id="81177-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="81177-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81177-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81177-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81177-115">Содержит сведения об указателе.</span><span class="sxs-lookup"><span data-stu-id="81177-115">Contains information about the pointer.</span></span> <span data-ttu-id="81177-116">Используйте следующие макросы для получения сведений из параметра wParam.</span><span class="sxs-lookup"><span data-stu-id="81177-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="81177-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): идентификатор указателя.</span><span class="sxs-lookup"><span data-stu-id="81177-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="81177-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, представляет ли данное сообщение первый вход, созданный новым указателем.</span><span class="sxs-lookup"><span data-stu-id="81177-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="81177-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, было ли это сообщение создано указателем в течение его времени существования.</span><span class="sxs-lookup"><span data-stu-id="81177-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="81177-120">Этот флаг не установлен для сообщений, указывающих на то, что указатель имеет диапазон обнаружения слева</span><span class="sxs-lookup"><span data-stu-id="81177-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="81177-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, было ли это сообщение создано указателем, который находится в связи с областью окна.</span><span class="sxs-lookup"><span data-stu-id="81177-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="81177-122">Этот флаг не задан для сообщений, указывающих на наведение указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="81177-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="81177-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): указывает, что этот указатель был обозначен как первичный.</span><span class="sxs-lookup"><span data-stu-id="81177-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="81177-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, имеется ли первичное действие.</span><span class="sxs-lookup"><span data-stu-id="81177-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="81177-125">Это аналогично левой кнопке мыши.</span><span class="sxs-lookup"><span data-stu-id="81177-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="81177-126">В связи с поверхностью дигитайзера этот набор будет иметь сенсорный указатель.</span><span class="sxs-lookup"><span data-stu-id="81177-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="81177-127">Этот набор будет иметь указатель пера, если он находится в контакте с поверхностью дигитайзера без нажатия кнопок.</span><span class="sxs-lookup"><span data-stu-id="81177-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="81177-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, есть ли вторичное действие.</span><span class="sxs-lookup"><span data-stu-id="81177-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="81177-129">Это аналогично нажатию кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="81177-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="81177-130">Этот набор будет иметь указатель пера, если он в связи с поверхностью дигитайзера нажата кнопка пера.</span><span class="sxs-lookup"><span data-stu-id="81177-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="81177-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий на наличие одного или нескольких третичных действий на основе типа указателя; приложения, которые хотят реагировать на третичные действия, должны получить информацию, относящуюся к типу указателя, чтобы определить, какие из них нажаты.</span><span class="sxs-lookup"><span data-stu-id="81177-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="81177-132">Например, приложение может определить состояния кнопок пера, вызвав [**жетпоинтерпенинфо**](/previous-versions/windows/desktop/api) и изучив флаги, указывающие состояния кнопок.</span><span class="sxs-lookup"><span data-stu-id="81177-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="81177-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, принял ли указанный указатель четвертое действие.</span><span class="sxs-lookup"><span data-stu-id="81177-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="81177-134">Приложения, которые хотят реагировать на четвертые действия, должны получить сведения, относящиеся к типу указателя, чтобы определить, нажата ли первая расширенная кнопка мыши (XButton1).</span><span class="sxs-lookup"><span data-stu-id="81177-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="81177-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**флаг**](pointer-flags-contants.md) , указывающий, принял ли указанный указатель пятое действие.</span><span class="sxs-lookup"><span data-stu-id="81177-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="81177-136">Приложения, которые хотят отвечать на пятое действие, должны получить информацию, относящуюся к типу указателя, чтобы определить, нажата ли вторая кнопка расширенной мыши (XButton2).</span><span class="sxs-lookup"><span data-stu-id="81177-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="81177-137">Дополнительные сведения см. в разделе [**Флаги указателя**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="81177-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="81177-138">Указатель мыши не имеет установленного флага кнопки.</span><span class="sxs-lookup"><span data-stu-id="81177-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="81177-139">Это аналогично перемещению мыши без кнопок мыши.</span><span class="sxs-lookup"><span data-stu-id="81177-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="81177-140">Приложение может определить состояния кнопок для наведения указателя мыши, например путем вызова [**жетпоинтерпенинфо**](/previous-versions/windows/desktop/api) и проверки флагов, указывающих на состояния кнопок.</span><span class="sxs-lookup"><span data-stu-id="81177-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="81177-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81177-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81177-142">Содержит расположение точки указателя.</span><span class="sxs-lookup"><span data-stu-id="81177-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="81177-143">Так как указатель может установить связь с устройством в нетривиальной области, это расположение может быть упрощено более сложной областью указателя.</span><span class="sxs-lookup"><span data-stu-id="81177-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="81177-144">Когда это возможно, приложение должно использовать полные сведения об области указателя, а не расположение точки.</span><span class="sxs-lookup"><span data-stu-id="81177-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="81177-145">Используйте следующие макросы, чтобы получить физические экранные координаты точки.</span><span class="sxs-lookup"><span data-stu-id="81177-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="81177-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): координата X (горизонтальная точка).</span><span class="sxs-lookup"><span data-stu-id="81177-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="81177-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): координата Y (вертикальная точка).</span><span class="sxs-lookup"><span data-stu-id="81177-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81177-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81177-148">Return value</span></span>

<span data-ttu-id="81177-149">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="81177-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="81177-150">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="81177-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="81177-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81177-151">Remarks</span></span>

<span data-ttu-id="81177-152">Каждый указатель имеет уникальный идентификатор указателя в течение своего времени существования.</span><span class="sxs-lookup"><span data-stu-id="81177-152">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="81177-153">Время существования указателя начинается при первом обнаружении.</span><span class="sxs-lookup"><span data-stu-id="81177-153">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="81177-154">При обнаружении указателя мыши создается [**WM_POINTERENTER**](wm-pointerenter.md) сообщение.</span><span class="sxs-lookup"><span data-stu-id="81177-154">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="81177-155">При обнаружении указателя, не являющегося указателем, создается [**WM_POINTERDOWN**](wm-pointerdown.md) сообщение, за которым следует сообщение **WM_POINTERENTER** .</span><span class="sxs-lookup"><span data-stu-id="81177-155">A [**WM_POINTERDOWN**](wm-pointerdown.md) message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="81177-156">Во время его существования указатель может формировать ряд **WM_POINTERUPDATE** сообщений при наведении указателя мыши или в контакте.</span><span class="sxs-lookup"><span data-stu-id="81177-156">During its lifetime, a pointer may generate a series of **WM_POINTERUPDATE** messages while it is hovering or in contact.</span></span>

<span data-ttu-id="81177-157">Время существования указателя заканчивается, когда он больше не обнаруживается.</span><span class="sxs-lookup"><span data-stu-id="81177-157">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="81177-158">При этом создается [**WM_POINTERLEAVE**](wm-pointerleave.md) сообщение.</span><span class="sxs-lookup"><span data-stu-id="81177-158">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="81177-159">При прерывании указателя задается [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="81177-159">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="81177-160">Сообщение [**WM_POINTERLEAVE**](wm-pointerleave.md) также может быть создано, когда незахваченный указатель перемещается за пределы окна.</span><span class="sxs-lookup"><span data-stu-id="81177-160">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="81177-161">Для получения горизонтального и вертикального расположения указателя используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="81177-161">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="81177-162">Макрос [**макепоинтс**](/windows/win32/api/wingdi/nf-wingdi-makepoints) также можно использовать для преобразования параметра lParam в структуру [**points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="81177-162">The [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro can also be used to convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="81177-163">Функцию [**жеткэйстате**](/windows/win32/api/winuser/nf-winuser-getkeystate) можно использовать для определения состояний клавиши модификатора клавиатуры, связанных с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="81177-163">The [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function can be used to determine the keyboard modifier key states associated with this message.</span></span> <span data-ttu-id="81177-164">Например, чтобы обнаружить, что нажата клавиша ALT, проверьте, не **жеткэйстате** ли значение 0 (VK_MENU) &lt; .</span><span class="sxs-lookup"><span data-stu-id="81177-164">For example, to detect that the ALT key was pressed, check whether **GetKeyState** (VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="81177-165">Если приложение не обрабатывает это сообщение, [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca) может создать одно или несколько [**WM_GESTURE**](../wintouch/wm-gesture.md) сообщений, если последовательность входных данных из этого и, возможно, других указателей распознается как жест.</span><span class="sxs-lookup"><span data-stu-id="81177-165">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="81177-166">Если жест не распознан, **дефвиндовпрок** может создавать ввод с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="81177-166">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="81177-167">Если приложение выборочно потребляет некоторые входные данные указателя и передает оставшуюся часть в [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca), то результирующее поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="81177-167">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="81177-168">Используйте функцию [**жетпоинтеринфо**](/previous-versions/windows/desktop/api) для получения дополнительных сведений, относящихся к этому сообщению.</span><span class="sxs-lookup"><span data-stu-id="81177-168">Use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function to retrieve further information related to this message.</span></span>

<span data-ttu-id="81177-169">Если приложение не обрабатывает эти сообщения так быстро, как они создаются, некоторые перемещения могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="81177-169">If the application does not process these messages as fast as they are generated, some moves may be coalesced.</span></span> <span data-ttu-id="81177-170">Журнал входных данных, Объединенных в это сообщение, можно получить с помощью функции [**жетпоинтеринфохистори**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="81177-170">The history of inputs that were coalesced into this message can be retrieved using the [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) function.</span></span>

## <a name="examples"></a><span data-ttu-id="81177-171">Примеры</span><span class="sxs-lookup"><span data-stu-id="81177-171">Examples</span></span>

<span data-ttu-id="81177-172">В следующем примере кода показано, как использовать [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)и [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) для получения релевантной информации из параметров WParam и LPARAM сообщения **WM_POINTERUPDATE** .</span><span class="sxs-lookup"><span data-stu-id="81177-172">The following code example shows how to use [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), and [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) to retrieve relevant information from the wParam and lParam parameters of the **WM_POINTERUPDATE** message.</span></span>


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with right button down
}
```



<span data-ttu-id="81177-173">В следующем примере кода показано, как использовать [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) для получения идентификатора указателя из параметра wParam **WM_POINTERUPDATE** сообщения.</span><span class="sxs-lookup"><span data-stu-id="81177-173">The following code example shows how to use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to retrieve the pointer id from the wParam parameter of the **WM_POINTERUPDATE** message.</span></span>


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



<span data-ttu-id="81177-174">В следующем примере кода показано, как управлять различными типами указателей.</span><span class="sxs-lookup"><span data-stu-id="81177-174">The following code example shows how to handle different pointer types.</span></span>


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_INPUT_TYPE pointerType = PT_POINTER;

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
        fHandled = HandleGenericPointerInfo(&pointerInfo);
    }
    break;
}
```



## <a name="requirements"></a><span data-ttu-id="81177-175">Требования</span><span class="sxs-lookup"><span data-stu-id="81177-175">Requirements</span></span>



| <span data-ttu-id="81177-176">Требование</span><span class="sxs-lookup"><span data-stu-id="81177-176">Requirement</span></span> | <span data-ttu-id="81177-177">Значение</span><span class="sxs-lookup"><span data-stu-id="81177-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81177-178">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81177-178">Minimum supported client</span></span><br/> | <span data-ttu-id="81177-179">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="81177-179">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="81177-180">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81177-180">Minimum supported server</span></span><br/> | <span data-ttu-id="81177-181">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="81177-181">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81177-182">Header</span><span class="sxs-lookup"><span data-stu-id="81177-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="81177-183"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81177-183"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81177-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81177-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81177-185">Сообщения</span><span class="sxs-lookup"><span data-stu-id="81177-185">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="81177-186">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="81177-186">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81177-187">**Флаги указателя**</span><span class="sxs-lookup"><span data-stu-id="81177-187">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="81177-188">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-188">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="81177-189">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-189">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="81177-190">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-190">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="81177-191">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-191">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="81177-192">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-192">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="81177-193">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-193">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="81177-194">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-194">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="81177-195">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-195">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="81177-196">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-196">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="81177-197">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="81177-197">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

