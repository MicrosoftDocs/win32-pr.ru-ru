---
description: В примере базового анализа рукописного ввода показано, как класс InkAnalyzer делит рукописный ввод на различные сегменты слов и рисования. Этот образец является обновленной версией примера для разделения рукописного текста.
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: Базовый анализ рукописного ввода — пример
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94ac73ca9049169c6e406059665a66e8eaa6f3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719284"
---
# <a name="basic-ink-analysis-sample"></a><span data-ttu-id="39179-103">Базовый анализ рукописного ввода — пример</span><span class="sxs-lookup"><span data-stu-id="39179-103">Basic Ink Analysis Sample</span></span>

<span data-ttu-id="39179-104">В примере базового анализа рукописного ввода показано, как класс [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) делит рукописный ввод на различные сегменты слов и рисования.</span><span class="sxs-lookup"><span data-stu-id="39179-104">The Basic Ink Analysis sample shows how the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class divides ink into various word and drawing segments.</span></span>

<span data-ttu-id="39179-105">Этот образец является обновленной версией примера для [разделения рукописного текста](ink-divider-sample.md).</span><span class="sxs-lookup"><span data-stu-id="39179-105">This sample is an updated version of the [Ink Divider Sample](ink-divider-sample.md).</span></span> <span data-ttu-id="39179-106">В примере с разделителем рукописного ввода используется класс- [Разделитель](/previous-versions/ms839398(v=msdn.10)) , в этом примере используется более новый и предпочтительный API инканалисис.</span><span class="sxs-lookup"><span data-stu-id="39179-106">Whereas the Ink Divider Sample uses the [Divider](/previous-versions/ms839398(v=msdn.10)) class, this sample uses the newer and preferred InkAnalysis API.</span></span> <span data-ttu-id="39179-107">API Инканалисис объединяет [рекогнизерконтекст](/previous-versions/ms828542(v=msdn.10)) и разделитель в один API и расширяет функциональность обоих типов.</span><span class="sxs-lookup"><span data-stu-id="39179-107">The InkAnalysis API combines the [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) and Divider into one API and expands on the functionality of both.</span></span>

<span data-ttu-id="39179-108">При обновлении формы в примере выводится прямоугольник вокруг каждой проанализированной единицы: слова, строки, абзацы, области записи, рисунки и маркеры.</span><span class="sxs-lookup"><span data-stu-id="39179-108">When you update the form, the sample draws a rectangle around each analyzed unit: words, lines, paragraphs, writing regions, drawings and bullets.</span></span> <span data-ttu-id="39179-109">В форме используются разные цвета для разных единиц.</span><span class="sxs-lookup"><span data-stu-id="39179-109">The form uses different colors for the different units.</span></span> <span data-ttu-id="39179-110">Прямоугольники также увеличены различными суммами, чтобы ни один прямоугольник не был скрыт другими.</span><span class="sxs-lookup"><span data-stu-id="39179-110">The rectangles are also enlarged by different amounts to ensure that no one rectangle is obscured by any others.</span></span>

