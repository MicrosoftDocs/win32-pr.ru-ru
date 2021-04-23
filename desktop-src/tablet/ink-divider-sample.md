---
description: Этот образец основан на образце коллекции рукописного ввода. В нем показано, как использовать объект разделителя для анализа рукописного ввода.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Пример рукописного разделителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a272d6a5530938e6fecfeefc9f46ffdd0835d045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497037"
---
# <a name="ink-divider-sample"></a><span data-ttu-id="ac57d-104">Пример рукописного разделителя</span><span class="sxs-lookup"><span data-stu-id="ac57d-104">Ink Divider Sample</span></span>

<span data-ttu-id="ac57d-105">Этот образец основан на [образце коллекции рукописного ввода](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ac57d-105">This sample is based on the [Ink Collection Sample](ink-collection-sample.md).</span></span> <span data-ttu-id="ac57d-106">В нем показано, как использовать объект [разделителя](/previous-versions/ms839398(v=msdn.10)) для анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ac57d-106">It shows how to use the [Divider](/previous-versions/ms839398(v=msdn.10)) object to analyze ink input.</span></span>

<span data-ttu-id="ac57d-107">Подробные концептуальные сведения о [делителье](/previous-versions/ms839398(v=msdn.10))см. [в разделе объект разделителя](the-divider-object.md).</span><span class="sxs-lookup"><span data-stu-id="ac57d-107">For detailed conceptual information about [Divider](/previous-versions/ms839398(v=msdn.10)), see [The Divider Object](the-divider-object.md).</span></span>

<span data-ttu-id="ac57d-108">При обновлении формы в примере создается ограничивающий прямоугольник вокруг каждой проанализированной единицы, разбитый на слова, линии, абзацы и рисунки.</span><span class="sxs-lookup"><span data-stu-id="ac57d-108">When the form is updated, the sample draws a bounding rectangle around each analyzed unit, broken into words, lines, paragraphs, and drawings.</span></span> <span data-ttu-id="ac57d-109">Кроме использования разных цветов, эти прямоугольники будут увеличены различными суммами, чтобы ни один из прямоугольников не был скрыт другими.</span><span class="sxs-lookup"><span data-stu-id="ac57d-109">Besides using different colors, these rectangles are enlarged by different amounts to ensure that none of the rectangles is obscured by others.</span></span> <span data-ttu-id="ac57d-110">В следующей таблице указаны цвет и увеличение для каждой проанализированной единицы.</span><span class="sxs-lookup"><span data-stu-id="ac57d-110">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="ac57d-111">проанализированная единица</span><span class="sxs-lookup"><span data-stu-id="ac57d-111">analyzed Unit</span></span>        | <span data-ttu-id="ac57d-112">Цвет</span><span class="sxs-lookup"><span data-stu-id="ac57d-112">Color</span></span>              | <span data-ttu-id="ac57d-113">Увеличение пикселя</span><span class="sxs-lookup"><span data-stu-id="ac57d-113">Pixel Enlargement</span></span> |
|----------------------|--------------------|-------------------|
| <span data-ttu-id="ac57d-114">Word</span><span class="sxs-lookup"><span data-stu-id="ac57d-114">Word</span></span><br/>      | <span data-ttu-id="ac57d-115">Зеленый</span><span class="sxs-lookup"><span data-stu-id="ac57d-115">Green</span></span><br/>   | <span data-ttu-id="ac57d-116">1</span><span class="sxs-lookup"><span data-stu-id="ac57d-116">1</span></span><br/>      |
| <span data-ttu-id="ac57d-117">Линия</span><span class="sxs-lookup"><span data-stu-id="ac57d-117">Line</span></span><br/>      | <span data-ttu-id="ac57d-118">Пурпурный</span><span class="sxs-lookup"><span data-stu-id="ac57d-118">Magenta</span></span><br/> | <span data-ttu-id="ac57d-119">3</span><span class="sxs-lookup"><span data-stu-id="ac57d-119">3</span></span><br/>      |
| <span data-ttu-id="ac57d-120">Paragraph</span><span class="sxs-lookup"><span data-stu-id="ac57d-120">Paragraph</span></span><br/> | <span data-ttu-id="ac57d-121">Синий</span><span class="sxs-lookup"><span data-stu-id="ac57d-121">Blue</span></span><br/>    | <span data-ttu-id="ac57d-122">5</span><span class="sxs-lookup"><span data-stu-id="ac57d-122">5</span></span><br/>      |
| <span data-ttu-id="ac57d-123">Рисование</span><span class="sxs-lookup"><span data-stu-id="ac57d-123">Drawing</span></span><br/>   | <span data-ttu-id="ac57d-124">Красный</span><span class="sxs-lookup"><span data-stu-id="ac57d-124">Red</span></span><br/>     | <span data-ttu-id="ac57d-125">1</span><span class="sxs-lookup"><span data-stu-id="ac57d-125">1</span></span><br/>      |



 

## <a name="setting-up-the-form"></a><span data-ttu-id="ac57d-126">Настройка формы</span><span class="sxs-lookup"><span data-stu-id="ac57d-126">Setting Up the Form</span></span>

<span data-ttu-id="ac57d-127">При загрузке формы создается объект- [Разделитель](/previous-versions/ms839398(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ac57d-127">When the form loads, a [Divider](/previous-versions/ms839398(v=msdn.10)) object is created.</span></span> <span data-ttu-id="ac57d-128">Создается объект [InkOverlay](/previous-versions/ms833057(v=msdn.10)) , который связывается с панелью в форме.</span><span class="sxs-lookup"><span data-stu-id="ac57d-128">An [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object is created and associated with a panel on the form.</span></span> <span data-ttu-id="ac57d-129">Затем обработчики событий присоединяются к объекту InkOverlay для контроля над добавлением и удалением штрихов.</span><span class="sxs-lookup"><span data-stu-id="ac57d-129">Then event handlers are attached to the InkOverlay object to track when strokes are added and deleted.</span></span> <span data-ttu-id="ac57d-130">Затем, если распознаватели доступны, к разделителю назначается объект [рекогнизерконтекст](/previous-versions/ms828542(v=msdn.10)) для распознавателя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ac57d-130">Then if recognizers are available, a [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) object for the default recognizer is assigned to the Divider.</span></span> <span data-ttu-id="ac57d-131">Затем задается свойство [LineHeight](/previous-versions/ms839409(v=msdn.10)) объекта-разделителя, и коллекция [росчерковs](/previous-versions/ms827799(v=msdn.10)) из объекта InkOverlay назначается разделителю.</span><span class="sxs-lookup"><span data-stu-id="ac57d-131">Then the Divider object's [LineHeight](/previous-versions/ms839409(v=msdn.10)) property is set and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection from the InkOverlay object is assigned to the Divider.</span></span> <span data-ttu-id="ac57d-132">Наконец, объект InkOverlay включен.</span><span class="sxs-lookup"><span data-stu-id="ac57d-132">Finally, the InkOverlay object is enabled.</span></span>


```C++
// Create the ink overlay and associate it with the form
myInkOverlay = new Microsoft.Ink.InkOverlay(DrawArea.Handle);

// Set the erasing mode to stroke erase.
myInkOverlay.EraserMode = InkOverlayEraserMode.StrokeErase;

// Hook event handler for the Stroke event to myInkOverlay_Stroke.
// This is necessary since the application needs to pass the strokes 
// to the ink divider.
myInkOverlay.Stroke += new InkCollectorStrokeEventHandler(myInkOverlay_Stroke); 

// Hook the event handler for StrokeDeleting event to myInkOverlay_StrokeDeleting.
// This is necessary as the application needs to remove the strokes from 
// ink divider object as well.
myInkOverlay.StrokesDeleting += new InkOverlayStrokesDeletingEventHandler(myInkOverlay_StrokeDeleting);

// Hook the event handler for StrokeDeleted event to myInkOverlay_StrokeDeleted.
// This is necessary to update the layout analysis result when automatic layout analysis
// option is selected.
myInkOverlay.StrokesDeleted += new InkOverlayStrokesDeletedEventHandler(myInkOverlay_StrokeDeleted);

// Create the ink divider object
myInkDivider = new Divider();

// Add a default recognizer context to the divider object
// without adding the recognizer context, the divider would
// not use a recognizer to do its word segmentation and would
// have less accurate results.
// Adding the recognizer context slows down the call to 
// myInkDivider.Divide though.
// It is possible that there is no recognizer installed on the
// machine for this language. In that case the divider does
// not use a recognizer to improve its accuracy.
// Get the default recognizer if any
try
{
    Recognizers recognizers = new Recognizers();
     myInkDivider.RecognizerContext = recognizers.GetDefaultRecognizer().CreateRecognizerContext();
}
catch (InvalidOperationException)
{
     //We are in the case where no default recognizers can be found
}

    // The LineHeight property helps the InkDivider distinguish between 
    // drawing and handwriting. The value should be the expected height 
    // of the user's handwriting in ink space units (0.01mm).
    // Here we set the LineHeight to 840, which is about 1/3 of an inch.
    myInkDivider.LineHeight = 840;

// Assign ink overlay's strokes collection to the ink divider
// This strokes collection is updated in the event handler
myInkDivider.Strokes = myInkOverlay.Ink.Strokes;

// Enable ink collection
myInkOverlay.Enabled = true;
```



<span data-ttu-id="ac57d-133">Коллекция [штрихов](/previous-versions/ms839422(v=msdn.10)) объекта- [разделителя](/previous-versions/ms839398(v=msdn.10)) должна быть синхронизирована с коллекцией [штрихов](/previous-versions/ms827799(v=msdn.10)) объекта [InkOverlay](/previous-versions/ms833057(v=msdn.10)) (доступ к которой осуществляется через свойство [пера](/previous-versions/ms833110(v=msdn.10)) объекта InkOverlay).</span><span class="sxs-lookup"><span data-stu-id="ac57d-133">The [Divider](/previous-versions/ms839398(v=msdn.10)) object's [Strokes](/previous-versions/ms839422(v=msdn.10)) collection must be kept in sync with the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Strokes](/previous-versions/ms827799(v=msdn.10)) collection (accessed through the InkOverlay object's [Ink](/previous-versions/ms833110(v=msdn.10)) property).</span></span> <span data-ttu-id="ac57d-134">Чтобы убедиться, что это происходит, обработчик событий [Stroke](/previous-versions/ms835344(v=msdn.10)) для объекта InkOverlay записывается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ac57d-134">To ensure that this happens, the [Stroke](/previous-versions/ms835344(v=msdn.10)) event handler for the InkOverlay object is written as follows.</span></span> <span data-ttu-id="ac57d-135">Обратите внимание, что обработчик событий сначала проверяет, установлен ли для [EditingMode](/previous-versions/ms833105(v=msdn.10)) **Рукописный ввод** для фильтрации штрихов ластика.</span><span class="sxs-lookup"><span data-stu-id="ac57d-135">Note that the event handler first tests to see if the [EditingMode](/previous-versions/ms833105(v=msdn.10)) is set to **Ink** to filter out eraser strokes.</span></span> <span data-ttu-id="ac57d-136">Если пользователь запросил автоматическое анализ макета, приложение вызывает метод Дивидеинк формы и обновляет область рисования.</span><span class="sxs-lookup"><span data-stu-id="ac57d-136">If the user has requested automatic layout analysis, then the application calls the form's DivideInk method and refreshes the drawing area.</span></span>


```C++
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e )
{
    // Filter out the eraser stroke.
    if(InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
    {
        // Add the new stroke to the ink divider's strokes collection
        myInkDivider.Strokes.Add(e.Stroke);
        
        if(miAutomaticLayoutAnalysis.Checked)
        {
            // Call DivideInk
            DivideInk();

            // Repaint the screen to reflect the change
            DrawArea.Refresh();
        }
    }
}
```



## <a name="dividing-the-ink"></a><span data-ttu-id="ac57d-137">Деление рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ac57d-137">Dividing the Ink</span></span>

<span data-ttu-id="ac57d-138">Когда пользователь щелкает пункт разделить в меню файл, метод [деления](/previous-versions/ms839461(v=msdn.10)) вызывается для объекта- [разделителя](/previous-versions/ms839398(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ac57d-138">When the user clicks Divide on the File menu, the [Divide](/previous-versions/ms839461(v=msdn.10)) method is called on the [Divider](/previous-versions/ms839398(v=msdn.10)) object.</span></span> <span data-ttu-id="ac57d-139">Используется распознаватель по умолчанию, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="ac57d-139">The default recognizer is used, if available.</span></span>


```C++
DivisionResult divResult = myInkDivider.Divide();
```



<span data-ttu-id="ac57d-140">Результирующий объект [дивисионресулт](/previous-versions/ms839371(v=msdn.10)) , на который ссылается переменная `divResult` , передается служебной функции, `getUnitBBBoxes()` .</span><span class="sxs-lookup"><span data-stu-id="ac57d-140">The resulting [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object, referenced by the variable `divResult`, is passed to a utility function, `getUnitBBBoxes()`.</span></span> <span data-ttu-id="ac57d-141">Служебная функция возвращает массив прямоугольников для любого запрошенного типа деления: сегменты, линии, абзацы или рисунки.</span><span class="sxs-lookup"><span data-stu-id="ac57d-141">The utility function returns an array of rectangles for whatever division type is requested: segments, lines, paragraphs, or drawings.</span></span>


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



<span data-ttu-id="ac57d-142">Наконец, панель формы вынуждена перерисовать, чтобы отображались ограничивающие прямоугольники.</span><span class="sxs-lookup"><span data-stu-id="ac57d-142">Finally, the form panel is forced to redraw so that the bounding rectangles appear.</span></span>


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a><span data-ttu-id="ac57d-143">Результаты анализа рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ac57d-143">Ink Analysis Results</span></span>

<span data-ttu-id="ac57d-144">В служебной функции объект [дивисионресулт](/previous-versions/ms839371(v=msdn.10)) запрашивает свои результаты с помощью метода [ресултбитипе](/previous-versions/ms839388(v=msdn.10)) , основанного на типе деления, запрошенном вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="ac57d-144">In the utility function, the [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object is queried for its results by using the [ResultByType](/previous-versions/ms839388(v=msdn.10)) method, based on the division type requested by the caller.</span></span> <span data-ttu-id="ac57d-145">Метод Ресултбитипе Возвращает коллекцию [дивисионунитс](/previous-versions/ms837954(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ac57d-145">The ResultByType method returns a [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) collection.</span></span> <span data-ttu-id="ac57d-146">Каждый [дивисионунит](/previous-versions/ms837976(v=msdn.10)) в коллекции представляет рисунок, один сегмент распознавания рукописного ввода, строку рукописного ввода или блок рукописного текста, в зависимости от того, что было указано при вызове служебной функции.</span><span class="sxs-lookup"><span data-stu-id="ac57d-146">Each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) in the collection represents a drawing, a single recognition segment of handwriting, a line of handwriting, or a block of handwriting, depending upon what was specified when the utility function was called.</span></span>


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



<span data-ttu-id="ac57d-147">Если имеется хотя бы один [дивисионунит](/previous-versions/ms837976(v=msdn.10)), создается массив прямоугольников, содержащий один ограничивающий прямоугольник на единицу.</span><span class="sxs-lookup"><span data-stu-id="ac57d-147">If there is at least one [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), an array of rectangles is created containing one bounding rectangle per unit.</span></span> <span data-ttu-id="ac57d-148">(Прямоугольники преобразуются разными суммами для каждого типа единицы, которые хранятся в переменной Deflate, чтобы предотвратить перекрытие.)</span><span class="sxs-lookup"><span data-stu-id="ac57d-148">(The rectangles are inflated by differing amounts for each type of unit, held in the inflate variable, to prevent overlapping.)</span></span>


```C++
// If there is at least one unit, we construct the rectangles
if((null != units) && (0 < units.Count))
{
    // We need to convert rectangles from ink units to
    // pixel units. For that, we need Graphics object
    // to pass to InkRenderer.InkSpaceToPixel method
    using (Graphics g = DrawArea.CreateGraphics())
    {

    // InkSpace to Pixel Space conversion setup done here. 
    // Not shown for brevity.

        // Iterate through the collection of division units to obtain the bounding boxes
        foreach(DivisionUnit unit in units)
        {
            // Get the bounding box of the strokes of the division unit
            divRects[i] = unit.Strokes.GetBoundingBox();

            // Div unit rect Ink space to Pixel space conversion done here. 
            // Not shown for brevity.

            // Inflate the rectangle by inflate pixels in both directions
            divRects[i].Inflate(inflate, inflate);

            // Increment the index
            ++i;
        }

    } // Relinquish the Graphics object
}
```



## <a name="redrawing-the-form"></a><span data-ttu-id="ac57d-149">Перерисовка формы</span><span class="sxs-lookup"><span data-stu-id="ac57d-149">Redrawing the Form</span></span>

<span data-ttu-id="ac57d-150">Когда перерисовка выполняется выше, выполняется следующий код для рисования ограничивающих прямоугольников для каждого [дивисионунит](/previous-versions/ms837976(v=msdn.10)) в форме вокруг рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ac57d-150">When the redraw is forced above, the following code executes to paint the bounding boxes for each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) on the form around the ink.</span></span>


```C++
private void DrawArea_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
        {
            // Create the Pen used to draw bounding boxes.
            // First set of bounding boxes drawn here are 
            // the bounding boxes of paragraphs.
            // These boxes are drawn with Blue pen.
            Pen penBox = new Pen(Color.Blue, 2);

            // First, draw the bounding boxes for Paragraphs
            if(null != myParagraphBoundingBoxes)
            {
                // Draw bounding boxes for Paragraphs
                e.Graphics.DrawRectangles(penBox, myParagraphBoundingBoxes);
            }

            // Next, draw the bounding boxes for Lines
            if(null != myLineBoundingBoxes)
            {
                // Color is Magenta pen
                penBox.Color = Color.Magenta;
                // Draw the bounding boxes for Lines
                e.Graphics.DrawRectangles(penBox, myLineBoundingBoxes);
            }
            
            // Then, draw the bounding boxes for Words
            if(null != myWordBoundingBoxes)
            {
                // Color is Green
                penBox.Color = Color.Green;
                // Draw bounding boxes for Words
                e.Graphics.DrawRectangles(penBox, myWordBoundingBoxes);
            }
            
            // Finally, draw the boxes for Drawings
            if(null != myDrawingBoundingBoxes)
            {
                // Color is Red pen
                penBox.Color = Color.Red;
                // Draw bounding boxes for Drawings
                e.Graphics.DrawRectangles(penBox, myDrawingBoundingBoxes);
            }
        }
```



## <a name="closing-the-form"></a><span data-ttu-id="ac57d-151">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="ac57d-151">Closing the Form</span></span>

<span data-ttu-id="ac57d-152">Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объекты [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [делитель](/previous-versions/ms839398(v=msdn.10)), [рекогнизерконтекст](/previous-versions/ms828542(v=msdn.10)) и коллекцию [штрихов](/previous-versions/ms827799(v=msdn.10)) , использованную в примере.</span><span class="sxs-lookup"><span data-stu-id="ac57d-152">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [Divider](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) objects and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection used in the sample.</span></span>

 

