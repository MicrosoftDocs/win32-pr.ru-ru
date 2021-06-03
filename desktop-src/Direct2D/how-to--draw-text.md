---
title: Рисование текста
description: Показывает, как визуализировать текст с помощью Direct2D.
ms.assetid: 914dd9d0-78c8-44a3-8504-837faf3201d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd841f3b07edbde5e3fc6ed70f679cd58b3725f4
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349973"
---
# <a name="how-to-draw-text"></a><span data-ttu-id="5cdc8-103">Рисование текста</span><span class="sxs-lookup"><span data-stu-id="5cdc8-103">How to Draw Text</span></span>

<span data-ttu-id="5cdc8-104">Чтобы нарисовать текст с помощью Direct2D, используйте метод [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) для текста, имеющего один формат.</span><span class="sxs-lookup"><span data-stu-id="5cdc8-104">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format.</span></span> <span data-ttu-id="5cdc8-105">Или используйте метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) для нескольких форматов, расширенных функций OpenType или проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="5cdc8-105">Or, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method for multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="5cdc8-106">Эти методы используют API DirectWrite для обеспечения высокого качества отображения текста.</span><span class="sxs-lookup"><span data-stu-id="5cdc8-106">These methods use the DirectWrite API to provide high-quality text display.</span></span>

## <a name="the-drawtext-method"></a><span data-ttu-id="5cdc8-107">Метод DrawText</span><span class="sxs-lookup"><span data-stu-id="5cdc8-107">The DrawText Method</span></span>

<span data-ttu-id="5cdc8-108">Чтобы нарисовать текст, имеющий один формат, используйте метод [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) .</span><span class="sxs-lookup"><span data-stu-id="5cdc8-108">To draw text that has a single format, use the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method.</span></span> <span data-ttu-id="5cdc8-109">Чтобы использовать этот метод, сначала используйте [**идвритефактори**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) для создания экземпляра [**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="5cdc8-109">To use this method, first use an [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) to create an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) instance.</span></span>

<span data-ttu-id="5cdc8-110">Следующий код создает объект [**идвритетекстформат**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) и сохраняет его в переменной *m \_ птекстформат* .</span><span class="sxs-lookup"><span data-stu-id="5cdc8-110">The following code creates an [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) object and stores it in the *m\_pTextFormat* variable.</span></span>


```C++
// Create resources which are not bound
// to any device. Their lifetime effectively extends for the
// duration of the app. These resources include the Direct2D and
// DirectWrite factories,  and a DirectWrite Text Format object
// (used for identifying particular font characteristics).
//
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    static const WCHAR msc_fontName[] = L"Verdana";
    static const FLOAT msc_fontSize = 50;
    HRESULT hr;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pD2DFactory);

    if (SUCCEEDED(hr))
    {        
        // Create a DirectWrite factory.
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(m_pDWriteFactory),
            reinterpret_cast<IUnknown **>(&m_pDWriteFactory)
            );
    }
    if (SUCCEEDED(hr))
    {
        // Create a DirectWrite text format object.
        hr = m_pDWriteFactory->CreateTextFormat(
            msc_fontName,
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            msc_fontSize,
            L"", //locale
            &m_pTextFormat
            );
    }
    if (SUCCEEDED(hr))
    {
        // Center the text horizontally and vertically.
        m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
        
        m_pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }

    return hr;
}
```



<span data-ttu-id="5cdc8-111">Так как объекты [**идвритефактори**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) и [**идвритетекстформат**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) являются [аппаратно-независимыми ресурсами](resources-and-resource-domains.md), можно повысить производительность приложения, создав их только один раз, вместо того чтобы создавать их каждый раз при отрисовке кадра.</span><span class="sxs-lookup"><span data-stu-id="5cdc8-111">Because [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) objects are [device-independent resources](resources-and-resource-domains.md), you can improve an application's performance by creating them only one time, instead of re-creating them every time that a frame is rendered.</span></span>

