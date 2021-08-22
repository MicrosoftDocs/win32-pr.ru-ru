---
description: Этот образец основан на образце коллекции рукописного ввода. В нем показано, как использовать объект разделителя для анализа рукописного ввода.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Пример рукописного разделителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c74592606ba98ec913dd419deda1b2b766066e17545e95f18a14980f36dafde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452101"
---
# <a name="ink-divider-sample"></a>Пример рукописного разделителя

Этот образец основан на [образце коллекции рукописного ввода](ink-collection-sample.md). В нем показано, как использовать объект [разделителя](/previous-versions/ms839398(v=msdn.10)) для анализа рукописного ввода.

Подробные концептуальные сведения о [делителье](/previous-versions/ms839398(v=msdn.10))см. [в разделе объект разделителя](the-divider-object.md).

При обновлении формы в примере создается ограничивающий прямоугольник вокруг каждой проанализированной единицы, разбитый на слова, линии, абзацы и рисунки. Кроме использования разных цветов, эти прямоугольники будут увеличены различными суммами, чтобы ни один из прямоугольников не был скрыт другими. В следующей таблице указаны цвет и увеличение для каждой проанализированной единицы.



| проанализированная единица        | Color              | Увеличение пикселя |
|----------------------|--------------------|-------------------|
| Word<br/>      | Зеленый<br/>   | 1<br/>      |
| Линия<br/>      | Пурпурный<br/> | 3<br/>      |
| Paragraph<br/> | Синий<br/>    | 5<br/>      |
| Рисование<br/>   | Красный<br/>     | 1<br/>      |



 

## <a name="setting-up-the-form"></a>Настройка формы

При загрузке формы создается объект- [Разделитель](/previous-versions/ms839398(v=msdn.10)) . Создается объект [InkOverlay](/previous-versions/ms833057(v=msdn.10)) , который связывается с панелью в форме. Затем обработчики событий присоединяются к объекту InkOverlay для контроля над добавлением и удалением штрихов. Затем, если распознаватели доступны, к разделителю назначается объект [рекогнизерконтекст](/previous-versions/ms828542(v=msdn.10)) для распознавателя по умолчанию. Затем задается свойство [LineHeight](/previous-versions/ms839409(v=msdn.10)) объекта-разделителя, и коллекция [росчерковs](/previous-versions/ms827799(v=msdn.10)) из объекта InkOverlay назначается разделителю. Наконец, объект InkOverlay включен.


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



Коллекция [штрихов](/previous-versions/ms839422(v=msdn.10)) объекта- [разделителя](/previous-versions/ms839398(v=msdn.10)) должна быть синхронизирована с коллекцией [штрихов](/previous-versions/ms827799(v=msdn.10)) объекта [InkOverlay](/previous-versions/ms833057(v=msdn.10)) (доступ к которой осуществляется через свойство [пера](/previous-versions/ms833110(v=msdn.10)) объекта InkOverlay). Чтобы убедиться, что это происходит, обработчик событий [Stroke](/previous-versions/ms835344(v=msdn.10)) для объекта InkOverlay записывается следующим образом. Обратите внимание, что обработчик событий сначала проверяет, установлен ли для [EditingMode](/previous-versions/ms833105(v=msdn.10)) **Рукописный ввод** для фильтрации штрихов ластика. Если пользователь запросил автоматическое анализ макета, приложение вызывает метод Дивидеинк формы и обновляет область рисования.


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



## <a name="dividing-the-ink"></a>Деление рукописного ввода

Когда пользователь щелкает пункт разделить в меню файл, метод [деления](/previous-versions/ms839461(v=msdn.10)) вызывается для объекта- [разделителя](/previous-versions/ms839398(v=msdn.10)) . Используется распознаватель по умолчанию, если он доступен.


```C++
DivisionResult divResult = myInkDivider.Divide();
```



Результирующий объект [дивисионресулт](/previous-versions/ms839371(v=msdn.10)) , на который ссылается переменная `divResult` , передается служебной функции, `getUnitBBBoxes()` . Служебная функция возвращает массив прямоугольников для любого запрошенного типа деления: сегменты, линии, абзацы или рисунки.


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



Наконец, панель формы вынуждена перерисовать, чтобы отображались ограничивающие прямоугольники.


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a>Результаты анализа рукописного ввода

В служебной функции объект [дивисионресулт](/previous-versions/ms839371(v=msdn.10)) запрашивает свои результаты с помощью метода [ресултбитипе](/previous-versions/ms839388(v=msdn.10)) , основанного на типе деления, запрошенном вызывающим объектом. Метод Ресултбитипе Возвращает коллекцию [дивисионунитс](/previous-versions/ms837954(v=msdn.10)) . Каждый [дивисионунит](/previous-versions/ms837976(v=msdn.10)) в коллекции представляет рисунок, один сегмент распознавания рукописного ввода, строку рукописного ввода или блок рукописного текста, в зависимости от того, что было указано при вызове служебной функции.


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



Если имеется хотя бы один [дивисионунит](/previous-versions/ms837976(v=msdn.10)), создается массив прямоугольников, содержащий один ограничивающий прямоугольник на единицу. (Прямоугольники преобразуются разными суммами для каждого типа единицы, которые хранятся в переменной Deflate, чтобы предотвратить перекрытие.)


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



## <a name="redrawing-the-form"></a>Перерисовка формы

Когда перерисовка выполняется выше, выполняется следующий код для рисования ограничивающих прямоугольников для каждого [дивисионунит](/previous-versions/ms837976(v=msdn.10)) в форме вокруг рукописного ввода.


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



## <a name="closing-the-form"></a>Закрытие формы

Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объекты [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [делитель](/previous-versions/ms839398(v=msdn.10)), [рекогнизерконтекст](/previous-versions/ms828542(v=msdn.10)) и коллекцию [штрихов](/previous-versions/ms827799(v=msdn.10)) , использованную в примере.

 

