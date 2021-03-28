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
# <a name="drawing-in-the-client-area"></a><span data-ttu-id="73680-103">Рисование в клиентской области</span><span class="sxs-lookup"><span data-stu-id="73680-103">Drawing in the Client Area</span></span>

<span data-ttu-id="73680-104">Для подготовки и завершения рисования в клиентской области используются функции [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) и [**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="73680-104">You use the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions to prepare for and complete the drawing in the client area.</span></span> <span data-ttu-id="73680-105">**Бегинпаинт** возвращает маркер контекста устройства отображения, используемого для рисования в клиентской области. **Ендпаинт** завершает запрос на рисование и освобождает контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="73680-105">**BeginPaint** returns a handle to the display device context used for drawing in the client area; **EndPaint** ends the paint request and releases the device context.</span></span>

<span data-ttu-id="73680-106">В следующем примере процедура окна записывает сообщение «Hello, Windows!».</span><span class="sxs-lookup"><span data-stu-id="73680-106">In the following example, the window procedure writes the message "Hello, Windows!"</span></span> <span data-ttu-id="73680-107">в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="73680-107">in the client area.</span></span> <span data-ttu-id="73680-108">Чтобы обеспечить видимость строки при первом создании окна, функция [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) вызывает [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) сразу после создания и отображения окна.</span><span class="sxs-lookup"><span data-stu-id="73680-108">To make sure the string is visible when the window is first created, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) immediately after creating and showing the window.</span></span> <span data-ttu-id="73680-109">Это приводит к немедленной отправке сообщения [**WM \_ Paint**](wm-paint.md) в процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="73680-109">This causes a [**WM\_PAINT**](wm-paint.md) message to be sent immediately to the window procedure.</span></span>


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



 

 
