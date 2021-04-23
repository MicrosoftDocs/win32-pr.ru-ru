---
title: Учебник начало работы с DirectWrite
description: В этом документе показано, как использовать DirectWrite и Direct2D для создания простого текста, содержащего один формат, а затем текст, содержащий несколько форматов.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, учебник
- DirectWrite, руководство по началу работы
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, интерфейс Идвритетекстлайаут
- Интерфейс Идвритетекстлайаут
- DirectWrite, интерфейс Идвритетипографи
- Интерфейс Идвритетипографи
- DirectWrite, интерфейс Идвритетекстформат
- Интерфейс Идвритетекстформат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338444"
---
# <a name="tutorial-getting-started-with-directwrite"></a><span data-ttu-id="85de3-113">Учебник. начало работы с DirectWrite</span><span class="sxs-lookup"><span data-stu-id="85de3-113">Tutorial: Getting Started with DirectWrite</span></span>

<span data-ttu-id="85de3-114">В этом документе показано, как использовать [DirectWrite](direct-write-portal.md) и [Direct2D](rendering-by-using-direct2d.md) для создания простого текста, содержащего один формат, а затем текст, содержащий несколько форматов.</span><span class="sxs-lookup"><span data-stu-id="85de3-114">This document shows you how to use [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to create simple text that contains a single format, and then text that contains multiple formats.</span></span>

<span data-ttu-id="85de3-115">Этот учебник содержит следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="85de3-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="85de3-116">Исходный код</span><span class="sxs-lookup"><span data-stu-id="85de3-116">Source Code</span></span>](#source-code)
-   [<span data-ttu-id="85de3-117">Рисование простого текста</span><span class="sxs-lookup"><span data-stu-id="85de3-117">Drawing Simple Text</span></span>](#drawing-simple-text)
    -   [<span data-ttu-id="85de3-118">Часть 1. объявление ресурсов DirectWrite и Direct2D.</span><span class="sxs-lookup"><span data-stu-id="85de3-118">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>](#part-1-declare-directwrite-and-direct2d-resources)
    -   [<span data-ttu-id="85de3-119">Часть 2. создание независимых ресурсов устройства.</span><span class="sxs-lookup"><span data-stu-id="85de3-119">Part 2: Create Device Independent Resources.</span></span>](#part-2-create-device-independent-resources)
    -   [<span data-ttu-id="85de3-120">Часть 3. Создание ресурсов Device-Dependent.</span><span class="sxs-lookup"><span data-stu-id="85de3-120">Part 3: Create Device-Dependent Resources.</span></span>](#part-3-create-device-dependent-resources)
    -   [<span data-ttu-id="85de3-121">Часть 4. Рисование текста с помощью метода Direct2D DrawText.</span><span class="sxs-lookup"><span data-stu-id="85de3-121">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [<span data-ttu-id="85de3-122">Часть 5. Отрисовка содержимого окна с помощью Direct2D</span><span class="sxs-lookup"><span data-stu-id="85de3-122">Part 5: Render the Window Contents Using Direct2D</span></span>](#part-5-render-the-window-contents-using-direct2d)
-   [<span data-ttu-id="85de3-123">Рисование текста с несколькими форматами.</span><span class="sxs-lookup"><span data-stu-id="85de3-123">Drawing Text with Multiple Formats.</span></span>](#drawing-text-with-multiple-formats)
    -   [<span data-ttu-id="85de3-124">Часть 1. Создание интерфейса Идвритетекстлайаут.</span><span class="sxs-lookup"><span data-stu-id="85de3-124">Part 1: Create an IDWriteTextLayout Interface.</span></span>](#part-1-create-an-idwritetextlayout-interface)
    -   [<span data-ttu-id="85de3-125">Часть 2. Применение форматирования с помощью Идвритетекстлайаут.</span><span class="sxs-lookup"><span data-stu-id="85de3-125">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>](#part-2-applying-formatting-with-idwritetextlayout)
    -   [<span data-ttu-id="85de3-126">Часть 3. Добавление типографских функций с помощью Идвритетипографи.</span><span class="sxs-lookup"><span data-stu-id="85de3-126">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>](#part-3-adding-typographic-features-with-idwritetypography)
    -   [<span data-ttu-id="85de3-127">Часть 4. Рисование текста с помощью метода Direct2D Дравтекстлайаут.</span><span class="sxs-lookup"><span data-stu-id="85de3-127">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a><span data-ttu-id="85de3-128">Исходный код</span><span class="sxs-lookup"><span data-stu-id="85de3-128">Source Code</span></span>

<span data-ttu-id="85de3-129">Исходный код, приведенный в этом обзоре, взят из [примера DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="85de3-129">The source code shown in this overview is taken from the [DirectWrite Hello World sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="85de3-130">Каждая часть реализуется в отдельном классе (Симплетекст и Мултиформаттедтекст) и отображается в отдельном дочернем окне.</span><span class="sxs-lookup"><span data-stu-id="85de3-130">Each part is implemented in a separate class (SimpleText and MultiformattedText) and is displayed in a separate child window.</span></span> <span data-ttu-id="85de3-131">Каждый класс представляет окно Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="85de3-131">Each class represents a Microsoft Win32 window.</span></span> <span data-ttu-id="85de3-132">Помимо метода *WndProc* , каждый класс содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="85de3-132">In addition to the *WndProc* method, each class contains the following methods:</span></span>



| <span data-ttu-id="85de3-133">Функция</span><span class="sxs-lookup"><span data-stu-id="85de3-133">Function</span></span>                              | <span data-ttu-id="85de3-134">Описание</span><span class="sxs-lookup"><span data-stu-id="85de3-134">Description</span></span>                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85de3-135">**CreateDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="85de3-135">**CreateDeviceIndependentResources**</span></span>  | <span data-ttu-id="85de3-136">Создает ресурсы, независимые от устройства, поэтому их можно использовать в любом месте.</span><span class="sxs-lookup"><span data-stu-id="85de3-136">Creates resources that are device independent, so they can be reused anywhere.</span></span>                      |
| <span data-ttu-id="85de3-137">**дискарддевицеиндепендентресаурцес**</span><span class="sxs-lookup"><span data-stu-id="85de3-137">**DiscardDeviceIndependentResources**</span></span> | <span data-ttu-id="85de3-138">Освобождает ресурсы, независимые от устройства, после того, как они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="85de3-138">Releases the device-independent resources after they are no longer needed.</span></span>                          |
| <span data-ttu-id="85de3-139">**CreateDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="85de3-139">**CreateDeviceResources**</span></span>             | <span data-ttu-id="85de3-140">Создает ресурсы, такие как кисти и целевые объекты рендеринга, привязанные к конкретному устройству.</span><span class="sxs-lookup"><span data-stu-id="85de3-140">Creates resources, such as brushes and render targets, that are tied to a particular device.</span></span>        |
| <span data-ttu-id="85de3-141">**дискарддевицересаурцес**</span><span class="sxs-lookup"><span data-stu-id="85de3-141">**DiscardDeviceResources**</span></span>            | <span data-ttu-id="85de3-142">Освобождает ресурсы, зависящие от устройства, после того, как они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="85de3-142">Releases the device-dependent resources after they are no longer needed.</span></span>                            |
| <span data-ttu-id="85de3-143">**DrawD2DContent**</span><span class="sxs-lookup"><span data-stu-id="85de3-143">**DrawD2DContent**</span></span>                    | <span data-ttu-id="85de3-144">Использует [Direct2D](../direct2d/direct2d-portal.md) для отображения на экране.</span><span class="sxs-lookup"><span data-stu-id="85de3-144">Uses [Direct2D](../direct2d/direct2d-portal.md) to render to the screen.</span></span>                              |
| <span data-ttu-id="85de3-145">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="85de3-145">**DrawText**</span></span>                          | <span data-ttu-id="85de3-146">Рисует текстовую строку с помощью [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="85de3-146">Draws the text string by using [Direct2D](../direct2d/direct2d-portal.md).</span></span>                            |
| <span data-ttu-id="85de3-147">**онресизе**</span><span class="sxs-lookup"><span data-stu-id="85de3-147">**OnResize**</span></span>                          | <span data-ttu-id="85de3-148">Изменяет размер целевого объекта отрисовки [Direct2D](../direct2d/direct2d-portal.md) при изменении размера окна.</span><span class="sxs-lookup"><span data-stu-id="85de3-148">Resizes the [Direct2D](../direct2d/direct2d-portal.md) render target when the window size is changed.</span></span> |



 

<span data-ttu-id="85de3-149">Вы можете использовать предоставленный образец или выполнить приведенные ниже инструкции, чтобы добавить [DirectWrite](direct-write-portal.md) и [Direct2D](rendering-by-using-direct2d.md) в собственное приложение Win32.</span><span class="sxs-lookup"><span data-stu-id="85de3-149">You can use the sample provided, or use the instructions that follow to add [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to your own Win32 application.</span></span> <span data-ttu-id="85de3-150">Дополнительные сведения о примере и связанных файлах проекта см. в [примере директвритехелловорлд](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="85de3-150">For more information about the sample and the associated project files, see the [DirectWriteHelloWorld sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="drawing-simple-text"></a><span data-ttu-id="85de3-151">Рисование простого текста</span><span class="sxs-lookup"><span data-stu-id="85de3-151">Drawing Simple Text</span></span>

<span data-ttu-id="85de3-152">В этом разделе показано, как использовать [DirectWrite](direct-write-portal.md) и [Direct2D](../direct2d/direct2d-portal.md) для отрисовки простого текста, имеющего один формат, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="85de3-152">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render simple text that has a single format, as shown in the following screen shot.</span></span>

![снимок экрана "Hello World, использующий DirectWrite!"](images/simplecropped.png)

<span data-ttu-id="85de3-155">Для рисования простого текста на экране необходимо четыре компонента:</span><span class="sxs-lookup"><span data-stu-id="85de3-155">Drawing simple text to the screen requires four components:</span></span>

-   <span data-ttu-id="85de3-156">Строка символов для отображения.</span><span class="sxs-lookup"><span data-stu-id="85de3-156">A character string to render.</span></span>
-   <span data-ttu-id="85de3-157">Экземпляр [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="85de3-157">An instance of [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span>
-   <span data-ttu-id="85de3-158">Размеры области, в которой будет содержаться текст.</span><span class="sxs-lookup"><span data-stu-id="85de3-158">The dimensions of the area to contain the text.</span></span>
-   <span data-ttu-id="85de3-159">Объект, который может визуализировать текст.</span><span class="sxs-lookup"><span data-stu-id="85de3-159">An object that can render the text.</span></span> <span data-ttu-id="85de3-160">В этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="85de3-160">In this tutorial.</span></span> <span data-ttu-id="85de3-161">используется целевой объект рендеринга [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="85de3-161">you use a [Direct2D](../direct2d/direct2d-portal.md) render target.</span></span>

<span data-ttu-id="85de3-162">Интерфейс [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) описывает имя, размер, вес, стиль и растяжение гарнитуры, используемые для форматирования текста, а также сведения о языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="85de3-162">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface describes the font-family name, size, weight, style, and stretch used to format text, and it describes locale information.</span></span> <span data-ttu-id="85de3-163">**Идвритетекстформат** также определяет методы для установки и получения следующих свойств:</span><span class="sxs-lookup"><span data-stu-id="85de3-163">**IDWriteTextFormat** also defines methods for setting and getting the following properties:</span></span>

-   <span data-ttu-id="85de3-164">Межстрочный шаг.</span><span class="sxs-lookup"><span data-stu-id="85de3-164">The line spacing.</span></span>
-   <span data-ttu-id="85de3-165">Выравнивание текста относительно левого и правого краев поля макета.</span><span class="sxs-lookup"><span data-stu-id="85de3-165">The text alignment relative to the left and right edges of the layout box.</span></span>
-   <span data-ttu-id="85de3-166">Выравнивание абзаца относительно верхнего и нижнего края поля макета.</span><span class="sxs-lookup"><span data-stu-id="85de3-166">The paragraph alignment relative to the top and bottom of the layout box.</span></span>
-   <span data-ttu-id="85de3-167">Направление чтения.</span><span class="sxs-lookup"><span data-stu-id="85de3-167">The reading direction.</span></span>
-   <span data-ttu-id="85de3-168">Степень гранулярности обрезки текста для текста, который переполняет поле макета.</span><span class="sxs-lookup"><span data-stu-id="85de3-168">The text trimming granularity for text that overflows the layout box.</span></span>
-   <span data-ttu-id="85de3-169">Позиция приращения вкладки.</span><span class="sxs-lookup"><span data-stu-id="85de3-169">The incremental tab stop.</span></span>
-   <span data-ttu-id="85de3-170">Направление потока абзацев.</span><span class="sxs-lookup"><span data-stu-id="85de3-170">The paragraph flow direction.</span></span>

<span data-ttu-id="85de3-171">Для рисования текста, использующего оба процесса, описанных в этом документе, требуется интерфейс [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="85de3-171">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is required for drawing text that uses both of the processes described in this document .</span></span>

<span data-ttu-id="85de3-172">Прежде чем можно будет создать объект [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) или любой другой объект [DirectWrite](direct-write-portal.md) , необходим экземпляр [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="85de3-172">Before you can create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, or any other [DirectWrite](direct-write-portal.md) object, you need an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) instance.</span></span> <span data-ttu-id="85de3-173">**Идвритефактори** используется для создания экземпляров **идвритетекстформат** и других объектов DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="85de3-173">You use an **IDWriteFactory** to create **IDWriteTextFormat** instances and other DirectWrite objects.</span></span> <span data-ttu-id="85de3-174">Чтобы получить экземпляр фабрики, используйте функцию [**двритекреатефактори**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="85de3-174">To obtain a factory instance, use the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function.</span></span>

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a><span data-ttu-id="85de3-175">Часть 1. объявление ресурсов DirectWrite и Direct2D.</span><span class="sxs-lookup"><span data-stu-id="85de3-175">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>

<span data-ttu-id="85de3-176">В этой части вы объявили объекты, которые будут использоваться позже для создания и отображения текста в качестве частных членов данных класса.</span><span class="sxs-lookup"><span data-stu-id="85de3-176">In this part, you declare the objects that you will use later for creating and displaying text as private data members of your class.</span></span> <span data-ttu-id="85de3-177">Все интерфейсы, функции и типы данных для [DirectWrite](direct-write-portal.md) объявляются в файле заголовка *дврите. h* , а их [Direct2D](../direct2d/direct2d-portal.md) объявляются в *D2D1. h*; Если вы еще не сделали этого, включите эти заголовки в свой проект.</span><span class="sxs-lookup"><span data-stu-id="85de3-177">All of the interfaces, functions, and datatypes for [DirectWrite](direct-write-portal.md) are declared in the *dwrite.h* header file, and those for [Direct2D](../direct2d/direct2d-portal.md) are declared in the *d2d1.h*; if you haven't already done this, include these headers in your project.</span></span>

1.  <span data-ttu-id="85de3-178">В файле заголовка класса (Симплетекст. h) объявите указатели на [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) и [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) интерфейсы как закрытые члены.</span><span class="sxs-lookup"><span data-stu-id="85de3-178">In your class header file (SimpleText.h), declare pointers to [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interfaces as private members.</span></span>
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  <span data-ttu-id="85de3-179">Объявите элементы для хранения текстовой строки для отображения и длины строки.</span><span class="sxs-lookup"><span data-stu-id="85de3-179">Declare members to hold the text string to render and the length of the string.</span></span>
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  <span data-ttu-id="85de3-180">Объявите указатели на интерфейсы [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)и [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) для отрисовки текста с помощью [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="85de3-180">Declare pointers to [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), and [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces for rendering the text with [Direct2D](../direct2d/direct2d-portal.md).</span></span>
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a><span data-ttu-id="85de3-181">Часть 2. создание независимых ресурсов устройства.</span><span class="sxs-lookup"><span data-stu-id="85de3-181">Part 2: Create Device Independent Resources.</span></span>

<span data-ttu-id="85de3-182">[Direct2D](rendering-by-using-direct2d.md) предоставляет два типа ресурсов: ресурсы, зависящие от устройства, и ресурсы, независимые от устройств.</span><span class="sxs-lookup"><span data-stu-id="85de3-182">[Direct2D](rendering-by-using-direct2d.md) provides two types of resources: device-dependent resources and device-independent resources.</span></span> <span data-ttu-id="85de3-183">Ресурсы, зависящие от устройства, связаны с устройством отрисовки и больше не работают, если это устройство удалено.</span><span class="sxs-lookup"><span data-stu-id="85de3-183">Device-dependent resources are associated with a rendering device and no longer function if that device is removed.</span></span> <span data-ttu-id="85de3-184">С другой стороны, независимые от устройства ресурсы могут быть последними в области приложения.</span><span class="sxs-lookup"><span data-stu-id="85de3-184">Device-independent resources, on the other hand, can last for the scope of your application.</span></span>

<span data-ttu-id="85de3-185">Ресурсы [DirectWrite](direct-write-portal.md) не зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="85de3-185">[DirectWrite](direct-write-portal.md) resources are device-independent.</span></span>

<span data-ttu-id="85de3-186">В этом разделе вы создадите независимые от устройства ресурсы, используемые приложением.</span><span class="sxs-lookup"><span data-stu-id="85de3-186">In this section, you create the device-independent resources that are used by your application.</span></span> <span data-ttu-id="85de3-187">Эти ресурсы должны быть освобождены с помощью вызова метода **Release** интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85de3-187">These resources must be freed with a call to the **Release** method of the interface.</span></span>

<span data-ttu-id="85de3-188">Некоторые используемые ресурсы должны быть созданы только один раз и не привязаны к устройству.</span><span class="sxs-lookup"><span data-stu-id="85de3-188">Some of the resources that are used have to be created only one time and are not tied to a device.</span></span> <span data-ttu-id="85de3-189">Инициализация этих ресурсов помещается в метод *симплетекст:: креатедевицеиндепендентресаурцес* , который вызывается при инициализации класса.</span><span class="sxs-lookup"><span data-stu-id="85de3-189">The initialization for these resources is put in the *SimpleText::CreateDeviceIndependentResources* method, which is called when initializing the class.</span></span>

1.  <span data-ttu-id="85de3-190">В методе *симплетекст:: креатедевицеиндепендентресаурцес* в файле реализации класса (симплетекст. cpp) вызовите функцию [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) , чтобы создать интерфейс [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , который является корневым интерфейсом фабрики для всех объектов [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="85de3-190">Inside the *SimpleText::CreateDeviceIndependentResources* method in the class implementation file (SimpleText.cpp), call the [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) function to create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface, which is the root factory interface for all [Direct2D](../direct2d/direct2d-portal.md) objects.</span></span> <span data-ttu-id="85de3-191">Вы используете ту же фабрику для создания экземпляров других ресурсов Direct2D.</span><span class="sxs-lookup"><span data-stu-id="85de3-191">You use the same factory to instantiate other Direct2D resources.</span></span>
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  <span data-ttu-id="85de3-192">Вызовите функцию [**двритекреатефактори**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) , чтобы создать интерфейс [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , который является корневым интерфейсом фабрики для всех объектов [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="85de3-192">Call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function to create an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface, which is the root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span> <span data-ttu-id="85de3-193">Вы используете ту же фабрику для создания экземпляров других ресурсов DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="85de3-193">You use the same factory to instantiate other DirectWrite resources.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  <span data-ttu-id="85de3-194">Инициализируйте текстовую строку и сохраняет ее длину.</span><span class="sxs-lookup"><span data-stu-id="85de3-194">Initialize the text string and store its length.</span></span>

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  <span data-ttu-id="85de3-195">Создайте объект интерфейса [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) с помощью метода [**Идвритефактори:: креатетекстформат**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) .</span><span class="sxs-lookup"><span data-stu-id="85de3-195">Create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface object by using the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method.</span></span> <span data-ttu-id="85de3-196">**Идвритетекстформат** задает шрифт, вес, растяжение, стиль и языковой стандарт, которые будут использоваться для отрисовки текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="85de3-196">The **IDWriteTextFormat** specifies the font, weight, stretch, style, and locale that will be used to render the text string.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  <span data-ttu-id="85de3-197">Центрирование текста по горизонтали и вертикали путем вызова методов [**идвритетекстформат:: сеттексталигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) и [**Идвритетекстформат:: сетпараграфалигнмент**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) .</span><span class="sxs-lookup"><span data-stu-id="85de3-197">Center the text horizontally and vertically by calling the [**IDWriteTextFormat::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) and [**IDWriteTextFormat::SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) methods.</span></span>
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

<span data-ttu-id="85de3-198">В этой части были инициализированы независимые от устройства ресурсы, используемые приложением.</span><span class="sxs-lookup"><span data-stu-id="85de3-198">In this part, you initialized the device-independent resources that are used by your application.</span></span> <span data-ttu-id="85de3-199">В следующей части вы инициализируем ресурсы, зависящие от устройства.</span><span class="sxs-lookup"><span data-stu-id="85de3-199">In the next part, you initialize the device-dependent resources.</span></span>

### <a name="part-3-create-device-dependent-resources"></a><span data-ttu-id="85de3-200">Часть 3. Создание ресурсов Device-Dependent.</span><span class="sxs-lookup"><span data-stu-id="85de3-200">Part 3: Create Device-Dependent Resources.</span></span>

<span data-ttu-id="85de3-201">В этой части вы создадите [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) и [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) для отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="85de3-201">In this part, you create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) for rendering your text.</span></span>

<span data-ttu-id="85de3-202">Цель отрисовки — это объект Direct2D, который создает ресурсы рисования и визуализирует команды рисования на устройстве отрисовки.</span><span class="sxs-lookup"><span data-stu-id="85de3-202">A render target is a Direct2D object that creates drawing resources and renders drawing commands to a rendering device.</span></span> <span data-ttu-id="85de3-203">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) — это целевой объект отрисовки, который готовится к просмотру в **HWND**.</span><span class="sxs-lookup"><span data-stu-id="85de3-203">An [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) is a render target that renders to an **HWND**.</span></span>

<span data-ttu-id="85de3-204">Одним из ресурсов рисования, которые может создать целевой объект рендеринга, является кисть для рисования контуров, заливок и текста.</span><span class="sxs-lookup"><span data-stu-id="85de3-204">One of the drawing resources that a render target can create is a brush for painting outlines, fills, and text.</span></span> <span data-ttu-id="85de3-205">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) закрашивается сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="85de3-205">An [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints with a solid color.</span></span>

<span data-ttu-id="85de3-206">Интерфейсы [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) и [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) привязываются к устройству отрисовки, когда они создаются и должны быть освобождены и созданы повторно, если устройство станет недействительным.</span><span class="sxs-lookup"><span data-stu-id="85de3-206">Both the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces are bound to a rendering device when they are created and must be released and recreated if the device becomes invalid.</span></span>

1.  <span data-ttu-id="85de3-207">В методе Симплетекст:: Креатедевицересаурцес проверьте, имеет ли указатель целевого объекта прорисовки **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="85de3-207">Inside the SimpleText::CreateDeviceResources method, check whether the render target pointer is **NULL**.</span></span> <span data-ttu-id="85de3-208">Если это так, извлеките размер области рендеринга и создайте [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) этого размера.</span><span class="sxs-lookup"><span data-stu-id="85de3-208">If it is, retrieve the size of the render area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of that size.</span></span> <span data-ttu-id="85de3-209">Используйте **ID2D1HwndRenderTarget** для создания [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="85de3-209">Use the **ID2D1HwndRenderTarget** to create an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  <span data-ttu-id="85de3-210">В методе Симплетекст::D Искарддевицересаурцес Освободите и кисть, и целевой объект прорисовки.</span><span class="sxs-lookup"><span data-stu-id="85de3-210">In the SimpleText::DiscardDeviceResources method, release both the brush and render target.</span></span>
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

<span data-ttu-id="85de3-211">Теперь, когда вы создали целевой объект отрисовки и кисть, их можно использовать для визуализации текста.</span><span class="sxs-lookup"><span data-stu-id="85de3-211">Now that you have created a render target and a brush, you can use them to render your text.</span></span>

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a><span data-ttu-id="85de3-212">Часть 4. Рисование текста с помощью метода Direct2D DrawText.</span><span class="sxs-lookup"><span data-stu-id="85de3-212">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>

1.  <span data-ttu-id="85de3-213">В методе Симплетекст::D Равтекст класса определите область для макета текста, извлекая размеры области отрисовки и создав прямоугольник [Direct2D](../direct2d/direct2d-portal.md) с теми же размерами.</span><span class="sxs-lookup"><span data-stu-id="85de3-213">In the SimpleText::DrawText method of your class, define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="85de3-214">Используйте метод [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) и объект [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) для отрисовки текста на экране.</span><span class="sxs-lookup"><span data-stu-id="85de3-214">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="85de3-215">Метод **ID2D1RenderTarget::D равтекст** принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="85de3-215">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="85de3-216">Строка для отображения.</span><span class="sxs-lookup"><span data-stu-id="85de3-216">A string to render.</span></span>
    -   <span data-ttu-id="85de3-217">Указатель на интерфейс [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="85de3-217">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="85de3-218">Прямоугольник макета [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="85de3-218">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="85de3-219">Указатель на интерфейс, предоставляющий [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span><span class="sxs-lookup"><span data-stu-id="85de3-219">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a><span data-ttu-id="85de3-220">Часть 5. Отрисовка содержимого окна с помощью Direct2D</span><span class="sxs-lookup"><span data-stu-id="85de3-220">Part 5: Render the Window Contents Using Direct2D</span></span>

<span data-ttu-id="85de3-221">Чтобы отобразить содержимое окна с помощью [Direct2D](../direct2d/direct2d-portal.md) при получении сообщения Paint, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="85de3-221">To render the contents of the window by using [Direct2D](../direct2d/direct2d-portal.md) when a paint message is received, do the following:</span></span>

1.  <span data-ttu-id="85de3-222">Создайте ресурсы, зависимые от устройства, вызвав метод Симплетекст:: Креатедевицересаурцес, реализованный в части 3.</span><span class="sxs-lookup"><span data-stu-id="85de3-222">Create the device dependent resources by calling the SimpleText::CreateDeviceResources method implemented in Part 3.</span></span>
2.  <span data-ttu-id="85de3-223">Вызовите метод [**ID2D1HwndRenderTarget:: бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="85de3-223">Call the [**ID2D1HwndRenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method of the render target.</span></span>
3.  <span data-ttu-id="85de3-224">Очистите целевой объект отрисовки, вызвав метод [**ID2D1HwndRenderTarget:: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) .</span><span class="sxs-lookup"><span data-stu-id="85de3-224">Clear the render target by calling the [**ID2D1HwndRenderTarget::Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) method.</span></span>
4.  <span data-ttu-id="85de3-225">Вызовите метод Симплетекст::D Равтекст, реализованный в части 4.</span><span class="sxs-lookup"><span data-stu-id="85de3-225">Call the SimpleText::DrawText method, implemented in Part 4.</span></span>
5.  <span data-ttu-id="85de3-226">Вызовите метод [**ID2D1HwndRenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="85de3-226">Call the [**ID2D1HwndRenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method of the render target.</span></span>
6.  <span data-ttu-id="85de3-227">При необходимости удалите ресурсы, зависящие от устройства, чтобы их можно было повторно создать при перерисовке окна.</span><span class="sxs-lookup"><span data-stu-id="85de3-227">If it is necessary, discard the device-dependent resources so that they can be recreated when the window is redrawn.</span></span>


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



<span data-ttu-id="85de3-228">Класс Симплетекст реализован в Симплетекст. h и Симплетекст. cpp.</span><span class="sxs-lookup"><span data-stu-id="85de3-228">The SimpleText class is implemented in SimpleText.h and SimpleText.cpp.</span></span>

## <a name="drawing-text-with-multiple-formats"></a><span data-ttu-id="85de3-229">Рисование текста с несколькими форматами.</span><span class="sxs-lookup"><span data-stu-id="85de3-229">Drawing Text with Multiple Formats.</span></span>

<span data-ttu-id="85de3-230">В этом разделе показано, как использовать [DirectWrite](direct-write-portal.md) и [Direct2D](../direct2d/direct2d-portal.md) для отрисовки текста с несколькими форматами, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="85de3-230">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render text with multiple formats, as shown in the following screen shot.</span></span>

![снимок экрана: "Hello World, используя DirectWrite!", с некоторыми частями в различных стилях, размерах и форматах](images/multiformattedcropped.png)

<span data-ttu-id="85de3-232">Код для этого раздела реализуется как класс Мултиформаттедтекст в [примере двритехелловорлд](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="85de3-232">The code for this section is implemented as the MultiformattedText class in the [DWriteHelloWorld Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="85de3-233">Он основан на шагах из предыдущего раздела.</span><span class="sxs-lookup"><span data-stu-id="85de3-233">It is based on the steps from the previous section.</span></span>

<span data-ttu-id="85de3-234">Чтобы создать многострочный текст, в дополнение к интерфейсу [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , представленному в предыдущем разделе, используется интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="85de3-234">To create multi-formatted text, you use the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface in addition to the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface introduced in the previous section.</span></span> <span data-ttu-id="85de3-235">Интерфейс **идвритетекстлайаут** Описывает форматирование и компоновку блока текста.</span><span class="sxs-lookup"><span data-stu-id="85de3-235">The **IDWriteTextLayout** interface describes the formatting and layout of a block of text.</span></span> <span data-ttu-id="85de3-236">В дополнение к форматированию по умолчанию, заданному объектом **идвритетекстформат** , форматирование для отдельных диапазонов текста можно изменить с помощью **идвритетекстлайаут**.</span><span class="sxs-lookup"><span data-stu-id="85de3-236">In addition to default formatting specified by an **IDWriteTextFormat** object, the formatting for specific ranges of text can be changed by using **IDWriteTextLayout**.</span></span> <span data-ttu-id="85de3-237">К ним относятся имя семейства шрифтов, размер, вес, стиль, растяжение, зачеркнутый и подчеркивание.</span><span class="sxs-lookup"><span data-stu-id="85de3-237">This includes font family name, size, weight, style, stretch, strikethrough, and underlining.</span></span>

<span data-ttu-id="85de3-238">[**Идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) также предоставляет методы проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="85de3-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) also provides hit-testing methods.</span></span> <span data-ttu-id="85de3-239">Метрики проверки попадания, возвращаемые этими методами, задаются относительно поля макета, заданного при создании объекта интерфейса **идвритетекстлайаут** с помощью метода [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) интерфейса [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="85de3-239">The hit-testing metrics returned by these methods are relative to the layout box specified when the **IDWriteTextLayout** interface object is created by using the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="85de3-240">Интерфейс [**идвритетипографи**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) используется для добавления дополнительных типографских функций [OpenType](../intl/opentype-font-format.md) в макет текста, таких как каллиграфические символы и альтернативные наборы стилистических текстовых наборов.</span><span class="sxs-lookup"><span data-stu-id="85de3-240">The [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface is used to add optional [OpenType](../intl/opentype-font-format.md) typographic features to a text layout, such as swashes and alternative stylistic text sets.</span></span> <span data-ttu-id="85de3-241">Типографские функции можно добавлять к конкретному фрагменту текста в макете, вызывая метод [**аддфонтфеатуре**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) интерфейса **идвритетипографи** .</span><span class="sxs-lookup"><span data-stu-id="85de3-241">Typographic features can be added to a specific range of text within a text layout by calling the [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method of the **IDWriteTypography** interface.</span></span> <span data-ttu-id="85de3-242">Этот метод получает структуру [**\_ \_ возможностей шрифта дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) в качестве параметра, который содержит константу перечисления **\_ \_ \_ тега функции шрифта дврите** и параметр выполнения **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="85de3-242">This method receives a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) structure as a parameter that contains a **DWRITE\_FONT\_FEATURE\_TAG** enumeration constant and a **UINT32** execution parameter.</span></span> <span data-ttu-id="85de3-243">Список зарегистрированных функций OpenType можно найти в [реестре тегов макета OpenType](https://www.microsoft.com/typography/otspec/features_ae.htm) на Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="85de3-243">A list of registered OpenType features can be found at the [OpenType Layout Tag Registry](https://www.microsoft.com/typography/otspec/features_ae.htm) on microsoft.com.</span></span> <span data-ttu-id="85de3-244">Эквивалентные константы перечисления DirectWrite см. в разделе **\_ \_ \_ тег функции шрифта дврите**.</span><span class="sxs-lookup"><span data-stu-id="85de3-244">For the equivalent DirectWrite enumeration constants, see **DWRITE\_FONT\_FEATURE\_TAG**.</span></span>

### <a name="part-1-create-an-idwritetextlayout-interface"></a><span data-ttu-id="85de3-245">Часть 1. Создание интерфейса Идвритетекстлайаут.</span><span class="sxs-lookup"><span data-stu-id="85de3-245">Part 1: Create an IDWriteTextLayout Interface.</span></span>

1.  <span data-ttu-id="85de3-246">Объявите указатель на интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) в качестве члена класса мултиформаттедтекст.</span><span class="sxs-lookup"><span data-stu-id="85de3-246">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the MultiformattedText class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="85de3-247">В конце метода Мултиформаттедтекст:: Креатедевицеиндепендентресаурцес создайте объект интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , вызвав метод [**креатетекстлайаут**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="85de3-247">At the end of the MultiformattedText::CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span> <span data-ttu-id="85de3-248">Интерфейс **идвритетекстлайаут** предоставляет дополнительные возможности форматирования, такие как возможность применения различных форматов к выбранным фрагментам текста.</span><span class="sxs-lookup"><span data-stu-id="85de3-248">The **IDWriteTextLayout** interface provides additional formatting features, such as the ability to apply different formats to selected portions of text.</span></span>
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

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a><span data-ttu-id="85de3-249">Часть 2. Применение форматирования с помощью Идвритетекстлайаут.</span><span class="sxs-lookup"><span data-stu-id="85de3-249">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>

<span data-ttu-id="85de3-250">Форматирование, например размер шрифта, вес и подчеркивание, можно применить к подстрокам текста, отображаемым с помощью интерфейса [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="85de3-250">Formatting, such as the font size, weight, and underlining, can be applied to substrings of the text to be displayed by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

1.  <span data-ttu-id="85de3-251">Установите размер шрифта для подстроки "Di" из "DirectWrite" в значение 100, объявив [**\_ \_ диапазон текста дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) и вызвав метод [**идвритетекстлайаут:: сетфонтсизе**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) .</span><span class="sxs-lookup"><span data-stu-id="85de3-251">Set the font size for the substring "Di" of "DirectWrite" to 100 by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) and calling the [**IDWriteTextLayout::SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) method.</span></span>
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  <span data-ttu-id="85de3-252">Подчеркивание подстроки "DirectWrite" путем вызова метода [**идвритетекстлайаут:: сетундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) .</span><span class="sxs-lookup"><span data-stu-id="85de3-252">Underline the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  <span data-ttu-id="85de3-253">Установите жирный шрифт для подстроки "DirectWrite", вызвав метод [**идвритетекстлайаут:: сетфонтвеигхт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) .</span><span class="sxs-lookup"><span data-stu-id="85de3-253">Set the font weight to bold for the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) method.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a><span data-ttu-id="85de3-254">Часть 3. Добавление типографских функций с помощью Идвритетипографи.</span><span class="sxs-lookup"><span data-stu-id="85de3-254">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>

1.  <span data-ttu-id="85de3-255">Объявите и создайте объект интерфейса [**идвритетипографи**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) , вызвав метод [**Идвритефактори:: креатетипографи**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) .</span><span class="sxs-lookup"><span data-stu-id="85de3-255">Declare and create an [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface object by calling the [**IDWriteFactory::CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) method.</span></span>
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  <span data-ttu-id="85de3-256">Добавьте функцию шрифта, объявив объект [**\_ \_ функции шрифта дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) с указанным набором стилистических 7 и вызвав метод [**идвритетипографи:: аддфонтфеатуре**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) .</span><span class="sxs-lookup"><span data-stu-id="85de3-256">Add a font feature by declaring a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) object that has the stylistic set 7 specified and calling the [**IDWriteTypography::AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method.</span></span>
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  <span data-ttu-id="85de3-257">Задайте макет текста для использования оформления всей строки путем объявления переменной [**\_ \_ диапазона текста дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) и вызова метода [**идвритетекстлайаут:: сеттипографи**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) и передачи текстового диапазона.</span><span class="sxs-lookup"><span data-stu-id="85de3-257">Set the text layout to use the typography over the whole string by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable and calling the [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) method and passing in the text range.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  <span data-ttu-id="85de3-258">Задайте новую ширину и высоту для объекта макета текста в методе Мултиформаттедтекст:: Онресизе.</span><span class="sxs-lookup"><span data-stu-id="85de3-258">Set the new width and height for the text layout object in the MultiformattedText::OnResize method.</span></span>
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a><span data-ttu-id="85de3-259">Часть 4. Рисование текста с помощью метода Direct2D Дравтекстлайаут.</span><span class="sxs-lookup"><span data-stu-id="85de3-259">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>

<span data-ttu-id="85de3-260">Чтобы нарисовать текст с параметрами макета текста, заданными в объекте [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , измените код в методе мултиформаттедтекст::D равтекст, чтобы использовать [**Идвритетекстлайаут::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span><span class="sxs-lookup"><span data-stu-id="85de3-260">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="85de3-261">Делкаре переменную [**D2D1 \_ \_ 2F**](../direct2d/d2d1-point-2f.md) и установите ее в верхнюю левую точку окна.</span><span class="sxs-lookup"><span data-stu-id="85de3-261">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="85de3-262">Выведите текст на экран, вызвав метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) целевого объекта прорисовки [Direct2D](../direct2d/direct2d-portal.md) и передав указатель [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="85de3-262">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

<span data-ttu-id="85de3-263">Класс Мултиформаттедтекст реализован в Мултиформаттедтекст. h и Мултиформаттедтекст. cpp.</span><span class="sxs-lookup"><span data-stu-id="85de3-263">The MultiformattedText class is implemented in MultiformattedText.h and MultiformattedText.cpp.</span></span>

 

 