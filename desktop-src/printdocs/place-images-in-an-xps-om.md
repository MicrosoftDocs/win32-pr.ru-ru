---
description: Описывает размещение изображений в объектной модели XPS.
ms.assetid: 4c7e3630-7331-47d7-91cc-da3cc2b7f8c9
title: Размещение изображений в объектной модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f72b5d1b1380cd870f9ff6b7a1cd15763e5b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702915"
---
# <a name="place-images-in-an-xps-om"></a><span data-ttu-id="267ad-103">Размещение изображений в объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="267ad-103">Place Images in an XPS OM</span></span>

<span data-ttu-id="267ad-104">Описывает размещение изображений в объектной модели XPS.</span><span class="sxs-lookup"><span data-stu-id="267ad-104">Describes how to place images in an XPS OM.</span></span>

<span data-ttu-id="267ad-105">Чтобы поместить изображения в объектную модель XPS, создайте объект Path, определяющий расположение и контур изображения, а затем используйте кисть изображения для заливки пути.</span><span class="sxs-lookup"><span data-stu-id="267ad-105">To place images in an XPS OM, create a path object that defines the location and outline of an image, then use an image brush to fill the path.</span></span> <span data-ttu-id="267ad-106">Добавьте созданный объект пути в список визуальных объектов страницы или холста, чтобы его можно было визуализировать с другим визуальным содержимым.</span><span class="sxs-lookup"><span data-stu-id="267ad-106">Add the created path object to the page's or canvas' list of visual objects, so that it can be rendered with the other visual content.</span></span>

<span data-ttu-id="267ad-107">Прежде чем использовать эти примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="267ad-107">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="267ad-108">Пример кода</span><span class="sxs-lookup"><span data-stu-id="267ad-108">Code Example</span></span>

### <a name="create-image-resource"></a><span data-ttu-id="267ad-109">Создать ресурс изображения</span><span class="sxs-lookup"><span data-stu-id="267ad-109">Create image resource</span></span>

<span data-ttu-id="267ad-110">Если исходный образ недоступен в модели XPS OM в качестве ресурса образа, сначала создайте ресурс образа:</span><span class="sxs-lookup"><span data-stu-id="267ad-110">If the source image is not available in the XPS OM as an image resource, first create the image resource:</span></span>


```C++
    HRESULT                hr = S_OK;
    IStreamPtr             imageStream; // the resulting image stream
    IOpcPartUri            *imagePartUri;
    IXpsOMImageResource    *imageResource;

     XPS_RECT    rect = {0.0f, 0.0f, 0.0f, 0.0f}; // set to image size

    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
            imageFileName, &imageStream );

    hr = xpsFactory->CreatePartUri( imagePartName, &imagePartUri );

    imageType; // set to type of image being read in
    hr = xpsFactory->CreateImageResource ( 
        imageStream,
        imageType,
        imagePartUri,
        &imageResource);
    imagePartUri->Release();
    imageStream->Release();

    // imageResource can now be used by other parts in the XPS OM.
```



### <a name="place-image-into-visual-collection"></a><span data-ttu-id="267ad-111">Поместить изображение в визуальную коллекцию</span><span class="sxs-lookup"><span data-stu-id="267ad-111">Place image into visual collection</span></span>

<span data-ttu-id="267ad-112">Если исходный образ доступен в объектной модели XPS в качестве ресурса изображения, его можно использовать для создания объекта кисти изображения и добавления его в качестве кисти заливки к контуру, описывающему расположение и размер изображения на странице.</span><span class="sxs-lookup"><span data-stu-id="267ad-112">If the source image is available in the XPS OM as an image resource, it can be used to create an image brush object and added as the fill brush to the path that describes the image location and size in the page.</span></span>


```C++
    // These variables are initialized outside of this code example,
    //  for example, as the parameters of a method or from some 
    //  preceding program code.

    // dimensions of the image in pixels
    XPS_SIZE    bmpDim = {0,0} ; 

    // DPI resolution values obtained from image
    FLOAT        dpiX = 96.0f;
    FLOAT        dpiY = 96.0f;
    
    // initialize viewport values 
    XPS_RECT    viewPort = {0.0,0.0,0.0,0.0};

    // initialize viewbox values
    XPS_RECT    viewBox = {0.0,0.0,0.0,0.0}; 

    // These are part of this code example.
    IXpsOMPath *imageRectPath;
    IXpsOMImageBrush *imageBrush;
    IXpsOMVisualCollection *pageVisuals;

    // Describe image source dimensions and set viewbox to be the 
    // entire image DIP width of image. 
    //  Example: 
    //    600 image pixels, 300 dpi -> 2 inches -> 2 * 96 = 192 DIP width
    viewBox.width = FLOAT((double)bmpDim.width * 96.0 / dpiX); 
    viewBox.height = FLOAT((double)bmpDim.height * 96.0 / dpiY);

    // Describe the size and position of the image destination.
    //  rect is an XPS_RECT structure that is initialized outside
    //  of this sample for example, it might be passed in as a parameter.

    // destination rectangle
    viewPort.x = rect.x;
    viewPort.y = rect.y;
    viewPort.width = rect.width;
    viewPort.height = rect.height;

    // Create the image brush.
    hr = xpsFactory->CreateImageBrush(imageResource, &viewBox, &viewPort, 
        reinterpret_cast<IXpsOMImageBrush**>(&imageBrush));

    // Create the path that describes the outline of the image on the page.
    //  This step uses the function described in the next code example.
    hr = CreateRectanglePath(xpsFactory, &rect,
        reinterpret_cast<IXpsOMPath**>(&imageRectPath));

    // Set the accessibility description for the path object as required.
    hr = imageRectPath->SetAccessibilityShortDescription( shortDescText );

    // Set the image brush to be the fill brush for this path.
    hr = imageRectPath->SetFillBrushLocal( imageBrush );

    // Get the list of visuals for this page...
    hr = xpsPage->GetVisuals( &pageVisuals );

    // ...and add the completed path to the list.
    hr = pageVisuals->Append( imageRectPath );

    // Release locally created interfaces.
    if (NULL != pageVisuals) pageVisuals->Release();
    if (NULL != imageRectPath) imageRectPath->Release();
    if (NULL != imageBrush) imageBrush->Release();

```



