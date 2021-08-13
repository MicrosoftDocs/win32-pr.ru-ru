---
description: для рисования линий с Windows GDI+ необходимо создать графический объект и объект Pen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Перья, линии и прямоугольники
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ac54d1e98a617492aa6f5f1194767fc56a34ffcaaee71ba71753dda08f8bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359594"
---
# <a name="pens-lines-and-rectangles"></a>Перья, линии и прямоугольники

для рисования линий с Windows GDI+ необходимо создать [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Объект **Graphics** предоставляет методы, которые на самом деле выполняют рисование, а объект **Pen** сохраняет атрибуты линии, такие как цвет, ширина и стиль. Рисование линии — это просто вопрос вызова метода [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) объекта **Graphics** . Адрес объекта **Pen** передается в качестве одного из аргументов метода DrawLine. В следующем примере рисуется линия с точки (4, 2) до точки (12, 6).


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



Метод [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) является перегруженным методом класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , поэтому существует несколько способов указать его с аргументами. Например, можно создать два объекта [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) и передать ссылки на объекты **Point** в качестве аргументов метода DrawLine.


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



При создании объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) можно указать определенные атрибуты. Например, один конструктор [пера](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) позволяет указать цвет и ширину. В следующем примере рисуется синяя линия толщины 2 из (0, 0) до (60, 30).


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



Объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) также имеет атрибуты, например тип штриха, который можно использовать для указания характеристик линии. Например, в следующем примере пунктирная линия рисуется от (100, 50) до (300, 80).


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



Можно использовать различные методы объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) для задания множества дополнительных атрибутов линии. Методы [**Pen:: сетстарткап**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) и [**Pen:: сетендкап**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) определяют внешний вид концов линии. конечными элементами могут быть плоские, квадратные, скругленные, треугольные или пользовательские фигуры. Метод [**Pen:: сетлинежоин**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) позволяет указать, будут ли Соединенные линии отсечены друг от друга (соединены с острыми углами), рельефными, скругленными или обрезанными. На следующем рисунке показаны линии с различными стилями крепления и объединения.

![Иллюстрация двух линий, демонстрирующих скругленные и круговые концы, скругленные и угловые углы и две стили стрелок](images/aboutgdip02-art04.png)

рисование прямоугольников с помощью GDI+ похоже на рисование линий. Чтобы нарисовать прямоугольник, необходим [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Объект **Graphics** предоставляет метод [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) , а объект **Pen** сохраняет атрибуты, такие как толщина линии и цвет. Адрес объекта **Pen** передается в метод DrawRectangle в качестве одного из аргументов. В следующем примере показано рисование прямоугольника с верхним левым углом в (100, 50), шириной 80 и высотой 40.


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) является перегруженным методом класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , поэтому его можно указать с помощью аргументов. Например, можно создать объект [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) и передать ссылку на объект **Rect** в качестве аргумента в метод DrawRectangle.


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



Объект [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) имеет методы для управления и сбора сведений об прямоугольнике. Например, методы [Deflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) и [offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) изменяют размер и расположение прямоугольника. Метод [**Rect:: интерсектсвис**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) указывает, пересекается ли прямоугольник с другим заданным прямоугольником, а метод [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) сообщает, находится ли заданная точка внутри прямоугольника.

 

 
