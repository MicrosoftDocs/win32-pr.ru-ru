---
title: Реагирование на щелчки мыши
description: Реагирование на щелчки мыши
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133854"
---
# <a name="responding-to-mouse-clicks"></a><span data-ttu-id="c31ec-103">Реагирование на щелчки мыши</span><span class="sxs-lookup"><span data-stu-id="c31ec-103">Responding to Mouse Clicks</span></span>

<span data-ttu-id="c31ec-104">Если пользователь нажимает кнопку мыши, когда курсор находится над клиентской областью окна, окно получает одно из следующих сообщений.</span><span class="sxs-lookup"><span data-stu-id="c31ec-104">If the user clicks a mouse button while the cursor is over the client area of a window, the window receives one of the following messages.</span></span>



| <span data-ttu-id="c31ec-105">Сообщение</span><span class="sxs-lookup"><span data-stu-id="c31ec-105">Message</span></span>                                        | <span data-ttu-id="c31ec-106">Значение</span><span class="sxs-lookup"><span data-stu-id="c31ec-106">Meaning</span></span>                   |
|------------------------------------------------|---------------------------|
| [<span data-ttu-id="c31ec-107">**WM \_ лбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="c31ec-107">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown) | <span data-ttu-id="c31ec-108">Левая кнопка вниз</span><span class="sxs-lookup"><span data-stu-id="c31ec-108">Left button down</span></span>          |
| [<span data-ttu-id="c31ec-109">**WM \_ лбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="c31ec-109">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)     | <span data-ttu-id="c31ec-110">Кнопка "влево"</span><span class="sxs-lookup"><span data-stu-id="c31ec-110">Left button up</span></span>            |
| [<span data-ttu-id="c31ec-111">**WM \_ мбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="c31ec-111">**WM\_MBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-mbuttondown) | <span data-ttu-id="c31ec-112">Средняя кнопка вниз</span><span class="sxs-lookup"><span data-stu-id="c31ec-112">Middle button down</span></span>        |
| [<span data-ttu-id="c31ec-113">**WM \_ мбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="c31ec-113">**WM\_MBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-mbuttonup)     | <span data-ttu-id="c31ec-114">Средняя кнопка вверх</span><span class="sxs-lookup"><span data-stu-id="c31ec-114">Middle button up</span></span>          |
| [<span data-ttu-id="c31ec-115">**WM \_ рбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="c31ec-115">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown) | <span data-ttu-id="c31ec-116">Правая кнопка вниз</span><span class="sxs-lookup"><span data-stu-id="c31ec-116">Right button down</span></span>         |
| [<span data-ttu-id="c31ec-117">**WM \_ рбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="c31ec-117">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)     | <span data-ttu-id="c31ec-118">Кнопка "вправо"</span><span class="sxs-lookup"><span data-stu-id="c31ec-118">Right button up</span></span>           |
| [<span data-ttu-id="c31ec-119">**WM \_ ксбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="c31ec-119">**WM\_XBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-xbuttondown) | <span data-ttu-id="c31ec-120">XBUTTON1 или XBUTTON2 Down</span><span class="sxs-lookup"><span data-stu-id="c31ec-120">XBUTTON1 or XBUTTON2 down</span></span> |
| [<span data-ttu-id="c31ec-121">**WM \_ ксбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="c31ec-121">**WM\_XBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-xbuttonup)     | <span data-ttu-id="c31ec-122">XBUTTON1 или XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="c31ec-122">XBUTTON1 or XBUTTON2 up</span></span>   |



 

<span data-ttu-id="c31ec-123">Вспомним, что клиентская область — это часть окна, исключающая фрейм.</span><span class="sxs-lookup"><span data-stu-id="c31ec-123">Recall that the client area is the portion of the window that excludes the frame.</span></span> <span data-ttu-id="c31ec-124">Дополнительные сведения о клиентских областях см [. в разделе что такое окно?](what-is-a-window-.md)</span><span class="sxs-lookup"><span data-stu-id="c31ec-124">For more information about client areas, see [What Is a Window?](what-is-a-window-.md)</span></span>

### <a name="mouse-coordinates"></a><span data-ttu-id="c31ec-125">Координаты мыши</span><span class="sxs-lookup"><span data-stu-id="c31ec-125">Mouse Coordinates</span></span>

<span data-ttu-id="c31ec-126">Во всех этих сообщениях параметр *lParam* содержит координаты x и y указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="c31ec-126">In all of these messages, the *lParam* parameter contains the x- and y-coordinates of the mouse pointer.</span></span> <span data-ttu-id="c31ec-127">Младшие 16 бит *lParam* содержат координату x, а следующие 16 бит содержат координату y.</span><span class="sxs-lookup"><span data-stu-id="c31ec-127">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="c31ec-128">Используйте макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для распаковки координат из *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c31ec-128">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="c31ec-129">Эти макросы определены в файле заголовка Виндовскс. h.</span><span class="sxs-lookup"><span data-stu-id="c31ec-129">These macros are defined in the header file WindowsX.h.</span></span>

