---
title: Применение эффектов к примитивам
description: В этом разделе показано, как применить ряд эффектов к примитивам Direct2D и DirectWrite.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafb171c20c567d1fbd6385d23cc3b2925efc154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413381"
---
# <a name="how-to-apply-effects-to-primitives"></a><span data-ttu-id="97f8a-103">Применение эффектов к примитивам</span><span class="sxs-lookup"><span data-stu-id="97f8a-103">How to Apply Effects to Primitives</span></span>

<span data-ttu-id="97f8a-104">В этом разделе показано, как применить ряд эффектов к примитивам [Direct2D](./direct2d-portal.md) и [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="97f8a-104">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span>

<span data-ttu-id="97f8a-105">[API эффектов Direct2D](effects-overview.md) можно использовать для применения графов эффектов к примитивам, отображаемым [Direct2D](./direct2d-portal.md) в изображении.</span><span class="sxs-lookup"><span data-stu-id="97f8a-105">You can use the [Direct2D effects API](effects-overview.md) to apply effect graphs to primitives rendered by [Direct2D](./direct2d-portal.md) to an image.</span></span> <span data-ttu-id="97f8a-106">В примере ниже два скругленных прямоугольника и текст «Direct2D».</span><span class="sxs-lookup"><span data-stu-id="97f8a-106">The example here has two rounded rectangles and the text "Direct2D".</span></span> <span data-ttu-id="97f8a-107">Используйте Direct2D для рисования прямоугольников и [DirectWrite](direct2d-and-directwrite.md) для отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="97f8a-107">Use Direct2D to draw the rectangles and [DirectWrite](direct2d-and-directwrite.md) to draw the text.</span></span>

![прямоугольники с текстом «Direct2D» в.](images/direct2d-rounded.png)

<span data-ttu-id="97f8a-109">Используя [эффекты Direct2D](effects-overview.md), можно сделать этот образ похожим на следующее изображение.</span><span class="sxs-lookup"><span data-stu-id="97f8a-109">Using [Direct2D effects](effects-overview.md), you can make this image look like the next image.</span></span> <span data-ttu-id="97f8a-110">Примените [Размытие по Гауссу](gaussian-blur.md), [поточечное освещение](specular-lighting.md), [арифметические составные](arithmetic-composite.md)и [Составные](composite.md) эффекты к 2D-примитивам, чтобы создать изображение здесь.</span><span class="sxs-lookup"><span data-stu-id="97f8a-110">Apply the [Gaussian Blur](gaussian-blur.md), [Point Specular Lighting](specular-lighting.md), [Arithmetic Composite](arithmetic-composite.md), and [Composite](composite.md) effects to the 2D primitives to create the image here.</span></span>

![прямоугольники с текстом «Direct2D» внутри после применения нескольких эффектов.](images/direct2d-svg.png)

<span data-ttu-id="97f8a-112">После отрисовки прямоугольников и текста на промежуточной поверхности можно использовать его в качестве входных данных для объектов [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) в графе изображения.</span><span class="sxs-lookup"><span data-stu-id="97f8a-112">After you render the rectangles and text to a intermediate surface, you can use this as input for [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects in the image graph.</span></span>

<span data-ttu-id="97f8a-113">В этом примере установите исходное изображение в качестве входных данных для [эффект размытия по Гауссу](gaussian-blur.md) , а затем установите выходные данные размытия в качестве входных данных для [эффектов отраженного освещения точки](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="97f8a-113">In this example, set the original image as the input to the [Gaussian Blur effect](gaussian-blur.md) and then set the output of the blur as the input for the [Point Specular Lighting effect](specular-lighting.md).</span></span> <span data-ttu-id="97f8a-114">Затем результат этого действия совмещен с исходным изображением дважды для получения окончательного изображения, отображаемого в окне.</span><span class="sxs-lookup"><span data-stu-id="97f8a-114">The result of this effect is then composited with the original image twice to get the final image that is rendered to the window.</span></span>

<span data-ttu-id="97f8a-115">Ниже приведена схема графа изображения.</span><span class="sxs-lookup"><span data-stu-id="97f8a-115">Here is a diagram of the image graph.</span></span>

![Диаграмма графа эффектов.](images/effect-graph.png)

<span data-ttu-id="97f8a-117">Эта диаграмма эффектов состоит из четырех объектов [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , каждый из которых представляет отдельный встроенный результат.</span><span class="sxs-lookup"><span data-stu-id="97f8a-117">This effect graph consists of four [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects, each representing a different built-in effect.</span></span> <span data-ttu-id="97f8a-118">Вы можете создавать и подключать пользовательские эффекты таким же образом после их регистрации с помощью [**ID1D1Factory1:: регистереффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span><span class="sxs-lookup"><span data-stu-id="97f8a-118">You can create and connect custom effects in the same way, after you register them using [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span></span> <span data-ttu-id="97f8a-119">Этот код создает эффекты, устанавливает свойства и подключается к показанной выше диаграмме эффектов.</span><span class="sxs-lookup"><span data-stu-id="97f8a-119">The code here creates the effects, sets the properties, and connects the effect graph shown earlier.</span></span>

1.  <span data-ttu-id="97f8a-120">Создайте эффект [размытия по Гауссу](gaussian-blur.md) с помощью метода [**ID2D1DeviceContext:: креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) и укажите правильный идентификатор CLSID.</span><span class="sxs-lookup"><span data-stu-id="97f8a-120">Create the [Gaussian blur](gaussian-blur.md) effect using the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method and specifying the proper CLSID.</span></span> <span data-ttu-id="97f8a-121">Идентификаторы CLSID для встроенных эффектов определяются в d2d1effects. h.</span><span class="sxs-lookup"><span data-stu-id="97f8a-121">The CLSIDs for the built-in effects are defined in d2d1effects.h.</span></span> <span data-ttu-id="97f8a-122">Затем вы устанавливаете стандартное отклонение размытия с помощью метода [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="97f8a-122">You then set the standard deviation of the blur using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Gaussian Blur Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect)
        );

    // Set the blur amount
    DX::ThrowIfFailed(
        gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, sc_gaussianBlurStDev)
        );
    ```

    

    <span data-ttu-id="97f8a-123">Эффект [размытия по Гауссу](gaussian-blur.md) выполняет размытие всех каналов изображения, включая альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="97f8a-123">The [Gaussian blur](gaussian-blur.md) effect blurs all of the channels of the image, including the alpha channel.</span></span>

2.  <span data-ttu-id="97f8a-124">Создайте эффекты [отраженного освещения](point-specular.md) и задайте свойства.</span><span class="sxs-lookup"><span data-stu-id="97f8a-124">Create the [specular lighting](point-specular.md) effect and set the properties.</span></span> <span data-ttu-id="97f8a-125">Положением освещения является вектор из 3 значений с плавающей запятой, поэтому его необходимо объявить как отдельную переменную и передать в метод [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="97f8a-125">The position of the light is a vector of 3 floating point values, so you must declare it as a separate variable and pass it to the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Specular Lighting Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1PointSpecular, &specularLightingEffect)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, sc_specularLightPosition)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, sc_specularExponent)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, sc_specularSurfaceScale)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, sc_specularConstant)
        );
    ```

    

    <span data-ttu-id="97f8a-126">В результате [отраженного освещения](point-specular.md) используется альфа-канал входных данных, чтобы создать карту высоты для освещения.</span><span class="sxs-lookup"><span data-stu-id="97f8a-126">The [specular lighting](point-specular.md) effect uses the alpha channel of the input to create a height map for the lighting.</span></span>

3.  <span data-ttu-id="97f8a-127">Существует два различных составных эффекта, с помощью которых можно использовать [составной](composite.md) эффект и [арифметическое составное](arithmetic-composite.md)действие.</span><span class="sxs-lookup"><span data-stu-id="97f8a-127">There are two different composite effects that you can use the [composite](composite.md) effect and the [arithmetic composite](arithmetic-composite.md).</span></span> <span data-ttu-id="97f8a-128">На этой диаграмме эффектов используются оба.</span><span class="sxs-lookup"><span data-stu-id="97f8a-128">This effect graph uses both.</span></span>

    <span data-ttu-id="97f8a-129">Создайте [составной](composite.md) эффекты и задайте для режима режим D2D1 \_ составного \_ \_ источника \_ в, который выводит пересечение исходного и целевого образов.</span><span class="sxs-lookup"><span data-stu-id="97f8a-129">Create the [composite](composite.md) effect and set the mode to D2D1\_COMPOSITE\_MODE\_SOURCE\_IN, which outputs the intersection of the source and destination images.</span></span>

    <span data-ttu-id="97f8a-130">[Арифметический составной](arithmetic-composite.md) результат объединяет два входных изображения на основе формулы, определенной консорциум W3C (W3C) для стандарта масштабируемой векторной графики (SVG).</span><span class="sxs-lookup"><span data-stu-id="97f8a-130">The [arithmetic composite](arithmetic-composite.md) effect composes the two input images based on a formula defined by the World Wide Web Consortium (W3C) for the Scalable Vector Graphics (SVG) standard.</span></span> <span data-ttu-id="97f8a-131">Создайте арифметическое составное выражение и задайте коэффициенты для формулы.</span><span class="sxs-lookup"><span data-stu-id="97f8a-131">Create arithmetic composite and set the coefficients for the formula.</span></span>

    ```C++
    // Create the Composite Effects
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect)
        );

    DX::ThrowIfFailed(
        compositeEffect->SetValue(D2D1_COMPOSITE_PROP_MODE, D2D1_COMPOSITE_MODE_SOURCE_IN)
        );

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &m_arithmeticCompositeEffect)
        );

    DX::ThrowIfFailed(
        m_arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, sc_arithmeticCoefficients)
        );
    ```

    

    <span data-ttu-id="97f8a-132">Коэффициенты для [арифметических составных](arithmetic-composite.md) эффектов показаны здесь.</span><span class="sxs-lookup"><span data-stu-id="97f8a-132">The coefficients for the [arithmetic composite](arithmetic-composite.md) effect are shown here.</span></span>

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    <span data-ttu-id="97f8a-133">На этой диаграмме эффекта оба составных эффекта принимают выходные данные других эффектов и промежуточную поверхность в качестве входных и их составных.</span><span class="sxs-lookup"><span data-stu-id="97f8a-133">In this effect graph, both of the composite effects take the output of the other effects and the intermediate surface as inputs and composites them.</span></span>

4.  <span data-ttu-id="97f8a-134">Наконец, вы подключаете эффекты для формирования графа, настроив входные значения для правильных изображений и точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="97f8a-134">Finally, you connect the effects to form the graph by setting the inputs to the proper images and bitmaps.</span></span>

    <span data-ttu-id="97f8a-135">Первый эффект [размытия по Гауссу](gaussian-blur.md)получает свои входные данные из промежуточной поверхности, в которую были отображены примитивы.</span><span class="sxs-lookup"><span data-stu-id="97f8a-135">The first effect, [Gaussian blur](gaussian-blur.md), receives its input from the intermediate surface that you rendered the primitives to.</span></span> <span data-ttu-id="97f8a-136">Входные данные задаются с помощью метода [**ID2D1Effect:: сетинпут**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) и задают индекс объекта [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) .</span><span class="sxs-lookup"><span data-stu-id="97f8a-136">You set the input using the [**ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method and specifying the index of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) object.</span></span> <span data-ttu-id="97f8a-137">Эффекты размытия по Гауссу и [отраженного освещения](point-specular.md) имеют только один вход.</span><span class="sxs-lookup"><span data-stu-id="97f8a-137">The Gaussian blur and [specular lighting](point-specular.md) effects have only a single input.</span></span> <span data-ttu-id="97f8a-138">Эффект отраженного освещения использует размытый альфа-канал размытия по Гауссу</span><span class="sxs-lookup"><span data-stu-id="97f8a-138">The specular lighting effect uses the blurred alpha channel of the Gaussian blur</span></span>

    <span data-ttu-id="97f8a-139">[Составные](composite.md) и [арифметические составные](arithmetic-composite.md) эффекты имеют несколько входов.</span><span class="sxs-lookup"><span data-stu-id="97f8a-139">The [composite](composite.md) and [arithmetic composite](arithmetic-composite.md) effects have multiple inputs.</span></span> <span data-ttu-id="97f8a-140">Чтобы убедиться, что изображения помещаются вместе в правильном порядке, необходимо указать правильный индекс для каждого входного изображения.</span><span class="sxs-lookup"><span data-stu-id="97f8a-140">To make sure the images are put together in the right order, you must specify the correct index for each input image.</span></span>

    ```C++
    // Connect the graph.
    // Apply a blur effect to the original image.
    gaussianBlurEffect->SetInput(0, m_inputImage.Get());

    // Apply a specular lighting effect to the result.
    specularLightingEffect->SetInputEffect(0, gaussianBlurEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    compositeEffect->SetInput(0, m_inputImage.Get());
    compositeEffect->SetInputEffect(1, specularLightingEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    m_arithmeticCompositeEffect->SetInput(0, m_inputImage.Get());
    m_arithmeticCompositeEffect->SetInputEffect(1, compositeEffect.Get());
    ```

    

5.  <span data-ttu-id="97f8a-141">Передайте объект [арифметического составного](arithmetic-composite.md) результата в метод [**ID2DDeviceContext::D равимаже**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) , который обрабатывает и рисует выходные данные графа.</span><span class="sxs-lookup"><span data-stu-id="97f8a-141">Pass the [arithmetic composite](arithmetic-composite.md) effect object into the [**ID2DDeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method and it processes and draws the output of the graph.</span></span>

    ```C++
        // Draw the output of the effects graph.
        m_d2dContext->DrawImage(
            m_arithmeticCompositeEffect.Get(),
            D2D1::Point2F(
                (size.width - sc_inputBitmapSize.width) / 2,
                (size.height - sc_inputBitmapSize.height) / 2 + sc_offset
                )
            );
    ```

    

 

 