<span data-ttu-id="39179-111">В следующей таблице указаны цвет и увеличение для каждой проанализированной единицы.</span><span class="sxs-lookup"><span data-stu-id="39179-111">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="39179-112">Проанализированная единица</span><span class="sxs-lookup"><span data-stu-id="39179-112">Analyzed unit</span></span>             | <span data-ttu-id="39179-113">Цвет прямоугольника</span><span class="sxs-lookup"><span data-stu-id="39179-113">Color of rectangle</span></span> | <span data-ttu-id="39179-114">Увеличение прямоугольника (в пикселях)</span><span class="sxs-lookup"><span data-stu-id="39179-114">Rectangle enlargement (pixels)</span></span> |
|---------------------------|--------------------|--------------------------------|
| <span data-ttu-id="39179-115">Word</span><span class="sxs-lookup"><span data-stu-id="39179-115">Word</span></span><br/>           | <span data-ttu-id="39179-116">Зеленый</span><span class="sxs-lookup"><span data-stu-id="39179-116">Green</span></span><br/>   | <span data-ttu-id="39179-117">1</span><span class="sxs-lookup"><span data-stu-id="39179-117">1</span></span><br/>                   |
| <span data-ttu-id="39179-118">Линия</span><span class="sxs-lookup"><span data-stu-id="39179-118">Line</span></span><br/>           | <span data-ttu-id="39179-119">Пурпурный</span><span class="sxs-lookup"><span data-stu-id="39179-119">Magenta</span></span><br/> | <span data-ttu-id="39179-120">3</span><span class="sxs-lookup"><span data-stu-id="39179-120">3</span></span><br/>                   |
| <span data-ttu-id="39179-121">Paragraph</span><span class="sxs-lookup"><span data-stu-id="39179-121">Paragraph</span></span><br/>      | <span data-ttu-id="39179-122">Синий</span><span class="sxs-lookup"><span data-stu-id="39179-122">Blue</span></span><br/>    | <span data-ttu-id="39179-123">5</span><span class="sxs-lookup"><span data-stu-id="39179-123">5</span></span><br/>                   |
| <span data-ttu-id="39179-124">Регион для записи</span><span class="sxs-lookup"><span data-stu-id="39179-124">Writing region</span></span><br/> | <span data-ttu-id="39179-125">Желтый</span><span class="sxs-lookup"><span data-stu-id="39179-125">Yellow</span></span><br/>  | <span data-ttu-id="39179-126">7</span><span class="sxs-lookup"><span data-stu-id="39179-126">7</span></span><br/>                   |
| <span data-ttu-id="39179-127">Рисование</span><span class="sxs-lookup"><span data-stu-id="39179-127">Drawing</span></span><br/>        | <span data-ttu-id="39179-128">Красный</span><span class="sxs-lookup"><span data-stu-id="39179-128">Red</span></span><br/>     | <span data-ttu-id="39179-129">1</span><span class="sxs-lookup"><span data-stu-id="39179-129">1</span></span><br/>                   |
| <span data-ttu-id="39179-130">Стандартный</span><span class="sxs-lookup"><span data-stu-id="39179-130">Bullet</span></span><br/>         | <span data-ttu-id="39179-131">Оранжевый</span><span class="sxs-lookup"><span data-stu-id="39179-131">Orange</span></span><br/>  | <span data-ttu-id="39179-132">1</span><span class="sxs-lookup"><span data-stu-id="39179-132">1</span></span><br/>                   |



 

<span data-ttu-id="39179-133">Можно стереть штрихи в форме.</span><span class="sxs-lookup"><span data-stu-id="39179-133">You can erase strokes in the form.</span></span> <span data-ttu-id="39179-134">В примере приложения можно переключаться между рукописным вводом и режимом стирания, чтобы изменить функцию пера.</span><span class="sxs-lookup"><span data-stu-id="39179-134">In the sample application, you can toggle between Ink and Erase mode to change the function of the pen.</span></span>


```C++
        private void miInk_Click(object sender, System.EventArgs e)
        {
            // Turn on the inking mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Ink;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = true;
            miErase.Checked = false;

            // Update the UI
            this.Refresh();
        }

        private void miErase_Click(object sender, System.EventArgs e)
        {
            // Turn on the ink deletion mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Delete;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = false;
            miErase.Checked = true;

            // Update the UI
            this.Refresh();
        }
```



