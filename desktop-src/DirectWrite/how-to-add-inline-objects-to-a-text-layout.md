---
title: Добавление встроенных объектов в макет текста
description: Содержит краткое руководство по добавлению встроенных объектов в приложение DirectWrite, которое отображает текст с помощью интерфейса Идвритетекстлайаут.
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d9ef34e38ec9b84afd887e565e76efb9618b88
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104556238"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a><span data-ttu-id="36c13-103">Добавление встроенных объектов в макет текста</span><span class="sxs-lookup"><span data-stu-id="36c13-103">How to Add Inline Objects to a Text Layout</span></span>

<span data-ttu-id="36c13-104">Содержит краткое руководство по добавлению встроенных объектов в приложение [DirectWrite](direct-write-portal.md) , которое отображает текст с помощью интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="36c13-104">Provides a short tutorial on adding inline objects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="36c13-105">Конечным продуктом этого учебника является приложение, которое отображает текст со встроенным изображением, которое встроено в него, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="36c13-105">The end product of this tutorial is an application that displays text with an inline image embedded in it, as shown in the following screen shot.</span></span>

![снимок экрана "Пример встроенного объекта" с внедренным изображением](images/inlineobject.png)

<span data-ttu-id="36c13-107">Этот учебник содержит следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="36c13-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="36c13-108">Шаг 1. Создание макета текста.</span><span class="sxs-lookup"><span data-stu-id="36c13-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="36c13-109">Шаг 2. определение класса, производного от интерфейса Идвритеинлинеобжект.</span><span class="sxs-lookup"><span data-stu-id="36c13-109">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [<span data-ttu-id="36c13-110">Шаг 3. Реализация встроенного класса объекта.</span><span class="sxs-lookup"><span data-stu-id="36c13-110">Step 3: Implement the Inline Object Class.</span></span>](#step-3-implement-the-inline-object-class)
    -   [<span data-ttu-id="36c13-111">Конструктор.</span><span class="sxs-lookup"><span data-stu-id="36c13-111">The Constructor.</span></span>](#the-constructor)
    -   [<span data-ttu-id="36c13-112">Метод Draw.</span><span class="sxs-lookup"><span data-stu-id="36c13-112">The Draw Method.</span></span>](#the-draw-method)
    -   [<span data-ttu-id="36c13-113">Методических метрик.</span><span class="sxs-lookup"><span data-stu-id="36c13-113">The GetMetrics Method.</span></span>](#the-getmetrics-method)
    -   [<span data-ttu-id="36c13-114">Метод Жетоверхангметрикс.</span><span class="sxs-lookup"><span data-stu-id="36c13-114">The GetOverhangMetrics Method.</span></span>](#the-getoverhangmetrics-method)
    -   [<span data-ttu-id="36c13-115">Метод Жетбреаккондитионс.</span><span class="sxs-lookup"><span data-stu-id="36c13-115">The GetBreakConditions Method.</span></span>](#the-getbreakconditions-method)
-   [<span data-ttu-id="36c13-116">Шаг 4. Создайте экземпляр класса Инлинеимаже и добавьте его в макет текста.</span><span class="sxs-lookup"><span data-stu-id="36c13-116">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="36c13-117">Шаг 1. Создание макета текста.</span><span class="sxs-lookup"><span data-stu-id="36c13-117">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="36c13-118">Для начала потребуется приложение с объектом [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="36c13-118">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="36c13-119">Если у вас уже есть приложение, отображающее текст с макетом, перейдите к шагу 2.</span><span class="sxs-lookup"><span data-stu-id="36c13-119">If you already have an application that displays text with a text layout, skip to Step 2.</span></span>

<span data-ttu-id="36c13-120">Чтобы добавить текстовый макет, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="36c13-120">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="36c13-121">Объявите указатель на интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) в качестве члена класса.</span><span class="sxs-lookup"><span data-stu-id="36c13-121">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="36c13-122">В конце метода Креатедевицеиндепендентресаурцес создайте объект интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , вызвав метод [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="36c13-122">At the end of the CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="36c13-123">Затем необходимо изменить вызов метода [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) на [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="36c13-123">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), as shown in the following code.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a><span data-ttu-id="36c13-124">Шаг 2. определение класса, производного от интерфейса Идвритеинлинеобжект.</span><span class="sxs-lookup"><span data-stu-id="36c13-124">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>

<span data-ttu-id="36c13-125">Поддержка встроенных объектов в [DirectWrite](direct-write-portal.md) предоставляется интерфейсом [**идвритеинлинеобжект**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) .</span><span class="sxs-lookup"><span data-stu-id="36c13-125">Support for inline objects in [DirectWrite](direct-write-portal.md) is provided by the [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) interface.</span></span> <span data-ttu-id="36c13-126">Чтобы использовать встроенные объекты, необходимо реализовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="36c13-126">To use inline objects, you must implement this interface.</span></span> <span data-ttu-id="36c13-127">Он обрабатывает рисунок встроенного объекта, а также предоставляет для модуля подготовки отчетов метрики и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="36c13-127">It handles the drawing of the inline object, as well as providing metrics and other information to the renderer.</span></span>

<span data-ttu-id="36c13-128">Создайте новый файл заголовка и объявите интерфейс с именем Инлинеимаже, производный от [**идвритеинлинеобжект**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span><span class="sxs-lookup"><span data-stu-id="36c13-128">Create a new header file and declare an interface called InlineImage, derived from [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span></span>

<span data-ttu-id="36c13-129">Помимо QueryInterface, AddRef и Release, унаследованных от IUnknown, этот класс должен иметь следующие методы:</span><span class="sxs-lookup"><span data-stu-id="36c13-129">In addition to QueryInterface, AddRef, and Release inherited from IUnknown, this class must have the following methods:</span></span>

-   [<span data-ttu-id="36c13-130">**Draw**</span><span class="sxs-lookup"><span data-stu-id="36c13-130">**Draw**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [<span data-ttu-id="36c13-131">**Метрики**</span><span class="sxs-lookup"><span data-stu-id="36c13-131">**GetMetrics**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [<span data-ttu-id="36c13-132">**жетоверхангметрикс**</span><span class="sxs-lookup"><span data-stu-id="36c13-132">**GetOverhangMetrics**</span></span>](idwriteinlineobject-getoverhangmetrics.md)
-   [<span data-ttu-id="36c13-133">**жетбреаккондитионс**</span><span class="sxs-lookup"><span data-stu-id="36c13-133">**GetBreakConditions**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a><span data-ttu-id="36c13-134">Шаг 3. Реализация встроенного класса объекта.</span><span class="sxs-lookup"><span data-stu-id="36c13-134">Step 3: Implement the Inline Object Class.</span></span>

<span data-ttu-id="36c13-135">Создайте новый файл C++ с именем Инлинеимаже. cpp для реализации класса.</span><span class="sxs-lookup"><span data-stu-id="36c13-135">Create a new C++ file, named InlineImage.cpp, for the class implementation.</span></span> <span data-ttu-id="36c13-136">В дополнение к методу Лоадбитмапфромфиле и методам, унаследованным от интерфейса IUnknown, класс Инлинеимаже состоит из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="36c13-136">In addition to the LoadBitmapFromFile method and the methods inherited from the IUnknown interface, the InlineImage class is made up of the following methods.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="36c13-137">Конструктор.</span><span class="sxs-lookup"><span data-stu-id="36c13-137">The Constructor.</span></span>


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



<span data-ttu-id="36c13-138">Первым аргументом конструктора является ID2D1RenderTarget, к которому будет отрисовываться встроенное изображение.</span><span class="sxs-lookup"><span data-stu-id="36c13-138">The first argument of the constructor is the ID2D1RenderTarget that the inline image will be rendered to.</span></span> <span data-ttu-id="36c13-139">Он сохраняется для дальнейшего использования при рисовании.</span><span class="sxs-lookup"><span data-stu-id="36c13-139">This is stored for use later when drawing.</span></span>

<span data-ttu-id="36c13-140">Целевой объект отрисовки, IWICImagingFactory и URI имени файла передаются в метод Лоадбитмапфромфиле, который загружает точечный рисунок и сохраняет размер битовой карты (ширину и высоту) в \_ переменной-члене Rect.</span><span class="sxs-lookup"><span data-stu-id="36c13-140">The render target, IWICImagingFactory, and the filename uri are all passed to the LoadBitmapFromFile method that loads the bitmap and stores the bitmap size (width and height) in the rect\_ member variable.</span></span>

### <a name="the-draw-method"></a><span data-ttu-id="36c13-141">Метод Draw.</span><span class="sxs-lookup"><span data-stu-id="36c13-141">The Draw Method.</span></span>

<span data-ttu-id="36c13-142">Метод [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) является обратным вызовом, который вызывается объектом [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) при необходимости прорисовки встроенного объекта.</span><span class="sxs-lookup"><span data-stu-id="36c13-142">The [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) method is a callback that is called by the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) object when the inline object needs to be drawn.</span></span> <span data-ttu-id="36c13-143">Макет текста не вызывает этот метод напрямую.</span><span class="sxs-lookup"><span data-stu-id="36c13-143">The text layout does not call this method directly.</span></span>


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



<span data-ttu-id="36c13-144">В этом случае Рисование растрового изображения выполняется с помощью метода [**ID2D1RenderTarget::D равбитмап**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) . Однако можно использовать любой метод рисования.</span><span class="sxs-lookup"><span data-stu-id="36c13-144">In this case, drawing the bitmap is done by using the [**ID2D1RenderTarget::DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) method; however, any method for drawing can be used.</span></span>

### <a name="the-getmetrics-method"></a><span data-ttu-id="36c13-145">Методических метрик.</span><span class="sxs-lookup"><span data-stu-id="36c13-145">The GetMetrics Method.</span></span>


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



<span data-ttu-id="36c13-146">Для метода [](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) дврите Храните ширину, высоту и базовую базу данных в структуре [**\_ \_ \_ метрики встроенного объекта**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) .</span><span class="sxs-lookup"><span data-stu-id="36c13-146">For the [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) method, store the width, height and baseline in an [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) structure.</span></span> <span data-ttu-id="36c13-147">[**Идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) вызывает эту функцию обратного вызова для получения измерения встроенного объекта.</span><span class="sxs-lookup"><span data-stu-id="36c13-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the measurement of the inline object.</span></span>

### <a name="the-getoverhangmetrics-method"></a><span data-ttu-id="36c13-148">Метод Жетоверхангметрикс.</span><span class="sxs-lookup"><span data-stu-id="36c13-148">The GetOverhangMetrics Method.</span></span>


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



<span data-ttu-id="36c13-149">В этом случае никакой выступ не требуется, поэтому метод [**жетоверхангметрикс**](idwriteinlineobject-getoverhangmetrics.md) возвращает все нули.</span><span class="sxs-lookup"><span data-stu-id="36c13-149">In this case, no overhang is necessary, so the [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) method returns all zeros.</span></span>

### <a name="the-getbreakconditions-method"></a><span data-ttu-id="36c13-150">Метод Жетбреаккондитионс.</span><span class="sxs-lookup"><span data-stu-id="36c13-150">The GetBreakConditions Method.</span></span>


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



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a><span data-ttu-id="36c13-151">Шаг 4. Создайте экземпляр класса Инлинеимаже и добавьте его в макет текста.</span><span class="sxs-lookup"><span data-stu-id="36c13-151">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>

<span data-ttu-id="36c13-152">Наконец, в методе Креатедевицедепендентресаурцес создайте экземпляр класса Инлинеимаже и добавьте его в макет текста.</span><span class="sxs-lookup"><span data-stu-id="36c13-152">Finally, in the CreateDeviceDependentResources method, create an instance of the InlineImage class and add it to the text layout.</span></span> <span data-ttu-id="36c13-153">Так как он содержит ссылку на [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), который является ресурсом, зависимым от устройства, и [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) создается с помощью целевого объекта прорисовки, инлинеимаже также зависит от устройства, и его необходимо создать повторно, если целевой объект прорисовки создан повторно.</span><span class="sxs-lookup"><span data-stu-id="36c13-153">Because it holds a reference to the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), which is a device dependent resource, and the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is created by using the render target, the InlineImage is also device dependent and must be recreated if the render target is recreated.</span></span>


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



<span data-ttu-id="36c13-154">Метод [**идвритетекстлайаут:: сетинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) принимает структуру текстового диапазона.</span><span class="sxs-lookup"><span data-stu-id="36c13-154">The [**IDWriteTextLayout::SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) method takes a text range structure.</span></span> <span data-ttu-id="36c13-155">Объект применяется к указанному здесь диапазону, и любой текст в диапазоне будет подавлен.</span><span class="sxs-lookup"><span data-stu-id="36c13-155">The object applies to the range specified here, and any text in the range will be suppressed.</span></span> <span data-ttu-id="36c13-156">Если длина текстового диапазона равна 0, объект не будет нарисован.</span><span class="sxs-lookup"><span data-stu-id="36c13-156">If the length of the text range is 0, the object will not be drawn.</span></span>

<span data-ttu-id="36c13-157">В этом примере есть звездочка () в \* качестве заполнителя в позиции, где будет отображаться изображение.</span><span class="sxs-lookup"><span data-stu-id="36c13-157">In this example, there is an asterisk (\*) as a place holder in the position where the image will be displayed.</span></span>


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



<span data-ttu-id="36c13-158">Так как класс Инлинеимаже зависит от [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), его необходимо освободить при освобождении целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="36c13-158">Since the InlineImage class is dependent on the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), you must release it when you release the render target.</span></span>


```C++
SafeRelease(&pInlineImage_);
```



 

 