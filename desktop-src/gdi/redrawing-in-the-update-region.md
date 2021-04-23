---
description: Можно ограничить объем отрисовки приложения при обработке \_ сообщения WM Paint, определив размер и расположение региона обновления.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Перерисовка в регионе обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997307"
---
# <a name="redrawing-in-the-update-region"></a><span data-ttu-id="dee9f-103">Перерисовка в регионе обновления</span><span class="sxs-lookup"><span data-stu-id="dee9f-103">Redrawing in the Update Region</span></span>

<span data-ttu-id="dee9f-104">Можно ограничить объем отрисовки приложения при обработке сообщения [**WM \_ Paint**](wm-paint.md) , определив размер и расположение региона обновления.</span><span class="sxs-lookup"><span data-stu-id="dee9f-104">You can limit the amount of drawing your application carries out when processing the [**WM\_PAINT**](wm-paint.md) message by determining the size and location of the update region.</span></span> <span data-ttu-id="dee9f-105">Так как система использует область обновления при создании области обрезки для контекста устройства просмотра окна, можно косвенно определить область обновления, изучив область обрезки.</span><span class="sxs-lookup"><span data-stu-id="dee9f-105">Because the system uses the update region when creating the clipping region for the window's display device context, you can indirectly determine the update region by examining the clipping region.</span></span>

<span data-ttu-id="dee9f-106">В следующем примере процедура окна рисует треугольник, прямоугольник, пятиугольник и шестиугольник, но только в том случае, если все или часть каждой из них находится в пределах области обновления.</span><span class="sxs-lookup"><span data-stu-id="dee9f-106">In the following example, the window procedure draws a triangle, a rectangle, a pentagon, and a hexagon, but only if all or a portion of each figure lies within the update region.</span></span> <span data-ttu-id="dee9f-107">В процедуре окна используется функция [**ректвисибле**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) и прямоугольник 100 на 100, чтобы определить, находится ли фигура в области обрезки (и, следовательно, в области обновления) для контекста общего устройства, полученного [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span><span class="sxs-lookup"><span data-stu-id="dee9f-107">The window procedure uses the [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) function and a 100-by-100 rectangle to determine whether a figure is within the clipping region (and therefore the update region) for the common device context retrieved by [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span></span>


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



<span data-ttu-id="dee9f-108">Координаты каждой из фигур в этом примере находятся в том же прямоугольнике 100-by-100.</span><span class="sxs-lookup"><span data-stu-id="dee9f-108">The coordinates of each figure in this example lie within the same 100-by-100 rectangle.</span></span> <span data-ttu-id="dee9f-109">Перед рисованием фигуры процедура Window устанавливает точку просмотра в другую часть клиентской области с помощью функции [**сетвиевпорторжекс**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) .</span><span class="sxs-lookup"><span data-stu-id="dee9f-109">Before drawing a figure, the window procedure sets the viewport origin to a different part of the client area by using the [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) function.</span></span> <span data-ttu-id="dee9f-110">Это предотвращает прорисовку фигур поверх другого.</span><span class="sxs-lookup"><span data-stu-id="dee9f-110">This prevents figures from being drawn one on top of the other.</span></span> <span data-ttu-id="dee9f-111">Изменение источника окна просмотра не влияет на область обрезки, но влияет на интерпретацию координат прямоугольника, переданного в [**ректвисибле**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) .</span><span class="sxs-lookup"><span data-stu-id="dee9f-111">Changing the viewport origin does not affect the clipping region, but does affect how the coordinates of the rectangle passed to [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) are interpreted.</span></span> <span data-ttu-id="dee9f-112">Изменение источника также позволяет использовать один прямоугольник для проверки региона обновления, а не отдельных прямоугольников для каждой фигуры.</span><span class="sxs-lookup"><span data-stu-id="dee9f-112">Changing the origin also allows you to use a single rectangle to check the update region rather than individual rectangles for each figure.</span></span>

 

 



