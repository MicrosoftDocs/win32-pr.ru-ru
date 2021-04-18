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
# <a name="drawing-a-shaded-rectangle"></a>Рисование затененного прямоугольника

Чтобы нарисовать затененный прямоугольник, определите массив [**тривертекс**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) с двумя элементами и одной структурой [**\_ прямоугольника градиента**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) . В следующем примере кода показано, как нарисовать затененный прямоугольник с помощью функции [**градиентфилл**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) с \_ \_ заданным режимом Rect Градиентная заливка.


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



На следующем рисунке показан результат рисования предыдущего примера кода.

![Иллюстрация с прямоугольником с градиентной заливкой от темной левой стороны к светлой с правой стороны](images/gradientfillrectangle.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения о точечных рисунках](bitmaps.md)
</dt> <dt>

[Функции точечного рисунка](bitmap-functions.md)
</dt> <dt>

[Рисование затененного треугольника](drawing-a-shaded-triangle.md)
</dt> <dt>

[**емрградиентфилл**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**прямоугольник ГРАДИЕНТа \_**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[**градиентфилл**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**тривертекс**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



