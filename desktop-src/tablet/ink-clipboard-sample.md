---
description: Эта программа демонстрирует копирование и вставку рукописного ввода в другое приложение. Он также позволяет пользователю скопировать выбранные штрихи и вставить результат в существующий объект рукописного ввода.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Пример рукописного буфера обмена
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541319"
---
# <a name="ink-clipboard-sample"></a>Пример рукописного буфера обмена

Эта программа демонстрирует копирование и вставку рукописного ввода в другое приложение. Он также позволяет пользователю скопировать выбранные штрихи и вставить результат в существующий объект рукописного ввода.

Доступны следующие режимы буфера обмена:

-   Формат сериализованных рукописных данных (ISF)
-   Метафайл
-   EMF (Enhanced Metafile —расширенный метафайл)
-   Bitmap
-   Рукописный ввод текста
-   Нарисовать рукописный ввод

Текстовые рукописные и эскизные краски — это два типа элементов управления рукописного ввода, которые используются в качестве текста или рисунков соответственно. Можно вставить ISF, текстовый рукописный ввод и нарисовать рукописный ввод в существующую краску.

В дополнение к буферу обмена в этом примере также показано, как выбрать штрихи с помощью инструмента "лассо". Пользователь может перемещать выбранные штрихи и изменять их атрибуты рисования. Эта функция является подмножеством функций выбора, которые уже предоставлены элементом управления наложением красок. Он реализуется здесь для наглядных целей.

В этом примере используются следующие функции.

-   Объект [InkCollector](/previous-versions/ms583683(v=vs.100)) .
-   Поддержка рукописного ввода в буфере обмена.
-   Использование Лассо с методом [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) .

В этом примере демонстрируется визуализация рукописного ввода, копирование рукописного ввода и последующая запись рукописного ввода в другое приложение, например Microsoft Paint.

## <a name="collecting-ink-and-setting-up-the-form"></a>Сбор рукописных данных и настройка формы

Во-первых, сослаться на интерфейсы автоматизации планшетных ПК, которые устанавливаются вместе с <entity type="reg"/> пакетом SDK для Microsoft Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



Далее в форме объявляются некоторые константы и поля, отмеченные далее в этом примере.


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



Наконец, в обработчике событий [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) формы инициализируется форма, создается объект [InkCollector](/previous-versions/ms583683(v=vs.100)) для формы, а также включается сборщик рукописных данных.


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>Обработка событий меню

Обработчики событий пункта меню в основном обновляют состояние формы.

Команда Clear удаляет прямоугольник выделения и удаляет штрихи из объекта [рукописного ввода](/previous-versions/ms583670(v=vs.100)) сборщика рукописных данных.

Команда exit отключает сборщик рукописных данных перед выходом из приложения.

Меню Правка позволяет выполнять команды вырезания и копирования в зависимости от состояния выбора формы, а также включает команду вставки на основе содержимого буфера обмена, определенную с помощью метода [канпасте](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) объекта [Ink](/previous-versions/ms583670(v=vs.100)) .

Команды "вырезать" и "Копировать" используют вспомогательный метод для копирования рукописных данных в буфер обмена. Команда Cut использует вспомогательный метод для удаления выбранных штрихов.

Команда вставки сначала проверяет метод [канпасте](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) объекта [рукописного ввода](/previous-versions/ms583670(v=vs.100)) , чтобы определить, можно ли вставить объект из буфера обмена. Затем команда «Вставить» вычислит верхний левый угол области вставки, преобразует координаты пикселов в область рукописного ввода и вставляет штрихи из буфера обмена в сборщик рукописных данных. Наконец, поле выбора обновляется.


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



Команды выбора и рукописного ввода обновляют режим приложения и атрибуты рисования по умолчанию, очищают текущее выделение, обновляют состояние меню и обновляют форму. Другие обработчики используют состояние приложения для выполнения правильной функции: Лассо или верстка рукописного ввода. Кроме того, команда SELECT добавляет обработчики событий [невпаккетс](/previous-versions/ms567621(v=vs.100)) и [Stroke](/previous-versions/ms567622(v=vs.100)) в сборщик рукописных данных, а команда рукописного ввода удаляет эти обработчики событий из сборщика рукописных данных.

Форматы, доступные в буфере обмена при копировании штрихов, перечислены в меню Формат, и пользователь выбирает формат для копирования рукописных данных из этого списка. Доступные типы форматов включают в себя формат сериализованного рукописного ввода (ISF), метафайл, расширенный метафайл и точечный рисунок. Форматы рукописного ввода и текста наброски являются взаимоисключающими и полагаются на копируемый рукописный фрагмент в буфер обмена как объект OLE.

Меню Style (стиль) позволяет пользователю изменять свойства цвета и ширины пера и всех выбранных штрихов.

