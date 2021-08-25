---
title: Использование ввода с помощью мыши
description: В этом разделе рассматриваются задачи, связанные с вводом с помощью мыши.
ms.assetid: b96d0046-a507-4733-bcf3-fcf757beec7f
keywords:
- Ввод данных пользователем, ввод с помощью мыши
- захват вводимых пользователем данных, ввод с помощью мыши
- ввод мыши
- курсоры, ввод с помощью мыши
- указатель мыши
- Дважды щелкните Обработка сообщений
- колесо мыши
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38105da1fbbe3bee1be9ca280f1f5573dbb41ba4b7b6aa2013d9c600b8ad00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829974"
---
# <a name="using-mouse-input"></a>Использование ввода с помощью мыши

В этом разделе рассматриваются задачи, связанные с вводом с помощью мыши.

-   [Отслеживание курсора мыши](#tracking-the-mouse-cursor)
-   [Рисование линий с помощью мыши](#drawing-lines-with-the-mouse)
-   [Обработка сообщения двойного щелчка](#processing-a-double-click-message)
-   [Выбор строки текста](#selecting-a-line-of-text)
-   [Использование колесика мыши в документе с внедренными объектами](#using-a-mouse-wheel-in-a-document-with-embedded-objects)
-   [Получение числа линий прокрутки колесика мыши](#retrieving-the-number-of-mouse-wheel-scroll-lines)

## <a name="tracking-the-mouse-cursor"></a>Отслеживание курсора мыши

Приложения часто выполняют задачи, связанные с отслеживанием положения курсора мыши. Большинство графических приложений, например, отслеживание положения курсора мыши во время операций рисования, позволяя пользователю рисовать в клиентской области окна путем перетаскивания мыши. Приложения обработки текста также отслеживанием курсора, позволяя пользователю выбрать слово или блок текста, щелкнув и перетащив мышью.

Отслеживание курсора обычно включает обработку сообщений [**WM \_ лбуттондовн**](wm-lbuttondown.md), [**WM \_ MOUSEMOVE**](wm-mousemove.md)и [**WM \_ лбуттонуп**](wm-lbuttonup.md) . Окно определяет время начала отслеживания курсора, проверяя позицию курсора, указанную в параметре *lParam* сообщения **WM \_ лбуттондовн** . Например, приложение для обработки текста начнет отслеживать курсор только в том случае, если сообщение **WM \_ лбуттондовн** произошло, когда курсор находился в строке текста, но не в том случае, если он находится за концом документа.

Окно отслеживает позицию курсора путем обработки потока сообщений [**WM \_ MOUSEMOVE**](wm-mousemove.md) , помещенных в окно при перемещении мыши. Обработка сообщения **WM \_ MOUSEMOVE** обычно включает в себя повторяющиеся операции рисования или рисования в клиентской области. Например, приложение рисования может многократно перерисовывать линию при перемещении мыши. Окно использует сообщение [**WM \_ лбуттонуп**](wm-lbuttonup.md) в качестве сигнала для прекращения отслеживания курсора.

Кроме того, приложение может вызвать функцию [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) , чтобы система отправляла другие сообщения, полезные для отслеживания курсора. Система отправляет сообщение [**WM \_ маусеховер**](wm-mousehover.md) при наведении курсора на клиентскую область в течение определенного периода времени. Он отправляет сообщение [**WM \_ MOUSELEAVE**](wm-mouseleave.md) , когда курсор покидает клиентскую область. Сообщения [**WM \_ Нкмаусеховер**](wm-ncmousehover.md) и [**WM \_ нкмауселеаве**](wm-ncmouseleave.md) представляют собой соответствующие сообщения для неклиентских областей.

## <a name="drawing-lines-with-the-mouse"></a>Рисование линий с помощью мыши

В примере в этом разделе показано, как отвести курсор мыши. Он содержит части процедуры окна, позволяющие пользователю рисовать линии в клиентской области окна путем перетаскивания мыши.

Когда процедура окна получает сообщение [**WM \_ лбуттондовн**](wm-lbuttondown.md) , она фиксирует мышь и сохраняет координаты курсора, используя координаты в качестве начальной точки линии. Он также использует функцию [**клипкурсор**](/windows/desktop/api/winuser/nf-winuser-clipcursor) для ограничения курсора на клиентскую область во время операции рисования линии.

Во время первого сообщения [**WM \_ MOUSEMOVE**](wm-mousemove.md) процедура окна рисует строку от начальной точки до текущей позиции курсора. При последующих сообщениях **WM \_ MOUSEMOVE** процедура Window удаляет предыдущую строку, рисуя ее с инвертированным цветом пера. Затем она рисует новую строку от начальной точки до новой позиции курсора.

Сообщение [**WM \_ лбуттонуп**](wm-lbuttonup.md) сигнализирует об окончании операции рисования. Процедура окна освобождает захват мыши и освобождает мышь от клиентской области.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                       // handle to device context 
    RECT rcClient;                 // client area rectangle 
    POINT ptClientUL;              // client upper left corner 
    POINT ptClientLR;              // client lower right corner 
    static POINTS ptsBegin;        // beginning point 
    static POINTS ptsEnd;          // new endpoint 
    static POINTS ptsPrevEnd;      // previous endpoint 
    static BOOL fPrevLine = FALSE; // previous line flag 
 
    switch (uMsg) 
    { 
       case WM_LBUTTONDOWN: 
 
            // Capture mouse input. 
 
            SetCapture(hwndMain); 
 
            // Retrieve the screen coordinates of the client area, 
            // and convert them into client coordinates. 
 
            GetClientRect(hwndMain, &rcClient); 
            ptClientUL.x = rcClient.left; 
            ptClientUL.y = rcClient.top; 
 
            // Add one to the right and bottom sides, because the 
            // coordinates retrieved by GetClientRect do not 
            // include the far left and lowermost pixels. 
 
            ptClientLR.x = rcClient.right + 1; 
            ptClientLR.y = rcClient.bottom + 1; 
            ClientToScreen(hwndMain, &ptClientUL); 
            ClientToScreen(hwndMain, &ptClientLR); 
 
            // Copy the client coordinates of the client area 
            // to the rcClient structure. Confine the mouse cursor 
            // to the client area by passing the rcClient structure 
            // to the ClipCursor function. 
 
            SetRect(&rcClient, ptClientUL.x, ptClientUL.y, 
                ptClientLR.x, ptClientLR.y); 
            ClipCursor(&rcClient); 
 
            // Convert the cursor coordinates into a POINTS 
            // structure, which defines the beginning point of the 
            // line drawn during a WM_MOUSEMOVE message. 
 
            ptsBegin = MAKEPOINTS(lParam); 
            return 0; 
 
        case WM_MOUSEMOVE: 
 
            // When moving the mouse, the user must hold down 
            // the left mouse button to draw lines. 
 
            if (wParam & MK_LBUTTON) 
            { 
 
                // Retrieve a device context (DC) for the client area. 
 
                hdc = GetDC(hwndMain); 
 
                // The following function ensures that pixels of 
                // the previously drawn line are set to white and 
                // those of the new line are set to black. 
 
                SetROP2(hdc, R2_NOTXORPEN); 
 
                // If a line was drawn during an earlier WM_MOUSEMOVE 
                // message, draw over it. This erases the line by 
                // setting the color of its pixels to white. 
 
                if (fPrevLine) 
                { 
                    MoveToEx(hdc, ptsBegin.x, ptsBegin.y, 
                        (LPPOINT) NULL); 
                    LineTo(hdc, ptsPrevEnd.x, ptsPrevEnd.y); 
                } 
 
                // Convert the current cursor coordinates to a 
                // POINTS structure, and then draw a new line. 
 
                ptsEnd = MAKEPOINTS(lParam); 
                MoveToEx(hdc, ptsBegin.x, ptsBegin.y, (LPPOINT) NULL); 
                LineTo(hdc, ptsEnd.x, ptsEnd.y); 
 
                // Set the previous line flag, save the ending 
                // point of the new line, and then release the DC. 
 
                fPrevLine = TRUE; 
                ptsPrevEnd = ptsEnd; 
                ReleaseDC(hwndMain, hdc); 
            } 
            break; 
 
        case WM_LBUTTONUP: 
 
            // The user has finished drawing the line. Reset the 
            // previous line flag, release the mouse cursor, and 
            // release the mouse capture. 
 
            fPrevLine = FALSE; 
            ClipCursor(NULL); 
            ReleaseCapture(); 
            return 0; 
 
        case WM_DESTROY: 
            PostQuitMessage(0); 
            break; 
 
        // Process other messages. 
        
```



## <a name="processing-a-double-click-message"></a>Обработка сообщения двойного щелчка

Чтобы получить сообщения двойного щелчка, окно должно принадлежать классу окна, имеющему стиль класса [**CS \_ дблклкс**](/windows/desktop/winmsg/about-window-classes) . Этот стиль задается при регистрации класса окна, как показано в следующем примере.


```
BOOL InitApplication(HINSTANCE hInstance) 
{ 
    WNDCLASS wc; 
 
    wc.style = CS_DBLCLKS | CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hInstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_IBEAM); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName = "MainMenu"; 
    wc.lpszClassName = "MainWClass"; 
 
    return RegisterClass(&wc); 
} 
```



Для сообщения двойного щелчка всегда предшествует сообщение с кнопкой. По этой причине приложения обычно используют сообщение двойного щелчка для расширения задачи, которая была начата при нажатии кнопки.

## <a name="selecting-a-line-of-text"></a>Выбор строки текста

Пример в этом разделе взят из простого приложения для обработки текста. Он включает код, позволяющий пользователю задать расположение курсора, щелкнув в любом месте строки текста и выбрав (выделять) строку текста, дважды щелкнув в любом месте строки.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                     // handle to device context 
    TEXTMETRIC tm;               // font size data 
    int i, j;                    // loop counters 
    int cCR = 0;                 // count of carriage returns 
    char ch;                     // character from input buffer 
    static int nBegLine;         // beginning of selected line 
    static int nCurrentLine = 0; // currently selected line 
    static int nLastLine = 0;    // last text line 
    static int nCaretPosX = 0;   // x-coordinate of caret 
    static int cch = 0;          // number of characters entered 
    static int nCharWidth = 0;   // exact width of a character 
    static char szHilite[128];   // text string to highlight 
    static DWORD dwCharX;        // average width of characters 
    static DWORD dwLineHeight;   // line height 
    static POINTS ptsCursor;     // coordinates of mouse cursor 
    static COLORREF crPrevText;  // previous text color 
    static COLORREF crPrevBk;    // previous background color 
    static PTCHAR pchInputBuf;   // pointer to input buffer 
    static BOOL fTextSelected = FALSE; // text-selection flag 
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
            dwLineHeight = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep( (UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return, and position the 
                    // caret at the beginning of the new line. 
 
                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCurrentLine += 1; 
                    break; 
 
                default:    / displayable character 
 
                    ch = (char) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width, and display the 
                    // character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, 
                        nCurrentLine * dwLineHeight, &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer. 
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the new position exceeds the maximum, 
                    // insert a carriage return and reposition the 
                    // caret at the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwMaxCharX) 
                    { 
                        nCaretPosX = 0; 
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCurrentLine; 
                    } 
 
                    ShowCaret(hwndMain); 
 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            nLastLine = max(nLastLine, nCurrentLine); 
            break; 
 
        // Process other messages. 
 
        case WM_LBUTTONDOWN: 
 
            // If a line of text is currently highlighted, redraw 
            // the text to remove the highlighting. 
 
            if (fTextSelected) 
            { 
                hdc = GetDC(hwndMain); 
                SetTextColor(hdc, crPrevText); 
                SetBkColor(hdc, crPrevBk);
                hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
                if (FAILED(hResult))
                {
                // TODO: write error handler
                } 
                TextOut(hdc, 0, nCurrentLine * dwLineHeight, 
                    szHilite, *pcch); 
                ReleaseDC(hwndMain, hdc); 
                ShowCaret(hwndMain); 
                fTextSelected = FALSE; 
            } 
 
            // Save the current mouse-cursor coordinates. 
 
            ptsCursor = MAKEPOINTS(lParam); 
 
            // Determine which line the cursor is on, and save 
            // the line number. Do not allow line numbers greater 
            // than the number of the last line of text. The 
            // line number is later multiplied by the average height 
            // of the current font. The result is used to set the 
            // y-coordinate of the caret. 
 
            nCurrentLine = min((int)(ptsCursor.y / dwLineHeight), 
                nLastLine); 
 
            // Parse the text input buffer to find the first 
            // character in the selected line of text. Each 
            // line ends with a carriage return, so it is possible 
            // to count the carriage returns to find the selected 
            // line. 
 
            cCR = 0; 
            nBegLine = 0; 
            if (nCurrentLine != 0) 
            { 
                for (i = 0; (i < cch) && 
                        (cCR < nCurrentLine); i++) 
                { 
                    if (pchInputBuf[i] == 0x0D) 
                        ++cCR; 
                } 
                nBegLine = i; 
            } 
 
            // Starting at the beginning of the selected line, 
            // measure  the width of each character, summing the 
            // width with each character measured. Stop when the 
            // sum is greater than the x-coordinate of the cursor. 
            // The sum is used to set the x-coordinate of the caret. 
 
            hdc = GetDC(hwndMain); 
            nCaretPosX = 0; 
            for (i = nBegLine; 
                (pchInputBuf[i] != 0x0D) && (i < cch); i++) 
            { 
                ch = pchInputBuf[i]; 
                GetCharWidth32(hdc, (int) ch, (int) ch, &nCharWidth); 
                if ((nCaretPosX + nCharWidth) > ptsCursor.x) break; 
                else nCaretPosX += nCharWidth; 
            } 
            ReleaseDC(hwndMain, hdc); 
 
            // Set the caret to the user-selected position. 
 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            break; 
 
        case WM_LBUTTONDBLCLK: 
 
            // Copy the selected line of text to a buffer. 
 
            for (i = nBegLine, j = 0; (pchInputBuf[i] != 0x0D) && 
                    (i < cch); i++) 
            {
                szHilite[j++] = pchInputBuf[i]; 
            }
            szHilite[j] = '\0'; 
 
            // Hide the caret, invert the background and foreground 
            // colors, and then redraw the selected line. 
 
            HideCaret(hwndMain); 
            hdc = GetDC(hwndMain); 
            crPrevText = SetTextColor(hdc, RGB(255, 255, 255)); 
            crPrevBk = SetBkColor(hdc, RGB(0, 0, 0));
            hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 0, nCurrentLine * dwLineHeight, szHilite, *pcch); 
            SetTextColor(hdc, crPrevText); 
            SetBkColor(hdc, crPrevBk); 
            ReleaseDC(hwndMain, hdc); 
 
            fTextSelected = TRUE; 
            break; 

            // Process other messages. 

        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="using-a-mouse-wheel-in-a-document-with-embedded-objects"></a>Использование колесика мыши в документе с внедренными объектами

в этом примере предполагается, что Microsoft Word документ с различными внедренными объектами:

-   электронная таблица Microsoft Excel
-   Встроенный элемент управления "список", который прокручивается в ответ на колесо
-   Элемент управления "встроенное текстовое поле", не отвечающий на колесо

Сообщение [МШ \_ маусевхил](about-mouse-input.md) всегда отправляется в главное окно в Microsoft Word. Это справедливо даже в том случае, если внедренная электронная таблица активна. В следующей таблице объясняется, как \_ обрабатываются сообщения МШ маусевхил в соответствии с фокусом.



| Фокус включен                | Обработка выполняется следующим образом.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Документ Word              | Word прокручивает окно документа.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| электронная таблица Embedded Excel | Word отправляет сообщение в Excel. Необходимо решить, должно ли встроенное приложение реагировать на сообщение или нет.                                                                                                                                                                                                                                                                                                                                                            |
| Внедренный элемент управления           | Приложение должно отправить сообщение во внедренный элемент управления, который имеет фокус, и проверить код возврата, чтобы узнать, обрабатывался ли элемент управления. Если элемент управления не обрабатывает его, приложение должно прокручивать окно документа. Например, если пользователь щелкнул поле со списком, а затем выполнил вращение колесика, этот элемент управления прокручивается в ответ на поворот колесика. Если пользователь щелкнул текстовое поле, а затем поворачивает колесико, то весь документ будет прокручиваться. |



 

В следующем примере показано, как приложение может управлять двумя сообщениями колесика.


```
/************************************************
* this code deals with MSH_MOUSEWHEEL
*************************************************/
#include "zmouse.h"

//
// Mouse Wheel rotation stuff, only define if we are
// on a version of the OS that does not support
// WM_MOUSEWHEEL messages.
//
#ifndef WM_MOUSEWHEEL
#define WM_MOUSEWHEEL WM_MOUSELAST+1 
    // Message ID for IntelliMouse wheel
#endif

UINT uMSH_MOUSEWHEEL = 0;   // Value returned from
                            // RegisterWindowMessage()

/**************************************************

INT WINAPI WinMain(
         HINSTANCE hInst, 
         HINSTANCE hPrevInst, 
         LPSTR lpCmdLine, 
         INT nCmdShow)
{
    MSG msg;
    BOOL bRet;

    if (!InitInstance(hInst, nCmdShow))
        return FALSE;

    //
    // The new IntelliMouse uses a Registered message to transmit
    // wheel rotation info. So register for it!
 
    uMSH_MOUSEWHEEL =
     RegisterWindowMessage(MSH_MOUSEWHEEL); 
    if ( !uMSH_MOUSEWHEEL )
    {
        MessageBox(NULL,"
                   RegisterWindowMessag Failed!",
                   "Error",MB_OK);
        return msg.wParam;
    }
    
    while (( bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            if (!TranslateAccelerator(ghwndApp,
                                      ghaccelTable,
                                      &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }

    return msg.wParam;
}

/************************************************
* this code deals with WM_MOUSEWHEEL
*************************************************/
LONG APIENTRY MainWndProc(
    HWND hwnd,
    UINT msg,
    WPARAM wParam,
    LPARAM lParam)
{
    static int nZoom = 0;
    

    switch (msg)
    {
        //
        // Handle Mouse Wheel messages generated
        // by the operating systems that have built-in
        // support for the WM_MOUSEWHEEL message.
        //

        case WM_MOUSEWHEEL:
            ((short) HIWORD(wParam)< 0) ? nZoom-- : nZoom++;

            //
            // Do other wheel stuff...
            //

            break;

        default:
            //
            // uMSH_MOUSEWHEEL is a message registered by
            // the mswheel dll on versions of Windows that
            // do not support the new message in the OS.

            if( msg == uMSH_MOUSEWHEEL )
            {
               ((int)wParam < 0) ? nZoom-- : nZoom++;

                //
                // Do other wheel stuff...
                //
                break;
            }

            return DefWindowProc(hwnd,
                                 msg,
                                 wParam,
                                 lParam);
    }

    return 0L;
}
```



## <a name="retrieving-the-number-of-mouse-wheel-scroll-lines"></a>Получение числа линий прокрутки колесика мыши

Следующий код позволяет приложению получить количество строк прокрутки с помощью функции [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .


```
#ifndef SPI_GETWHEELSCROLLLINES
#define SPI_GETWHEELSCROLLLINES   104
#endif

#include "zmouse.h"

/*********************************************************
* FUNCTION: GetNumScrollLines
* Purpose : An OS independent method to retrieve the 
*           number of wheel scroll lines
* Params  : none
* Returns : UINT:  Number of scroll lines where WHEEL_PAGESCROLL 
*           indicates to scroll a page at a time.
*********************************************************/
UINT GetNumScrollLines(void)
{
   HWND hdlMsWheel;
   UINT ucNumLines=3;  // 3 is the default
   OSVERSIONINFO osversion;
   UINT uiMsh_MsgScrollLines;
   

   memset(&osversion, 0, sizeof(osversion));
   osversion.dwOSVersionInfoSize =sizeof(osversion);
   GetVersionEx(&osversion);

   if ((osversion.dwPlatformId == VER_PLATFORM_WIN32_WINDOWS) ||
       ( (osversion.dwPlatformId == VER_PLATFORM_WIN32_NT) && 
         (osversion.dwMajorVersion < 4) )   )
   {
        hdlMsWheel = FindWindow(MSH_WHEELMODULE_CLASS, 
                                MSH_WHEELMODULE_TITLE);
        if (hdlMsWheel)
        {
           uiMsh_MsgScrollLines = RegisterWindowMessage
                                     (MSH_SCROLL_LINES);
           if (uiMsh_MsgScrollLines)
                ucNumLines = (int)SendMessage(hdlMsWheel,
                                    uiMsh_MsgScrollLines, 
                                                       0, 
                                                       0);
        }
   }
   else if ( (osversion.dwPlatformId ==
                         VER_PLATFORM_WIN32_NT) &&
             (osversion.dwMajorVersion >= 4) )
   {
      SystemParametersInfo(SPI_GETWHEELSCROLLLINES,
                                          0,
                                    &ucNumLines, 0);
   }
   return(ucNumLines);
}
```



 

 