<span data-ttu-id="5cdc8-112">После создания объекта текстового формата его можно использовать с целевым объектом рендеринга.</span><span class="sxs-lookup"><span data-stu-id="5cdc8-112">After you create the text format object, you can use it with a render target.</span></span> <span data-ttu-id="5cdc8-113">Следующий код выводит текст с помощью метода [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) целевого объекта отрисовки (переменная *\_ прендертаржет m* ).</span><span class="sxs-lookup"><span data-stu-id="5cdc8-113">The following code draws the text by using the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method of the render target (the *m\_pRenderTarget* variable).</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="the-drawtextlayout-method"></a><span data-ttu-id="5cdc8-114">Метод Дравтекстлайаут</span><span class="sxs-lookup"><span data-stu-id="5cdc8-114">The DrawTextLayout Method</span></span>

<span data-ttu-id="5cdc8-115">Метод [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) визуализирует объект [**идвритетекстлайаут**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5cdc8-115">The [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method renders an [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="5cdc8-116">Этот метод используется для применения нескольких форматов к блоку текста (например, для подчеркивания части текста), для использования расширенных функций OpenType или для проведения поддержки проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="5cdc8-116">Use this method to apply multiple formats to a block of text (such as underlining a part of text), to use advanced OpenType features, or to perform hit testing support.</span></span>

<span data-ttu-id="5cdc8-117">Метод [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) также предоставляет преимущества для повышения производительности при многократном рисовании одного и того же текста.</span><span class="sxs-lookup"><span data-stu-id="5cdc8-117">The [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method also provides performance benefits for drawing the same text repeatedly.</span></span> <span data-ttu-id="5cdc8-118">Объект [**идвритетекстлайаут**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) измеряет и размещает свой текст при создании.</span><span class="sxs-lookup"><span data-stu-id="5cdc8-118">The [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) object measures and lays out its text when you create it.</span></span> <span data-ttu-id="5cdc8-119">Если вы создаете объект **идвритетекстлайаут** только один раз и повторно используете его каждый раз, когда потребуется перерисовать текст, производительность повысится, поскольку системе не нужно измерять и размещать текст снова.</span><span class="sxs-lookup"><span data-stu-id="5cdc8-119">If you create an **IDWriteTextLayout** object only one time and reuse it every time that you have to redraw the text, the performance improves because the system does not have to measure and lay out the text again.</span></span>

<span data-ttu-id="5cdc8-120">Прежде чем можно будет использовать метод [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , необходимо использовать [**идвритефактори**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) для создания объектов [**идвритетекстформат**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) и [**идвритетекстлайаут**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5cdc8-120">Before you can use the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, you must use an [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) to create [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) and [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) objects.</span></span> <span data-ttu-id="5cdc8-121">После создания этих объектов вызовите метод **дравтекстлайаут** .</span><span class="sxs-lookup"><span data-stu-id="5cdc8-121">After these objects are created, call the **DrawTextLayout** method.</span></span>

<span data-ttu-id="5cdc8-122">Дополнительные сведения и примеры см. в разделе Общие сведения о [форматировании и макете текста](/windows/desktop/DirectWrite/text-formatting-and-layout) .</span><span class="sxs-lookup"><span data-stu-id="5cdc8-122">For more information and examples, see the [Text Formatting and Layout](/windows/desktop/DirectWrite/text-formatting-and-layout) overview.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cdc8-123">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5cdc8-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5cdc8-124">[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="5cdc8-124">[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>
</dt> <dt>

[<span data-ttu-id="5cdc8-125">**дравтекстлайаут**</span><span class="sxs-lookup"><span data-stu-id="5cdc8-125">**DrawTextLayout**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[<span data-ttu-id="5cdc8-126">**идвритетекстформат**</span><span class="sxs-lookup"><span data-stu-id="5cdc8-126">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="5cdc8-127">**идвритетекстлайаут**</span><span class="sxs-lookup"><span data-stu-id="5cdc8-127">**IDWriteTextLayout**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="5cdc8-128">Форматирование и макет текста</span><span class="sxs-lookup"><span data-stu-id="5cdc8-128">Text Formatting and Layout</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 
