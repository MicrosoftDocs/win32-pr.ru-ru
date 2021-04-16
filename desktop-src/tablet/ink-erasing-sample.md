---
description: 'Это приложение построено на примере образца рукописного ввода, демонстрирующим Удаление рукописных штрихов. Образец предоставляет пользователю меню с четырьмя режимами выбора: с поддержкой рукописного ввода, стирание в КУСП, стирание в разных пересечениях и стирание штрихов.'
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Пример стирания рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540415"
---
# <a name="ink-erasing-sample"></a>Пример стирания рукописного ввода

Это приложение построено на [примере образца рукописного ввода](ink-collection-sample.md) , демонстрирующим Удаление рукописных штрихов. Образец предоставляет пользователю меню с четырьмя режимами выбора: с поддержкой рукописного ввода, стирание в КУСП, стирание в разных пересечениях и стирание штрихов.

В режиме с поддержкой рукописного ввода объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) собирает рукописные данные, как показано в [примере сбора рукописных данных](ink-collection-sample.md).

В режиме стирания сегменты рукописных штрихов, которые пользователь касается курсором, удаляются. Кроме того, куспс или пересечения могут быть помечены красным кругом.

Наиболее интересные части этого примера `InkErase` находятся в `OnPaint` обработчике событий формы и в функциях стирания, которые вызываются из `OnMouseMove` обработчика событий формы.

## <a name="circling-the-cusps-and-intersections"></a>Изогнутыми Куспс и пересечения

`OnPaint`Обработчик событий формы сначала закрашивает штрихи и, в зависимости от режима приложения, может найти и пометить все куспс или пересечения с небольшим красным кружком. КУСП помечает точку, в которой линия изменяется при внезапном направлении. Пересечение отмечает точку, в которой один росчерк пересекается с самим собой или с другим росчерком.

Событие [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) возникает при перерисовке элемента управления.

> [!Note]  
> Образец заставляет форму перерисовывать себя при удалении штриха или при изменении режима приложения с помощью метода [обновления](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) формы.

 


```C++
private void InkErase_OnPaint(object sender, PaintEventArgs e)
{
    Strokes strokesToPaint = myInkCollector.Ink.Strokes;

    myInkCollector.Renderer.Draw(e.Graphics, strokesToPaint);

    switch (mode)
    {
        case ApplicationMode.CuspErase:
            PaintCusps(e.Graphics, strokesToPaint);
            break;
        case ApplicationMode.IntersectErase:
            PaintIntersections(e.Graphics, strokesToPaint);
            break;
    }
}
```



