---
description: Для подготовки и завершения рисования в клиентской области используются функции Бегинпаинт и Ендпаинт.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Рисование в клиентской области
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e14c8492a11a7ad9764416b2453cea3264fbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898421"
---
# <a name="drawing-in-the-client-area"></a>Рисование в клиентской области

Для подготовки и завершения рисования в клиентской области используются функции [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) и [**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint) . **Бегинпаинт** возвращает маркер контекста устройства отображения, используемого для рисования в клиентской области. **Ендпаинт** завершает запрос на рисование и освобождает контекст устройства.

В следующем примере процедура окна записывает сообщение «Hello, Windows!». в клиентской области. Чтобы обеспечить видимость строки при первом создании окна, функция [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) вызывает [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) сразу после создания и отображения окна. Это приводит к немедленной отправке сообщения [**WM \_ Paint**](wm-paint.md) в процедуру окна.


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



 

 
