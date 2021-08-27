---
description: В этом разделе приведен пример использования интерфейсов, связанных с геометрией, в объектной модели XPS.
ms.assetid: 2663c6fc-301e-4765-b37c-b5e29a714ce8
title: Геометрические объекты модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db68127535b37e216d28423a034083e979f58c714cbbbee875bc3f1621974bfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112094"
---
# <a name="xps-om-geometry-objects"></a>Геометрические объекты модели XPS

В этом разделе приведен пример использования интерфейсов, связанных с геометрией, в объектной модели XPS.

## <a name="create-a-rectangular-geometry"></a>Создание прямоугольной геометрии

В следующем примере кода создается объект Geometry, описывающий замкнутую прямоугольную фигуру.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMVisualCollection          *canvasVisuals = NULL;
    IXpsOMPath                      *pathSidebar = NULL;
    IXpsOMGeometry                  *xpsGeometry = NULL;
    IXpsOMGeometryFigure            *xpsFigure = NULL;
    IXpsOMGeometryFigureCollection  *xpsFigureCollection = NULL;
    IXpsOMSolidColorBrush           *sidebarBrush = NULL;

    XPS_POINT      startPoint;
    XPS_RECT       shape;

    // define the rectangle
    shape.x = 10.0f;
    shape.y = 10.0f;
    shape.height = 100.0f;
    shape.width = 200.0f;

    // set the start point
    startPoint.x = shape.x;
    startPoint.y = shape.y;

    // define the segment types to be straight lines
    XPS_SEGMENT_TYPE sidebarSegmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // define the points of the rectangular shape
    // other than the start point
    FLOAT sidebarSegmentData[6] = {
        shape.x,               shape.y + shape.height,
        shape.x + shape.width, shape.y + shape.height,
        shape.x + shape.width, shape.y
    };

    // set the lines to be solid (not stroked)
    BOOL sidebarSegmentStrokes[3] = {
        FALSE, FALSE, FALSE
    };

    // create the geometry figure interface
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &xpsFigure );

    // close the figure so that the last segment point is
    // connected to the start point
    hr = xpsFigure->SetIsClosed( TRUE );

    // set the shape to be filled by the fill brush
    hr = xpsFigure->SetIsFilled( TRUE );

    // set the segments using the information defined above
    hr = xpsFigure->SetSegments(
        3, 
        6, 
        sidebarSegmentTypes,
        sidebarSegmentData, 
        sidebarSegmentStrokes);

    // create a geometry using the figure just created
    hr = xpsFactory->CreateGeometry(&xpsGeometry);

    // get a pointer to the figure collection
    hr = xpsGeometry->GetFigures(&xpsFigureCollection);

    // and add the figure of the rectangle to the geometry
    hr = xpsFigureCollection->Append(xpsFigure);
```



Дополнительные сведения о добавлении сегментов к геометрической фигуре см. в примерах кода в разделах о методах [**икспсомжеометрифигуре:: жетсегментдата**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata) и [**Икспсомжеометрифигуре:: сетсегментс**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setsegments) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Икспсомжеометри**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[**Интерфейс Икспсомжеометрифигуре**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[**Метод Икспсомжеометрифигуре:: Жетсегментдата**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata)
</dt> <dt>

[**Метод Икспсомжеометрифигуре:: Сетсегментс**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setsegments)
</dt> <dt>

[**Интерфейс Икспсомжеометрифигуреколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> </dl>

 

 



