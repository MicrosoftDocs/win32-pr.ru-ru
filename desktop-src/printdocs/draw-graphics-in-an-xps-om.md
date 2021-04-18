---
description: На этой странице описывается рисование графики в OM-объекте XPS.
ms.assetid: 2384b522-208a-48db-ae0d-f82fa0214d09
title: Рисование графики в OM-объекте XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabbf8cfb821c80dfff43e2e7844331c8920f726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711933"
---
# <a name="draw-graphics-in-an-xps-om"></a><span data-ttu-id="7cac9-103">Рисование графики в OM-объекте XPS</span><span class="sxs-lookup"><span data-stu-id="7cac9-103">Draw Graphics in an XPS OM</span></span>

<span data-ttu-id="7cac9-104">На этой странице описывается рисование графики в OM-объекте XPS.</span><span class="sxs-lookup"><span data-stu-id="7cac9-104">This page describes how to draw graphics in an XPS OM.</span></span>

<span data-ttu-id="7cac9-105">Чтобы нарисовать векторную графику на странице, создайте экземпляр интерфейса [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) , заполните его нужным содержимым и добавьте его в список визуальных объектов страницы или холста.</span><span class="sxs-lookup"><span data-stu-id="7cac9-105">To draw vector-based graphics in a page, instantiate an [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface, populate it with the desired content, and add it to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="7cac9-106">Интерфейс **икспсомпас** содержит такие свойства фигуры на основе вектора, как структура, цвет заливки, стиль линии и цвет линии.</span><span class="sxs-lookup"><span data-stu-id="7cac9-106">An **IXpsOMPath** interface contains such properties of a vector-based shape as the outline, fill color, line style, and line color.</span></span> <span data-ttu-id="7cac9-107">Фигура пути задается интерфейсом [**икспсомжеометри**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) , который содержит коллекцию интерфейсов [**икспсомжеометрифигуре**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) и (необязательно) интерфейс [**икспсомматрикстрансформ**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) .</span><span class="sxs-lookup"><span data-stu-id="7cac9-107">The path's shape is specified by an [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface, which contains a collection of [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interfaces and, optionally, an [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) interface.</span></span> <span data-ttu-id="7cac9-108">Можно использовать любой интерфейс, наследующий от интерфейса [**икспсомбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) , для заполнения периметра пути и внутренней части фигуры, описываемой путем.</span><span class="sxs-lookup"><span data-stu-id="7cac9-108">You can use any interface that inherits from the [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) interface to fill the perimeter of the path and the interior of the shape that is described by the path.</span></span>

<span data-ttu-id="7cac9-109">Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="7cac9-109">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="7cac9-110">Пример кода</span><span class="sxs-lookup"><span data-stu-id="7cac9-110">Code Example</span></span>

<span data-ttu-id="7cac9-111">В следующем примере кода создается простой путь, описывающий прямоугольник, который заполняется одним цветом.</span><span class="sxs-lookup"><span data-stu-id="7cac9-111">The following code example creates a simple path that describes a rectangle that is filled with a single color.</span></span>

### <a name="create-the-stroke-and-the-fill-brushes"></a><span data-ttu-id="7cac9-112">Создание мазков и кистей заливки</span><span class="sxs-lookup"><span data-stu-id="7cac9-112">Create the stroke and the fill brushes</span></span>

<span data-ttu-id="7cac9-113">В первом разделе примера кода создается [**икспсомсолидколорбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) , который будет использоваться для заполнения объекта Path.</span><span class="sxs-lookup"><span data-stu-id="7cac9-113">The first section of the code example creates the [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) that will be used to fill the path object.</span></span>


```C++
    HRESULT               hr = S_OK;

    XPS_COLOR             xpsColor;
    IXpsOMSolidColorBrush *xpsFillBrush = NULL;
    IXpsOMSolidColorBrush *xpsStrokeBrush = NULL;

    // Set the fill brush color to RED.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColor,
        NULL,          // color profile resource
        &xpsFillBrush);
    // The color profile resource parameter is NULL because
    //  this color type does not use a color profile resource.

    // Set the stroke brush color to BLACK.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0x00;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
            &xpsColor,
            NULL, // This color type does not use a color profile resource.
            &xpsStrokeBrush);

    // The brushes are released below after they have been used.
```



### <a name="define-the-shape"></a><span data-ttu-id="7cac9-114">Определение фигуры</span><span class="sxs-lookup"><span data-stu-id="7cac9-114">Define the shape</span></span>

<span data-ttu-id="7cac9-115">Во втором разделе примера кода создается интерфейс [**икспсомжеометри**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) .</span><span class="sxs-lookup"><span data-stu-id="7cac9-115">The second section of the code example creates the [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface.</span></span> <span data-ttu-id="7cac9-116">Затем он создает интерфейс [**икспсомжеометрифигуре**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) , который указывает фигуру фигуры, и добавляет рисунок в интерфейс **икспсомжеометри** .</span><span class="sxs-lookup"><span data-stu-id="7cac9-116">It then creates the [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interface that specifies the figure's shape, and adds the figure to the **IXpsOMGeometry** interface.</span></span> <span data-ttu-id="7cac9-117">В примере создается прямоугольник, заданный параметром *Rect*.</span><span class="sxs-lookup"><span data-stu-id="7cac9-117">The example creates a rectangle that is specified by *rect*.</span></span> <span data-ttu-id="7cac9-118">Сегменты должны быть определены только для трех из четырех сторон прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="7cac9-118">Segments must be defined for only three of the four sides of the rectangle.</span></span> <span data-ttu-id="7cac9-119">Периметр фигуры, прямоугольник в данном случае, начинается с начальной точки и расширяется в соответствии с сегментами фигуры геометрии.</span><span class="sxs-lookup"><span data-stu-id="7cac9-119">The perimeter of the shape, the rectangle in this case, starts from the start point and extends as defined by the segments of the geometry figure.</span></span> <span data-ttu-id="7cac9-120">Установка свойства **"Closed** " в **значение true** означает, что прямоугольник закрыт путем добавления одного дополнительного сегмента, соединяющего конец последнего сегмента с начальной точкой.</span><span class="sxs-lookup"><span data-stu-id="7cac9-120">Setting the **IsClosed** property to **TRUE** indicates that the rectangle is closed by adding one additional segment that connects the end of the last segment to the start point.</span></span>


```C++
    // rect is initialized outside of the sample and 
    //  contains the coordinates of the rectangular geometry to create.
    XPS_RECT                            rect = {0,0,100,100};       

    HRESULT                             hr = S_OK;
    IXpsOMGeometryFigure                *rectFigure;
    IXpsOMGeometry                      *imageRectGeometry;
    IXpsOMGeometryFigureCollection      *geomFigureCollection;

    // Define the start point and create an empty figure.
    XPS_POINT                           startPoint = {rect.x, rect.y};
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    // Define the segments of the geometry figure.
    //  First, define the type of each segment.
    XPS_SEGMENT_TYPE segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE,  // each segment is a straight line
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // Define the x and y coordinates of each corner of the figure
    //  the start point has already been defined so only the 
    //  remaining three corners need to be defined.
    FLOAT segmentData[6] = {
        rect.x,                (rect.y + rect.height),
        (rect.x + rect.width), (rect.y + rect.height), 
        (rect.x + rect.width), rect.y 
    };

    // Describe if the segments are stroked (that is if the segment lines
    //  should be drawn as a line).
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE // Yes, draw each of the segment lines.
    };

    // Add the segment data to the figure.
    hr = rectFigure->SetSegments(
                        3, 
                        6, 
                        segmentTypes, 
                        segmentData, 
                        segmentStrokes);

    // Set the closed and filled properties of the figure.
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
 
    // Create the geometry object.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    
    // Get a pointer to the figure collection interface of the geometry...
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );

    // ...and then add the figure created above to this geometry.
    hr = geomFigureCollection->Append( rectFigure );
    // If not needed for anything else, release the rectangle figure.
    rectFigure->Release();

    // when done adding figures, release the figure collection. 
    geomFigureCollection->Release();

    //  When done with the geometry object, release the object.
    // imageRectGeometry->Release();
    //  In this case, imageRectGeometry is used in the next sample
    //  so the geometry object is not released, yet.
    
```



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a><span data-ttu-id="7cac9-121">Создайте путь и добавьте его в коллекцию визуальных элементов.</span><span class="sxs-lookup"><span data-stu-id="7cac9-121">Create the path and add it to the visual collection</span></span>

<span data-ttu-id="7cac9-122">В последнем разделе этого примера кода создается и настраивается объект Path, а затем он добавляется в список визуальных объектов страницы.</span><span class="sxs-lookup"><span data-stu-id="7cac9-122">The final section of this code example creates and configures the path object, then adds it to the page's list of visual objects.</span></span>


```C++
    HRESULT                    hr = S_OK;
    // The page interface pointer is initialized outside of this sample.
    IXpsOMPath                *rectPath = NULL;
    IXpsOMVisualCollection    *pageVisuals = NULL;

    // Create the new path object.
    hr = xpsFactory->CreatePath( &rectPath );

    // Add the geometry to the path.
    //  imageRectGeometry is initialized outside of this example.
    hr = rectPath->SetGeometryLocal( imageRectGeometry );

    // Set the short description of the path to provide
    //  a textual description of the object for accessibility.
    hr = rectPath->SetAccessibilityShortDescription( L"Red Rectangle" );
    
    // Set the fill and stroke brushes to use the brushes 
    //  created in the first section.
    hr = rectPath->SetFillBrushLocal( xpsFillBrush );
    hr = rectPath->SetStrokeBrushLocal( xpsStrokeBrush);

    // Get the visual collection of this page and add this path to it.
    hr = xpsPage->GetVisuals( &pageVisuals );
    hr = pageVisuals->Append( rectPath );
    // If not needed for anything else, release the rectangle path.
    rectPath->Release();
    
    // When done with the visual collection, release it.
    pageVisuals->Release();

    // When finished with the brushes, release the interface pointers.
    if (NULL != xpsFillBrush) xpsFillBrush->Release();
    if (NULL != xpsStrokeBrush) xpsStrokeBrush->Release();

    // When done with the geometry interface, release it.
    imageRectGeometry->Release();

    // When done with the path interface, release it.
    rectPath->Release();

```



## <a name="best-practices"></a><span data-ttu-id="7cac9-123">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="7cac9-123">Best Practices</span></span>

<span data-ttu-id="7cac9-124">Добавьте текстовое описание фигуры, заданное интерфейсом [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) .</span><span class="sxs-lookup"><span data-stu-id="7cac9-124">Add a textual description of the shape that is specified by the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface.</span></span> <span data-ttu-id="7cac9-125">Чтобы воспользоваться преимуществами пользователей с ослабленным зрением, используйте методы [**сетакцессибилитишортдескриптион**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) и [**сетакцессибилитилонгдескриптион**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) , чтобы предоставить текстовое содержимое для функций поддержки специальных возможностей, таких как средства чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="7cac9-125">For the benefit of visually impaired users, use the [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) and [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) methods to provide textual content for accessibility support features, such as screen readers.</span></span>

## <a name="additional-information"></a><span data-ttu-id="7cac9-126">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="7cac9-126">Additional Information</span></span>

<span data-ttu-id="7cac9-127">В примере кода на этой странице используется интерфейс [**икспсомсолидколорбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) в качестве кисти заливки и кисть Stroke для пути.</span><span class="sxs-lookup"><span data-stu-id="7cac9-127">The code example on this page uses an [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) interface as the fill brush and stroke brush for the path.</span></span> <span data-ttu-id="7cac9-128">В дополнение к интерфейсу **икспсомсолидколорбруш** можно использовать интерфейс [**икспсомградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**икспсомимажебруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)или [**икспсомвисуалбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) .</span><span class="sxs-lookup"><span data-stu-id="7cac9-128">In addition to the **IXpsOMSolidColorBrush** interface, you can use an [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush), or [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) interface.</span></span>

<span data-ttu-id="7cac9-129">Штрих — это линия, которую можно прорисовать вокруг периметра фигуры.</span><span class="sxs-lookup"><span data-stu-id="7cac9-129">The stroke is the line that can be drawn around the perimeter of the figure.</span></span> <span data-ttu-id="7cac9-130">[Спецификация XML Paper](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) поддерживает множество различных стилей линий обводки.</span><span class="sxs-lookup"><span data-stu-id="7cac9-130">The [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) supports many different stroke line styles.</span></span> <span data-ttu-id="7cac9-131">Чтобы задать стиль линии обводки, задайте свойства Stroke с помощью следующих методов интерфейса [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) :</span><span class="sxs-lookup"><span data-stu-id="7cac9-131">To specify the stroke line style, set the stroke properties with the following methods of the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface:</span></span>

-   <span data-ttu-id="7cac9-132">[**Сетстрокебрушлокал**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) или [**сетстрокебрушлукуп**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) для установки кисти обводки</span><span class="sxs-lookup"><span data-stu-id="7cac9-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) or [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) to set the stroke brush</span></span>
-   <span data-ttu-id="7cac9-133">[**Жетстрокедашес**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) для получения коллекции штрихов штриха, описывающей штрихи</span><span class="sxs-lookup"><span data-stu-id="7cac9-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) to get the stroke dash collection that describes the strokes</span></span>
-   <span data-ttu-id="7cac9-134">[**Сетстрокедашкап**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) to и [**сетстрокедашоффсет**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) для описания внешнего вида штриховой штриха</span><span class="sxs-lookup"><span data-stu-id="7cac9-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) to and [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) to describe the appearance of a dashed stroke</span></span>
-   <span data-ttu-id="7cac9-135">[**Сетстрокиндлинекап**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) и [**сетстрокестартлинекап**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) для определения стиля завершения строки</span><span class="sxs-lookup"><span data-stu-id="7cac9-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) and [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) to define the line termination style</span></span>
-   <span data-ttu-id="7cac9-136">[**Сетстрокелинежоин**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) и [**сетстрокемитерлимит**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) , описывающие, как соединяются сегменты</span><span class="sxs-lookup"><span data-stu-id="7cac9-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) and [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) to describe how the segments are joined</span></span>
-   <span data-ttu-id="7cac9-137">[**Сетстрокесиккнесс**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) для установки толщины штриха</span><span class="sxs-lookup"><span data-stu-id="7cac9-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) to set the stroke thickness</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cac9-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7cac9-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7cac9-139">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="7cac9-139">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="7cac9-140">Навигация по OM XPS</span><span class="sxs-lookup"><span data-stu-id="7cac9-140">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="7cac9-141">Запись текста в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="7cac9-141">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="7cac9-142">Размещение изображений в объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="7cac9-142">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="7cac9-143">Запись объектной модели XPS в документ XPS</span><span class="sxs-lookup"><span data-stu-id="7cac9-143">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="7cac9-144">Печать OM-объекта XPS</span><span class="sxs-lookup"><span data-stu-id="7cac9-144">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="7cac9-145">**Используется на этой странице**</span><span class="sxs-lookup"><span data-stu-id="7cac9-145">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="7cac9-146">**иопкпартури**</span><span class="sxs-lookup"><span data-stu-id="7cac9-146">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="7cac9-147">**икспсомжеометри**</span><span class="sxs-lookup"><span data-stu-id="7cac9-147">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="7cac9-148">**икспсомжеометрифигуре**</span><span class="sxs-lookup"><span data-stu-id="7cac9-148">**IXpsOMGeometryFigure**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="7cac9-149">**икспсомжеометрифигуреколлектион**</span><span class="sxs-lookup"><span data-stu-id="7cac9-149">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[<span data-ttu-id="7cac9-150">**икспсомобжектфактори**</span><span class="sxs-lookup"><span data-stu-id="7cac9-150">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="7cac9-151">**икспсомпаже**</span><span class="sxs-lookup"><span data-stu-id="7cac9-151">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="7cac9-152">**икспсомпас**</span><span class="sxs-lookup"><span data-stu-id="7cac9-152">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[<span data-ttu-id="7cac9-153">**икспсомсолидколорбруш**</span><span class="sxs-lookup"><span data-stu-id="7cac9-153">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="7cac9-154">**икспсомвисуалколлектион**</span><span class="sxs-lookup"><span data-stu-id="7cac9-154">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="7cac9-155">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="7cac9-155">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="7cac9-156">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="7cac9-156">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="7cac9-157">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="7cac9-157">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="7cac9-158">XPS</span><span class="sxs-lookup"><span data-stu-id="7cac9-158">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
