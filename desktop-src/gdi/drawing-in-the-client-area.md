---
description: Для подготовки и завершения рисования в клиентской области используются функции Бегинпаинт и Ендпаинт.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Рисование в клиентской области
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d01331ae60a7814602f6c10c0d9109ae665da39aa140223e31ac03303048b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832024"
---
# <a name="drawing-in-the-client-area"></a>Рисование в клиентской области

Для подготовки и завершения рисования в клиентской области используются функции [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) и [**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint) . **Бегинпаинт** возвращает маркер контекста устройства отображения, используемого для рисования в клиентской области. **Ендпаинт** завершает запрос на рисование и освобождает контекст устройства.

В следующем примере процедура Window записывает сообщение «Hello, Windows!». в клиентской области. Чтобы обеспечить видимость строки при первом создании окна, функция [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) вызывает [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) сразу после создания и отображения окна. Это приводит к немедленной отправке сообщения [**WM \_ Paint**](wm-paint.md) в процедуру окна.


```C++
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
 
    switch (message) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            TextOut(hdc, 0, 0, "Hello, Windows!", 15); 
            EndPaint(hwnd, &ps); 
            return 0L; 

        // Process other messages.   
    } 
} 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    HWND hwnd; 
 
    hwnd = CreateWindowEx( 
        // parameters  
        ); 
 
    ShowWindow(hwnd, SW_SHOW); 
    UpdateWindow(hwnd); 
 
    return msg.wParam; 
} 
```



 

 
