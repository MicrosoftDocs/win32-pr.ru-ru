---
title: Обрезка изображения
description: Обрезка изображения
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- Макрос МЦивнджетсаурце
- Макрос МЦивндпутсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d73eb37792c124ad907f660d4b906ca80e715d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486757"
---
# <a name="cropping-an-image"></a>Обрезка изображения

В следующем примере создается окно МЦивнд и загружается файл AVI. Окно содержит команду обрезки в меню, которая обрезает одну четвертую высоту или ширину каждой из четырех сторон рамки. В примере извлекаются текущие (начальные) измерения исходного прямоугольника с помощью макроса [**мЦивнджетсаурце**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) . Измененный исходный прямоугольник является половиной исходной высоты и ширины и выравнивается по центру исходного фрейма. Вызов макроса [**мЦивндпутсаурце**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) переопределяет координаты исходного прямоугольника.


```C++
// extern RECT rSource, rDest; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE, 
                "sample.avi" ); 
            break; 
        case IDM_CROPIMAGE:                          // crops image 
            MCIWndGetSource(g_hwndMCIWnd, &rSource); // source rectangle
            rDest.left = rSource.left +              // new boundaries
                ((rSource.right - rSource.left) / 4); 
            rDest.right = rSource.right - 
                ((rSource.right - rSource.left) / 4); 
            rDest.top = rSource.top + 
                ((rSource.bottom - rSource.top) / 4); 
            rDest.bottom = rSource.bottom - 
                ((rSource.bottom - rSource.top) / 4); 
 
            MCIWndPutSource(g_hwndMCIWnd, &rDest);   // new source rectangle 
    } 
    break; 

    // Handle other messages here. 
```



 

 




