---
description: 'Можно включить гамма-коррекцию для градиентной кисти, передав значение TRUE методу Пасградиентбруш:: Сетгаммакорректион этой кисти.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Применение гамма-коррекции к градиенту
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156234"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Применение гамма-коррекции к градиенту

Можно включить гамма-коррекцию для градиентной кисти, передав **значение true** методу [**Пасградиентбруш:: сетгаммакорректион**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) этой кисти. Можно отключить гамма-коррекцию, передав **значение false** методу **Пасградиентбруш:: сетгаммакорректион** . По умолчанию гамма-коррекция отключена.

В следующем примере создается кисть линейного градиента и используется эта кисть для заливки двух прямоугольников. Первый прямоугольник заполняется без гамма-коррекции, а второй прямоугольник заполняется гаммой-коррекцией.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



На следующем рисунке показаны два закрашенных прямоугольника. Верхний прямоугольник, который не имеет гамма-коррекции, отображается темным в середине. Нижний прямоугольник, в котором имеется гамма-коррекция, имеет более однородную интенсивность.

![Иллюстрация, демонстрирующая два прямоугольника: цвет заливки первого цвета зависит от интенсивности, заливка второго — меньше](images/gammagradient1.png)

В следующем примере создается кисть градиента контура на основе траектории в форме звезды. Код использует кисть градиента вдоль пути с отключенной коррекцией гаммы (по умолчанию) для заполнения пути. Затем код передает **значение true** методу [**Пасградиентбруш:: сетгаммакорректион**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) , чтобы включить гамма-коррекцию для кисти градиента вдоль пути. Вызов [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) устанавливает универсальное преобразование [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта таким образом, что последующий вызов [**Graphics:: филлпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) заполняет звезду, расположенную справа от первой звезды.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



На следующем рисунке показаны выходные данные предыдущего кода. Звездочка справа имеет гамма-коррекцию. Обратите внимание, что звездочка слева, не имеющая гамма-коррекции, содержит области, которые выглядят темными.

![Иллюстрация 2 5, на которую указывает, начинается с цветной градиентной заливки; Первый имеет темные области, второй — нет.](images/gammagradient2.png)

 

 



