---
title: Рисование и заливка сложной фигуры
description: Direct2D предоставляет интерфейс ID2D1PathGeometry для описания сложных фигур, которые могут содержать кривые, дуги и линии. В этом разделе описывается определение и отрисовка геометрии пути.
ms.assetid: d7aad487-04e0-448d-bedf-b8dfadc7bbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df463265b48a67a6d844d36b7de009200465256
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792889"
---
# <a name="how-to-draw-and-fill-a-complex-shape"></a><span data-ttu-id="33df3-104">Рисование и заливка сложной фигуры</span><span class="sxs-lookup"><span data-stu-id="33df3-104">How to Draw and Fill a Complex Shape</span></span>

<span data-ttu-id="33df3-105">Direct2D предоставляет интерфейс [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) для описания сложных фигур, которые могут содержать кривые, дуги и линии.</span><span class="sxs-lookup"><span data-stu-id="33df3-105">Direct2D provides the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface for describing complex shapes that can contain curves, arcs, and lines.</span></span> <span data-ttu-id="33df3-106">В этом разделе описывается определение и отрисовка геометрии пути.</span><span class="sxs-lookup"><span data-stu-id="33df3-106">This topic describes how to define and render a path geometry.</span></span>

<span data-ttu-id="33df3-107">Чтобы определить геометрию пути, сначала используйте метод [**ID2D1Factory:: креатепасжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) , чтобы создать геометрию пути, а затем используйте метод [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) геометрии Path для получения [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span><span class="sxs-lookup"><span data-stu-id="33df3-107">To define a path geometry, first use the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create the path geometry, then use the path geometry's [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="33df3-108">Затем можно добавить линии, кривые и дуги, вызвав различные методы Add приемника.</span><span class="sxs-lookup"><span data-stu-id="33df3-108">You can then add lines, curves, and arcs by calling the sink's various Add methods.</span></span>

<span data-ttu-id="33df3-109">В следующем примере создается [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), извлекается приемник и используется для определения формы песочных часов.</span><span class="sxs-lookup"><span data-stu-id="33df3-109">The following example creates an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), retrieves a sink, and uses it to define an hourglass shape.</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;

// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```

<span data-ttu-id="33df3-110">Обратите внимание, что [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) является аппаратно-независимым ресурсом и может быть создан один раз и храниться в течение всего жизненного цикла приложения.</span><span class="sxs-lookup"><span data-stu-id="33df3-110">Note that an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) is a device-independent resource and can, therefore, be created once and retained for the life of the application.</span></span> <span data-ttu-id="33df3-111">(Дополнительные сведения о различных типах ресурсов см. в разделе [Общие сведения о ресурсах](resources-and-resource-domains.md).)</span><span class="sxs-lookup"><span data-stu-id="33df3-111">(For more information about different types of resources, see the [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="33df3-112">В следующем примере создаются две кисти, которые будут использоваться для рисования контура и заливки геометрии контура.</span><span class="sxs-lookup"><span data-stu-id="33df3-112">The next example creates two brushes that will be used to paint the path geometry's outline and fill.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Create a black brush.
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &m_pBlackBrush
        );
}

if (SUCCEEDED(hr))
{
    // Create a linear gradient.
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 0.25f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = m_pRenderTarget->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(100, 0),
                D2D1::Point2F(100, 200)),
            D2D1::BrushProperties(),
            pGradientStops,
            &m_pLGBrush
            );
    }

    SafeRelease(&pGradientStops);
}
```



<span data-ttu-id="33df3-113">В последнем примере используются методы [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) и [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) для рисования контура и внутренней геометрии.</span><span class="sxs-lookup"><span data-stu-id="33df3-113">The final example uses the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods to paint the geometry's outline and interior.</span></span> <span data-ttu-id="33df3-114">В этом примере создаются выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="33df3-114">This example produces the output shown in the following illustration.</span></span>

![Иллюстрация геометрии в форме песочных часов](images/transformgeometryexample-1.png)


```C++
void DemoApp::RenderGeometryExample()
{
   // Translate subsequent drawings by 20 device-independent pixels.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Translation(20.f, 20.f)
        );

    // Draw the hour glass geometry at the upper left corner of the client area.
    m_pRenderTarget->DrawGeometry(m_pPathGeometry, m_pBlackBrush, 10.f);
    m_pRenderTarget->FillGeometry(m_pPathGeometry, m_pLGBrush);</code></pre></td>
```

<span data-ttu-id="33df3-116">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="33df3-116">Code has been omitted from this example.</span></span> <span data-ttu-id="33df3-117">Дополнительные сведения о геометрических элементах см. в [обзоре геометрических объектов](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="33df3-117">For more information about geometries, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>