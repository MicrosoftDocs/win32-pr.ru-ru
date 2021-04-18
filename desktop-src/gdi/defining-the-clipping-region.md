---
description: Когда пользователь нажимает кнопку определить область обрезки, система выдает \_ сообщение командной строки WM.
ms.assetid: 4b20f310-98c0-42c1-b3b3-eadf9bb2003c
title: Определение области обрезки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e49693c0e94ab9b43af817f80985af98ae2ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544530"
---
# <a name="defining-the-clipping-region"></a><span data-ttu-id="a27a5-103">Определение области обрезки</span><span class="sxs-lookup"><span data-stu-id="a27a5-103">Defining the Clipping Region</span></span>

<span data-ttu-id="a27a5-104">Когда пользователь нажимает кнопку определить область обрезки, система выдает сообщение [**\_ командной строки WM**](../menurc/wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="a27a5-104">When the user clicks Define Clip Region , the system issues a [**WM\_COMMAND**](../menurc/wm-command.md) message.</span></span> <span data-ttu-id="a27a5-105">Параметр *wParam* этого сообщения содержит определяемую приложением константу, ОПРЕДЕЛЯЕМУЮ группой IDM, \_ которая указывает, что пользователь выбрал этот параметр в меню.</span><span class="sxs-lookup"><span data-stu-id="a27a5-105">The *wParam* parameter of this message contains an application-defined constant, IDM\_DEFINE, that indicates that the user selected this option from the menu.</span></span> <span data-ttu-id="a27a5-106">Приложение обрабатывает эти входные данные, устанавливая логический флаг Фдефинерегион, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="a27a5-106">The application processes this input by setting a Boolean flag, fDefineRegion, as shown in the following code sample.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
 
        case IDM_DEFINE: 
            fDefineRegion = TRUE; 
            break; 
```



<span data-ttu-id="a27a5-107">После нажатия кнопки **определить область обрезки** пользователь может начать рисование прямоугольника, щелкнув и перетащив указатель мыши, когда курсор находится в клиентской области приложения.</span><span class="sxs-lookup"><span data-stu-id="a27a5-107">After clicking **Define Clipping Region** , the user can begin drawing the rectangle by clicking and dragging the mouse while the cursor is in the application's client area.</span></span>

<span data-ttu-id="a27a5-108">Когда пользователь нажимает левую кнопку, система выдает сообщение [**WM \_ лбуттондовн**](../inputdev/wm-lbuttondown.md) .</span><span class="sxs-lookup"><span data-stu-id="a27a5-108">When the user presses the left button, the system issues a [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message.</span></span> <span data-ttu-id="a27a5-109">Параметр *lParam* этого сообщения содержит координаты курсора, которые соответствуют верхнему левому углу прямоугольника, используемого для определения вырезанной области.</span><span class="sxs-lookup"><span data-stu-id="a27a5-109">The *lParam* parameter of this message contains the cursor coordinates, which correspond to the upper left corner of a rectangle used to define the clipping region.</span></span> <span data-ttu-id="a27a5-110">Приложение обрабатывает сообщение **WM \_ лбуттондовн** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="a27a5-110">The application processes the **WM\_LBUTTONDOWN** message, as follows.</span></span>


```C++
// These variables are required for clipping.  
 
static POINT ptUpperLeft; 
static POINT ptLowerRight; 
static POINT aptRect[5]; 
static POINT ptTmp; 
static POINTS ptsTmp; 
static BOOL fDefineRegion; 
static BOOL fRegionExists; 
static HRGN hrgn; 
static RECT rctTmp; 
int i; 
 
switch (message) 
{ 
 
    case WM_LBUTTONDOWN: 
        if (fDefineRegion) 
        { 
 
        // Retrieve the new upper left corner.  
 
            ptsTmp = MAKEPOINTS(lParam); 
            ptUpperLeft.x = (LONG) ptsTmp.x; 
            ptUpperLeft.y = (LONG) ptsTmp.y; 
        } 
 
        if (fRegionExists) 
        { 
 
            // Erase the previous rectangle.  
 
            hdc = GetDC(hwnd); 
            SetROP2(hdc, R2_NOTXORPEN); 
 
            if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
                errhandler("Polyline Failed", hwnd); 
            ReleaseDC(hwnd, hdc); 
 
            // Clear the rectangle coordinates.  
 
            for (i = 0; i < 4; i++) 
            { 
                aptRect[i].x = 0; 
                aptRect[i].y = 0; 
            } 
 
            // Clear the temporary point structure.  
 
            ptTmp.x = 0; 
            ptTmp.y = 0; 
 
            // Clear the lower right coordinates.  
 
            ptLowerRight.x = 0; 
            ptLowerRight.y = 0; 
 
            // Reset the flag.  
 
            fRegionExists = FALSE; 
            fDefineRegion = TRUE; 
 
            // Retrieve the new upper left corner.  
 
            ptsTmp = MAKEPOINTS(lParam); 
            ptUpperLeft.x = (LONG) ptsTmp.x; 
            ptUpperLeft.y = (LONG) ptsTmp.y; 
        } 
    break; 
}
```



<span data-ttu-id="a27a5-111">Когда пользователь перетаскивает мышь, система выдает сообщение [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) и сохраняет новые координаты курсора в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="a27a5-111">As the user drags the mouse, the system issues [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages and stores the new cursor coordinates in the *lParam* parameter.</span></span> <span data-ttu-id="a27a5-112">Каждый раз, когда приложение получает новое сообщение **WM \_ MOUSEMOVE** , оно удаляет предыдущий прямоугольник (если он существует) и рисует новый прямоугольник путем вызова функции [**ломаной линии**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) , передавая ей координаты четырех углов прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="a27a5-112">Each time the application receives a new **WM\_MOUSEMOVE** message, it erases the previous rectangle (if one exists) and draws the new rectangle by calling the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function, passing it the coordinates of the four corners of the rectangle.</span></span> <span data-ttu-id="a27a5-113">Приложение выполняет следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="a27a5-113">The application performs the following tasks.</span></span>


```C++
// These variables are required for clipping.  
 
static POINT ptUpperLeft; 
static POINT ptLowerRight; 
static POINT aptRect[5]; 
static POINT ptTmp; 
static POINTS ptsTmp; 
static BOOL fDefineRegion; 
static BOOL fRegionExists; 
static HRGN hrgn; 
static RECT rctTmp; 
int i; 
 
switch (message) 
{ 
 
    case WM_MOUSEMOVE: 
 
    if (wParam & MK_LBUTTON && fDefineRegion) 
    { 
 
        // Get a window DC.  
 
        hdc = GetDC(hwnd); 
 
        if (!SetROP2(hdc, R2_NOTXORPEN)) 
            errhandler("SetROP2 Failed", hwnd); 
 
        // If previous mouse movement occurred, store the original  
        // lower right corner coordinates in a temporary structure.  
 
        if (ptLowerRight.x) 
        { 
            ptTmp.x = ptLowerRight.x; 
            ptTmp.y = ptLowerRight.y; 
        } 
 
        // Get the new coordinates of the clipping region's lower  
        // right corner.  
 
        ptsTmp = MAKEPOINTS(lParam); 
        ptLowerRight.x = (LONG) ptsTmp.x; 
        ptLowerRight.y = (LONG) ptsTmp.y; 
 
        // If previous mouse movement occurred, erase the original  
        // rectangle.  
 
        if (ptTmp.x) 
        { 
            aptRect[0].x = ptUpperLeft.x; 
            aptRect[0].y = ptUpperLeft.y; 
            aptRect[1].x = ptTmp.x; 
            aptRect[1].y = ptUpperLeft.y; 
            aptRect[2].x = ptTmp.x; 
            aptRect[2].y = ptTmp.y; 
            aptRect[3].x = ptUpperLeft.x; 
            aptRect[3].y = ptTmp.y; 
            aptRect[4].x = aptRect[0].x; 
            aptRect[4].y = aptRect[0].y; 
 
            if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
                errhandler("Polyline Failed", hwnd); 
        } 
 
        aptRect[0].x = ptUpperLeft.x; 
        aptRect[0].y = ptUpperLeft.y; 
        aptRect[1].x = ptLowerRight.x; 
        aptRect[1].y = ptUpperLeft.y; 
        aptRect[2].x = ptLowerRight.x; 
        aptRect[2].y = ptLowerRight.y; 
        aptRect[3].x = ptUpperLeft.x; 
        aptRect[3].y = ptLowerRight.y; 
        aptRect[4].x = aptRect[0].x; 
        aptRect[4].y = aptRect[0].y; 
 
        if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
             errhandler("Polyline Failed", hwnd); 
 
        ReleaseDC(hwnd, hdc); 
    } 
    break; 
```



 

 
