---
Description: Сообщение WM \_ Paint отправляется, когда система или другое приложение выполняет запрос на закрасить часть окна приложения.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Сообщение WM_PAINT (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987506"
---
# <a name="wm_paint-message"></a><span data-ttu-id="aa5d0-103">\_Сообщение WM Paint</span><span class="sxs-lookup"><span data-stu-id="aa5d0-103">WM\_PAINT message</span></span>

<span data-ttu-id="aa5d0-104">Сообщение **WM \_ Paint** отправляется, когда система или другое приложение выполняет запрос на закрасить часть окна приложения.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-104">The **WM\_PAINT** message is sent when the system or another application makes a request to paint a portion of an application's window.</span></span> <span data-ttu-id="aa5d0-105">Сообщение отправляется, когда вызывается функция [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) или [**Редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) или функция [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , когда приложение получает сообщение **WM \_ Paint** с помощью функции WITH [**Message**](/windows/win32/api/winuser/nf-winuser-getmessage) или [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="aa5d0-105">The message is sent when the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) or [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) function is called, or by the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function when the application obtains a **WM\_PAINT** message by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>

<span data-ttu-id="aa5d0-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aa5d0-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="aa5d0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa5d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa5d0-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa5d0-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa5d0-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="aa5d0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa5d0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa5d0-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa5d0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa5d0-112">Return value</span></span>

<span data-ttu-id="aa5d0-113">Приложение возвращает нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-113">An application returns zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="aa5d0-114">Например, .</span><span class="sxs-lookup"><span data-stu-id="aa5d0-114">Example</span></span>

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

<span data-ttu-id="aa5d0-115">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa5d0-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa5d0-116">Remarks</span></span>

<span data-ttu-id="aa5d0-117">Сообщение **WM \_ Paint** создается системой и не должно отправляться приложением.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-117">The **WM\_PAINT** message is generated by the system and should not be sent by an application.</span></span> <span data-ttu-id="aa5d0-118">Чтобы заставить окно нарисоваться в конкретном контексте устройства, используйте сообщение [**WM \_ Print**](wm-print.md) или [**WM \_ принтклиент**](wm-printclient.md) .</span><span class="sxs-lookup"><span data-stu-id="aa5d0-118">To force a window to draw into a specific device context, use the [**WM\_PRINT**](wm-print.md) or [**WM\_PRINTCLIENT**](wm-printclient.md) message.</span></span> <span data-ttu-id="aa5d0-119">Обратите внимание, что для этого требуется, чтобы целевое окно поддерживало сообщение **WM \_ принтклиент** .</span><span class="sxs-lookup"><span data-stu-id="aa5d0-119">Note that this requires the target window to support the **WM\_PRINTCLIENT** message.</span></span> <span data-ttu-id="aa5d0-120">Большинство стандартных элементов управления поддерживают сообщение **WM \_ принтклиент** .</span><span class="sxs-lookup"><span data-stu-id="aa5d0-120">Most common controls support the **WM\_PRINTCLIENT** message.</span></span>

<span data-ttu-id="aa5d0-121">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  проверяет регион обновления.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function validates the update region.</span></span> <span data-ttu-id="aa5d0-122">Функция также может отправить сообщение [**WM \_ нкпаинт**](wm-ncpaint.md) в оконную процедуру, если рамка окна должна быть окрашена, и отправить сообщение [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) , если фон окна необходимо стереть.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-122">The function may also send the [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

<span data-ttu-id="aa5d0-123">Система отправляет это сообщение при отсутствии других сообщений в очереди сообщений приложения.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-123">The system sends this message when there are no other messages in the application's message queue.</span></span> <span data-ttu-id="aa5d0-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) определяет, куда отправить сообщение; [**Сообщение о выправке определяет,**](/windows/win32/api/winuser/nf-winuser-getmessage) какое сообщение следует отправлять.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determines where to send the message; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determines which message to dispatch.</span></span> <span data-ttu-id="aa5d0-125">Функция **onmessage** возвращает сообщение **WM \_ Paint** , если в очереди сообщений приложения нет других сообщений, а **DispatchMessage** отправляет сообщение в соответствующую процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-125">**GetMessage** returns the **WM\_PAINT** message when there are no other messages in the application's message queue, and **DispatchMessage** sends the message to the appropriate window procedure.</span></span>

