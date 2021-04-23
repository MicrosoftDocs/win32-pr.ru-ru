---
description: В этом образце программы показано, как изменять масштаб и прокручивать рукописный ввод.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Пример масштабирования рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20253a3f56b2a03b5a6dad45ab9a8b72090b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540407"
---
# <a name="ink-zoom-sample"></a><span data-ttu-id="993e4-103">Пример масштабирования рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="993e4-103">Ink Zoom Sample</span></span>

<span data-ttu-id="993e4-104">В этом образце программы показано, как изменять масштаб и прокручивать рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="993e4-104">This sample program demonstrates how to zoom and scroll ink.</span></span> <span data-ttu-id="993e4-105">В частности, он позволяет пользователю увеличивать и уменьшать рукописные данные с приращениями.</span><span class="sxs-lookup"><span data-stu-id="993e4-105">In particular, it enables the user to zoom in and out of ink in increments.</span></span> <span data-ttu-id="993e4-106">Здесь также показано, как увеличить масштаб в определенном регионе с помощью прямоугольника масштабирования.</span><span class="sxs-lookup"><span data-stu-id="993e4-106">It also demonstrates how to zoom into a particular region using a zoom rectangle.</span></span> <span data-ttu-id="993e4-107">Наконец, в этом образце показано, как выполнять накопление рукописного ввода с различными коэффициентами масштабирования и как настроить прокрутку в масштабной области рисования.</span><span class="sxs-lookup"><span data-stu-id="993e4-107">Finally, this sample illustrates how to collect ink at different zoom ratios and how to set up scrolling within the zoomed drawing area.</span></span>

<span data-ttu-id="993e4-108">В этом примере для выполнения масштабирования и прокрутки используются представление объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов и преобразования объектов.</span><span class="sxs-lookup"><span data-stu-id="993e4-108">In the sample, the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's view and object transforms are used to perform zooming and scrolling.</span></span> <span data-ttu-id="993e4-109">Преобразование «представление» применяется к точкам и ширине пера.</span><span class="sxs-lookup"><span data-stu-id="993e4-109">The view transform applies to the points and the pen width.</span></span> <span data-ttu-id="993e4-110">Преобразование объекта применяется только к точкам.</span><span class="sxs-lookup"><span data-stu-id="993e4-110">The object transform applies only to the points.</span></span> <span data-ttu-id="993e4-111">Пользователь может управлять тем, какое преобразование используется, изменяя элемент ширина пера шкалы в меню режим.</span><span class="sxs-lookup"><span data-stu-id="993e4-111">The user can control which transform is used by changing the Scale Pen Width item on the Mode menu.</span></span>

> [!Note]  
> <span data-ttu-id="993e4-112">При отправке сообщения возникают проблемы при выполнении некоторых вызовов COM для определенных методов интерфейса (например,[**инкрендерер. сетвиевтрансформ**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) и [**инкрендерер. сетобжекттрансформ**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)).</span><span class="sxs-lookup"><span data-stu-id="993e4-112">It is problematic to perform some COM calls on certain interface methods ([**InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) and [**InkRenderer.SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), for example) when a message has been SENT.</span></span> <span data-ttu-id="993e4-113">Когда сообщения отправляются, они должны быть упакованы в очередь сообщений POST.</span><span class="sxs-lookup"><span data-stu-id="993e4-113">When messages are SENT, they need to be marshalled to the POST message queue.</span></span> <span data-ttu-id="993e4-114">Чтобы решить эту проблему, проверьте, обрабатывается ли сообщение от POST путем вызова [**инсендмесссажеекс**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) , и опубликуйте сообщение в себе, если сообщение было отправлено.</span><span class="sxs-lookup"><span data-stu-id="993e4-114">To address this scenario, test whether you are handling a message from POST by calling [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) and POST the message to yourself if the message was SENT.</span></span>

 

<span data-ttu-id="993e4-115">В этом примере используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="993e4-115">The following features are used in this sample:</span></span>

