---
title: Добавление клиентских эффектов рисования в макет текста
description: краткое руководство по добавлению эффектов рисования клиента в DirectWrite приложение, которое отображает текст с помощью интерфейса идвритетекстлайаут и пользовательского модуля подготовки отчетов к тексту.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bae98813d8f8aa8fc8a7df0a1a53d11a0329c93abb22a7f60d60754b8edc91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071717"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a>Добавление клиентских эффектов рисования в макет текста

краткое руководство по добавлению эффектов рисования клиента в [DirectWrite](direct-write-portal.md) приложение, которое отображает текст с помощью интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) и пользовательского модуля подготовки отчетов к тексту.

Конечным продуктом этого учебника является приложение, которое отображает текст с диапазонами текста с разными цветами рисования на каждом изображении, как показано на следующем снимке экрана.

![снимок экрана "пример создания клиентского документа" в разных цветах](images/drawingeffects.png)

> [!Note]  
> Этот учебник является упрощенным примером создания пользовательских эффектов отрисовки клиента, а не примером простого метода для рисования цвета текста. Дополнительные сведения см. на странице справочника по [**идвритетекстлайаут:: сетдравинжеффект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) .

 

Этот учебник содержит следующие компоненты.

-   [Шаг 1. Создание макета текста](#step-1-create-a-text-layout)
-   [Шаг 2. Реализация пользовательского класса эффектов рисования](#step-2-implement-a-custom-drawing-effect-class)
-   [Шаг 3. Реализация пользовательского класса модуля подготовки текста](#step-3-implement-a-custom-text-renderer-class)
    -   [Конструктор](#the-constructor)
    -   [Метод DrawGlyphRun](#the-drawglyphrun-method)
    -   [Деструктор](#the-destructor)
-   [Шаг 4. Создание модуля подготовки текста](#step-4-create-the-text-renderer)
-   [Шаг 5. Создание экземпляра объектов эффектов рисования цветов](#step-5-instantiate-the-color-drawing-effect-objects)
-   [Шаг 6. Установка эффектов рисования для конкретных диапазонов текста](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [Шаг 7. Рисование макета текста с помощью пользовательского модуля подготовки отчетов](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [Шаг 8. Очистка](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a>Шаг 1. Создание макета текста

Для начала потребуется приложение с объектом [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Если у вас уже есть приложение, отображающее текст с макетом текста, или вы используете Пользовательский пример кода Дравинжеффект, перейдите к шагу 2.

Чтобы добавить текстовый макет, необходимо выполнить следующие действия.

1.  Объявите указатель на интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) в качестве члена класса.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  В конце метода **креатедевицеиндепендентресаурцес** создайте объект интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , вызвав метод [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

3.  Наконец, не забудьте освободить текстовый макет в деструкторе.
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a>Шаг 2. Реализация пользовательского класса эффектов рисования

В отличие от методов, унаследованных от IUnknown, Пользовательский интерфейс эффектов рисования клиента не имеет никаких требований к методу, который он должен реализовывать. В этом случае класс **колордравинжеффект** просто содержит значение [**D2D1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) и объявляет методы для получения и задания этого значения, а также конструктор, который может изначально установить цвет.

После применения эффектов рисования клиента к текстовому диапазону в объекте [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) этот результат передается методу [**Идвритетекстрендерер::D равглифрун**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) любого выполнения глифа, который должен быть визуализирован. После этого методы рисования становятся доступными для модуля подготовки текста.

Результат рисования клиента может быть настолько сложным, насколько вы хотите сделать, составлять больше информации, чем в этом примере, а также предоставлять методы для изменения глифов, создания объектов, используемых для рисования, и т. д.

## <a name="step-3-implement-a-custom-text-renderer-class"></a>Шаг 3. Реализация пользовательского класса модуля подготовки текста

Чтобы воспользоваться преимуществами рисования клиента, необходимо реализовать пользовательский модуль подготовки текста. Этот модуль визуализации текста применяет к рисуемому фрагменту глифа результат рисования, переданный в него методом [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) .

### <a name="the-constructor"></a>Конструктор

Конструктор пользовательского текстового модуля подготовки отчетов сохраняет объект [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , который будет использоваться для создания объектов [Direct2D](../direct2d/direct2d-portal.md) , и целевой объект отрисовки Direct2D, на который будет нарисован текст.


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
}
```



### <a name="the-drawglyphrun-method"></a>Метод DrawGlyphRun

Запуск глифа — это набор глифов, имеющих одинаковый формат, включая эффекты рисования клиента. Метод [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) осуществляет отрисовку текста для указанного запуска глифа.

Сначала создайте [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) и [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), а затем извлеките структуру запуска глифов с помощью [**идвритефонтфаце:: жетглифрунаутлине**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline). Затем преобразуйте источник геометрии с помощью метода [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory:: креатетрансформеджеометри**](../direct2d/id2d1factory-createtransformedgeometry.md) , как показано в следующем коде.


```C++
HRESULT hr = S_OK;

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

// Close the geometry sink
if (SUCCEEDED(hr))
{
    hr = pSink->Close();
}

// Initialize a matrix to translate the origin of the glyph run.
D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
    1.0f, 0.0f,
    0.0f, 1.0f,
    baselineOriginX, baselineOriginY
    );

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



Затем объявите объект сплошной кисти [Direct2D](../direct2d/direct2d-portal.md) .


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



Если параметр *клиентдравинжеффект* имеет значение, отличное от NULL, запросите объект для интерфейса **колордравинжеффект** . Это будет работать, так как этот класс будет установлен как результат рисования клиента в текстовых диапазонах объекта макета текста.

Получив указатель на интерфейс **колордравинжеффект** , можно получить значение [**D2D1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) , которое он **сохраняет, с помощью метода WebMethod** . Затем используйте **D2D1 \_ Color \_ F** , чтобы создать [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) в этом цвете.

Если параметр *клиентдравинжеффект* имеет **значение NULL**, просто создайте черный [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).


```C++
// If there is a drawing effect create a color brush using it, otherwise create a black brush.
if (clientDrawingEffect != NULL)
{
    // Go from IUnknown to ColorDrawingEffect.
    ColorDrawingEffect *colorDrawingEffect;

    clientDrawingEffect->QueryInterface(__uuidof(ColorDrawingEffect), reinterpret_cast<void**>(&colorDrawingEffect));

    // Get the color from the ColorDrawingEffect object.
    D2D1_COLOR_F color;

    colorDrawingEffect->GetColor(&color);

    // Create the brush using the color pecified by our ColorDrawingEffect object.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            color,
            &pBrush);
    }

    SafeRelease(&colorDrawingEffect);
}
else
{
    // Create a black brush.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            D2D1::ColorF(
            D2D1::ColorF::Black
            ),
            &pBrush);
    }
}
```



Наконец, нарисуйте геометрию контура и заполните ее, используя только что созданную цветную кисть.


```C++
if (SUCCEEDED(hr))
{
    // Draw the outline of the glyph run
    pRT_->DrawGeometry(
        pTransformedGeometry,
        pBrush
        );

    // Fill in the glyph run
    pRT_->FillGeometry(
        pTransformedGeometry,
        pBrush
        );
}
```



### <a name="the-destructor"></a>Деструктор

Не забудьте освободить фабрику [Direct2D](../direct2d/direct2d-portal.md) и целевой объект отрисовки в деструкторе.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a>Шаг 4. Создание модуля подготовки текста

В ресурсах **креатедевицедепендент** создайте пользовательский объект модуля подготовки текста. Он зависит от устройства, так как использует **ID2D1RenderTarget**, который зависит от устройства.


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a>Шаг 5. Создание экземпляра объектов эффектов рисования цветов

Создавайте объекты **колордравинжеффект** красным, зеленым и синим.


```C++
// Instantiate some custom color drawing effects.
redDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Red
        )
    );

blueDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Blue
        )
    );

greenDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Green
        )
    );
```



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a>Шаг 6. Установка эффектов рисования для конкретных диапазонов текста

Установите эффекты рисования для отдельных диапазонов текста с помощью метода [**идвритетекстлайау:: сетдравинжеффект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) и структуры [**\_ текстового \_ диапазона дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) .


```C++
// Set the drawing effects.

// Red.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {0,
                                   14};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(redDrawingEffect_, textRange);
    }
}

// Blue.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {14,
                                   7};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(blueDrawingEffect_, textRange);
    }
}

// Green.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {21,
                                   8};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(greenDrawingEffect_, textRange);
    }
}
```



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a>Шаг 7. Рисование макета текста с помощью пользовательского модуля подготовки отчетов

Необходимо вызвать метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , а не методы [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) или [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) .


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a>Шаг 8. Очистка

В деструкторе DemoApp отпустите пользовательский модуль подготовки текста.


```C++
SafeRelease(&pTextRenderer_);
```



После этого добавьте код для освобождения классов эффектов рисования клиента.


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 