---
description: Приложение может перерисовывать все содержимое клиентской области каждый раз, когда размер окна изменяется путем установки \_ стилей CS хредрав и CS \_ вредрав для класса Window.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Перерисовка всей клиентской области
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3c438fe36160f27b1015daf7874e237035f927825199b93b3a508668f40bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759150"
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



 

 



