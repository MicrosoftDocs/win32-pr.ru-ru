---
description: Система не является единственным источником \_ сообщений WM Paint. Функция Инвалидатерект или Инвалидатергн может косвенно создавать \_ сообщения WM Paint для окон. Эти функции отмечают всю клиентскую область как недопустимую (которую необходимо перерисовать) или ее часть.
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Идет недействительность клиентской области
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76fb02be44f600b80f87ec8f05c022fa3c35d827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997347"
---
# <a name="invalidating-the-client-area"></a><span data-ttu-id="20e59-105">Идет недействительность клиентской области</span><span class="sxs-lookup"><span data-stu-id="20e59-105">Invalidating the Client Area</span></span>

<span data-ttu-id="20e59-106">Система не является единственным источником сообщений [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="20e59-106">The system is not the only source of [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="20e59-107">Функция [**инвалидатерект**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) или [**инвалидатергн**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) может косвенно создавать сообщения **WM \_ Paint** для окон.</span><span class="sxs-lookup"><span data-stu-id="20e59-107">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function can indirectly generate **WM\_PAINT** messages for your windows.</span></span> <span data-ttu-id="20e59-108">Эти функции отмечают всю клиентскую область как недопустимую (которую необходимо перерисовать) или ее часть.</span><span class="sxs-lookup"><span data-stu-id="20e59-108">These functions mark all or part of a client area as invalid (that must be redrawn).</span></span>

<span data-ttu-id="20e59-109">В следующем примере оконная процедура делает всю клиентскую область недействительной при обработке сообщений [**WM \_ char**](../inputdev/wm-char.md) .</span><span class="sxs-lookup"><span data-stu-id="20e59-109">In the following example, the window procedure invalidates the entire client area when processing [**WM\_CHAR**](../inputdev/wm-char.md) messages.</span></span> <span data-ttu-id="20e59-110">Это позволяет пользователю изменить рисунок, введя число и просмотрев результаты. Эти результаты отображаются, как только в очереди сообщений приложения отсутствуют другие сообщения.</span><span class="sxs-lookup"><span data-stu-id="20e59-110">This allows the user to change the figure by typing a number and view the results; these results are drawn as soon as there are no other messages in the application's message queue.</span></span>


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



<span data-ttu-id="20e59-111">В этом примере аргумент **null** , используемый в [**инвалидатерект**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) , указывает всю клиентскую область. Аргумент **true** приводит к удалению фона.</span><span class="sxs-lookup"><span data-stu-id="20e59-111">In this example, the **NULL** argument used by [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) specifies the entire client area; the **TRUE** argument causes the background to be erased.</span></span> <span data-ttu-id="20e59-112">Если вы не хотите, чтобы приложение ожидало, чтобы в очереди сообщений приложения не было других сообщений, используйте функцию [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) , чтобы принудительно отправить сообщение [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="20e59-112">If you do not want the application to wait until the application's message queue has no other messages, use the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) function to force the [**WM\_PAINT**](wm-paint.md) message to be sent immediately.</span></span> <span data-ttu-id="20e59-113">Если в клиентской области имеется какая-либо недопустимая часть, **упдатевиндов** отправляет сообщение **WM \_ Paint** для указанного окна непосредственно в процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="20e59-113">If there is any invalid part of the client area, **UpdateWindow** sends the **WM\_PAINT** message for the specified window directly to the window procedure.</span></span>

 

 
