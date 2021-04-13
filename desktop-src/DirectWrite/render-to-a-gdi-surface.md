---
title: Подготовка к просмотру на поверхности GDI
description: Подготовка к просмотру на поверхности GDI
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff292feb2250a4dd81abeb62d8ee48ebfb4488b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413577"
---
# <a name="render-to-a-gdi-surface"></a>Подготовка к просмотру на поверхности GDI

В некоторых случаях может потребоваться возможность отображения текста [DirectWrite](direct-write-portal.md) на поверхности GDI. Интерфейс [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) инкапсулирует растровое изображение и контекст устройства для отрисовки текста. Вы создаете **идвритебитмапрендертаржет** с помощью метода [**Идвритегдиинтероп:: креатебитмапрендертаржет**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) , как показано в следующем коде.


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



Для подготовки к просмотру с помощью [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)необходимо реализовать интерфейс обратного вызова пользовательского текстового интерфейса, производный от интерфейса [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . Необходимо реализовать методы для рисования выполнения глифа, подчеркивания, зачеркивания, встроенных объектов и т. д. Полный список методов см. на странице справочника по [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . Не все методы должны быть реализованы, они могут просто возвращать **E \_ нотимпл**, и рисование продолжится.

Затем можно нарисовать текст с помощью метода [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) и передать интерфейс обратного вызова, реализованный в качестве параметра. Метод **идвритетекстлайаут::D RAW** вызывает методы предоставляемого обратного вызова пользовательского модуля подготовки отчетов. Методы [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**дравундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**дравинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)и [**дравстрикесраугх**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) выполняют функции рисования.

В реализации [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)вызовите метод [**Идвритебитмапрендертаржет::D равглифрун**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) для рисования глифов. Отрисовка подчеркивания, перечеркивания и встроенных объектов должна выполняться пользовательским модулем подготовки отчетов.

[**Идвритебитмапрендертаржет::D равглифрун**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) имеет необязательный параметр rect out, который содержит границы области, в которой был нарисован текст. Эти сведения можно использовать для установки ограничивающего прямоугольника для контекста устройства с помощью функции [**сетбаундсрект**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) , предоставляемой GDI. Следующий код является примером реализации метода [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) пользовательского модуля подготовки отчетов.


```C++
STDMETHODIMP GdiTextRenderer::DrawGlyphRun(
    __maybenull void* clientDrawingContext,
    FLOAT baselineOriginX,
    FLOAT baselineOriginY,
    DWRITE_MEASURING_MODE measuringMode,
    __in DWRITE_GLYPH_RUN const* glyphRun,
    __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
    IUnknown* clientDrawingEffect
    )
{
    HRESULT hr = S_OK;

    // Pass on the drawing call to the render target to do the real work.
    RECT dirtyRect = {0};

    hr = pRenderTarget_->DrawGlyphRun(
        baselineOriginX,
        baselineOriginY,
        measuringMode,
        glyphRun,
        pRenderingParams_,
        RGB(0,200,255),
        &dirtyRect
        );
    

    return hr;
}
```



Интерфейс [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) преобразуется в контекст устройства (DC) в памяти. Вы получаете маркер этого контроллера домена с помощью метода [**идвритебитмапрендертаржет:: жетмеморидк**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) . Как только Рисование будет выполнено, контроллер домена памяти объекта **идвритебитмапрендертаржет** должен быть скопирован на целевую поверхность GDI.

Ограничивающий прямоугольник можно получить с помощью функции [**жетбаундсрект**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) , а затем использовать ограничивающий прямоугольник с функцией [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) для копирования подготовленного текста [DirectWrite](direct-write-portal.md) из контроллера памяти на поверхность GDI, как показано в следующем коде.


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



 

 