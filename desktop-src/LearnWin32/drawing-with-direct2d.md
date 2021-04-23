---
title: Рисование с использованием Direct2D
description: После создания графических ресурсов можно приступать к рисованию.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487612"
---
# <a name="drawing-with-direct2d"></a><span data-ttu-id="1d117-103">Рисование с использованием Direct2D</span><span class="sxs-lookup"><span data-stu-id="1d117-103">Drawing with Direct2D</span></span>

<span data-ttu-id="1d117-104">После создания графических ресурсов можно приступать к рисованию.</span><span class="sxs-lookup"><span data-stu-id="1d117-104">After you create your graphics resources, you are ready to draw.</span></span>

## <a name="drawing-an-ellipse"></a><span data-ttu-id="1d117-105">Рисование эллипса</span><span class="sxs-lookup"><span data-stu-id="1d117-105">Drawing an Ellipse</span></span>

<span data-ttu-id="1d117-106">Программа [Circle](your-first-direct2d-program.md) выполняет очень простую логику рисования:</span><span class="sxs-lookup"><span data-stu-id="1d117-106">The [Circle](your-first-direct2d-program.md) program performs very simple drawing logic:</span></span>

1.  <span data-ttu-id="1d117-107">Заполните фон сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="1d117-107">Fill the background with a solid color.</span></span>
2.  <span data-ttu-id="1d117-108">Рисование заполненного круга.</span><span class="sxs-lookup"><span data-stu-id="1d117-108">Draw a filled circle.</span></span>

![снимок экрана программы круга.](images/graphics08.png)

