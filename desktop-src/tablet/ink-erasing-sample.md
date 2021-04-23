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
# <a name="ink-erasing-sample"></a><span data-ttu-id="d08e8-104">Пример стирания рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="d08e8-104">Ink Erasing Sample</span></span>

<span data-ttu-id="d08e8-105">Это приложение построено на [примере образца рукописного ввода](ink-collection-sample.md) , демонстрирующим Удаление рукописных штрихов.</span><span class="sxs-lookup"><span data-stu-id="d08e8-105">This application builds on the [Ink Collection Sample](ink-collection-sample.md) sample by demonstrating ink strokes deletion.</span></span> <span data-ttu-id="d08e8-106">Образец предоставляет пользователю меню с четырьмя режимами выбора: с поддержкой рукописного ввода, стирание в КУСП, стирание в разных пересечениях и стирание штрихов.</span><span class="sxs-lookup"><span data-stu-id="d08e8-106">The sample provides the user with a menu that has four modes to choose from: ink-enabled, erasing at cusp, erasing at intersections, and erasing strokes.</span></span>

<span data-ttu-id="d08e8-107">В режиме с поддержкой рукописного ввода объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) собирает рукописные данные, как показано в [примере сбора рукописных данных](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d08e8-107">In ink-enabled mode, the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object collects ink as shown in [Ink Collection Sample](ink-collection-sample.md).</span></span>

<span data-ttu-id="d08e8-108">В режиме стирания сегменты рукописных штрихов, которые пользователь касается курсором, удаляются.</span><span class="sxs-lookup"><span data-stu-id="d08e8-108">In an erasing mode, segments of existing ink strokes that the user touches with the cursor are erased.</span></span> <span data-ttu-id="d08e8-109">Кроме того, куспс или пересечения могут быть помечены красным кругом.</span><span class="sxs-lookup"><span data-stu-id="d08e8-109">Also, the cusps or intersections may be marked with a red circle.</span></span>

<span data-ttu-id="d08e8-110">Наиболее интересные части этого примера `InkErase` находятся в `OnPaint` обработчике событий формы и в функциях стирания, которые вызываются из `OnMouseMove` обработчика событий формы.</span><span class="sxs-lookup"><span data-stu-id="d08e8-110">The most interesting parts of this sample lie in the `InkErase` form's `OnPaint` event handler and in the erasing functions that are called from the form's `OnMouseMove` event handler.</span></span>

## <a name="circling-the-cusps-and-intersections"></a><span data-ttu-id="d08e8-111">Изогнутыми Куспс и пересечения</span><span class="sxs-lookup"><span data-stu-id="d08e8-111">Circling the Cusps and Intersections</span></span>

<span data-ttu-id="d08e8-112">`OnPaint`Обработчик событий формы сначала закрашивает штрихи и, в зависимости от режима приложения, может найти и пометить все куспс или пересечения с небольшим красным кружком.</span><span class="sxs-lookup"><span data-stu-id="d08e8-112">The form's `OnPaint` event handler first paints the strokes, and depending on the application mode, may find and mark all of the cusps or intersections with a small red circle.</span></span> <span data-ttu-id="d08e8-113">КУСП помечает точку, в которой линия изменяется при внезапном направлении.</span><span class="sxs-lookup"><span data-stu-id="d08e8-113">A cusp marks the point where a stroke changes direction abruptly.</span></span> <span data-ttu-id="d08e8-114">Пересечение отмечает точку, в которой один росчерк пересекается с самим собой или с другим росчерком.</span><span class="sxs-lookup"><span data-stu-id="d08e8-114">An intersection marks a point where one stroke intersects with itself or another stroke.</span></span>

<span data-ttu-id="d08e8-115">Событие [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) возникает при перерисовке элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d08e8-115">The [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event occurs whenever a control is redrawn.</span></span>

> [!Note]  
> <span data-ttu-id="d08e8-116">Образец заставляет форму перерисовывать себя при удалении штриха или при изменении режима приложения с помощью метода [обновления](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) формы.</span><span class="sxs-lookup"><span data-stu-id="d08e8-116">The sample forces the form to redraw itself whenever a stroke is erased, or when the application mode changes, using the form's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method.</span></span>

 


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



<span data-ttu-id="d08e8-117">В `PaintCusps` код проходит по каждому куспу в каждом штрихе и рисует вокруг него красный кружок.</span><span class="sxs-lookup"><span data-stu-id="d08e8-117">In `PaintCusps`, the code iterates through each cusp in each stroke, and draws a red circle around it.</span></span> <span data-ttu-id="d08e8-118">Свойство [полилинекуспс](/previous-versions/ms827853(v=msdn.10)) Stroke возвращает индексы точек в необходимо, которые соответствуют куспс.</span><span class="sxs-lookup"><span data-stu-id="d08e8-118">The stroke's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) property returns the indices of the points within a stoke that correspond to cusps.</span></span> <span data-ttu-id="d08e8-119">Кроме того, обратите внимание на метод [инкспацетопиксел](/previous-versions/ms828495(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) , который преобразует точку в координаты, относящиеся к методу DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="d08e8-119">Also, note the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) method, which converts the point to coordinates relevant to the DrawEllipse method.</span></span>


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



<span data-ttu-id="d08e8-120">В `PaintIntersections` код проходит по каждому штриху, чтобы найти его пересечения с целым набором штрихов.</span><span class="sxs-lookup"><span data-stu-id="d08e8-120">In `PaintIntersections`, the code iterates through each stroke to find its intersections with the entire set of strokes.</span></span> <span data-ttu-id="d08e8-121">Обратите внимание, что метод [финдинтерсектионс](/previous-versions/ms827856(v=msdn.10)) Stroke передает коллекцию [штрихов](/previous-versions/ms827799(v=msdn.10)) и возвращает массив значений индекса с плавающей точкой, представляющих пересечения.</span><span class="sxs-lookup"><span data-stu-id="d08e8-121">Note that the stroke's [FindIntersections](/previous-versions/ms827856(v=msdn.10)) method is passed a [Strokes](/previous-versions/ms827799(v=msdn.10)) collection and returns an array of floating point index values representing the intersections.</span></span> <span data-ttu-id="d08e8-122">Затем код вычисляет координаты X-Y для каждого пересечения и рисует вокруг него красную окружность.</span><span class="sxs-lookup"><span data-stu-id="d08e8-122">The code then calculates an X-Y coordinate for each intersection, and draws a red circle around it.</span></span>


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a><span data-ttu-id="d08e8-123">Обработка пера с двумя концами</span><span class="sxs-lookup"><span data-stu-id="d08e8-123">Handling a Pen That Has Two Ends</span></span>

<span data-ttu-id="d08e8-124">Для объекта [InkCollector](/previous-versions/ms836493(v=msdn.10)) для событий [курсордовн](/previous-versions/ms567611(v=vs.100)), [невпаккетс](/previous-versions/ms567621(v=vs.100))и [Stroke](/previous-versions/ms567622(v=vs.100)) определены три обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="d08e8-124">Three event handlers are defined for the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100)), and [Stroke](/previous-versions/ms567622(v=vs.100)) events.</span></span> <span data-ttu-id="d08e8-125">Каждый обработчик событий проверяет [Инвертированное](/previous-versions/ms839525(v=msdn.10)) свойство объекта [cursor](/previous-versions/ms839521(v=msdn.10)) , чтобы узнать, какой конец пера используется.</span><span class="sxs-lookup"><span data-stu-id="d08e8-125">Each event handler checks the [Cursor](/previous-versions/ms839521(v=msdn.10)) object's [Inverted](/previous-versions/ms839525(v=msdn.10)) property to see which end of the pen is being used.</span></span> <span data-ttu-id="d08e8-126">При инвертировании пера:</span><span class="sxs-lookup"><span data-stu-id="d08e8-126">When the pen is inverted:</span></span>

