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
# <a name="render-to-a-gdi-surface"></a><span data-ttu-id="9a5ca-103">Подготовка к просмотру на поверхности GDI</span><span class="sxs-lookup"><span data-stu-id="9a5ca-103">Render to a GDI Surface</span></span>

<span data-ttu-id="9a5ca-104">В некоторых случаях может потребоваться возможность отображения текста [DirectWrite](direct-write-portal.md) на поверхности GDI.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-104">In some cases, you may want to be able to display [DirectWrite](direct-write-portal.md) text on a GDI surface.</span></span> <span data-ttu-id="9a5ca-105">Интерфейс [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) инкапсулирует растровое изображение и контекст устройства для отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-105">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface encapsulates a bitmap and device context to render text onto.</span></span> <span data-ttu-id="9a5ca-106">Вы создаете **идвритебитмапрендертаржет** с помощью метода [**Идвритегдиинтероп:: креатебитмапрендертаржет**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-106">You create an **IDWriteBitmapRenderTarget** by using the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method, as shown in the following code.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



<span data-ttu-id="9a5ca-107">Для подготовки к просмотру с помощью [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)необходимо реализовать интерфейс обратного вызова пользовательского текстового интерфейса, производный от интерфейса [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) .</span><span class="sxs-lookup"><span data-stu-id="9a5ca-107">To render with an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), you must implement a custom text renderer callback interface derived from the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) interface.</span></span> <span data-ttu-id="9a5ca-108">Необходимо реализовать методы для рисования выполнения глифа, подчеркивания, зачеркивания, встроенных объектов и т. д.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-108">You must implement methods for drawing a glyph run, underline, strikethrough, inline objects, and so on.</span></span> <span data-ttu-id="9a5ca-109">Полный список методов см. на странице справочника по [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) .</span><span class="sxs-lookup"><span data-stu-id="9a5ca-109">For a complete list of the methods, see the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page.</span></span> <span data-ttu-id="9a5ca-110">Не все методы должны быть реализованы, они могут просто возвращать **E \_ нотимпл**, и рисование продолжится.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-110">Not every method must be implemented, they can just return **E\_NOTIMPL**, and drawing will continue.</span></span>

<span data-ttu-id="9a5ca-111">Затем можно нарисовать текст с помощью метода [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) и передать интерфейс обратного вызова, реализованный в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-111">You can then draw the text by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method and passing the callback interface that you implemented as a parameter.</span></span> <span data-ttu-id="9a5ca-112">Метод **идвритетекстлайаут::D RAW** вызывает методы предоставляемого обратного вызова пользовательского модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-112">The **IDWriteTextLayout::Draw** method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="9a5ca-113">Методы [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**дравундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**дравинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)и [**дравстрикесраугх**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) выполняют функции рисования.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="9a5ca-114">В реализации [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)вызовите метод [**Идвритебитмапрендертаржет::D равглифрун**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) для рисования глифов.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-114">In your implementation of [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), call the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="9a5ca-115">Отрисовка подчеркивания, перечеркивания и встроенных объектов должна выполняться пользовательским модулем подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-115">The rendering of the underline, strikethrough and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="9a5ca-116">[**Идвритебитмапрендертаржет::D равглифрун**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) имеет необязательный параметр rect out, который содержит границы области, в которой был нарисован текст.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-116">[**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) has an optional RECT out parameter that contains the bounds of the area where the text was drawn.</span></span> <span data-ttu-id="9a5ca-117">Эти сведения можно использовать для установки ограничивающего прямоугольника для контекста устройства с помощью функции [**сетбаундсрект**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) , предоставляемой GDI.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-117">You can use this information to set the bounding rectangle for the device context with the [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) function that is provided by GDI.</span></span> <span data-ttu-id="9a5ca-118">Следующий код является примером реализации метода [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) пользовательского модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-118">The following code is an example implementation of the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of a custom renderer.</span></span>


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



<span data-ttu-id="9a5ca-119">Интерфейс [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) преобразуется в контекст устройства (DC) в памяти.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-119">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="9a5ca-120">Вы получаете маркер этого контроллера домена с помощью метода [**идвритебитмапрендертаржет:: жетмеморидк**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .</span><span class="sxs-lookup"><span data-stu-id="9a5ca-120">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span> <span data-ttu-id="9a5ca-121">Как только Рисование будет выполнено, контроллер домена памяти объекта **идвритебитмапрендертаржет** должен быть скопирован на целевую поверхность GDI.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-121">As soon as the drawing has been performed, the memory DC of the **IDWriteBitmapRenderTarget** object must be copied to the destination GDI surface.</span></span>

<span data-ttu-id="9a5ca-122">Ограничивающий прямоугольник можно получить с помощью функции [**жетбаундсрект**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) , а затем использовать ограничивающий прямоугольник с функцией [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) для копирования подготовленного текста [DirectWrite](direct-write-portal.md) из контроллера памяти на поверхность GDI, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="9a5ca-122">You can retrieve the bounding rectangle by using the [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) function, then use the bounding rectangle with the [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) function to copy the rendered [DirectWrite](direct-write-portal.md) text from the memory DC to the GDI surface as shown in the following code.</span></span>


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



 

 