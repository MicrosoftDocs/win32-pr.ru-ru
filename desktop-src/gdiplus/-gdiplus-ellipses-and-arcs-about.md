---
description: С ограничивающим прямоугольником задается эллипс. На следующем рисунке показан эллипс, а также его ограничивающий прямоугольник.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Эллипсы и дуги
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadd0a34107681d2d155ead5d4f80b7208b8926603f21fa4541d502886edaf73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036752"
---
# <a name="ellipses-and-arcs"></a>Эллипсы и дуги

С ограничивающим прямоугольником задается эллипс. На следующем рисунке показан эллипс, а также его ограничивающий прямоугольник.

![Иллюстрация эллипса, заключенного в ограничивающем прямоугольнике](images/aboutgdip02-art05.png)

Чтобы нарисовать эллипс, необходим объект [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и объект [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . Объект **Graphics** предоставляет метод [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , а объект **Pen** сохраняет атрибуты эллипса, например толщину и цвет линии. Адрес объекта **Pen** передается в качестве одного из аргументов в метод DrawEllipse. Остальные аргументы, передаваемые в метод DrawEllipse, задают ограничивающий прямоугольник для эллипса. В следующем примере рисуется эллипс; ограничивающий прямоугольник имеет ширину 160, высоту 80 и левый верхний угол (100, 50).


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



Метод [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) является перегруженным методом класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , поэтому существует несколько способов указать его с аргументами. Например, можно создать объект [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) и передать ссылку на объект **Rect** в качестве аргумента в метод DrawEllipse.


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



Дуга — это часть эллипса. Чтобы нарисовать дугу, вызовите метод [драварк](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Параметры метода Драварк совпадают с параметрами метода [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , за исключением того, что драварк требует начальный угол и угол поворота. В следующем примере демонстрируется рисование дуги с начальным углом 30 градусов и углом поворота в 180 градусов.


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



На следующем рисунке показана дуга, эллипс и ограничивающий прямоугольник.

![Иллюстрация эллипса в ограничивающем прямоугольнике; Нижняя левая половина эллипса отображается красным цветом](images/aboutgdip02-art06.png)

 

 



