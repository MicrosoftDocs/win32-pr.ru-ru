---
title: DirectWrite отрисовки
description: DirectWrite отрисовки
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7012bc4861a8befc9beb97c945dc0b03b4e761
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413271"
---
# <a name="rendering-directwrite"></a><span data-ttu-id="e32c3-103">DirectWrite отрисовки</span><span class="sxs-lookup"><span data-stu-id="e32c3-103">Rendering DirectWrite</span></span>

## <a name="rendering-options"></a><span data-ttu-id="e32c3-104">Параметры подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="e32c3-104">Rendering Options</span></span>

<span data-ttu-id="e32c3-105">Текст с форматированием, описанным только в объекте [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , может быть визуализирован с помощью [Direct2D](../direct2d/direct2d-portal.md), однако существует несколько дополнительных параметров для отрисовки объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="e32c3-105">Text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="e32c3-106">Строку, описываемую объектом [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , можно визуализировать с помощью методов, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="e32c3-106">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

## <a name="1-render-using-direct2d"></a><span data-ttu-id="e32c3-107">1. прорисовка с помощью Direct2D</span><span class="sxs-lookup"><span data-stu-id="e32c3-107">1. Render using Direct2D</span></span>

<span data-ttu-id="e32c3-108">Чтобы отобразить объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) с помощью Direct2D, используйте метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="e32c3-108">To render an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using Direct2D, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, as shown in the following code.</span></span>


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



<span data-ttu-id="e32c3-109">Более подробные сведения о рисовании объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) с помощью [Direct2D](../direct2d/direct2d-portal.md)см. в разделе [Начало работы with DirectWrite](getting-started-with-directwrite.md).</span><span class="sxs-lookup"><span data-stu-id="e32c3-109">For a more in depth look at drawing an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using [Direct2D](../direct2d/direct2d-portal.md), see [Getting Started with DirectWrite](getting-started-with-directwrite.md).</span></span>

## <a name="2-render-using-a-custom-text-renderer"></a><span data-ttu-id="e32c3-110">2. прорисовка с помощью пользовательского модуля подготовки текста.</span><span class="sxs-lookup"><span data-stu-id="e32c3-110">2. Render using a custom text renderer.</span></span>

