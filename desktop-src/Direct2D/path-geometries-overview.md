---
title: Общие сведения о геометрических контурах
description: Описывает использование геометрических контуров для определения сложных фигур.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104550950"
---
# <a name="path-geometries-overview"></a>Общие сведения о геометрических контурах

В этом разделе описывается использование географических объектов Direct2D Path для создания сложных рисунков. В него входят следующие разделы.

-   [Предварительные условия](#prerequisites)
-   [Геометрические контуры в Direct2D](#path-geometries-in-direct2d)
-   [Использование ID2D1GeometrySink для заполнения геометрии контура](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [Пример. Создание сложного рисунка](#example-create-a-complex-drawing)
    -   [Создание геометрического пути для левого Mountain](#create-a-path-geometry-for-the-left-mountain)
    -   [Создание геометрического пути для правого Mountain](#create-a-path-geometry-for-the-right-mountain)
    -   [Создание геометрического пути для Sun](#create-a-path-geometry-for-the-sun)
    -   [Создание геометрического пути для River](#create-a-path-geometry-for-the-river)
    -   [Отображение геометрических объектов пути на экране](#render-the-path-geometries-onto-the-display)
-   [См. также](#related-topics)

## <a name="prerequisites"></a>Предварительные условия

В этом обзоре предполагается, что вы знакомы с созданием базовых Direct2D приложений, как описано в разделе [Создание простого приложения Direct2D](direct2d-quickstart.md). Также предполагается, что вы знакомы с основными возможностями геометрических объектов Direct2D, как описано в [обзоре геометрических объектов](direct2d-geometries-overview.md).

## <a name="path-geometries-in-direct2d"></a>Геометрические контуры в Direct2D

Геометрические контуры представлены интерфейсом [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Чтобы создать экземпляр геометрии пути, вызовите метод [**ID2D1Factory:: креатепасжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) . Эти объекты можно использовать для описания сложных геометрических фигур, состоящих из сегментов, таких как дуги, кривые и линии. Чтобы заполнить геометрию контура рисунками и сегментами, вызовите метод [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) , чтобы получить [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) и использовать методы приемника геометрии для добавления фигур и сегментов к геометрии контура.

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a>Использование ID2D1GeometrySink для заполнения геометрии контура

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) описывает геометрический путь, который может содержать строки, дуги, кривые Безье и кривые Безье второго порядка.

Геометрический приемник состоит из одной или нескольких фигур. Каждая фигура состоит из одного или нескольких сегментов линии, кривой или дуги. Чтобы создать фигуру, вызовите метод [**бегинфигуре**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) , передав начальную точку рисунка, а затем используйте его методы Add (такие как [**аддлине**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) и [**аддбезиер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) , чтобы добавить сегменты. По завершении добавления сегментов вызовите метод [**ендфигуре**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) . Эту последовательность можно повторить для создания дополнительных фигур. По завершении создания фигур вызовите метод [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .

## <a name="example-create-a-complex-drawing"></a>Пример. Создание сложного рисунка

На следующем рисунке показана сложная прорисовка с линиями, дугами и кривыми Безье. В следующем примере кода показано, как создать рисунок, используя четыре объекта Geometry, один для левого Mountain, один для правого Mountain, один для River, а другой для Sun с фларес.

![Иллюстрация River, горы и Sun с помощью геометрических контуров](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a>Создание геометрического пути для левого Mountain

В примере сначала создается геометрия контура для левого Mountain, как показано на следующем рисунке.

![Показывает комплексное рисование многоугольника, который показывает Mountain.](images/path-geo-leftmnt.png)

Чтобы создать левое горное значение, в примере вызывается метод [**ID2D1Factory:: креатепасжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) для создания [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



Затем в примере используется метод [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) для получения геометрического приемника из [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) и его сохранения в переменной *псинк* .


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



Затем в примере вызывается [**бегинфигуре**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), передающий [**\_ рисунок \_ D2D1 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) , который указывает, что эта фигура заполнена, затем вызывает [**аддлинес**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), передает массив точек [**D2D1 \_ \_**](d2d1-point-2f.md) (267, 177), (236, 192), (212, 160), (156, 255) и (346, 255).

В следующем примере кода показано, как это сделать:


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a>Создание геометрического пути для правого Mountain

Затем в примере создается другая геометрическая траектория для правого Mountain с точками (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) и (575, 263). На следующем рисунке показано, как отображается правильное значение Mountain.

![Иллюстрация многоугольника, показывающего Mountain](images/path-geo-rightmnt.png)

В следующем примере кода показано, как это сделать:


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a>Создание геометрического пути для Sun

Затем в примере заполняется другой геометрический контур для солнца, как показано на следующем рисунке.

![Иллюстрация дуги и кривых Безье, показывающих солнце](images/path-geo-sun.png)

Для этого схема геометрического пути создает приемник и добавляет к ней фигуру для дуги и фигуры для каждого блика. Повторяя последовательность [**бегинфигуре**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), ее методов Add (например, [**Аддбезиер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) и [**ендфигуре**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), к приемнику добавляются несколько фигур.

В следующем примере кода показано, как это сделать:


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a>Создание геометрического пути для River

Затем в примере создается другой путь геометрического объекта для River, содержащего кривые Безье. На следующем рисунке показано, как отображается River.

![Иллюстрация кривых Безье, показывающих River](images/path-geo-river.png)

В следующем примере кода показано, как это сделать:


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a>Отображение геометрических объектов пути на экране

В следующем коде показано, как визуализировать заполненные геометрические объекты на экране. Сначала рисуется и рисуется геометрическая геометрия Sun, затем слева горное геометрическое, River геометрия и, наконец, правая геометрия Mountain.


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



Полный пример показан на следующем рисунке.

![Иллюстрация River, горы и Sun с помощью геометрических контуров](images/path-geo-mnts.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание простого приложения Direct2D](direct2d-quickstart.md)
</dt> <dt>

[Обзор геометрий](direct2d-geometries-overview.md)
</dt> </dl>

 

 