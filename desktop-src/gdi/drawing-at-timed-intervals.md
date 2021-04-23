---
description: Вы можете рисовать через интервал времени, создав таймер с помощью функции Сеттимер.
ms.assetid: 82f9aa5e-8e42-49cf-bcd0-785bc78fe159
title: Рисование с интервалами времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1757aca4e6be8f169aea378c52038420519ee879
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544503"
---
# <a name="drawing-at-timed-intervals"></a><span data-ttu-id="aa2a6-103">Рисование с интервалами времени</span><span class="sxs-lookup"><span data-stu-id="aa2a6-103">Drawing at Timed Intervals</span></span>

<span data-ttu-id="aa2a6-104">Вы можете рисовать через интервал времени, создав таймер с помощью функции [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) .</span><span class="sxs-lookup"><span data-stu-id="aa2a6-104">You can draw at timed intervals by creating a timer with the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function.</span></span> <span data-ttu-id="aa2a6-105">Используя таймер для отправки сообщений [**\_ таймера WM**](../winmsg/wm-timer.md) в процедуру окна с регулярными интервалами, приложение может выполнять простую анимацию в клиентской области, в то время как другие приложения продолжают работать.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-105">By using a timer to send [**WM\_TIMER**](../winmsg/wm-timer.md) messages to the window procedure at regular intervals, an application can carry out simple animation in the client area while other applications continue running.</span></span>

<span data-ttu-id="aa2a6-106">В следующем примере приложение перемещает звезду из стороны в клиентскую область.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-106">In the following example, the application bounces a star from side to side in the client area.</span></span> <span data-ttu-id="aa2a6-107">Каждый раз, когда процедура окна получает [**сообщение \_ таймера WM**](../winmsg/wm-timer.md) , процедура удаляет звезду в текущей позиции, вычисляет новую позиции и рисует звездочку в новой позиции.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-107">Each time the window procedure receives a [**WM\_TIMER**](../winmsg/wm-timer.md) message, the procedure erases the star at the current position, calculates a new position, and draws the star within the new position.</span></span> <span data-ttu-id="aa2a6-108">Процедура запускает таймер, вызывая [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) при обработке сообщения о [**\_ создании WM**](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="aa2a6-108">The procedure starts the timer by calling [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) while processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>


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



<span data-ttu-id="aa2a6-109">Это приложение использует частный контекст устройства, чтобы максимально сокращать время, необходимое для подготовки контекста устройства к рисованию.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-109">This application uses a private device context to minimize the time required to prepare the device context for drawing.</span></span> <span data-ttu-id="aa2a6-110">Процедура Window извлекает и инициализирует контекст закрытого устройства при обработке сообщения о [**\_ создании WM**](../winmsg/wm-create.md) , устанавливая режим двоичной растровой операции, чтобы разрешить стирание и прорисовку звезды с помощью того же вызова функции [**ломаной линии**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) .</span><span class="sxs-lookup"><span data-stu-id="aa2a6-110">The window procedure retrieves and initializes the private device context when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message, setting the binary raster operation mode to allow the star to be erased and drawn using the same call to the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function.</span></span> <span data-ttu-id="aa2a6-111">В процедуре окна также задается источник окна просмотра, чтобы можно было рисовать звездочку, используя тот же набор точек независимо от положения звезды в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-111">The window procedure also sets the viewport origin to allow the star to be drawn using the same set of points regardless of the star's position in the client area.</span></span>

<span data-ttu-id="aa2a6-112">Приложение использует сообщение [**WM \_ Paint**](wm-paint.md) для отрисовки звезды при необходимости обновления окна.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-112">The application uses the [**WM\_PAINT**](wm-paint.md) message to draw the star whenever the window must be updated.</span></span> <span data-ttu-id="aa2a6-113">Процедура окна рисует звезду только в том случае, если она не видна; то есть только в том случае, если он был удален с помощью сообщения [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) .</span><span class="sxs-lookup"><span data-stu-id="aa2a6-113">The window procedure draws the star only if it is not visible; that is, only if it has been erased by the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message.</span></span> <span data-ttu-id="aa2a6-114">Процедура Window перехватывает сообщение **WM \_ ерасебкгнд** , чтобы установить переменную *фвисибле* , но передает сообщение [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , чтобы система могла рисовать фон окна.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-114">The window procedure intercepts the **WM\_ERASEBKGND** message to set the *fVisible* variable, but passes the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so that the system can draw the window background.</span></span>

<span data-ttu-id="aa2a6-115">Приложение использует сообщение [**\_ размера WM**](../winmsg/wm-size.md) , чтобы прерывать таймер при сворачивании окна и перезапускать таймер при восстановлении окна.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-115">The application uses the [**WM\_SIZE**](../winmsg/wm-size.md) message to stop the timer when the window is minimized and to restart the timer when the minimized window is restored.</span></span> <span data-ttu-id="aa2a6-116">В процедуре окна также используется сообщение, чтобы обновить текущую точку звезды, если размер окна уменьшился, чтобы звезда больше не наработала в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-116">The window procedure also uses the message to update the current position of the star if the size of the window has been reduced so that the star is no longer in the client area.</span></span> <span data-ttu-id="aa2a6-117">Приложение отслеживает текущую координату звезды, используя структуру, заданную параметром Рккуррент, который определяет ограничивающий прямоугольник для звезды.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-117">The application keeps track of the star's current position by using the structure specified by rcCurrent, which defines the bounding rectangle for the star.</span></span> <span data-ttu-id="aa2a6-118">Сохранение всех углов прямоугольника в клиентской области позволяет сохранить звезду в области.</span><span class="sxs-lookup"><span data-stu-id="aa2a6-118">Keeping all corners of the rectangle in the client area keeps the star in the area.</span></span> <span data-ttu-id="aa2a6-119">Процедура окна изначально выравнивает звезду в клиентской области при обработке сообщения о [**\_ создании WM**](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="aa2a6-119">The window procedure initially centers the star in the client area when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>

 

 
