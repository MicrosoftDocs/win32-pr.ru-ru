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
# <a name="how-to-draw-text"></a>Рисование текста

Чтобы нарисовать текст с помощью Direct2D, используйте метод [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) для текста, имеющего один формат. Или используйте метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) для нескольких форматов, расширенных функций OpenType или проверки попадания. Эти методы используют API DirectWrite для обеспечения высокого качества отображения текста.

## <a name="the-drawtext-method"></a>Метод DrawText

Чтобы нарисовать текст, имеющий один формат, используйте метод [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) . Чтобы использовать этот метод, сначала используйте [**идвритефактори**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) для создания экземпляра [**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .

Следующий код создает объект [**идвритетекстформат**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) и сохраняет его в переменной *m \_ птекстформат* .


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



Так как объекты [**идвритефактори**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) и [**идвритетекстформат**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) являются [аппаратно-независимыми ресурсами](resources-and-resource-domains.md), можно повысить производительность приложения, создав их только один раз, вместо того чтобы создавать их каждый раз при отрисовке кадра.

После создания объекта текстового формата его можно использовать с целевым объектом рендеринга. Следующий код выводит текст с помощью метода [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) целевого объекта отрисовки (переменная *\_ прендертаржет m* ).


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



## <a name="the-drawtextlayout-method"></a>Метод Дравтекстлайаут

Метод [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) визуализирует объект [**идвритетекстлайаут**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) . Этот метод используется для применения нескольких форматов к блоку текста (например, для подчеркивания части текста), для использования расширенных функций OpenType или для проведения поддержки проверки попадания.

Метод [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) также предоставляет преимущества для повышения производительности при многократном рисовании одного и того же текста. Объект [**идвритетекстлайаут**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) измеряет и размещает свой текст при создании. Если вы создаете объект **идвритетекстлайаут** только один раз и повторно используете его каждый раз, когда потребуется перерисовать текст, производительность повысится, поскольку системе не нужно измерять и размещать текст снова.

Прежде чем можно будет использовать метод [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , необходимо использовать [**идвритефактори**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) для создания объектов [**идвритетекстформат**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) и [**идвритетекстлайаут**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) . После создания этих объектов вызовите метод **дравтекстлайаут** .

Дополнительные сведения и примеры см. в разделе Общие сведения о [форматировании и макете текста](/windows/desktop/DirectWrite/text-formatting-and-layout) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))
</dt> <dt>

[**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[**идвритетекстформат**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[**идвритетекстлайаут**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[Форматирование и макет текста](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 
