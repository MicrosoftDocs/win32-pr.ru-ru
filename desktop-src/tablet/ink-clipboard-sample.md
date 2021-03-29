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
# <a name="ink-clipboard-sample"></a><span data-ttu-id="69534-104">Пример рукописного буфера обмена</span><span class="sxs-lookup"><span data-stu-id="69534-104">Ink Clipboard Sample</span></span>

<span data-ttu-id="69534-105">Эта программа демонстрирует копирование и вставку рукописного ввода в другое приложение.</span><span class="sxs-lookup"><span data-stu-id="69534-105">This program demonstrates how to copy and paste ink into another application.</span></span> <span data-ttu-id="69534-106">Он также позволяет пользователю скопировать выбранные штрихи и вставить результат в существующий объект рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="69534-106">It also enables the user to copy a selection of strokes and paste the result into the existing ink object.</span></span>

<span data-ttu-id="69534-107">Доступны следующие режимы буфера обмена:</span><span class="sxs-lookup"><span data-stu-id="69534-107">The following clipboard modes are available:</span></span>

-   <span data-ttu-id="69534-108">Формат сериализованных рукописных данных (ISF)</span><span class="sxs-lookup"><span data-stu-id="69534-108">Ink serialized format (ISF)</span></span>
-   <span data-ttu-id="69534-109">Метафайл</span><span class="sxs-lookup"><span data-stu-id="69534-109">Metafile</span></span>
-   <span data-ttu-id="69534-110">EMF (Enhanced Metafile —расширенный метафайл)</span><span class="sxs-lookup"><span data-stu-id="69534-110">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="69534-111">Bitmap</span><span class="sxs-lookup"><span data-stu-id="69534-111">Bitmap</span></span>
-   <span data-ttu-id="69534-112">Рукописный ввод текста</span><span class="sxs-lookup"><span data-stu-id="69534-112">Text Ink</span></span>
-   <span data-ttu-id="69534-113">Нарисовать рукописный ввод</span><span class="sxs-lookup"><span data-stu-id="69534-113">Sketch Ink</span></span>

<span data-ttu-id="69534-114">Текстовые рукописные и эскизные краски — это два типа элементов управления рукописного ввода, которые используются в качестве текста или рисунков соответственно.</span><span class="sxs-lookup"><span data-stu-id="69534-114">Text ink and sketch ink are two types of ink controls used as text or drawing respectively.</span></span> <span data-ttu-id="69534-115">Можно вставить ISF, текстовый рукописный ввод и нарисовать рукописный ввод в существующую краску.</span><span class="sxs-lookup"><span data-stu-id="69534-115">It is possible to paste ISF, text ink, and sketch ink into existing ink.</span></span>

<span data-ttu-id="69534-116">В дополнение к буферу обмена в этом примере также показано, как выбрать штрихи с помощью инструмента "лассо".</span><span class="sxs-lookup"><span data-stu-id="69534-116">In addition to the clipboard, this sample also illustrates how to select strokes with the lasso tool.</span></span> <span data-ttu-id="69534-117">Пользователь может перемещать выбранные штрихи и изменять их атрибуты рисования.</span><span class="sxs-lookup"><span data-stu-id="69534-117">The user can move selected strokes and modify their drawing attributes.</span></span> <span data-ttu-id="69534-118">Эта функция является подмножеством функций выбора, которые уже предоставлены элементом управления наложением красок. Он реализуется здесь для наглядных целей.</span><span class="sxs-lookup"><span data-stu-id="69534-118">This functionality is a subset of the selection functionality already provided by the ink overlay control; it is implemented here for illustrative purposes.</span></span>

<span data-ttu-id="69534-119">В этом примере используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="69534-119">The following features are used in this sample:</span></span>

