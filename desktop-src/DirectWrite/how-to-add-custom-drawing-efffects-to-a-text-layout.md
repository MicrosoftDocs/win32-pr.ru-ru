---
title: Добавление клиентских эффектов рисования в макет текста
description: Краткое руководство по добавлению эффектов рисования клиента в приложение DirectWrite, которое отображает текст с помощью интерфейса Идвритетекстлайаут и пользовательского модуля подготовки текста.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338dc1a720bde80c1daf2b4baf7c7a4bad6d2cff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070259"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a><span data-ttu-id="5e38e-103">Добавление клиентских эффектов рисования в макет текста</span><span class="sxs-lookup"><span data-stu-id="5e38e-103">How to Add Client Drawing Effects to a Text Layout</span></span>

<span data-ttu-id="5e38e-104">Краткое руководство по добавлению эффектов рисования клиента в приложение [DirectWrite](direct-write-portal.md) , которое отображает текст с помощью интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) и пользовательского модуля подготовки текста.</span><span class="sxs-lookup"><span data-stu-id="5e38e-104">Provides a short tutorial on adding client drawing effects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface and a custom text renderer.</span></span>

<span data-ttu-id="5e38e-105">Конечным продуктом этого учебника является приложение, которое отображает текст с диапазонами текста с разными цветами рисования на каждом изображении, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="5e38e-105">The end product of this tutorial is an application that displays text that has ranges of text with a different color drawing effect on each, as shown in the following screen shot.</span></span>

![снимок экрана "пример создания клиентского документа"](images/drawingeffects.png)

> [!Note]  
> <span data-ttu-id="5e38e-108">Этот учебник является упрощенным примером создания пользовательских эффектов отрисовки клиента, а не примером простого метода для рисования цвета текста.</span><span class="sxs-lookup"><span data-stu-id="5e38e-108">This tutorial is meant to be a simplified example of how to create custom client drawing effects, not an example of a simple method for drawing color text.</span></span> <span data-ttu-id="5e38e-109">Дополнительные сведения см. на странице справочника по [**идвритетекстлайаут:: сетдравинжеффект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) .</span><span class="sxs-lookup"><span data-stu-id="5e38e-109">See the [**IDWriteTextLayout::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) reference page for more information.</span></span>

 

