---
description: Фундаментальный сплайн — это кривая, которая плавно проходит через заданный набор точек.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Рисование фундаментальных сплайнов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c780cb4486f579acb57170a8eda4fd187a421ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558248"
---
# <a name="drawing-cardinal-splines"></a><span data-ttu-id="be139-103">Рисование фундаментальных сплайнов</span><span class="sxs-lookup"><span data-stu-id="be139-103">Drawing Cardinal Splines</span></span>

<span data-ttu-id="be139-104">Фундаментальный сплайн — это кривая, которая плавно проходит через заданный набор точек.</span><span class="sxs-lookup"><span data-stu-id="be139-104">A cardinal spline is a curve that passes smoothly through a given set of points.</span></span> <span data-ttu-id="be139-105">Чтобы нарисовать фундаментальный сплайн, создайте объект [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и передайте адрес массива точек в метод [**Graphics::D равкурве**](/previous-versions//ms536070(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="be139-105">To draw a cardinal spline, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass the address of an array of points to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="be139-106">В следующем примере рисуется замкнутая в форме фундаментальная кривая, которая проходит через пять указанных точек:</span><span class="sxs-lookup"><span data-stu-id="be139-106">The following example draws a bell-shaped cardinal spline that passes through five designated points:</span></span>


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



<span data-ttu-id="be139-107">На следующем рисунке показана кривая и пять точек.</span><span class="sxs-lookup"><span data-stu-id="be139-107">The following illustration shows the curve and five points.</span></span>

![Иллюстрация фундаментального сплайна, проходящего через набор из пяти пунктов](images/cardinalspline1.png)

<span data-ttu-id="be139-109">Для рисования замкнутого фундаментального сплайна можно использовать метод [**Graphics::D равклоседкурве**](/previous-versions//ms536143(v=vs.85)) класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="be139-109">You can use the [**Graphics::DrawClosedCurve**](/previous-versions//ms536143(v=vs.85)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a closed cardinal spline.</span></span> <span data-ttu-id="be139-110">В замкнутом фундаментальном сплайне кривая просматривается до последней точки в массиве и соединяется с первой точкой массива.</span><span class="sxs-lookup"><span data-stu-id="be139-110">In a closed cardinal spline, the curve continues through the last point in the array and connects with the first point in the array.</span></span>

<span data-ttu-id="be139-111">В следующем примере рисуется замкнутый фундаментальный сплайн, проходящий через шесть указанных точек.</span><span class="sxs-lookup"><span data-stu-id="be139-111">The following example draws a closed cardinal spline that passes through six designated points.</span></span>


```
Point points[] = {Point(60, 60),
   Point(150, 80),
   Point(200, 40),
   Point(180, 120),
   Point(120, 100),
   Point(80, 160)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawClosedCurve(&pen, points, 6);
```



<span data-ttu-id="be139-112">На следующем рисунке показан замкнутый сплайн вместе с шестью точками:</span><span class="sxs-lookup"><span data-stu-id="be139-112">The following illustration shows the closed spline along with the six points:</span></span>

![Иллюстрация замкнутой фундаментальной сплайна, проходящей через набор из шести точек](images/cardinalspline1a.png)

<span data-ttu-id="be139-114">Можно изменить способ изгиба фундаментального сплайна, передав аргумент натяжения в метод [**Graphics::D равкурве**](/previous-versions//ms536070(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="be139-114">You can change the way a cardinal spline bends by passing a tension argument to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="be139-115">В следующем примере рисуются три фундаментальных сплайна, которые проходят через один и тот же набор точек:</span><span class="sxs-lookup"><span data-stu-id="be139-115">The following example draws three cardinal splines that pass through the same set of points:</span></span>


```
Point points[] = {Point(20, 50),
                  Point(100, 10),
                  Point(200, 100),
                  Point(300, 50),
                  Point(400, 80)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5, 0.0f);  // tension 0.0
graphics.DrawCurve(&pen, points, 5, 0.6f);  // tension 0.6
graphics.DrawCurve(&pen, points, 5, 1.0f);  // tension 1.0
```



<span data-ttu-id="be139-116">На следующем рисунке показаны три сплайна, а также их значения натяжения.</span><span class="sxs-lookup"><span data-stu-id="be139-116">The following illustration shows the three splines along with their tension values.</span></span> <span data-ttu-id="be139-117">Обратите внимание, что если натяжение равно 0, точки соединяются прямыми линиями.</span><span class="sxs-lookup"><span data-stu-id="be139-117">Note that when the tension is 0, the points are connected by straight lines.</span></span>

![Иллюстрация трех фундаментальных линий, передаваемых через один набор точек, но с разными натяжениями](images/cardinalspline2.png)

 

 
