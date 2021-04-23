---
description: 'В этом разделе приведен пример, демонстрирующий следующие задачи:'
ms.assetid: 61db38d7-9371-4ff1-b96b-1bed4c2a2749
title: Использование пространств координат и преобразований
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b75f9cab36946eee157ade824e7012018bf80d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985364"
---
# <a name="using-coordinate-spaces-and-transformations"></a><span data-ttu-id="15454-103">Использование пространств координат и преобразований</span><span class="sxs-lookup"><span data-stu-id="15454-103">Using Coordinate Spaces and Transformations</span></span>

<span data-ttu-id="15454-104">В этом разделе приведен пример, демонстрирующий следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="15454-104">This section contains an example that demonstrates the following tasks:</span></span>

-   <span data-ttu-id="15454-105">Рисование графики с предопределенными единицами.</span><span class="sxs-lookup"><span data-stu-id="15454-105">Drawing graphics with predefined units.</span></span>
-   <span data-ttu-id="15454-106">Центрирование графики в клиентской области приложения.</span><span class="sxs-lookup"><span data-stu-id="15454-106">Centering graphics in the application's client area.</span></span>
-   <span data-ttu-id="15454-107">Масштабирование вывода графики до половины исходного размера.</span><span class="sxs-lookup"><span data-stu-id="15454-107">Scaling graphics output to half its original size.</span></span>
-   <span data-ttu-id="15454-108">Преобразование графического вывода 3/4 дюйма вправо.</span><span class="sxs-lookup"><span data-stu-id="15454-108">Translating graphics output 3/4 of an inch to the right.</span></span>
-   <span data-ttu-id="15454-109">Вращение графики на 30 градусов.</span><span class="sxs-lookup"><span data-stu-id="15454-109">Rotating graphics 30 degrees.</span></span>
-   <span data-ttu-id="15454-110">Наклон графического вывода вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="15454-110">Shearing graphics output along the x-axis.</span></span>
-   <span data-ttu-id="15454-111">Отражение графического вывода о мнимой горизонтальной оси, нарисованной по средней точке.</span><span class="sxs-lookup"><span data-stu-id="15454-111">Reflecting graphics output about an imaginary horizontal axis drawn through its midpoint.</span></span>

<span data-ttu-id="15454-112">Следующий пример использовался для создания иллюстраций, которые отображаются ранее в этом обзоре.</span><span class="sxs-lookup"><span data-stu-id="15454-112">The following example was used to create the illustrations that appear earlier in this overview.</span></span>