-   <span data-ttu-id="993e4-116">Объект [InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="993e4-116">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object</span></span>
-   <span data-ttu-id="993e4-117">Метод [сетвиевтрансформ](/previous-versions/ms828514(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов</span><span class="sxs-lookup"><span data-stu-id="993e4-117">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method</span></span>
-   <span data-ttu-id="993e4-118">Метод [сетобжекттрансформ](/previous-versions/ms828513(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) отчетов</span><span class="sxs-lookup"><span data-stu-id="993e4-118">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method</span></span>

## <a name="initializing-the-form"></a><span data-ttu-id="993e4-119">Инициализация формы</span><span class="sxs-lookup"><span data-stu-id="993e4-119">Initializing the Form</span></span>

<span data-ttu-id="993e4-120">Во-первых, образец ссылается на интерфейсы автоматизации планшетных ПК, которые предоставляются в пакете SDK для Windows Vista или Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="993e4-120">First, the sample references the Tablet PC Automation interfaces, which are provided in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="993e4-121">В примере объявляются объект [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` и некоторые закрытые члены, помогающие при масштабировании.</span><span class="sxs-lookup"><span data-stu-id="993e4-121">The sample declares an [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector`, and some private members to help with scaling.</span></span>


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



<span data-ttu-id="993e4-122">Затем в примере создается и включается объект [InkCollector](/previous-versions/ms583683(v=vs.100)) в обработчике событий [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) формы.</span><span class="sxs-lookup"><span data-stu-id="993e4-122">Then the sample creates and enables the [InkCollector](/previous-versions/ms583683(v=vs.100)) in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="993e4-123">Кроме того, задается свойство [Width](/previous-versions/ms837941(v=msdn.10)) свойства [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) объекта InkCollector.</span><span class="sxs-lookup"><span data-stu-id="993e4-123">Also, the [Width](/previous-versions/ms837941(v=msdn.10)) property of the InkCollector object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property is set.</span></span> <span data-ttu-id="993e4-124">Наконец, задаются диапазоны полосы прокрутки и `UpdateZoomAndScroll` вызывается метод приложения.</span><span class="sxs-lookup"><span data-stu-id="993e4-124">Finally, the scroll bar ranges are defined and the application's `UpdateZoomAndScroll` method is called.</span></span>


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



## <a name="updating-the-zoom-and-scroll-values"></a><span data-ttu-id="993e4-125">Обновление значений масштаба и прокрутки</span><span class="sxs-lookup"><span data-stu-id="993e4-125">Updating the Zoom and Scroll Values</span></span>

<span data-ttu-id="993e4-126">Многие события влияют на область рисования сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="993e4-126">The drawing area of the ink collector is affected by many events.</span></span> <span data-ttu-id="993e4-127">В `UpdateZoomAndScroll` методе матрица преобразования используется для масштабирования и преобразования сборщика рукописных данных в пределах окна.</span><span class="sxs-lookup"><span data-stu-id="993e4-127">In the `UpdateZoomAndScroll` method, a transformation matrix is used to both scale and translate the ink collector within the window.</span></span>

> [!Note]  
> <span data-ttu-id="993e4-128">Метод [сетвиевтрансформ](/previous-versions/ms828514(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) применяет преобразование к штрихам и ширине пера, тогда как метод [сетобжекттрансформ](/previous-versions/ms828513(v=msdn.10)) применяет преобразование только к штрихам.</span><span class="sxs-lookup"><span data-stu-id="993e4-128">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method applies the transform to both the strokes and the pen width, while the [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method only applies the transform to the strokes.</span></span>

 

<span data-ttu-id="993e4-129">Наконец, `UpdateScrollBars` вызывается метод приложения, и форма принудительно обновляется.</span><span class="sxs-lookup"><span data-stu-id="993e4-129">Finally, the application's `UpdateScrollBars` method is called and the form is forced to refresh.</span></span>


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



## <a name="managing-the-scroll-bars"></a><span data-ttu-id="993e4-130">Управление полосами прокрутки</span><span class="sxs-lookup"><span data-stu-id="993e4-130">Managing the Scroll Bars</span></span>

<span data-ttu-id="993e4-131">`UpdateScrollBars`Метод настраивает полосы прокрутки для правильной работы с текущим размером окна, параметром масштабирования и расположением прокрутки в объекте [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="993e4-131">The `UpdateScrollBars` method sets up the scroll bars to work correctly with the current window size, zoom setting, and scroll location within the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span> <span data-ttu-id="993e4-132">Этот метод вычисляет большое и небольшое изменение значений для вертикальной и горизонтальной полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="993e4-132">This method calculates the large change and small change values for the vertical and horizontal scroll bars.</span></span> <span data-ttu-id="993e4-133">Он также вычисляет текущее значение полос прокрутки и указывает, должны ли они быть видимыми.</span><span class="sxs-lookup"><span data-stu-id="993e4-133">It also calculates the current value of the scroll bars and whether they should be visible.</span></span> <span data-ttu-id="993e4-134">Метод [пикселтоинкспаце](/previous-versions/ms828505(v=msdn.10)) объекта модуля [подготовки](/previous-versions/ms828481(v=msdn.10)) обрабатывает преобразование пикселов в увеличенное пространство координат и учетные записи для любого масштабирования и прокрутки, которые применяются при преобразовании представления и объекта.</span><span class="sxs-lookup"><span data-stu-id="993e4-134">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method handles the conversion from pixels to the zoomed coordinate space and accounts for any scaling and scrolling that is applied through the view and object transforms.</span></span>


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



## <a name="zooming-to-a-rectangle"></a><span data-ttu-id="993e4-135">Масштаб прямоугольника</span><span class="sxs-lookup"><span data-stu-id="993e4-135">Zooming to a Rectangle</span></span>

<span data-ttu-id="993e4-136">`pnlDrawingArea`Обработчики событий панели управляют рисованием прямоугольника в окне.</span><span class="sxs-lookup"><span data-stu-id="993e4-136">The `pnlDrawingArea` panel event handlers manage drawing the rectangle to the window.</span></span> <span data-ttu-id="993e4-137">Если команда Zoom to Rect выбрана в меню режим, обработчик событий [MouseUp](/previous-versions/ms567618(v=vs.100)) вызывает `ZoomToRectangle` метод приложения.</span><span class="sxs-lookup"><span data-stu-id="993e4-137">If the Zoom To Rect command is checked on the Mode menu, then the [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler calls the application's `ZoomToRectangle` method.</span></span> <span data-ttu-id="993e4-138">`ZoomToRectangle`Метод вычисляет ширину и высоту прямоугольника, проверяет наличие граничных условий, обновляет значения полосы прокрутки и коэффициент масштабирования, а затем вызывает `UpdateZoomAndScroll` метод приложения для применения новых параметров.</span><span class="sxs-lookup"><span data-stu-id="993e4-138">The `ZoomToRectangle` method calculates the width and height of the rectangle, checks for boundary conditions, updates the scroll bar values and the scale factor, and then calls the application's `UpdateZoomAndScroll` method to apply the new settings.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="993e4-139">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="993e4-139">Closing the Form</span></span>

<span data-ttu-id="993e4-140">Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="993e4-140">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