В `PaintCusps` код проходит по каждому куспу в каждом штрихе и рисует вокруг него красный кружок. Свойство [полилинекуспс](/previous-versions/ms827853(v=msdn.10)) Stroke возвращает индексы точек в необходимо, которые соответствуют куспс. Кроме того, обратите внимание на метод [инкспацетопиксел](/previous-versions/ms828495(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) , который преобразует точку в координаты, относящиеся к методу DrawEllipse.


```C++
private void PaintCusps(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        int[] cusps = currentStroke.PolylineCusps;

        foreach (int i in cusps)
        {
            Point pt = currentStroke.GetPoint(i);

            // Convert the X, Y position to Window based pixel coordinates
            myInkCollector.Renderer.InkSpaceToPixel(g, ref pt);

            // Draw a red circle as the cusp position
            g.DrawEllipse(Pens.Red, pt.X-3, pt.Y-3, 6, 6);
        }
    }
}
```



В `PaintIntersections` код проходит по каждому штриху, чтобы найти его пересечения с целым набором штрихов. Обратите внимание, что метод [финдинтерсектионс](/previous-versions/ms827856(v=msdn.10)) Stroke передает коллекцию [штрихов](/previous-versions/ms827799(v=msdn.10)) и возвращает массив значений индекса с плавающей точкой, представляющих пересечения. Затем код вычисляет координаты X-Y для каждого пересечения и рисует вокруг него красную окружность.


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a>Обработка пера с двумя концами

Для объекта [InkCollector](/previous-versions/ms836493(v=msdn.10)) для событий [курсордовн](/previous-versions/ms567611(v=vs.100)), [невпаккетс](/previous-versions/ms567621(v=vs.100))и [Stroke](/previous-versions/ms567622(v=vs.100)) определены три обработчика событий. Каждый обработчик событий проверяет [Инвертированное](/previous-versions/ms839525(v=msdn.10)) свойство объекта [cursor](/previous-versions/ms839521(v=msdn.10)) , чтобы узнать, какой конец пера используется. При инвертировании пера:

-   `myInkCollector_CursorDown`Метод делает штрих прозрачным.
-   `myInkCollector_NewPackets`Метод удаляет штрихи.
-   `myInkCollector_Stroke`Метод отменяет событие. События [невпаккетс](/previous-versions/ms567621(v=vs.100)) создаются до события [Stroke](/previous-versions/ms567622(v=vs.100)) .

## <a name="tracking-the-cursor"></a>Отслеживание курсора

Когда пользователь использует перо или мышь, создаются события [MouseMove](/previous-versions/ms567617(v=vs.100)) . Обработчик событий MouseMove сначала проверяет, является ли текущий режим режимом стирания, и при нажатии какой-либо кнопки мыши и пропускает событие, если эти состояния отсутствуют. Затем обработчик событий преобразует координаты пикселя курсора в координаты пространства рукописного ввода с помощью метода [пикселтоинкспаце](/previous-versions/ms828505(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) и вызывает один из методов стирания кода в зависимости от текущего режима стирания.

## <a name="erasing-strokes"></a>Стирание штрихов

`EraseStrokes`Метод принимает положение курсора в пространстве рукописного ввода и формирует коллекцию штрихов, находящихся в пределах `HitTestRadius` единиц. `currentStroke`Параметр задает объект [Stroke](/previous-versions/ms827842(v=msdn.10)) , который не должен удаляться. Затем коллекция штрихов удаляется из сборщика, а форма перерисовывается.


```C++
private void EraseStrokes(Point pt, Stroke currentStroke)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    if (null!=currentStroke && strokesHit.Contains(currentStroke))
    {
        strokesHit.Remove(currentStroke);
    }

    myInkCollector.Ink.DeleteStrokes(strokesHit);

    if (strokesHit.Count > 0)
    {
        this.Refresh();
    }
}
```



## <a name="erasing-at-intersections"></a>Стирание в пересечениях

`EraseAtIntersections`Метод выполняет итерацию по каждому штриху, который попадает в тестовый радиус, и создает массив пересечения между этим обводкой и всеми другими штрихами в коллекции. Если пересечения не обнаружены, все штрихи удаляются. в противном случае размещается ближайшая точка на штрихе в тестовой точке, и из нее перечисляются пересечения с обеих сторон точки, описывающие удаляемый сегмент.

Метод [Split](/previous-versions/ms828477(v=msdn.10)) объекта [Stroke](/previous-versions/ms827842(v=msdn.10)) используется для отделения сегмента от остальной части штриха, после чего сегмент удаляется, оставшаяся часть штриха остается неизменной. Как `EraseStrokes` и в, форма перерисовывается перед возвратом метода.


```C++
private void EraseAtIntersections(Point pt)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    foreach (Stroke currentStroke in strokesHit)
    {
        float[] intersections = currentStroke.FindIntersections(myInkCollector.Ink.Strokes);
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(intersections[i]);
        ...
    }
    ...
}
```



## <a name="erasing-at-cusps"></a>Стирание на Куспс

Для каждого штриха, попадающего в тестовый радиус, `EraseAtCusps` метод извлекает массив куспс из метода [Полилинекуспс](/previous-versions/ms827853(v=msdn.10)) объекта [Stroke](/previous-versions/ms827842(v=msdn.10)) . Каждый конец штриха также является КУСП, поэтому если у росчерка только два куспс, то весь штрих будет удален. в противном случае размещается ближайшая точка на штрихе в тестовой точке, и из нее перечисляются пересечения с обеих сторон точки, описывающие удаляемый сегмент.

Метод [Split](/previous-versions/ms828477(v=msdn.10)) объекта [Stroke](/previous-versions/ms827842(v=msdn.10)) используется для отделения сегмента от остальной части штриха, после чего сегмент удаляется, оставшаяся часть штриха остается неизменной. Как `EraseStrokes` и в, форма перерисовывается перед возвратом метода.


```C++
private void EraseAtCusps(Point pt)
{
    ...
    strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);
    
    foreach (Stroke currentStroke in strokesHit)
    {
        int[] cusps = currentStroke.PolylineCusps;
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(cusps[i]); 
        myInkCollector.Ink.DeleteStroke(strokeToDelete);
        ...
    }
    ...
}
```



## <a name="closing-the-form"></a>Закрытие формы

Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 
