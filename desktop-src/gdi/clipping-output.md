---
description: После того, как пользователь щелкнет клип в меню, приложение будет использовать координаты прямоугольника, созданного пользователем для определения области отсечения.
ms.assetid: 5ae60181-c72e-4a28-99eb-e23d35c46685
title: Вырезание выходных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc0181340b03421815ebe0f5cd8328d4793a406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991502"
---
# <a name="clipping-output"></a><span data-ttu-id="b29f3-103">Вырезание выходных данных</span><span class="sxs-lookup"><span data-stu-id="b29f3-103">Clipping Output</span></span>

<span data-ttu-id="b29f3-104">После того, как пользователь щелкнет клип в меню, приложение будет использовать координаты прямоугольника, созданного пользователем для определения области отсечения.</span><span class="sxs-lookup"><span data-stu-id="b29f3-104">After the user clicks Clip from the menu, the application uses the coordinates of the rectangle the user created to define a clipping region.</span></span> <span data-ttu-id="b29f3-105">Определив вырезанную область и выбрав ее в контексте устройства приложения, приложение Перерисовывает изображение точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="b29f3-105">After defining the clipping region and selecting it into the application's device context, the application redraws the bitmapped image.</span></span> <span data-ttu-id="b29f3-106">Приложение выполняет следующие задачи, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="b29f3-106">The application performs these tasks, as follows.</span></span>


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
 
case WM_COMMAND: 
    switch (wParam) 
    { 
 
    case IDM_CLIP: 
 
    hdc = GetDC(hwnd); 
 
    // Retrieve the application's client rectangle and paint  
    // with the default (white) brush.  
 
    GetClientRect(hwnd, &rctTmp); 
    FillRect(hdc, &rctTmp, GetStockObject(WHITE_BRUSH)); 
 
    // Use the rect coordinates to define a clipping region.  
 
    hrgn = CreateRectRgn(aptRect[0].x, aptRect[0].y, 
        aptRect[2].x, aptRect[2].y); 
    SelectClipRgn(hdc, hrgn); 
 
    // Transfer (draw) the bitmap into the clipped rectangle.  
 
    BitBlt(hdc, 
       0, 0, 
       bmp.bmWidth, bmp.bmHeight, 
       hdcCompatible, 
       0, 0, 
       SRCCOPY); 
 
    ReleaseDC(hwnd, hdc); 
    break; 
    }
```



 

 



