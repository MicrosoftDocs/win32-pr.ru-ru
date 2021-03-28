---
description: Преобразование «мир» является свойством класса Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Использование объемного преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263045"
---
# <a name="using-the-world-transformation"></a>Использование объемного преобразования

Преобразование «мир» является свойством класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Числа, определяющие объемное преобразование, хранятся в объекте [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , который представляет матрицу размером 3 × 3. Классы **Matrix** и **Graphics** имеют несколько методов для настройки чисел в матрице универсального преобразования. Примеры в этом разделе посвящены управлению прямоугольниками, так как прямоугольники легко изображать, и можно легко увидеть влияние преобразований на прямоугольники.

Начнем с создания прямоугольника 50 на 50 и нахождения его в источнике (0, 0). Источник находится в левом верхнем углу клиентской области.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



Следующий код применяет преобразование масштабирования, которое расширяет прямоугольник с коэффициентом 1,75 в направлении x и сжимает прямоугольник на множители 0,5 в направлении по оси y:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



Результатом является прямоугольник, который больше в направлении x и короче по оси y, чем у оригинала.

Чтобы повернуть прямоугольник вместо его масштабирования, используйте следующий код вместо приведенного выше кода:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



Чтобы преобразовать прямоугольник, используйте следующий код:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



