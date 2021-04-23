---
description: Вы можете нарисовать собственные окна с минимальным количеством окон, а не нарисовать их.
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: Рисование окна с минимальным объемом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced1f3205243ea098856517590d58caee851329a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423829"
---
# <a name="drawing-a-minimized-window"></a><span data-ttu-id="ebdc2-103">Рисование окна с минимальным объемом</span><span class="sxs-lookup"><span data-stu-id="ebdc2-103">Drawing a Minimized Window</span></span>

<span data-ttu-id="ebdc2-104">Вы можете нарисовать собственные окна с минимальным количеством окон, а не нарисовать их.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-104">You can draw your own minimized windows rather than having the system draw them for you.</span></span> <span data-ttu-id="ebdc2-105">Большинство приложений определяют значок класса при регистрации класса окна для окна, и система рисует значок при сворачивании окна.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-105">Most applications define a class icon when registering the window class for the window, and the system draws the icon when the window is minimized.</span></span> <span data-ttu-id="ebdc2-106">Однако если задать для значка класса **значение NULL**, система отправляет сообщение [**WM \_ Paint**](wm-paint.md) в свою оконную процедуру всякий раз, когда окно свернется, позволяя оконной процедуре рисовать в скрытом окне.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-106">If you set the class icon to **NULL**, however, the system sends a [**WM\_PAINT**](wm-paint.md) message to your window procedure whenever the window is minimized, enabling the window procedure to draw in the minimized window.</span></span>

<span data-ttu-id="ebdc2-107">В следующем примере процедура окна рисует звезду в окне с уменьшенным числом.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-107">In the following example, the window procedure draws a star in the minimized window.</span></span> <span data-ttu-id="ebdc2-108">Процедура использует функцию « [**Icon**](/windows/win32/api/winuser/nf-winuser-isiconic) », чтобы определить, когда окно свернется.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-108">The procedure uses the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function to determine when the window is minimized.</span></span> <span data-ttu-id="ebdc2-109">Это гарантирует, что звезда будет отображаться только при сворачивании окна.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-109">This ensures that the star is drawn only when the window is minimized.</span></span>


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



<span data-ttu-id="ebdc2-110">Чтобы задать для значка класса **значение NULL** , установите для элемента **Хикон** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) **значение NULL** перед вызовом функции [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) для класса Window.</span><span class="sxs-lookup"><span data-stu-id="ebdc2-110">You set the class icon to **NULL** by setting the **hIcon** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to **NULL** before calling the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function for the window class.</span></span>

 

 
