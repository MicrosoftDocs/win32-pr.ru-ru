---
<span data-ttu-id="db860-101">Title: Расширенный пример входных данных пользователя. Описание: ввод пользователя: Расширенный пример MS. AssetID: A408E0EC-E0A7-4F18-BFCA-21D28007FACC MS. Topic: статья MS. Date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="db860-101">title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="user-input-extended-example"></a><span data-ttu-id="db860-102">Ввод данных пользователем: Расширенный пример</span><span class="sxs-lookup"><span data-stu-id="db860-102">User Input: Extended Example</span></span>

<span data-ttu-id="db860-103">Объедините все, что мы узнали о вводе данных пользователем для создания простой программы рисования.</span><span class="sxs-lookup"><span data-stu-id="db860-103">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="db860-104">Ниже приведен снимок экрана программы:</span><span class="sxs-lookup"><span data-stu-id="db860-104">Here is a screen shot of the program:</span></span>

![снимок экрана программы рисования](images/input03.png)

<span data-ttu-id="db860-106">Пользователь может рисовать многоточие в нескольких разных цветах, а также выбирать, перемещать или удалять эллипсы.</span><span class="sxs-lookup"><span data-stu-id="db860-106">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="db860-107">Чтобы не усложнять пользовательский интерфейс, программа не позволяет пользователю выбрать цвета эллипса.</span><span class="sxs-lookup"><span data-stu-id="db860-107">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="db860-108">Вместо этого программа автоматически выполняет циклический перебор заранее определенного списка цветов.</span><span class="sxs-lookup"><span data-stu-id="db860-108">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="db860-109">Программа не поддерживает никакие фигуры, кроме эллипсов.</span><span class="sxs-lookup"><span data-stu-id="db860-109">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="db860-110">Очевидно, что эта программа не будет Выиграйте никаких наград по графическому программному обеспечению.</span><span class="sxs-lookup"><span data-stu-id="db860-110">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="db860-111">Тем не менее, это еще один полезный пример для изучения.</span><span class="sxs-lookup"><span data-stu-id="db860-111">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="db860-112">Вы можете скачать полный исходный код из [простого примера рисования](simple-drawing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="db860-112">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="db860-113">В этом разделе рассматриваются некоторые особенности.</span><span class="sxs-lookup"><span data-stu-id="db860-113">This section will just cover some highlights.</span></span>

<span data-ttu-id="db860-114">Многоточие представлено в программе структурой, содержащей эллипсы ([**D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) и Color ([**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)).</span><span class="sxs-lookup"><span data-stu-id="db860-114">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="db860-115">Структура также определяет два метода: метод для рисования эллипса и метод для выполнения проверки нажатия.</span><span class="sxs-lookup"><span data-stu-id="db860-115">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


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



<span data-ttu-id="db860-116">Программа использует ту же Кисть сплошного цвета для рисования заливки и контура для каждого эллипса, изменяя цвет при необходимости.</span><span class="sxs-lookup"><span data-stu-id="db860-116">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="db860-117">В Direct2D изменение цвета кисти с сплошным цветом является эффективной операцией.</span><span class="sxs-lookup"><span data-stu-id="db860-117">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="db860-118">Таким образом, объект кисти в сплошном цвете поддерживает метод [**сетколор**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .</span><span class="sxs-lookup"><span data-stu-id="db860-118">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="db860-119">Многоточие хранится в контейнере **списка** STL:</span><span class="sxs-lookup"><span data-stu-id="db860-119">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="db860-120">**Shared \_ ptr** — это класс интеллектуальных указателей, добавленный в C++ в TR1 и формализованный в C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="db860-120">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="db860-121">В Visual Studio 2010 добавлена поддержка **общих \_** компонентов r и других функций C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="db860-121">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="db860-122">Дополнительные сведения см. в разделе [изучение новых функций C++ и MFC в Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) в *журнале MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="db860-122">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="db860-123">(Этот ресурс может быть недоступен в некоторых языках и странах.)</span><span class="sxs-lookup"><span data-stu-id="db860-123">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="db860-124">Программа имеет три режима:</span><span class="sxs-lookup"><span data-stu-id="db860-124">The program has three modes:</span></span>

-   <span data-ttu-id="db860-125">Режим рисования.</span><span class="sxs-lookup"><span data-stu-id="db860-125">Draw mode.</span></span> <span data-ttu-id="db860-126">Пользователь может нарисовать новые эллипсы.</span><span class="sxs-lookup"><span data-stu-id="db860-126">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="db860-127">Режим выбора.</span><span class="sxs-lookup"><span data-stu-id="db860-127">Selection mode.</span></span> <span data-ttu-id="db860-128">Пользователь может выбрать эллипс.</span><span class="sxs-lookup"><span data-stu-id="db860-128">The user can select an ellipse.</span></span>
-   <span data-ttu-id="db860-129">Режим перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="db860-129">Drag mode.</span></span> <span data-ttu-id="db860-130">Пользователь может перетащить выбранный эллипс.</span><span class="sxs-lookup"><span data-stu-id="db860-130">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="db860-131">Пользователь может переключаться между режимом рисования и режимом выделения с помощью тех же сочетаний клавиш, которые описаны в разделе [таблицы сочетаний клавиш](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="db860-131">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="db860-132">В режиме выбора программа переключается в режим перетаскивания, если пользователь щелкнет эллипс.</span><span class="sxs-lookup"><span data-stu-id="db860-132">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="db860-133">Он переключается обратно в режим выбора, когда пользователь отпускает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="db860-133">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="db860-134">Текущий выделенный фрагмент хранится в виде итератора в списке эллипсов.</span><span class="sxs-lookup"><span data-stu-id="db860-134">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="db860-135">Вспомогательный метод `MainWindow::Selection` возвращает указатель на выбранный эллипс или значение **nullptr** , если ничего не выбрано.</span><span class="sxs-lookup"><span data-stu-id="db860-135">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


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



<span data-ttu-id="db860-136">В следующей таблице перечислены эффекты ввода с помощью мыши в каждом из трех режимов.</span><span class="sxs-lookup"><span data-stu-id="db860-136">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="db860-137">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="db860-137">Mouse Input</span></span>      | <span data-ttu-id="db860-138">Режим рисования</span><span class="sxs-lookup"><span data-stu-id="db860-138">Draw Mode</span></span>                                          | <span data-ttu-id="db860-139">Режим выбора</span><span class="sxs-lookup"><span data-stu-id="db860-139">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="db860-140">Режим перетаскивания</span><span class="sxs-lookup"><span data-stu-id="db860-140">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="db860-141">Левая кнопка вниз</span><span class="sxs-lookup"><span data-stu-id="db860-141">Left button down</span></span> | <span data-ttu-id="db860-142">Установите захват мыши и начните рисовать новый эллипс.</span><span class="sxs-lookup"><span data-stu-id="db860-142">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="db860-143">Освобождение текущего выделения и выполнение проверки нажатия.</span><span class="sxs-lookup"><span data-stu-id="db860-143">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="db860-144">Если достигнуто многоточие, захватите курсор, выберите эллипс и переключитесь в режим перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="db860-144">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="db860-145">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="db860-145">No action.</span></span>                 |
| <span data-ttu-id="db860-146">Перемещение мыши</span><span class="sxs-lookup"><span data-stu-id="db860-146">Mouse move</span></span>       | <span data-ttu-id="db860-147">Если левая кнопка не работает, измените размер эллипса.</span><span class="sxs-lookup"><span data-stu-id="db860-147">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="db860-148">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="db860-148">No action.</span></span>                                                                                                                                   | <span data-ttu-id="db860-149">Переместить выбранный эллипс.</span><span class="sxs-lookup"><span data-stu-id="db860-149">Move the selected ellipse.</span></span> |
| <span data-ttu-id="db860-150">Кнопка "влево"</span><span class="sxs-lookup"><span data-stu-id="db860-150">Left button up</span></span>   | <span data-ttu-id="db860-151">Прерывать Рисование эллипса.</span><span class="sxs-lookup"><span data-stu-id="db860-151">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="db860-152">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="db860-152">No action.</span></span>                                                                                                                                   | <span data-ttu-id="db860-153">Переключиться в режим выбора.</span><span class="sxs-lookup"><span data-stu-id="db860-153">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="db860-154">Следующий метод в `MainWindow` классе обрабатывает сообщения [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) .</span><span class="sxs-lookup"><span data-stu-id="db860-154">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


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



<span data-ttu-id="db860-155">Координаты мыши передаются этому методу в пикселях, а затем преобразуются в DIP.</span><span class="sxs-lookup"><span data-stu-id="db860-155">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="db860-156">Важно не путать эти две единицы.</span><span class="sxs-lookup"><span data-stu-id="db860-156">It is important not to confuse these two units.</span></span> <span data-ttu-id="db860-157">Например, функция [**драгдетект**](/windows/desktop/api/winuser/nf-winuser-dragdetect) использует пиксели, но при рисовании и проверке попадания используются DIP.</span><span class="sxs-lookup"><span data-stu-id="db860-157">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="db860-158">Общее правило заключается в том, что функции, связанные с вводом на входе Windows или мыши, используют Пиксели, тогда как Direct2D и DirectWrite используют DIP.</span><span class="sxs-lookup"><span data-stu-id="db860-158">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="db860-159">Всегда Протестируйте программу с параметром высокого DPI и не забудьте пометить программу как поддерживающую DPI.</span><span class="sxs-lookup"><span data-stu-id="db860-159">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="db860-160">Дополнительные сведения см. в разделе [dpi и Device-Independent пикселей](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="db860-160">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="db860-161">Ниже приведен код, который обрабатывает сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="db860-161">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


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



<span data-ttu-id="db860-162">Логика изменения размера эллипса описана ранее в разделе [Пример: Рисование кругов](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="db860-162">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="db860-163">Также обратите внимание на вызов [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="db860-163">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="db860-164">Это гарантирует, что окно будет перерисовано.</span><span class="sxs-lookup"><span data-stu-id="db860-164">This makes sure that the window is repainted.</span></span> <span data-ttu-id="db860-165">Следующий код обрабатывает сообщения [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="db860-165">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


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



<span data-ttu-id="db860-166">Как видите, обработчики сообщений для ввода с помощью мыши имеют код ветвления в зависимости от текущего режима.</span><span class="sxs-lookup"><span data-stu-id="db860-166">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="db860-167">Это приемлемая структура для этой довольно простой программы.</span><span class="sxs-lookup"><span data-stu-id="db860-167">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="db860-168">Однако он может быстро стать слишком сложным при добавлении новых режимов.</span><span class="sxs-lookup"><span data-stu-id="db860-168">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="db860-169">Для более крупной программы архитектура "модель-представление-контроллер" (MVC) может быть лучшей конструкцией.</span><span class="sxs-lookup"><span data-stu-id="db860-169">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="db860-170">В архитектуре такого типа *контроллер*, который обрабатывает ввод пользователя, отделен от *модели*, которая управляет данными приложения.</span><span class="sxs-lookup"><span data-stu-id="db860-170">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="db860-171">Когда программа переключает режимы, курсор изменяется для предоставления пользователю обратной связи.</span><span class="sxs-lookup"><span data-stu-id="db860-171">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


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



<span data-ttu-id="db860-172">И, наконец, не забудьте установить курсор при получении окном [**сообщения \_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) :</span><span class="sxs-lookup"><span data-stu-id="db860-172">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="db860-173">Сводка</span><span class="sxs-lookup"><span data-stu-id="db860-173">Summary</span></span>

<span data-ttu-id="db860-174">В этом модуле вы узнали, как управлять вводом с помощью мыши и клавиатуры. Определение сочетаний клавиш; и как обновить изображение курсора, чтобы отразить текущее состояние программы.</span><span class="sxs-lookup"><span data-stu-id="db860-174">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 
