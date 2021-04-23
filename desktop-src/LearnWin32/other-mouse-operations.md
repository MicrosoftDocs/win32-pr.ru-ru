---
title: Различные операции мыши
description: В предыдущих разделах обсуждались щелчки мыши и перемещения мыши. Ниже приведены некоторые другие операции, которые можно выполнить с помощью мыши.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337385"
---
# <a name="miscellaneous-mouse-operations"></a><span data-ttu-id="c3956-104">Различные операции мыши</span><span class="sxs-lookup"><span data-stu-id="c3956-104">Miscellaneous Mouse Operations</span></span>

<span data-ttu-id="c3956-105">В предыдущих разделах обсуждались щелчки мыши и перемещения мыши.</span><span class="sxs-lookup"><span data-stu-id="c3956-105">The previous sections have discussed mouse clicks and mouse movement.</span></span> <span data-ttu-id="c3956-106">Ниже приведены некоторые другие операции, которые можно выполнить с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="c3956-106">Here are some other operations that can be performed with the mouse.</span></span>

## <a name="dragging-ui-elements"></a><span data-ttu-id="c3956-107">Перетаскивание элементов пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c3956-107">Dragging UI Elements</span></span>

<span data-ttu-id="c3956-108">Если пользовательский интерфейс поддерживает перетаскивание элементов пользовательского интерфейса, то существует еще одна функция, которую следует вызывать в обработчике сообщений с помощью мыши: [**драгдетект**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span><span class="sxs-lookup"><span data-stu-id="c3956-108">If your UI supports dragging of UI elements, there is one other function that you should call in your mouse-down message handler: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span></span> <span data-ttu-id="c3956-109">Функция **драгдетект** возвращает **значение true** , если пользователь инициирует жест мыши, который должен интерпретироваться как перетаскивание.</span><span class="sxs-lookup"><span data-stu-id="c3956-109">The **DragDetect** function returns **TRUE** if the user initiates a mouse gesture that should be interpreted as dragging.</span></span> <span data-ttu-id="c3956-110">В следующем коде показано, как использовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="c3956-110">The following code shows how to use this function.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



<span data-ttu-id="c3956-111">Вот идея: когда программа поддерживает перетаскивание, каждое нажатие кнопки мыши не должно интерпретироваться как перетаскивание.</span><span class="sxs-lookup"><span data-stu-id="c3956-111">Here's the idea: When a program supports drag and drop, you don't want every mouse click to be interpreted as a drag.</span></span> <span data-ttu-id="c3956-112">В противном случае пользователь может случайно перетащить объект, если он просто щелкнул его (например, чтобы выбрать его).</span><span class="sxs-lookup"><span data-stu-id="c3956-112">Otherwise, the user might accidentally drag something when he or she simply meant to click on it (for example, to select it).</span></span> <span data-ttu-id="c3956-113">Но если мышь особенно важна, при нажатии на нее может быть трудно держать мышь.</span><span class="sxs-lookup"><span data-stu-id="c3956-113">But if a mouse is particularly sensitive, it can be hard to keep the mouse perfectly still while clicking.</span></span> <span data-ttu-id="c3956-114">Таким образом, Windows определяет пороговое значение перетаскивания в несколько пикселей.</span><span class="sxs-lookup"><span data-stu-id="c3956-114">Therefore, Windows defines a drag threshold of a few pixels.</span></span> <span data-ttu-id="c3956-115">Когда пользователь нажимает кнопку мыши, он не считается перетаскиванием, если только указатель мыши не пересекает это пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="c3956-115">When the user presses the mouse button, it is not considered a drag unless the mouse crosses this threshold.</span></span> <span data-ttu-id="c3956-116">Функция [**драгдетект**](/windows/desktop/api/winuser/nf-winuser-dragdetect) проверяет, достигнуто ли это пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="c3956-116">The [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function tests whether this threshold is reached.</span></span> <span data-ttu-id="c3956-117">Если функция возвращает **значение true**, щелчок мыши можно интерпретировать как перетаскивание.</span><span class="sxs-lookup"><span data-stu-id="c3956-117">If the function returns **TRUE**, you can interpret the mouse click as a drag.</span></span> <span data-ttu-id="c3956-118">В противном случае — нет.</span><span class="sxs-lookup"><span data-stu-id="c3956-118">Otherwise, do not.</span></span>

> [!Note]  
> <span data-ttu-id="c3956-119">Если [**драгдетект**](/windows/desktop/api/winuser/nf-winuser-dragdetect) возвращает **значение false**, Windows подавляет сообщение [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) , когда пользователь отпускает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="c3956-119">If [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) returns **FALSE**, Windows suppresses the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message when the user releases the mouse button.</span></span> <span data-ttu-id="c3956-120">Поэтому не вызывайте **драгдетект** , если программа в данный момент находится в режиме, поддерживающем перетаскивание.</span><span class="sxs-lookup"><span data-stu-id="c3956-120">Therefore, do not call **DragDetect** unless your program is currently in a mode that supports dragging.</span></span> <span data-ttu-id="c3956-121">(Например, если уже выбран перетаскиваемый элемент пользовательского интерфейса.) В конце этого модуля мы рассмотрим более длинный пример кода, использующий функцию **драгдетект** .</span><span class="sxs-lookup"><span data-stu-id="c3956-121">(For example, if a draggable UI element is already selected.) At the end of this module, we will see a longer code example that uses the **DragDetect** function.</span></span>

 

## <a name="confining-the-cursor"></a><span data-ttu-id="c3956-122">Ограничивать курсор</span><span class="sxs-lookup"><span data-stu-id="c3956-122">Confining the Cursor</span></span>

<span data-ttu-id="c3956-123">Иногда может потребоваться ограничить курсор клиентской областью или частью клиентской области.</span><span class="sxs-lookup"><span data-stu-id="c3956-123">Sometimes you might want to restrict the cursor to the client area or a portion of the client area.</span></span> <span data-ttu-id="c3956-124">Функция [**клипкурсор**](/windows/desktop/api/winuser/nf-winuser-clipcursor) ограничивают перемещение курсора на указанный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="c3956-124">The [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) function restricts the movement of the cursor to a specified rectangle.</span></span> <span data-ttu-id="c3956-125">Этот прямоугольник задается в экранных координатах, а не в координатах клиента, поэтому точка (0, 0) обозначает верхний левый угол экрана.</span><span class="sxs-lookup"><span data-stu-id="c3956-125">This rectangle is given in screen coordinates, rather than client coordinates, so the point (0, 0) means the upper left corner of the screen.</span></span> <span data-ttu-id="c3956-126">Чтобы перевести клиентские координаты в экранные координаты, вызовите функцию [**клиенттоскрин**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span><span class="sxs-lookup"><span data-stu-id="c3956-126">To translate client coordinates into screen coordinates, call the function [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span></span>

<span data-ttu-id="c3956-127">В следующем коде курсор ограничивается клиентской областью окна.</span><span class="sxs-lookup"><span data-stu-id="c3956-127">The following code confines the cursor to the client area of the window.</span></span>


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



<span data-ttu-id="c3956-128">[**Клипкурсор**](/windows/desktop/api/winuser/nf-winuser-clipcursor) принимает структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , но [**клиенттоскрин**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) принимает структуру [**Point**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c3956-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) takes a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure, but [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) takes a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="c3956-129">Прямоугольник определяется его верхней левой и нижней правой точками.</span><span class="sxs-lookup"><span data-stu-id="c3956-129">A rectangle is defined by its top-left and bottom-right points.</span></span> <span data-ttu-id="c3956-130">Можно ограничить курсор на любую прямоугольную область, включая области за пределами окна, но ограничивать курсор в клиентскую область — типичный способ использования функции.</span><span class="sxs-lookup"><span data-stu-id="c3956-130">You can confine the cursor to any rectangular area, including areas outside the window, but confining the cursor to the client area is a typical way to use the function.</span></span> <span data-ttu-id="c3956-131">Ограничивать курсор в регион, который полностью выходит за пределы окна, будет ненеобычным, и пользователи, вероятно, воспримет его как ошибку.</span><span class="sxs-lookup"><span data-stu-id="c3956-131">Confining the cursor to a region entirely outside your window would be unusual, and users would probably perceive it as a bug.</span></span>

<span data-ttu-id="c3956-132">Чтобы удалить ограничение, вызовите [**клипкурсор**](/windows/desktop/api/winuser/nf-winuser-clipcursor) со значением **null**.</span><span class="sxs-lookup"><span data-stu-id="c3956-132">To remove the restriction, call [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) with the value **NULL**.</span></span>


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a><span data-ttu-id="c3956-133">События отслеживания мыши: наведение и выход</span><span class="sxs-lookup"><span data-stu-id="c3956-133">Mouse Tracking Events: Hover and Leave</span></span>

<span data-ttu-id="c3956-134">Два других сообщения мыши по умолчанию отключены, но могут быть полезны для некоторых приложений:</span><span class="sxs-lookup"><span data-stu-id="c3956-134">Two other mouse messages are disabled by default, but may be useful for some applications:</span></span>

-   <span data-ttu-id="c3956-135">[**WM \_ МАУСЕХОВЕР**](/windows/desktop/inputdev/wm-mousehover): курсор наводится на клиентскую область в течение фиксированного периода времени.</span><span class="sxs-lookup"><span data-stu-id="c3956-135">[**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): The cursor has hovered over the client area for a fixed period of time.</span></span>
-   <span data-ttu-id="c3956-136">[**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): курсор остался в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="c3956-136">[**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): The cursor has left the client area.</span></span>

<span data-ttu-id="c3956-137">Чтобы включить эти сообщения, вызовите функцию [**TrackMouseEven**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) .</span><span class="sxs-lookup"><span data-stu-id="c3956-137">To enable these messages, call the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function.</span></span>


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



<span data-ttu-id="c3956-138">Структура [**TrackMouseEven**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) содержит параметры функции.</span><span class="sxs-lookup"><span data-stu-id="c3956-138">The [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) structure contains the parameters for the function.</span></span> <span data-ttu-id="c3956-139">Элемент **dwFlags** структуры содержит битовые флаги, указывающие, какие сообщения отслеживания вас интересуют.</span><span class="sxs-lookup"><span data-stu-id="c3956-139">The **dwFlags** member of the structure contains bit flags that specify which tracking messages you are interested in.</span></span> <span data-ttu-id="c3956-140">Вы можете получить и [**WM \_ маусеховер**](/windows/desktop/inputdev/wm-mousehover) , и [**WM \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), как показано здесь, или только один из двух.</span><span class="sxs-lookup"><span data-stu-id="c3956-140">You can choose to get both [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) and [**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), as shown here, or just one of the two.</span></span> <span data-ttu-id="c3956-141">Член **двховертиме** указывает, как долго мышь должна навести указатель мыши, прежде чем система создаст сообщение наведения.</span><span class="sxs-lookup"><span data-stu-id="c3956-141">The **dwHoverTime** member specifies how long the mouse needs to hover before the system generates a hover message.</span></span> <span data-ttu-id="c3956-142">Это значение указывается в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="c3956-142">This value is given in milliseconds.</span></span> <span data-ttu-id="c3956-143">Константа **\_ по умолчанию при наведении** означает использование системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3956-143">The constant **HOVER\_DEFAULT** means to use the system default.</span></span>

<span data-ttu-id="c3956-144">После получения одного из запрошенных сообщений функция [**TrackMouseEven**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="c3956-144">After you get one of the messages that you requested, the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function resets.</span></span> <span data-ttu-id="c3956-145">Чтобы получить другое сообщение отслеживания, необходимо вызвать его снова.</span><span class="sxs-lookup"><span data-stu-id="c3956-145">You must call it again to get another tracking message.</span></span> <span data-ttu-id="c3956-146">Однако следует дождаться следующего сообщения, перемещая мышь, перед вызовом **TrackMouseEven** .</span><span class="sxs-lookup"><span data-stu-id="c3956-146">However, you should wait until the next mouse-move message before calling **TrackMouseEvent** again.</span></span> <span data-ttu-id="c3956-147">В противном случае окно может быть переполнено сообщениями отслеживания.</span><span class="sxs-lookup"><span data-stu-id="c3956-147">Otherwise, your window might be flooded with tracking messages.</span></span> <span data-ttu-id="c3956-148">Например, при наведении указателя мыши система продолжит создавать поток сообщений [**WM \_ маусеховер**](/windows/desktop/inputdev/wm-mousehover) , когда мышь является стационарной.</span><span class="sxs-lookup"><span data-stu-id="c3956-148">For example, if the mouse is hovering, the system would continue to generate a stream of [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) messages while the mouse is stationary.</span></span> <span data-ttu-id="c3956-149">На самом деле не требуется другое сообщение **WM \_ маусеховер** , пока мышь не перемещается в другую точку и наводится на другой элемент.</span><span class="sxs-lookup"><span data-stu-id="c3956-149">You don't actually want another **WM\_MOUSEHOVER** message until the mouse moves to another spot and hovers again.</span></span>

<span data-ttu-id="c3956-150">Ниже приведен небольшой вспомогательный класс, который можно использовать для управления событиями отслеживания мыши.</span><span class="sxs-lookup"><span data-stu-id="c3956-150">Here is a small helper class that you can use to manage mouse-tracking events.</span></span>


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



<span data-ttu-id="c3956-151">В следующем примере показано, как использовать этот класс в процедуре окна.</span><span class="sxs-lookup"><span data-stu-id="c3956-151">The next example shows how to use this class in your window procedure.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="c3956-152">События отслеживания мыши требуют дополнительной обработки системой, поэтому оставьте их отключенными, если они не нужны.</span><span class="sxs-lookup"><span data-stu-id="c3956-152">Mouse tracking events require additional processing by the system, so leave them disabled if you do not need them.</span></span>

<span data-ttu-id="c3956-153">Для полноты рассмотрим функцию, которая запрашивает у системы время ожидания при наведении по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3956-153">For completeness, here is a function that queries the system for the default hover timeout.</span></span>


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a><span data-ttu-id="c3956-154">Колесико мыши</span><span class="sxs-lookup"><span data-stu-id="c3956-154">Mouse Wheel</span></span>

<span data-ttu-id="c3956-155">Следующая функция проверяет наличие колесика мыши.</span><span class="sxs-lookup"><span data-stu-id="c3956-155">The following function checks if a mouse wheel is present.</span></span>


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



<span data-ttu-id="c3956-156">Если пользователь поворачивает колесико мыши, окно с фокусом получает сообщение [**WM \_ маусевхил**](/windows/desktop/inputdev/wm-mousewheel) .</span><span class="sxs-lookup"><span data-stu-id="c3956-156">If the user rotates the mouse wheel, the window with focus receives a [**WM\_MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) message.</span></span> <span data-ttu-id="c3956-157">Параметр *wParam* этого сообщения содержит целочисленное значение, называемое *разностным* значением, которое измеряет расстояние поворота колесика.</span><span class="sxs-lookup"><span data-stu-id="c3956-157">The *wParam* parameter of this message contains an integer value called the *delta* that measures how far the wheel was rotated.</span></span> <span data-ttu-id="c3956-158">Дельта использует произвольные единицы, где 120 единиц определяется как поворот, необходимый для выполнения одного действия.</span><span class="sxs-lookup"><span data-stu-id="c3956-158">The delta uses arbitrary units, where 120 units is defined as the rotation needed to perform one "action."</span></span> <span data-ttu-id="c3956-159">Конечно, определение действия зависит от программы.</span><span class="sxs-lookup"><span data-stu-id="c3956-159">Of course, the definition of an action depends on your program.</span></span> <span data-ttu-id="c3956-160">Например, если колесико мыши используется для прокрутки текста, каждая 120 единиц вращения будет прокручиваться на одну строку текста.</span><span class="sxs-lookup"><span data-stu-id="c3956-160">For example, if the mouse wheel is used to scroll text, each 120 units of rotation would scroll one line of text.</span></span>

<span data-ttu-id="c3956-161">Знак Дельта указывает направление поворота:</span><span class="sxs-lookup"><span data-stu-id="c3956-161">The sign of the delta indicates the direction of rotation:</span></span>

-   <span data-ttu-id="c3956-162">Положительный: поворот вперед от пользователя.</span><span class="sxs-lookup"><span data-stu-id="c3956-162">Positive: Rotate forward, away from the user.</span></span>
-   <span data-ttu-id="c3956-163">Отрицательно: поворот назад, направленный к пользователю.</span><span class="sxs-lookup"><span data-stu-id="c3956-163">Negative: Rotate backward, toward the user.</span></span>

<span data-ttu-id="c3956-164">Значение дельты помещается в *wParam* вместе с некоторыми дополнительными флагами.</span><span class="sxs-lookup"><span data-stu-id="c3956-164">The value of the delta is placed in *wParam* along with some additional flags.</span></span> <span data-ttu-id="c3956-165">Чтобы получить значение разностного значения, используйте макрос [**Get \_ Wheel \_ Дельта \_ wParam**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) .</span><span class="sxs-lookup"><span data-stu-id="c3956-165">Use the [**GET\_WHEEL\_DELTA\_WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) macro to get the value of the delta.</span></span>


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="c3956-166">Если колесико мыши имеет высокое разрешение, абсолютное значение разницы может быть меньше 120.</span><span class="sxs-lookup"><span data-stu-id="c3956-166">If the mouse wheel has a high resolution, the absolute value of the delta might be less than 120.</span></span> <span data-ttu-id="c3956-167">В этом случае, если имеет смысл выполнить действие с меньшим шагом, это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="c3956-167">In that case, if it makes sense for the action to occur in smaller increments, you can do so.</span></span> <span data-ttu-id="c3956-168">Например, текст может прокручиваться с шагом меньше одной строки.</span><span class="sxs-lookup"><span data-stu-id="c3956-168">For example, text could scroll by increments of less than one line.</span></span> <span data-ttu-id="c3956-169">В противном случае суммируйте общую разницу до того, как колесо поворачивается достаточно для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="c3956-169">Otherwise, accumulate the total delta until the wheel rotates enough to perform the action.</span></span> <span data-ttu-id="c3956-170">Сохраните неиспользуемую разницу в переменной и, когда 120 единиц накапливает (положительное или отрицательное), выполните действие.</span><span class="sxs-lookup"><span data-stu-id="c3956-170">Store the unused delta in a variable, and when 120 units accumulate (either positive or negative), perform the action.</span></span>

## <a name="next"></a><span data-ttu-id="c3956-171">Следующая</span><span class="sxs-lookup"><span data-stu-id="c3956-171">Next</span></span>

[<span data-ttu-id="c3956-172">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="c3956-172">Keyboard Input</span></span>](keyboard-input.md)

 

 