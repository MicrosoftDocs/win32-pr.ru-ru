---
Title: Расширенный пример входных данных пользователя. Описание: ввод пользователя: Расширенный пример MS. AssetID: A408E0EC-E0A7-4F18-BFCA-21D28007FACC MS. Topic: статья MS. Date: 05/31/2018
---

# <a name="user-input-extended-example"></a>Ввод данных пользователем: Расширенный пример

Объедините все, что мы узнали о вводе данных пользователем для создания простой программы рисования. Ниже приведен снимок экрана программы:

![снимок экрана программы рисования](images/input03.png)

Пользователь может рисовать многоточие в нескольких разных цветах, а также выбирать, перемещать или удалять эллипсы. Чтобы не усложнять пользовательский интерфейс, программа не позволяет пользователю выбрать цвета эллипса. Вместо этого программа автоматически выполняет циклический перебор заранее определенного списка цветов. Программа не поддерживает никакие фигуры, кроме эллипсов. Очевидно, что эта программа не будет Выиграйте никаких наград по графическому программному обеспечению. Тем не менее, это еще один полезный пример для изучения. Вы можете скачать полный исходный код из [простого примера рисования](simple-drawing-sample.md). В этом разделе рассматриваются некоторые особенности.

Многоточие представлено в программе структурой, содержащей эллипсы ([**D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) и Color ([**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)). Структура также определяет два метода: метод для рисования эллипса и метод для выполнения проверки нажатия.


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



Программа использует ту же Кисть сплошного цвета для рисования заливки и контура для каждого эллипса, изменяя цвет при необходимости. В Direct2D изменение цвета кисти с сплошным цветом является эффективной операцией. Таким образом, объект кисти в сплошном цвете поддерживает метод [**сетколор**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .

Многоточие хранится в контейнере **списка** STL:


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **Shared \_ ptr** — это класс интеллектуальных указателей, добавленный в C++ в TR1 и формализованный в C + + 0x. В Visual Studio 2010 добавлена поддержка **общих \_** компонентов r и других функций C + + 0x. Дополнительные сведения см. в разделе [изучение новых функций C++ и MFC в Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) в *журнале MSDN Magazine*. (Этот ресурс может быть недоступен в некоторых языках и странах.)

 

Программа имеет три режима:

-   Режим рисования. Пользователь может нарисовать новые эллипсы.
-   Режим выбора. Пользователь может выбрать эллипс.
-   Режим перетаскивания. Пользователь может перетащить выбранный эллипс.

Пользователь может переключаться между режимом рисования и режимом выделения с помощью тех же сочетаний клавиш, которые описаны в разделе [таблицы сочетаний клавиш](accelerator-tables.md). В режиме выбора программа переключается в режим перетаскивания, если пользователь щелкнет эллипс. Он переключается обратно в режим выбора, когда пользователь отпускает кнопку мыши. Текущий выделенный фрагмент хранится в виде итератора в списке эллипсов. Вспомогательный метод `MainWindow::Selection` возвращает указатель на выбранный эллипс или значение **nullptr** , если ничего не выбрано.


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



В следующей таблице перечислены эффекты ввода с помощью мыши в каждом из трех режимов.



| Ввод с помощью мыши      | Режим рисования                                          | Режим выбора                                                                                                                               | Режим перетаскивания                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Левая кнопка вниз | Установите захват мыши и начните рисовать новый эллипс. | Освобождение текущего выделения и выполнение проверки нажатия. Если достигнуто многоточие, захватите курсор, выберите эллипс и переключитесь в режим перетаскивания. | Никаких действий не требуется.                 |
| Перемещение мыши       | Если левая кнопка не работает, измените размер эллипса.    | Никаких действий не требуется.                                                                                                                                   | Переместить выбранный эллипс. |
| Кнопка "влево"   | Прерывать Рисование эллипса.                          | Никаких действий не требуется.                                                                                                                                   | Переключиться в режим выбора.  |



 

Следующий метод в `MainWindow` классе обрабатывает сообщения [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) .


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



Координаты мыши передаются этому методу в пикселях, а затем преобразуются в DIP. Важно не путать эти две единицы. Например, функция [**драгдетект**](/windows/desktop/api/winuser/nf-winuser-dragdetect) использует пиксели, но при рисовании и проверке попадания используются DIP. Общее правило заключается в том, что функции, связанные с вводом на входе Windows или мыши, используют Пиксели, тогда как Direct2D и DirectWrite используют DIP. Всегда Протестируйте программу с параметром высокого DPI и не забудьте пометить программу как поддерживающую DPI. Дополнительные сведения см. в разделе [dpi и Device-Independent пикселей](dpi-and-device-independent-pixels.md).

Ниже приведен код, который обрабатывает сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .


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



Логика изменения размера эллипса описана ранее в разделе [Пример: Рисование кругов](mouse-movement.md). Также обратите внимание на вызов [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Это гарантирует, что окно будет перерисовано. Следующий код обрабатывает сообщения [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) .


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



Как видите, обработчики сообщений для ввода с помощью мыши имеют код ветвления в зависимости от текущего режима. Это приемлемая структура для этой довольно простой программы. Однако он может быстро стать слишком сложным при добавлении новых режимов. Для более крупной программы архитектура "модель-представление-контроллер" (MVC) может быть лучшей конструкцией. В архитектуре такого типа *контроллер*, который обрабатывает ввод пользователя, отделен от *модели*, которая управляет данными приложения.

Когда программа переключает режимы, курсор изменяется для предоставления пользователю обратной связи.


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



И, наконец, не забудьте установить курсор при получении окном [**сообщения \_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) :


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a>Сводка

В этом модуле вы узнали, как управлять вводом с помощью мыши и клавиатуры. Определение сочетаний клавиш; и как обновить изображение курсора, чтобы отразить текущее состояние программы.

 

 
