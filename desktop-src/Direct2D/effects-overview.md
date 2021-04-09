---
title: Эффекты (Direct2D)
description: Обзор Direct2Dных эффектов.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070371"
---
# <a name="effects"></a><span data-ttu-id="7c1e8-103">Произведенный эффект</span><span class="sxs-lookup"><span data-stu-id="7c1e8-103">Effects</span></span>

## <a name="what-are-direct2d-effects"></a><span data-ttu-id="7c1e8-104">Что такое Direct2Dные эффекты?</span><span class="sxs-lookup"><span data-stu-id="7c1e8-104">What are Direct2D effects?</span></span>

<span data-ttu-id="7c1e8-105">Direct2D можно использовать для применения одного или более высококачественных эффектов к изображению или набору изображений.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-105">You can use Direct2D to apply one or more high quality effects to an image or a set of images.</span></span> <span data-ttu-id="7c1e8-106">Интерфейсы API эффектов основаны на [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) и используют возможности GPU для обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-106">The effects APIs are built on [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) and take advantage of GPU features for image processing.</span></span> <span data-ttu-id="7c1e8-107">Можно создать цепочку эффектов на диаграмме эффектов, а также составить или смешать выходные данные эффектов.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-107">You can chain effects in an effect graph and compose or blend the output of effects.</span></span>

<span data-ttu-id="7c1e8-108">Эффект Direct2D выполняет задачу создания образов, например изменение яркости, снятие насыщенности изображения или создание тени.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-108">A Direct2D effect performs an imaging task, like changing brightness, de-saturating an image, or creating a drop shadow.</span></span> <span data-ttu-id="7c1e8-109">Эффекты могут принимать ноль или более входных изображений, предоставлять несколько свойств, управляющих их работой, и создавать одно выходное изображение.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-109">Effects can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="7c1e8-110">Каждый результат создает внутренний граф преобразования, состоящие из отдельных преобразований.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-110">Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="7c1e8-111">Каждое преобразование представляет одну операцию с изображением.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-111">Each transform represents a single image operation.</span></span> <span data-ttu-id="7c1e8-112">Основное назначение преобразования заключается в размещении шейдеров, которые выполняются для каждого выходного пикселя.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-112">The main purpose of a transform is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="7c1e8-113">Эти шейдеры могут включать шейдеры пикселей, шейдеры вершин, стадию смешения GPU и шейдеры вычислений.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-113">These shaders can include pixel shaders, vertex shaders, the blend stage of a GPU, and compute shaders.</span></span>

