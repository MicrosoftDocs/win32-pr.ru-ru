---
title: Использование крышки
description: В этом разделе приводятся примеры кода, демонстрирующие выполнение задач, связанных с «крышки».
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- ресурсы, символы крышки
- символы крышки, создание
- крышки, отображение
- крышки, удаление
- крышки, скрытие
- крышки, мигающие моменты
- Мигающие линии
- Мигающие блоки
- Мигающие растровые изображения
- Создание «крышки»
- Отображение за«крышки»
- Скрытие крышки
- уничтожение крышки
- мерцание времени
- Ввод данных пользователем, ввод с клавиатуры
- запись вводимых пользователем данных, ввод с клавиатуры
- ввод с клавиатуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6450a3169588b3072d1fee271f4890a7cdeafd2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069896"
---
# <a name="using-carets"></a><span data-ttu-id="7840e-120">Использование крышки</span><span class="sxs-lookup"><span data-stu-id="7840e-120">Using Carets</span></span>

<span data-ttu-id="7840e-121">В этом разделе приведены примеры кода для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="7840e-121">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="7840e-122">Создание и отображение курсора</span><span class="sxs-lookup"><span data-stu-id="7840e-122">Creating and Displaying a Caret</span></span>](#creating-and-displaying-a-caret)
-   [<span data-ttu-id="7840e-123">Скрытие курсора</span><span class="sxs-lookup"><span data-stu-id="7840e-123">Hiding a Caret</span></span>](#hiding-a-caret)
-   [<span data-ttu-id="7840e-124">Уничтожение курсора</span><span class="sxs-lookup"><span data-stu-id="7840e-124">Destroying a Caret</span></span>](#destroying-a-caret)
-   [<span data-ttu-id="7840e-125">Настройка времени мерцания</span><span class="sxs-lookup"><span data-stu-id="7840e-125">Adjusting the Blink Time</span></span>](#adjusting-the-blink-time)
-   [<span data-ttu-id="7840e-126">Обработка ввода с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="7840e-126">Processing Keyboard Input</span></span>](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a><span data-ttu-id="7840e-127">Создание и отображение курсора</span><span class="sxs-lookup"><span data-stu-id="7840e-127">Creating and Displaying a Caret</span></span>

<span data-ttu-id="7840e-128">При получении фокуса клавиатуры окно должно создать и отобразить курсор.</span><span class="sxs-lookup"><span data-stu-id="7840e-128">Upon receiving the keyboard focus, the window should create and display the caret.</span></span> <span data-ttu-id="7840e-129">Используйте функцию [**креатекарет**](/windows/desktop/api/Winuser/nf-winuser-createcaret) для создания курсора в заданном окне.</span><span class="sxs-lookup"><span data-stu-id="7840e-129">Use the [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) function to create a caret in the given window.</span></span> <span data-ttu-id="7840e-130">Затем можно вызвать [**сеткаретпос**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) , чтобы установить текущую позиции курсора и [**шовкарет**](/windows/desktop/api/Winuser/nf-winuser-showcaret) , чтобы сделать курсор видимым.</span><span class="sxs-lookup"><span data-stu-id="7840e-130">You can then call [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) to set the current position of the caret and [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) to make the caret visible.</span></span>

<span data-ttu-id="7840e-131">Система отправляет сообщение [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) окну, получающему фокус клавиатуры, поэтому приложение должно создать и отобразить курсор во время обработки этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="7840e-131">The system sends the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message to the window receiving keyboard focus; therefore, an application should create and display the caret while processing this message.</span></span>


```
HWND hwnd,       // window handle 
int x;           // horizontal coordinate of cursor 
int y;           // vertical coordinate of cursor 
int nWidth;      // width of cursor 
int nHeight;     // height of cursor 
char *lpszChar;  // pointer to character 
 
    case WM_SETFOCUS: 
 
    // Create a solid black caret. 
        CreateCaret(hwnd, (HBITMAP) NULL, nWidth, nHeight); 
 
    // Adjust the caret position, in client coordinates. 
        SetCaretPos(x, y); 
 
    // Display the caret. 
        ShowCaret(hwnd); 
 
        break; 
```



<span data-ttu-id="7840e-132">Чтобы создать курсор на основе растрового изображения, необходимо указать маркер растрового изображения при использовании [**креатекарет**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span><span class="sxs-lookup"><span data-stu-id="7840e-132">To create a caret based on a bitmap, you must specify a bitmap handle when using [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span></span> <span data-ttu-id="7840e-133">Вы можете использовать графическое приложение для создания растрового изображения и компилятора ресурсов, чтобы добавить точечный рисунок в ресурсы приложения.</span><span class="sxs-lookup"><span data-stu-id="7840e-133">You can use a graphics application to create the bitmap and a resource compiler to add the bitmap to your application's resources.</span></span> <span data-ttu-id="7840e-134">Приложение может использовать функцию [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) для загрузки маркера точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="7840e-134">Your application can then use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap handle.</span></span> <span data-ttu-id="7840e-135">Например, можно заменить строку **креатекарет** в предыдущем примере на следующие строки, чтобы создать курсор точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="7840e-135">For example, you could replace the **CreateCaret** line in the preceding example with the following lines to create a bitmap caret.</span></span>


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



<span data-ttu-id="7840e-136">Кроме того, можно использовать функцию [**креатебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) или [**креатедибитмап**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) для получения маркера точечного рисунка курсора.</span><span class="sxs-lookup"><span data-stu-id="7840e-136">Alternatively, you can use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) or [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) function to retrieve the handle of the caret bitmap.</span></span> <span data-ttu-id="7840e-137">Дополнительные сведения о растровых изображениях см. в разделе [точечные рисунки](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="7840e-137">For more information about bitmaps, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

<span data-ttu-id="7840e-138">Если в приложении задан маркер точечного рисунка, [**креатекарет**](/windows/desktop/api/Winuser/nf-winuser-createcaret) игнорирует параметры ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="7840e-138">If your application specifies a bitmap handle, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignores the width and height parameters.</span></span> <span data-ttu-id="7840e-139">Точечный рисунок определяет размер курсора.</span><span class="sxs-lookup"><span data-stu-id="7840e-139">The bitmap defines the size of the caret.</span></span>

## <a name="hiding-a-caret"></a><span data-ttu-id="7840e-140">Скрытие курсора</span><span class="sxs-lookup"><span data-stu-id="7840e-140">Hiding a Caret</span></span>

<span data-ttu-id="7840e-141">Всякий раз, когда приложение перерисовывает экран при обработке сообщения, отличного от [**WM \_ Paint**](/windows/desktop/gdi/wm-paint), он должен сделать курсор невидимым с помощью функции [**хидекарет**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) .</span><span class="sxs-lookup"><span data-stu-id="7840e-141">Whenever your application redraws a screen while processing a message other than [**WM\_PAINT**](/windows/desktop/gdi/wm-paint), it must make the caret invisible by using the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function.</span></span> <span data-ttu-id="7840e-142">Когда приложение завершит рисование, снова отобразите курсор с помощью функции [**шовкарет**](/windows/desktop/api/Winuser/nf-winuser-showcaret) .</span><span class="sxs-lookup"><span data-stu-id="7840e-142">When your application is finished drawing, redisplay the caret by using the [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) function.</span></span> <span data-ttu-id="7840e-143">Если приложение обрабатывает сообщение **WM \_ Paint** , нет необходимости скрывать и повторно отображать курсор, поскольку эта функция делает это автоматически.</span><span class="sxs-lookup"><span data-stu-id="7840e-143">If your application processes the **WM\_PAINT** message, it is not necessary to hide and redisplay the caret, because this function does this automatically.</span></span>

<span data-ttu-id="7840e-144">В следующем образце кода показано, как приложение скрывает курсор, вырисуя символ на экране и обрабатывая сообщение [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="7840e-144">The following code sample shows how to have your application hide the caret while drawing a character on the screen and while processing the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


```
HWND hwnd,   // window handle 
HDC hdc;     // device context 
 
    case WM_CHAR: 
        switch (wParam) 
        { 
            case 0x08: 
             
             // Process a backspace. 
             
                break; 
 
            case 0x09: 
             
             // Process a tab.  
             
                break; 
 
            case 0x0D: 
             
             // Process a carriage return. 
             
                break; 
 
            case 0x1B: 
             
             // Process an escape. 
             
                break; 
 
            case 0x0A: 
             
             // Process a linefeed. 
             
                break; 
 
            default: 
                // Hide the caret. 
                HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                hdc = GetDC(hwnd); 
                SelectObject(hdc, 
                    GetStockObject(SYSTEM_FIXED_FONT)); 
 
                TextOut(hdc, x, y, lpszChar, 1); 
 
                ReleaseDC(hwnd, hdc); 
 
                // Display the caret. 
 
                ShowCaret(hwnd); 
 
        } 
```



<span data-ttu-id="7840e-145">Если приложение вызывает функцию [**хидекарет**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) несколько раз без вызова [**шовкарет**](/windows/desktop/api/Winuser/nf-winuser-showcaret), курсор не будет отображаться до тех пор, пока приложение не вызовет **шовкарет** одинаковое число раз.</span><span class="sxs-lookup"><span data-stu-id="7840e-145">If your application calls the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function several times without calling [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), the caret will not be displayed until the application also calls **ShowCaret** the same number of times.</span></span>

## <a name="destroying-a-caret"></a><span data-ttu-id="7840e-146">Уничтожение курсора</span><span class="sxs-lookup"><span data-stu-id="7840e-146">Destroying a Caret</span></span>

<span data-ttu-id="7840e-147">Когда окно теряет фокус клавиатуры, система отправляет сообщение [**WM \_ киллфокус**](/windows/desktop/inputdev/wm-killfocus) в окно.</span><span class="sxs-lookup"><span data-stu-id="7840e-147">When a window loses the keyboard focus, the system sends the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message to the window.</span></span> <span data-ttu-id="7840e-148">Приложение должно уничтожить курсор при обработке этого сообщения с помощью функции [**дестройкарет**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) .</span><span class="sxs-lookup"><span data-stu-id="7840e-148">Your application should destroy the caret while processing this message by using the [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) function.</span></span> <span data-ttu-id="7840e-149">В следующем коде показано, как уничтожить курсор в окне, которое больше не имеет фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="7840e-149">The following code shows how to destroy a caret in a window that no longer has the keyboard focus.</span></span>


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a><span data-ttu-id="7840e-150">Настройка времени мерцания</span><span class="sxs-lookup"><span data-stu-id="7840e-150">Adjusting the Blink Time</span></span>

<span data-ttu-id="7840e-151">В 16-разрядных Windows приложение Windows может вызвать функцию [**жеткаретблинктиме**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) для сохранения текущего времени мигания, а затем вызвать функцию [**сеткаретблинктиме**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) для настройки времени мигания во время обработки сообщения [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="7840e-151">In 16-bit Windows, a Windows-based application could call the [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) function to save the current blink time, then call the [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function to adjust the blink time during its processing of the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="7840e-152">Приложение Восстанавливает сохраненное время мигания для использования других приложений, вызывая **сеткаретблинктиме** во время обработки сообщения [**WM \_ киллфокус**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="7840e-152">The application would restore the saved blink time for the use of other applications by calling **SetCaretBlinkTime** during its processing of the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="7840e-153">Однако этот метод не работает в многопоточных средах.</span><span class="sxs-lookup"><span data-stu-id="7840e-153">However, this technique does not work in multithreaded environments.</span></span> <span data-ttu-id="7840e-154">В частности, деактивация одного приложения не синхронизирована с активацией другого приложения, чтобы при зависании одного приложения можно было активировать другое.</span><span class="sxs-lookup"><span data-stu-id="7840e-154">Specifically, the deactivation of one application is not synchronized with the activation of another application, so that if one application hangs, another application can still be activated.</span></span>

<span data-ttu-id="7840e-155">Приложения должны учитывать время мерцания, выбранное пользователем.</span><span class="sxs-lookup"><span data-stu-id="7840e-155">Applications should respect the blink time chosen by the user.</span></span> <span data-ttu-id="7840e-156">Функция [**сеткаретблинктиме**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) должна вызываться только приложением, которое позволяет пользователю задать время мерцания.</span><span class="sxs-lookup"><span data-stu-id="7840e-156">The [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function should only be called by an application that allows the user to set the blink time.</span></span>

## <a name="processing-keyboard-input"></a><span data-ttu-id="7840e-157">Обработка ввода с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="7840e-157">Processing Keyboard Input</span></span>

<span data-ttu-id="7840e-158">В следующем примере показано, как использовать курсор в простом текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="7840e-158">The following example demonstrates how to use a caret in a simple text editor.</span></span> <span data-ttu-id="7840e-159">В этом примере положение курсора обновляется по мере того, как пользователь вводит печатные символы и использует различные ключи для перемещения по клиентской области.</span><span class="sxs-lookup"><span data-stu-id="7840e-159">The example updates the caret position as the user types printable characters and uses various keys to move through the client area.</span></span>


```
#define TEXTMATRIX(x, y) *(pTextMatrix + (y * nWindowCharsX) + x) 
// Global variables.
HINSTANCE hinst;                  // current instance 
HBITMAP hCaret;                   // caret bitmap 
HDC hdc;                          // device context  
PAINTSTRUCT ps;                   // client area paint info 
static char *pTextMatrix = NULL;  // points to text matrix 
static int  nCharX,               // width of char. in logical units 
            nCharY,               // height of char. in logical units 
            nWindowX,             // width of client area 
            nWindowY,             // height of client area 
            nWindowCharsX,        // width of client area 
            nWindowCharsY,        // height of client area 
            nCaretPosX,           // x-position of caret 
            nCaretPosY;           // y-position of caret 
static UINT uOldBlink;            // previous blink rate 
int x, y;                         // coordinates for text matrix 
TEXTMETRIC tm;                    // font information 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,            // window handle 
    UINT message,         // type of message 
    UINT wParam,          // additional information 
    LONG lParam)          // additional information 
{ 
 
    switch (message) 
    { 
        case WM_CREATE: 
        // Select a fixed-width system font, and get its text metrics.
 
            hdc = GetDC(hwnd); 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwnd, hdc); 
 
        // Save the avg. width and height of characters. 
 
            nCharX = tm.tmAveCharWidth; 
            nCharY = tm.tmHeight; 
 
            return 0; 
 
        case WM_SIZE: 
        // Determine the width of the client area, in pixels 
        // and in number of characters. 
 
            nWindowX = LOWORD(lParam); 
            nWindowCharsX = max(1, nWindowX/nCharX); 
 
            // Determine the height of the client area, in 
            // pixels and in number of characters. 
 
            nWindowY = HIWORD(lParam); 
            nWindowCharsY = max(1, nWindowY/nCharY); 
 
            // Clear the buffer that holds the text input. 
 
            if (pTextMatrix != NULL) 
                free(pTextMatrix); 
 
            // If there is enough memory, allocate space for the 
            // text input buffer. 
 
            pTextMatrix = malloc(nWindowCharsX * nWindowCharsY); 
 
            if (pTextMatrix == NULL) 
                ErrorHandler("Not enough memory."); 
            else 
                for (y = 0; y < nWindowCharsY; y++) 
                    for (x = 0; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, y) = ' '; 
 
            // Move the caret to the origin. 
 
            SetCaretPos(0, 0); 
 
            return 0; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_HOME:       // Home 
                    nCaretPosX = 0; 
                    break; 
 
                case VK_END:        // End 
                    nCaretPosX = nWindowCharsX - 1; 
                    break; 
 
                case VK_PRIOR:      // Page Up 
                    nCaretPosY = 0; 
                    break; 
 
                case VK_NEXT:       // Page Down 
                    nCaretPosY = nWindowCharsY -1; 
                    break; 
 
                case VK_LEFT:       // Left arrow 
                    nCaretPosX = max(nCaretPosX - 1, 0); 
                    break; 
 
                case VK_RIGHT:      // Right arrow 
                    nCaretPosX = min(nCaretPosX + 1, 
                        nWindowCharsX - 1); 
                    break; 
 
                case VK_UP:         // Up arrow 
                    nCaretPosY = max(nCaretPosY - 1, 0); 
                    break; 
 
                case VK_DOWN:       // Down arrow 
                    nCaretPosY = min(nCaretPosY + 1, 
                        nWindowCharsY - 1); 
                    break; 
 
                case VK_DELETE:     // Delete 
 
                // Move all the characters that followed the 
                // deleted character (on the same line) one 
                // space back (to the left) in the matrix. 
 
                    for (x = nCaretPosX; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, nCaretPosY) = 
                            TEXTMATRIX(x + 1, nCaretPosY); 
 
                    // Replace the last character on the 
                    // line with a space. 
 
                    TEXTMATRIX(nWindowCharsX - 1, 
                        nCaretPosY) = ' '; 
 
                    // The application will draw outside the 
                    // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                    // Redraw the line, adjusted for the 
                    // deleted character. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 
                        nWindowCharsX - nCaretPosX); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // virtual-key processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:          // Backspace 
                // Move the caret back one space, and then 
                // process this like the DEL key. 
 
                    if (nCaretPosX > 0) 
                    { 
                        nCaretPosX--; 
                        SendMessage(hwnd, WM_KEYDOWN, 
                            VK_DELETE, 1L); 
                    } 
                    break; 
 
                case 0x09:          // Tab 
                // Tab stops exist every four spaces, so add 
                // spaces until the user hits the next tab. 
 
                    do 
                    { 
                        SendMessage(hwnd, WM_CHAR, ' ', 1L); 
                    } while (nCaretPosX % 4 != 0); 
                    break; 
 
                case 0x0D:          // Carriage return 
                // Go to the beginning of the next line. 
                // The bottom line wraps around to the top. 
 
                    nCaretPosX = 0; 
 
                    if (++nCaretPosY == nWindowCharsY) 
                        nCaretPosY = 0; 
                    break; 
 
                case 0x1B:        // Escape 
                case 0x0A:        // Linefeed 
                    MessageBeep((UINT) -1); 
                    break; 
 
                default: 
                // Add the character to the text buffer. 
 
                    TEXTMATRIX(nCaretPosX, nCaretPosY) = 
                        (char) wParam; 
 
                // The application will draw outside the 
                // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 1); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    // Prepare to wrap around if you reached the 
                    // end of the line. 
 
                    if (++nCaretPosX == nWindowCharsX) 
                    { 
                        nCaretPosX = 0; 
                        if (++nCaretPosY == nWindowCharsY) 
                            nCaretPosY = 0; 
                    } 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // character processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_PAINT: 
        // Draw all the characters in the buffer, line by line. 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
 
            for (y = 0; y < nWindowCharsY; y++) 
                TextOut(hdc, 0, y * nCharY, &TEXTMATRIX(0, y), 
                    nWindowCharsX); 
 
            EndPaint(hwnd, &ps); 
 
        case WM_SETFOCUS: 
        // The window has the input focus. Load the 
        // application-defined caret resource. 
 
            hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
            // Create the caret. 
 
            CreateCaret(hwnd, hCaret, 0, 0); 
 
            // Adjust the caret position. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            // Display the caret. 
 
            ShowCaret(hwnd); 
 
            break; 
 
        case WM_KILLFOCUS: 
        // The window is losing the input focus, 
        // so destroy the caret. 
 
            DestroyCaret(); 
 
            break; 
 
        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
    } 
 
    return NULL; 
} 
```



 

 