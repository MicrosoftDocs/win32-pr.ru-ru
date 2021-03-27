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
# <a name="redrawing-the-entire-client-area"></a>Перерисовка всей клиентской области

Приложение может перерисовывать все содержимое клиентской области каждый раз, когда размер окна изменяется путем установки \_ стилей CS хредрав и CS \_ вредрав для класса Window. Приложения, которые корректируют размер рисунка на основе размера окна, используют эти стили, чтобы гарантировать, что они начинают с полностью пустой области клиента при рисовании.

В следующем примере процедура Window рисует пять-направленную звезду, которая точно соответствует в клиентской области. Он использует общий контекст устройства и должен устанавливать режим сопоставления, а также экстенты окон и окна просмотра каждый раз, когда обрабатывается сообщение [**WM \_ Paint**](wm-paint.md) .


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



 

 



