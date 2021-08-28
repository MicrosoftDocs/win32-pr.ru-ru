---
title: Добавление встроенных объектов в макет текста
description: содержит краткое руководство по добавлению встроенных объектов в DirectWrite приложение, которое отображает текст с помощью интерфейса идвритетекстлайаут.
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca4969ded311bbaa4e87e5b70f1df1379c4ca549d2db06c8d1186ba548c77a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902902"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a>Добавление встроенных объектов в макет текста

содержит краткое руководство по добавлению встроенных объектов в [DirectWrite](direct-write-portal.md) приложение, которое отображает текст с помощью интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Конечным продуктом этого учебника является приложение, которое отображает текст со встроенным изображением, которое встроено в него, как показано на следующем снимке экрана.

![снимок экрана "Пример встроенного объекта" с внедренным изображением](images/inlineobject.png)

Этот учебник содержит следующие компоненты.

-   [Шаг 1. Создание макета текста.](#step-1-create-a-text-layout)
-   [Шаг 2. определение класса, производного от интерфейса Идвритеинлинеобжект.](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [Шаг 3. Реализация встроенного класса объекта.](#step-3-implement-the-inline-object-class)
    -   [Конструктор.](#the-constructor)
    -   [Метод Draw.](#the-draw-method)
    -   [Методических метрик.](#the-getmetrics-method)
    -   [Метод Жетоверхангметрикс.](#the-getoverhangmetrics-method)
    -   [Метод Жетбреаккондитионс.](#the-getbreakconditions-method)
-   [Шаг 4. Создайте экземпляр класса Инлинеимаже и добавьте его в макет текста.](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a>Шаг 1. Создание макета текста.

Для начала потребуется приложение с объектом [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Если у вас уже есть приложение, отображающее текст с макетом, перейдите к шагу 2.

Чтобы добавить текстовый макет, необходимо выполнить следующие действия.

1.  Объявите указатель на интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) в качестве члена класса.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  В конце метода Креатедевицеиндепендентресаурцес создайте объект интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , вызвав метод [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .
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

    

3.  Затем необходимо изменить вызов метода [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) на [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), как показано в следующем коде.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a>Шаг 2. определение класса, производного от интерфейса Идвритеинлинеобжект.

поддержка встроенных объектов в [DirectWrite](direct-write-portal.md) предоставляется интерфейсом [**идвритеинлинеобжект**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) . Чтобы использовать встроенные объекты, необходимо реализовать этот интерфейс. Он обрабатывает рисунок встроенного объекта, а также предоставляет для модуля подготовки отчетов метрики и другие сведения.

Создайте новый файл заголовка и объявите интерфейс с именем Инлинеимаже, производный от [**идвритеинлинеобжект**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).

Помимо QueryInterface, AddRef и Release, унаследованных от IUnknown, этот класс должен иметь следующие методы:

-   [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [**Метрики**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [**жетоверхангметрикс**](idwriteinlineobject-getoverhangmetrics.md)
-   [**жетбреаккондитионс**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a>Шаг 3. Реализация встроенного класса объекта.

Создайте новый файл C++ с именем Инлинеимаже. cpp для реализации класса. В дополнение к методу Лоадбитмапфромфиле и методам, унаследованным от интерфейса IUnknown, класс Инлинеимаже состоит из следующих методов.

### <a name="the-constructor"></a>Конструктор.


```C++
InlineImage::InlineImage(
    ID2D1RenderTarget *pRenderTarget, 
    IWICImagingFactory *pIWICFactory,
    PCWSTR uri
    )
{
    // Save the render target for later.
    pRT_ = pRenderTarget;

    pRT_->AddRef();

    // Load the bitmap from a file.
    LoadBitmapFromFile(
        pRenderTarget,
        pIWICFactory,
        uri,
        &pBitmap_
        );
}
```



Первым аргументом конструктора является ID2D1RenderTarget, к которому будет отрисовываться встроенное изображение. Он сохраняется для дальнейшего использования при рисовании.

Целевой объект отрисовки, IWICImagingFactory и URI имени файла передаются в метод Лоадбитмапфромфиле, который загружает точечный рисунок и сохраняет размер битовой карты (ширину и высоту) в \_ переменной-члене Rect.

### <a name="the-draw-method"></a>Метод Draw.

Метод [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) является обратным вызовом, который вызывается объектом [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) при необходимости прорисовки встроенного объекта. Макет текста не вызывает этот метод напрямую.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::Draw(
    __maybenull void* clientDrawingContext,
    IDWriteTextRenderer* renderer,
    FLOAT originX,
    FLOAT originY,
    BOOL isSideways,
    BOOL isRightToLeft,
    IUnknown* clientDrawingEffect
    )
{
    float height    = rect_.bottom - rect_.top;
    float width     = rect_.right  - rect_.left;
    D2D1_RECT_F destRect  = {originX, originY, originX + width, originY + height};

    pRT_->DrawBitmap(pBitmap_, destRect);

    return S_OK;
}
```



В этом случае Рисование растрового изображения выполняется с помощью метода [**ID2D1RenderTarget::D равбитмап**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) . Однако можно использовать любой метод рисования.

### <a name="the-getmetrics-method"></a>Методических метрик.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetMetrics(
    __out DWRITE_INLINE_OBJECT_METRICS* metrics
    )
{
    DWRITE_INLINE_OBJECT_METRICS inlineMetrics = {};
    inlineMetrics.width     = rect_.right  - rect_.left;
    inlineMetrics.height    = rect_.bottom - rect_.top;
    inlineMetrics.baseline  = baseline_;
    *metrics = inlineMetrics;
    return S_OK;
}
```



Для метода [](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) дврите Храните ширину, высоту и базовую базу данных в структуре [**\_ \_ \_ метрики встроенного объекта**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) . [**Идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) вызывает эту функцию обратного вызова для получения измерения встроенного объекта.

### <a name="the-getoverhangmetrics-method"></a>Метод Жетоверхангметрикс.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetOverhangMetrics(
    __out DWRITE_OVERHANG_METRICS* overhangs
    )
{
    overhangs->left      = 0;
    overhangs->top       = 0;
    overhangs->right     = 0;
    overhangs->bottom    = 0;
    return S_OK;
}
```



В этом случае никакой выступ не требуется, поэтому метод [**жетоверхангметрикс**](idwriteinlineobject-getoverhangmetrics.md) возвращает все нули.

### <a name="the-getbreakconditions-method"></a>Метод Жетбреаккондитионс.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetBreakConditions(
    __out DWRITE_BREAK_CONDITION* breakConditionBefore,
    __out DWRITE_BREAK_CONDITION* breakConditionAfter
    )
{
    *breakConditionBefore = DWRITE_BREAK_CONDITION_NEUTRAL;
    *breakConditionAfter  = DWRITE_BREAK_CONDITION_NEUTRAL;
    return S_OK;
}
```



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a>Шаг 4. Создайте экземпляр класса Инлинеимаже и добавьте его в макет текста.

Наконец, в методе Креатедевицедепендентресаурцес создайте экземпляр класса Инлинеимаже и добавьте его в макет текста. Так как он содержит ссылку на [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), который является ресурсом, зависимым от устройства, и [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) создается с помощью целевого объекта прорисовки, инлинеимаже также зависит от устройства, и его необходимо создать повторно, если целевой объект прорисовки создан повторно.


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



Метод [**идвритетекстлайаут:: сетинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) принимает структуру текстового диапазона. Объект применяется к указанному здесь диапазону, и любой текст в диапазоне будет подавлен. Если длина текстового диапазона равна 0, объект не будет нарисован.

В этом примере есть звездочка () в \* качестве заполнителя в позиции, где будет отображаться изображение.


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



Так как класс Инлинеимаже зависит от [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), его необходимо освободить при освобождении целевого объекта отрисовки.


```C++
SafeRelease(&pInlineImage_);
```



 

 