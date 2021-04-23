---
description: Чтобы создать путь, создайте объект GraphicsPath, а затем вызовите методы, такие как Аддлине и Аддкурве, чтобы добавить к пути примитивы.
ms.assetid: 66faeb73-16fb-4b7f-a4d5-a90ec2590d8c
title: Создание геометрических объектов из линий, кривых и фигур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c473dfececcaa86347dc02efdfd62131eb9a63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991642"
---
# <a name="creating-figures-from-lines-curves-and-shapes"></a><span data-ttu-id="cec22-103">Создание геометрических объектов из линий, кривых и фигур</span><span class="sxs-lookup"><span data-stu-id="cec22-103">Creating Figures from Lines, Curves, and Shapes</span></span>

<span data-ttu-id="cec22-104">Чтобы создать путь, создайте объект [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) , а затем вызовите методы, такие как [аддлине](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) и [аддкурве](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), чтобы добавить к пути примитивы.</span><span class="sxs-lookup"><span data-stu-id="cec22-104">To create a path, construct a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object, and then call methods, such as [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) and [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), to add primitives to the path.</span></span>

<span data-ttu-id="cec22-105">В следующем примере создается путь с одной дугой. Дуга имеет угол поворота – 180 градусов, который в системе координат по умолчанию имеет значение против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="cec22-105">The following example creates a path that has a single arc. The arc has a sweep angle of –180 degrees, which is counterclockwise in the default coordinate system.</span></span>


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="cec22-106">В следующем примере создается путь с двумя рисунками.</span><span class="sxs-lookup"><span data-stu-id="cec22-106">The following example creates a path that has two figures.</span></span> <span data-ttu-id="cec22-107">Первый рисунок — это дуга, за которой следует строка.</span><span class="sxs-lookup"><span data-stu-id="cec22-107">The first figure is an arc followed by a line.</span></span> <span data-ttu-id="cec22-108">Второй рисунок — это строка, за которой следует кривая, за которой следует строка.</span><span class="sxs-lookup"><span data-stu-id="cec22-108">The second figure is a line followed by a curve, followed by a line.</span></span> <span data-ttu-id="cec22-109">Первая фигура остается открытой, а вторая — закрытой.</span><span class="sxs-lookup"><span data-stu-id="cec22-109">The first figure is left open, and the second figure is closed.</span></span>


```
Point points[] = {Point(40, 60), Point(50, 70), Point(30, 90)};

Pen pen(Color(255, 255, 0, 0), 2);
GraphicsPath path;

// The first figure is started automatically, so there is
// no need to call StartFigure here.
path.AddArc(175, 50, 50, 50, 0.0f, -180.0f);
path.AddLine(100, 0, 250, 20);

path.StartFigure();
path.AddLine(50, 20, 5, 90);
path.AddCurve(points, 3);
path.AddLine(50, 150, 150, 180);
path.CloseFigure();

graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="cec22-110">Помимо добавления линий и кривых к контурам, можно добавлять замкнутые фигуры: прямоугольники, эллипсы, круги и многоугольники.</span><span class="sxs-lookup"><span data-stu-id="cec22-110">In addition to adding lines and curves to paths, you can add closed shapes: rectangles, ellipses, pies, and polygons.</span></span> <span data-ttu-id="cec22-111">В следующем примере создается контур с двумя линиями, прямоугольником и эллипсом.</span><span class="sxs-lookup"><span data-stu-id="cec22-111">The following example creates a path that has two lines, a rectangle, and an ellipse.</span></span> <span data-ttu-id="cec22-112">Код использует перо для рисования контура и кисти для заполнения пути.</span><span class="sxs-lookup"><span data-stu-id="cec22-112">The code uses a pen to draw the path and a brush to fill the path.</span></span>


```
GraphicsPath path;
Pen          pen(Color(255, 255, 0, 0), 2);
SolidBrush   brush(Color(255, 0, 0, 200));

path.AddLine(10, 10, 100, 40);
path.AddLine(100, 60, 30, 60);
path.AddRectangle(Rect(50, 35, 20, 40));
path.AddEllipse(10, 75, 40, 30);

graphics.DrawPath(&pen, &path);
graphics.FillPath(&brush, &path);
```



<span data-ttu-id="cec22-113">Путь в предыдущем примере содержит три цифры.</span><span class="sxs-lookup"><span data-stu-id="cec22-113">The path in the preceding example has three figures.</span></span> <span data-ttu-id="cec22-114">Первая фигура состоит из двух строк, вторая фигура состоит из прямоугольника, а третья фигура состоит из эллипса.</span><span class="sxs-lookup"><span data-stu-id="cec22-114">The first figure consists of the two lines, the second figure consists of the rectangle, and the third figure consists of the ellipse.</span></span> <span data-ttu-id="cec22-115">Даже если нет вызовов [**GraphicsPath:: клосефигуре**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) или [**GraphicsPath:: стартфигуре**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), внутренние замкнутые фигуры, такие как прямоугольники и эллипсы, считаются отдельными цифрами.</span><span class="sxs-lookup"><span data-stu-id="cec22-115">Even when there are no calls to [**GraphicsPath::CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) or [**GraphicsPath::StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), intrinsically closed shapes, such as rectangles and ellipses, are considered separate figures.</span></span>

 

 



