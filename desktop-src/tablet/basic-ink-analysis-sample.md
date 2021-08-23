---
description: В примере базового анализа рукописного ввода показано, как класс InkAnalyzer делит рукописный ввод на различные сегменты слов и рисования. Этот образец является обновленной версией примера для разделения рукописного текста.
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: Базовый анализ рукописного ввода — пример
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ab307deac8ac58a741b0c7f332986b09074f4f5c6a8afa53f0156a94916bf16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660834"
---
# <a name="basic-ink-analysis-sample"></a>Базовый анализ рукописного ввода — пример

В примере базового анализа рукописного ввода показано, как класс [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) делит рукописный ввод на различные сегменты слов и рисования.

Этот образец является обновленной версией примера для [разделения рукописного текста](ink-divider-sample.md). В примере с разделителем рукописного ввода используется класс- [Разделитель](/previous-versions/ms839398(v=msdn.10)) , в этом примере используется более новый и предпочтительный API инканалисис. API Инканалисис объединяет [рекогнизерконтекст](/previous-versions/ms828542(v=msdn.10)) и разделитель в один API и расширяет функциональность обоих типов.

При обновлении формы в примере выводится прямоугольник вокруг каждой проанализированной единицы: слова, строки, абзацы, области записи, рисунки и маркеры. В форме используются разные цвета для разных единиц. Прямоугольники также увеличены различными суммами, чтобы ни один прямоугольник не был скрыт другими.

В следующей таблице указаны цвет и увеличение для каждой проанализированной единицы.



| Проанализированная единица             | Цвет прямоугольника | Увеличение прямоугольника (в пикселях) |
|---------------------------|--------------------|--------------------------------|
| Word<br/>           | Зеленый<br/>   | 1<br/>                   |
| Линия<br/>           | Пурпурный<br/> | 3<br/>                   |
| Paragraph<br/>      | Синий<br/>    | 5<br/>                   |
| Регион для записи<br/> | Желтый<br/>  | 7<br/>                   |
| Рисование<br/>        | Красный<br/>     | 1<br/>                   |
| Стандартный<br/>         | Оранжевый<br/>  | 1<br/>                   |



 

Можно стереть штрихи в форме. В примере приложения можно переключаться между рукописным вводом и режимом стирания, чтобы изменить функцию пера.


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



При добавлении или удалении штрихов образцы обновляют [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).


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



Обратите внимание, что в меню режим автоматический анализ макета включен по умолчанию. Если этот параметр выбран, обработчики событий [Stroke](/previous-versions/ms835344(v=msdn.10)) и [строкесделетинг](/previous-versions/ms835360(v=msdn.10)) объекта [InkOverlay](/previous-versions/ms833057(v=msdn.10)) вызывают метод [баккграунданализе](/previous-versions/ms568972(v=vs.100)) каждый раз при создании или удалении штриха.

> [!Note]  
> Вызов метода [Analyze](/previous-versions/ms568971(v=vs.100)) объекта [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) с более чем несколькими штрихами создает заметную задержку в приложении. Это обусловлено тем, что анализ — это синхронная операция анализа рукописного ввода. На практике вызывайте метод Analyze только в том случае, если требуется результат. В противном случае используйте асинхронный метод [баккграунданализе](/previous-versions/ms568972(v=vs.100)) , как показано в примере.

 

## <a name="handling-the-analysis-results"></a>Обработка результатов анализа

В примере создаются два массива для хранения различных прямоугольников: горизонтальные или повернутые. Используйте повернутый ограничивающий прямоугольник для получения угла, на котором написано строка слов. В примере показаны свойства, возвращаемые [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) , и отображается ограничивающий прямоугольник или повернутый ограничивающий прямоугольник (в зависимости от выбранного пункта меню).


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



Средство синтаксического анализа вычисляет [жетротатедбаундингбокс](/previous-versions/ms569544(v=vs.100)) во время анализа. Доступ к сведениям из повернутых ограничивающих прямоугольников в приложении можно получить по ряду полезных причин.

-   Обнаружение или рисование границ одной линии, абзаца или другой единицы.
-   Определите угол, в котором записывается строка или абзац.
-   Реализуйте такие функции, как выделение линий, абзацев или других единиц.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Базовый анализ и распознавание рукописного текста](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[Образец печатной формы](scanned-paper-form-sample.md)
</dt> <dt>

[Пример рукописного разделителя](ink-divider-sample.md)
</dt> </dl>

 

