---
description: Для рисования маркеров можно использовать функции линий.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Маркеры рисования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b725e3a266e296950394a9bb9b2b76a17cb25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811974"
---
# <a name="drawing-markers"></a><span data-ttu-id="e8679-103">Маркеры рисования</span><span class="sxs-lookup"><span data-stu-id="e8679-103">Drawing Markers</span></span>

<span data-ttu-id="e8679-104">Для рисования маркеров можно использовать функции линий.</span><span class="sxs-lookup"><span data-stu-id="e8679-104">You can use the line functions to draw markers.</span></span> <span data-ttu-id="e8679-105">Маркер — это символ в центре точки.</span><span class="sxs-lookup"><span data-stu-id="e8679-105">A marker is a symbol centered over a point.</span></span> <span data-ttu-id="e8679-106">Графические приложения используют маркеры для обозначения начальных точек, конечных точек и контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="e8679-106">Drawing applications use markers to designate starting points, ending points, and control points.</span></span> <span data-ttu-id="e8679-107">Приложения электронных таблиц используют маркеры для обозначения интересующих вас точек на диаграмме или графике.</span><span class="sxs-lookup"><span data-stu-id="e8679-107">Spreadsheet applications use markers to designate points of interest on a chart or graph.</span></span>

<span data-ttu-id="e8679-108">В следующем примере кода функция с маркерами, определяемая приложением, создает маркер с помощью функций [**моветоекс**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) и [**lineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) .</span><span class="sxs-lookup"><span data-stu-id="e8679-108">In the following code sample, the application-defined Marker function creates a marker by using the [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) and [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) functions.</span></span> <span data-ttu-id="e8679-109">Эти функции нарисуют две пересекающиеся линии, 20 пикселов в длине, центрированные по координатам курсора.</span><span class="sxs-lookup"><span data-stu-id="e8679-109">These functions draw two intersecting lines, 20 pixels in length, centered over the cursor coordinates.</span></span>


```C++
void Marker(LONG x, LONG y, HWND hwnd) 
{ 
    HDC hdc; 
 
    hdc = GetDC(hwnd); 
        MoveToEx(hdc, (int) x - 10, (int) y, (LPPOINT) NULL); 
        LineTo(hdc, (int) x + 10, (int) y); 
        MoveToEx(hdc, (int) x, (int) y - 10, (LPPOINT) NULL); 
        LineTo(hdc, (int) x, (int) y + 10); 

    ReleaseDC(hwnd, hdc); 
} 
```



<span data-ttu-id="e8679-110">Система сохраняет координаты курсора в параметре *lParam* сообщения [**WM \_ лбуттондовн**](../inputdev/wm-lbuttondown.md) , когда пользователь нажимает левую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="e8679-110">The system stores the coordinates of the cursor in the *lParam* parameter of the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message when the user presses the left mouse button.</span></span> <span data-ttu-id="e8679-111">В следующем коде показано, как приложение получает эти координаты, определяет, находятся ли они в своей клиентской области, и передает их функции маркера для рисования маркера.</span><span class="sxs-lookup"><span data-stu-id="e8679-111">The following code demonstrates how an application gets these coordinates, determines whether they lie within its client area, and passes them to the Marker function to draw the marker.</span></span>


```C++
// Line- and arc-drawing variables  
 
static BOOL bCollectPoints; 
static POINT ptMouseDown[32]; 
static int index; 
POINTS ptTmp; 
RECT rc; 
 
    case WM_LBUTTONDOWN: 
 
 
        if (bCollectPoints && index < 32)
        { 
            // Create the region from the client area.  
 
            GetClientRect(hwnd, &rc); 
            hrgn = CreateRectRgn(rc.left, rc.top, 
                rc.right, rc.bottom); 
 
            ptTmp = MAKEPOINTS((POINTS FAR *) lParam); 
            ptMouseDown[index].x = (LONG) ptTmp.x; 
            ptMouseDown[index].y = (LONG) ptTmp.y; 
 
            // Test for a hit in the client rectangle.  
 
            if (PtInRegion(hrgn, ptMouseDown[index].x, 
                    ptMouseDown[index].y)) 
            { 
                // If a hit occurs, record the mouse coords.  
 
                Marker(ptMouseDown[index].x, ptMouseDown[index].y, 
                    hwnd); 
                index++; 
            } 
        } 
        break; 
```



 

 
