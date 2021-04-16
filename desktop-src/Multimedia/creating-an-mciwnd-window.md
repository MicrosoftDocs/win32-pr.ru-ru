---
title: Создание окна МЦивнд
description: Создание окна МЦивнд
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Окно МЦивнд, создание
- Функция МЦивндкреате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672039"
---
# <a name="creating-an-mciwnd-window"></a><span data-ttu-id="7ee7b-105">Создание окна МЦивнд</span><span class="sxs-lookup"><span data-stu-id="7ee7b-105">Creating an MCIWnd Window</span></span>

<span data-ttu-id="7ee7b-106">Функция [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) регистрирует и создает окно мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="7ee7b-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function registers and creates an MCIWnd window.</span></span> <span data-ttu-id="7ee7b-107">Окно может быть родительским, дочерним или всплывающим окном.</span><span class="sxs-lookup"><span data-stu-id="7ee7b-107">The window can be a parent, child, or pop-up window.</span></span> <span data-ttu-id="7ee7b-108">В следующем примере создается окно МЦивнд в качестве дочернего окна, позволяющее воспроизвести пользовательский элемент управления, предоставляя доступ к параметрам TrackBar, а также к кнопкам **воспроизведения**, **окончания** и **меню** .</span><span class="sxs-lookup"><span data-stu-id="7ee7b-108">The following example creates an MCIWnd window as a child window and lets the user control playback by providing access to the trackbar and the **Play**, **Stop**, and **Menu** buttons.</span></span> <span data-ttu-id="7ee7b-109">В примере задается маркер родительского окна и указывается **значение NULL** для стилей окна, поэтому для создания окна мЦивнд используются стили окна по умолчанию для WS- \_ потомков, WS \_ Border и WS \_ Visible.</span><span class="sxs-lookup"><span data-stu-id="7ee7b-109">The example specifies a handle of a parent window and specifies **NULL** for the window styles, so the default window styles of WS\_CHILD, WS\_BORDER, and WS\_VISIBLE are used to create the MCIWnd window.</span></span>


```C++
// Global variable and constants 
// extern HINSTANCE g_hinst;       instance handle 
// extern HWND g_hwndMCIWnd;       MCIWnd window handle 
 
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, NULL, 
            "sample.avi"); 
        break;    
    } 
    break; 
```



> [!Note]  
> <span data-ttu-id="7ee7b-110">Можно также указать **значение NULL** как для маркера родительского окна, так и для стилей окна. в этом случае стили окна по умолчанию будут иметь вид WS \_ OVERLAPPED и WS \_ Visible.</span><span class="sxs-lookup"><span data-stu-id="7ee7b-110">You could also specify **NULL** for both the parent window handle and the window styles, in which case the default window styles would be WS\_OVERLAPPED and WS\_VISIBLE.</span></span>

 

 

 