<span data-ttu-id="39179-135">При добавлении или удалении штрихов образцы обновляют [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="39179-135">When you add or delete strokes, the samples updates the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span></span>


```C++
        private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
        {
            // Filter out the eraser stroke.
            if (InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
            {

                // Add the new stroke to the InkAnalyzer's stroke collection
                myInkAnalyzer.AddStroke(e.Stroke);

                if (miAutomaticLayoutAnalysis.Checked)
                {
                    // Invoke an analysis operation on the background thread
                    myInkAnalyzer.BackgroundAnalyze();
                }
            }
        }

        void myInkOverlay_StrokeDeleting(object sender, InkOverlayStrokesDeletingEventArgs e)
        {
            // Remove the strokes to be deleted from the InkAnalyzer's stroke collection
            myInkAnalyzer.RemoveStrokes(e.StrokesToDelete);

            // If automatic layout analysis is turned on, analyze the ink on the background thread
            if ( miAutomaticLayoutAnalysis.Checked )
            {
                // Invoke an analysis operation on the background thread
                myInkAnalyzer.BackgroundAnalyze ( );
            }
        }
```



<span data-ttu-id="39179-136">Обратите внимание, что в меню режим автоматический анализ макета включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39179-136">Notice that in the Mode menu, Automatic Layout Analysis is on by default.</span></span> <span data-ttu-id="39179-137">Если этот параметр выбран, обработчики событий [Stroke](/previous-versions/ms835344(v=msdn.10)) и [строкесделетинг](/previous-versions/ms835360(v=msdn.10)) объекта [InkOverlay](/previous-versions/ms833057(v=msdn.10)) вызывают метод [баккграунданализе](/previous-versions/ms568972(v=vs.100)) каждый раз при создании или удалении штриха.</span><span class="sxs-lookup"><span data-stu-id="39179-137">With this option selected, the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Stroke](/previous-versions/ms835344(v=msdn.10)) and [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) event handlers call the [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method every time a stroke is created or deleted.</span></span>

> [!Note]  
> <span data-ttu-id="39179-138">Вызов метода [Analyze](/previous-versions/ms568971(v=vs.100)) объекта [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) с более чем несколькими штрихами создает заметную задержку в приложении.</span><span class="sxs-lookup"><span data-stu-id="39179-138">Calling the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object's [Analyze](/previous-versions/ms568971(v=vs.100)) method with more than a few strokes present creates a noticeable delay in an application.</span></span> <span data-ttu-id="39179-139">Это обусловлено тем, что анализ — это синхронная операция анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="39179-139">This is because Analyze is a synchronous ink analysis operation.</span></span> <span data-ttu-id="39179-140">На практике вызывайте метод Analyze только в том случае, если требуется результат.</span><span class="sxs-lookup"><span data-stu-id="39179-140">In practice, call the Analyze method only when you need the result.</span></span> <span data-ttu-id="39179-141">В противном случае используйте асинхронный метод [баккграунданализе](/previous-versions/ms568972(v=vs.100)) , как показано в примере.</span><span class="sxs-lookup"><span data-stu-id="39179-141">Otherwise use the asynchronous [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method, as shown in the sample.</span></span>

 

## <a name="handling-the-analysis-results"></a><span data-ttu-id="39179-142">Обработка результатов анализа</span><span class="sxs-lookup"><span data-stu-id="39179-142">Handling the Analysis Results</span></span>

<span data-ttu-id="39179-143">В примере создаются два массива для хранения различных прямоугольников: горизонтальные или повернутые.</span><span class="sxs-lookup"><span data-stu-id="39179-143">The sample creates two arrays to hold the various rectangles, either horizontal or rotated.</span></span> <span data-ttu-id="39179-144">Используйте повернутый ограничивающий прямоугольник для получения угла, на котором написано строка слов.</span><span class="sxs-lookup"><span data-stu-id="39179-144">Use a rotated bounding box to get the angle on which a line of words is written.</span></span> <span data-ttu-id="39179-145">В примере показаны свойства, возвращаемые [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) , и отображается ограничивающий прямоугольник или повернутый ограничивающий прямоугольник (в зависимости от выбранного пункта меню).</span><span class="sxs-lookup"><span data-stu-id="39179-145">The sample shows the properties returned by the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) and displays the bounding box or the rotated bounding box (depending on the menu selection).</span></span>


