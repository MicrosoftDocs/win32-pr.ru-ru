---
description: В этом образце программы показано, как изменять масштаб и прокручивать рукописный ввод.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Пример масштабирования рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d786fe502e1510a44df39049e845f05694a1befae0d4a21bcfa2ba2bd2b19b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939444"
---
# <a name="ink-zoom-sample"></a>Пример масштабирования рукописного ввода

В этом образце программы показано, как изменять масштаб и прокручивать рукописный ввод. В частности, он позволяет пользователю увеличивать и уменьшать рукописные данные с приращениями. Здесь также показано, как увеличить масштаб в определенном регионе с помощью прямоугольника масштабирования. Наконец, в этом образце показано, как выполнять накопление рукописного ввода с различными коэффициентами масштабирования и как настроить прокрутку в масштабной области рисования.

В этом примере для выполнения масштабирования и прокрутки используются представление объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов и преобразования объектов. Преобразование «представление» применяется к точкам и ширине пера. Преобразование объекта применяется только к точкам. Пользователь может управлять тем, какое преобразование используется, изменяя элемент ширина пера шкалы в меню режим.

> [!Note]  
> При отправке сообщения возникают проблемы при выполнении некоторых вызовов COM для определенных методов интерфейса (например,[**инкрендерер. сетвиевтрансформ**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) и [**инкрендерер. сетобжекттрансформ**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)). Когда сообщения отправляются, они должны быть упакованы в очередь сообщений POST. Чтобы решить эту проблему, проверьте, обрабатывается ли сообщение от POST путем вызова [**инсендмесссажеекс**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) , и опубликуйте сообщение в себе, если сообщение было отправлено.

 

В этом примере используются следующие функции.