<span data-ttu-id="1d117-110">Так как целевой объект прорисовки является окном (а не точечным рисунком или другой заданной областью), рисование выполняется в ответ на сообщения [**\_ рисования WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="1d117-110">Because the render target is a window (as opposed to a bitmap or other offscreen surface), drawing is done in response to [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) messages.</span></span> <span data-ttu-id="1d117-111">В следующем коде показана процедура окна для круговой программы.</span><span class="sxs-lookup"><span data-stu-id="1d117-111">The following code shows the window procedure for the Circle program.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

<span data-ttu-id="1d117-112">Вот код, который рисует окружность.</span><span class="sxs-lookup"><span data-stu-id="1d117-112">Here is the code that draws the circle.</span></span>

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="1d117-113">Интерфейс [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) используется для всех операций рисования.</span><span class="sxs-lookup"><span data-stu-id="1d117-113">The [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface is used for all drawing operations.</span></span> <span data-ttu-id="1d117-114">`OnPaint`Метод программы выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1d117-114">The program's `OnPaint` method does the following:</span></span>

1.  <span data-ttu-id="1d117-115">Метод [**ID2D1RenderTarget:: бегиндрав**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) сигнализирует о начале рисования.</span><span class="sxs-lookup"><span data-stu-id="1d117-115">The [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method signals the start of drawing.</span></span>
2.  <span data-ttu-id="1d117-116">Метод [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) заполняет весь целевой объект отрисовки сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="1d117-116">The [**ID2D1RenderTarget::Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) method fills the entire render target with a solid color.</span></span> <span data-ttu-id="1d117-117">Цвет задается в виде структуры [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="1d117-117">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure.</span></span> <span data-ttu-id="1d117-118">Для инициализации структуры можно использовать класс [**D2D1:: колорф**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="1d117-118">You can use the [**D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class to initialize the structure.</span></span> <span data-ttu-id="1d117-119">Дополнительные сведения см. [в разделе Использование цвета в Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="1d117-119">For more information, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>
3.  <span data-ttu-id="1d117-120">Метод [**ID2D1RenderTarget:: филлеллипсе**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) Рисует закрашенный эллипс, используя указанную кисть для заливки.</span><span class="sxs-lookup"><span data-stu-id="1d117-120">The [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws a filled ellipse, using the specified brush for the fill.</span></span> <span data-ttu-id="1d117-121">Эллипс задается центральной точкой и осями x и y.</span><span class="sxs-lookup"><span data-stu-id="1d117-121">An ellipse is specified by a center point and the x- and y-radii.</span></span> <span data-ttu-id="1d117-122">Если оси x и y одинаковы, результатом будет окружность.</span><span class="sxs-lookup"><span data-stu-id="1d117-122">If the x- and y-radii are the same, the result is a circle.</span></span>
4.  <span data-ttu-id="1d117-123">Метод [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) сигнализирует о завершении рисования для этого кадра.</span><span class="sxs-lookup"><span data-stu-id="1d117-123">The [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method signals the completion of drawing for this frame.</span></span> <span data-ttu-id="1d117-124">Все операции рисования должны размещаться между вызовами [**бегиндрав**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) и **EndDraw**.</span><span class="sxs-lookup"><span data-stu-id="1d117-124">All drawing operations must be placed between calls to [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw**.</span></span>

<span data-ttu-id="1d117-125">Методы [**бегиндрав**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)и [**филлеллипсе**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) имеют тип возвращаемого значения **void** .</span><span class="sxs-lookup"><span data-stu-id="1d117-125">The [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear), and [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) methods all have a **void** return type.</span></span> <span data-ttu-id="1d117-126">Если во время выполнения любого из этих методов возникает ошибка, то эта ошибка сообщается через возвращаемое значение метода [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="1d117-126">If an error occurs during the execution of any of these methods, the error is signaled through the return value of the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="1d117-127">`CreateGraphicsResources`Метод показан в разделе [Создание ресурсов Direct2D](render-targets--devices--and-resources.md).</span><span class="sxs-lookup"><span data-stu-id="1d117-127">The `CreateGraphicsResources` method is shown in the topic [Creating Direct2D Resources](render-targets--devices--and-resources.md).</span></span> <span data-ttu-id="1d117-128">Этот метод создает целевой объект отрисовки и Кисть сплошного цвета.</span><span class="sxs-lookup"><span data-stu-id="1d117-128">This method creates the render target and the solid-color brush.</span></span>

<span data-ttu-id="1d117-129">Устройство может буферизовать команды рисования и откладывать их выполнение до тех пор, пока не будет вызван [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="1d117-129">The device might buffer the drawing commands and defer executing them until [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) is called.</span></span> <span data-ttu-id="1d117-130">Можно заставить устройство выполнять любые ожидающие команды рисования, вызывая [**ID2D1RenderTarget:: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="1d117-130">You can force the device to execute any pending drawing commands by calling [**ID2D1RenderTarget::Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span> <span data-ttu-id="1d117-131">Однако при сбросе может снизиться производительность.</span><span class="sxs-lookup"><span data-stu-id="1d117-131">Flushing can reduce performance, however.</span></span>

## <a name="handling-device-loss"></a><span data-ttu-id="1d117-132">Обработка потери устройства</span><span class="sxs-lookup"><span data-stu-id="1d117-132">Handling Device Loss</span></span>

<span data-ttu-id="1d117-133">Во время выполнения программы используемое графическое устройство может стать недоступным.</span><span class="sxs-lookup"><span data-stu-id="1d117-133">While your program is running, the graphics device that you are using might become unavailable.</span></span> <span data-ttu-id="1d117-134">Например, устройство может быть потеряно при изменении разрешения экрана или при удалении пользователем видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="1d117-134">For example, the device can be lost if the display resolution changes, or if the user removes the display adapter.</span></span> <span data-ttu-id="1d117-135">Если устройство потеряно, то целевой объект рендеринга также становится недействительным, наряду с ресурсами, зависящими от устройства, которые были связаны с устройством.</span><span class="sxs-lookup"><span data-stu-id="1d117-135">If the device is lost, the render target also becomes invalid, along with any device-dependent resources that were associated with the device.</span></span> <span data-ttu-id="1d117-136">Direct2D передает потерянное устройство, возвращая код ошибки **D2DERR \_ Повторное создание \_ целевого объекта** из метода [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="1d117-136">Direct2D signals a lost device by returning the error code **D2DERR\_RECREATE\_TARGET** from the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="1d117-137">Если вы получаете этот код ошибки, необходимо повторно создать целевой объект рендеринга и все ресурсы, зависящие от устройства.</span><span class="sxs-lookup"><span data-stu-id="1d117-137">If you receive this error code, you must re-create the render target and all device-dependent resources.</span></span>

<span data-ttu-id="1d117-138">Чтобы отменить ресурс, просто освободите интерфейс для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="1d117-138">To discard a resource, simply release the interface for that resource.</span></span>


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



<span data-ttu-id="1d117-139">Создание ресурса может быть дорогостоящей операцией, поэтому не следует повторно создавать ресурсы для каждого сообщения [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="1d117-139">Creating a resource can be an expensive operation, so do not recreate your resources for every [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="1d117-140">Создайте ресурс один раз и кэшировать указатель ресурса, пока ресурс не станет недопустимым из-за потери устройства или пока не будет нужен ресурс.</span><span class="sxs-lookup"><span data-stu-id="1d117-140">Create a resource once, and cache the resource pointer until the resource becomes invalid due to device loss, or until you no longer need that resource.</span></span>

## <a name="the-direct2d-render-loop"></a><span data-ttu-id="1d117-141">Цикл рендеринга Direct2D</span><span class="sxs-lookup"><span data-stu-id="1d117-141">The Direct2D Render Loop</span></span>

<span data-ttu-id="1d117-142">Независимо от того, что вы рисуете, программа должна выполнить цикл, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="1d117-142">Regardless of what you draw, your program should perform a loop similar to following.</span></span>

1.  <span data-ttu-id="1d117-143">Создание ресурсов, независимых от устройства.</span><span class="sxs-lookup"><span data-stu-id="1d117-143">Create device-independent resources.</span></span>
2.  <span data-ttu-id="1d117-144">Отрисовка сцены.</span><span class="sxs-lookup"><span data-stu-id="1d117-144">Render the scene.</span></span>
    1.  <span data-ttu-id="1d117-145">Проверьте, существует ли допустимый целевой объект рендеринга.</span><span class="sxs-lookup"><span data-stu-id="1d117-145">Check if a valid render target exists.</span></span> <span data-ttu-id="1d117-146">В противном случае создайте целевой объект рендеринга и ресурсы, зависящие от устройства.</span><span class="sxs-lookup"><span data-stu-id="1d117-146">If not, create the render target and the device-dependent resources.</span></span>
    2.  <span data-ttu-id="1d117-147">Вызовите [**ID2D1RenderTarget:: бегиндрав**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span><span class="sxs-lookup"><span data-stu-id="1d117-147">Call [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span></span>
    3.  <span data-ttu-id="1d117-148">Выдача команд рисования.</span><span class="sxs-lookup"><span data-stu-id="1d117-148">Issue drawing commands.</span></span>
    4.  <span data-ttu-id="1d117-149">Вызовите [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="1d117-149">Call [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>
    5.  <span data-ttu-id="1d117-150">Если [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) возвращает **\_ \_ целевой объект D2DERR recreate**, удалите целевой объект рендеринга и ресурсы, зависящие от устройства.</span><span class="sxs-lookup"><span data-stu-id="1d117-150">If [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) returns **D2DERR\_RECREATE\_TARGET**, discard the render target and device-dependent resources.</span></span>
3.  <span data-ttu-id="1d117-151">Повторите шаг 2 при необходимости обновить или перерисовать сцену.</span><span class="sxs-lookup"><span data-stu-id="1d117-151">Repeat step 2 whenever you need to update or redraw the scene.</span></span>

<span data-ttu-id="1d117-152">Если целевой объект прорисовки является окном, шаг 2 возникает каждый раз, когда окно получает сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="1d117-152">If the render target is a window, step 2 occurs whenever the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="1d117-153">Приведенный здесь цикл обрабатывает потери устройства, удаляя ресурсы, зависящие от устройства, и повторно создавая их в начале следующего цикла (шаг 2A).</span><span class="sxs-lookup"><span data-stu-id="1d117-153">The loop shown here handles device loss by discarding the device-dependent resources and re-creating them at the start of the next loop (step 2a).</span></span>

## <a name="next"></a><span data-ttu-id="1d117-154">Следующая</span><span class="sxs-lookup"><span data-stu-id="1d117-154">Next</span></span>

[<span data-ttu-id="1d117-155">DPI и Device-Independent пикселей</span><span class="sxs-lookup"><span data-stu-id="1d117-155">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)

 

 