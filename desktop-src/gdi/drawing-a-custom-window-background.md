---
description: Вы можете нарисовать собственный фон окна, не нарисуя его.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Рисование пользовательского фона окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984985"
---
# <a name="drawing-a-custom-window-background"></a><span data-ttu-id="19896-103">Рисование пользовательского фона окна</span><span class="sxs-lookup"><span data-stu-id="19896-103">Drawing a Custom Window Background</span></span>

<span data-ttu-id="19896-104">Вы можете нарисовать собственный фон окна, не нарисуя его.</span><span class="sxs-lookup"><span data-stu-id="19896-104">You can draw your own window background rather than having the system draw it for you.</span></span> <span data-ttu-id="19896-105">Большинство приложений задают дескриптор кисти или значение системного цвета для кисти фона класса при регистрации класса окна; для рисования фона система использует кисть или цвет.</span><span class="sxs-lookup"><span data-stu-id="19896-105">Most applications specify a brush handle or system color value for the class background brush when registering the window class; the system uses the brush or color to draw the background.</span></span> <span data-ttu-id="19896-106">Однако если задать для кисти фона класса **значение NULL**, система отправляет сообщение [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) в вашу оконную процедуру каждый раз, когда необходимо прорисовка фона окна, позволяя рисовать пользовательский фон.</span><span class="sxs-lookup"><span data-stu-id="19896-106">If you set the class background brush to **NULL**, however, the system sends a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to your window procedure whenever the window background must be drawn, letting you draw a custom background.</span></span>

<span data-ttu-id="19896-107">В следующем примере процедура Window рисует большой шаблон шахматной доски, который точно соответствует в окне.</span><span class="sxs-lookup"><span data-stu-id="19896-107">In the following example, the window procedure draws a large checkerboard pattern that fits neatly in the window.</span></span> <span data-ttu-id="19896-108">Процедура заполняет клиентскую область белой кистью, а затем Рисует прямоугольники 13 20 на 20 с помощью серой кисти.</span><span class="sxs-lookup"><span data-stu-id="19896-108">The procedure fills the client area with a white brush and then draws thirteen 20-by-20 rectangles using a gray brush.</span></span> <span data-ttu-id="19896-109">Контекст устройства отображения, используемый при рисовании фона, задается в параметре *wParam* сообщения.</span><span class="sxs-lookup"><span data-stu-id="19896-109">The display device context to use when drawing the background is specified in the *wParam* parameter for the message.</span></span>


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



<span data-ttu-id="19896-110">Если приложение рисует собственное окно с минимальным объемом, система также отправляет сообщение [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) в процедуру окна, чтобы нарисовать фон для сворачивания окна.</span><span class="sxs-lookup"><span data-stu-id="19896-110">If the application draws its own minimized window, the system also sends the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to the window procedure to draw the background for the minimized window.</span></span> <span data-ttu-id="19896-111">Ту же методику, которую использует [**WM \_ Paint**](wm-paint.md) , можно использовать, чтобы определить, является ли окно сведенным, то есть вызвать функцию « [**Icon**](/windows/win32/api/winuser/nf-winuser-isiconic) » и проверить возвращаемое значение **true**.</span><span class="sxs-lookup"><span data-stu-id="19896-111">You can use the same technique used by [**WM\_PAINT**](wm-paint.md) to determine whether the window is minimized that is, call the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function and check for the return value **TRUE**.</span></span>

 

 