<span data-ttu-id="e32c3-111">Для отображения с помощью пользовательского модуля подготовки отчетов используется метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , который принимает в качестве аргумента интерфейс обратного вызова, производный от [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="e32c3-111">You render with a custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="e32c3-112">Метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) вызывает методы предоставляемого обратного вызова пользовательского модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="e32c3-112">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="e32c3-113">Методы [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**дравундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**дравинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)и [**дравстрикесраугх**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) выполняют функции рисования.</span><span class="sxs-lookup"><span data-stu-id="e32c3-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="e32c3-114">[**Идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) объявляет методы для рисования выполнения глифа, подчеркивания, перечеркивания и встроенных объектов.</span><span class="sxs-lookup"><span data-stu-id="e32c3-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declares methods for drawing a glyph run, underline, strikethrough, and inline objects.</span></span> <span data-ttu-id="e32c3-115">Реализация этих методов реализована в приложении.</span><span class="sxs-lookup"><span data-stu-id="e32c3-115">It is up to the application to implement these methods.</span></span> <span data-ttu-id="e32c3-116">Создание пользовательского модуля подготовки текста позволяет приложению применять дополнительные эффекты при отрисовке текста, например пользовательской заливки или контура.</span><span class="sxs-lookup"><span data-stu-id="e32c3-116">Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.</span></span> <span data-ttu-id="e32c3-117">Образец пользовательского обработчика текста включен в [пример Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="e32c3-117">A sample custom text renderer is included in the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="3-render-cleartype-to-a-gdi-surface"></a><span data-ttu-id="e32c3-118">3. отрисовка ClearType на поверхность GDI.</span><span class="sxs-lookup"><span data-stu-id="e32c3-118">3. Render ClearType to a GDI surface.</span></span>

<span data-ttu-id="e32c3-119">В действительности отрисовка на поверхность GDI является примером использования пользовательского модуля подготовки текста.</span><span class="sxs-lookup"><span data-stu-id="e32c3-119">Rendering to a GDI surface is actually an example of using a custom text renderer.</span></span> <span data-ttu-id="e32c3-120">Однако некоторые действия выполняются в форме интерфейса [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="e32c3-120">However, some of the work is done for you in the form of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface.</span></span>

<span data-ttu-id="e32c3-121">Чтобы создать этот интерфейс, используйте метод [**идвритегдиинтероп:: креатебитмапрендертаржет**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="e32c3-121">To create this interface, use the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method.</span></span>

<span data-ttu-id="e32c3-122">Метод [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) пользовательского обработчика текста вызывает метод [**Идвритебитмапрендертаржет::D равглифрун**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) для рисования глифов.</span><span class="sxs-lookup"><span data-stu-id="e32c3-122">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of your custom text renderer calls the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="e32c3-123">Отрисовка подчеркивания, перечеркивания и встроенных объектов должна выполняться пользовательским модулем подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="e32c3-123">The rendering of the underline, strikethrough, and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="e32c3-124">Интерфейс [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) преобразуется в контекст устройства (DC) в памяти.</span><span class="sxs-lookup"><span data-stu-id="e32c3-124">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="e32c3-125">Вы получаете маркер этого контроллера домена с помощью метода [**идвритебитмапрендертаржет:: жетмеморидк**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .</span><span class="sxs-lookup"><span data-stu-id="e32c3-125">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span>


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



<span data-ttu-id="e32c3-126">После выполнения рисования контроллер домена памяти объекта [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) должен быть скопирован на целевую поверхность GDI.</span><span class="sxs-lookup"><span data-stu-id="e32c3-126">Once the drawing has been performed, the memory DC of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object must be copied to the destination GDI surface.</span></span>

> [!Note]  
> <span data-ttu-id="e32c3-127">Вы также можете передать точечный рисунок на другой тип поверхности, например в область GDI+.</span><span class="sxs-lookup"><span data-stu-id="e32c3-127">You also have the option of transferring the bitmap to another type of surface, such as a GDI+ surface.</span></span>

 


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



> [!Note]  
> <span data-ttu-id="e32c3-128">Приложение несет ответственность за визуализацию всех элементов в окне в конце.</span><span class="sxs-lookup"><span data-stu-id="e32c3-128">Your app has the responsibility to render everything to the window in the end.</span></span> <span data-ttu-id="e32c3-129">Сюда входит текст и графика.</span><span class="sxs-lookup"><span data-stu-id="e32c3-129">This includes text and graphics.</span></span> <span data-ttu-id="e32c3-130">Это приводит к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="e32c3-130">There is a performance penalty to this.</span></span> <span data-ttu-id="e32c3-131">Кроме того, при подготовке к просмотру на КОНТРОЛЛЕРе памяти не используется аппаратный ускоренный интерфейс GDI.</span><span class="sxs-lookup"><span data-stu-id="e32c3-131">Additionally, rendering to a memory DC is not GDI hardware accelerated.</span></span>

 

<span data-ttu-id="e32c3-132">Более подробный обзор взаимодействия с GDI см. в статье [взаимодействие с GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="e32c3-132">For a more detailed overview of interoperating with GDI see [Interoperating with GDI](interoperating-with-gdi.md).</span></span>

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a><span data-ttu-id="e32c3-133">4. Прозрачное отображение текста в градациях серого на поверхности GDI.</span><span class="sxs-lookup"><span data-stu-id="e32c3-133">4. Render Grayscale Text Transparently to a GDI Surface.</span></span> <span data-ttu-id="e32c3-134">(Windows 8 и более поздние версии)</span><span class="sxs-lookup"><span data-stu-id="e32c3-134">(Windows 8 and later)</span></span>

<span data-ttu-id="e32c3-135">Начиная с Windows 8, можно прозрачно визуализировать текст в градациях серого до поверхности GDI для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="e32c3-135">Starting in Windows 8, you can render grayscale text transparently to a GDI surface for better performance.</span></span> <span data-ttu-id="e32c3-136">Для этого необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e32c3-136">To do this you need to:</span></span>

1.  <span data-ttu-id="e32c3-137">Очистите контроллер памяти, чтобы он был прозрачным.</span><span class="sxs-lookup"><span data-stu-id="e32c3-137">Clear the memory DC to transparent.</span></span>
2.  <span data-ttu-id="e32c3-138">Отрисовка текста в памяти HDC с помощью сглаживания в оттенках серого (ДВРИТЕ \_ \_ режим сглаживания текста в \_ \_ оттенках серого).</span><span class="sxs-lookup"><span data-stu-id="e32c3-138">Render text to the memory HDC using grayscale antialiasing (DWRITE\_TEXT\_ANTIALIAS\_MODE\_GRAYSCALE).</span></span>
3.  <span data-ttu-id="e32c3-139">Используйте функцию [**алфабленд**](/windows/win32/api/wingdi/nf-wingdi-alphablend) , чтобы ВИЗУАЛИЗИРОВАТЬ память HDC явным образом на основе конечного целевого параметра HDC.</span><span class="sxs-lookup"><span data-stu-id="e32c3-139">Use the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function to render the memory HDC transparently on top of the final target HDC.</span></span>
4.  <span data-ttu-id="e32c3-140">Повторяйте столько раз, сколько необходимо (скажем, один раз в каждом глифе) и между другими изображениями может быть визуализирован непосредственно в конечный режим HDC без переписывания функцией [**алфабленд**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="e32c3-140">Repeat as many times as necessary (say, once per glyph run) and in between other graphics may be rendered directly to the final target HDC without being overwritten by the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a><span data-ttu-id="e32c3-141">См. также</span><span class="sxs-lookup"><span data-stu-id="e32c3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e32c3-142">Прорисовка с помощью Direct2D</span><span class="sxs-lookup"><span data-stu-id="e32c3-142">Render Using Direct2D</span></span>](rendering-by-using-direct2d.md)
</dt> <dt>

[<span data-ttu-id="e32c3-143">Отрисовка с использованием пользовательского средства отрисовки текста</span><span class="sxs-lookup"><span data-stu-id="e32c3-143">Render Using a Custom Text Renderer</span></span>](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[<span data-ttu-id="e32c3-144">Подготовка к просмотру на поверхности GDI</span><span class="sxs-lookup"><span data-stu-id="e32c3-144">Render to a GDI surface</span></span>](render-to-a-gdi-surface.md)
</dt> <dt>

[<span data-ttu-id="e32c3-145">Взаимодействие с GDI</span><span class="sxs-lookup"><span data-stu-id="e32c3-145">Interoperating with GDI</span></span>](interoperating-with-gdi.md)
</dt> </dl>

 

 