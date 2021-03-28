---
description: Обрезка включает в себя ограничения рисования в определенном регионе. На следующем рисунке показана строка &\# 0034; Привет&\# 0034; обрезаны до области в форме сердца.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Обрезка (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080639"
---
# <a name="clipping-gdi"></a>Обрезка (GDI+)

Обрезка включает в себя ограничения рисования в определенном регионе. На следующем рисунке показана строка "Hello", обрезанная до области в форме сердца.

![Иллюстрация, демонстрирующая части строки "Hello" в красном сердце](images/aboutgdip02-art30.png)

Регионы можно создавать на основе контуров, а пути могут содержать контуры строк, поэтому для обрезки можно использовать обрезку текста. На следующем рисунке показан набор концентрических эллипсов, обрезанных по внутренней части строки текста.

![Иллюстрация, показывающая строку "Hello", заполненную шаблоном концентрических кругов](images/aboutgdip02-art31.png)

Чтобы рисовать с помощью обрезки, создайте объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , вызовите его метод [сетклип](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) , а затем вызовите методы рисования такого же **графического** объекта. В следующем примере рисуется линия, обрезанная до прямоугольной области.


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



На следующем рисунке показана прямоугольная область вместе с обрезанной линией.

![Иллюстрация, демонстрирующая прямоугольник с диагональным линиям сверху вниз](images/aboutgdip02-art31a.png)

 

 



