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
# <a name="drawing-a-minimized-window"></a>Рисование окна с минимальным объемом

Вы можете нарисовать собственные окна с минимальным количеством окон, а не нарисовать их. Большинство приложений определяют значок класса при регистрации класса окна для окна, и система рисует значок при сворачивании окна. Однако если задать для значка класса **значение NULL**, система отправляет сообщение [**WM \_ Paint**](wm-paint.md) в свою оконную процедуру всякий раз, когда окно свернется, позволяя оконной процедуре рисовать в скрытом окне.

В следующем примере процедура окна рисует звезду в окне с уменьшенным числом. Процедура использует функцию « [**Icon**](/windows/win32/api/winuser/nf-winuser-isiconic) », чтобы определить, когда окно свернется. Это гарантирует, что звезда будет отображаться только при сворачивании окна.


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



Чтобы задать для значка класса **значение NULL** , установите для элемента **Хикон** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) **значение NULL** перед вызовом функции [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) для класса Window.

 

 