<span data-ttu-id="c31ec-130">В 64-разрядной версии Windows параметр *lParam* имеет значение 64-bit.</span><span class="sxs-lookup"><span data-stu-id="c31ec-130">On 64-bit Windows, *lParam* is 64-bit value.</span></span> <span data-ttu-id="c31ec-131">Верхние 32 бит *lParam* не используются.</span><span class="sxs-lookup"><span data-stu-id="c31ec-131">The upper 32 bits of *lParam* are not used.</span></span> <span data-ttu-id="c31ec-132">В документации MSDN упоминается "слово с низким приоритетом" и "слово" с высоким приоритетом *".*</span><span class="sxs-lookup"><span data-stu-id="c31ec-132">The MSDN documentation mentions the "low-order word" and "high-order word" of *lParam*.</span></span> <span data-ttu-id="c31ec-133">В 64-разрядном случае это означает младшее и высокое количество слов с более низкими 32 битами.</span><span class="sxs-lookup"><span data-stu-id="c31ec-133">In the 64-bit case, this means the low- and high-order words of the lower 32 bits.</span></span> <span data-ttu-id="c31ec-134">Эти макросы извлекают правильные значения, поэтому при их использовании вы будете уверены в безопасности.</span><span class="sxs-lookup"><span data-stu-id="c31ec-134">The macros extract the right values, so if you use them, you will be safe.</span></span>

