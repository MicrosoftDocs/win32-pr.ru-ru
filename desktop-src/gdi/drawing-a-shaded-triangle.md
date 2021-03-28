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
# <a name="drawing-a-shaded-triangle"></a>Рисование затененного треугольника

Чтобы нарисовать затененный треугольник, определите структуру [**тривертекс**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) с тремя элементами и одной [**градиентной \_**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) структурой. В следующем примере кода показано, как нарисовать затененный треугольник с помощью функции [**градиентфилл**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) с \_ \_ определенным РЕЖИМом треугольника градиентной заливки.


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



На следующем рисунке показан результат рисования предыдущего примера кода.

![Иллюстрация, показывающая треугольник, который заполняется от оранжевый в верхней точке до пурпурного на нижнем крае](images/gradientfilltriangle.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения о точечных рисунках](bitmaps.md)
</dt> <dt>

[Функции точечного рисунка](bitmap-functions.md)
</dt> <dt>

[Рисование затененного прямоугольника](drawing-a-shaded-rectangle.md)
</dt> <dt>

[**емрградиентфилл**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**ГРАДИЕНТный \_ треугольник**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)
</dt> <dt>

[**градиентфилл**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**тривертекс**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



