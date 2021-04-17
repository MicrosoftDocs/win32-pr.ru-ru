---
title: Перемещение мыши
description: Перемещение мыши
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "105684720"
---
# <a name="mouse-movement"></a><span data-ttu-id="cc803-103">Перемещение мыши</span><span class="sxs-lookup"><span data-stu-id="cc803-103">Mouse Movement</span></span>

<span data-ttu-id="cc803-104">При перемещении мыши Windows отправляет сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="cc803-104">When the mouse moves, Windows posts a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="cc803-105">По умолчанию **WM \_ MOUSEMOVE** перемещается в окно, содержащее курсор.</span><span class="sxs-lookup"><span data-stu-id="cc803-105">By default, **WM\_MOUSEMOVE** goes to the window that contains the cursor.</span></span> <span data-ttu-id="cc803-106">Это поведение можно переопределить, *записывая* мышь, которая описана в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="cc803-106">You can override this behavior by *capturing* the mouse, which is described in the next section.</span></span>

<span data-ttu-id="cc803-107">Сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) содержит те же параметры, что и сообщения для щелчков мыши.</span><span class="sxs-lookup"><span data-stu-id="cc803-107">The [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message contains the same parameters as the messages for mouse clicks.</span></span> <span data-ttu-id="cc803-108">Младшие 16 бит *lParam* содержат координату x, а следующие 16 бит содержат координату y.</span><span class="sxs-lookup"><span data-stu-id="cc803-108">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="cc803-109">Используйте макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для распаковки координат из *lParam*.</span><span class="sxs-lookup"><span data-stu-id="cc803-109">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span> <span data-ttu-id="cc803-110">Параметр *wParam* содержит побитовое **или** для флагов, указывающих состояние других кнопок мыши, а также клавиши Shift и CTRL.</span><span class="sxs-lookup"><span data-stu-id="cc803-110">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span> <span data-ttu-id="cc803-111">Следующий код получает координаты мыши от *lParam*.</span><span class="sxs-lookup"><span data-stu-id="cc803-111">The following code gets the mouse coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="cc803-112">Помните, что эти координаты находятся в пикселях, а не в аппаратно-независимых пикселях (DIP).</span><span class="sxs-lookup"><span data-stu-id="cc803-112">Remember that these coordinates are in pixels, not device-independent pixels (DIPs).</span></span> <span data-ttu-id="cc803-113">Далее в этом разделе мы рассмотрим код, который выполняет преобразование между двумя единицами.</span><span class="sxs-lookup"><span data-stu-id="cc803-113">Later in this topic, we will look at code that converts between the two units.</span></span>

<span data-ttu-id="cc803-114">Окно также может получить сообщение [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , если положения курсора меняются относительно окна.</span><span class="sxs-lookup"><span data-stu-id="cc803-114">A window can also receive a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message if the position of the cursor changes relative to the window.</span></span> <span data-ttu-id="cc803-115">Например, если курсор находится над окном, а пользователь скрывает окно, окно получает сообщения **WM \_ MOUSEMOVE** , даже если мышь не была перемещена.</span><span class="sxs-lookup"><span data-stu-id="cc803-115">For example, if the cursor is positioned over a window, and the user hides the window, the window receives **WM\_MOUSEMOVE** messages even if the mouse did not move.</span></span> <span data-ttu-id="cc803-116">Одним из последствий такого поведения является то, что координаты мыши могут не меняться между сообщениями **WM \_ MOUSEMOVE** .</span><span class="sxs-lookup"><span data-stu-id="cc803-116">One consequence of this behavior is that the mouse coordinates might not change between **WM\_MOUSEMOVE** messages.</span></span>

## <a name="capturing-mouse-movement-outside-the-window"></a><span data-ttu-id="cc803-117">Захват перемещения мыши за пределами окна</span><span class="sxs-lookup"><span data-stu-id="cc803-117">Capturing Mouse Movement Outside the Window</span></span>

<span data-ttu-id="cc803-118">По умолчанию окно прекращает получать сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , если мышь перемещается за границей клиентской области.</span><span class="sxs-lookup"><span data-stu-id="cc803-118">By default, a window stops receiving [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages if the mouse moves past the edge of the client area.</span></span> <span data-ttu-id="cc803-119">Но для некоторых операций может потребоваться отслеживание позиции мыши за пределами этой точки.</span><span class="sxs-lookup"><span data-stu-id="cc803-119">But for some operations, you might need to track the mouse position beyond this point.</span></span> <span data-ttu-id="cc803-120">Например, программа рисования может позволить пользователю перетаскивать прямоугольник выделения за пределы окна, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="cc803-120">For example, a drawing program might enable the user to drag the selection rectangle beyond the edge of the window, as shown in the following diagram.</span></span>

![Иллюстрация захвата мыши.](images/input01.png)

<span data-ttu-id="cc803-122">Чтобы получить сообщения, перемещаемые с помощью мыши, за границей окна, вызовите функцию [**сеткаптуре**](/windows/desktop/api/winuser/nf-winuser-setcapture) .</span><span class="sxs-lookup"><span data-stu-id="cc803-122">To receive mouse-move messages past the edge of the window, call the [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) function.</span></span> <span data-ttu-id="cc803-123">После вызова этой функции окно продолжает принимать сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) в течение всего времени, когда пользователь удерживает по крайней мере одну кнопку мыши, даже если мышь перемещается за пределы окна.</span><span class="sxs-lookup"><span data-stu-id="cc803-123">After this function is called, the window will continue to receive [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages for as long as the user holds at least one mouse button down, even if the mouse moves outside the window.</span></span> <span data-ttu-id="cc803-124">Окно захвата должно быть окном переднего плана, и только одно окно может быть окном захвата за раз.</span><span class="sxs-lookup"><span data-stu-id="cc803-124">The capture window must be the foreground window, and only one window can be the capture window at a time.</span></span> <span data-ttu-id="cc803-125">Чтобы освободить захват мыши, вызовите функцию [**релеасекаптуре**](/windows/desktop/api/winuser/nf-winuser-releasecapture) .</span><span class="sxs-lookup"><span data-stu-id="cc803-125">To release mouse capture, call the [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) function.</span></span>

<span data-ttu-id="cc803-126">Обычно [**сеткаптуре**](/windows/desktop/api/winuser/nf-winuser-setcapture) и [**релеасекаптуре**](/windows/desktop/api/winuser/nf-winuser-releasecapture) используются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="cc803-126">You would typically use [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) and [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) in the following way.</span></span>

1.  <span data-ttu-id="cc803-127">Когда пользователь нажимает левую кнопку мыши, вызовите [**сеткаптуре**](/windows/desktop/api/winuser/nf-winuser-setcapture) , чтобы начать захват мыши.</span><span class="sxs-lookup"><span data-stu-id="cc803-127">When the user presses the left mouse button, call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to start capturing the mouse.</span></span>
2.  <span data-ttu-id="cc803-128">Реагирование на сообщения, перемещаемые мышью.</span><span class="sxs-lookup"><span data-stu-id="cc803-128">Respond to mouse-move messages.</span></span>
3.  <span data-ttu-id="cc803-129">Когда пользователь отпускает левую кнопку мыши, вызовите [**релеасекаптуре**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span><span class="sxs-lookup"><span data-stu-id="cc803-129">When the user releases the left mouse button, call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span></span>

## <a name="example-drawing-circles"></a><span data-ttu-id="cc803-130">Пример: Рисование кругов</span><span class="sxs-lookup"><span data-stu-id="cc803-130">Example: Drawing Circles</span></span>

<span data-ttu-id="cc803-131">Добавим круговую программу из [модуля 3](module-3---windows-graphics.md) , позволяя пользователю рисовать окружность с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="cc803-131">Let's extend the Circle program from [Module 3](module-3---windows-graphics.md) by enabling the user to draw a circle with the mouse.</span></span> <span data-ttu-id="cc803-132">Начните с [примера программы Direct2D Circle](direct2d-circle-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="cc803-132">Start with the [Direct2D Circle Sample](direct2d-circle-sample.md) program.</span></span> <span data-ttu-id="cc803-133">Мы изменим код в этом примере, чтобы добавить простой рисунок.</span><span class="sxs-lookup"><span data-stu-id="cc803-133">We will modify the code in this sample to add simple drawing.</span></span> <span data-ttu-id="cc803-134">Сначала добавьте в класс новую переменную-член `MainWindow` .</span><span class="sxs-lookup"><span data-stu-id="cc803-134">First, add a new member variable to the `MainWindow` class.</span></span>


```C++
    D2D1_POINT_2F           ptMouse;
```



<span data-ttu-id="cc803-135">Эта переменная сохраняет указатель мыши в то время, когда пользователь перетаскивает указатель мыши.</span><span class="sxs-lookup"><span data-stu-id="cc803-135">This variable stores the mouse-down position while the user is dragging the mouse.</span></span> <span data-ttu-id="cc803-136">В `MainWindow` конструкторе Инициализируйте переменные *Ellipse* и *птмаусе* .</span><span class="sxs-lookup"><span data-stu-id="cc803-136">In the `MainWindow` constructor, initialize the *ellipse* and *ptMouse* variables.</span></span>


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



<span data-ttu-id="cc803-137">Удалите текст `MainWindow::CalculateLayout` метода; он не является обязательным для этого примера.</span><span class="sxs-lookup"><span data-stu-id="cc803-137">Remove the body of the `MainWindow::CalculateLayout` method; it's not required for this example.</span></span>


```C++
    void    CalculateLayout() { }
```



<span data-ttu-id="cc803-138">Затем объявите обработчики сообщений для левой кнопки вниз, левой кнопки вверх и переместите сообщения.</span><span class="sxs-lookup"><span data-stu-id="cc803-138">Next, declare message handlers for the left-button down, left-button up, and mouse-move messages.</span></span>


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



<span data-ttu-id="cc803-139">Координаты мыши задаются в физических пикселях, но Direct2D — аппаратно-независимые пиксели (DIP).</span><span class="sxs-lookup"><span data-stu-id="cc803-139">Mouse coordinates are given in physical pixels, but Direct2D expects device-independent pixels (DIPs).</span></span> <span data-ttu-id="cc803-140">Чтобы правильно обрабатывались параметры с высоким разрешением, необходимо преобразовать координаты пикселя в DIP.</span><span class="sxs-lookup"><span data-stu-id="cc803-140">To handle high-DPI settings correctly, you must translate the pixel coordinates into DIPs.</span></span> <span data-ttu-id="cc803-141">Дополнительные сведения о DPI см. в разделе [dpi и Device-Independent пикселей](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="cc803-141">For more discussion about DPI, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span> <span data-ttu-id="cc803-142">В следующем коде показан вспомогательный класс, который преобразует пиксели в DIP.</span><span class="sxs-lookup"><span data-stu-id="cc803-142">The following code shows a helper class that converts pixels into DIPs.</span></span>


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



<span data-ttu-id="cc803-143">`DPIScale::Initialize`После создания объекта фабрики Direct2D вызовите в обработчике [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="cc803-143">Call `DPIScale::Initialize` in your [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) handler, after you create the Direct2D factory object.</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



<span data-ttu-id="cc803-144">Чтобы получить координаты мыши в DIP из сообщений мыши, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cc803-144">To get the mouse coordinates in DIPs from the mouse messages, do the following:</span></span>

1.  <span data-ttu-id="cc803-145">Используйте макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для получения координат пикселя.</span><span class="sxs-lookup"><span data-stu-id="cc803-145">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to get the pixel coordinates.</span></span> <span data-ttu-id="cc803-146">Эти макросы определяются в Виндовскс. h, поэтому не забудьте включить этот заголовок в проект.</span><span class="sxs-lookup"><span data-stu-id="cc803-146">These macros are defined in WindowsX.h, so remember to include that header in your project.</span></span>
2.  <span data-ttu-id="cc803-147">Вызовите метод `DPIScale::PixelsToDipsX` и `DPIScale::PixelsToDipsY` , чтобы преобразовать Пиксели в DIP.</span><span class="sxs-lookup"><span data-stu-id="cc803-147">Call `DPIScale::PixelsToDipsX` and `DPIScale::PixelsToDipsY` to convert pixels to DIPs.</span></span>

<span data-ttu-id="cc803-148">Теперь добавьте обработчики сообщений в процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="cc803-148">Now add the message handlers to your window procedure.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



<span data-ttu-id="cc803-149">Наконец, реализуйте сами обработчики сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc803-149">Finally, implement the message handlers themselves.</span></span>

### <a name="left-button-down"></a><span data-ttu-id="cc803-150">Левая кнопка вниз</span><span class="sxs-lookup"><span data-stu-id="cc803-150">Left Button Down</span></span>

<span data-ttu-id="cc803-151">Для сообщения, расположенного слева, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cc803-151">For the left-button down message, do the following:</span></span>

1.  <span data-ttu-id="cc803-152">Вызовите [**сеткаптуре**](/windows/desktop/api/winuser/nf-winuser-setcapture) , чтобы начать захват мыши.</span><span class="sxs-lookup"><span data-stu-id="cc803-152">Call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to begin capturing the mouse.</span></span>
2.  <span data-ttu-id="cc803-153">Сохраните расположение щелчка мыши в переменной *птмаусе* .</span><span class="sxs-lookup"><span data-stu-id="cc803-153">Store the position of the mouse click in the *ptMouse* variable.</span></span> <span data-ttu-id="cc803-154">Это расположение определяет верхний левый угол ограничивающего прямоугольника для эллипса.</span><span class="sxs-lookup"><span data-stu-id="cc803-154">This position defines the upper left corner of the bounding box for the ellipse.</span></span>
3.  <span data-ttu-id="cc803-155">Сброс структуры эллипса.</span><span class="sxs-lookup"><span data-stu-id="cc803-155">Reset the ellipse structure.</span></span>
4.  <span data-ttu-id="cc803-156">Вызовите [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="cc803-156">Call [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="cc803-157">Эта функция заставляет окно перерисовываться.</span><span class="sxs-lookup"><span data-stu-id="cc803-157">This function forces the window to be repainted.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a><span data-ttu-id="cc803-158">Перемещение мыши</span><span class="sxs-lookup"><span data-stu-id="cc803-158">Mouse Move</span></span>

<span data-ttu-id="cc803-159">Для сообщения о перемещении мыши проверьте, не отключена ли левая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="cc803-159">For the mouse-move message, check whether the left mouse button is down.</span></span> <span data-ttu-id="cc803-160">Если это так, повторно Вычислите эллипс и перерисовывает окно.</span><span class="sxs-lookup"><span data-stu-id="cc803-160">If it is, recalculate the ellipse and repaint the window.</span></span> <span data-ttu-id="cc803-161">В Direct2D Эллипс определяется центральной точкой и осями x и y.</span><span class="sxs-lookup"><span data-stu-id="cc803-161">In Direct2D, an ellipse is defined by the center point and x- and y-radii.</span></span> <span data-ttu-id="cc803-162">Нам нужно нарисовать эллипс, соответствующий ограничивающему прямоугольнику, определенному точкой (*птмаусе*) и текущей позицией курсора (*x*, *y*), поэтому для поиска ширины, высоты и положения эллипса требуется несколько арифметических действий.</span><span class="sxs-lookup"><span data-stu-id="cc803-162">We want to draw an ellipse that fits the bounding box defined by the mouse-down point (*ptMouse*) and the current cursor position (*x*, *y*), so a bit of arithmetic is needed to find the width, height, and position of the ellipse.</span></span>

<span data-ttu-id="cc803-163">Следующий код повторно вычисляет эллипс, а затем вызывает [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) для перерисовки окна.</span><span class="sxs-lookup"><span data-stu-id="cc803-163">The following code recalculates the ellipse and then calls [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) to repaint the window.</span></span>

![Схема, на которой показан эллипс с радиусами x и y.](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a><span data-ttu-id="cc803-165">Кнопка "влево"</span><span class="sxs-lookup"><span data-stu-id="cc803-165">Left Button Up</span></span>

<span data-ttu-id="cc803-166">Для сообщения с левой кнопкой мыши просто вызовите [**релеасекаптуре**](/windows/desktop/api/winuser/nf-winuser-releasecapture) , чтобы освободить мышь.</span><span class="sxs-lookup"><span data-stu-id="cc803-166">For the left-button-up message, simply call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) to release the mouse capture.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a><span data-ttu-id="cc803-167">Следующая</span><span class="sxs-lookup"><span data-stu-id="cc803-167">Next</span></span>

[<span data-ttu-id="cc803-168">Другие операции с мышью</span><span class="sxs-lookup"><span data-stu-id="cc803-168">Other Mouse Operations</span></span>](other-mouse-operations.md)

 

 