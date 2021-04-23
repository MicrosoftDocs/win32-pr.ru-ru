---
title: Как загрузить изображение в эффекты Direct2D с помощью операция filepicker
description: Показывает, как использовать средство выбора хранилища Windows Филеопенпиккер для загрузки изображения в эффекты Direct2D.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- Операция filepicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4346cc0e337374fa41313cb77debf4faca781669
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681646"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a><span data-ttu-id="8e17d-105">Как загрузить изображение в эффекты Direct2D с помощью операция filepicker</span><span class="sxs-lookup"><span data-stu-id="8e17d-105">How to load an image into Direct2D effects using the FilePicker</span></span>

<span data-ttu-id="8e17d-106">Показывает, как использовать [**Windows:: Storage::P иккерс:: филеопенпиккер**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) для загрузки изображения в [эффекты Direct2D](effects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8e17d-106">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="8e17d-107">Если вы хотите позволить пользователю выбрать файл изображения из хранилища в приложении для Магазина Windows, рекомендуется использовать [**филеопенпиккер**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).</span><span class="sxs-lookup"><span data-stu-id="8e17d-107">If you want to let the user select an image file from storage in a Windows Store app, we recommend that you use the [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8e17d-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="8e17d-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8e17d-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="8e17d-109">Technologies</span></span>

-   [<span data-ttu-id="8e17d-110">Direct2D</span><span class="sxs-lookup"><span data-stu-id="8e17d-110">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="8e17d-111">Эффекты Direct2D</span><span class="sxs-lookup"><span data-stu-id="8e17d-111">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="8e17d-112">**Windows:: Storage::P иккерс:: Филеопенпиккер**</span><span class="sxs-lookup"><span data-stu-id="8e17d-112">**Windows::Storage::Pickers::FileOpenPicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a><span data-ttu-id="8e17d-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="8e17d-113">Prerequisites</span></span>

-   <span data-ttu-id="8e17d-114">Для создания эффектов необходим объект [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="8e17d-114">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object for creating effects.</span></span>
-   <span data-ttu-id="8e17d-115">Для создания объектов WIC необходим объект [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) .</span><span class="sxs-lookup"><span data-stu-id="8e17d-115">You need an [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) object for creating WIC objects.</span></span>

## <a name="instructions"></a><span data-ttu-id="8e17d-116">Инструкции</span><span class="sxs-lookup"><span data-stu-id="8e17d-116">Instructions</span></span>

### <a name="step-1-open-the-file-picker"></a><span data-ttu-id="8e17d-117">Шаг 1. Открытие средства выбора файлов</span><span class="sxs-lookup"><span data-stu-id="8e17d-117">Step 1: Open the file picker</span></span>

<span data-ttu-id="8e17d-118">Создайте объект [**филеопенпиккер**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) и задайте *ViewMode*, *сугжестедстартлокатион* и *филетипефилтер* для выбора изображений.</span><span class="sxs-lookup"><span data-stu-id="8e17d-118">Create a [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) object and set the *ViewMode*, *SuggestedStartLocation*, and the *FileTypeFilter* for selecting images.</span></span> <span data-ttu-id="8e17d-119">Вызовите метод [**пикксинглефилеасинк**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) .</span><span class="sxs-lookup"><span data-stu-id="8e17d-119">Call the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) method.</span></span>


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



<span data-ttu-id="8e17d-120">После завершения [**пикксинглефилеасинк**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) вы получаете файловый поток из интерфейса [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) , который он возвращает.</span><span class="sxs-lookup"><span data-stu-id="8e17d-120">After the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) completes, you get a file stream from the [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) interface it returns.</span></span>

### <a name="step-2-get-a-file-stream"></a><span data-ttu-id="8e17d-121">Шаг 2. получение файлового потока</span><span class="sxs-lookup"><span data-stu-id="8e17d-121">Step 2: Get a file stream</span></span>

<span data-ttu-id="8e17d-122">Объявите обработчик завершения для запуска после возвращения асинхронной операции выбора файлов.</span><span class="sxs-lookup"><span data-stu-id="8e17d-122">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="8e17d-123">Для получения файла и получения объекта файлового потока используйте метод " [**Results**](/previous-versions//br205815(v=vs.85)) ".</span><span class="sxs-lookup"><span data-stu-id="8e17d-123">Use the [**GetResults**](/previous-versions//br205815(v=vs.85)) method to retrieve the file and to get the file stream object.</span></span>


```C++
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file) // If file == nullptr, the user did not select a file.
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
```



<span data-ttu-id="8e17d-124">На следующем шаге вы преобразуете объект [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) в [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , который можно передать в [WIC](/windows/desktop/wic/-wic-api).</span><span class="sxs-lookup"><span data-stu-id="8e17d-124">In the next step you convert the [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) object to an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) that you can pass to [WIC](/windows/desktop/wic/-wic-api).</span></span>

### <a name="step-3-convert-the-file-stream"></a><span data-ttu-id="8e17d-125">Шаг 3. Преобразование файлового потока</span><span class="sxs-lookup"><span data-stu-id="8e17d-125">Step 3: Convert the file stream</span></span>

<span data-ttu-id="8e17d-126">Используйте функцию [**креатестреамоверрандомакцессстреам**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) для преобразования файлового потока.</span><span class="sxs-lookup"><span data-stu-id="8e17d-126">Use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function to convert the file stream.</span></span> <span data-ttu-id="8e17d-127">Среда выполнения Windows API представляют потоки с помощью [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), а [WIC](/windows/desktop/wic/-wic-api) использует [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="8e17d-127">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while [WIC](/windows/desktop/wic/-wic-api) consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


```C++
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
        reinterpret_cast<IUnknown*>(fileStream),
        IID_PPV_ARGS(&istream)
        )
    );
```



> [!Note]  
> <span data-ttu-id="8e17d-128">Чтобы использовать функцию [**креатестреамоверрандомакцессстреам**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , в проекте необходимо включить *шкоре. h* .</span><span class="sxs-lookup"><span data-stu-id="8e17d-128">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include *shcore.h* in your project.</span></span>

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a><span data-ttu-id="8e17d-129">Шаг 4. создание декодера WIC и получение рамки</span><span class="sxs-lookup"><span data-stu-id="8e17d-129">Step 4: Create a WIC decoder and get the frame</span></span>

<span data-ttu-id="8e17d-130">Создайте объект [**ивикбитмапдекодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) с помощью метода [**IWICImagingFactory:: креатедекодерфромстреам**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="8e17d-130">Create an [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) object using the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>


```C++
    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );
```



<span data-ttu-id="8e17d-131">Получите первый кадр изображения из декодера с помощью метода [**ивикбитмапдекодер:: noframes**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .</span><span class="sxs-lookup"><span data-stu-id="8e17d-131">Get the first frame of the image from the decoder using the [**IWICBitmapDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a><span data-ttu-id="8e17d-132">Шаг 5. создание преобразователя WIC и инициализация</span><span class="sxs-lookup"><span data-stu-id="8e17d-132">Step 5: Create a WIC converter and initialize</span></span>

<span data-ttu-id="8e17d-133">Преобразование изображения в формат цвета BGRA с помощью [WIC](/windows/desktop/wic/-wic-api).</span><span class="sxs-lookup"><span data-stu-id="8e17d-133">Convert the image to the BGRA color format using [WIC](/windows/desktop/wic/-wic-api).</span></span> <span data-ttu-id="8e17d-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) вернет собственный формат пикселей изображения, например, JPEG ХРАНИТСЯ в GUID \_ WICPixelFormat24bppBGR.</span><span class="sxs-lookup"><span data-stu-id="8e17d-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) will return the native pixel format of the image, like JPEGs are stored in GUID\_WICPixelFormat24bppBGR.</span></span> <span data-ttu-id="8e17d-135">Однако в целях оптимизации производительности с помощью Direct2D рекомендуется преобразовать в WICPixelFormat32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="8e17d-135">However, as a performance optimization with Direct2D we recommend that you convert to WICPixelFormat32bppPBGRA.</span></span>

1.  <span data-ttu-id="8e17d-136">Создайте объект [**ивикформатконвертер**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) с помощью метода [**IWICImagingFactory:: креатеформатконвертер**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="8e17d-136">Create a [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) object using the [**IWICImagingFactory::CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  <span data-ttu-id="8e17d-137">Инициализируйте преобразователь формата, чтобы использовать WICPixelFormat32bppPBGRA и передать кадр растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="8e17d-137">Initialize the format converter to use the WICPixelFormat32bppPBGRA and pass in the bitmap frame.</span></span>

    ```C++
       DX::ThrowIfFailed(
            converter->Initialize(
                frame.Get(),
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                nullptr,
                0.0f,
                WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
                )
            );
    ```

    

<span data-ttu-id="8e17d-138">Интерфейс [**ивикформатконвертер**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) является производным от интерфейса [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) , поэтому можно передать преобразователь в [Исходный растровый](bitmap-source.md) результат.</span><span class="sxs-lookup"><span data-stu-id="8e17d-138">The [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) interface is derived from the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) interface, so you can pass the converter to the [bitmap source](bitmap-source.md) effect.</span></span>

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a><span data-ttu-id="8e17d-139">Шаг 6. Создание действия и передача IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="8e17d-139">Step 6: Create effect and pass in an IWICBitmapSource</span></span>

<span data-ttu-id="8e17d-140">Используйте метод [**креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) для создания объекта ID2D1Effect [исходного растрового изображения](bitmap-source.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) с помощью [](getting-started-with-direct2d.md) [**контекста устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e17d-140">Use the [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method to create a [bitmap source](bitmap-source.md) [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object using the [Direct2D](getting-started-with-direct2d.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span>

<span data-ttu-id="8e17d-141">Используйте метод [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) , чтобы установить в *качестве \_ \_ исходного свойства \_ \_ \_ источника для растрового изображения D2D1* перекодировки WIC значение [**преобразователя формата**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) [WIC](/windows/desktop/wic/-wic-api) .</span><span class="sxs-lookup"><span data-stu-id="8e17d-141">Use the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method to set the *D2D1\_BITMAPSOURCE\_PROP\_WIC\_BITMAP\_SOURCE* property to the [WIC](/windows/desktop/wic/-wic-api) [**format converter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter).</span></span>

> [!Note]  
> <span data-ttu-id="8e17d-142">[Исходный эффект растрового изображения](bitmap-source.md) не принимает входные данные из метода [**сетинпут**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) , такого как многие [эффекты Direct2D](effects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8e17d-142">The [bitmap source](bitmap-source.md) effect doesn't take an input from the [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method like many [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="8e17d-143">Вместо этого объект [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) задается как свойство.</span><span class="sxs-lookup"><span data-stu-id="8e17d-143">Instead, the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) object is specified as a property.</span></span>

 


```C++
    ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
```



<span data-ttu-id="8e17d-144">Теперь, когда у вас есть [Исходный растровый](bitmap-source.md) результат, его можно использовать в качестве входных данных для любого [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) и создания диаграммы эффектов.</span><span class="sxs-lookup"><span data-stu-id="8e17d-144">Now that you have the [bitmap source](bitmap-source.md) effect, you can use it as input to any [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) and create an effect graph.</span></span>

## <a name="complete-example"></a><span data-ttu-id="8e17d-145">Полный пример</span><span class="sxs-lookup"><span data-stu-id="8e17d-145">Complete example</span></span>

<span data-ttu-id="8e17d-146">Ниже приведен полный код для этого примера.</span><span class="sxs-lookup"><span data-stu-id="8e17d-146">Here is the full code for this example.</span></span>


```C++
ComPtr<ID2D1Effect> bitmapSourceEffect;

void OpenFilePicker()
{
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
    
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file)
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
}

void OpenFile(Windows::Storage::Streams::IRandomAccessStream^ fileStream)
{
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
            reinterpret_cast<IUnknown*>(fileStream),
            IID_PPV_ARGS(&istream)
            )
        );

    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );

    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );

    ComPtr<IWICFormatConverter> converter;
    DX::ThrowIfFailed(
        m_wicFactory->CreateFormatConverter(&converter)
        );

    DX::ThrowIfFailed(
        converter->Initialize(
            frame.Get(),
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            nullptr,
            0.0f,
            WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
            )
        );

       ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
}
```



 

 