-   <span data-ttu-id="d08e8-127">`myInkCollector_CursorDown`Метод делает штрих прозрачным.</span><span class="sxs-lookup"><span data-stu-id="d08e8-127">The `myInkCollector_CursorDown` method makes the stroke transparent.</span></span>
-   <span data-ttu-id="d08e8-128">`myInkCollector_NewPackets`Метод удаляет штрихи.</span><span class="sxs-lookup"><span data-stu-id="d08e8-128">The `myInkCollector_NewPackets` method erases strokes.</span></span>
-   <span data-ttu-id="d08e8-129">`myInkCollector_Stroke`Метод отменяет событие.</span><span class="sxs-lookup"><span data-stu-id="d08e8-129">The `myInkCollector_Stroke` method cancels the event.</span></span> <span data-ttu-id="d08e8-130">События [невпаккетс](/previous-versions/ms567621(v=vs.100)) создаются до события [Stroke](/previous-versions/ms567622(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d08e8-130">[NewPackets](/previous-versions/ms567621(v=vs.100)) events are generated prior to the [Stroke](/previous-versions/ms567622(v=vs.100)) event.</span></span>

## <a name="tracking-the-cursor"></a><span data-ttu-id="d08e8-131">Отслеживание курсора</span><span class="sxs-lookup"><span data-stu-id="d08e8-131">Tracking the Cursor</span></span>

<span data-ttu-id="d08e8-132">Когда пользователь использует перо или мышь, создаются события [MouseMove](/previous-versions/ms567617(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d08e8-132">Whether the user is using a pen or a mouse, [MouseMove](/previous-versions/ms567617(v=vs.100)) events are generated.</span></span> <span data-ttu-id="d08e8-133">Обработчик событий MouseMove сначала проверяет, является ли текущий режим режимом стирания, и при нажатии какой-либо кнопки мыши и пропускает событие, если эти состояния отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="d08e8-133">The MouseMove event handler first checks to determine whether the current mode is an erase mode and if any mouse button is pressed, and ignores the event if these states are not present.</span></span> <span data-ttu-id="d08e8-134">Затем обработчик событий преобразует координаты пикселя курсора в координаты пространства рукописного ввода с помощью метода [пикселтоинкспаце](/previous-versions/ms828505(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) и вызывает один из методов стирания кода в зависимости от текущего режима стирания.</span><span class="sxs-lookup"><span data-stu-id="d08e8-134">Then, the event handler converts the pixel coordinates for the cursor into ink space coordinates by using the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method, and calls one of the code's erase methods depending on the current erase mode.</span></span>

## <a name="erasing-strokes"></a><span data-ttu-id="d08e8-135">Стирание штрихов</span><span class="sxs-lookup"><span data-stu-id="d08e8-135">Erasing Strokes</span></span>

<span data-ttu-id="d08e8-136">`EraseStrokes`Метод принимает положение курсора в пространстве рукописного ввода и формирует коллекцию штрихов, находящихся в пределах `HitTestRadius` единиц.</span><span class="sxs-lookup"><span data-stu-id="d08e8-136">The `EraseStrokes` method takes the cursor's location in ink space and generates a collection of strokes that are within `HitTestRadius` units.</span></span> <span data-ttu-id="d08e8-137">`currentStroke`Параметр задает объект [Stroke](/previous-versions/ms827842(v=msdn.10)) , который не должен удаляться.</span><span class="sxs-lookup"><span data-stu-id="d08e8-137">The `currentStroke` parameter specifies a [Stroke](/previous-versions/ms827842(v=msdn.10)) object that should not be deleted.</span></span> <span data-ttu-id="d08e8-138">Затем коллекция штрихов удаляется из сборщика, а форма перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="d08e8-138">Then the strokes collection is deleted from the collector, and the form is redrawn.</span></span>


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



## <a name="erasing-at-intersections"></a><span data-ttu-id="d08e8-139">Стирание в пересечениях</span><span class="sxs-lookup"><span data-stu-id="d08e8-139">Erasing at Intersections</span></span>

<span data-ttu-id="d08e8-140">`EraseAtIntersections`Метод выполняет итерацию по каждому штриху, который попадает в тестовый радиус, и создает массив пересечения между этим обводкой и всеми другими штрихами в коллекции.</span><span class="sxs-lookup"><span data-stu-id="d08e8-140">The `EraseAtIntersections` method iterates over each stroke that falls within the test radius and generates an array of intersections between that stroke and all the other strokes in the collection.</span></span> <span data-ttu-id="d08e8-141">Если пересечения не обнаружены, все штрихи удаляются. в противном случае размещается ближайшая точка на штрихе в тестовой точке, и из нее перечисляются пересечения с обеих сторон точки, описывающие удаляемый сегмент.</span><span class="sxs-lookup"><span data-stu-id="d08e8-141">If no intersections are found, then that entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="d08e8-142">Метод [Split](/previous-versions/ms828477(v=msdn.10)) объекта [Stroke](/previous-versions/ms827842(v=msdn.10)) используется для отделения сегмента от остальной части штриха, после чего сегмент удаляется, оставшаяся часть штриха остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="d08e8-142">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="d08e8-143">Как `EraseStrokes` и в, форма перерисовывается перед возвратом метода.</span><span class="sxs-lookup"><span data-stu-id="d08e8-143">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


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



## <a name="erasing-at-cusps"></a><span data-ttu-id="d08e8-144">Стирание на Куспс</span><span class="sxs-lookup"><span data-stu-id="d08e8-144">Erasing at Cusps</span></span>

<span data-ttu-id="d08e8-145">Для каждого штриха, попадающего в тестовый радиус, `EraseAtCusps` метод извлекает массив куспс из метода [Полилинекуспс](/previous-versions/ms827853(v=msdn.10)) объекта [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="d08e8-145">For each stroke that falls within the test radius, the `EraseAtCusps` method retrieves the array of cusps from the [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) method.</span></span> <span data-ttu-id="d08e8-146">Каждый конец штриха также является КУСП, поэтому если у росчерка только два куспс, то весь штрих будет удален. в противном случае размещается ближайшая точка на штрихе в тестовой точке, и из нее перечисляются пересечения с обеих сторон точки, описывающие удаляемый сегмент.</span><span class="sxs-lookup"><span data-stu-id="d08e8-146">Each end of the stroke is also a cusp, so if the stroke only has two cusps, then the entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="d08e8-147">Метод [Split](/previous-versions/ms828477(v=msdn.10)) объекта [Stroke](/previous-versions/ms827842(v=msdn.10)) используется для отделения сегмента от остальной части штриха, после чего сегмент удаляется, оставшаяся часть штриха остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="d08e8-147">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="d08e8-148">Как `EraseStrokes` и в, форма перерисовывается перед возвратом метода.</span><span class="sxs-lookup"><span data-stu-id="d08e8-148">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="d08e8-149">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="d08e8-149">Closing the Form</span></span>

<span data-ttu-id="d08e8-150">Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="d08e8-150">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