<span data-ttu-id="c31ec-135">Координаты мыши задаются в пикселях, а не в аппаратно-независимых пикселях (DIP) и измеряются относительно клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="c31ec-135">Mouse coordinates are given in pixels, not device-independent pixels (DIPs), and are measured relative to the client area of the window.</span></span> <span data-ttu-id="c31ec-136">Координаты являются значениями со знаком.</span><span class="sxs-lookup"><span data-stu-id="c31ec-136">Coordinates are signed values.</span></span> <span data-ttu-id="c31ec-137">Позиции выше и слева от клиентской области имеют отрицательные координаты, что важно при отслеживании положения мыши за пределами окна.</span><span class="sxs-lookup"><span data-stu-id="c31ec-137">Positions above and to the left of the client area have negative coordinates, which is important if you track the mouse position outside the window.</span></span> <span data-ttu-id="c31ec-138">Мы увидим, как это сделать в более позднем разделе, [записывая перемещение мыши за пределы окна](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="c31ec-138">We will see how to do that in a later topic, [Capturing Mouse Movement Outside the Window](mouse-movement.md).</span></span>

### <a name="additional-flags"></a><span data-ttu-id="c31ec-139">Дополнительные флаги</span><span class="sxs-lookup"><span data-stu-id="c31ec-139">Additional Flags</span></span>

<span data-ttu-id="c31ec-140">Параметр *wParam* содержит побитовое **или** для флагов, указывающих состояние других кнопок мыши, а также клавиши Shift и CTRL.</span><span class="sxs-lookup"><span data-stu-id="c31ec-140">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span>



| <span data-ttu-id="c31ec-141">Flag</span><span class="sxs-lookup"><span data-stu-id="c31ec-141">Flag</span></span>             | <span data-ttu-id="c31ec-142">Значение</span><span class="sxs-lookup"><span data-stu-id="c31ec-142">Meaning</span></span>                          |
|------------------|----------------------------------|
| <span data-ttu-id="c31ec-143">**MK, \_ элемент управления**</span><span class="sxs-lookup"><span data-stu-id="c31ec-143">**MK\_CONTROL**</span></span>  | <span data-ttu-id="c31ec-144">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="c31ec-144">The CTRL key is down.</span></span>            |
| <span data-ttu-id="c31ec-145">**MK \_ лбуттон**</span><span class="sxs-lookup"><span data-stu-id="c31ec-145">**MK\_LBUTTON**</span></span>  | <span data-ttu-id="c31ec-146">Левая кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="c31ec-146">The left mouse button is down.</span></span>   |
| <span data-ttu-id="c31ec-147">**MK \_ мбуттон**</span><span class="sxs-lookup"><span data-stu-id="c31ec-147">**MK\_MBUTTON**</span></span>  | <span data-ttu-id="c31ec-148">Средняя кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="c31ec-148">The middle mouse button is down.</span></span> |
| <span data-ttu-id="c31ec-149">**MK \_ рбуттон**</span><span class="sxs-lookup"><span data-stu-id="c31ec-149">**MK\_RBUTTON**</span></span>  | <span data-ttu-id="c31ec-150">Нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="c31ec-150">The right mouse button is down.</span></span>  |
| <span data-ttu-id="c31ec-151">**MK \_ SHIFT**</span><span class="sxs-lookup"><span data-stu-id="c31ec-151">**MK\_SHIFT**</span></span>    | <span data-ttu-id="c31ec-152">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="c31ec-152">The SHIFT key is down.</span></span>           |
| <span data-ttu-id="c31ec-153">**MK \_ XBUTTON1**</span><span class="sxs-lookup"><span data-stu-id="c31ec-153">**MK\_XBUTTON1**</span></span> | <span data-ttu-id="c31ec-154">Кнопка XBUTTON1 не работает.</span><span class="sxs-lookup"><span data-stu-id="c31ec-154">The XBUTTON1 button is down.</span></span>     |
| <span data-ttu-id="c31ec-155">**MK \_ XBUTTON2**</span><span class="sxs-lookup"><span data-stu-id="c31ec-155">**MK\_XBUTTON2**</span></span> | <span data-ttu-id="c31ec-156">Кнопка XBUTTON2 не работает.</span><span class="sxs-lookup"><span data-stu-id="c31ec-156">The XBUTTON2 button is down.</span></span>     |



 

<span data-ttu-id="c31ec-157">Отсутствие флага означает, что соответствующая кнопка или клавиша не была нажата.</span><span class="sxs-lookup"><span data-stu-id="c31ec-157">The absence of a flag means the corresponding button or key was not pressed.</span></span> <span data-ttu-id="c31ec-158">Например, чтобы проверить, не нажата ли клавиша CTRL, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="c31ec-158">For example, to test whether the CTRL key is down:</span></span>


```C++
if (wParam & MK_CONTROL) { ...
```



<span data-ttu-id="c31ec-159">Если необходимо найти состояние других клавиш, помимо клавиш CTRL и SHIFT, используйте функцию [**жеткэйстате**](/windows/desktop/api/winuser/nf-winuser-getkeystate) , описанную в разделе [Ввод с клавиатуры](keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="c31ec-159">If you need to find the state of other keys besides CTRL and SHIFT, use the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function, which is described in [Keyboard Input](keyboard-input.md).</span></span>

<span data-ttu-id="c31ec-160">Сообщения окон [**WM \_ Ксбуттондовн**](/windows/desktop/inputdev/wm-xbuttondown) и [**WM \_ ксбуттонуп**](/windows/desktop/inputdev/wm-xbuttonup) применяются как к XBUTTON1, так и к XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="c31ec-160">The [**WM\_XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) and [**WM\_XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) window messages apply to both XBUTTON1 and XBUTTON2.</span></span> <span data-ttu-id="c31ec-161">Параметр *wParam* указывает, какая кнопка была нажата.</span><span class="sxs-lookup"><span data-stu-id="c31ec-161">The *wParam* parameter indicates which button was clicked.</span></span>


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a><span data-ttu-id="c31ec-162">Двойные щелчки</span><span class="sxs-lookup"><span data-stu-id="c31ec-162">Double Clicks</span></span>

<span data-ttu-id="c31ec-163">По умолчанию окно не получает уведомлений о двойном щелчке.</span><span class="sxs-lookup"><span data-stu-id="c31ec-163">A window does not receive double-click notifications by default.</span></span> <span data-ttu-id="c31ec-164">Чтобы получить двойные щелчки, установите флаг **CS \_ дблклкс** в структуре [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) при регистрации класса окна.</span><span class="sxs-lookup"><span data-stu-id="c31ec-164">To receive double clicks, set the **CS\_DBLCLKS** flag in the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure when you register the window class.</span></span>


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



<span data-ttu-id="c31ec-165">Если установить флаг **CS \_ дблклкс** как показано, окно будет получать уведомления двойным щелчком.</span><span class="sxs-lookup"><span data-stu-id="c31ec-165">If you set the **CS\_DBLCLKS** flag as shown, the window will receive double-click notifications.</span></span> <span data-ttu-id="c31ec-166">Двойной щелчок обозначается сообщением окна с «ДБЛКЛК» в имени.</span><span class="sxs-lookup"><span data-stu-id="c31ec-166">A double click is indicated by a window message with "DBLCLK" in the name.</span></span> <span data-ttu-id="c31ec-167">Например, двойной щелчок левой кнопкой мыши выдает следующую последовательность сообщений:</span><span class="sxs-lookup"><span data-stu-id="c31ec-167">For example, a double click on the left mouse button produces the following sequence of messages:</span></span>

<dl>

[<span data-ttu-id="c31ec-168">**WM \_ лбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="c31ec-168">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)  
[<span data-ttu-id="c31ec-169">**WM \_ лбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="c31ec-169">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
[<span data-ttu-id="c31ec-170">**WM \_ лбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="c31ec-170">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)  
[<span data-ttu-id="c31ec-171">**WM \_ лбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="c31ec-171">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

<span data-ttu-id="c31ec-172">По сути, второе сообщение [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) , которое обычно создается, превращается в [**сообщение \_ лбуттондблклк WM**](/windows/desktop/inputdev/wm-lbuttondblclk) .</span><span class="sxs-lookup"><span data-stu-id="c31ec-172">In effect, the second [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message that would normally be generated becomes a [**WM\_LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) message.</span></span> <span data-ttu-id="c31ec-173">Эквивалентные сообщения определяются для кнопок "справа", "по середине" и "КСБУТТОН".</span><span class="sxs-lookup"><span data-stu-id="c31ec-173">Equivalent messages are defined for right, middle, and XBUTTON buttons.</span></span>

<span data-ttu-id="c31ec-174">Пока не будет получено сообщение двойного щелчка, невозможно определить, что первый щелчок мыши является началом двойного щелчка.</span><span class="sxs-lookup"><span data-stu-id="c31ec-174">Until you get the double-click message, there is no way to tell that the first mouse click is the start of a double click.</span></span> <span data-ttu-id="c31ec-175">Поэтому действие двойного щелчка должно продолжить действие, которое начинается с первого щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="c31ec-175">Therefore, a double-click action should continue an action that begins with the first mouse click.</span></span> <span data-ttu-id="c31ec-176">Например, в оболочке Windows один щелчок выбирает папку, а двойной щелчок открывает папку.</span><span class="sxs-lookup"><span data-stu-id="c31ec-176">For example, in the Windows Shell, a single click selects a folder, while a double click opens the folder.</span></span>

## <a name="non-client-mouse-messages"></a><span data-ttu-id="c31ec-177">Сообщения, не являющиеся клиентскими мышью</span><span class="sxs-lookup"><span data-stu-id="c31ec-177">Non-client Mouse Messages</span></span>

<span data-ttu-id="c31ec-178">Отдельный набор сообщений определяется для событий мыши, которые происходят в неклиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="c31ec-178">A separate set of messages are defined for mouse events that occur within the non-client area of the window.</span></span> <span data-ttu-id="c31ec-179">Эти сообщения имеют имена "NC" в имени.</span><span class="sxs-lookup"><span data-stu-id="c31ec-179">These messages have the letters "NC" in the name.</span></span> <span data-ttu-id="c31ec-180">Например, [**WM \_ нклбуттондовн**](/windows/desktop/inputdev/wm-nclbuttondown) является неклиентским эквивалентом [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown).</span><span class="sxs-lookup"><span data-stu-id="c31ec-180">For example, [**WM\_NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) is the non-client equivalent of [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="c31ec-181">Обычное приложение не будет перехватывать эти сообщения, так как функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) обрабатывает эти сообщения правильно.</span><span class="sxs-lookup"><span data-stu-id="c31ec-181">A typical application will not intercept these messages, because the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function handles these messages correctly.</span></span> <span data-ttu-id="c31ec-182">Однако они могут быть полезны для некоторых расширенных функций.</span><span class="sxs-lookup"><span data-stu-id="c31ec-182">However, they can be useful for certain advanced functions.</span></span> <span data-ttu-id="c31ec-183">Например, эти сообщения можно использовать для реализации пользовательского поведения в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="c31ec-183">For example, you could use these messages to implement custom behavior in the title bar.</span></span> <span data-ttu-id="c31ec-184">Если вы обработаете эти сообщения, их обычно следует передавать в **дефвиндовпрок** .</span><span class="sxs-lookup"><span data-stu-id="c31ec-184">If you do handle these messages, you should generally pass them to **DefWindowProc** afterward.</span></span> <span data-ttu-id="c31ec-185">В противном случае приложение будет прерывать стандартные функциональные возможности, такие как перетаскивание или свертывание окна.</span><span class="sxs-lookup"><span data-stu-id="c31ec-185">Otherwise, your application will break standard functionality such as dragging or minimizing the window.</span></span>

## <a name="next"></a><span data-ttu-id="c31ec-186">Следующая</span><span class="sxs-lookup"><span data-stu-id="c31ec-186">Next</span></span>

[<span data-ttu-id="c31ec-187">Перемещение мыши</span><span class="sxs-lookup"><span data-stu-id="c31ec-187">Mouse Movement</span></span>](mouse-movement.md)

 

 