---
title: Рисование и заполнение базовой фигуры
description: В этом разделе описывается рисование основной фигуры.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d072d6f43467aab9230796bfb24139630995e3f525c7e86a0c5e179ddd82048e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003755"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a>Рисование и заполнение базовой фигуры

В этом разделе описывается рисование основной фигуры. Интерфейс [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) предоставляет методы для структурирования и заливки эллипсов, прямоугольников и линий. В следующих примерах показано, как создать и нарисовать эллипс.

Этот раздел состоит из следующих подразделов.

-   [Рисование контура эллипса с помощью сплошного штриха](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [Рисование эллипса штриховой линией](#draw-an-ellipse-with-a-dashed-stroke)
-   [Рисование и заливка эллипса](#draw-and-fill-an-ellipse)
-   [Рисование более сложных фигур](#drawing-more-complex-shapes)
-   [Связанные темы](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a>Рисование контура эллипса с помощью сплошного штриха

Чтобы нарисовать контур эллипса, необходимо определить кисть (например, [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) или [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) для рисования контура и [**D2D1 \_ эллипс**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) для описания его расположения и измерений, а затем передать эти объекты в метод [**ID2D1RenderTarget::D равеллипсе**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) . В следующем примере создается черная сплошная кисть цвета и сохраняется в \_ члене класса m спблаккбруш.


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



В следующем примере определяется [**D2D1 \_ эллипс**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) и используется с кистью, определенной в предыдущем примере, для рисования контура эллипса. В этом примере создаются выходные данные, показанные на следующем рисунке.

![Иллюстрация эллипса с сплошным росчерком](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a>Рисование эллипса штриховой линией

В предыдущем примере использовался обычный штрих. Внешний вид штриха можно изменить несколькими способами, создав [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle). **ID2D1StrokeStyle** позволяет указать фигуру в начале и в конце штриха, будь то шаблон штриха и т. д. В следующем примере создается **ID2D1StrokeStyle** , описывающий штриховую штриховку. В этом примере используется стандартный шаблон штриха, [**D2D1 \_ пунктирный \_ стиль \_ штриховая \_ \_ точка**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), но можно также указать собственный.


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



В следующем примере используется стиль Stroke с методом [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) . В этом примере создаются выходные данные, показанные на следующем рисунке.

![Иллюстрация эллипса с пунктирным штрихом](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a>Рисование и заливка эллипса

Чтобы закрасить внутреннюю часть эллипса, используйте метод [**филлеллипсе**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) . В следующем примере метод [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) используется для формирования контура эллипса, а затем используется метод **филлеллипсе** для рисования внутренней части. В этом примере создаются выходные данные, показанные на следующем рисунке.

![Иллюстрация эллипса с пунктирным штрихом и последующее заполнение сплошным серым цветом](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



В следующем примере сначала заполняется эллипс, а затем его контур. В этом примере создаются выходные данные, показанные на следующем рисунке.

![Иллюстрация эллипса, заполненного сплошным серым цветом и направленная штриховой линией](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



В этих примерах отсутствует код.

## <a name="drawing-more-complex-shapes"></a>Рисование более сложных фигур

Чтобы нарисовать более сложные фигуры, необходимо определить объекты ID2D1Geometry и использовать их с методами [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) и [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) . Дополнительные сведения см. в разделе [Общие сведения о геометрических](direct2d-geometries-overview.md)элементах.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обзор геометрий](direct2d-geometries-overview.md)
</dt> <dt>

[Обзор кистей](direct2d-brushes-overview.md)
</dt> </dl>

 

 