<span data-ttu-id="5e38e-110">Этот учебник содержит следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="5e38e-110">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="5e38e-111">Шаг 1. Создание макета текста</span><span class="sxs-lookup"><span data-stu-id="5e38e-111">Step 1: Create a Text Layout</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="5e38e-112">Шаг 2. Реализация пользовательского класса эффектов рисования</span><span class="sxs-lookup"><span data-stu-id="5e38e-112">Step 2: Implement a Custom Drawing Effect Class</span></span>](#step-2-implement-a-custom-drawing-effect-class)
-   [<span data-ttu-id="5e38e-113">Шаг 3. Реализация пользовательского класса модуля подготовки текста</span><span class="sxs-lookup"><span data-stu-id="5e38e-113">Step 3: Implement a Custom Text Renderer Class</span></span>](#step-3-implement-a-custom-text-renderer-class)
    -   [<span data-ttu-id="5e38e-114">Конструктор</span><span class="sxs-lookup"><span data-stu-id="5e38e-114">The Constructor</span></span>](#the-constructor)
    -   [<span data-ttu-id="5e38e-115">Метод DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="5e38e-115">The DrawGlyphRun Method</span></span>](#the-drawglyphrun-method)
    -   [<span data-ttu-id="5e38e-116">Деструктор</span><span class="sxs-lookup"><span data-stu-id="5e38e-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="5e38e-117">Шаг 4. Создание модуля подготовки текста</span><span class="sxs-lookup"><span data-stu-id="5e38e-117">Step 4: Create the Text Renderer</span></span>](#step-4-create-the-text-renderer)
-   [<span data-ttu-id="5e38e-118">Шаг 5. Создание экземпляра объектов эффектов рисования цветов</span><span class="sxs-lookup"><span data-stu-id="5e38e-118">Step 5: Instantiate the Color Drawing Effect Objects</span></span>](#step-5-instantiate-the-color-drawing-effect-objects)
-   [<span data-ttu-id="5e38e-119">Шаг 6. Установка эффектов рисования для конкретных диапазонов текста</span><span class="sxs-lookup"><span data-stu-id="5e38e-119">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [<span data-ttu-id="5e38e-120">Шаг 7. Рисование макета текста с помощью пользовательского модуля подготовки отчетов</span><span class="sxs-lookup"><span data-stu-id="5e38e-120">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [<span data-ttu-id="5e38e-121">Шаг 8. Очистка</span><span class="sxs-lookup"><span data-stu-id="5e38e-121">Step 8: Clean up</span></span>](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="5e38e-122">Шаг 1. Создание макета текста</span><span class="sxs-lookup"><span data-stu-id="5e38e-122">Step 1: Create a Text Layout</span></span>

<span data-ttu-id="5e38e-123">Для начала потребуется приложение с объектом [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5e38e-123">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="5e38e-124">Если у вас уже есть приложение, отображающее текст с макетом текста, или вы используете Пользовательский пример кода Дравинжеффект, перейдите к шагу 2.</span><span class="sxs-lookup"><span data-stu-id="5e38e-124">If you already have an application that displays text with a text layout, or you are using the Custom DrawingEffect Example Code, skip to Step 2.</span></span>

<span data-ttu-id="5e38e-125">Чтобы добавить текстовый макет, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5e38e-125">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="5e38e-126">Объявите указатель на интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) в качестве члена класса.</span><span class="sxs-lookup"><span data-stu-id="5e38e-126">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="5e38e-127">В конце метода **креатедевицеиндепендентресаурцес** создайте объект интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , вызвав метод [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5e38e-127">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="5e38e-128">Наконец, не забудьте освободить текстовый макет в деструкторе.</span><span class="sxs-lookup"><span data-stu-id="5e38e-128">Finally, remember to release the text layout in the destructor.</span></span>
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a><span data-ttu-id="5e38e-129">Шаг 2. Реализация пользовательского класса эффектов рисования</span><span class="sxs-lookup"><span data-stu-id="5e38e-129">Step 2: Implement a Custom Drawing Effect Class</span></span>

<span data-ttu-id="5e38e-130">В отличие от методов, унаследованных от IUnknown, Пользовательский интерфейс эффектов рисования клиента не имеет никаких требований к методу, который он должен реализовывать.</span><span class="sxs-lookup"><span data-stu-id="5e38e-130">Other than the methods inherited from IUnknown, a custom client drawing effect interface has no requirements as to what it must implement.</span></span> <span data-ttu-id="5e38e-131">В этом случае класс **колордравинжеффект** просто содержит значение [**D2D1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) и объявляет методы для получения и задания этого значения, а также конструктор, который может изначально установить цвет.</span><span class="sxs-lookup"><span data-stu-id="5e38e-131">In this case, the **ColorDrawingEffect** class simply holds a [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value and declares methods to get and set this value, as well as a constructor that can set the color initially.</span></span>

<span data-ttu-id="5e38e-132">После применения эффектов рисования клиента к текстовому диапазону в объекте [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) этот результат передается методу [**Идвритетекстрендерер::D равглифрун**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) любого выполнения глифа, который должен быть визуализирован.</span><span class="sxs-lookup"><span data-stu-id="5e38e-132">After a client drawing effect is applied to a text range in a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, the drawing effect is passed to the [**IDWriteTextRenderer::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of any glyph run that is to be rendered.</span></span> <span data-ttu-id="5e38e-133">После этого методы рисования становятся доступными для модуля подготовки текста.</span><span class="sxs-lookup"><span data-stu-id="5e38e-133">The methods of the drawing effect are then available to the text renderer.</span></span>

<span data-ttu-id="5e38e-134">Результат рисования клиента может быть настолько сложным, насколько вы хотите сделать, составлять больше информации, чем в этом примере, а также предоставлять методы для изменения глифов, создания объектов, используемых для рисования, и т. д.</span><span class="sxs-lookup"><span data-stu-id="5e38e-134">A client drawing effect can be as complex as you want to make it, carrying more information than in this example, as well as providing methods to alter glyphs, create objects to be used for drawing, and so on.</span></span>

## <a name="step-3-implement-a-custom-text-renderer-class"></a><span data-ttu-id="5e38e-135">Шаг 3. Реализация пользовательского класса модуля подготовки текста</span><span class="sxs-lookup"><span data-stu-id="5e38e-135">Step 3: Implement a Custom Text Renderer Class</span></span>

<span data-ttu-id="5e38e-136">Чтобы воспользоваться преимуществами рисования клиента, необходимо реализовать пользовательский модуль подготовки текста.</span><span class="sxs-lookup"><span data-stu-id="5e38e-136">In order to take advantage of a client drawing effect, you must implement a custom text renderer.</span></span> <span data-ttu-id="5e38e-137">Этот модуль визуализации текста применяет к рисуемому фрагменту глифа результат рисования, переданный в него методом [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) .</span><span class="sxs-lookup"><span data-stu-id="5e38e-137">This text renderer will apply the drawing effect passed to it by the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method to the glyph run being drawn.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="5e38e-138">Конструктор</span><span class="sxs-lookup"><span data-stu-id="5e38e-138">The Constructor</span></span>

<span data-ttu-id="5e38e-139">Конструктор пользовательского текстового модуля подготовки отчетов сохраняет объект [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , который будет использоваться для создания объектов [Direct2D](../direct2d/direct2d-portal.md) , и целевой объект отрисовки Direct2D, на который будет нарисован текст.</span><span class="sxs-lookup"><span data-stu-id="5e38e-139">The constructor for the custom text renderer stores the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create [Direct2D](../direct2d/direct2d-portal.md) objects, and the Direct2D render target that the text will be drawn on to.</span></span>


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



### <a name="the-drawglyphrun-method"></a><span data-ttu-id="5e38e-140">Метод DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="5e38e-140">The DrawGlyphRun Method</span></span>

<span data-ttu-id="5e38e-141">Запуск глифа — это набор глифов, имеющих одинаковый формат, включая эффекты рисования клиента.</span><span class="sxs-lookup"><span data-stu-id="5e38e-141">A glyph run is a set of glyphs that share the same format, including the client drawing effect.</span></span> <span data-ttu-id="5e38e-142">Метод [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) осуществляет отрисовку текста для указанного запуска глифа.</span><span class="sxs-lookup"><span data-stu-id="5e38e-142">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method takes care of the text rendering for a specified glyph run.</span></span>

<span data-ttu-id="5e38e-143">Сначала создайте [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) и [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), а затем извлеките структуру запуска глифов с помощью [**идвритефонтфаце:: жетглифрунаутлине**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span><span class="sxs-lookup"><span data-stu-id="5e38e-143">First, create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), and then retrieve the glyph run outline by using [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span></span> <span data-ttu-id="5e38e-144">Затем преобразуйте источник геометрии с помощью метода [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory:: креатетрансформеджеометри**](../direct2d/id2d1factory-createtransformedgeometry.md) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="5e38e-144">Then transform the origin of the geometry by using the [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method, as shown in the following code.</span></span>


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



<span data-ttu-id="5e38e-145">Затем объявите объект сплошной кисти [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5e38e-145">Next, declare a [Direct2D](../direct2d/direct2d-portal.md) solid brush object.</span></span>


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



<span data-ttu-id="5e38e-146">Если параметр *клиентдравинжеффект* имеет значение, отличное от NULL, запросите объект для интерфейса **колордравинжеффект** .</span><span class="sxs-lookup"><span data-stu-id="5e38e-146">If the *clientDrawingEffect* parameter is not NULL, query the object for the **ColorDrawingEffect** interface.</span></span> <span data-ttu-id="5e38e-147">Это будет работать, так как этот класс будет установлен как результат рисования клиента в текстовых диапазонах объекта макета текста.</span><span class="sxs-lookup"><span data-stu-id="5e38e-147">This will work because you will set this class as the client drawing effect on text ranges of the text layout object.</span></span>

<span data-ttu-id="5e38e-148">Получив указатель на интерфейс **колордравинжеффект** , можно получить значение [**D2D1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) , которое он **сохраняет, с помощью метода WebMethod** .</span><span class="sxs-lookup"><span data-stu-id="5e38e-148">Once you have a pointer to the **ColorDrawingEffect** interface, you can retrieve the [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value that it stores using the **GetColor** method.</span></span> <span data-ttu-id="5e38e-149">Затем используйте **D2D1 \_ Color \_ F** , чтобы создать [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) в этом цвете.</span><span class="sxs-lookup"><span data-stu-id="5e38e-149">Then, use the **D2D1\_COLOR\_F** to create a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in that color.</span></span>

<span data-ttu-id="5e38e-150">Если параметр *клиентдравинжеффект* имеет **значение NULL**, просто создайте черный [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="5e38e-150">If the *clientDrawingEffect* parameter is **NULL**, then just create a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


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



<span data-ttu-id="5e38e-151">Наконец, нарисуйте геометрию контура и заполните ее, используя только что созданную цветную кисть.</span><span class="sxs-lookup"><span data-stu-id="5e38e-151">Finally, draw the outline geometry and fill it using the solid color brush that you just created.</span></span>


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



### <a name="the-destructor"></a><span data-ttu-id="5e38e-152">Деструктор</span><span class="sxs-lookup"><span data-stu-id="5e38e-152">The Destructor</span></span>

<span data-ttu-id="5e38e-153">Не забудьте освободить фабрику [Direct2D](../direct2d/direct2d-portal.md) и целевой объект отрисовки в деструкторе.</span><span class="sxs-lookup"><span data-stu-id="5e38e-153">Don't forget to release the [Direct2D](../direct2d/direct2d-portal.md) factory and render target in the destructor.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a><span data-ttu-id="5e38e-154">Шаг 4. Создание модуля подготовки текста</span><span class="sxs-lookup"><span data-stu-id="5e38e-154">Step 4: Create the Text Renderer</span></span>

<span data-ttu-id="5e38e-155">В ресурсах **креатедевицедепендент** создайте пользовательский объект модуля подготовки текста.</span><span class="sxs-lookup"><span data-stu-id="5e38e-155">In the **CreateDeviceDependent** resources, create the custom text renderer object.</span></span> <span data-ttu-id="5e38e-156">Он зависит от устройства, так как использует **ID2D1RenderTarget**, который зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="5e38e-156">It is device dependent because it uses the **ID2D1RenderTarget**, which is itself device dependent.</span></span>


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a><span data-ttu-id="5e38e-157">Шаг 5. Создание экземпляра объектов эффектов рисования цветов</span><span class="sxs-lookup"><span data-stu-id="5e38e-157">Step 5: Instantiate the Color Drawing Effect Objects</span></span>

<span data-ttu-id="5e38e-158">Создавайте объекты **колордравинжеффект** красным, зеленым и синим.</span><span class="sxs-lookup"><span data-stu-id="5e38e-158">Instantiate **ColorDrawingEffect** objects in red, green, and blue.</span></span>


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



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a><span data-ttu-id="5e38e-159">Шаг 6. Установка эффектов рисования для конкретных диапазонов текста</span><span class="sxs-lookup"><span data-stu-id="5e38e-159">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>

<span data-ttu-id="5e38e-160">Установите эффекты рисования для отдельных диапазонов текста с помощью метода [**идвритетекстлайау:: сетдравинжеффект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) и структуры [**\_ текстового \_ диапазона дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) .</span><span class="sxs-lookup"><span data-stu-id="5e38e-160">Set the drawing effect for specific ranges of text by using the [**IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) method and a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) struct.</span></span>


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



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a><span data-ttu-id="5e38e-161">Шаг 7. Рисование макета текста с помощью пользовательского модуля подготовки отчетов</span><span class="sxs-lookup"><span data-stu-id="5e38e-161">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>

<span data-ttu-id="5e38e-162">Необходимо вызвать метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , а не методы [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) или [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5e38e-162">You must call the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method rather than the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) or [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) methods.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a><span data-ttu-id="5e38e-163">Шаг 8. Очистка</span><span class="sxs-lookup"><span data-stu-id="5e38e-163">Step 8: Clean up</span></span>

<span data-ttu-id="5e38e-164">В деструкторе DemoApp отпустите пользовательский модуль подготовки текста.</span><span class="sxs-lookup"><span data-stu-id="5e38e-164">In the DemoApp destructor, release the custom text renderer.</span></span>


```C++
SafeRelease(&pTextRenderer_);
```



<span data-ttu-id="5e38e-165">После этого добавьте код для освобождения классов эффектов рисования клиента.</span><span class="sxs-lookup"><span data-stu-id="5e38e-165">After that, add code to release the client drawing effect classes.</span></span>


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 