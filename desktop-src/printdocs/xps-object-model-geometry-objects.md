---
description: В этом разделе приведен пример использования интерфейсов, связанных с геометрией, в объектной модели XPS.
ms.assetid: 2663c6fc-301e-4765-b37c-b5e29a714ce8
title: Геометрические объекты модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca767de311d2f2d49b0b194c372c0e69eaa637c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647267"
---
# <a name="xps-om-geometry-objects"></a><span data-ttu-id="06c75-103">Геометрические объекты модели XPS</span><span class="sxs-lookup"><span data-stu-id="06c75-103">XPS OM Geometry Objects</span></span>

<span data-ttu-id="06c75-104">В этом разделе приведен пример использования интерфейсов, связанных с геометрией, в объектной модели XPS.</span><span class="sxs-lookup"><span data-stu-id="06c75-104">This topic provides an example of using the geometry-related interfaces in an XPS OM.</span></span>

## <a name="create-a-rectangular-geometry"></a><span data-ttu-id="06c75-105">Создание прямоугольной геометрии</span><span class="sxs-lookup"><span data-stu-id="06c75-105">Create a rectangular geometry</span></span>

<span data-ttu-id="06c75-106">В следующем примере кода создается объект Geometry, описывающий замкнутую прямоугольную фигуру.</span><span class="sxs-lookup"><span data-stu-id="06c75-106">The following code example creates a geometry object that describes a closed rectangular shape.</span></span>


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



<span data-ttu-id="06c75-107">Дополнительные сведения о добавлении сегментов к геометрической фигуре см. в примерах кода в разделах о методах [**икспсомжеометрифигуре:: жетсегментдата**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata) и [**Икспсомжеометрифигуре:: сетсегментс**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setsegments) .</span><span class="sxs-lookup"><span data-stu-id="06c75-107">For more information about adding segments to a geometry figure, see the code examples in the [**IXpsOMGeometryFigure::GetSegmentData Method**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata) and [**IXpsOMGeometryFigure::SetSegments Method**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setsegments) reference topics.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06c75-108">См. также</span><span class="sxs-lookup"><span data-stu-id="06c75-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06c75-109">**Интерфейс Икспсомжеометри**</span><span class="sxs-lookup"><span data-stu-id="06c75-109">**IXpsOMGeometry Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="06c75-110">**Интерфейс Икспсомжеометрифигуре**</span><span class="sxs-lookup"><span data-stu-id="06c75-110">**IXpsOMGeometryFigure Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="06c75-111">**Метод Икспсомжеометрифигуре:: Жетсегментдата**</span><span class="sxs-lookup"><span data-stu-id="06c75-111">**IXpsOMGeometryFigure::GetSegmentData Method**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata)
</dt> <dt>

[<span data-ttu-id="06c75-112">**Метод Икспсомжеометрифигуре:: Сетсегментс**</span><span class="sxs-lookup"><span data-stu-id="06c75-112">**IXpsOMGeometryFigure::SetSegments Method**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setsegments)
</dt> <dt>

[<span data-ttu-id="06c75-113">**Интерфейс Икспсомжеометрифигуреколлектион**</span><span class="sxs-lookup"><span data-stu-id="06c75-113">**IXpsOMGeometryFigureCollection Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> </dl>

 

 



