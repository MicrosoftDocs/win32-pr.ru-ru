---
description: Для рисования маркеров можно использовать функции линий.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Маркеры рисования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5e05c651bf95aa48a8ef11fd0819523ee5da7652e27ecebaeff8ee9de4f1e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887122"
---
# <a name="drawing-markers"></a>Маркеры рисования

Для рисования маркеров можно использовать функции линий. Маркер — это символ в центре точки. Графические приложения используют маркеры для обозначения начальных точек, конечных точек и контрольных точек. Приложения электронных таблиц используют маркеры для обозначения интересующих вас точек на диаграмме или графике.

В следующем примере кода функция с маркерами, определяемая приложением, создает маркер с помощью функций [**моветоекс**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) и [**lineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) . Эти функции нарисуют две пересекающиеся линии, 20 пикселов в длине, центрированные по координатам курсора.


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



Система сохраняет координаты курсора в параметре *lParam* сообщения [**WM \_ лбуттондовн**](../inputdev/wm-lbuttondown.md) , когда пользователь нажимает левую кнопку мыши. В следующем коде показано, как приложение получает эти координаты, определяет, находятся ли они в своей клиентской области, и передает их функции маркера для рисования маркера.


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



 

 
