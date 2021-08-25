---
title: Растяжение изображения
description: Растяжение изображения
ms.assetid: 7cfd91c3-0ebd-47eb-a33d-c81a66f820e5
keywords:
- Макрос МЦивнджетдест
- Макрос МЦивндпутдест
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 283ecc69af3298930b4fb9788a02fb60167483fc10b185dd21e696affe4ee58a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892574"
---
# <a name="stretching-an-image"></a>Растяжение изображения

Следующий пример растягивает изображения видеоклипа. Он увеличивает размеры целевого прямоугольника с помощью макроса [**мЦивндпутдест**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) . Размер области воспроизведения остается неизменным, поэтому результат представляет собой искаженное, увеличенное изображение. В примерах используется функция **мЦивндпутдест** для изменения расположения прямоугольника назначения относительно области воспроизведения, что позволяет просматривать различные фрагменты растянутого изображения.


```C++
extern RECT rCurrent, rDest; 
 
case WM_COMMAND: 
   switch (wParam) 
   { 
       case IDM_CREATEMCIWND: 
           g_hwndMCIWnd = MCIWndCreate(hwnd, 
               g_hinst, 
               WS_CHILD | WS_VISIBLE, 
               "sample.avi"); 
           break; 
 
       case  IDM_STRETCHIMAGE:      // stretch destination RECT 3:2, 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rDest.top = rCurrent.top;               // new boundaries 
           rDest.right = rCurrent.right; 
           rDest.left = rCurrent.left + 
               ((rCurrent.left - rCurrent.right) * 3); 
           rDest.bottom = rCurrent.top + 
               ((rCurrent.bottom - rCurrent.top) * 2); 
           MCIWndPutDest(g_hwndMCIWnd, &rDest); // new destination 
           break; 
       case IDM_MOVEDOWN:           // move toward bottom of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top -= 100;                    // new boundaries 
           rCurrent.bottom -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination
           break; 
       case IDM_MOVEUP:             // move toward top of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top += 100;                    // new boundaries 
           rCurrent.bottom += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case IDM_MOVELEFT:           // move toward left edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.right += 100;                  // new boundaries 
           rCurrent.left += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case  IDM_MOVERIGHT:         // move toward right edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT
           rCurrent.right -= 100;                  // new boundaries 
           rCurrent.left -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
   } 
   break; 
 
   // Handle other messages here. 
```



 

 