```C++
      private Rectangle[] GetHorizontalBBoxes(Guid nodeType, int inflate)
        {
            // Declare the array of rectangles to hold the result
            Rectangle[] analysisRects;

            // Get the division units from the division result of division type
            ContextNodeCollection nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // If there is at least one unit, we construct the rectangles
            if ((null != nodes) && (0 < nodes.Count))
            {
                // We need to convert rectangles from ink units to
                // pixel units. For that, we need Graphics object
                // to pass to InkRenderer.InkSpaceToPixel method
                using (Graphics g = drawArea.CreateGraphics())
                {
                    // Construct the rectangles
                    analysisRects = new Rectangle[nodes.Count];

                    // InkRenderer.InkSpaceToPixel takes Point as parameter. 
                    // Create two Point objects to point to (Top, Left) and
                    // (Width, Height) properties of rectangle. (Width, Height)
                    // is used instead of (Right, Bottom) because (Right, Bottom)
                    // are read-only properties on Rectangle
                    Point ptLocation = new Point();
                    Point ptSize = new Point();

                    // Index into the bounding boxes
                    int i = 0;

                    // Iterate through the collection of division units to obtain the bounding boxes
                    foreach (ContextNode node in nodes)
                    {
                        // Get the bounding box of the strokes of the division unit
                        analysisRects[i] = node.Location.GetBounds();

                        // The bounding box is in ink space unit. Convert them into pixel unit. 
                        ptLocation = analysisRects[i].Location;
                        ptSize.X = analysisRects[i].Width;
                        ptSize.Y = analysisRects[i].Height;

                        // Convert the Location from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptLocation);

                        // Convert the Size from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptSize);

                        // Assign the result back to the corresponding properties
                        analysisRects[i].Location = ptLocation;
                        analysisRects[i].Width = ptSize.X;
                        analysisRects[i].Height = ptSize.Y;

                        // Inflate the rectangle by inflate pixels in both directions
                        analysisRects[i].Inflate(inflate, inflate);

                        // Increment the index
                        ++i;
                    }

                } // Relinquish the Graphics object
            }
            else
            {
                // Otherwise we return null
                analysisRects = null;
            }

            // Return the Rectangle[] object
            return analysisRects;
        }

        private System.Collections.ArrayList GetRotatedBBoxes(Guid nodeType, int inflate)
        {
            //Find the correct collection of results nodes.
            ContextNodeCollection Nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // Declare the array list to hold the results; 
            // This array represents the four points of a rectangle, with the first point
            // copied again to complete the cycle of points.

            ArrayList polygonPoints = new ArrayList(Nodes.Count);

            // Cycle through each results node, get and convert the
            // rotated bounding box points
            foreach (ContextNode node in Nodes)
            {
                //Declare the point array
                Point[] rotatedBoundingBox = null;

                //Switch on the type of ContextNode to cast into the
                //appropriate type.  This is required to access the 
                //type specific property "RotatedBoundingBox" which
                //is not found on all ContextNode types.
                if (nodeType == ContextNodeType.InkWord)
                {
                    rotatedBoundingBox = ((InkWordNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Line)
                {
                    rotatedBoundingBox = ((LineNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Paragraph)
                {
                    rotatedBoundingBox = ((ParagraphNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.WritingRegion ||
                         nodeType == ContextNodeType.InkDrawing ||
                         nodeType == ContextNodeType.InkBullet )
                {

                    // Rotated Bounding Boxes are not a supported option for 
                    // Writing Regions or Drawings.  We return the axis aligned 
                    // bounding box instead
                    Rectangle rect = node.Location.GetBounds();

                    // We need to create a looped list of 4 points to be consistent
                    // with the way InkAnalysis represents rotated bounding boxes.  
                    rotatedBoundingBox = new Point[4];

                    rotatedBoundingBox[0] = new Point(rect.X, rect.Y);
                    rotatedBoundingBox[1] = new Point(rect.Right, rect.Y);
                    rotatedBoundingBox[2] = new Point(rect.Right, rect.Bottom);
                    rotatedBoundingBox[3] = new Point(rect.X, rect.Bottom);

                }


                if (null != rotatedBoundingBox)
                {
                    // We need to convert rectangles from ink units to
                    // pixel units. For that, we need Graphics object
                    // to pass to InkRenderer.InkSpaceToPixel method
                    using (Graphics g = drawArea.CreateGraphics())
                    {
                        // convert each of the points from ink space to pixel space
                        for (int i = 0; i < rotatedBoundingBox.Length; i++)
                        {
                            myInkOverlay.Renderer.InkSpaceToPixel(g, ref rotatedBoundingBox[i]);
                        }

                        //inflate the points by calling helper method
                        InflateHelperMethod(ref rotatedBoundingBox, inflate);

                        // increment the node portion of the polygonPoints array
                        polygonPoints.Add(rotatedBoundingBox);
                    }
                }
            }
            //Return the results
            return polygonPoints;
        }
```



<span data-ttu-id="39179-146">Средство синтаксического анализа вычисляет [жетротатедбаундингбокс](/previous-versions/ms569544(v=vs.100)) во время анализа.</span><span class="sxs-lookup"><span data-stu-id="39179-146">The parser calculates [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) during analysis.</span></span> <span data-ttu-id="39179-147">Доступ к сведениям из повернутых ограничивающих прямоугольников в приложении можно получить по ряду полезных причин.</span><span class="sxs-lookup"><span data-stu-id="39179-147">You can access the information from the rotated bounding boxes in your application for a number of useful reasons:</span></span>

-   <span data-ttu-id="39179-148">Обнаружение или рисование границ одной линии, абзаца или другой единицы.</span><span class="sxs-lookup"><span data-stu-id="39179-148">Detect or draw the bounds of a single line, paragraph, or other unit.</span></span>
-   <span data-ttu-id="39179-149">Определите угол, в котором записывается строка или абзац.</span><span class="sxs-lookup"><span data-stu-id="39179-149">Determine the angle at which a line or paragraph is written.</span></span>
-   <span data-ttu-id="39179-150">Реализуйте такие функции, как выделение линий, абзацев или других единиц.</span><span class="sxs-lookup"><span data-stu-id="39179-150">Implement features such as selection for a line, paragraph, or other unit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39179-151">См. также</span><span class="sxs-lookup"><span data-stu-id="39179-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39179-152">Базовый анализ и распознавание рукописного текста</span><span class="sxs-lookup"><span data-stu-id="39179-152">Basic Recognition and Ink Analysis</span></span>](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[<span data-ttu-id="39179-153">Образец печатной формы</span><span class="sxs-lookup"><span data-stu-id="39179-153">Scanned Paper Form Sample</span></span>](scanned-paper-form-sample.md)
</dt> <dt>

[<span data-ttu-id="39179-154">Пример рукописного разделителя</span><span class="sxs-lookup"><span data-stu-id="39179-154">Ink Divider Sample</span></span>](ink-divider-sample.md)
</dt> </dl>

 

