---
title: Рисование и заполнение базовой фигуры
description: В этом разделе описывается рисование основной фигуры.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6b6b5a6fb08ac962475c2f0aa2812b4c3ae5da03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104564889"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a><span data-ttu-id="93655-103">Рисование и заполнение базовой фигуры</span><span class="sxs-lookup"><span data-stu-id="93655-103">How to Draw and Fill a Basic Shape</span></span>

<span data-ttu-id="93655-104">В этом разделе описывается рисование основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="93655-104">This topic describes how to draw a basic shape.</span></span> <span data-ttu-id="93655-105">Интерфейс [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) предоставляет методы для структурирования и заливки эллипсов, прямоугольников и линий.</span><span class="sxs-lookup"><span data-stu-id="93655-105">The [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface provides methods for outlining and filling ellipses, rectangles, and lines.</span></span> <span data-ttu-id="93655-106">В следующих примерах показано, как создать и нарисовать эллипс.</span><span class="sxs-lookup"><span data-stu-id="93655-106">The following examples show how to create and draw an ellipse.</span></span>

<span data-ttu-id="93655-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="93655-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="93655-108">Рисование контура эллипса с помощью сплошного штриха</span><span class="sxs-lookup"><span data-stu-id="93655-108">Draw the Outline of an Ellipse with a Solid Stroke</span></span>](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [<span data-ttu-id="93655-109">Рисование эллипса штриховой линией</span><span class="sxs-lookup"><span data-stu-id="93655-109">Draw an Ellipse with a Dashed Stroke</span></span>](#draw-an-ellipse-with-a-dashed-stroke)
-   [<span data-ttu-id="93655-110">Рисование и заливка эллипса</span><span class="sxs-lookup"><span data-stu-id="93655-110">Draw and Fill an Ellipse</span></span>](#draw-and-fill-an-ellipse)
-   [<span data-ttu-id="93655-111">Рисование более сложных фигур</span><span class="sxs-lookup"><span data-stu-id="93655-111">Drawing More Complex Shapes</span></span>](#drawing-more-complex-shapes)
-   [<span data-ttu-id="93655-112">См. также</span><span class="sxs-lookup"><span data-stu-id="93655-112">Related topics</span></span>](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a><span data-ttu-id="93655-113">Рисование контура эллипса с помощью сплошного штриха</span><span class="sxs-lookup"><span data-stu-id="93655-113">Draw the Outline of an Ellipse with a Solid Stroke</span></span>

<span data-ttu-id="93655-114">Чтобы нарисовать контур эллипса, необходимо определить кисть (например, [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) или [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) для рисования контура и [**D2D1 \_ эллипс**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) для описания его расположения и измерений, а затем передать эти объекты в метод [**ID2D1RenderTarget::D равеллипсе**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) .</span><span class="sxs-lookup"><span data-stu-id="93655-114">To draw the outline of an ellipse, you define a brush (such as a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) for painting the outline and a [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) for describing the ellipse's position and dimensions, then pass these objects to the [**ID2D1RenderTarget::DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="93655-115">В следующем примере создается черная сплошная кисть цвета и сохраняется в \_ члене класса m спблаккбруш.</span><span class="sxs-lookup"><span data-stu-id="93655-115">The following example creates a black solid color brush and stores it in the m\_spBlackBrush class member.</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



<span data-ttu-id="93655-116">В следующем примере определяется [**D2D1 \_ эллипс**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) и используется с кистью, определенной в предыдущем примере, для рисования контура эллипса.</span><span class="sxs-lookup"><span data-stu-id="93655-116">The next example defines an [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) and uses it with the brush defined in the previous example to draw the outline of an ellipse.</span></span> <span data-ttu-id="93655-117">В этом примере создаются выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="93655-117">This example produces the output shown in the following illustration.</span></span>

![Иллюстрация эллипса с сплошным росчерком](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a><span data-ttu-id="93655-119">Рисование эллипса штриховой линией</span><span class="sxs-lookup"><span data-stu-id="93655-119">Draw an Ellipse with a Dashed Stroke</span></span>

<span data-ttu-id="93655-120">В предыдущем примере использовался обычный штрих.</span><span class="sxs-lookup"><span data-stu-id="93655-120">The preceding example used a plain stroke.</span></span> <span data-ttu-id="93655-121">Внешний вид штриха можно изменить несколькими способами, создав [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span><span class="sxs-lookup"><span data-stu-id="93655-121">You can modify the look of a stroke in several ways by creating an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span></span> <span data-ttu-id="93655-122">**ID2D1StrokeStyle** позволяет указать фигуру в начале и в конце штриха, будь то шаблон штриха и т. д.</span><span class="sxs-lookup"><span data-stu-id="93655-122">The **ID2D1StrokeStyle** lets you specify the shape at the beginning and end of a stroke, whether it has a dash pattern, and so on.</span></span> <span data-ttu-id="93655-123">В следующем примере создается **ID2D1StrokeStyle** , описывающий штриховую штриховку.</span><span class="sxs-lookup"><span data-stu-id="93655-123">The following example creates an **ID2D1StrokeStyle** that describes a dashed stroke.</span></span> <span data-ttu-id="93655-124">В этом примере используется стандартный шаблон штриха, [**D2D1 \_ пунктирный \_ стиль \_ штриховая \_ \_ точка**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), но можно также указать собственный.</span><span class="sxs-lookup"><span data-stu-id="93655-124">This example uses a predefined dash pattern, [**D2D1\_DASH\_STYLE\_DASH\_DOT\_DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), but you can also specify your own.</span></span>


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



<span data-ttu-id="93655-125">В следующем примере используется стиль Stroke с методом [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) .</span><span class="sxs-lookup"><span data-stu-id="93655-125">The next example uses the stroke style with the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="93655-126">В этом примере создаются выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="93655-126">This example produces the output shown in the following illustration.</span></span>

![Иллюстрация эллипса с пунктирным штрихом](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a><span data-ttu-id="93655-128">Рисование и заливка эллипса</span><span class="sxs-lookup"><span data-stu-id="93655-128">Draw and Fill an Ellipse</span></span>

<span data-ttu-id="93655-129">Чтобы закрасить внутреннюю часть эллипса, используйте метод [**филлеллипсе**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) .</span><span class="sxs-lookup"><span data-stu-id="93655-129">To paint the interior of an ellipse, you use the [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method.</span></span> <span data-ttu-id="93655-130">В следующем примере используется метод [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse (constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) для формирования контура эллипса, а затем используется метод **филлеллипсе** для рисования внутренней части.</span><span class="sxs-lookup"><span data-stu-id="93655-130">The following example uses the [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method to outline the ellipse, then uses the **FillEllipse** method to paint its interior.</span></span> <span data-ttu-id="93655-131">В этом примере создаются выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="93655-131">This example produces the output shown in the following illustration.</span></span>

![Иллюстрация эллипса с пунктирным штрихом и последующее заполнение сплошным серым цветом](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



<span data-ttu-id="93655-133">В следующем примере сначала заполняется эллипс, а затем его контур.</span><span class="sxs-lookup"><span data-stu-id="93655-133">The next example fills the ellipse first, then draws its outline.</span></span> <span data-ttu-id="93655-134">В этом примере создаются выходные данные, показанные на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="93655-134">This example produces the output shown in the following illustration.</span></span>

![Иллюстрация эллипса, заполненного сплошным серым цветом и направленная штриховой линией](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



<span data-ttu-id="93655-136">В этих примерах отсутствует код.</span><span class="sxs-lookup"><span data-stu-id="93655-136">Code has been omitted from these examples.</span></span>

## <a name="drawing-more-complex-shapes"></a><span data-ttu-id="93655-137">Рисование более сложных фигур</span><span class="sxs-lookup"><span data-stu-id="93655-137">Drawing More Complex Shapes</span></span>

<span data-ttu-id="93655-138">Чтобы нарисовать более сложные фигуры, необходимо определить объекты ID2D1Geometry и использовать их с методами [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) и [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="93655-138">To draw more complex shapes, you define ID2D1Geometry objects and use them with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods.</span></span> <span data-ttu-id="93655-139">Дополнительные сведения см. в разделе [Общие сведения о геометрических](direct2d-geometries-overview.md)элементах.</span><span class="sxs-lookup"><span data-stu-id="93655-139">For more information, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="93655-140">См. также</span><span class="sxs-lookup"><span data-stu-id="93655-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93655-141">Обзор геометрий</span><span class="sxs-lookup"><span data-stu-id="93655-141">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="93655-142">Обзор кистей</span><span class="sxs-lookup"><span data-stu-id="93655-142">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

 

 