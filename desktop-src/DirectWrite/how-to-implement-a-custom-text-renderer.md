---
title: Отрисовка с использованием пользовательского средства отрисовки текста
description: Макет текста DirectWrite \ 160; может быть нарисован пользовательским модулем отрисовки текста, производным от Идвритетекстрендерер.
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cda56fc5cc38a62e48a2f62066edfec2327e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413246"
---
# <a name="render-using-a-custom-text-renderer"></a><span data-ttu-id="dddb2-103">Отрисовка с использованием пользовательского средства отрисовки текста</span><span class="sxs-lookup"><span data-stu-id="dddb2-103">Render Using a Custom Text Renderer</span></span>

<span data-ttu-id="dddb2-104"> [**Макет текста**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) [DirectWrite](direct-write-portal.md)может быть нарисован пользовательским модулем отрисовки текста, производным от [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span><span class="sxs-lookup"><span data-stu-id="dddb2-104">A [DirectWrite](direct-write-portal.md) [**text layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) can be drawn by a custom text renderer derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span></span> <span data-ttu-id="dddb2-105">Пользовательский модуль подготовки отчетов необходим для использования преимуществ некоторых расширенных функций DirectWrite, таких как отрисовка растрового изображения или поверхности GDI, встроенные объекты и эффекты рисования клиента.</span><span class="sxs-lookup"><span data-stu-id="dddb2-105">A custom renderer is required to take advantage of some advanced features of DirectWrite, such as rendering to a bitmap or GDI surface, inline objects, and client drawing effects.</span></span> <span data-ttu-id="dddb2-106">В этом руководстве описываются методы **идвритетекстрендерер** и приводится пример реализации, которая использует [Direct2D](../direct2d/direct2d-portal.md) для отрисовки текста с заливкой битовой карты.</span><span class="sxs-lookup"><span data-stu-id="dddb2-106">This tutorial describes the methods of **IDWriteTextRenderer**, and provides an example implementation that uses [Direct2D](../direct2d/direct2d-portal.md) to render text with a bitmap fill.</span></span>

<span data-ttu-id="dddb2-107">Этот учебник содержит следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="dddb2-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="dddb2-108">Конструктор</span><span class="sxs-lookup"><span data-stu-id="dddb2-108">The Constructor</span></span>](#the-constructor)
-   [<span data-ttu-id="dddb2-109">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-109">DrawGlyphRun()</span></span>](#drawglyphrun)
-   [<span data-ttu-id="dddb2-110">Дравундерлине () и Дравстрикесраугх ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-110">DrawUnderline() and DrawStrikethrough()</span></span>](#drawunderline-and-drawstrikethrough)
-   [<span data-ttu-id="dddb2-111">Привязка пикселей, пикселы на DIP и преобразование</span><span class="sxs-lookup"><span data-stu-id="dddb2-111">Pixel Snapping, Pixels per DIP, and Transform</span></span>](#pixel-snapping-pixels-per-dip-and-transform)
    -   [<span data-ttu-id="dddb2-112">Испикселснаппингдисаблед ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-112">IsPixelSnappingDisabled()</span></span>](#ispixelsnappingdisabled)
    -   [<span data-ttu-id="dddb2-113">Жеткурренттрансформ ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-113">GetCurrentTransform()</span></span>](#getcurrenttransform)
    -   [<span data-ttu-id="dddb2-114">Жетпикселспердип ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-114">GetPixelsPerDip()</span></span>](#getpixelsperdip)
-   [<span data-ttu-id="dddb2-115">Дравинлинеобжект ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-115">DrawInlineObject()</span></span>](#drawinlineobject)
-   [<span data-ttu-id="dddb2-116">Деструктор</span><span class="sxs-lookup"><span data-stu-id="dddb2-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="dddb2-117">Использование пользовательского модуля подготовки текста</span><span class="sxs-lookup"><span data-stu-id="dddb2-117">Using the Custom Text Renderer</span></span>](#using-the-custom-text-renderer)

<span data-ttu-id="dddb2-118">Пользовательский модуль подготовки текста должен реализовать методы, унаследованные от IUnknown, в дополнение к методам, перечисленным на странице ссылок [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) и ниже.</span><span class="sxs-lookup"><span data-stu-id="dddb2-118">Your custom text renderer must implement the methods inherited from IUnknown in addition to the methods listed on the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page and below.</span></span>

<span data-ttu-id="dddb2-119">Полный исходный код для пользовательского модуля подготовки отчетов к тексту см. в файлах Кустомтекстрендерер. cpp и Кустомтекстрендерер. h [примера DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="dddb2-119">For the full source code for the custom text renderer, see the CustomTextRenderer.cpp and CustomTextRenderer.h files of the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="the-constructor"></a><span data-ttu-id="dddb2-120">Конструктор</span><span class="sxs-lookup"><span data-stu-id="dddb2-120">The Constructor</span></span>

<span data-ttu-id="dddb2-121">Обработчику пользовательского текста потребуется конструктор.</span><span class="sxs-lookup"><span data-stu-id="dddb2-121">Your custom text renderer will need a constructor.</span></span> <span data-ttu-id="dddb2-122">В этом примере для отрисовки текста используются как сплошные, так и растровые [Direct2D](../direct2d/direct2d-portal.md) кисти.</span><span class="sxs-lookup"><span data-stu-id="dddb2-122">This example uses both solid and bitmap [Direct2D](../direct2d/direct2d-portal.md) brushes to render the text.</span></span>

<span data-ttu-id="dddb2-123">Поэтому конструктор принимает параметры, приведенные в таблице ниже, с описанием.</span><span class="sxs-lookup"><span data-stu-id="dddb2-123">Because of this, the constructor takes the parameters found in the table below with descriptions.</span></span>



| <span data-ttu-id="dddb2-124">Параметр</span><span class="sxs-lookup"><span data-stu-id="dddb2-124">Parameter</span></span>       | <span data-ttu-id="dddb2-125">Описание</span><span class="sxs-lookup"><span data-stu-id="dddb2-125">Description</span></span>                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dddb2-126">*pD2DFactory*</span><span class="sxs-lookup"><span data-stu-id="dddb2-126">*pD2DFactory*</span></span>   | <span data-ttu-id="dddb2-127">Указатель на объект [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , который будет использоваться для создания любых необходимых ресурсов Direct2D.</span><span class="sxs-lookup"><span data-stu-id="dddb2-127">A pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create any Direct2D resources that are needed.</span></span>                                                                                                        |
| <span data-ttu-id="dddb2-128">*pRT*</span><span class="sxs-lookup"><span data-stu-id="dddb2-128">*pRT*</span></span>           | <span data-ttu-id="dddb2-129">Указатель на объект [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) , в который будет визуализирован текст.</span><span class="sxs-lookup"><span data-stu-id="dddb2-129">A pointer to the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object that the text will be rendered to.</span></span> |
| <span data-ttu-id="dddb2-130">*паутлинебруш*</span><span class="sxs-lookup"><span data-stu-id="dddb2-130">*pOutlineBrush*</span></span> | <span data-ttu-id="dddb2-131">Указатель на [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) , который будет использоваться для рисования контура текста</span><span class="sxs-lookup"><span data-stu-id="dddb2-131">A pointer to the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) that will be use to draw outline of the text</span></span>                                                                                                                     |
| <span data-ttu-id="dddb2-132">*пфиллбруш*</span><span class="sxs-lookup"><span data-stu-id="dddb2-132">*pFillBrush*</span></span>    | <span data-ttu-id="dddb2-133">Указатель на [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , который будет использоваться для заполнения текста.</span><span class="sxs-lookup"><span data-stu-id="dddb2-133">A pointer to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that will be used to fill the text.</span></span>                                                                                                                                      |



 

<span data-ttu-id="dddb2-134">Они будут храниться в конструкторе, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="dddb2-134">These will be stored by the constructor as shown in the following code.</span></span>


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT, 
    ID2D1SolidColorBrush* pOutlineBrush, 
    ID2D1BitmapBrush* pFillBrush
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT), 
pOutlineBrush_(pOutlineBrush), 
pFillBrush_(pFillBrush)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
    pOutlineBrush_->AddRef();
    pFillBrush_->AddRef();
}
```



## <a name="drawglyphrun"></a><span data-ttu-id="dddb2-135">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-135">DrawGlyphRun()</span></span>

<span data-ttu-id="dddb2-136">Метод [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) является основным методом обратного вызова модуля подготовки текста.</span><span class="sxs-lookup"><span data-stu-id="dddb2-136">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method is the main callback method of the text renderer.</span></span> <span data-ttu-id="dddb2-137">В дополнение к таким сведениям, как начальное начало и режим измерения, ему передается запуск глифов.</span><span class="sxs-lookup"><span data-stu-id="dddb2-137">It is passed a run of glyphs to be rendered in addition to information such as the baseline origin and measuring mode.</span></span> <span data-ttu-id="dddb2-138">Он также передает объект эффектов рисования клиента, применяемый к исполнению глифа.</span><span class="sxs-lookup"><span data-stu-id="dddb2-138">It also passes a client drawing effect object to be applied to the glyph run.</span></span> <span data-ttu-id="dddb2-139">Дополнительные сведения см. в разделе [Добавление эффектов отрисовки клиента в раздел макета текста](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="dddb2-139">For more information, see the [How to Add Client Drawing Effects to a Text Layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) topic.</span></span>

<span data-ttu-id="dddb2-140">Эта реализация модуля подготовки отчетов выполняет визуализацию глифов, преобразуя их в [Direct2D](rendering-by-using-direct2d.md) геометрии, а затем рисуя и заполняя геометрические объекты.</span><span class="sxs-lookup"><span data-stu-id="dddb2-140">This text renderer implementation renders glyph runs by converting them to [Direct2D](rendering-by-using-direct2d.md) geometries and then drawing and filling the geometries.</span></span> <span data-ttu-id="dddb2-141">Это состоит из следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="dddb2-141">This consists of the following steps.</span></span>

1.  <span data-ttu-id="dddb2-142">Создайте объект [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , а затем извлеките объект [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) с помощью метода [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .</span><span class="sxs-lookup"><span data-stu-id="dddb2-142">Create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object, and then retrieve the [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) object by using the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>

    ```C++
    // Create the path geometry.
    ID2D1PathGeometry* pPathGeometry = NULL;
    hr = pD2DFactory_->CreatePathGeometry(
            &pPathGeometry
            );

    // Write to the path geometry using the geometry sink.
    ID2D1GeometrySink* pSink = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Open(
            &pSink
            );
    }
    ```

    

2.  <span data-ttu-id="dddb2-143">[**\_ \_ Запуск глифа дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) , который передается в [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) , содержит объект [**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) с именем *фонтфаце*, который представляет начертание шрифта для всего выполнения глифа.</span><span class="sxs-lookup"><span data-stu-id="dddb2-143">The [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) that is passed to [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contains a [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object, named *fontFace*, that represents the font face for the whole glyph run.</span></span> <span data-ttu-id="dddb2-144">Переведите контур глифа в приемник геометрии с помощью метода [**идвритефонтфаце:: жетглифрунаутлине**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="dddb2-144">Put the outline of the glyph run into the geometry sink by using the [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) method, as shown in the following code.</span></span>

    ```C++
    // Get the glyph run outline geometries back from DirectWrite and place them within the
    // geometry sink.
    if (SUCCEEDED(hr))
    {
        hr = glyphRun->fontFace->GetGlyphRunOutline(
            glyphRun->fontEmSize,
            glyphRun->glyphIndices,
            glyphRun->glyphAdvances,
            glyphRun->glyphOffsets,
            glyphRun->glyphCount,
            glyphRun->isSideways,
            glyphRun->bidiLevel%2,
            pSink
            );
    }
    ```

    

3.  <span data-ttu-id="dddb2-145">Завершив заполнение геометрического приемника, закройте его.</span><span class="sxs-lookup"><span data-stu-id="dddb2-145">After filling the geometry sink, close it.</span></span>

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  <span data-ttu-id="dddb2-146">Начало работы с отсчетом глифа должно быть преобразовано, чтобы оно отображалось из правильного базового источника, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="dddb2-146">The origin of the glyph run must be translated so that it is rendered from the correct baseline origin, as shown in the following code.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    <span data-ttu-id="dddb2-147">*Баселинеоригинкс* и *баселинеоригини* передаются как параметры в метод обратного вызова [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="dddb2-147">The *baselineOriginX* and *baselineOriginY* are passed as parameters to the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback method.</span></span>

5.  <span data-ttu-id="dddb2-148">Создайте преобразованную геометрию с помощью метода [**ID2D1Factory:: креатетрансформеджеометри**](../direct2d/id2d1factory-createtransformedgeometry.md) , передав геометрию пути и матрицу перевода.</span><span class="sxs-lookup"><span data-stu-id="dddb2-148">Create the transformed geometry by using the [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method and passing the path geometry and the translation matrix.</span></span>

    ```C++
    // Create the transformed geometry
    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pPathGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

6.  <span data-ttu-id="dddb2-149">Наконец, Нарисуйте контур преобразованной геометрии и заполните его с помощью методов [**ID2D1RenderTarget::D равжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) и [**ID2D1RenderTarget:: филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) и [Direct2D](../direct2d/direct2d-portal.md) кистей, сохраненных как переменные члена.</span><span class="sxs-lookup"><span data-stu-id="dddb2-149">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

7.  <span data-ttu-id="dddb2-150">Теперь, когда рисование закончено, не забудьте очистить объекты, созданные в этом методе.</span><span class="sxs-lookup"><span data-stu-id="dddb2-150">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a><span data-ttu-id="dddb2-151">Дравундерлине () и Дравстрикесраугх ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-151">DrawUnderline() and DrawStrikethrough()</span></span>

<span data-ttu-id="dddb2-152">[**Идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) также имеет обратные вызовы для рисования подчеркивания и зачеркивания.</span><span class="sxs-lookup"><span data-stu-id="dddb2-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) also has callbacks for drawing the underline and strikethrough.</span></span> <span data-ttu-id="dddb2-153">В этом примере рисуется простой прямоугольник для подчеркивания или зачеркивания, но могут быть выведены другие фигуры.</span><span class="sxs-lookup"><span data-stu-id="dddb2-153">This example draws a simple rectangle for an underline or strikethrough, but other shapes can be drawn.</span></span>

<span data-ttu-id="dddb2-154">Рисование подчеркивания с помощью [Direct2D](../direct2d/direct2d-portal.md) состоит из следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="dddb2-154">Drawing an underline by using [Direct2D](../direct2d/direct2d-portal.md) consists of the following steps.</span></span>

1.  <span data-ttu-id="dddb2-155">Сначала создайте структуру [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) размера и формы подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="dddb2-155">First, create a [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure of the size and shape of the underline.</span></span> <span data-ttu-id="dddb2-156">Структура [**\_ подчеркивания дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) , которая передается в метод обратного вызова [**дравундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) , предоставляет смещение, ширину и толщину подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="dddb2-156">The [**DWRITE\_UNDERLINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) structure that is passed to the [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) callback method provides the offset, width, and thickness of the underline.</span></span>

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  <span data-ttu-id="dddb2-157">Затем создайте объект [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) с помощью метода [**ID2D1Factory:: креатеректанглежеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) и инициализированной структуры [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) .</span><span class="sxs-lookup"><span data-stu-id="dddb2-157">Next, create an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object by using the [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) method and the initialized [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure.</span></span>

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  <span data-ttu-id="dddb2-158">Как и при выполнении глифа, источник геометрии подчеркивания должен быть преобразован на основе значений исходного плана с помощью метода [**креатетрансформеджеометри**](../direct2d/id2d1factory-createtransformedgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="dddb2-158">As with the glyph run, the origin of the underline geometry must be translated, based on the baseline origin values, by using the [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the underline
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );

    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pRectangleGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

4.  <span data-ttu-id="dddb2-159">Наконец, Нарисуйте контур преобразованной геометрии и заполните его с помощью методов [**ID2D1RenderTarget::D равжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) и [**ID2D1RenderTarget:: филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) и [Direct2D](../direct2d/direct2d-portal.md) кистей, сохраненных как переменные члена.</span><span class="sxs-lookup"><span data-stu-id="dddb2-159">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

5.  <span data-ttu-id="dddb2-160">Теперь, когда рисование закончено, не забудьте очистить объекты, созданные в этом методе.</span><span class="sxs-lookup"><span data-stu-id="dddb2-160">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

<span data-ttu-id="dddb2-161">Процесс рисования зачеркивания одинаков.</span><span class="sxs-lookup"><span data-stu-id="dddb2-161">The process for drawing a strikethrough is the same.</span></span> <span data-ttu-id="dddb2-162">Однако зачеркивание будет иметь другое смещение и, скорее всего, другие значения ширины и толщины.</span><span class="sxs-lookup"><span data-stu-id="dddb2-162">However, the strikethrough will have a different offset, and likely a different width and thickness.</span></span>

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a><span data-ttu-id="dddb2-163">Привязка пикселей, пикселы на DIP и преобразование</span><span class="sxs-lookup"><span data-stu-id="dddb2-163">Pixel Snapping, Pixels per DIP, and Transform</span></span>

### <a name="ispixelsnappingdisabled"></a><span data-ttu-id="dddb2-164">Испикселснаппингдисаблед ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-164">IsPixelSnappingDisabled()</span></span>

<span data-ttu-id="dddb2-165">Этот метод вызывается для определения того, отключена ли привязка пикселей.</span><span class="sxs-lookup"><span data-stu-id="dddb2-165">This method is called to determine whether pixel snapping is disabled.</span></span> <span data-ttu-id="dddb2-166">Рекомендуемое значение по умолчанию — **false**, а это выходные данные этого примера.</span><span class="sxs-lookup"><span data-stu-id="dddb2-166">The recommended default is **FALSE**, and that is the output of this example.</span></span>


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a><span data-ttu-id="dddb2-167">Жеткурренттрансформ ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-167">GetCurrentTransform()</span></span>

<span data-ttu-id="dddb2-168">Этот пример визуализируется в целевом объекте отрисовки Direct2D, поэтому перешлите преобразование из целевого объекта отрисовки с помощью [**ID2D1RenderTarget:: Transform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span><span class="sxs-lookup"><span data-stu-id="dddb2-168">This example renders to a Direct2D render target, so forward the transform from the render target using [**ID2D1RenderTarget::GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span></span>


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a><span data-ttu-id="dddb2-169">Жетпикселспердип ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-169">GetPixelsPerDip()</span></span>

<span data-ttu-id="dddb2-170">Этот метод вызывается для получения количества пикселей на аппаратно-независимый пиксель (DIP).</span><span class="sxs-lookup"><span data-stu-id="dddb2-170">This method is called to get the number of pixels per Device Independent Pixel (DIP).</span></span>


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a><span data-ttu-id="dddb2-171">Дравинлинеобжект ()</span><span class="sxs-lookup"><span data-stu-id="dddb2-171">DrawInlineObject()</span></span>

<span data-ttu-id="dddb2-172">Пользовательский обработчик текста также имеет обратный вызов для рисования встроенных объектов.</span><span class="sxs-lookup"><span data-stu-id="dddb2-172">A custom text renderer also has a callback for drawing inline objects.</span></span> <span data-ttu-id="dddb2-173">В этом примере [**дравинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="dddb2-173">In this example, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) returns E\_NOTIMPL.</span></span> <span data-ttu-id="dddb2-174">Объяснение того, как нарисовать встроенные объекты, выходит за рамки данного учебника.</span><span class="sxs-lookup"><span data-stu-id="dddb2-174">An explanation of how to draw inline objects is beyond the scope of this tutorial.</span></span> <span data-ttu-id="dddb2-175">Дополнительные сведения см. в разделе [Добавление встроенных объектов в макет текста](how-to-add-inline-objects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="dddb2-175">For more information, see the [How to Add Inline Objects to a Text Layout](how-to-add-inline-objects-to-a-text-layout.md) topic.</span></span>

## <a name="the-destructor"></a><span data-ttu-id="dddb2-176">Деструктор</span><span class="sxs-lookup"><span data-stu-id="dddb2-176">The Destructor</span></span>

<span data-ttu-id="dddb2-177">Важно освободить все указатели, которые использовались классом модуля визуализации пользовательского текста.</span><span class="sxs-lookup"><span data-stu-id="dddb2-177">It is important to release any pointers that were used by the custom text renderer class.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a><span data-ttu-id="dddb2-178">Использование пользовательского модуля подготовки текста</span><span class="sxs-lookup"><span data-stu-id="dddb2-178">Using the Custom Text Renderer</span></span>

<span data-ttu-id="dddb2-179">Для отображения с помощью пользовательского модуля подготовки отчетов используется метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , который принимает в качестве аргумента интерфейс обратного вызова, производный от [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="dddb2-179">You render with the custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="dddb2-180">Метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) вызывает методы предоставляемого обратного вызова пользовательского модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="dddb2-180">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="dddb2-181">Описанные выше методы [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**дравундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**дравинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)и [**дравстрикесраугх**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) выполняют функции рисования.</span><span class="sxs-lookup"><span data-stu-id="dddb2-181">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods described above perform the drawing functions.</span></span>

 

 