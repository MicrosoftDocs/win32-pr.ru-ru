---
description: Windows GDI+ рисует линии, прямоугольники и другие фигуры в системе координат.
ms.assetid: a43bcb27-473b-4ca2-a937-2b54384ab86b
title: Обзор векторной графики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33566b5d1d683c87ea1f6858abcc6ae375ce09b71e0ac74711118e92bca656c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695662"
---
# <a name="overview-of-vector-graphics"></a>Обзор векторной графики

Windows GDI+ рисует линии, прямоугольники и другие фигуры в системе координат. Вы можете выбрать одну из различных систем координат, но в верхнем левом углу система координат по умолчанию имеет точку, указывающую вправо и ось y. Единицей измерения в системе координат по умолчанию является пиксель.

![Иллюстрация системы координат с осью x, расположенной справа, и оси y, которая расширяется вниз](images/aboutgdip02-art01.png)

Монитор компьютера создает свой экран на прямоугольном массиве точек, называемых элементами изображения или пикселами. Количество пикселов, отображаемых на экране, меняется от одного монитора к другому, а количество пикселов, отображаемых на отдельном мониторе, обычно может быть настроено пользователем в некоторой степени.

![Иллюстрация прямоугольной сетки с тремя ячейками в этой сетке, обозначенными их координатами](images/aboutgdip02-art02.png)

при использовании GDI+ для рисования линии, прямоугольника или кривой вы предоставляете определенную ключевую информацию о рисуемом элементе. Например, можно указать строку, указав две точки, и прямоугольник можно указать, указав точку, высоту и ширину. GDI+ работает совместно с программным обеспечением драйвера экрана, чтобы определить, какие пикселы должны быть включены для отображения линии, прямоугольника или кривой. На следующем рисунке показаны пиксели, включенные для отображения линии с точки (4, 2) до точки (12, 8).

![Иллюстрация, демонстрирующая прямоугольную сетку с ячейками, заполненными для обозначения линии между двумя конечными точками](images/aboutgdip02-art03.png)

Со временем некоторые основные стандартные блоки были признаны наиболее полезными для создания двумерных изображений. эти стандартные блоки, которые поддерживаются GDI+, приведены в следующем списке:

-   Линии
-   Прямоугольники
-   Многоточие
-   Дуги
-   многоугольники
-   Фундаментальные сплайны
-   Сплайны Безье

класс [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) в GDI+ предоставляет следующие методы для рисования элементов в предыдущем списке: [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)), [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_)), [дравполигон](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpointf_inint)), [драварк](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)), [дравкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) (для элементов кардинала) и [дравбезиер](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpoint__inconstpoint__inconstpoint__inconstpoint_)). Каждый из этих методов перегружен; то есть каждый метод имеет несколько вариантов с разными списками параметров. Например, один из вариантов метода DrawLine получает адрес объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) и четыре целых числа, тогда как другой вариант метода DrawLine получает адрес объекта **Pen** и две ссылки на объект [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .

Методы рисования линий, прямоугольников и сплайнов Безье содержат вспомогательные методы, которые рисуют несколько элементов в одном вызове: [дравлинес](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpointf_inint)), [дравректанглес](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint))и [дравбезиерс](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)). Кроме того, метод [дравкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) имеет вспомогательный метод [дравклоседкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)), который закрывает кривую, подключив конечную точку кривой к начальной точке.

Все методы рисования класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) работают совместно с объектом [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Таким образом, чтобы нарисовать что угодно, необходимо создать по крайней мере два объекта: **графический** объект и объект **Pen** . Объект **Pen** сохраняет атрибуты рисуемого элемента, например толщину и цвет линии. Адрес объекта **Pen** передается в качестве одного из аргументов метода рисования. Например, один из вариантов метода [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) получает адрес объекта **Pen** и четыре целых числа, как показано в следующем коде, который рисует прямоугольник с шириной 100, высотой 50 и верхним левым углом (20, 10).


```
myGraphics.DrawRectangle(&myPen, 20, 10, 100, 50);
```



 

 



