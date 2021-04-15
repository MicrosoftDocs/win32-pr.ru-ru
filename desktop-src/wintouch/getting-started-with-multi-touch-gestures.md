---
title: начало работы с помощью сенсорных жестов Windows
description: В этом разделе описаны основные шаги для использования жестов Мультисенсорная.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Касание Windows, жесты
- Касание Windows, сообщения
- жесты, сведения
- жесты, сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410653"
---
# <a name="getting-started-with-windows-touch-gestures"></a>начало работы с помощью сенсорных жестов Windows

В этом разделе описаны основные шаги для использования жестов Мультисенсорная.

При использовании жестов касания Windows обычно выполняются следующие действия.

1.  Настройка окна для получения жестов.
2.  Обрабатывает сообщения жестов.
3.  Интерпретировать сообщения жестов.

## <a name="setting-up-a-window-to-receive-gestures"></a>Настройка окна для получения жестов

По умолчанию вы получаете [**сообщения \_ жестов WM**](wm-gesture.md) .

> [!Note]  
> При вызове [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)вы перестанете получать [**сообщения \_ жестов WM**](wm-gesture.md) . Если вы не получаете сообщения **\_ жестов WM** , убедитесь, что вы не вызывали **регистертаучвиндов**.

 

В следующем коде показана простая реализация InitInstance.


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a>Обработка сообщений жестов

Аналогично обработке сообщений сенсорного ввода Windows можно обрабатывать сообщения жестов различными способами. Если вы используете Win32, вы можете проверить сообщение [**\_ жеста WM**](wm-gesture.md) в WndProc. При создании приложения другого типа можно добавить в схему сообщений сообщение **\_ жеста WM** , а затем реализовать пользовательский обработчик.

В следующем коде показано, как можно обработать сообщения жестов.


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a>Интерпретация сообщений жестов

Функция [**жетжестуреинфо**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) используется для интерпретации сообщения жеста в структуру, описывающую жест. Структура [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)содержит сведения о жесте, например расположение, в котором был выполнен жест, и тип жеста. В следующем коде показано, как можно получить и интерпретировать сообщение жеста.


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Сенсорные жесты Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




