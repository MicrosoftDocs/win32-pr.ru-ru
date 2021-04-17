---
title: Как обрезать геометрическую маску
description: Показывает, как обрезать область с помощью слоев.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 979281fb7fa6e034894bffaecbd6246fe8a9aa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488025"
---
# <a name="how-to-clip-to-a-geometric-mask"></a><span data-ttu-id="a1b47-103">Как обрезать геометрическую маску</span><span class="sxs-lookup"><span data-stu-id="a1b47-103">How to Clip to a Geometric Mask</span></span>

<span data-ttu-id="a1b47-104">В этом разделе описывается использование геометрической маски для обрезки области слоя.</span><span class="sxs-lookup"><span data-stu-id="a1b47-104">This topic describes how to use a geometric mask to clip a region of a layer.</span></span>

<span data-ttu-id="a1b47-105">**Обрезка области с геометрической маской**</span><span class="sxs-lookup"><span data-stu-id="a1b47-105">**To clip a region with a geometric mask**</span></span>

1.  <span data-ttu-id="a1b47-106">Создайте [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , который будет использоваться для обрезки области.</span><span class="sxs-lookup"><span data-stu-id="a1b47-106">Create the [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) that will be used to clip the region.</span></span>
2.  <span data-ttu-id="a1b47-107">Вызовите метод [**ID2D1RenderTarget:: креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , чтобы создать слой.</span><span class="sxs-lookup"><span data-stu-id="a1b47-107">Call [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>
3.  <span data-ttu-id="a1b47-108">Вызовите [**ID2D1RenderTarget::P ушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) и передайте геометрическую маску, определенную на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="a1b47-108">Call [**ID2D1RenderTarget::PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and pass the geometric mask you defined in step 1.</span></span>
4.  <span data-ttu-id="a1b47-109">Нарисуйте содержимое в Clip.</span><span class="sxs-lookup"><span data-stu-id="a1b47-109">Draw the content to clip.</span></span>
5.  <span data-ttu-id="a1b47-110">Вызовите [**ID2D1RenderTarget::P оплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , чтобы удалить слой из целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="a1b47-110">Call [**ID2D1RenderTarget::PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to remove the layer from the render target.</span></span>

<span data-ttu-id="a1b47-111">В следующем примере используется геометрическая маска для обрезки изображения и нескольких прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="a1b47-111">The example that follows uses a geometric mask to clip an image and several rectangles.</span></span> <span data-ttu-id="a1b47-112">На следующем рисунке показана исходная битовая карта слева, а растровое изображение, обрезанное до геометрической маски справа.</span><span class="sxs-lookup"><span data-stu-id="a1b47-112">The following illustration shows the original bitmap on the left, and the bitmap clipped to the geometric mask on the right.</span></span>

![Иллюстрация точечного рисунка Голдфиш до и после того, как растровое изображение обрезано до маски в форме звезды](images/cliparegion-layers.png)

<span data-ttu-id="a1b47-114">Чтобы обрезать рисунок, как показано на предыдущем рисунке, создайте [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) и используйте его для определения звезды.</span><span class="sxs-lookup"><span data-stu-id="a1b47-114">To clip the drawing as shown in the preceding illustration, you create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and use it to define a star.</span></span> <span data-ttu-id="a1b47-115">В следующем примере кода показано, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="a1b47-115">The following code shows how to do this.</span></span>


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



<span data-ttu-id="a1b47-116">Вызовите [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , чтобы создать слой.</span><span class="sxs-lookup"><span data-stu-id="a1b47-116">Call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>

> [!Note]  
> <span data-ttu-id="a1b47-117">Начиная с Windows 8, вам не нужно вызывать [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="a1b47-117">Starting with Windows 8, you don't need to call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span></span> <span data-ttu-id="a1b47-118">В большинстве случаев производительность лучше, если не вызывать этот метод, и Direct2D управляет ресурсами слоя.</span><span class="sxs-lookup"><span data-stu-id="a1b47-118">In most situations performance is better if you don't call this method and Direct2D manages the layer resources.</span></span>

 

<span data-ttu-id="a1b47-119">Вызовите [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) с помощью геометрической маски, чтобы отправить слой.</span><span class="sxs-lookup"><span data-stu-id="a1b47-119">Call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) with the geometry mask to push the layer.</span></span> <span data-ttu-id="a1b47-120">Нарисуйте содержимое в Clip, а затем вызовите [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , чтобы открыть слой.</span><span class="sxs-lookup"><span data-stu-id="a1b47-120">Draw the content to clip, then call [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to pop the layer.</span></span> <span data-ttu-id="a1b47-121">При этом создается рисунок в форме звезды.</span><span class="sxs-lookup"><span data-stu-id="a1b47-121">This produces the star-shaped drawing.</span></span> <span data-ttu-id="a1b47-122">В следующем примере кода показано, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="a1b47-122">The following code shows how to do this.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a1b47-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a1b47-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1b47-124">Общие сведения о слоях</span><span class="sxs-lookup"><span data-stu-id="a1b47-124">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> <dt>

[<span data-ttu-id="a1b47-125">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="a1b47-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 