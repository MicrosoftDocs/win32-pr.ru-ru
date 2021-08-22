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
ms.openlocfilehash: 8c930931df8ce401fbed8cc9af16db3cb52de08ebe9cf539109b426497318d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472650"
---
# <a name="using-carets"></a>Использование крышки

В этом разделе приведены примеры кода для следующих задач:

-   [Создание и отображение курсора](#creating-and-displaying-a-caret)
-   [Скрытие курсора](#hiding-a-caret)
-   [Уничтожение курсора](#destroying-a-caret)
-   [Настройка времени мерцания](#adjusting-the-blink-time)
-   [Обработка ввода с клавиатуры](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a>Создание и отображение курсора

При получении фокуса клавиатуры окно должно создать и отобразить курсор. Используйте функцию [**креатекарет**](/windows/desktop/api/Winuser/nf-winuser-createcaret) для создания курсора в заданном окне. Затем можно вызвать [**сеткаретпос**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) , чтобы установить текущую позиции курсора и [**шовкарет**](/windows/desktop/api/Winuser/nf-winuser-showcaret) , чтобы сделать курсор видимым.

Система отправляет сообщение [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) окну, получающему фокус клавиатуры, поэтому приложение должно создать и отобразить курсор во время обработки этого сообщения.


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



Чтобы создать курсор на основе растрового изображения, необходимо указать маркер растрового изображения при использовании [**креатекарет**](/windows/desktop/api/Winuser/nf-winuser-createcaret). Вы можете использовать графическое приложение для создания растрового изображения и компилятора ресурсов, чтобы добавить точечный рисунок в ресурсы приложения. Приложение может использовать функцию [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) для загрузки маркера точечного рисунка. Например, можно заменить строку **креатекарет** в предыдущем примере на следующие строки, чтобы создать курсор точечного рисунка.


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



Кроме того, можно использовать функцию [**креатебитмап**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) или [**креатедибитмап**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) для получения маркера точечного рисунка курсора. Дополнительные сведения о растровых изображениях см. в разделе [точечные рисунки](/windows/desktop/gdi/bitmaps).

Если в приложении задан маркер точечного рисунка, [**креатекарет**](/windows/desktop/api/Winuser/nf-winuser-createcaret) игнорирует параметры ширины и высоты. Точечный рисунок определяет размер курсора.

## <a name="hiding-a-caret"></a>Скрытие курсора

Всякий раз, когда приложение перерисовывает экран при обработке сообщения, отличного от [**WM \_ Paint**](/windows/desktop/gdi/wm-paint), он должен сделать курсор невидимым с помощью функции [**хидекарет**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) . Когда приложение завершит рисование, снова отобразите курсор с помощью функции [**шовкарет**](/windows/desktop/api/Winuser/nf-winuser-showcaret) . Если приложение обрабатывает сообщение **WM \_ Paint** , нет необходимости скрывать и повторно отображать курсор, поскольку эта функция делает это автоматически.

В следующем образце кода показано, как приложение скрывает курсор, вырисуя символ на экране и обрабатывая сообщение [**WM \_ char**](/windows/desktop/inputdev/wm-char) .


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



Если приложение вызывает функцию [**хидекарет**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) несколько раз без вызова [**шовкарет**](/windows/desktop/api/Winuser/nf-winuser-showcaret), курсор не будет отображаться до тех пор, пока приложение не вызовет **шовкарет** одинаковое число раз.

## <a name="destroying-a-caret"></a>Уничтожение курсора

Когда окно теряет фокус клавиатуры, система отправляет сообщение [**WM \_ киллфокус**](/windows/desktop/inputdev/wm-killfocus) в окно. Приложение должно уничтожить курсор при обработке этого сообщения с помощью функции [**дестройкарет**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) . В следующем коде показано, как уничтожить курсор в окне, которое больше не имеет фокуса клавиатуры.


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a>Настройка времени мерцания

в 16-разрядных Windowsах приложение на основе Windows может вызвать функцию [**жеткаретблинктиме**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) для сохранения текущего времени мигания, а затем вызвать функцию [**сеткаретблинктиме**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) для настройки времени мигания во время обработки сообщения [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) . Приложение Восстанавливает сохраненное время мигания для использования других приложений, вызывая **сеткаретблинктиме** во время обработки сообщения [**WM \_ киллфокус**](/windows/desktop/inputdev/wm-killfocus) . Однако этот метод не работает в многопоточных средах. В частности, деактивация одного приложения не синхронизирована с активацией другого приложения, чтобы при зависании одного приложения можно было активировать другое.

Приложения должны учитывать время мерцания, выбранное пользователем. Функция [**сеткаретблинктиме**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) должна вызываться только приложением, которое позволяет пользователю задать время мерцания.

## <a name="processing-keyboard-input"></a>Обработка ввода с клавиатуры

В следующем примере показано, как использовать курсор в простом текстовом редакторе. В этом примере положение курсора обновляется по мере того, как пользователь вводит печатные символы и использует различные ключи для перемещения по клиентской области.


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



 

 