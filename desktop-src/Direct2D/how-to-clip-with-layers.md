---
title: Как обрезать геометрическую маску
description: Показывает, как обрезать область с помощью слоев.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0c2258938020593014b5b6f5ea77516e7770f8589601cf4139971b3532b22fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569353"
---
# <a name="how-to-clip-to-a-geometric-mask"></a>Как обрезать геометрическую маску

В этом разделе описывается использование геометрической маски для обрезки области слоя.

**Обрезка области с геометрической маской**

1.  Создайте [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , который будет использоваться для обрезки области.
2.  Вызовите метод [**ID2D1RenderTarget:: креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , чтобы создать слой.
3.  Вызовите [**ID2D1RenderTarget::P ушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) и передайте геометрическую маску, определенную на шаге 1.
4.  Нарисуйте содержимое в Clip.
5.  Вызовите [**ID2D1RenderTarget::P оплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , чтобы удалить слой из целевого объекта рендеринга.

В следующем примере используется геометрическая маска для обрезки изображения и нескольких прямоугольников. На следующем рисунке показана исходная битовая карта слева, а растровое изображение, обрезанное до геометрической маски справа.

![Иллюстрация точечного рисунка Голдфиш до и после того, как растровое изображение обрезано до маски в форме звезды](images/cliparegion-layers.png)

Чтобы обрезать рисунок, как показано на предыдущем рисунке, создайте [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) и используйте его для определения звезды. В следующем примере кода показано, как это сделать:


```C++
// Create the path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
}

// Write to the path geometry using the geometry sink to create a star.
if (SUCCEEDED(hr))
{
    hr = m_pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
    pSink->BeginFigure(D2D1::Point2F(20, 50), D2D1_FIGURE_BEGIN_FILLED);
    pSink->AddLine(D2D1::Point2F(130, 50));
    pSink->AddLine(D2D1::Point2F(20, 130));
    pSink->AddLine(D2D1::Point2F(80, 0));
    pSink->AddLine(D2D1::Point2F(130, 130));
    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}

SafeRelease(&pSink);
```



Вызовите [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , чтобы создать слой.

> [!Note]  
> начиная с Windows 8 вам не нужно вызывать [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)). В большинстве случаев производительность лучше, если не вызывать этот метод, и Direct2D управляет ресурсами слоя.

 

Вызовите [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) с помощью геометрической маски, чтобы отправить слой. Нарисуйте содержимое в Clip, а затем вызовите [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , чтобы открыть слой. При этом создается рисунок в форме звезды. В следующем примере кода показано, как это сделать:


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Общие сведения о слоях](direct2d-layers-overview.md)
</dt> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 