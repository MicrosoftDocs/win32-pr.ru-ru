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
# <a name="creating-figures-from-lines-curves-and-shapes"></a>Создание геометрических объектов из линий, кривых и фигур

Чтобы создать путь, создайте объект [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) , а затем вызовите методы, такие как [аддлине](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) и [аддкурве](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), чтобы добавить к пути примитивы.

В следующем примере создается путь с одной дугой. Дуга имеет угол поворота – 180 градусов, который в системе координат по умолчанию имеет значение против часовой стрелки.


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



В следующем примере создается путь с двумя рисунками. Первый рисунок — это дуга, за которой следует строка. Второй рисунок — это строка, за которой следует кривая, за которой следует строка. Первая фигура остается открытой, а вторая — закрытой.


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



Помимо добавления линий и кривых к контурам, можно добавлять замкнутые фигуры: прямоугольники, эллипсы, круги и многоугольники. В следующем примере создается контур с двумя линиями, прямоугольником и эллипсом. Код использует перо для рисования контура и кисти для заполнения пути.


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



Путь в предыдущем примере содержит три цифры. Первая фигура состоит из двух строк, вторая фигура состоит из прямоугольника, а третья фигура состоит из эллипса. Даже если нет вызовов [**GraphicsPath:: клосефигуре**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) или [**GraphicsPath:: стартфигуре**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), внутренние замкнутые фигуры, такие как прямоугольники и эллипсы, считаются отдельными цифрами.

 

 