### <a name="create-path-object-for-image"></a><span data-ttu-id="267ad-113">Создание объекта пути для изображения</span><span class="sxs-lookup"><span data-stu-id="267ad-113">Create path object for image</span></span>

<span data-ttu-id="267ad-114">Следующий метод принимает структуру **\_ Rect в формате XPS** и создает прямоугольный путь.</span><span class="sxs-lookup"><span data-stu-id="267ad-114">The following method accepts an **XPS\_RECT** structure and creates a rectangular path.</span></span>


```C++
HRESULT 
CreateRectanglePath(
    __in  IXpsOMObjectFactory   *xpsFactory,
    __in  const XPS_RECT        *rect,
    __out IXpsOMPath            **rectPath
)
{
   
    HRESULT hr = S_OK;

    IXpsOMGeometryFigure           *rectFigure;
    IXpsOMGeometry                 *imageRectGeometry;
    IXpsOMGeometryFigureCollection *geomFigureCollection;

    // Define start point and three of the four sides of the rectangle.
    //  The fourth side is implied by setting the path type to CLOSED.
    XPS_POINT            startPoint = {rect->x, rect->y};
    XPS_SEGMENT_TYPE     segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };
    FLOAT segmentData[6] = {
        rect->x,              rect->y+rect->height, 
        rect->x+rect->width,  rect->y+rect->height, 
        rect->x+rect->width,  rect->y 
    };
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE
    };

    // Create a closed geometry figure using the three 
    //  segments defined above.

    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
    hr = rectFigure->SetSegments( 3, 6, 
            segmentTypes, segmentData, segmentStrokes );

    // Create a geometry that consists of the figure created above.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );
    hr = geomFigureCollection->Append( rectFigure );

    // Create the path that consists of the geometry created above
    //  and return the pointer in the parameter passed in to the function.
    hr = xpsFactory->CreatePath( reinterpret_cast<IXpsOMPath**>(rectPath) );
    hr = (*rectPath)->SetGeometryLocal( imageRectGeometry );

    // The calling method will release these interfaces when 
    //  it is done with them.

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="267ad-115">См. также</span><span class="sxs-lookup"><span data-stu-id="267ad-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="267ad-116">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="267ad-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="267ad-117">Навигация по OM XPS</span><span class="sxs-lookup"><span data-stu-id="267ad-117">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="267ad-118">Запись текста в объектную модель XPS</span><span class="sxs-lookup"><span data-stu-id="267ad-118">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="267ad-119">Рисование графики в OM-объекте XPS</span><span class="sxs-lookup"><span data-stu-id="267ad-119">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="267ad-120">Запись объектной модели XPS в документ XPS</span><span class="sxs-lookup"><span data-stu-id="267ad-120">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="267ad-121">Печать OM-объекта XPS</span><span class="sxs-lookup"><span data-stu-id="267ad-121">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="267ad-122">**Используется на этой странице**</span><span class="sxs-lookup"><span data-stu-id="267ad-122">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="267ad-123">**иопкпартури**</span><span class="sxs-lookup"><span data-stu-id="267ad-123">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="267ad-124">**икспсомимажебруш**</span><span class="sxs-lookup"><span data-stu-id="267ad-124">**IXpsOMImageBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[<span data-ttu-id="267ad-125">**икспсомимажересаурце**</span><span class="sxs-lookup"><span data-stu-id="267ad-125">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)
</dt> <dt>

[<span data-ttu-id="267ad-126">**икспсомжеометри**</span><span class="sxs-lookup"><span data-stu-id="267ad-126">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="267ad-127">**икспсомжеометрифигуре**</span><span class="sxs-lookup"><span data-stu-id="267ad-127">**IXpsOMGeometryFigure**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="267ad-128">**икспсомжеометрифигуреколлектион**</span><span class="sxs-lookup"><span data-stu-id="267ad-128">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[<span data-ttu-id="267ad-129">**икспсомобжектфактори**</span><span class="sxs-lookup"><span data-stu-id="267ad-129">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="267ad-130">**икспсомпаккаже**</span><span class="sxs-lookup"><span data-stu-id="267ad-130">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="267ad-131">**икспсомпас**</span><span class="sxs-lookup"><span data-stu-id="267ad-131">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[<span data-ttu-id="267ad-132">**икспсомвисуалколлектион**</span><span class="sxs-lookup"><span data-stu-id="267ad-132">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="267ad-133">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="267ad-133">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="267ad-134">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="267ad-134">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="267ad-135">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="267ad-135">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="267ad-136">XPS</span><span class="sxs-lookup"><span data-stu-id="267ad-136">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
