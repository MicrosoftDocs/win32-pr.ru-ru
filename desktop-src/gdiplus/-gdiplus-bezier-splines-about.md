---
description: 'A B&\# 233; сплайн Безье — это кривая, определяемая четырьмя точками: две конечные точки (P1 и P2) и две контрольные точки (C1 и C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Сплайны Безье
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156231"
---
# <a name="bezier-splines"></a><span data-ttu-id="81c07-103">Сплайны Безье</span><span class="sxs-lookup"><span data-stu-id="81c07-103">Bezier Splines</span></span>

<span data-ttu-id="81c07-104">Сплайн Безье — это кривая, определяемая четырьмя точками: две конечные точки (P1 и P2) и две контрольные точки (C1 и C2).</span><span class="sxs-lookup"><span data-stu-id="81c07-104">A Bézier spline is a curve specified by four points: two end points (p1 and p2) and two control points (c1 and c2).</span></span> <span data-ttu-id="81c07-105">Кривая начинается с P1 и заканчивается в P2.</span><span class="sxs-lookup"><span data-stu-id="81c07-105">The curve begins at p1 and ends at p2.</span></span> <span data-ttu-id="81c07-106">Кривая не проходит через контрольные точки, но контрольные точки действуют как магнитные линии, изменяя кривую в определенных направлениях и изменяя способ изгиба кривой.</span><span class="sxs-lookup"><span data-stu-id="81c07-106">The curve doesn't pass through the control points, but the control points act as magnets, pulling the curve in certain directions and influencing the way the curve bends.</span></span> <span data-ttu-id="81c07-107">На следующем рисунке показана кривая Безье, а также ее конечные точки и контрольные точки.</span><span class="sxs-lookup"><span data-stu-id="81c07-107">The following illustration shows a Bézier curve along with its endpoints and control points.</span></span>

![Иллюстрация, демонстрирующая сплайн Безье с двумя конечными точками и двумя контрольными точками](images/aboutgdip02-art11a.png)

<span data-ttu-id="81c07-109">Обратите внимание, что кривая начинается с P1 и перемещается к точке управления C1.</span><span class="sxs-lookup"><span data-stu-id="81c07-109">Note that the curve starts at p1 and moves toward the control point c1.</span></span> <span data-ttu-id="81c07-110">Касательная к кривой в P1 равна линии, нарисованной из P1 в C1.</span><span class="sxs-lookup"><span data-stu-id="81c07-110">The tangent line to the curve at p1 is the line drawn from p1 to c1.</span></span> <span data-ttu-id="81c07-111">Также обратите внимание, что касательная в конечной точке p2 является линией, нарисованной из C2 в P2.</span><span class="sxs-lookup"><span data-stu-id="81c07-111">Also note that the tangent line at the endpoint p2 is the line drawn from c2 to p2.</span></span>

<span data-ttu-id="81c07-112">Чтобы нарисовать сплайн Безье, необходим объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="81c07-112">To draw a Bézier spline, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="81c07-113">Объект **Graphics** предоставляет метод [дравбезиер](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) , а объект **Pen** сохраняет атрибуты кривой, например толщину и цвет линии.</span><span class="sxs-lookup"><span data-stu-id="81c07-113">The **Graphics** object provides the [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) method, and the **Pen** object stores attributes of the curve, such as line width and color.</span></span> <span data-ttu-id="81c07-114">Адрес объекта **Pen** передается в метод дравбезиер в качестве одного из аргументов.</span><span class="sxs-lookup"><span data-stu-id="81c07-114">The address of the **Pen** object is passed as one of the arguments to the DrawBezier method.</span></span> <span data-ttu-id="81c07-115">Остальные аргументы, передаваемые в метод Дравбезиер, являются конечными точками и контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="81c07-115">The remaining arguments passed to the DrawBezier method are the endpoints and the control points.</span></span> <span data-ttu-id="81c07-116">В следующем примере рисуется сплайн Безье с начальной точкой (0, 0), контрольными точками (40, 20) и (80, 150) и конечной точкой (100, 10).</span><span class="sxs-lookup"><span data-stu-id="81c07-116">The following example draws a Bézier spline with starting point (0, 0), control points (40, 20) and (80, 150), and ending point (100, 10).</span></span>


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



<span data-ttu-id="81c07-117">На следующем рисунке показана кривая, контрольные точки и две касательные линии.</span><span class="sxs-lookup"><span data-stu-id="81c07-117">The following illustration shows the curve, the control points, and two tangent lines.</span></span>

![Иллюстрация, демонстрирующая сплайн Безье с двумя конечными точками, двумя контрольными точками и двумя касательными](images/aboutgdip02-art12.png)

<span data-ttu-id="81c07-119">Сплайны Безье изначально разрабатывались Пьером Безье для проектирования в индустрии автомобильных отраслей.</span><span class="sxs-lookup"><span data-stu-id="81c07-119">Bézier splines were originally developed by Pierre Bézier for design in the automotive industry.</span></span> <span data-ttu-id="81c07-120">Так как они были очень полезны для множества типов автоматизированного проектирования, они также используются для определения контуров шрифтов.</span><span class="sxs-lookup"><span data-stu-id="81c07-120">They have since proven to be very useful in many types of computer-aided design and are also used to define the outlines of fonts.</span></span> <span data-ttu-id="81c07-121">Сплайны Безье могут выдавать разнообразные фигуры, некоторые из которых показаны на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="81c07-121">Bézier splines can yield a wide variety of shapes, some of which are shown in the following illustration.</span></span>

![Иллюстрация, демонстрирующая три сплайна Безье](images/aboutgdip02-art13.png)

 

 



