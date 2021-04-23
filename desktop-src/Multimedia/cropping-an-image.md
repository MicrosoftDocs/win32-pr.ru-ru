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
# <a name="cropping-an-image"></a><span data-ttu-id="0ee43-105">Обрезка изображения</span><span class="sxs-lookup"><span data-stu-id="0ee43-105">Cropping an Image</span></span>

<span data-ttu-id="0ee43-106">В следующем примере создается окно МЦивнд и загружается файл AVI.</span><span class="sxs-lookup"><span data-stu-id="0ee43-106">The following example creates an MCIWnd window and loads an AVI file.</span></span> <span data-ttu-id="0ee43-107">Окно содержит команду обрезки в меню, которая обрезает одну четвертую высоту или ширину каждой из четырех сторон рамки.</span><span class="sxs-lookup"><span data-stu-id="0ee43-107">The window includes a crop command in the menu, which crops one-quarter of the height or width from each of the four sides of the frame.</span></span> <span data-ttu-id="0ee43-108">В примере извлекаются текущие (начальные) измерения исходного прямоугольника с помощью макроса [**мЦивнджетсаурце**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .</span><span class="sxs-lookup"><span data-stu-id="0ee43-108">The example retrieves the current (initial) dimensions of the source rectangle by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span> <span data-ttu-id="0ee43-109">Измененный исходный прямоугольник является половиной исходной высоты и ширины и выравнивается по центру исходного фрейма.</span><span class="sxs-lookup"><span data-stu-id="0ee43-109">The modified source rectangle is half the original height and width and is centered in the original frame.</span></span> <span data-ttu-id="0ee43-110">Вызов макроса [**мЦивндпутсаурце**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) переопределяет координаты исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="0ee43-110">The call to the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro redefines the coordinates of the source rectangle.</span></span>


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



 

 




