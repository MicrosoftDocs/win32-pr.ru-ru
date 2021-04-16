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
# <a name="creating-an-mciwnd-window"></a>Создание окна МЦивнд

Функция [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) регистрирует и создает окно мЦивнд. Окно может быть родительским, дочерним или всплывающим окном. В следующем примере создается окно МЦивнд в качестве дочернего окна, позволяющее воспроизвести пользовательский элемент управления, предоставляя доступ к параметрам TrackBar, а также к кнопкам **воспроизведения**, **окончания** и **меню** . В примере задается маркер родительского окна и указывается **значение NULL** для стилей окна, поэтому для создания окна мЦивнд используются стили окна по умолчанию для WS- \_ потомков, WS \_ Border и WS \_ Visible.


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
> Можно также указать **значение NULL** как для маркера родительского окна, так и для стилей окна. в этом случае стили окна по умолчанию будут иметь вид WS \_ OVERLAPPED и WS \_ Visible.

 

 

 




