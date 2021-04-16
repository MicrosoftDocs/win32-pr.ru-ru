---
title: Использование ввода с клавиатуры
description: В этом разделе рассматриваются задачи, связанные с вводом с клавиатуры.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- Ввод данных пользователем, ввод с клавиатуры
- запись вводимых пользователем данных, ввод с клавиатуры
- ввод с клавиатуры
- сообщения о нажатии клавиш
- Символьные сообщения
- крышки, ввод с клавиатуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76b3f90a626506430b91e7539069c6ecdf634c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710281"
---
# <a name="using-keyboard-input"></a>Использование ввода с клавиатуры

Окно получает ввод с клавиатуры в виде сообщений о нажатиях клавиш и символьных сообщений. В цикле сообщений, присоединенном к окну, должен быть указан код для преобразования сообщений о нажатии клавиш в соответствующие символьные сообщения. Если окно отображает ввод с клавиатуры в клиентской области, он должен создать и отобразить курсор, указывающий позицию, в которой будет введен следующий символ. В следующих разделах описывается код, связанный с получением, обработкой и отображением ввода с клавиатуры.

-   [Обработка сообщений с нажатием клавиши](#processing-keystroke-messages)
-   [Преобразование символьных сообщений](#translating-character-messages)
-   [Обработка сообщений с символами](#processing-character-messages)
-   [Использование курсора](#using-the-caret)
-   [Отображение ввода с клавиатуры](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a>Обработка сообщений с нажатием клавиши

Оконная процедура окна с фокусом клавиатуры получает сообщения о нажатии клавиш, когда пользователь вводит клавиатуру. Сообщения о нажатии клавиши: [**WM \_ KeyDown**](wm-keydown.md), [**WM \_ KEYUP**](wm-keyup.md), [**WM \_ сискэйдовн**](wm-syskeydown.md)и [**WM \_ сискэйуп**](wm-syskeyup.md). Типичная процедура окна игнорирует все сообщения с нажатием клавиши, за исключением **WM \_ KeyDown**. Система отправляет сообщение **WM \_ KeyDown** , когда пользователь нажимает клавишу.

Когда процедура окна получает сообщение [**WM \_ KeyDown**](wm-keydown.md) , она должна изучить код виртуального ключа, сопровождающего сообщение, чтобы определить, как обрабатывать нажатие клавиши. Код виртуального ключа находится в параметре *wParam* сообщения. Как правило, приложение обрабатывает только нажатия клавиш, созданные несимвольными ключами, включая функциональные клавиши, клавиши перемещения курсора и специальные сочетания клавиш, такие как INS, DEL, HOME и END.

В следующем примере показана структура оконной процедуры, используемая обычным приложением для получения и обработки сообщений о нажатии клавиш.


```
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT: 
                    
                    // Process the LEFT ARROW key. 
                     
                    break; 
 
                case VK_RIGHT: 
                    
                    // Process the RIGHT ARROW key. 
                     
                    break; 
 
                case VK_UP: 
                    
                    // Process the UP ARROW key. 
                     
                    break; 
 
                case VK_DOWN: 
                    
                    // Process the DOWN ARROW key. 
                     
                    break; 
 
                case VK_HOME: 
                    
                    // Process the HOME key. 
                     
                    break; 
 
                case VK_END: 
                    
                    // Process the END key. 
                     
                    break; 
 
                case VK_INSERT: 
                    
                    // Process the INS key. 
                     
                    break; 
 
                case VK_DELETE: 
                    
                    // Process the DEL key. 
                     
                    break; 
 
                case VK_F2: 
                    
                    // Process the F2 key. 
                    
                    break; 
 
                
                // Process other non-character keystrokes. 
                 
                default: 
                    break; 
            } 
```



## <a name="translating-character-messages"></a>Преобразование символьных сообщений

Любой поток, принимающий символьные данные от пользователя, должен включать функцию [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) в свой цикл обработки сообщений. Эта функция проверяет код виртуального ключа сообщения о нажатии клавиши и, если код соответствует символу, помещает в очередь сообщений символьное сообщение. Символьное сообщение удаляется и отправляется при следующей итерации цикла обработки сообщений. параметр *wParam* сообщения содержит код символа.

Как правило, цикл обработки сообщений потока должен использовать функцию [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) для преобразования каждого сообщения, а не только для сообщений с виртуальным ключом. Хотя **TranslateMessage** не влияет на другие типы сообщений, это гарантирует, что ввод с клавиатуры будет преобразован правильно. В следующем примере показано, как включить функцию **TranslateMessage** в типичный цикл обработки сообщений потока.


```
MSG msg;
BOOL bRet;

while (( bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0) 
{
    if (bRet == -1);
    {
        // handle the error and possibly exit
    }
    else
    { 
        if (TranslateAccelerator(hwndMain, haccl, &msg) == 0) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



## <a name="processing-character-messages"></a>Обработка сообщений с символами

Оконная процедура получает символьное сообщение, когда функция [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) преобразует код виртуальной клавиши, соответствующий символьной клавише. Символьные сообщения имеют [**\_ тип WM char**](wm-char.md), [**WM \_ Деадчар**](wm-deadchar.md), [**WM \_ сисчар**](/windows/desktop/menurc/wm-syschar)и [**WM \_ сисдеадчар**](wm-sysdeadchar.md). Типичная процедура окна игнорирует все символьные сообщения, кроме **WM \_ char**. Функция **TranslateMessage** создает сообщение **WM \_ char** , когда пользователь нажимает любой из следующих клавиш:

-   Любой ключ символа
-   BACKSPACE
-   Ввод (возврат каретки)
-   ESC
-   SHIFT + ВВОД (перевод строки)
-   TAB

Когда процедура окна получает сообщение [**WM \_ char**](wm-char.md) , она должна проверить код символа, сопровождающего сообщение, чтобы определить способ обработки символа. Код символа находится в параметре *wParam* сообщения.

В следующем примере показана структура оконной процедуры, используемая обычным приложением для получения и обработки символьных сообщений.


```
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08: 
                    
                    // Process a backspace. 
                     
                    break; 
 
                case 0x0A: 
                    
                    // Process a linefeed. 
                     
                    break; 
 
                case 0x1B: 
                    
                    // Process an escape. 
                    
                    break; 
 
                case 0x09: 
                    
                    // Process a tab. 
                     
                    break; 
 
                case 0x0D: 
                    
                    // Process a carriage return. 
                     
                    break; 
 
                default: 
                    
                    // Process displayable characters. 
                     
                    break; 
            } 
```



## <a name="using-the-caret"></a>Использование курсора

Окно, получающее ввод с клавиатуры, обычно отображает символы, которые пользователь вводит в клиентской области окна. Окно должно использовать курсор, чтобы указать позицию в клиентской области, где будет отображаться следующий символ. Окно также должно создавать и отображать курсор при получении фокуса клавиатуры, а также скрывать и уничтожать курсор при потере фокуса. Окно может выполнять эти операции при обработке сообщений [**WM \_ SETFOCUS**](wm-setfocus.md) и [**WM \_ киллфокус**](wm-killfocus.md) . Дополнительные сведения о параметре крышки см. в разделе символы [крышки](/windows/desktop/menurc/carets).

## <a name="displaying-keyboard-input"></a>Отображение ввода с клавиатуры

В примере в этом разделе показано, как приложение может принимать символы с клавиатуры, отображать их в клиентской области окна и обновлять позиции курсора с каждым введенным символом. Здесь также показано, как переместить курсор в ответ на стрелку влево, стрелку вправо, домой и завершить нажатия клавиш и показать, как выделить выделенный текст в ответ на сочетание клавиш SHIFT + стрелка вправо.

При обработке сообщения, [**\_ созданного**](/windows/desktop/winmsg/wm-create) с помощью WM, процедура Window, показанная в примере, выделяет буфер размером 64 КБ для хранения ввода с клавиатуры. Он также извлекает метрики текущего загруженного шрифта, сохраняя высоту и среднюю ширину символов в шрифте. Высота и ширина используются при обработке сообщения [**\_ размера WM**](/windows/desktop/winmsg/wm-size) для вычисления длины строки и максимального количества строк в зависимости от размера клиентской области.

Процедура окна создает и отображает курсор при обработке сообщения [**WM \_ SETFOCUS**](wm-setfocus.md) . Он скрывает и удаляет курсор при обработке сообщения [**WM \_ киллфокус**](wm-killfocus.md) .

При обработке сообщения [**WM \_ char**](wm-char.md) процедура Window отображает символы, сохраняет их во входном буфере и обновляет позиции курсора. Процедура окна также преобразует символы табуляции в четыре последовательных символа пробела. Символы Backspace, перевода строки и экранирования создают звуковой сигнал, но не обрабатываются иным образом.

При обработке сообщения [**WM \_ KeyDown**](wm-keydown.md) в процедуре Window выполняются перемещения влево, вправо, конечных и домашних курсоров. При обработке действия клавиши со стрелкой вправо процедура окна проверяет состояние клавиши SHIFT и, если она не работает, выбирает символ справа от курсора при перемещении курсора.

Обратите внимание, что следующий код написан таким образом, чтобы его можно было скомпилировать как в Юникоде, так и в формате ANSI. Если исходный код определяет Юникод, строки обрабатываются как символы Юникода. в противном случае они обрабатываются как символы ANSI.


```
#define BUFSIZE 65535 
#define SHIFTED 0x8000 
 
LONG APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                   // handle to device context 
    TEXTMETRIC tm;             // structure for text metrics 
    static DWORD dwCharX;      // average width of characters 
    static DWORD dwCharY;      // height of characters 
    static DWORD dwClientX;    // width of client area 
    static DWORD dwClientY;    // height of client area 
    static DWORD dwLineLen;    // line length 
    static DWORD dwLines;      // text lines in client area 
    static int nCaretPosX = 0; // horizontal position of caret 
    static int nCaretPosY = 0; // vertical position of caret 
    static int nCharWidth = 0; // width of a character 
    static int cch = 0;        // characters in buffer 
    static int nCurChar = 0;   // index of current character 
    static PTCHAR pchInputBuf; // input buffer 
    int i, j;                  // loop counters 
    int cCR = 0;               // count of carriage returns 
    int nCRIndex = 0;          // index of last carriage return 
    int nVirtKey;              // virtual-key code 
    TCHAR szBuf[128];          // temporary buffer 
    TCHAR ch;                  // current character 
    PAINTSTRUCT ps;            // required by BeginPaint 
    RECT rc;                   // output rectangle for DrawText 
    SIZE sz;                   // string dimensions 
    COLORREF crPrevText;       // previous text color 
    COLORREF crPrevBk;         // previous background color
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Get the metrics of the current font. 
 
            hdc = GetDC(hwndMain); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwndMain, hdc); 
 
            // Save the average character width and height. 
 
            dwCharX = tm.tmAveCharWidth; 
            dwCharY = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPTSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
            return 0; 
 
        case WM_SIZE: 
 
            // Save the new width and height of the client area. 
 
            dwClientX = LOWORD(lParam); 
            dwClientY = HIWORD(lParam); 
 
            // Calculate the maximum width of a line and the 
            // maximum number of lines in the client area. 
            
            dwLineLen = dwClientX - dwCharX; 
            dwLines = dwClientY / dwCharY; 
            break; 
 
 
        case WM_SETFOCUS: 
 
            // Create, position, and display the caret when the 
            // window receives the keyboard focus. 
 
            CreateCaret(hwndMain, (HBITMAP) 1, 0, dwCharY); 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            ShowCaret(hwndMain); 
            break; 
 
        case WM_KILLFOCUS: 
 
            // Hide and destroy the caret when the window loses the 
            // keyboard focus. 
 
            HideCaret(hwndMain); 
            DestroyCaret(); 
            break; 
 
        case WM_CHAR:
        // check if current location is close enough to the
        // end of the buffer that a buffer overflow may
        // occur. If so, add null and display contents. 
    if (cch > BUFSIZE-5)
    {
        pchInputBuf[cch] = 0x00;
        SendMessage(hwndMain, WM_PAINT, 0, 0);
    } 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return and position the 
                    // caret at the beginning of the new line.

                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCaretPosY += 1; 
                    break; 
 
                default:    // displayable character 
 
                    ch = (TCHAR) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width and output 
                    // the character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, nCaretPosY * dwCharY, 
                        &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer.
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the position exceeds the maximum, 
                    // insert a carriage return and move the caret 
                    // to the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwLineLen) 
                    { 
                        nCaretPosX = 0;
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCaretPosY; 
                    } 
                    nCurChar = cch; 
                    ShowCaret(hwndMain); 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT:   // LEFT ARROW 
 
                    // The caret can move only to the beginning of 
                    // the current line. 
 
                    if (nCaretPosX > 0) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the left of 
                        // the caret, calculate the character's 
                        // width, then subtract the width from the 
                        // current horizontal position of the caret 
                        // to obtain the new position. 
 
                        ch = pchInputBuf[--nCurChar]; 
                        hdc = GetDC(hwndMain); 
                        GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                        ReleaseDC(hwndMain, hdc); 
                        nCaretPosX = max(nCaretPosX - nCharWidth, 
                            0); 
                        ShowCaret(hwndMain); 
                    } 
                    break; 
 
                case VK_RIGHT:  // RIGHT ARROW 
 
                    // Caret moves to the right or, when a carriage 
                    // return is encountered, to the beginning of 
                    // the next line. 
 
                    if (nCurChar < cch) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the right of 
                        // the caret. If it's a carriage return, 
                        // position the caret at the beginning of 
                        // the next line. 
 
                        ch = pchInputBuf[nCurChar]; 
                        if (ch == 0x0D) 
                        { 
                            nCaretPosX = 0; 
                            nCaretPosY++; 
                        } 
 
                        // If the character isn't a carriage 
                        // return, check to see whether the SHIFT 
                        // key is down. If it is, invert the text 
                        // colors and output the character. 
 
                        else 
                        { 
                            hdc = GetDC(hwndMain); 
                            nVirtKey = GetKeyState(VK_SHIFT); 
                            if (nVirtKey & SHIFTED) 
                            { 
                                crPrevText = SetTextColor(hdc, 
                                    RGB(255, 255, 255)); 
                                crPrevBk = SetBkColor(hdc, 
                                    RGB(0,0,0)); 
                                TextOut(hdc, nCaretPosX, 
                                    nCaretPosY * dwCharY, 
                                    &ch, 1); 
                                SetTextColor(hdc, crPrevText); 
                                SetBkColor(hdc, crPrevBk); 
                            } 
 
                            // Get the width of the character and 
                            // calculate the new horizontal 
                            // position of the caret. 
 
                            GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                            ReleaseDC(hwndMain, hdc); 
                            nCaretPosX = nCaretPosX + nCharWidth; 
                        } 
                        nCurChar++; 
                        ShowCaret(hwndMain); 
                        break; 
                    } 
                    break; 
 
                case VK_UP:     // UP ARROW 
                case VK_DOWN:   // DOWN ARROW 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case VK_HOME:   // HOME 
 
                    // Set the caret's position to the upper left 
                    // corner of the client area. 
 
                    nCaretPosX = nCaretPosY = 0; 
                    nCurChar = 0; 
                    break; 
 
                case VK_END:    // END  
 
                    // Move the caret to the end of the text. 
 
                    for (i=0; i < cch; i++) 
                    { 
                        // Count the carriage returns and save the 
                        // index of the last one. 
 
                        if (pchInputBuf[i] == 0x0D) 
                        { 
                            cCR++; 
                            nCRIndex = i + 1; 
                        } 
                    } 
                    nCaretPosY = cCR; 
 
                    // Copy all text between the last carriage 
                    // return and the end of the keyboard input 
                    // buffer to a temporary buffer. 
 
                    for (i = nCRIndex, j = 0; i < cch; i++, j++) 
                        szBuf[j] = pchInputBuf[i]; 
                    szBuf[j] = TEXT('\0'); 
 
                    // Retrieve the text extent and use it 
                    // to set the horizontal position of the 
                    // caret. 
 
                    hdc = GetDC(hwndMain);
                    hResult = StringCchLength(szBuf, 128, pcch);
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    GetTextExtentPoint32(hdc, szBuf, *pcch, 
                        &sz); 
                    nCaretPosX = sz.cx; 
                    ReleaseDC(hwndMain, hdc); 
                    nCurChar = cch; 
                    break; 
 
                default: 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_PAINT: 
            if (cch == 0)       // nothing in input buffer 
                break; 
 
            hdc = BeginPaint(hwndMain, &ps); 
            HideCaret(hwndMain); 
 
            // Set the clipping rectangle, and then draw the text 
            // into it. 
 
            SetRect(&rc, 0, 0, dwLineLen, dwClientY); 
            DrawText(hdc, pchInputBuf, -1, &rc, DT_LEFT); 
 
            ShowCaret(hwndMain); 
            EndPaint(hwndMain, &ps); 
            break; 
        
        // Process other messages. 
        
        case WM_DESTROY: 
            PostQuitMessage(0); 
 
            // Free the input buffer. 
 
            GlobalFree((HGLOBAL) pchInputBuf); 
            UnregisterHotKey(hwndMain, 0xAAAA); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



 

 