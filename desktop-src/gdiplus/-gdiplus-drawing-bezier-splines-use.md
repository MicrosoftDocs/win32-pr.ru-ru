---
description: 'A B&\# 233; сплайн Безье определяется четырьмя точками: начальной точкой, двумя контрольными точками и конечной точкой.'
ms.assetid: af19e82b-0d13-4fb0-981e-8d5dd1bbfb36
title: Рисование сплайнов Безье
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea97d25f482372c387239e8f9083b31e3b2d912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812935"
---
# <a name="drawing-bezier-splines"></a><span data-ttu-id="199e0-103">Рисование сплайнов Безье</span><span class="sxs-lookup"><span data-stu-id="199e0-103">Drawing Bezier Splines</span></span>

<span data-ttu-id="199e0-104">Сплайн Безье определяется четырьмя точками: начальной точкой, двумя контрольными точками и конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="199e0-104">A Bézier spline is defined by four points: a start point, two control points, and an end point.</span></span> <span data-ttu-id="199e0-105">В следующем примере рисуется сплайн Безье с начальной точкой (10, 100) и конечной точкой (200, 100).</span><span class="sxs-lookup"><span data-stu-id="199e0-105">The following example draws a Bézier spline with start point (10, 100) and end point (200, 100).</span></span> <span data-ttu-id="199e0-106">Контрольные точки — (100, 10) и (150, 150):</span><span class="sxs-lookup"><span data-stu-id="199e0-106">The control points are (100, 10) and (150, 150):</span></span>


```
Point p1(10, 100);   // start point
Point c1(100, 10);   // first control point
Point c2(150, 150);  // second control point
Point p2(200, 100);  // end point
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBezier(&pen, p1, c1, c2, p2);
```



<span data-ttu-id="199e0-107">На следующем рисунке показан итоговый сплайн Безье, а также его начальная точка, контрольные точки и конечная точка.</span><span class="sxs-lookup"><span data-stu-id="199e0-107">The following illustration shows the resulting Bézier spline along with its start point, control points, and end point.</span></span> <span data-ttu-id="199e0-108">На рисунке также показана выпуклойная поверхности сплайна, образованная путем соединения четырех точек с прямыми линиями.</span><span class="sxs-lookup"><span data-stu-id="199e0-108">The illustration also shows the spline's convex hull, which is a polygon formed by connecting the four points with straight lines.</span></span>

![Иллюстрация, демонстрирующая сплайн Безье с двумя конечными точками и двумя контрольными точками](images/bezierspline1.png)

<span data-ttu-id="199e0-110">Для рисования последовательности Соединенных сплайнов Безье можно использовать метод [дравбезиерс](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="199e0-110">You can use the [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a sequence of connected Bézier splines.</span></span> <span data-ttu-id="199e0-111">В следующем примере рисуется кривая, состоящая из двух Соединенных сплайнов Безье.</span><span class="sxs-lookup"><span data-stu-id="199e0-111">The following example draws a curve that consists of two connected Bézier splines.</span></span> <span data-ttu-id="199e0-112">Конечная точка первого сплайна Безье является начальной точкой второго сплайна Безье.</span><span class="sxs-lookup"><span data-stu-id="199e0-112">The end point of the first Bézier spline is the start point of the second Bézier spline.</span></span>


```
Point p[] = {
   Point(10, 100),   // start point of first spline
   Point(75, 10),    // first control point of first spline
   Point(80, 50),    // second control point of first spline
   Point(100, 150),  // end point of first spline and 
                     // start point of second spline
   Point(125, 80),   // first control point of second spline
   Point(175, 200),  // second control point of second spline
   Point(200, 80)};  // end point of second spline
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBeziers(&pen, p, 7);
```



<span data-ttu-id="199e0-113">На следующем рисунке показаны Соединенные сплайны и семь точек.</span><span class="sxs-lookup"><span data-stu-id="199e0-113">The following illustration shows the connected splines along with the seven points.</span></span>

![Иллюстрация, показывающая конечные точки и контрольные точки двух линий, совместно использующих одну из конечных точек](images/bezierspline2.png)

 

 



