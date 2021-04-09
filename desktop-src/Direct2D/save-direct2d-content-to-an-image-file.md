---
title: Сохранение содержимого Direct2D в файл изображения
description: В этом разделе показано, как использовать ИвиЦимажеенкодер для сохранения содержимого в виде ID2D1Image в закодированный файл изображения, например JPEG.
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19146d838474046fd634cb5524ddf2367fd1d6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890737"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a><span data-ttu-id="13dfd-103">Сохранение содержимого Direct2D в файл изображения</span><span class="sxs-lookup"><span data-stu-id="13dfd-103">How to save Direct2D content to an image file</span></span>

<span data-ttu-id="13dfd-104">В этом разделе показано, как использовать [**ивиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) для сохранения содержимого в виде [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) в закодированный файл изображения, например JPEG.</span><span class="sxs-lookup"><span data-stu-id="13dfd-104">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span> <span data-ttu-id="13dfd-105">При создании приложения для Магазина Windows пользователь может выбрать файл назначения с помощью [**Windows:: Storage::P иккерс:: филесавепиккер**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span><span class="sxs-lookup"><span data-stu-id="13dfd-105">If you are writing a Windows Store app, you can have the user select a destination file using [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="13dfd-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="13dfd-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="13dfd-107">Технологии</span><span class="sxs-lookup"><span data-stu-id="13dfd-107">Technologies</span></span>

-   [<span data-ttu-id="13dfd-108">Direct2D</span><span class="sxs-lookup"><span data-stu-id="13dfd-108">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="13dfd-109">Эффекты Direct2D</span><span class="sxs-lookup"><span data-stu-id="13dfd-109">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="13dfd-110">**Windows:: Storage::P иккерс:: Филесавепиккер**</span><span class="sxs-lookup"><span data-stu-id="13dfd-110">**Windows::Storage::Pickers::FileSavePicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a><span data-ttu-id="13dfd-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="13dfd-111">Prerequisites</span></span>

-   <span data-ttu-id="13dfd-112">Необходим объект [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) и объект, содержащий [Direct2D](./direct2d-portal.md) содержимое, которое реализует [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) , например [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) или [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span><span class="sxs-lookup"><span data-stu-id="13dfd-112">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object and an object containing [Direct2D](./direct2d-portal.md) content that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) such as [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) or [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span></span>

## <a name="instructions"></a><span data-ttu-id="13dfd-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="13dfd-113">Instructions</span></span>

### <a name="step-1-get-a-destination-file-and-stream"></a><span data-ttu-id="13dfd-114">Шаг 1. Получение целевого файла и потока</span><span class="sxs-lookup"><span data-stu-id="13dfd-114">Step 1: Get a destination file and stream</span></span>

<span data-ttu-id="13dfd-115">Если вы хотите разрешить пользователю выбирать файл назначения, можно использовать [**филесавепиккер**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), открыть возвращенный файл и получить [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) для использования с WIC.</span><span class="sxs-lookup"><span data-stu-id="13dfd-115">If you want to allow the user to select a destination file, you can use [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), open the returned file, and obtain an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) to use with WIC.</span></span>

<span data-ttu-id="13dfd-116">Создайте элемент [**Windows:: Storage::P иккерс:: филесавепиккер**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) и задайте его параметры для файлов изображений.</span><span class="sxs-lookup"><span data-stu-id="13dfd-116">Create a [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) and set its parameters for image files.</span></span> <span data-ttu-id="13dfd-117">Вызовите метод [**пикксавефилеасинк**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) .</span><span class="sxs-lookup"><span data-stu-id="13dfd-117">Call the [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) method.</span></span>


```C++
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    savePicker->DefaultFileExtension = ".jpg";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
```



<span data-ttu-id="13dfd-118">Объявите обработчик завершения для запуска после возвращения асинхронной операции выбора файлов.</span><span class="sxs-lookup"><span data-stu-id="13dfd-118">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="13dfd-119">Для получения файла и получения объекта файлового потока используйте метод " [**Results**](/windows/desktop/WinRT/iasyncaction-getresults) ".</span><span class="sxs-lookup"><span data-stu-id="13dfd-119">Use the [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) method to retrieve the file and to get the file stream object.</span></span>


```C++
    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }
```



<span data-ttu-id="13dfd-120">Получите [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) , вызвав [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) в файле и получая результат асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="13dfd-120">Obtain an [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) by calling [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) on the file and getting the result of the async operation.</span></span>


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



<span data-ttu-id="13dfd-121">Наконец, используйте метод [**креатестреамоверрандомакцессстреам**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) для преобразования файлового потока.</span><span class="sxs-lookup"><span data-stu-id="13dfd-121">Finally, use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) method to convert the file stream.</span></span> <span data-ttu-id="13dfd-122">Среда выполнения Windows API представляют потоки с помощью [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), а WIC использует [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="13dfd-122">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while WIC consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> <span data-ttu-id="13dfd-123">Чтобы использовать функцию [**креатестреамоверрандомакцессстреам**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , в проекте необходимо включить **шкоре. h** .</span><span class="sxs-lookup"><span data-stu-id="13dfd-123">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include **shcore.h** in your project.</span></span>

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a><span data-ttu-id="13dfd-124">Шаг 2. получение битовой карты WIC и кодировщика кадров</span><span class="sxs-lookup"><span data-stu-id="13dfd-124">Step 2: Get the WIC bitmap and frame encoder</span></span>

<span data-ttu-id="13dfd-125">[Ивикбитмапенкодер](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) и [ивикбитмапфраминкоде](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) предоставляют функции для сохранения данных образов в формате закодированного файла.</span><span class="sxs-lookup"><span data-stu-id="13dfd-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) provide the functionality to save imaging data to an encoded file format.</span></span>

<span data-ttu-id="13dfd-126">Создание и инициализация объектов кодировщика.</span><span class="sxs-lookup"><span data-stu-id="13dfd-126">Create and initialize the encoder objects.</span></span>


```C++
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );
```



### <a name="step-3-get-an-iwicimageencoder"></a><span data-ttu-id="13dfd-127">Шаг 3. получение ИвиЦимажеенкодер</span><span class="sxs-lookup"><span data-stu-id="13dfd-127">Step 3: Get an IWICImageEncoder</span></span>

<span data-ttu-id="13dfd-128">[**ИвиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) — это новый интерфейс в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="13dfd-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) is a new interface in Windows 8.</span></span> <span data-ttu-id="13dfd-129">Его можно создать из [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), который расширяет **IWICImagingFactory** и также является новым для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="13dfd-129">It can be created from [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), which extends **IWICImagingFactory** and is also new for Windows 8.</span></span>


```C++
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );
```



<span data-ttu-id="13dfd-130">Вызовите [**IWICImagingFactory2:: креатеимажеенкодер**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="13dfd-130">Call [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span> <span data-ttu-id="13dfd-131">Первый параметр является [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) и должен быть устройством, на котором был создан образ, который вы хотите закодировать — нельзя смешивать образы из разных доменов ресурсов в пределах одного [**ивиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span><span class="sxs-lookup"><span data-stu-id="13dfd-131">The first parameter is an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) and must be the device on which the image you want to encode was created – you cannot mix images from different resource domains within a single [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span></span>


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a><span data-ttu-id="13dfd-132">Шаг 4. запись содержимого Direct2D с помощью ИвиЦимажеенкодер</span><span class="sxs-lookup"><span data-stu-id="13dfd-132">Step 4: Write the Direct2D content using IWICImageEncoder</span></span>

<span data-ttu-id="13dfd-133">[**ИвиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) может записывать изображение [Direct2D](./direct2d-portal.md) в кадр изображения, эскиз кадра или эскиз контейнера.</span><span class="sxs-lookup"><span data-stu-id="13dfd-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) can write a [Direct2D](./direct2d-portal.md) image into an image frame, a frame thumbnail, or the container thumbnail.</span></span> <span data-ttu-id="13dfd-134">Затем можно использовать [ивикбитмапенкодер](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) и [ивикбитмапфраминкоде](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) для кодирования данных о образах в файл обычным образом.</span><span class="sxs-lookup"><span data-stu-id="13dfd-134">You can then use [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) to encode the imaging data to a file as normal.</span></span>

<span data-ttu-id="13dfd-135">Запишите изображение [Direct2D](./direct2d-portal.md) в кадр.</span><span class="sxs-lookup"><span data-stu-id="13dfd-135">Write the [Direct2D](./direct2d-portal.md) image to the frame.</span></span> <span data-ttu-id="13dfd-136">В этом фрагменте кода мы записываем [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , содержащий растровое содержимое Direct2D.</span><span class="sxs-lookup"><span data-stu-id="13dfd-136">In this snippet we write an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) that contains rasterized Direct2D content.</span></span> <span data-ttu-id="13dfd-137">Однако можно предоставить любой интерфейс, реализующий [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span><span class="sxs-lookup"><span data-stu-id="13dfd-137">However, you can provide any interface that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span></span>


```C++
    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );
```



> [!Note]  
> <span data-ttu-id="13dfd-138">Параметр [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) должен быть создан на [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) , который был передан в [**IWICImagingFactory2:: креатеимажеенкодер**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="13dfd-138">The [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) parameter must have been created on the [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) that was passed into [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span>

 

<span data-ttu-id="13dfd-139">Зафиксируйте ресурсы WIC и Stream, чтобы завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="13dfd-139">Commit the WIC and stream resources to finalize the operation.</span></span>


```C++
    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
```



> [!Note]  
> <span data-ttu-id="13dfd-140">Некоторые реализации [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) не реализуют метод [**commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) и возвращают **E \_ нотимпл**.</span><span class="sxs-lookup"><span data-stu-id="13dfd-140">Some implementations of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) do not implement the [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) method and return **E\_NOTIMPL**.</span></span>

 

<span data-ttu-id="13dfd-141">Теперь у вас есть файл, содержащий образ [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="13dfd-141">Now you have a file containing the [Direct2D](./direct2d-portal.md) image.</span></span>

## <a name="complete-example"></a><span data-ttu-id="13dfd-142">Полный пример</span><span class="sxs-lookup"><span data-stu-id="13dfd-142">Complete example</span></span>

<span data-ttu-id="13dfd-143">Здесь приведен полный код для этого примера.</span><span class="sxs-lookup"><span data-stu-id="13dfd-143">Here the full code for this example.</span></span>

```cpp
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );

void SaveAsImageFile::SaveBitmapToFile()
{
    // Prepare a file picker for customers to input image file name.
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto pngExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    auto bmpExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    bmpExtensions->Append(".bmp");
    savePicker->FileTypeChoices->Insert("BMP file", bmpExtensions);
    savePicker->DefaultFileExtension = ".png";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            m_imageFileName = file->Name;
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".bmp")
            {
                wicFormat = GUID_ContainerFormatBmp;
            }
            else if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }

            // Retrieve a stream from the file.
            task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
            createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
                // Convert the RandomAccessStream to an IStream.
                ComPtr<IStream> stream;
                DX::ThrowIfFailed(
                    CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
                    );

                SaveBitmapToStream(m_d2dTargetBitmap, m_wicFactory, m_d2dContext, wicFormat, stream.Get());
            });
        }
    });
}

// Save render target bitmap to a stream using WIC.
void SaveAsImageFile::SaveBitmapToStream(
    _In_ ComPtr<ID2D1Bitmap1> d2dBitmap,
    _In_ ComPtr<IWICImagingFactory2> wicFactory2,
    _In_ ComPtr<ID2D1DeviceContext> d2dContext,
    _In_ REFGUID wicFormat,
    _In_ IStream* stream
    )
{
    // Create and initialize WIC Bitmap Encoder.
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    // Create and initialize WIC Frame Encoder.
    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );

    // Retrieve D2D Device.
    ComPtr<ID2D1Device> d2dDevice;
    d2dContext->GetDevice(&d2dDevice);

    // Create IWICImageEncoder.
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );

    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
}

```



 

 