-   Объект [InkCollector](/previous-versions/ms583683(v=vs.100))
-   Метод [сетвиевтрансформ](/previous-versions/ms828514(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов
-   Метод [сетобжекттрансформ](/previous-versions/ms828513(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов

## <a name="initializing-the-form"></a>Инициализация формы

во-первых, образец ссылается на интерфейсы автоматизации планшетных пк, предоставляемые в Windows Vista или Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



В примере объявляются объект [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` и некоторые закрытые члены, помогающие при масштабировании.


```C++
// Declare the Ink Collector object
private InkCollector myInkCollector = null;
...
// The starting and ending points of the zoom rectangle
private Rectangle zoomRectangle = Rectangle.Empty;

// The current zoom factor (1 = 100% zoom level)
private float zoomFactor = 1;

// Declare constants for the width and height of the 
// drawing area (in ink space coordinates).
private const int InkSpaceWidth = 50000;
private const int InkSpaceHeight = 50000;
...
// Declare constant for the pen width used by this application
private const float MediumInkWidth = 100;
```



Затем в примере создается и включается объект [InkCollector](/previous-versions/ms583683(v=vs.100)) в обработчике событий [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) формы. Кроме того, задается свойство [Width](/previous-versions/ms837941(v=msdn.10)) свойства [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) объекта InkCollector. Наконец, задаются диапазоны полосы прокрутки и `UpdateZoomAndScroll` вызывается метод приложения.


```C++
private void InkZoom_Load(object sender, System.EventArgs e)
{
   // Create the pen used to draw the zoom rectangle
    blackPen = new Pen(Color.Black, 1);

    // Create the ink collector and associate it with the form
    myInkCollector = new InkCollector(pnlDrawingArea.Handle);

    // Set the pen width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth;

    // Enable ink collection
    myInkCollector.Enabled = true;

    // Define ink space size - note that the scroll bars
    // map directly to ink space
    hScrollBar.Minimum = 0;
    hScrollBar.Maximum = InkSpaceWidth;
    vScrollBar.Minimum = 0;
    vScrollBar.Maximum = InkSpaceHeight;

    // Set the scroll bars to map to the current zoom level
    UpdateZoomAndScroll();
}
```



## <a name="updating-the-zoom-and-scroll-values"></a>Обновление значений масштаба и прокрутки

Многие события влияют на область рисования сборщика рукописных данных. В `UpdateZoomAndScroll` методе матрица преобразования используется для масштабирования и преобразования сборщика рукописных данных в пределах окна.

> [!Note]  
> Метод [сетвиевтрансформ](/previous-versions/ms828514(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) применяет преобразование к штрихам и ширине пера, тогда как метод [сетобжекттрансформ](/previous-versions/ms828513(v=msdn.10)) применяет преобразование только к штрихам.

 

Наконец, `UpdateScrollBars` вызывается метод приложения, и форма принудительно обновляется.


```C++
// Create a transformation matrix
Matrix m = new Matrix();

// Apply the current scale factor
m.Scale(zoomFactor,zoomFactor);

// Apply the current translation factor - note that since 
// the scroll bars map directly to ink space, their values
// can be used directly.
m.Translate(-hScrollBar.Value, -vScrollBar.Value);

// ...
if (miScalePenWidth.Checked)
{
    myInkCollector.Renderer.SetViewTransform(m);
}
else
{
    myInkCollector.Renderer.SetObjectTransform(m);
}

// Set the scroll bars to map to the current zoom level
UpdateScrollBars();

Refresh();
```



## <a name="managing-the-scroll-bars"></a>Управление полосами прокрутки

`UpdateScrollBars`Метод настраивает полосы прокрутки для правильной работы с текущим размером окна, параметром масштабирования и расположением прокрутки в объекте [InkCollector](/previous-versions/ms583683(v=vs.100)). Этот метод вычисляет большое и небольшое изменение значений для вертикальной и горизонтальной полос прокрутки. Он также вычисляет текущее значение полос прокрутки и указывает, должны ли они быть видимыми. Метод [пикселтоинкспаце](/previous-versions/ms828505(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) обрабатывает преобразование пикселов в увеличенное пространство координат и учетные записи для любого масштабирования и прокрутки, которые применяются при преобразовании представления и объекта.


```C++
// Create a point representing the top left of the drawing area (in pixels)
Point ptUpperLeft = new Point(0, 0);

// Create a point representing the size of a small change
Point ptSmallChange = new Point(SmallChangeSize, SmallChangeSize);

// Create a point representing the lower right of the drawing area (in pixels)
Point ptLowerRight = new Point(hScrollBar.Width, vScrollBar.Height);

using (Graphics g = CreateGraphics())
{
    // Convert each of the points to ink space
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptUpperLeft);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptLowerRight);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptSmallChange);
}

// Set the SmallChange values (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.SmallChange = ptSmallChange.X - ptUpperLeft.X;
vScrollBar.SmallChange = ptSmallChange.Y - ptUpperLeft.Y;

// Set the LargeChange values to the drawing area width (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.LargeChange = ptLowerRight.X - ptUpperLeft.X;
vScrollBar.LargeChange = ptLowerRight.Y - ptUpperLeft.Y;

// If the scroll bars are not needed, hide them
hScrollBar.Visible = hScrollBar.LargeChange < hScrollBar.Maximum;
vScrollBar.Visible = vScrollBar.LargeChange < vScrollBar.Maximum;

// If the horizontal scroll bar value would run off of the drawing area, 
// adjust it
if(hScrollBar.Visible && (hScrollBar.Value + hScrollBar.LargeChange > hScrollBar.Maximum)) 
{
    hScrollBar.Value = hScrollBar.Maximum - hScrollBar.LargeChange;
}

// If the vertical scroll bar value would run off of the drawing area, 
// adjust it
if(vScrollBar.Visible && (vScrollBar.Value + vScrollBar.LargeChange > vScrollBar.Maximum))
{
    vScrollBar.Value = vScrollBar.Maximum - vScrollBar.LargeChange;
}
```



## <a name="zooming-to-a-rectangle"></a>Масштаб прямоугольника

`pnlDrawingArea`Обработчики событий панели управляют рисованием прямоугольника в окне. Если команда Zoom to Rect выбрана в меню режим, обработчик событий [MouseUp](/previous-versions/ms567618(v=vs.100)) вызывает `ZoomToRectangle` метод приложения. `ZoomToRectangle`Метод вычисляет ширину и высоту прямоугольника, проверяет наличие граничных условий, обновляет значения полосы прокрутки и коэффициент масштабирования, а затем вызывает `UpdateZoomAndScroll` метод приложения для применения новых параметров.

## <a name="closing-the-form"></a>Закрытие формы

Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
