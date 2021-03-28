---
description: Контуры формируются путем объединения линий, прямоугольников и простых кривых. Взпомним о векторной графике, которые были признаны наиболее полезными для рисования изображений в следующих основных стандартных блоках.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Контуры (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554300"
---
# <a name="paths-gdi"></a>Контуры (GDI+)

Контуры формируются путем объединения линий, прямоугольников и простых кривых. Взпомним [о векторной графике](-gdiplus-overview-of-vector-graphics-about.md) , которые были признаны наиболее полезными для рисования изображений в следующих основных стандартных блоках.

-   Линии
-   Прямоугольники
-   Многоточие
-   Дуги
-   многоугольники
-   Фундаментальные сплайны
-   Сплайны Безье

В Windows GDI+ объект [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) позволяет собрать последовательность этих стандартных блоков в единый блок. Затем вся последовательность линий, прямоугольников, многоугольников и кривых может быть выведена одним вызовом метода [**Graphics::D равпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . На следующем рисунке показан путь, созданный путем объединения линии, дуги, сплайна Безье и фундаментального сплайна.

![Иллюстрация контура, объединяющего линию, дугу, сплайн Безье и фундаментальный сплайн](images/aboutgdip02-art14.png)

Класс [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) предоставляет следующие методы для создания последовательности элементов для рисования: [аддлине](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [аддректангле](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [аддарк](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [аддполигон](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [аддкурве](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (для элементов кардинала) и [аддбезиер](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)). Каждый из этих методов перегружен; то есть каждый метод имеет несколько вариантов с разными списками параметров. Например, один из вариантов метода Аддлине получает четыре целых числа, а другой вариант метода Аддлине получает два объекта [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .

Методы добавления линий, прямоугольников и сплайнов Безье в путь содержат вспомогательные методы, которые добавляют в путь несколько элементов в одном вызове: [аддлинес](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [аддректанглес](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))и [аддбезиерс](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)). Кроме того, метод [аддкурве](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) имеет вспомогательный метод [аддклоседкурве](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), который добавляет замкнутую кривую к контуру.

Чтобы нарисовать контур, необходим объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) и объект [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . Объект **Graphics** предоставляет метод [**Graphics::D равпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) , а объект **Pen** сохраняет атрибуты пути, такие как толщина линии и цвет. Объект **GraphicsPath** сохраняет последовательность линий, прямоугольников и кривых, составляющих путь. Адреса объекта **Pen** и объекта **GraphicsPath** передаются в виде аргументов в метод **Graphics::D равпас** . В следующем примере рисуется контур, состоящий из линии, эллипса и сплайна Безье.


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



На следующем рисунке показан путь.

![Иллюстрация контура, который состоит из линии, эллипса и сплайна Безье](images/aboutgdip02-art15.png)

Помимо добавления линий, прямоугольников и кривых к контуру, можно добавлять пути к контуру. Это позволяет объединять существующие пути для формирования больших и сложных путей. Следующий код добавляет **graphicsPath1** и **graphicsPath2** в **миграфикспас**. Второй параметр метода [**GraphicsPath:: аддпас**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) указывает, подключен ли добавленный путь к существующему пути.


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



В путь можно добавить еще два элемента: строки и круги. Круговая диаграмма является частью внутренней части эллипса. В следующем примере создается контур из дуги, фундаментального сплайна, строки и круговой диаграммы.


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



На следующем рисунке показан путь. Обратите внимание, что путь не обязательно должен быть подключен; Дуга, фундаментальная кривая, строка и круговая диаграмма разделяются.

![Иллюстрация пути, состоящие из отключенных линий: дуги, фундаментального сплайна, строки и круговой диаграммы](images/aboutgdip02-art16.png)

 

 