Например, Красная команда устанавливает свойство [Color](/previous-versions/ms582103(v=vs.100)) для свойства [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) сборщика рукописных данных на красный цвет. Так как свойство [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) объекта [cursor](/previous-versions/ms552104(v=vs.100)) не задано, все новые рукописные данные, нарисованные в сборщике рукописного ввода, наследуются цветом рисования по умолчанию. Кроме того, если в данный момент выбраны какие-либо штрихи, то также обновляется свойство цвета для атрибутов рисования каждого штриха.


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a>Обработка событий мыши

Обработчик событий [MouseMove](/previous-versions/ms567617(v=vs.100)) проверяет режим приложения. Если режим — Мовеинк, а кнопка мыши не нажата, обработчик перемещает штрихи с помощью метода Move коллекции [штрихов](/previous-versions/ms552701(v=vs.100)) и обновляет поле выбора. В противном случае обработчик проверяет, содержит ли прямоугольник выделения курсор, включает сбор рукописных данных, а также соответствующим образом задает курсор.

Обработчик событий [MouseDown](/previous-versions/ms567616(v=vs.100)) проверяет настройку курсора. Если курсор имеет значение [сизеалл](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), обработчик устанавливает для режима приложения значение мовеинк и записывает расположение курсора. В противном случае, если имеется текущее выделение, очистите его.

Обработчик событий [MouseUp](/previous-versions/ms567618(v=vs.100)) проверяет режим приложения. Если используется режим Мовеинк, обработчик устанавливает режим приложения на основе состояния проверки команды SELECT.

Событие [невпаккетс](/previous-versions/ms567621(v=vs.100)) возникает в режиме выделения, когда сборщик рукописных данных получает новые данные пакета. Если приложение находится в режиме выбора, необходимо перехватить новые пакеты и использовать их для рисования выделения Лассо.

Координаты каждого пакета преобразуются в пиксели, ограничены областью рисования и добавляются в коллекцию точек Лассо. Затем вызывается вспомогательный метод для рисования лассо в форме.

## <a name="handling-a-new-stroke"></a>Обработка нового росчерка

Событие [Stroke](/previous-versions/ms567622(v=vs.100)) возникает в режиме выбора при прорисовке нового штриха. Если приложение находится в режиме выбора, этот штрих соответствует Лассо и необходимо обновить сведения о выбранных штрихах.

Обработчик отменяет событие [Stroke](/previous-versions/ms567622(v=vs.100)) , проверяет наличие более двух точек Лассо, копирует коллекцию точек в массив объектов [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) и преобразует координаты точек в массиве из пикселов в пространство рукописного ввода. Затем обработчик использует метод [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) объекта [Ink](/previous-versions/ms583670(v=vs.100)) для получения штрихов, выбранных точками Лассо, и обновляет состояние выбора формы. Наконец, штрих, вызвавший событие, удаляется из коллекции выбранных штрихов, коллекция точек Лассо очищается, а вспомогательный метод рисует прямоугольник выделения.


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a>Копирование рукописного ввода в буфер обмена

Вспомогательный метод Копинктоклипбоард создает значение [инкклипбоардформатс](/previous-versions/ms583681(v=vs.100)) , проверяет состояние меню Формат, чтобы обновить форматы, помещаемые в буфер обмена, и использует метод [клипбоардкопи](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) объекта [рукописного ввода](/previous-versions/ms583670(v=vs.100)) для копирования штрихов в буфер обмена.


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a>Обновление выделенного фрагмента

Вспомогательный метод Сетселектион обновляет заданные Селектедстрокес и, если коллекция имеет **значение NULL** или **пуста**, прямоугольник выделения устанавливается равным пустому прямоугольнику. Если выбранная коллекция [штрихов](/previous-versions/ms552701(v=vs.100)) не пуста, метод сетселектион выполняет следующие действия:

-   Определяет ограничивающий прямоугольник с помощью метода [жетбаундингбокс](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) коллекции штрихов
-   Преобразует координаты прямоугольника из области рукописного ввода в Пиксели
-   Увеличивает прямоугольник, чтобы обеспечить некоторое визуальное пространство между ним и выбранными штрихами
-   Создает маркеры выбора для текущего поля выбора

Наконец, метод Сетселектион задает видимость дескрипторов выбора и устанавливает свойство [ауторедрав](/previous-versions/ms571706(v=vs.100)) сборщика рукописных данных в **значение false**, если штрихи выбраны.


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a>Рисование Лассо

Лассо рисуется в виде ряда открытых точек, которые следуют за контуром штриха Лассо и пунктирной линией соединительной линии между двумя концами. Событие [невпаккетс](/previous-versions/ms567621(v=vs.100)) возникает при прорисовке Лассо, а обработчик событий передает сведения о штрихах в метод дравлассо.

Вспомогательный метод Дравлассо сначала удаляет старую строку соединителя, а затем выполняет перебор точек в штрихе. Затем Дравлассо вычисляет место размещения точек вдоль штриха и отображает их. Наконец, он рисует новую линию соединителя.

## <a name="closing-the-form"></a>Закрытие формы

Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms583683(v=vs.100)) , минкколлектор.

 

 