<span data-ttu-id="7c1e8-114">Как [встроенные эффекты](built-in-effects.md) [Direct2D](./direct2d-portal.md) , так и пользовательские эффекты, которые можно использовать для работы с [API пользовательских эффектов](custom-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1e8-114">Both the [Direct2D](./direct2d-portal.md) [built-in effects](built-in-effects.md) and custom effects you can make using the [custom effects API](custom-effects.md) work this way.</span></span>

<span data-ttu-id="7c1e8-115">Существует ряд [встроенных эффектов](built-in-effects.md) из категорий, таких как здесь.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-115">There are a range of [built-in effects](built-in-effects.md) from categories like the ones here.</span></span> <span data-ttu-id="7c1e8-116">Полный список см. в разделе [встроенные эффекты](built-in-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1e8-116">See the [Built-in Effects](built-in-effects.md) section for a full list.</span></span>

-   [<span data-ttu-id="7c1e8-117">Записей</span><span class="sxs-lookup"><span data-stu-id="7c1e8-117">Filtering</span></span>](built-in-effects.md)
-   [<span data-ttu-id="7c1e8-118">Композиция и смешивание</span><span class="sxs-lookup"><span data-stu-id="7c1e8-118">Composition and Blending</span></span>](built-in-effects.md)
-   [<span data-ttu-id="7c1e8-119">Прозрачность</span><span class="sxs-lookup"><span data-stu-id="7c1e8-119">Transparency</span></span>](built-in-effects.md)
-   [<span data-ttu-id="7c1e8-120">Цвет</span><span class="sxs-lookup"><span data-stu-id="7c1e8-120">Color</span></span>](built-in-effects.md)
-   [<span data-ttu-id="7c1e8-121">Освещение и стилизация</span><span class="sxs-lookup"><span data-stu-id="7c1e8-121">Lighting and Stylizing</span></span>](built-in-effects.md)
-   [<span data-ttu-id="7c1e8-122">Преобразование и масштабирование</span><span class="sxs-lookup"><span data-stu-id="7c1e8-122">Transforming and Scaling</span></span>](built-in-effects.md)
-   [<span data-ttu-id="7c1e8-123">Источники</span><span class="sxs-lookup"><span data-stu-id="7c1e8-123">Sources</span></span>](built-in-effects.md)

<span data-ttu-id="7c1e8-124">Эффекты можно применять к любым растровым изображениям, включая изображения, загруженные [компонентом Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), примитивы, нарисованные [Direct2D](./direct2d-portal.md), Text FROM [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)или сцены, отображаемые [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="7c1e8-124">You can apply effects to any bitmap, including: images loaded by the [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitives drawn by [Direct2D](./direct2d-portal.md), text from [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), or scenes rendered by [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

<span data-ttu-id="7c1e8-125">С помощью эффектов Direct2D можно создавать собственные эффекты, которые можно использовать для приложений.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-125">With Direct2D effects you can write your own effects that you can use for your applications.</span></span> <span data-ttu-id="7c1e8-126">Платформа настраиваемых эффектов позволяет использовать такие возможности GPU, как шейдеры пикселей, шейдер вершин и блок смешения.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-126">A custom effect framework allows you to use GPU features such as pixel shaders, vertex shaders, and the blending unit.</span></span> <span data-ttu-id="7c1e8-127">В пользовательский эффект также можно включить другие встроенные или пользовательские эффекты.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-127">You can also include other built-in or custom effects in your custom effect.</span></span> <span data-ttu-id="7c1e8-128">Платформой для создания пользовательских эффектов является то же, что использовалось для создания встроенных эффектов [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="7c1e8-128">The framework for building custom effects is the same one that was used to create the built-in effects of [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="7c1e8-129">[API Direct2D Effect Author](custom-effects.md) предоставляет набор интерфейсов для создания и регистрации эффектов.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-129">The [Direct2D effect author API](custom-effects.md) provides a set of interfaces to create and register effects.</span></span>

### <a name="more-effects-topics"></a><span data-ttu-id="7c1e8-130">Дополнительные эффекты</span><span class="sxs-lookup"><span data-stu-id="7c1e8-130">More effects topics</span></span>

<span data-ttu-id="7c1e8-131">Оставшаяся часть этого раздела посвящена основам эффектов Direct2D, таких как применение эффекта к изображению.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-131">The rest of this topic explains the basics of Direct2D effects, like applying an effect to an image.</span></span> <span data-ttu-id="7c1e8-132">В таблице ниже приведены ссылки на дополнительные разделы, посвященные влиянию.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-132">The table here has links to additional topics about effects.</span></span>

| <span data-ttu-id="7c1e8-133">Раздел</span><span class="sxs-lookup"><span data-stu-id="7c1e8-133">Topic</span></span>                                                                                                                    | <span data-ttu-id="7c1e8-134">Описание</span><span class="sxs-lookup"><span data-stu-id="7c1e8-134">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c1e8-135">Связывание шейдеров эффектов</span><span class="sxs-lookup"><span data-stu-id="7c1e8-135">Effect Shader Linking</span></span>](effect-shader-linking.md)<br/>                                                            | <span data-ttu-id="7c1e8-136">Direct2D использует оптимизацию, называемую связыванием шейдера эффектов, которая сочетает визуализацию диаграммы с несколькими эффектыми, передавая один проход.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-136">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span><br/>                                               |
| [<span data-ttu-id="7c1e8-137">Пользовательские эффекты</span><span class="sxs-lookup"><span data-stu-id="7c1e8-137">Custom effects</span></span>](custom-effects.md)<br/>                                                                          | <span data-ttu-id="7c1e8-138">Описание процесса написания собственных пользовательских эффектов с помощью стандартных HLSL.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-138">Shows you how to write your own custom effects using standard HLSL.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="7c1e8-139">Как загрузить изображение в эффекты Direct2D с помощью операция filepicker</span><span class="sxs-lookup"><span data-stu-id="7c1e8-139">How to load an image into Direct2D Effects using the FilePicker</span></span>](load-a-id2d1image-using-the-filepicker.md)<br/> | <span data-ttu-id="7c1e8-140">Показывает, как использовать [**Windows:: Storage::P иккерс:: филеопенпиккер**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) для загрузки изображения в эффекты Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-140">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into Direct2D effects.</span></span><br/>                                      |
| [<span data-ttu-id="7c1e8-141">Сохранение содержимого Direct2D в файл изображения</span><span class="sxs-lookup"><span data-stu-id="7c1e8-141">How to save Direct2D content to an image file</span></span>](save-direct2d-content-to-an-image-file.md)<br/>                   | <span data-ttu-id="7c1e8-142">В этом разделе показано, как использовать [**ивиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) для сохранения содержимого в виде [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) в закодированный файл изображения, например JPEG.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-142">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span><br/> |
| [<span data-ttu-id="7c1e8-143">Применение эффектов к примитивам</span><span class="sxs-lookup"><span data-stu-id="7c1e8-143">How to Apply Effects to Primitives</span></span>](how-to-apply-effects-to-primitives.md)<br/>                                  | <span data-ttu-id="7c1e8-144">В этом разделе показано, как применить ряд эффектов к примитивам [Direct2D](./direct2d-portal.md) и [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1e8-144">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span><br/>                           |
| [<span data-ttu-id="7c1e8-145">Управление точностью и числовыми обрезками на диаграммах эффектов</span><span class="sxs-lookup"><span data-stu-id="7c1e8-145">Controlling Precision and Numerical Clipping in Effect Graphs</span></span>](precision-and-clipping-in-effect-graphs.md)<br/>  | <span data-ttu-id="7c1e8-146">Приложения, которые визуализируют эффекты с помощью Direct2D, должны обеспечивать требуемый уровень качества и предсказуемости относительно числовой точности.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-146">Applications that render effects using Direct2D must take care to achieve the desired level of quality and predictability with respect to numerical precision.</span></span> <br/>                    |

## <a name="applying-an-effect-to-an-image"></a><span data-ttu-id="7c1e8-147">Применение эффектов к изображению</span><span class="sxs-lookup"><span data-stu-id="7c1e8-147">Applying an effect to an image</span></span>

<span data-ttu-id="7c1e8-148">Для применения преобразований к изображениям можно использовать API Direct2D Effects.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-148">You can use the Direct2D effects API to apply transforms to images.</span></span>

> [!Note]  
> <span data-ttu-id="7c1e8-149">В этом примере предполагается, что объекты [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) и [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) уже созданы.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-149">This example assumes that you already have [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) objects created.</span></span> <span data-ttu-id="7c1e8-150">Дополнительные сведения о создании этих объектов см. в статье [Загрузка изображения в эффекты Direct2D с помощью операция filepicker](load-a-id2d1image-using-the-filepicker.md) и [устройств и контекстов устройств](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="7c1e8-150">For more information on creating these objects see [How to load an image into Direct2D effects using the FilePicker](load-a-id2d1image-using-the-filepicker.md) and [Devices and Device Contexts](devices-and-device-contexts.md).</span></span>

 

1.  <span data-ttu-id="7c1e8-151">Объявите переменную [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , а затем создайте [Исходный растровый](bitmap-source.md) результат с помощью метода [**ID2DDeviceContext:: креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .</span><span class="sxs-lookup"><span data-stu-id="7c1e8-151">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create a [bitmap source](bitmap-source.md) effect using the [**ID2DDeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method.</span></span>

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  <span data-ttu-id="7c1e8-152">Задайте свойство «Источник битовой карты WIC» с помощью [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span><span class="sxs-lookup"><span data-stu-id="7c1e8-152">Set the BitmapSource property to the WIC bitmap source using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span></span>

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  <span data-ttu-id="7c1e8-153">Объявите переменную [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , а затем создайте эффект [размытия по Гауссу](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1e8-153">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create the [gaussian blur](gaussian-blur.md) effect.</span></span>

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  <span data-ttu-id="7c1e8-154">Задайте входные данные, чтобы получить изображение из исходного результата растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-154">Set the input to receive the image from the bitmap source effect.</span></span> <span data-ttu-id="7c1e8-155">Задайте степень размытия для метода [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) и стандартного свойства отклонения.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-155">Set the blur amount the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method and the standard deviation property.</span></span>

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  <span data-ttu-id="7c1e8-156">Используйте контекст устройства для отрисовки результирующего вывода изображения.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-156">Use the device context to draw the resulting image output.</span></span>

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    <span data-ttu-id="7c1e8-157">Метод [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) должен вызываться между вызовами [**ID2DDeviceContext:: бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) и [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , как и другие операции отрисовки Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-157">The [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method must be called between the [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) calls like other Direct2D render operations.</span></span> <span data-ttu-id="7c1e8-158">**DrawImage** может принимать изображение или выходные данные действия и подготавливать его к целевой поверхности.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-158">**DrawImage** can take an image or the output of an effect and render it to the target surface.</span></span>

## <a name="spatial-transforms"></a><span data-ttu-id="7c1e8-159">Пространственные преобразования</span><span class="sxs-lookup"><span data-stu-id="7c1e8-159">Spatial Transforms</span></span>

<span data-ttu-id="7c1e8-160">Direct2D предоставляет встроенные эффекты, которые могут преобразовывать изображения в 2D-и трехмерном пространстве, а также масштабировать.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-160">Direct2D provides built-in effects that can transform images in 2D and 3D space, as well as scaling.</span></span> <span data-ttu-id="7c1e8-161">Эффекты масштабирования и преобразования предлагают различные уровни качества, например: ближайший соседний, линейный, кубический, многопримерный линейный, анизотропный и высококачественный кубический уровень.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-161">The scale and transform effects offer various quality levels like: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

> [!Note]  
> <span data-ttu-id="7c1e8-162">В режиме анизотропного масштабирования создается MIP-карты при масштабировании, однако если для свойства **кэширования** задано значение true на эффектах, вводимых для преобразования, MIP-карты не будет создаваться каждый раз для достаточно мелких изображений.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-162">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to the transform the mipmaps won't be generated every time for sufficiently small images.</span></span>

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="7c1e8-163">При использовании этого действия 2D-преобразование поворачивает растровое изображение немного против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-163">This use of the 2D affine transform effect rotates the bitmap counterclockwise slightly.</span></span>



| <span data-ttu-id="7c1e8-164">До</span><span class="sxs-lookup"><span data-stu-id="7c1e8-164">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![2D-аффинное действие перед изображением.](images/default-before.jpg)      |
| <span data-ttu-id="7c1e8-166">После</span><span class="sxs-lookup"><span data-stu-id="7c1e8-166">After</span></span>                                                             |
| ![двумерные аффинное эффекты после изображения.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a><span data-ttu-id="7c1e8-168">Совмещение изображений</span><span class="sxs-lookup"><span data-stu-id="7c1e8-168">Compositing images</span></span>

<span data-ttu-id="7c1e8-169">Некоторые эффекты принимают несколько входных данных и объединяют их в один полученный образ.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-169">Some effects accept multiple inputs and composite them into one resulting image.</span></span>

<span data-ttu-id="7c1e8-170">Встроенные составные и арифметические составные эффекты предоставляют различные режимы. Дополнительные сведения см. в [составном](composite.md) разделе.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-170">The built-in composite and arithmetic composite effects provide various modes, for more info see the [composite](composite.md) topic.</span></span> <span data-ttu-id="7c1e8-171">В результате [смешения](blend.md) доступны разнообразные режимы ускорения GPU.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-171">The [blend](blend.md) effect has a variety of GPU accelerated modes available.</span></span>


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="7c1e8-172">Составной результат объединяет изображения разными способами в соответствии с заданным режимом.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-172">The composite effect combines images in various different ways according to the mode you specify.</span></span>

## <a name="pixel-adjustments"></a><span data-ttu-id="7c1e8-173">Корректировки пикселей</span><span class="sxs-lookup"><span data-stu-id="7c1e8-173">Pixel adjustments</span></span>

<span data-ttu-id="7c1e8-174">Существует несколько встроенных эффектов Direct2D, позволяющих изменять данные пикселей.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-174">There are a few built-in Direct2D effects that allow you to alter the pixel data.</span></span> <span data-ttu-id="7c1e8-175">Например, для изменения цвета изображения можно использовать эффекты матрицы цветов.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-175">For example, the color matrix effect can be used to change the color of an image.</span></span>


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="7c1e8-176">Этот код принимает изображение и изменяет цвет, как показано в примерах изображений здесь.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-176">This code takes the image and alters the color as shown in the example images here.</span></span>



| <span data-ttu-id="7c1e8-177">До</span><span class="sxs-lookup"><span data-stu-id="7c1e8-177">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![Матрица цветов перед изображением.](images/default-before.jpg) |
| <span data-ttu-id="7c1e8-179">После</span><span class="sxs-lookup"><span data-stu-id="7c1e8-179">After</span></span>                                                           |
| ![Цветовая матрица после изображения.](images/15-colormatrix.png)  |



 

<span data-ttu-id="7c1e8-181">Дополнительные сведения см. в разделе [встроенные эффекты цвета](how-to-create-a-solid-color-brush.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1e8-181">See the [color built-in effects](how-to-create-a-solid-color-brush.md) section for more info.</span></span>

## <a name="building-effect-graphs"></a><span data-ttu-id="7c1e8-182">Создание графов эффектов</span><span class="sxs-lookup"><span data-stu-id="7c1e8-182">Building effect graphs</span></span>

<span data-ttu-id="7c1e8-183">Вы можете объединить эффекты в цепочки для преобразования изображений.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-183">You can chain effects together to transform images.</span></span> <span data-ttu-id="7c1e8-184">Например, код здесь применяет тень и 2D-преобразование, а затем объединяет результаты вместе.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-184">For example, the code here applies a shadow and a 2D transform, then composites the results together.</span></span>


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="7c1e8-185">Ниже приводится результат.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-185">Here is the result.</span></span>

![выходные данные эффект тени.](images/effect-overview-shadow.png)

<span data-ttu-id="7c1e8-187">Эффекты принимают в качестве входных данных объекты [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) .</span><span class="sxs-lookup"><span data-stu-id="7c1e8-187">Effects take [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) objects as input.</span></span> <span data-ttu-id="7c1e8-188">Можно использовать [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , поскольку интерфейс является производным от **ID2D1Image**.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-188">You can use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) because the interface is derived from **ID2D1Image**.</span></span> <span data-ttu-id="7c1e8-189">Можно также использовать [**ID2D1Effect::**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) GetObject для получения выходных данных объекта [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) в качестве **ID2D1Image** или использовать метод **сетинпутеффект** , который преобразует выходные данные для вас.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-189">You can also use the [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) to get the output of an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object as an **ID2D1Image** or use the **SetInputEffect** method, which converts the output for you.</span></span> <span data-ttu-id="7c1e8-190">В большинстве случаев граф эффектов состоит из объектов **ID2D1Effect** , напрямую связанных друг с другом, что позволяет легко применить к изображению несколько эффектов для создания привлекательных визуальных элементов.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-190">In most cases an effect graph consists of **ID2D1Effect** objects directly chained together, which makes it easy to apply multiple effects to an image to create compelling visuals.</span></span>

<span data-ttu-id="7c1e8-191">Дополнительные сведения см. [в разделе Применение эффектов к примитивам](how-to-apply-effects-to-primitives.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1e8-191">See [How to apply effects to primitives](how-to-apply-effects-to-primitives.md) for more info.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c1e8-192">См. также</span><span class="sxs-lookup"><span data-stu-id="7c1e8-192">Related topics</span></span>

[<span data-ttu-id="7c1e8-193">Пример Direct2D Basic Image Effects</span><span class="sxs-lookup"><span data-stu-id="7c1e8-193">Direct2D basic image effects sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[<span data-ttu-id="7c1e8-194">Встроенные эффекты</span><span class="sxs-lookup"><span data-stu-id="7c1e8-194">Built-in Effects</span></span>](built-in-effects.md)