<span data-ttu-id="aa5d0-126">Окно может получить внутренние сообщения рисования в результате вызова [**редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) с \_ установленным флагом РДВ интерналпаинт.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-126">A window may receive internal paint messages as a result of calling [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span> <span data-ttu-id="aa5d0-127">В этом случае в окне может отсутствовать регион обновления.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-127">In this case, the window may not have an update region.</span></span> <span data-ttu-id="aa5d0-128">Приложение может вызвать функцию [**жетупдатерект**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) , чтобы определить, имеет ли окно регион обновления.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-128">An application may call the [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) function to determine whether the window has an update region.</span></span> <span data-ttu-id="aa5d0-129">Если **жетупдатерект** возвращает ноль, приложению не нужно вызывать функции [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) и [**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="aa5d0-129">If **GetUpdateRect** returns zero, the application need not call the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions.</span></span>

<span data-ttu-id="aa5d0-130">Приложение должно проверять все необходимое внутреннее оформление, просматривая внутренние структуры данных для каждого сообщения **WM \_ Paint** , так как сообщение **WM \_ Paint** могло быть вызвано ненулевым регионом обновления и вызовом [**редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) с \_ установленным флагом РДВ интерналпаинт.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-130">An application must check for any necessary internal painting by looking at its internal data structures for each **WM\_PAINT** message, because a **WM\_PAINT** message may have been caused by both a non-NULL update region and a call to [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="aa5d0-131">Система отправляет внутреннее сообщение **WM \_ Paint** только один раз.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-131">The system sends an internal **WM\_PAINT** message only once.</span></span> <span data-ttu-id="aa5d0-132">После того как внутреннее сообщение **WM \_ Paint** [**возвращается из метода**](/windows/win32/api/winuser/nf-winuser-getmessage) [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) или отправляется в окно с помощью [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), система не отправляет или не передает последующие сообщения **WM \_ Paint** до тех пор, пока окно не станет недействительным или пока не будет вызван [**редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) с \_ установленным флагом РДВ интерналпаинт.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-132">After an internal **WM\_PAINT** message is returned from [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) or is sent to a window by [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), the system does not post or send further **WM\_PAINT** messages until the window is invalidated or until [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) is called again with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="aa5d0-133">Для некоторых стандартных элементов управления обработка сообщений **WM \_ Paint** по умолчанию проверяет параметр *wParam* .</span><span class="sxs-lookup"><span data-stu-id="aa5d0-133">For some common controls, the default **WM\_PAINT** message processing checks the *wParam* parameter.</span></span> <span data-ttu-id="aa5d0-134">Если параметр *wParam* не равен null, то элемент управления предполагает, что значение является HDC и рисует его с помощью контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="aa5d0-134">If *wParam* is non-NULL, the control assumes that the value is an HDC and paints using that device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5d0-135">Требования</span><span class="sxs-lookup"><span data-stu-id="aa5d0-135">Requirements</span></span>



| <span data-ttu-id="aa5d0-136">Требование</span><span class="sxs-lookup"><span data-stu-id="aa5d0-136">Requirement</span></span> | <span data-ttu-id="aa5d0-137">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5d0-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5d0-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa5d0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5d0-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa5d0-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="aa5d0-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa5d0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5d0-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa5d0-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aa5d0-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aa5d0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa5d0-143"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d0-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa5d0-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa5d0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5d0-145">Общие сведения о рисовании и рисовании</span><span class="sxs-lookup"><span data-stu-id="aa5d0-145">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="aa5d0-146">Рисование и рисование сообщений</span><span class="sxs-lookup"><span data-stu-id="aa5d0-146">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="aa5d0-147">**бегинпаинт**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-147">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="aa5d0-148">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="aa5d0-149">**DispatchMessage**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-149">**DispatchMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[<span data-ttu-id="aa5d0-150">**ендпаинт**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-150">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="aa5d0-151">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-151">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="aa5d0-152">**жетупдатерект**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-152">**GetUpdateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[<span data-ttu-id="aa5d0-153">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-153">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="aa5d0-154">**редраввиндов**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-154">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[<span data-ttu-id="aa5d0-155">**упдатевиндов**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-155">**UpdateWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[<span data-ttu-id="aa5d0-156">**WM \_ ерасебкгнд**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-156">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="aa5d0-157">**WM \_ нкпаинт**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-157">**WM\_NCPAINT**</span></span>](wm-ncpaint.md)
</dt> <dt>

[<span data-ttu-id="aa5d0-158">**\_Печать WM**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-158">**WM\_PRINT**</span></span>](wm-print.md)
</dt> <dt>

[<span data-ttu-id="aa5d0-159">**WM \_ принтклиент**</span><span class="sxs-lookup"><span data-stu-id="aa5d0-159">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
