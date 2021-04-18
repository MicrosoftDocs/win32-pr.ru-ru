---
description: Чтобы нарисовать затененный прямоугольник, определите массив ТРИВЕРТЕКС с двумя элементами и одной \_ структурой прямоугольника градиента. В следующем примере кода показано, как нарисовать затененный прямоугольник с помощью функции Градиентфилл с \_ \_ заданным режимом Rect Градиентная заливка.
ms.assetid: a4277e22-03f8-470f-87e9-5aeab258b6d2
title: Рисование затененного прямоугольника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665e76c730ada1bd8efc9967fd10e550f0aa2e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544506"
---
# <a name="drawing-a-shaded-rectangle"></a><span data-ttu-id="f3c2f-104">Рисование затененного прямоугольника</span><span class="sxs-lookup"><span data-stu-id="f3c2f-104">Drawing a Shaded Rectangle</span></span>

<span data-ttu-id="f3c2f-105">Чтобы нарисовать затененный прямоугольник, определите массив [**тривертекс**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) с двумя элементами и одной структурой [**\_ прямоугольника градиента**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) .</span><span class="sxs-lookup"><span data-stu-id="f3c2f-105">To draw a shaded rectangle, define a [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) array with two elements and a single [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) structure.</span></span> <span data-ttu-id="f3c2f-106">В следующем примере кода показано, как нарисовать затененный прямоугольник с помощью функции [**градиентфилл**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) с \_ \_ заданным режимом Rect Градиентная заливка.</span><span class="sxs-lookup"><span data-stu-id="f3c2f-106">The following code example shows how to draw a shaded rectangle using the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function with the GRADIENT\_FILL\_RECT mode defined.</span></span>


```C++
// Create an array of TRIVERTEX structures that describe 
// positional and color values for each vertex. For a rectangle, 
// only two vertices need to be defined: upper-left and lower-right. 
TRIVERTEX vertex[2] ;
vertex[0].x     = 0;
vertex[0].y     = 0;
vertex[0].Red   = 0x0000;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x8000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 300;
vertex[1].y     = 80; 
vertex[1].Red   = 0x0000;
vertex[1].Green = 0xd000;
vertex[1].Blue  = 0xd000;
vertex[1].Alpha = 0x0000;

// Create a GRADIENT_RECT structure that 
// references the TRIVERTEX vertices. 
GRADIENT_RECT gRect;
gRect.UpperLeft  = 0;
gRect.LowerRight = 1;

// Draw a shaded rectangle. 
GradientFill(hdc, vertex, 2, &gRect, 1, GRADIENT_FILL_RECT_H);
```



<span data-ttu-id="f3c2f-107">На следующем рисунке показан результат рисования предыдущего примера кода.</span><span class="sxs-lookup"><span data-stu-id="f3c2f-107">The following image shows the drawing output of the preceding code example.</span></span>

![Иллюстрация с прямоугольником с градиентной заливкой от темной левой стороны к светлой с правой стороны](images/gradientfillrectangle.png)

## <a name="related-topics"></a><span data-ttu-id="f3c2f-109">См. также</span><span class="sxs-lookup"><span data-stu-id="f3c2f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c2f-110">Общие сведения о точечных рисунках</span><span class="sxs-lookup"><span data-stu-id="f3c2f-110">Bitmaps Overview</span></span>](bitmaps.md)
</dt> <dt>

[<span data-ttu-id="f3c2f-111">Функции точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="f3c2f-111">Bitmap Functions</span></span>](bitmap-functions.md)
</dt> <dt>

[<span data-ttu-id="f3c2f-112">Рисование затененного треугольника</span><span class="sxs-lookup"><span data-stu-id="f3c2f-112">Drawing a Shaded Triangle</span></span>](drawing-a-shaded-triangle.md)
</dt> <dt>

[<span data-ttu-id="f3c2f-113">**емрградиентфилл**</span><span class="sxs-lookup"><span data-stu-id="f3c2f-113">**EMRGRADIENTFILL**</span></span>](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[<span data-ttu-id="f3c2f-114">**прямоугольник ГРАДИЕНТа \_**</span><span class="sxs-lookup"><span data-stu-id="f3c2f-114">**GRADIENT\_RECT**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[<span data-ttu-id="f3c2f-115">**градиентфилл**</span><span class="sxs-lookup"><span data-stu-id="f3c2f-115">**GradientFill**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[<span data-ttu-id="f3c2f-116">**тривертекс**</span><span class="sxs-lookup"><span data-stu-id="f3c2f-116">**TRIVERTEX**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



