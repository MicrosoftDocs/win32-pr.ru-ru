---
description: 'На следующем рисунке показаны две кривые: одна открытая и одна закрытая.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Незамкнутые и замкнутые кривые
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383f7c68909a73291c00c6e760d1cc6554b061d5749b33e6e90ba3a986c71906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885129"
---
# <a name="open-and-closed-curves"></a>Незамкнутые и замкнутые кривые

На следующем рисунке показаны две кривые: одна открытая и одна закрытая.

![Иллюстрация открытой кривой (изогнутая линия) и замкнутой кривой (контур фигуры)](images/aboutgdip02-art24.png)

Замкнутые кривые имеют внутреннее пространство, поэтому их можно заполнить кистью. класс [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) в Windows GDI+ предоставляет следующие методы заполнения замкнутых фигур и кривых: [филлректангле](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [филлеллипсе](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [филлпие](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [филлполигон](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [филлклоседкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics:: филлпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)и [**Graphics:: филлрегион**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion). При каждом вызове одного из этих методов необходимо передать в качестве аргумента адрес одного из конкретных типов кисти ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**хатчбруш**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)или [**пасградиентбруш**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)).

Метод [филлпие](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) является вспомогательным для метода [драварк](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) . Точно так же, как метод Драварк рисует часть контура эллипса, метод Филлпие заполняет часть внутренней части эллипса. В следующем примере рисуется дуга и заполняется соответствующая часть внутри эллипса.


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



На следующем рисунке показана дуга и заполненная круговая диаграмма.

![Иллюстрация, показывающая сегмент закрашенного эллипса](images/aboutgdip02-art25.png)

Метод [филлклоседкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) является вспомогательным для метода [дравклоседкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) . Оба метода автоматически закрывают кривую, подключив конечную точку к начальной точке. В следующем примере рисуется кривая, которая проходит через (0, 0), (60, 20) и (40, 50). Затем кривая автоматически закрывается путем подключения (40, 50) к начальной точке (0, 0), а внутренняя часть заполняется сплошным цветом.


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



Путь может состоять из нескольких иллюстраций (подконтуров). Метод [**Graphics:: филлпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) заполняет внутреннюю часть каждой фигуры. Если фигура не закрыта, метод **Graphics:: филлпас** заполняет область, которая будет заключена, если фигура была закрыта. В следующем примере рисуется и заполняется контур, состоящий из дуги, фундаментального сплайна, строки и круговой диаграммы.


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



На следующем рисунке показан путь до и после заполнения сплошной кистью. Обратите внимание, что текст в строке имеет контур, но не заполняется методом [**Graphics::D равпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) . Это метод [**Graphics:: филлпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) , который закрашивает внутренние части символов в строке.

![Иллюстрация, на которой дважды отображается текст, а также открытая и замкнутая кривая; они пусты и заполняются второй раз.](images/aboutgdip02-art26.png)

 

 



