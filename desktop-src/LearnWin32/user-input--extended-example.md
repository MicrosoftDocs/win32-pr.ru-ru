---
title: Расширенный пример входных данных пользователя
description: .
ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdde7f14dda356d0f65103c77e3b73c2f0de50a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104558218"
---
# <a name="user-input-extended-example"></a><span data-ttu-id="fe21d-103">Ввод данных пользователем: Расширенный пример</span><span class="sxs-lookup"><span data-stu-id="fe21d-103">User Input: Extended Example</span></span>

<span data-ttu-id="fe21d-104">Объедините все, что мы узнали о вводе данных пользователем для создания простой программы рисования.</span><span class="sxs-lookup"><span data-stu-id="fe21d-104">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="fe21d-105">Ниже приведен снимок экрана программы:</span><span class="sxs-lookup"><span data-stu-id="fe21d-105">Here is a screen shot of the program:</span></span>

![снимок экрана программы рисования](images/input03.png)

<span data-ttu-id="fe21d-107">Пользователь может рисовать многоточие в нескольких разных цветах, а также выбирать, перемещать или удалять эллипсы.</span><span class="sxs-lookup"><span data-stu-id="fe21d-107">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="fe21d-108">Чтобы не усложнять пользовательский интерфейс, программа не позволяет пользователю выбрать цвета эллипса.</span><span class="sxs-lookup"><span data-stu-id="fe21d-108">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="fe21d-109">Вместо этого программа автоматически выполняет циклический перебор заранее определенного списка цветов.</span><span class="sxs-lookup"><span data-stu-id="fe21d-109">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="fe21d-110">Программа не поддерживает никакие фигуры, кроме эллипсов.</span><span class="sxs-lookup"><span data-stu-id="fe21d-110">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="fe21d-111">Очевидно, что эта программа не будет Выиграйте никаких наград по графическому программному обеспечению.</span><span class="sxs-lookup"><span data-stu-id="fe21d-111">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="fe21d-112">Тем не менее, это еще один полезный пример для изучения.</span><span class="sxs-lookup"><span data-stu-id="fe21d-112">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="fe21d-113">Вы можете скачать полный исходный код из [простого примера рисования](simple-drawing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="fe21d-113">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="fe21d-114">В этом разделе рассматриваются некоторые особенности.</span><span class="sxs-lookup"><span data-stu-id="fe21d-114">This section will just cover some highlights.</span></span>

<span data-ttu-id="fe21d-115">Многоточие представлено в программе структурой, содержащей эллипсы ([**D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) и Color ([**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)).</span><span class="sxs-lookup"><span data-stu-id="fe21d-115">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="fe21d-116">Структура также определяет два метода: метод для рисования эллипса и метод для выполнения проверки нажатия.</span><span class="sxs-lookup"><span data-stu-id="fe21d-116">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


```C++
struct MyEllipse
{
    D2D1_ELLIPSE    ellipse;
    D2D1_COLOR_F    color;

    void Draw(ID2D1RenderTarget *pRT, ID2D1SolidColorBrush *pBrush)
    {
        pBrush->SetColor(color);
        pRT->FillEllipse(ellipse, pBrush);
        pBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black));
        pRT->DrawEllipse(ellipse, pBrush, 1.0f);
    }

    BOOL HitTest(float x, float y)
    {
        const float a = ellipse.radiusX;
        const float b = ellipse.radiusY;
        const float x1 = x - ellipse.point.x;
        const float y1 = y - ellipse.point.y;
        const float d = ((x1 * x1) / (a * a)) + ((y1 * y1) / (b * b));
        return d <= 1.0f;
    }
};
```



<span data-ttu-id="fe21d-117">Программа использует ту же Кисть сплошного цвета для рисования заливки и контура для каждого эллипса, изменяя цвет при необходимости.</span><span class="sxs-lookup"><span data-stu-id="fe21d-117">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="fe21d-118">В Direct2D изменение цвета кисти с сплошным цветом является эффективной операцией.</span><span class="sxs-lookup"><span data-stu-id="fe21d-118">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="fe21d-119">Таким образом, объект кисти в сплошном цвете поддерживает метод [**сетколор**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .</span><span class="sxs-lookup"><span data-stu-id="fe21d-119">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="fe21d-120">Многоточие хранится в контейнере **списка** STL:</span><span class="sxs-lookup"><span data-stu-id="fe21d-120">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="fe21d-121">**Shared \_ ptr** — это класс интеллектуальных указателей, добавленный в C++ в TR1 и формализованный в C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="fe21d-121">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="fe21d-122">В Visual Studio 2010 добавлена поддержка **общих \_** компонентов r и других функций C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="fe21d-122">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="fe21d-123">Дополнительные сведения см. в разделе [изучение новых функций C++ и MFC в Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) в *журнале MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="fe21d-123">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="fe21d-124">(Этот ресурс может быть недоступен в некоторых языках и странах.)</span><span class="sxs-lookup"><span data-stu-id="fe21d-124">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="fe21d-125">Программа имеет три режима:</span><span class="sxs-lookup"><span data-stu-id="fe21d-125">The program has three modes:</span></span>

-   <span data-ttu-id="fe21d-126">Режим рисования.</span><span class="sxs-lookup"><span data-stu-id="fe21d-126">Draw mode.</span></span> <span data-ttu-id="fe21d-127">Пользователь может нарисовать новые эллипсы.</span><span class="sxs-lookup"><span data-stu-id="fe21d-127">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="fe21d-128">Режим выбора.</span><span class="sxs-lookup"><span data-stu-id="fe21d-128">Selection mode.</span></span> <span data-ttu-id="fe21d-129">Пользователь может выбрать эллипс.</span><span class="sxs-lookup"><span data-stu-id="fe21d-129">The user can select an ellipse.</span></span>
-   <span data-ttu-id="fe21d-130">Режим перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="fe21d-130">Drag mode.</span></span> <span data-ttu-id="fe21d-131">Пользователь может перетащить выбранный эллипс.</span><span class="sxs-lookup"><span data-stu-id="fe21d-131">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="fe21d-132">Пользователь может переключаться между режимом рисования и режимом выделения с помощью тех же сочетаний клавиш, которые описаны в разделе [таблицы сочетаний клавиш](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fe21d-132">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="fe21d-133">В режиме выбора программа переключается в режим перетаскивания, если пользователь щелкнет эллипс.</span><span class="sxs-lookup"><span data-stu-id="fe21d-133">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="fe21d-134">Он переключается обратно в режим выбора, когда пользователь отпускает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="fe21d-134">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="fe21d-135">Текущий выделенный фрагмент хранится в виде итератора в списке эллипсов.</span><span class="sxs-lookup"><span data-stu-id="fe21d-135">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="fe21d-136">Вспомогательный метод `MainWindow::Selection` возвращает указатель на выбранный эллипс или значение **nullptr** , если ничего не выбрано.</span><span class="sxs-lookup"><span data-stu-id="fe21d-136">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


```C++
    list<shared_ptr<MyEllipse>>::iterator   selection;
     
    shared_ptr<MyEllipse> Selection() 
    { 
        if (selection == ellipses.end()) 
        { 
            return nullptr;
        }
        else
        {
            return (*selection);
        }
    }

    void    ClearSelection() { selection = ellipses.end(); }
```



<span data-ttu-id="fe21d-137">В следующей таблице перечислены эффекты ввода с помощью мыши в каждом из трех режимов.</span><span class="sxs-lookup"><span data-stu-id="fe21d-137">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="fe21d-138">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="fe21d-138">Mouse Input</span></span>      | <span data-ttu-id="fe21d-139">Режим рисования</span><span class="sxs-lookup"><span data-stu-id="fe21d-139">Draw Mode</span></span>                                          | <span data-ttu-id="fe21d-140">Режим выбора</span><span class="sxs-lookup"><span data-stu-id="fe21d-140">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="fe21d-141">Режим перетаскивания</span><span class="sxs-lookup"><span data-stu-id="fe21d-141">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="fe21d-142">Левая кнопка вниз</span><span class="sxs-lookup"><span data-stu-id="fe21d-142">Left button down</span></span> | <span data-ttu-id="fe21d-143">Установите захват мыши и начните рисовать новый эллипс.</span><span class="sxs-lookup"><span data-stu-id="fe21d-143">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="fe21d-144">Освобождение текущего выделения и выполнение проверки нажатия.</span><span class="sxs-lookup"><span data-stu-id="fe21d-144">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="fe21d-145">Если достигнуто многоточие, захватите курсор, выберите эллипс и переключитесь в режим перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="fe21d-145">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="fe21d-146">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="fe21d-146">No action.</span></span>                 |
| <span data-ttu-id="fe21d-147">Перемещение мыши</span><span class="sxs-lookup"><span data-stu-id="fe21d-147">Mouse move</span></span>       | <span data-ttu-id="fe21d-148">Если левая кнопка не работает, измените размер эллипса.</span><span class="sxs-lookup"><span data-stu-id="fe21d-148">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="fe21d-149">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="fe21d-149">No action.</span></span>                                                                                                                                   | <span data-ttu-id="fe21d-150">Переместить выбранный эллипс.</span><span class="sxs-lookup"><span data-stu-id="fe21d-150">Move the selected ellipse.</span></span> |
| <span data-ttu-id="fe21d-151">Кнопка "влево"</span><span class="sxs-lookup"><span data-stu-id="fe21d-151">Left button up</span></span>   | <span data-ttu-id="fe21d-152">Прерывать Рисование эллипса.</span><span class="sxs-lookup"><span data-stu-id="fe21d-152">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="fe21d-153">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="fe21d-153">No action.</span></span>                                                                                                                                   | <span data-ttu-id="fe21d-154">Переключиться в режим выбора.</span><span class="sxs-lookup"><span data-stu-id="fe21d-154">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="fe21d-155">Следующий метод в `MainWindow` классе обрабатывает сообщения [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) .</span><span class="sxs-lookup"><span data-stu-id="fe21d-155">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if (mode == DrawMode)
    {
        POINT pt = { pixelX, pixelY };

        if (DragDetect(m_hwnd, pt))
        {
            SetCapture(m_hwnd);
        
            // Start a new ellipse.
            InsertEllipse(dipX, dipY);
        }
    }
    else
    {
        ClearSelection();

        if (HitTest(dipX, dipY))
        {
            SetCapture(m_hwnd);

            ptMouse = Selection()->ellipse.point;
            ptMouse.x -= dipX;
            ptMouse.y -= dipY;

            SetMode(DragMode);
        }
    }
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



<span data-ttu-id="fe21d-156">Координаты мыши передаются этому методу в пикселях, а затем преобразуются в DIP.</span><span class="sxs-lookup"><span data-stu-id="fe21d-156">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="fe21d-157">Важно не путать эти две единицы.</span><span class="sxs-lookup"><span data-stu-id="fe21d-157">It is important not to confuse these two units.</span></span> <span data-ttu-id="fe21d-158">Например, функция [**драгдетект**](/windows/desktop/api/winuser/nf-winuser-dragdetect) использует пиксели, но при рисовании и проверке попадания используются DIP.</span><span class="sxs-lookup"><span data-stu-id="fe21d-158">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="fe21d-159">Общее правило заключается в том, что функции, связанные с вводом на входе Windows или мыши, используют Пиксели, тогда как Direct2D и DirectWrite используют DIP.</span><span class="sxs-lookup"><span data-stu-id="fe21d-159">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="fe21d-160">Всегда Протестируйте программу с параметром высокого DPI и не забудьте пометить программу как поддерживающую DPI.</span><span class="sxs-lookup"><span data-stu-id="fe21d-160">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="fe21d-161">Дополнительные сведения см. в разделе [dpi и Device-Independent пикселей](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="fe21d-161">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="fe21d-162">Ниже приведен код, который обрабатывает сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="fe21d-162">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if ((flags & MK_LBUTTON) && Selection())
    { 
        if (mode == DrawMode)
        {
            // Resize the ellipse.
            const float width = (dipX - ptMouse.x) / 2;
            const float height = (dipY - ptMouse.y) / 2;
            const float x1 = ptMouse.x + width;
            const float y1 = ptMouse.y + height;

            Selection()->ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);
        }
        else if (mode == DragMode)
        {
            // Move the ellipse.
            Selection()->ellipse.point.x = dipX + ptMouse.x;
            Selection()->ellipse.point.y = dipY + ptMouse.y;
        }
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="fe21d-163">Логика изменения размера эллипса описана ранее в разделе [Пример: Рисование кругов](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="fe21d-163">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="fe21d-164">Также обратите внимание на вызов [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="fe21d-164">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="fe21d-165">Это гарантирует, что окно будет перерисовано.</span><span class="sxs-lookup"><span data-stu-id="fe21d-165">This makes sure that the window is repainted.</span></span> <span data-ttu-id="fe21d-166">Следующий код обрабатывает сообщения [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="fe21d-166">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    if ((mode == DrawMode) && Selection())
    {
        ClearSelection();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
    else if (mode == DragMode)
    {
        SetMode(SelectMode);
    }
    ReleaseCapture(); 
}
```



<span data-ttu-id="fe21d-167">Как видите, обработчики сообщений для ввода с помощью мыши имеют код ветвления в зависимости от текущего режима.</span><span class="sxs-lookup"><span data-stu-id="fe21d-167">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="fe21d-168">Это приемлемая структура для этой довольно простой программы.</span><span class="sxs-lookup"><span data-stu-id="fe21d-168">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="fe21d-169">Однако он может быстро стать слишком сложным при добавлении новых режимов.</span><span class="sxs-lookup"><span data-stu-id="fe21d-169">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="fe21d-170">Для более крупной программы архитектура "модель-представление-контроллер" (MVC) может быть лучшей конструкцией.</span><span class="sxs-lookup"><span data-stu-id="fe21d-170">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="fe21d-171">В архитектуре такого типа *контроллер*, который обрабатывает ввод пользователя, отделен от *модели*, которая управляет данными приложения.</span><span class="sxs-lookup"><span data-stu-id="fe21d-171">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="fe21d-172">Когда программа переключает режимы, курсор изменяется для предоставления пользователю обратной связи.</span><span class="sxs-lookup"><span data-stu-id="fe21d-172">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


```C++
void MainWindow::SetMode(Mode m)
{
    mode = m;

    // Update the cursor
    LPWSTR cursor;
    switch (mode)
    {
    case DrawMode:
        cursor = IDC_CROSS;
        break;

    case SelectMode:
        cursor = IDC_HAND;
        break;

    case DragMode:
        cursor = IDC_SIZEALL;
        break;
    }

    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
}
```



<span data-ttu-id="fe21d-173">И, наконец, не забудьте установить курсор при получении окном [**сообщения \_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) :</span><span class="sxs-lookup"><span data-stu-id="fe21d-173">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="fe21d-174">Сводка</span><span class="sxs-lookup"><span data-stu-id="fe21d-174">Summary</span></span>

<span data-ttu-id="fe21d-175">В этом модуле вы узнали, как управлять вводом с помощью мыши и клавиатуры. Определение сочетаний клавиш; и как обновить изображение курсора, чтобы отразить текущее состояние программы.</span><span class="sxs-lookup"><span data-stu-id="fe21d-175">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 