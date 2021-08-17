---
description: Вы можете рисовать через интервал времени, создав таймер с помощью функции Сеттимер.
ms.assetid: 82f9aa5e-8e42-49cf-bcd0-785bc78fe159
title: Рисование с интервалами времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d82d385dce232c84be0dfeb8fd0f825891563ec64daa6c6cd41b82db81c6f67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887112"
---
# <a name="drawing-at-timed-intervals"></a>Рисование с интервалами времени

Вы можете рисовать через интервал времени, создав таймер с помощью функции [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) . Используя таймер для отправки сообщений [**\_ таймера WM**](../winmsg/wm-timer.md) в процедуру окна с регулярными интервалами, приложение может выполнять простую анимацию в клиентской области, в то время как другие приложения продолжают работать.

В следующем примере приложение перемещает звезду из стороны в клиентскую область. Каждый раз, когда процедура окна получает [**сообщение \_ таймера WM**](../winmsg/wm-timer.md) , процедура удаляет звезду в текущей позиции, вычисляет новую позиции и рисует звездочку в новой позиции. Процедура запускает таймер, вызывая [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) при обработке сообщения о [**\_ создании WM**](../winmsg/wm-create.md) .


```C++
RECT rcCurrent = {0,0,20,20}; 
POINT aptStar[6] = {10,1, 1,19, 19,6, 1,6, 19,19, 10,1}; 
int X = 2, Y = -1, idTimer = -1; 
BOOL fVisible = FALSE; 
HDC hdc; 
 
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    RECT rc; 
 
    switch (message) 
    { 
        case WM_CREATE: 
 
            // Calculate the starting point.  
 
            GetClientRect(hwnd, &rc); 
            OffsetRect(&rcCurrent, rc.right / 2, rc.bottom / 2); 
 
            // Initialize the private DC.  
 
            hdc = GetDC(hwnd); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            SetROP2(hdc, R2_NOT); 
 
            // Start the timer.  
 
            SetTimer(hwnd, idTimer = 1, 10, NULL); 
            return 0L; 
 
        case WM_DESTROY: 
            KillTimer(hwnd, 1); 
            PostQuitMessage(0); 
            return 0L; 
 
        case WM_SIZE: 
            switch (wParam) 
            { 
                case SIZE_MINIMIZED: 
 
                    // Stop the timer if the window is minimized. 
 
                    KillTimer(hwnd, 1); 
                    idTimer = -1; 
                    break; 
 
                case SIZE_RESTORED: 
 
                    // Move the star back into the client area  
                    // if necessary.  
 
                    if (rcCurrent.right > (int) LOWORD(lParam)) 
                    {
                        rcCurrent.left = 
                            (rcCurrent.right = 
                                (int) LOWORD(lParam)) - 20; 
                    }
                    if (rcCurrent.bottom > (int) HIWORD(lParam)) 
                    {
                        rcCurrent.top = 
                            (rcCurrent.bottom = 
                                (int) HIWORD(lParam)) - 20; 
                    }
 
                    // Fall through to the next case.  
 
                case SIZE_MAXIMIZED: 
 
                    // Start the timer if it had been stopped.  
 
                    if (idTimer == -1) 
                        SetTimer(hwnd, idTimer = 1, 10, NULL); 
                    break; 
            } 
            return 0L; 
 
        case WM_TIMER: 
 
            // Hide the star if it is visible.  
 
            if (fVisible) 
                Polyline(hdc, aptStar, 6); 
 
            // Bounce the star off a side if necessary.  
 
            GetClientRect(hwnd, &rc); 
            if (rcCurrent.left + X < rc.left || 
                rcCurrent.right + X > rc.right) 
                X = -X; 
            if (rcCurrent.top + Y < rc.top || 
                rcCurrent.bottom + Y > rc.bottom) 
                Y = -Y; 
 
            // Show the star in its new position.  
 
            OffsetRect(&rcCurrent, X, Y); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            fVisible = Polyline(hdc, aptStar, 6); 
 
            return 0L; 
 
        case WM_ERASEBKGND: 
 
            // Erase the star.  
 
            fVisible = FALSE; 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
        case WM_PAINT: 
 
            // Show the star if it is not visible. Use BeginPaint  
            // to clear the update region.  
 
            BeginPaint(hwnd, &ps); 
            if (!fVisible) 
                fVisible = Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
    } 
    return DefWindowProc(hwnd, message, wParam, lParam); 
} 
```



Это приложение использует частный контекст устройства, чтобы максимально сокращать время, необходимое для подготовки контекста устройства к рисованию. Процедура Window извлекает и инициализирует контекст закрытого устройства при обработке сообщения о [**\_ создании WM**](../winmsg/wm-create.md) , устанавливая режим двоичной растровой операции, чтобы разрешить стирание и прорисовку звезды с помощью того же вызова функции [**ломаной линии**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) . В процедуре окна также задается источник окна просмотра, чтобы можно было рисовать звездочку, используя тот же набор точек независимо от положения звезды в клиентской области.

Приложение использует сообщение [**WM \_ Paint**](wm-paint.md) для отрисовки звезды при необходимости обновления окна. Процедура окна рисует звезду только в том случае, если она не видна; то есть только в том случае, если он был удален с помощью сообщения [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) . Процедура Window перехватывает сообщение **WM \_ ерасебкгнд** , чтобы установить переменную *фвисибле* , но передает сообщение [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , чтобы система могла рисовать фон окна.

Приложение использует сообщение [**\_ размера WM**](../winmsg/wm-size.md) , чтобы прерывать таймер при сворачивании окна и перезапускать таймер при восстановлении окна. В процедуре окна также используется сообщение, чтобы обновить текущую точку звезды, если размер окна уменьшился, чтобы звезда больше не наработала в клиентской области. Приложение отслеживает текущую координату звезды, используя структуру, заданную параметром Рккуррент, который определяет ограничивающий прямоугольник для звезды. Сохранение всех углов прямоугольника в клиентской области позволяет сохранить звезду в области. Процедура окна изначально выравнивает звезду в клиентской области при обработке сообщения о [**\_ создании WM**](../winmsg/wm-create.md) .

 

 
