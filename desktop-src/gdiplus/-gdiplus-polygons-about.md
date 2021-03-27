---
description: Многоугольник — это замкнутая фигура с тремя или более прямыми сторонами.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: многоугольники
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809640"
---
# <a name="polygons"></a>многоугольники

Многоугольник — это замкнутая фигура с тремя или более прямыми сторонами. Например, треугольником является многоугольник с тремя сторонами, прямоугольник — многоугольник с четырьмя сторонами, а пятиугольник — многоугольник с пятью сторонами. На следующем рисунке показаны несколько многоугольников.

![Иллюстрация, демонстрирующая пять многоугольников различных фигур, размеров и цветов](images/aboutgdip02-art07.png)

Чтобы нарисовать многоугольник, необходим [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект, объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) и массив объектов [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (или [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)). Объект **Graphics** предоставляет метод [дравполигон](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) . Объект **Pen** сохраняет атрибуты многоугольника, такие как ширина и цвет линии, а массив объектов **Point** хранит точки, которые должны быть соединены прямыми линиями. Адреса объекта **Pen** и массива объектов **Point** передаются в качестве аргументов в метод дравполигон. В следующем примере рисуется трехмерный многоугольник. Обратите внимание, что в **мипоинтаррай** есть только три точки: (0, 0), (50, 30) и (30, 60). Метод Дравполигон автоматически закрывает многоугольник, рисуя строку из (30, 60) обратно в начальную точку (0, 0);


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



На следующем рисунке показан многоугольник.

![Иллюстрация, демонстрирующая треугольник относительно осей координат](images/aboutgdip02-art08.png)

 

 



