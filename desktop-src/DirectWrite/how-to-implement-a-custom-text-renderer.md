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
# <a name="render-using-a-custom-text-renderer"></a>Отрисовка с использованием пользовательского средства отрисовки текста

 [**Макет текста**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) [DirectWrite](direct-write-portal.md)может быть нарисован пользовательским модулем отрисовки текста, производным от [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). Пользовательский модуль подготовки отчетов необходим для использования преимуществ некоторых расширенных функций DirectWrite, таких как отрисовка растрового изображения или поверхности GDI, встроенные объекты и эффекты рисования клиента. В этом руководстве описываются методы **идвритетекстрендерер** и приводится пример реализации, которая использует [Direct2D](../direct2d/direct2d-portal.md) для отрисовки текста с заливкой битовой карты.

Этот учебник содержит следующие компоненты.

-   [Конструктор](#the-constructor)
-   [DrawGlyphRun ()](#drawglyphrun)
-   [Дравундерлине () и Дравстрикесраугх ()](#drawunderline-and-drawstrikethrough)
-   [Привязка пикселей, пикселы на DIP и преобразование](#pixel-snapping-pixels-per-dip-and-transform)
    -   [Испикселснаппингдисаблед ()](#ispixelsnappingdisabled)
    -   [Жеткурренттрансформ ()](#getcurrenttransform)
    -   [Жетпикселспердип ()](#getpixelsperdip)
-   [Дравинлинеобжект ()](#drawinlineobject)
-   [Деструктор](#the-destructor)
-   [Использование пользовательского модуля подготовки текста](#using-the-custom-text-renderer)

Пользовательский модуль подготовки текста должен реализовать методы, унаследованные от IUnknown, в дополнение к методам, перечисленным на странице ссылок [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) и ниже.

Полный исходный код для пользовательского модуля подготовки отчетов к тексту см. в файлах Кустомтекстрендерер. cpp и Кустомтекстрендерер. h [примера DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="the-constructor"></a>Конструктор

Обработчику пользовательского текста потребуется конструктор. В этом примере для отрисовки текста используются как сплошные, так и растровые [Direct2D](../direct2d/direct2d-portal.md) кисти.

Поэтому конструктор принимает параметры, приведенные в таблице ниже, с описанием.



| Параметр       | Описание                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *pD2DFactory*   | Указатель на объект [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , который будет использоваться для создания любых необходимых ресурсов Direct2D.                                                                                                        |
| *pRT*           | Указатель на объект [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) , в который будет визуализирован текст. |
| *паутлинебруш* | Указатель на [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) , который будет использоваться для рисования контура текста                                                                                                                     |
| *пфиллбруш*    | Указатель на [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , который будет использоваться для заполнения текста.                                                                                                                                      |



 

Они будут храниться в конструкторе, как показано в следующем коде.


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



## <a name="drawglyphrun"></a>DrawGlyphRun ()

Метод [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) является основным методом обратного вызова модуля подготовки текста. В дополнение к таким сведениям, как начальное начало и режим измерения, ему передается запуск глифов. Он также передает объект эффектов рисования клиента, применяемый к исполнению глифа. Дополнительные сведения см. в разделе [Добавление эффектов отрисовки клиента в раздел макета текста](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .

Эта реализация модуля подготовки отчетов выполняет визуализацию глифов, преобразуя их в [Direct2D](rendering-by-using-direct2d.md) геометрии, а затем рисуя и заполняя геометрические объекты. Это состоит из следующих шагов.

1.  Создайте объект [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , а затем извлеките объект [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) с помощью метода [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .

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

    

2.  [**\_ \_ Запуск глифа дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) , который передается в [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) , содержит объект [**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) с именем *фонтфаце*, который представляет начертание шрифта для всего выполнения глифа. Переведите контур глифа в приемник геометрии с помощью метода [**идвритефонтфаце:: жетглифрунаутлине**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , как показано в следующем коде.

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

    

3.  Завершив заполнение геометрического приемника, закройте его.

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  Начало работы с отсчетом глифа должно быть преобразовано, чтобы оно отображалось из правильного базового источника, как показано в следующем коде.

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    *Баселинеоригинкс* и *баселинеоригини* передаются как параметры в метод обратного вызова [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .

5.  Создайте преобразованную геометрию с помощью метода [**ID2D1Factory:: креатетрансформеджеометри**](../direct2d/id2d1factory-createtransformedgeometry.md) , передав геометрию пути и матрицу перевода.

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

    

6.  Наконец, Нарисуйте контур преобразованной геометрии и заполните его с помощью методов [**ID2D1RenderTarget::D равжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) и [**ID2D1RenderTarget:: филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) и [Direct2D](../direct2d/direct2d-portal.md) кистей, сохраненных как переменные члена.

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

    

7.  Теперь, когда рисование закончено, не забудьте очистить объекты, созданные в этом методе.

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a>Дравундерлине () и Дравстрикесраугх ()

[**Идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) также имеет обратные вызовы для рисования подчеркивания и зачеркивания. В этом примере рисуется простой прямоугольник для подчеркивания или зачеркивания, но могут быть выведены другие фигуры.

Рисование подчеркивания с помощью [Direct2D](../direct2d/direct2d-portal.md) состоит из следующих шагов.

1.  Сначала создайте структуру [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) размера и формы подчеркивания. Структура [**\_ подчеркивания дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) , которая передается в метод обратного вызова [**дравундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) , предоставляет смещение, ширину и толщину подчеркивания.

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  Затем создайте объект [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) с помощью метода [**ID2D1Factory:: креатеректанглежеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) и инициализированной структуры [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) .

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  Как и при выполнении глифа, источник геометрии подчеркивания должен быть преобразован на основе значений исходного плана с помощью метода [**креатетрансформеджеометри**](../direct2d/id2d1factory-createtransformedgeometry.md) .

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

    

4.  Наконец, Нарисуйте контур преобразованной геометрии и заполните его с помощью методов [**ID2D1RenderTarget::D равжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) и [**ID2D1RenderTarget:: филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) и [Direct2D](../direct2d/direct2d-portal.md) кистей, сохраненных как переменные члена.

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

    

5.  Теперь, когда рисование закончено, не забудьте очистить объекты, созданные в этом методе.

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

Процесс рисования зачеркивания одинаков. Однако зачеркивание будет иметь другое смещение и, скорее всего, другие значения ширины и толщины.

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a>Привязка пикселей, пикселы на DIP и преобразование

### <a name="ispixelsnappingdisabled"></a>Испикселснаппингдисаблед ()

Этот метод вызывается для определения того, отключена ли привязка пикселей. Рекомендуемое значение по умолчанию — **false**, а это выходные данные этого примера.


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a>Жеткурренттрансформ ()

Этот пример визуализируется в целевом объекте отрисовки Direct2D, поэтому перешлите преобразование из целевого объекта отрисовки с помощью [**ID2D1RenderTarget:: Transform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a>Жетпикселспердип ()

Этот метод вызывается для получения количества пикселей на аппаратно-независимый пиксель (DIP).


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a>Дравинлинеобжект ()

Пользовательский обработчик текста также имеет обратный вызов для рисования встроенных объектов. В этом примере [**дравинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) возвращает E \_ нотимпл. Объяснение того, как нарисовать встроенные объекты, выходит за рамки данного учебника. Дополнительные сведения см. в разделе [Добавление встроенных объектов в макет текста](how-to-add-inline-objects-to-a-text-layout.md) .

## <a name="the-destructor"></a>Деструктор

Важно освободить все указатели, которые использовались классом модуля визуализации пользовательского текста.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a>Использование пользовательского модуля подготовки текста

Для отображения с помощью пользовательского модуля подготовки отчетов используется метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , который принимает в качестве аргумента интерфейс обратного вызова, производный от [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) , как показано в следующем коде.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



Метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) вызывает методы предоставляемого обратного вызова пользовательского модуля подготовки отчетов. Описанные выше методы [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**дравундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**дравинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)и [**дравстрикесраугх**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) выполняют функции рисования.

 

 