---
description: Чтобы нарисовать затененный треугольник, определите структуру ТРИВЕРТЕКС с тремя элементами и одной ГРАДИЕНТной \_ структурой.
ms.assetid: 78834f92-00cb-4899-851a-1de5e3c1f4fa
title: Рисование затененного треугольника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3200a1ec061d7513cbac56c8c66104154005cef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155638"
---
# <a name="drawing-a-shaded-triangle"></a><span data-ttu-id="673f7-103">Рисование затененного треугольника</span><span class="sxs-lookup"><span data-stu-id="673f7-103">Drawing a Shaded Triangle</span></span>

<span data-ttu-id="673f7-104">Чтобы нарисовать затененный треугольник, определите структуру [**тривертекс**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) с тремя элементами и одной [**градиентной \_**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) структурой.</span><span class="sxs-lookup"><span data-stu-id="673f7-104">To draw a shaded triangle, define a [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) structure with three elements and a single [**GRADIENT\_TRIANGLE**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) structure.</span></span> <span data-ttu-id="673f7-105">В следующем примере кода показано, как нарисовать затененный треугольник с помощью функции [**градиентфилл**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) с \_ \_ определенным РЕЖИМом треугольника градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="673f7-105">The following code example shows how to draw a shaded triangle using the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function with the GRADIENT\_FILL\_TRIANGLE mode defined.</span></span>


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_PAINT:
        {hdc = BeginPaint(hWnd, &ps);
// Create an array of TRIVERTEX structures that describe
// positional and color values for each vertex.
TRIVERTEX vertex[3];
vertex[0].x     = 150;
vertex[0].y     = 0;
vertex[0].Red   = 0xff00;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x0000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 0;
vertex[1].y     = 150;
vertex[1].Red   = 0x9000;
vertex[1].Green = 0x0000;
vertex[1].Blue  = 0x9000;
vertex[1].Alpha = 0x0000;

vertex[2].x     = 300;
vertex[2].y     = 150; 
vertex[2].Red   = 0x9000;
vertex[2].Green = 0x0000;
vertex[2].Blue  = 0x9000;
vertex[2].Alpha = 0x0000;

// Create a GRADIENT_TRIANGLE structure that
// references the TRIVERTEX vertices.
GRADIENT_TRIANGLE gTriangle;
gTriangle.Vertex1 = 0;
gTriangle.Vertex2 = 1;
gTriangle.Vertex3 = 2;

// Draw a shaded triangle.
GradientFill(hdc, vertex, 3, &gTriangle, 1, GRADIENT_FILL_TRIANGLE);
        EndPaint(hWnd, &ps);
        break;}
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



<span data-ttu-id="673f7-106">На следующем рисунке показан результат рисования предыдущего примера кода.</span><span class="sxs-lookup"><span data-stu-id="673f7-106">The following image shows the drawing output of the preceding code example.</span></span>

![Иллюстрация, показывающая треугольник, который заполняется от оранжевый в верхней точке до пурпурного на нижнем крае](images/gradientfilltriangle.png)

## <a name="related-topics"></a><span data-ttu-id="673f7-108">См. также</span><span class="sxs-lookup"><span data-stu-id="673f7-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="673f7-109">Общие сведения о точечных рисунках</span><span class="sxs-lookup"><span data-stu-id="673f7-109">Bitmaps Overview</span></span>](bitmaps.md)
</dt> <dt>

[<span data-ttu-id="673f7-110">Функции точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="673f7-110">Bitmap Functions</span></span>](bitmap-functions.md)
</dt> <dt>

[<span data-ttu-id="673f7-111">Рисование затененного прямоугольника</span><span class="sxs-lookup"><span data-stu-id="673f7-111">Drawing a Shaded Rectangle</span></span>](drawing-a-shaded-rectangle.md)
</dt> <dt>

[<span data-ttu-id="673f7-112">**емрградиентфилл**</span><span class="sxs-lookup"><span data-stu-id="673f7-112">**EMRGRADIENTFILL**</span></span>](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[<span data-ttu-id="673f7-113">**ГРАДИЕНТный \_ треугольник**</span><span class="sxs-lookup"><span data-stu-id="673f7-113">**GRADIENT\_TRIANGLE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)
</dt> <dt>

[<span data-ttu-id="673f7-114">**градиентфилл**</span><span class="sxs-lookup"><span data-stu-id="673f7-114">**GradientFill**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[<span data-ttu-id="673f7-115">**тривертекс**</span><span class="sxs-lookup"><span data-stu-id="673f7-115">**TRIVERTEX**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



