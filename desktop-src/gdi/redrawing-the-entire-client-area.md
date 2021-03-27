---
description: Приложение может перерисовывать все содержимое клиентской области каждый раз, когда размер окна изменяется путем установки \_ стилей CS хредрав и CS \_ вредрав для класса Window.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Перерисовка всей клиентской области
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67640d1b464173755029bef1d0feb91f215cda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997306"
---
# <a name="redrawing-the-entire-client-area"></a><span data-ttu-id="b654e-103">Перерисовка всей клиентской области</span><span class="sxs-lookup"><span data-stu-id="b654e-103">Redrawing the Entire Client Area</span></span>

<span data-ttu-id="b654e-104">Приложение может перерисовывать все содержимое клиентской области каждый раз, когда размер окна изменяется путем установки \_ стилей CS хредрав и CS \_ вредрав для класса Window.</span><span class="sxs-lookup"><span data-stu-id="b654e-104">You can have your application redraw the entire contents of the client area whenever the window changes size by setting the CS\_HREDRAW and CS\_VREDRAW styles for the window class.</span></span> <span data-ttu-id="b654e-105">Приложения, которые корректируют размер рисунка на основе размера окна, используют эти стили, чтобы гарантировать, что они начинают с полностью пустой области клиента при рисовании.</span><span class="sxs-lookup"><span data-stu-id="b654e-105">Applications that adjust the size of the drawing based on the size of the window use these styles to ensure that they start with a completely empty client area when drawing.</span></span>

<span data-ttu-id="b654e-106">В следующем примере процедура Window рисует пять-направленную звезду, которая точно соответствует в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="b654e-106">In the following example, the window procedure draws a five-pointed star that fits neatly in the client area.</span></span> <span data-ttu-id="b654e-107">Он использует общий контекст устройства и должен устанавливать режим сопоставления, а также экстенты окон и окна просмотра каждый раз, когда обрабатывается сообщение [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="b654e-107">It uses a common device context and must set the mapping mode as well as window and viewport extents each time the [**WM\_PAINT**](wm-paint.md) message is processed.</span></span>


```C++
LRESULT APIENTRY WndProc(HWMD hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
    RECT rc; 
    POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
    . 
    . 
    . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            GetClientRect(hwnd, &rc); 
            SetMapMode(hdc, MM_ANISOTROPIC); 
            SetWindowExtEx(hdc, 100, 100, NULL); 
            SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
            Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
        . 
        . 
        . 
} 
 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    WNDCLASS wc; 
 
    . 
    . 
    . 
 
        wc.style = CS_HREDRAW | CS_VREDRAW; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
 
    . 
    . 
    . 
 
        RegisterClass(&wc); 
 
    . 
    . 
    . 
 
    return msg.wParam; 
} 
```



 

 



