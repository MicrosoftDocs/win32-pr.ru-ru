---
description: При заполнении фигуры необходимо передать адрес объекта Brush в один из методов Fill класса Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Рисование с помощью непрозрачных и полупрозрачных кистей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156195"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>Рисование с помощью непрозрачных и полупрозрачных кистей

При заполнении фигуры необходимо передать адрес объекта [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) в один из методов Fill класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Единственным параметром конструктора [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) является объект [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) . Чтобы залить непрозрачную фигуру, следует установить значение альфа-компонента цвета в 255. Чтобы залить полупрозрачную фигуру, установите значение альфа-компонента в интервале от 1 до 254.

При заполнении полупрозрачной фигуры цвет фигуры смешивается с цветами фона. Альфа-компонент указывает, как цвета фигур и фона смешиваются. Альфа-значения рядом с 0 помещают больший вес на цвета фона, а альфа-значения около 255 помещают на цвет фигуры.

В следующем примере рисуется изображение, которое затем заполняется тремя эллипсами, которые перекрывают изображение. Для первого эллипса используется значение альфа-компонента, равное 255, поэтому он непрозрачен. Для второго и третьего эллипсов используется значение альфа-компонента, равное 128, поэтому они полупрозрачные и сквозь эллипсы видно фоновое изображение. Вызов [**Graphics:: сеткомпоситингкуалити**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) приводит к тому, что смешение третьего эллипса выполняется вместе с гаммой коррекцией.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



На следующем рисунке показаны выходные данные предыдущего кода.

![Иллюстрация, показывающая изображение, наложенное тремя эллипсами: один непрозрачный, один немного прозрачный, один очень прозрачный](images/compqualellipse.png)

 

 



