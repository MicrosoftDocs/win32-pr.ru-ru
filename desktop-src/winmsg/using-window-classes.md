---
description: В этом разделе приведен пример кода, показывающий, как зарегистрировать локальное окно и использовать его для создания главного окна.
ms.assetid: ea9e36c9-b10d-441e-b1b5-1ab93e009e1d
title: Использование классов окон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac7edfaf89ee336534e2cca8e25a3222b3fddd159fa6c52d34a3832a44f03a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849580"
---
# <a name="using-window-classes"></a>Использование классов окон

В этом разделе приведен пример кода, показывающий, как зарегистрировать локальное окно и использовать его для создания главного окна.

Каждый процесс должен зарегистрировать собственные классы окон. Чтобы зарегистрировать локальный класс приложения, используйте функцию [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Необходимо определить процедуру окна, заполнить члены структуры [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) , а затем передать указатель на структуру в функцию **RegisterClassEx** .

В следующем примере показано, как зарегистрировать локальный класс окна и использовать его для создания главного окна.


```
#include <windows.h> 
 
// Global variable 
 
HINSTANCE hinst; 
 
// Function prototypes. 
 
int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int); 
InitApplication(HINSTANCE); 
InitInstance(HINSTANCE, int); 
LRESULT CALLBACK MainWndProc(HWND, UINT, WPARAM, LPARAM); 
 
// Application entry point. 
 
int WINAPI WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, 
    LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg; 
 
    if (!InitApplication(hinstance)) 
        return FALSE; 
 
    if (!InitInstance(hinstance, nCmdShow)) 
        return FALSE; 
 
    BOOL fGotMessage;
    while ((fGotMessage = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0 && fGotMessage != -1) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(lpCmdLine); 
} 
 
BOOL InitApplication(HINSTANCE hinstance) 
{ 
    WNDCLASSEX wcx; 
 
    // Fill in the window class structure with parameters 
    // that describe the main window. 
 
    wcx.cbSize = sizeof(wcx);          // size of structure 
    wcx.style = CS_HREDRAW | 
        CS_VREDRAW;                    // redraw if size changes 
    wcx.lpfnWndProc = MainWndProc;     // points to window procedure 
    wcx.cbClsExtra = 0;                // no extra class memory 
    wcx.cbWndExtra = 0;                // no extra window memory 
    wcx.hInstance = hinstance;         // handle to instance 
    wcx.hIcon = LoadIcon(NULL, 
        IDI_APPLICATION);              // predefined app. icon 
    wcx.hCursor = LoadCursor(NULL, 
        IDC_ARROW);                    // predefined arrow 
    wcx.hbrBackground = GetStockObject( 
        WHITE_BRUSH);                  // white background brush 
    wcx.lpszMenuName =  "MainMenu";    // name of menu resource 
    wcx.lpszClassName = "MainWClass";  // name of window class 
    wcx.hIconSm = LoadImage(hinstance, // small class icon 
        MAKEINTRESOURCE(5),
        IMAGE_ICON, 
        GetSystemMetrics(SM_CXSMICON), 
        GetSystemMetrics(SM_CYSMICON), 
        LR_DEFAULTCOLOR); 
 
    // Register the window class. 
 
    return RegisterClassEx(&wcx); 
} 
 
BOOL InitInstance(HINSTANCE hinstance, int nCmdShow) 
{ 
    HWND hwnd; 
 
    // Save the application-instance handle. 
 
    hinst = hinstance; 
 
    // Create the main window. 
 
    hwnd = CreateWindow( 
        "MainWClass",        // name of window class 
        "Sample",            // title-bar string 
        WS_OVERLAPPEDWINDOW, // top-level window 
        CW_USEDEFAULT,       // default horizontal position 
        CW_USEDEFAULT,       // default vertical position 
        CW_USEDEFAULT,       // default width 
        CW_USEDEFAULT,       // default height 
        (HWND) NULL,         // no owner window 
        (HMENU) NULL,        // use class menu 
        hinstance,           // handle to application instance 
        (LPVOID) NULL);      // no window-creation data 
 
    if (!hwnd) 
        return FALSE; 
 
    // Show the window and send a WM_PAINT message to the window 
    // procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
    return TRUE; 
 
} 
```



Регистрация глобального класса приложения аналогична регистрации локального класса приложения, за исключением того, что элемент **Style** структуры [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) должен указывать стиль **CS \_ глобалкласс** .

 

 