-   <span data-ttu-id="69534-120">Объект [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="69534-120">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>
-   <span data-ttu-id="69534-121">Поддержка рукописного ввода в буфере обмена.</span><span class="sxs-lookup"><span data-stu-id="69534-121">Ink clipboard support.</span></span>
-   <span data-ttu-id="69534-122">Использование Лассо с методом [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) .</span><span class="sxs-lookup"><span data-stu-id="69534-122">The use of the lasso with the [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method.</span></span>

<span data-ttu-id="69534-123">В этом примере демонстрируется визуализация рукописного ввода, копирование рукописного ввода и последующая запись рукописного ввода в другое приложение, например Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="69534-123">This sample demonstrates rendering ink, copying that ink, and then pasting the ink into another application such as Microsoft Paint.</span></span>

## <a name="collecting-ink-and-setting-up-the-form"></a><span data-ttu-id="69534-124">Сбор рукописных данных и настройка формы</span><span class="sxs-lookup"><span data-stu-id="69534-124">Collecting Ink and Setting Up the Form</span></span>

<span data-ttu-id="69534-125">Во-первых, сослаться на интерфейсы автоматизации планшетных ПК, которые устанавливаются вместе с <entity type="reg"/> пакетом SDK для Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="69534-125">First, reference the Tablet PC Automation interfaces, which are installed with the Microsoft Windows<entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="69534-126">Далее в форме объявляются некоторые константы и поля, отмеченные далее в этом примере.</span><span class="sxs-lookup"><span data-stu-id="69534-126">Next, the form declares some constants and fields that are noted later in this sample.</span></span>


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



<span data-ttu-id="69534-127">Наконец, в обработчике событий [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) формы инициализируется форма, создается объект [InkCollector](/previous-versions/ms583683(v=vs.100)) для формы, а также включается сборщик рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="69534-127">Finally, in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler, the form is initialized, an [InkCollector](/previous-versions/ms583683(v=vs.100)) object for the form is created and the ink collector is enabled.</span></span>


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a><span data-ttu-id="69534-128">Обработка событий меню</span><span class="sxs-lookup"><span data-stu-id="69534-128">Handling Menu Events</span></span>

<span data-ttu-id="69534-129">Обработчики событий пункта меню в основном обновляют состояние формы.</span><span class="sxs-lookup"><span data-stu-id="69534-129">The menu item event handlers primarily update the form's state.</span></span>

<span data-ttu-id="69534-130">Команда Clear удаляет прямоугольник выделения и удаляет штрихи из объекта [рукописного ввода](/previous-versions/ms583670(v=vs.100)) сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="69534-130">The Clear command removes the selection rectangle, and deletes the strokes from the ink collector's [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span>

<span data-ttu-id="69534-131">Команда exit отключает сборщик рукописных данных перед выходом из приложения.</span><span class="sxs-lookup"><span data-stu-id="69534-131">The Exit command disables the ink collector before exiting the application.</span></span>

<span data-ttu-id="69534-132">Меню Правка позволяет выполнять команды вырезания и копирования в зависимости от состояния выбора формы, а также включает команду вставки на основе содержимого буфера обмена, определенную с помощью метода [канпасте](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) объекта [Ink](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="69534-132">The Edit menu enables the Cut and Copy commands based on the selection state of the form, and enables the Paste command based on the contents of the clipboard, determined by using the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method.</span></span>

<span data-ttu-id="69534-133">Команды "вырезать" и "Копировать" используют вспомогательный метод для копирования рукописных данных в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="69534-133">The Cut and Copy commands both use a helper method to copy ink to the clipboard.</span></span> <span data-ttu-id="69534-134">Команда Cut использует вспомогательный метод для удаления выбранных штрихов.</span><span class="sxs-lookup"><span data-stu-id="69534-134">The Cut command uses a helper method to delete the selected strokes.</span></span>

<span data-ttu-id="69534-135">Команда вставки сначала проверяет метод [канпасте](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) объекта [рукописного ввода](/previous-versions/ms583670(v=vs.100)) , чтобы определить, можно ли вставить объект из буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="69534-135">The Paste command first checks the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method to see if the object on the clipboard can be pasted.</span></span> <span data-ttu-id="69534-136">Затем команда «Вставить» вычислит верхний левый угол области вставки, преобразует координаты пикселов в область рукописного ввода и вставляет штрихи из буфера обмена в сборщик рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="69534-136">The Paste command then computes the upper-left corner for the paste region, converts the coordinates from pixels to ink space, and pastes the strokes from the clipboard to the ink collector.</span></span> <span data-ttu-id="69534-137">Наконец, поле выбора обновляется.</span><span class="sxs-lookup"><span data-stu-id="69534-137">Finally, the selection box is updated.</span></span>


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



<span data-ttu-id="69534-138">Команды выбора и рукописного ввода обновляют режим приложения и атрибуты рисования по умолчанию, очищают текущее выделение, обновляют состояние меню и обновляют форму.</span><span class="sxs-lookup"><span data-stu-id="69534-138">The Select and Ink commands update the application mode and the default drawing attributes, clear the current selection, update the menu state, and refresh the form.</span></span> <span data-ttu-id="69534-139">Другие обработчики используют состояние приложения для выполнения правильной функции: Лассо или верстка рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="69534-139">Other handlers rely on the application state to perform the correct function, either lassoing or laying down ink.</span></span> <span data-ttu-id="69534-140">Кроме того, команда SELECT добавляет обработчики событий [невпаккетс](/previous-versions/ms567621(v=vs.100)) и [Stroke](/previous-versions/ms567622(v=vs.100)) в сборщик рукописных данных, а команда рукописного ввода удаляет эти обработчики событий из сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="69534-140">In addition, the Select command adds the [NewPackets](/previous-versions/ms567621(v=vs.100)) and [Stroke](/previous-versions/ms567622(v=vs.100)) event handlers to the ink collector and the Ink command removes these event handlers from the ink collector.</span></span>

<span data-ttu-id="69534-141">Форматы, доступные в буфере обмена при копировании штрихов, перечислены в меню Формат, и пользователь выбирает формат для копирования рукописных данных из этого списка.</span><span class="sxs-lookup"><span data-stu-id="69534-141">The formats that are available on the Clipboard when strokes are copied are listed on the Format menu, and the user selects the format for copying the ink from this list.</span></span> <span data-ttu-id="69534-142">Доступные типы форматов включают в себя формат сериализованного рукописного ввода (ISF), метафайл, расширенный метафайл и точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="69534-142">The types of formats available include Ink Serialized Format (ISF), metafile, enhanced metafile, and bitmap.</span></span> <span data-ttu-id="69534-143">Форматы рукописного ввода и текста наброски являются взаимоисключающими и полагаются на копируемый рукописный фрагмент в буфер обмена как объект OLE.</span><span class="sxs-lookup"><span data-stu-id="69534-143">The sketch ink and text ink formats are mutually exclusive, and rely on the ink being copied to the clipboard as an OLE object.</span></span>

<span data-ttu-id="69534-144">Меню Style (стиль) позволяет пользователю изменять свойства цвета и ширины пера и всех выбранных штрихов.</span><span class="sxs-lookup"><span data-stu-id="69534-144">The Style menu enables the user to change the color and width properties of the pen and any selected strokes.</span></span>

<span data-ttu-id="69534-145">Например, Красная команда устанавливает свойство [Color](/previous-versions/ms582103(v=vs.100)) для свойства [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) сборщика рукописных данных на красный цвет.</span><span class="sxs-lookup"><span data-stu-id="69534-145">For example, the Red command sets the [Color](/previous-versions/ms582103(v=vs.100)) property of the ink collector's [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) property to the color red.</span></span> <span data-ttu-id="69534-146">Так как свойство [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) объекта [cursor](/previous-versions/ms552104(v=vs.100)) не задано, все новые рукописные данные, нарисованные в сборщике рукописного ввода, наследуются цветом рисования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69534-146">Because the [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) property of the [Cursor](/previous-versions/ms552104(v=vs.100)) object has not been set, any new ink drawn to the ink collector inherits to default drawing color.</span></span> <span data-ttu-id="69534-147">Кроме того, если в данный момент выбраны какие-либо штрихи, то также обновляется свойство цвета для атрибутов рисования каждого штриха.</span><span class="sxs-lookup"><span data-stu-id="69534-147">Also, if any strokes are currently selected, each stroke's drawing attributes Color property is updated as well.</span></span>


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



## <a name="handling-mouse-events"></a><span data-ttu-id="69534-148">Обработка событий мыши</span><span class="sxs-lookup"><span data-stu-id="69534-148">Handling Mouse Events</span></span>

<span data-ttu-id="69534-149">Обработчик событий [MouseMove](/previous-versions/ms567617(v=vs.100)) проверяет режим приложения.</span><span class="sxs-lookup"><span data-stu-id="69534-149">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="69534-150">Если режим — Мовеинк, а кнопка мыши не нажата, обработчик перемещает штрихи с помощью метода Move коллекции [штрихов](/previous-versions/ms552701(v=vs.100)) и обновляет поле выбора.</span><span class="sxs-lookup"><span data-stu-id="69534-150">If the mode is MoveInk and a mouse button is down, then the handler moves the strokes by using the [Strokes](/previous-versions/ms552701(v=vs.100)) collection's Move method and updates the selection box.</span></span> <span data-ttu-id="69534-151">В противном случае обработчик проверяет, содержит ли прямоугольник выделения курсор, включает сбор рукописных данных, а также соответствующим образом задает курсор.</span><span class="sxs-lookup"><span data-stu-id="69534-151">Otherwise, the handler checks to determine whether the selection rectangle contains the cursor, enables ink collection accordingly, and also sets the cursor accordingly.</span></span>

<span data-ttu-id="69534-152">Обработчик событий [MouseDown](/previous-versions/ms567616(v=vs.100)) проверяет настройку курсора.</span><span class="sxs-lookup"><span data-stu-id="69534-152">The [MouseDown](/previous-versions/ms567616(v=vs.100)) event handler checks the cursor setting.</span></span> <span data-ttu-id="69534-153">Если курсор имеет значение [сизеалл](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), обработчик устанавливает для режима приложения значение мовеинк и записывает расположение курсора.</span><span class="sxs-lookup"><span data-stu-id="69534-153">If the cursor is set to [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), then the handler sets the application mode to MoveInk and records the cursor location.</span></span> <span data-ttu-id="69534-154">В противном случае, если имеется текущее выделение, очистите его.</span><span class="sxs-lookup"><span data-stu-id="69534-154">Otherwise, if there is a current selection, clear it.</span></span>

<span data-ttu-id="69534-155">Обработчик событий [MouseUp](/previous-versions/ms567618(v=vs.100)) проверяет режим приложения.</span><span class="sxs-lookup"><span data-stu-id="69534-155">The [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="69534-156">Если используется режим Мовеинк, обработчик устанавливает режим приложения на основе состояния проверки команды SELECT.</span><span class="sxs-lookup"><span data-stu-id="69534-156">If the mode is MoveInk, then the handler sets the application mode based on the Select command's checked state.</span></span>

<span data-ttu-id="69534-157">Событие [невпаккетс](/previous-versions/ms567621(v=vs.100)) возникает в режиме выделения, когда сборщик рукописных данных получает новые данные пакета.</span><span class="sxs-lookup"><span data-stu-id="69534-157">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised in selection mode when the ink collector receives new packet data.</span></span> <span data-ttu-id="69534-158">Если приложение находится в режиме выбора, необходимо перехватить новые пакеты и использовать их для рисования выделения Лассо.</span><span class="sxs-lookup"><span data-stu-id="69534-158">If the application is in selection mode, it is necessary to intercept the new packets and use them to draw the selection lasso.</span></span>

<span data-ttu-id="69534-159">Координаты каждого пакета преобразуются в пиксели, ограничены областью рисования и добавляются в коллекцию точек Лассо.</span><span class="sxs-lookup"><span data-stu-id="69534-159">Each packet's coordinate is converted to pixels, constrained to the drawing area, and added to the lasso's collection of points.</span></span> <span data-ttu-id="69534-160">Затем вызывается вспомогательный метод для рисования лассо в форме.</span><span class="sxs-lookup"><span data-stu-id="69534-160">A helper method is then called to draw the lasso on the form.</span></span>

## <a name="handling-a-new-stroke"></a><span data-ttu-id="69534-161">Обработка нового росчерка</span><span class="sxs-lookup"><span data-stu-id="69534-161">Handling a New Stroke</span></span>

<span data-ttu-id="69534-162">Событие [Stroke](/previous-versions/ms567622(v=vs.100)) возникает в режиме выбора при прорисовке нового штриха.</span><span class="sxs-lookup"><span data-stu-id="69534-162">The [Stroke](/previous-versions/ms567622(v=vs.100)) event is raised in the selection mode when a new stroke is drawn.</span></span> <span data-ttu-id="69534-163">Если приложение находится в режиме выбора, этот штрих соответствует Лассо и необходимо обновить сведения о выбранных штрихах.</span><span class="sxs-lookup"><span data-stu-id="69534-163">If the application is in selection mode, this stroke corresponds to the lasso and it is necessary to update the selected strokes' information.</span></span>

<span data-ttu-id="69534-164">Обработчик отменяет событие [Stroke](/previous-versions/ms567622(v=vs.100)) , проверяет наличие более двух точек Лассо, копирует коллекцию точек в массив объектов [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) и преобразует координаты точек в массиве из пикселов в пространство рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="69534-164">The handler cancels the [Stroke](/previous-versions/ms567622(v=vs.100)) event, checks for more than two lasso points, copies the Points collection to an array of [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) objects, and converts the coordinates of the points in the array from pixels to ink space.</span></span> <span data-ttu-id="69534-165">Затем обработчик использует метод [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) объекта [Ink](/previous-versions/ms583670(v=vs.100)) для получения штрихов, выбранных точками Лассо, и обновляет состояние выбора формы.</span><span class="sxs-lookup"><span data-stu-id="69534-165">Then, the handler uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to get the strokes selected by the lasso points and updates the selection state of the form.</span></span> <span data-ttu-id="69534-166">Наконец, штрих, вызвавший событие, удаляется из коллекции выбранных штрихов, коллекция точек Лассо очищается, а вспомогательный метод рисует прямоугольник выделения.</span><span class="sxs-lookup"><span data-stu-id="69534-166">Finally, the stroke that raised the event is removed from the collection of selected strokes, the lasso Points collection is emptied, and a helper method draws the selection rectangle.</span></span>


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



## <a name="copying-ink-to-the-clipboard"></a><span data-ttu-id="69534-167">Копирование рукописного ввода в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="69534-167">Copying Ink to the Clipboard</span></span>

<span data-ttu-id="69534-168">Вспомогательный метод Копинктоклипбоард создает значение [инкклипбоардформатс](/previous-versions/ms583681(v=vs.100)) , проверяет состояние меню Формат, чтобы обновить форматы, помещаемые в буфер обмена, и использует метод [клипбоардкопи](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) объекта [рукописного ввода](/previous-versions/ms583670(v=vs.100)) для копирования штрихов в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="69534-168">The CopyInkToClipboard helper method creates an [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) value, checks the Format menu's state to update the formats to put on the clipboard, and uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) method to copy the strokes to the clipboard.</span></span>


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



## <a name="updating-a-selection"></a><span data-ttu-id="69534-169">Обновление выделенного фрагмента</span><span class="sxs-lookup"><span data-stu-id="69534-169">Updating a Selection</span></span>

<span data-ttu-id="69534-170">Вспомогательный метод Сетселектион обновляет заданные Селектедстрокес и, если коллекция имеет **значение NULL** или **пуста**, прямоугольник выделения устанавливается равным пустому прямоугольнику.</span><span class="sxs-lookup"><span data-stu-id="69534-170">The SetSelection helper method updates the selectedStrokes filed and if the collection is **NULL** or **EMPTY**, the selection rectangle is set to the empty rectangle.</span></span> <span data-ttu-id="69534-171">Если выбранная коллекция [штрихов](/previous-versions/ms552701(v=vs.100)) не пуста, метод сетселектион выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="69534-171">If the selected [Strokes](/previous-versions/ms552701(v=vs.100)) collection is not empty the SetSelection method performs the following steps:</span></span>

-   <span data-ttu-id="69534-172">Определяет ограничивающий прямоугольник с помощью метода [жетбаундингбокс](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) коллекции штрихов</span><span class="sxs-lookup"><span data-stu-id="69534-172">Determines the bounding rectangle by using the [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) method of the strokes collection</span></span>
-   <span data-ttu-id="69534-173">Преобразует координаты прямоугольника из области рукописного ввода в Пиксели</span><span class="sxs-lookup"><span data-stu-id="69534-173">Converts the rectangle coordinates from ink space to pixels</span></span>
-   <span data-ttu-id="69534-174">Увеличивает прямоугольник, чтобы обеспечить некоторое визуальное пространство между ним и выбранными штрихами</span><span class="sxs-lookup"><span data-stu-id="69534-174">Inflates the rectangle to provide some visual space between it and the selected strokes</span></span>
-   <span data-ttu-id="69534-175">Создает маркеры выбора для текущего поля выбора</span><span class="sxs-lookup"><span data-stu-id="69534-175">Creates selection handles for the current selection box</span></span>

<span data-ttu-id="69534-176">Наконец, метод Сетселектион задает видимость дескрипторов выбора и устанавливает свойство [ауторедрав](/previous-versions/ms571706(v=vs.100)) сборщика рукописных данных в **значение false**, если штрихи выбраны.</span><span class="sxs-lookup"><span data-stu-id="69534-176">Finally, the SetSelection method sets the visibility of the selection handles and sets the ink collector's [AutoRedraw](/previous-versions/ms571706(v=vs.100)) property to **FALSE**, if strokes are selected.</span></span>


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



## <a name="drawing-the-lasso"></a><span data-ttu-id="69534-177">Рисование Лассо</span><span class="sxs-lookup"><span data-stu-id="69534-177">Drawing the Lasso</span></span>

<span data-ttu-id="69534-178">Лассо рисуется в виде ряда открытых точек, которые следуют за контуром штриха Лассо и пунктирной линией соединительной линии между двумя концами.</span><span class="sxs-lookup"><span data-stu-id="69534-178">The lasso is drawn as a series of open dots that follow the path of the lasso stroke and a dashed connector line between the two ends.</span></span> <span data-ttu-id="69534-179">Событие [невпаккетс](/previous-versions/ms567621(v=vs.100)) возникает при прорисовке Лассо, а обработчик событий передает сведения о штрихах в метод дравлассо.</span><span class="sxs-lookup"><span data-stu-id="69534-179">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised as the lasso is being drawn, and the event handler passes the stroke information to the DrawLasso method.</span></span>

<span data-ttu-id="69534-180">Вспомогательный метод Дравлассо сначала удаляет старую строку соединителя, а затем выполняет перебор точек в штрихе.</span><span class="sxs-lookup"><span data-stu-id="69534-180">The DrawLasso helper method first removes the old connector line and then iterates over the points in the stroke.</span></span> <span data-ttu-id="69534-181">Затем Дравлассо вычисляет место размещения точек вдоль штриха и отображает их.</span><span class="sxs-lookup"><span data-stu-id="69534-181">Then, DrawLasso calculates where to place the dots along the stroke and draws them.</span></span> <span data-ttu-id="69534-182">Наконец, он рисует новую линию соединителя.</span><span class="sxs-lookup"><span data-stu-id="69534-182">Finally, it draws a new connector line.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="69534-183">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="69534-183">Closing the Form</span></span>

<span data-ttu-id="69534-184">Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms583683(v=vs.100)) , минкколлектор.</span><span class="sxs-lookup"><span data-stu-id="69534-184">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object, myInkCollector.</span></span>

 

 
