---
description: В этом примере показаны два метода поиска рукописного ввода по заданному положению экрана.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Пример проверки нажатия рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710990"
---
# <a name="ink-hit-test-sample"></a>Пример проверки нажатия рукописного ввода

В этом примере показаны два метода поиска рукописного ввода по заданному положению экрана.

В этом примере используются следующие функции.

-   Использование сборщика рукописных данных
-   Выполнение проверки нажатия
-   Поиск ближайшей точки

## <a name="accessing-the-ink-api"></a>Доступ к API рукописного ввода

Во-первых, сослаться на классы планшетных ПК, которые находятся в пакете SDK для Windows Vista или Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>Обработка событий загрузки и рисования форм

Обработчик событий загрузки формы:

-   Создает объект [InkCollector](/previous-versions/ms583683(v=vs.100)) (IC) для формы.
-   Задает для свойства [режиме CollectionMode](/previous-versions/ms836497(v=msdn.10)) объекта [InkCollector](/previous-versions/ms583683(v=vs.100)) игнорирование жестов.
-   Включает объект [InkCollector](/previous-versions/ms583683(v=vs.100)).
-   Задает для свойства [ауторедрав](/previous-versions/ms836495(v=msdn.10)) объекта [InkCollector](/previous-versions/ms583683(v=vs.100)) **значение true**.


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



Обработчик событий Paint формы проверяет режим приложения:

-   В режиме HitTest он рисует окружность вокруг курсора. Активное перо задается в методе Хандлехиттест приложения.
-   В режиме Неарестпоинт он рисует красную линию между курсором и точкой, ближайшей к курсору. Ближайшая точка вычисляется в методе Хандленеарестпоинт приложения.


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



Этот пример имеет очень простой алгоритм перерисовки. Если свойство [ауторедрав](/previous-versions/ms836495(v=msdn.10)) имеет значение **true**, сборщик рукописного ввода перерисовывается при перерисовке формы. Чтобы упростить перерисовку формы, приложение отслеживает ограничивающий прямоугольник, переменную-член Инвалидатерект, для области, в которую добавляется Paint, которая становится недействительной при каждом перерисовке формы.

## <a name="handling-menu-events"></a>Обработка событий меню

Команда exit отключает объект [InkCollector](/previous-versions/ms583683(v=vs.100)) перед выходом из приложения.

Команда рукописного ввода обновляет состояние режима приложения и меню, включает сборщик рукописных данных и делает недействительным закрашиваемую область формы.

Команды проверки попадания и ближайших точек изменяют курсор, обновляют режим приложения и состояние меню, отключают сборщик рукописных данных и делают недействительными ранее закрашиваемую область формы.

Очистка! команда отключает [InkCollector](/previous-versions/ms583683(v=vs.100)) , заменяя свойство [рукописного ввода](/previous-versions/ms836505(v=msdn.10)) объекта InkCollector новым объектом [рукописного ввода](/previous-versions/ms571716(v=vs.100)) , создает событие команды рукописного ввода и принудительно выполняет обновление элемента управления.

## <a name="handling-mouse-events"></a>Обработка событий мыши

Обработчик событий [MouseMove](/previous-versions/ms567617(v=vs.100)) проверяет режим приложения:

-   В режиме рукописного ввода ничего не делает, позволяя обычным образом собирать рукописные данные с помощью сборщика рукописных данных.
-   В режиме HitTest он отправляет аргументы события в метод Хандлехиттест приложения.
-   В режиме Неарестпоинт он отправляет аргументы события в метод Хандленеарестпоинт приложения.

## <a name="performing-a-hit-test"></a>Выполнение проверки нажатия

Метод Хандлехиттест приложения создает две точки: положение курсора и точку Хитсизе Пиксели, удаленные от курсора, а затем преобразует эти две точки из пикселов в координаты рукописного пространства.


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



Затем объект [InkCollector](/previous-versions/ms583683(v=vs.100)) использует метод [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) для поиска штрихов, находящихся в PT3. X-PT2. Единицы измерения позиции курсора по оси X, PT2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



Затем метод Хандлехиттест задает цвет пера на основе того, были ли обнаружены штрихи, делает недействительным Инвалидатерект область, вычисляет новый регион, в котором рисуется окружность проверки нажатия, а затем делает недействительным новый регион.

## <a name="locating-the-nearest-point"></a>Поиск ближайшей точки

Метод Хандленеарестпоинт приложения создает две точки, равные положению курсора, одна из этих точек, пт, преобразуется в пространство рукописного ввода и используется в вызове метода Неарестпоинт объекта [рукописного ввода](/previous-versions/ms836505(v=msdn.10)) [InkCollector](/previous-versions/ms583683(v=vs.100)). Метод Неарестпоинт возвращает объект [Stroke](/previous-versions/ms827842(v=msdn.10)) , ближайший к точке, и задает выходной параметр индекса с плавающей точкой.


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



Если штрихи отсутствуют, метод Неарестпоинт возвращает **значение NULL**, а положение курсора используется в качестве ближайшей точки. В противном случае вычисляется положение в штрихе, соответствующем индексу с плавающей запятой.

Затем координаты ближайших точек преобразуются в пиксели из пространства рукописного ввода, метод Хандленеарестпоинт делает недействительным Инвалидатерект область, вычисляет новый регион, в котором рисуется линия до ближайшей точки, и делает новую область недействительной.

## <a name="closing-the-form"></a>Закрытие формы

Метод Dispose удаляет объект [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
