---
description: Одним из свойств класса Graphics является отсеченная область. Вся прорисовка, выполненная данным объектом Graphics, ограничена областью отсечения этого графического объекта. Можно задать отсеченную область, вызвав метод Сетклип.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Обрезка с использованием региона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2569350dd0d25066c42fc8ee102cad76e8e77c425bd075122da2179dd3249c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943904"
---
# <a name="clipping-with-a-region"></a>Обрезка с использованием региона

Одним из свойств класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) является отсеченная область. Вся прорисовка, выполненная данным объектом **Graphics** , ограничена областью отсечения этого **графического** объекта. Можно задать отсеченную область, вызвав метод **сетклип** .

В следующем примере создается путь, состоящий из одного многоугольника. Затем код конструирует регион на основе этого пути. Адрес региона передается методу **сетклип** объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , а затем рисуются две строки.


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



На следующем рисунке показаны обрезанные строки.

![Иллюстрация, демонстрирующая части двух предложений, которые появляются в фигурной форме](images/clip1.png)

 

 