```C++
void TransformAndDraw(int iTransform, HWND hWnd) 
{ 
    HDC hDC; 
    XFORM xForm; 
    RECT rect; 
 
    // Retrieve a DC handle for the application's window.  
 
    hDC = GetDC(hWnd); 
 
    // Set the mapping mode to LOENGLISH. This moves the  
    // client area origin from the upper left corner of the  
    // window to the lower left corner (this also reorients  
    // the y-axis so that drawing operations occur in a true  
    // Cartesian space). It guarantees portability so that  
    // the object drawn retains its dimensions on any display.  

    SetGraphicsMode(hDC, GM_ADVANCED);
    SetMapMode(hDC, MM_LOENGLISH); 
 
    // Set the appropriate world transformation (based on the  
    // user's menu selection).  
 
    switch (iTransform) 
    { 
        case SCALE:        // Scale to 1/2 of the original size.  
            xForm.eM11 = (FLOAT) 0.5; 
            xForm.eM12 = (FLOAT) 0.0; 
            xForm.eM21 = (FLOAT) 0.0; 
            xForm.eM22 = (FLOAT) 0.5; 
            xForm.eDx  = (FLOAT) 0.0; 
            xForm.eDy  = (FLOAT) 0.0; 
            SetWorldTransform(hDC, &xForm); 
            break; 
 
        case TRANSLATE:   // Translate right by 3/4 inch.  
            xForm.eM11 = (FLOAT) 1.0; 
            xForm.eM12 = (FLOAT) 0.0; 
            xForm.eM21 = (FLOAT) 0.0; 
            xForm.eM22 = (FLOAT) 1.0; 
            xForm.eDx  = (FLOAT) 75.0; 
            xForm.eDy  = (FLOAT) 0.0; 
            SetWorldTransform(hDC, &xForm); 
            break; 
 
        case ROTATE:      // Rotate 30 degrees counterclockwise.  
            xForm.eM11 = (FLOAT) 0.8660; 
            xForm.eM12 = (FLOAT) 0.5000; 
            xForm.eM21 = (FLOAT) -0.5000; 
            xForm.eM22 = (FLOAT) 0.8660; 
            xForm.eDx  = (FLOAT) 0.0; 
            xForm.eDy  = (FLOAT) 0.0; 
            SetWorldTransform(hDC, &xForm); 
            break; 
 
        case SHEAR:       // Shear along the x-axis with a  
                          // proportionality constant of 1.0.  
            xForm.eM11 = (FLOAT) 1.0; 
            xForm.eM12 = (FLOAT) 1.0; 
            xForm.eM21 = (FLOAT) 0.0; 
            xForm.eM22 = (FLOAT) 1.0; 
            xForm.eDx  = (FLOAT) 0.0; 
            xForm.eDy  = (FLOAT) 0.0; 
            SetWorldTransform(hDC, &xForm); 
            break; 
 
        case REFLECT:     // Reflect about a horizontal axis.  
            xForm.eM11 = (FLOAT) 1.0; 
            xForm.eM12 = (FLOAT) 0.0; 
            xForm.eM21 = (FLOAT) 0.0; 
            xForm.eM22 = (FLOAT) -1.0; 
            xForm.eDx  = (FLOAT) 0.0; 
            xForm.eDy  = (FLOAT) 0.0; 
            SetWorldTransform(hDC, &xForm); 
            break; 
 
        case NORMAL:      // Set the unity transformation.  
            xForm.eM11 = (FLOAT) 1.0; 
            xForm.eM12 = (FLOAT) 0.0; 
            xForm.eM21 = (FLOAT) 0.0; 
            xForm.eM22 = (FLOAT) 1.0; 
            xForm.eDx  = (FLOAT) 0.0; 
            xForm.eDy  = (FLOAT) 0.0; 
            SetWorldTransform(hDC, &xForm); 
            break; 
 
    } 
 
    // Find the midpoint of the client area.  
 
    GetClientRect(hWnd, (LPRECT) &rect); 
    DPtoLP(hDC, (LPPOINT) &rect, 2); 
 
    // Select a hollow brush.  
 
    SelectObject(hDC, GetStockObject(HOLLOW_BRUSH)); 
 
    // Draw the exterior circle.  
 
    Ellipse(hDC, (rect.right / 2 - 100), (rect.bottom / 2 + 100), 
        (rect.right / 2 + 100), (rect.bottom / 2 - 100)); 
 
    // Draw the interior circle.  
 
    Ellipse(hDC, (rect.right / 2 -94), (rect.bottom / 2 + 94), 
        (rect.right / 2 + 94), (rect.bottom / 2 - 94)); 
 
    // Draw the key.  
 
    Rectangle(hDC, (rect.right / 2 - 13), (rect.bottom / 2 + 113), 
        (rect.right / 2 + 13), (rect.bottom / 2 + 50)); 
    Rectangle(hDC, (rect.right / 2 - 13), (rect.bottom / 2 + 96), 
        (rect.right / 2 + 13), (rect.bottom / 2 + 50)); 
 
    // Draw the horizontal lines.  
 
    MoveToEx(hDC, (rect.right/2 - 150), (rect.bottom / 2 + 0), NULL); 
    LineTo(hDC, (rect.right / 2 - 16), (rect.bottom / 2 + 0)); 
 
    MoveToEx(hDC, (rect.right / 2 - 13), (rect.bottom / 2 + 0), NULL); 
    LineTo(hDC, (rect.right / 2 + 13), (rect.bottom / 2 + 0)); 
 
    MoveToEx(hDC, (rect.right / 2 + 16), (rect.bottom / 2 + 0), NULL); 
    LineTo(hDC, (rect.right / 2 + 150), (rect.bottom / 2 + 0)); 
 
    // Draw the vertical lines.  
 
    MoveToEx(hDC, (rect.right/2 + 0), (rect.bottom / 2 - 150), NULL); 
    LineTo(hDC, (rect.right / 2 + 0), (rect.bottom / 2 - 16)); 
 
    MoveToEx(hDC, (rect.right / 2 + 0), (rect.bottom / 2 - 13), NULL); 
    LineTo(hDC, (rect.right / 2 + 0), (rect.bottom / 2 + 13)); 
 
    MoveToEx(hDC, (rect.right / 2 + 0), (rect.bottom / 2 + 16), NULL); 
    LineTo(hDC, (rect.right / 2 + 0), (rect.bottom / 2 + 150)); 
 
    ReleaseDC(hWnd, hDC); 
} 
```



 

 



