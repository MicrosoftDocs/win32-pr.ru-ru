---
description: В этом разделе показано, как создавать и удалять таймеры, а также как использовать таймер для перехвата входных данных мыши через определенные промежутки времени.
ms.assetid: eee54078-759f-4fd4-9cf4-10a8bde888b7
title: Использование таймеров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7922be60012ae81ce1971afe6f2300f54689f7a6cc8d7f088df2fb126e834ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028312"
---
# <a name="using-timers"></a>Использование таймеров

В этом разделе показано, как создавать и удалять таймеры, а также как использовать таймер для перехвата входных данных мыши через определенные промежутки времени.

В этом разделе содержатся следующие подразделы.

-   [Создание таймера](#creating-a-timer)
-   [Уничтожение таймера](#destroying-a-timer)
-   [Использование функций таймера для перехвата ввода с помощью мыши](#using-timer-functions-to-trap-mouse-input)
-   [Связанные темы](#related-topics)

## <a name="creating-a-timer"></a>Создание таймера

В следующем примере используется функция [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) для создания двух таймеров. Первый таймер задается каждые 10 секунд, второй — каждые 5 минут.


```
// Set two timers. 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER1,            // timer identifier 
    10000,                 // 10-second interval 
    (TIMERPROC) NULL);     // no timer callback 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER2,            // timer identifier 
    300000,                // five-minute interval 
    (TIMERPROC) NULL);     // no timer callback 
```



Для обработки сообщений [**\_ таймера WM**](wm-timer.md) , созданных этими таймерами, добавьте в оконную процедуру для параметра *HWND* оператор Case **\_ таймера WM** .


```
case WM_TIMER: 
 
    switch (wParam) 
    { 
        case IDT_TIMER1: 
            // process the 10-second timer 
 
             return 0; 
 
        case IDT_TIMER2: 
            // process the five-minute timer 

            return 0; 
    } 
```



Приложение также может создать таймер, сообщения [**\_ таймера WM**](wm-timer.md) которого обрабатываются не процедурой главного окна, а функцией обратного вызова, определяемой приложением, как показано в следующем примере кода, который создает таймер и использует функцию обратного вызова **митимерпрок** для обработки сообщений **\_ таймера WM** таймера.


```
// Set the timer. 
 
SetTimer(hwnd,                // handle to main window 
    IDT_TIMER3,               // timer identifier 
    5000,                     // 5-second interval 
    (TIMERPROC) MyTimerProc); // timer callback
```



Соглашение о вызовах для **митимерпрок** должно быть основано на функции обратного вызова [*тимерпрок*](/windows/win32/api/winuser/nc-winuser-timerproc) .

Если приложение создает таймер без указания маркера окна, приложение должно отслеживать очередь сообщений на наличие сообщений [**\_ таймера WM**](wm-timer.md) и отправлять их в соответствующее окно.


```
HWND hwndTimer;   // handle to window for timer messages 
MSG msg;          // message structure 
 
    while (GetMessage(&msg, // message structure 
            NULL,           // handle to window to receive the message 
               0,           // lowest message to examine 
               0))          // highest message to examine 
    { 
 
        // Post WM_TIMER messages to the hwndTimer procedure. 
 
        if (msg.message == WM_TIMER) 
        { 
            msg.hwnd = hwndTimer; 
        } 
 
        TranslateMessage(&msg); // translates virtual-key codes 
        DispatchMessage(&msg);  // dispatches message to window 
    } 
```



## <a name="destroying-a-timer"></a>Уничтожение таймера

Приложения должны использовать функцию [**киллтимер**](/windows/win32/api/winuser/nf-winuser-killtimer) для уничтожения таймеров, которые больше не нужны. В следующем примере удаляются таймеры, определяемые константами IDT \_ TIMER1, IDT \_ TIMER2 и IDT \_ TIMER3.


```
// Destroy the timers. 
 
KillTimer(hwnd, IDT_TIMER1); 
KillTimer(hwnd, IDT_TIMER2); 
KillTimer(hwnd, IDT_TIMER3); 
```



## <a name="using-timer-functions-to-trap-mouse-input"></a>Использование функций таймера для перехвата ввода с помощью мыши

Иногда необходимо предотвратить дополнительные входные данные, если на экране есть указатель мыши. Один из способов сделать это — создать специальную подпрограммы, которая перехватывает ввод мыши, пока не произойдет определенное событие. Многие разработчики обращаются к этой подпрограмме как «создание маусетрап».

В следующем примере функции [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) и [**киллтимер**](/windows/win32/api/winuser/nf-winuser-killtimer) используются для перехвата ввода с помощью мыши. **Сеттимер** создает таймер, который отправляет сообщение [**\_ таймера WM**](wm-timer.md) каждые 10 секунд. Каждый раз, когда приложение получает **сообщение \_ таймера WM** , оно записывает расположение указателя мыши. Если текущее расположение совпадает с предыдущим расположением, а главное окно приложения является минимальным, приложение перемещает указатель мыши на значок. Когда приложение закрывается, **киллтимер** останавливает таймер.


```
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
UINT uResult;               // SetTimer's return value 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the initial cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,             // handle to main window 
    IDT_MOUSETRAP,                   // timer identifier 
    10000,                           // 10-second interval 
    (TIMERPROC) NULL);               // no timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM  lParam)     // additional information 
{ 
 
    HDC hdc;        // handle to device context 
    POINT pt;       // current cursor location 
    RECT rc;        // location of minimized window 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
 
        case WM_TIMER: 
        // If the window is minimized, compare the current 
        // cursor position with the one from 10 seconds 
        // earlier. If the cursor position has not changed, 
        // move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left, rc.top); 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_DESTROY: 
 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
```



Хотя в следующем примере также показано, как захватывать входные данные мыши, он обрабатывает сообщение [**\_ таймера WM**](wm-timer.md) через определяемую приложением функцию обратного вызова **митимерпрок**, а не через очередь сообщений приложения.


```
UINT uResult;               // SetTimer's return value 
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the current cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,      // handle to main window 
    IDT_MOUSETRAP,            // timer identifier 
    10000,                    // 10-second interval 
    (TIMERPROC) MyTimerProc); // timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM   lParam)    // additional information 
{ 
 
    HDC hdc;            // handle to device context 
 
    switch (message) 
    { 
    // 
    // Process other messages. 
    // 
 
        case WM_DESTROY: 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
 
// MyTimerProc is an application-defined callback function that 
// processes WM_TIMER messages. 
 
VOID CALLBACK MyTimerProc( 
    HWND hwnd,        // handle to window for timer messages 
    UINT message,     // WM_TIMER message 
    UINT idTimer,     // timer identifier 
    DWORD dwTime)     // current system time 
{ 
 
    RECT rc; 
    POINT pt; 
 
    // If the window is minimized, compare the current 
    // cursor position with the one from 10 seconds earlier. 
    // If the cursor position has not changed, move the 
    // cursor to the icon. 
 
    if (IsIconic(hwnd)) 
    { 
        GetCursorPos(&pt); 
 
        if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
        { 
            GetWindowRect(hwnd, &rc); 
            SetCursorPos(rc.left, rc.top); 
        } 
        else 
        { 
            ptOld.x = pt.x; 
            ptOld.y = pt.y; 
        } 
    } 
} 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[О таймерах](about-timers.md)
</dt> </dl>

 

 
