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
# <a name="draw-graphics-in-an-xps-om"></a>Рисование графики в OM-объекте XPS

На этой странице описывается рисование графики в OM-объекте XPS.

Чтобы нарисовать векторную графику на странице, создайте экземпляр интерфейса [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) , заполните его нужным содержимым и добавьте его в список визуальных объектов страницы или холста. Интерфейс **икспсомпас** содержит такие свойства фигуры на основе вектора, как структура, цвет заливки, стиль линии и цвет линии. Фигура пути задается интерфейсом [**икспсомжеометри**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) , который содержит коллекцию интерфейсов [**икспсомжеометрифигуре**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) и (необязательно) интерфейс [**икспсомматрикстрансформ**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) . Можно использовать любой интерфейс, наследующий от интерфейса [**икспсомбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) , для заполнения периметра пути и внутренней части фигуры, описываемой путем.

Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Пример кода

В следующем примере кода создается простой путь, описывающий прямоугольник, который заполняется одним цветом.

### <a name="create-the-stroke-and-the-fill-brushes"></a>Создание мазков и кистей заливки

В первом разделе примера кода создается [**икспсомсолидколорбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) , который будет использоваться для заполнения объекта Path.


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



### <a name="define-the-shape"></a>Определение фигуры

Во втором разделе примера кода создается интерфейс [**икспсомжеометри**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) . Затем он создает интерфейс [**икспсомжеометрифигуре**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) , который указывает фигуру фигуры, и добавляет рисунок в интерфейс **икспсомжеометри** . В примере создается прямоугольник, заданный параметром *Rect*. Сегменты должны быть определены только для трех из четырех сторон прямоугольника. Периметр фигуры, прямоугольник в данном случае, начинается с начальной точки и расширяется в соответствии с сегментами фигуры геометрии. Установка свойства **"Closed** " в **значение true** означает, что прямоугольник закрыт путем добавления одного дополнительного сегмента, соединяющего конец последнего сегмента с начальной точкой.


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



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a>Создайте путь и добавьте его в коллекцию визуальных элементов.

В последнем разделе этого примера кода создается и настраивается объект Path, а затем он добавляется в список визуальных объектов страницы.


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



## <a name="best-practices"></a>Рекомендации

Добавьте текстовое описание фигуры, заданное интерфейсом [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) . Чтобы воспользоваться преимуществами пользователей с ослабленным зрением, используйте методы [**сетакцессибилитишортдескриптион**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) и [**сетакцессибилитилонгдескриптион**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) , чтобы предоставить текстовое содержимое для функций поддержки специальных возможностей, таких как средства чтения с экрана.

## <a name="additional-information"></a>Дополнительные сведения

В примере кода на этой странице используется интерфейс [**икспсомсолидколорбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) в качестве кисти заливки и кисть Stroke для пути. В дополнение к интерфейсу **икспсомсолидколорбруш** можно использовать интерфейс [**икспсомградиентбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**икспсомимажебруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)или [**икспсомвисуалбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) .

Штрих — это линия, которую можно прорисовать вокруг периметра фигуры. [Спецификация XML Paper](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) поддерживает множество различных стилей линий обводки. Чтобы задать стиль линии обводки, задайте свойства Stroke с помощью следующих методов интерфейса [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) :

-   [**Сетстрокебрушлокал**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) или [**сетстрокебрушлукуп**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) для установки кисти обводки
-   [**Жетстрокедашес**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) для получения коллекции штрихов штриха, описывающей штрихи
-   [**Сетстрокедашкап**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) to и [**сетстрокедашоффсет**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) для описания внешнего вида штриховой штриха
-   [**Сетстрокиндлинекап**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) и [**сетстрокестартлинекап**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) для определения стиля завершения строки
-   [**Сетстрокелинежоин**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) и [**сетстрокемитерлимит**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) , описывающие, как соединяются сегменты
-   [**Сетстрокесиккнесс**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) для установки толщины штриха

## <a name="related-topics"></a>См. также

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Навигация по OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[Запись текста в объектную модель XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Размещение изображений в объектной модели XPS](place-images-in-an-xps-om.md)
</dt> <dt>

[Запись объектной модели XPS в документ XPS](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[Печать OM-объекта XPS](print-an-xps-om.md)
</dt> <dt>

**Используется на этой странице**
</dt> <dt>

[**иопкпартури**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**икспсомжеометри**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[**икспсомжеометрифигуре**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[**икспсомжеометрифигуреколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[**икспсомобжектфактори**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**икспсомсолидколорбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**икспсомвисуалколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[Инициализация объектной модели XPS](xps-object-model-initialization.md)
</dt> <dt>

[Справочник по API документов XPS](xps-programming-reference.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
