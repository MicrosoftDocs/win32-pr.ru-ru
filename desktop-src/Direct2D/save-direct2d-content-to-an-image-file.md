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
# <a name="how-to-save-direct2d-content-to-an-image-file"></a>Сохранение содержимого Direct2D в файл изображения

В этом разделе показано, как использовать [**ивиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) для сохранения содержимого в виде [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) в закодированный файл изображения, например JPEG. При создании приложения для Магазина Windows пользователь может выбрать файл назначения с помощью [**Windows:: Storage::P иккерс:: филесавепиккер**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Direct2D](./direct2d-portal.md)
-   [Эффекты Direct2D](effects-overview.md)
-   [**Windows:: Storage::P иккерс:: Филесавепиккер**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a>Предварительные условия

-   Необходим объект [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) и объект, содержащий [Direct2D](./direct2d-portal.md) содержимое, которое реализует [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) , например [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) или [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).

## <a name="instructions"></a>Инструкции

### <a name="step-1-get-a-destination-file-and-stream"></a>Шаг 1. Получение целевого файла и потока

Если вы хотите разрешить пользователю выбирать файл назначения, можно использовать [**филесавепиккер**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), открыть возвращенный файл и получить [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) для использования с WIC.

Создайте элемент [**Windows:: Storage::P иккерс:: филесавепиккер**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) и задайте его параметры для файлов изображений. Вызовите метод [**пикксавефилеасинк**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) .


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



Объявите обработчик завершения для запуска после возвращения асинхронной операции выбора файлов. Для получения файла и получения объекта файлового потока используйте метод " [**Results**](/windows/desktop/WinRT/iasyncaction-getresults) ".


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



Получите [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) , вызвав [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) в файле и получая результат асинхронной операции.


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



Наконец, используйте метод [**креатестреамоверрандомакцессстреам**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) для преобразования файлового потока. Среда выполнения Windows API представляют потоки с помощью [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), а WIC использует [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> Чтобы использовать функцию [**креатестреамоверрандомакцессстреам**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , в проекте необходимо включить **шкоре. h** .

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a>Шаг 2. получение битовой карты WIC и кодировщика кадров

[Ивикбитмапенкодер](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) и [ивикбитмапфраминкоде](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) предоставляют функции для сохранения данных образов в формате закодированного файла.

Создание и инициализация объектов кодировщика.


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



### <a name="step-3-get-an-iwicimageencoder"></a>Шаг 3. получение ИвиЦимажеенкодер

[**ИвиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) — это новый интерфейс в Windows 8. Его можно создать из [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), который расширяет **IWICImagingFactory** и также является новым для Windows 8.


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



Вызовите [**IWICImagingFactory2:: креатеимажеенкодер**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder). Первый параметр является [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) и должен быть устройством, на котором был создан образ, который вы хотите закодировать — нельзя смешивать образы из разных доменов ресурсов в пределах одного [**ивиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a>Шаг 4. запись содержимого Direct2D с помощью ИвиЦимажеенкодер

[**ИвиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) может записывать изображение [Direct2D](./direct2d-portal.md) в кадр изображения, эскиз кадра или эскиз контейнера. Затем можно использовать [ивикбитмапенкодер](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) и [ивикбитмапфраминкоде](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) для кодирования данных о образах в файл обычным образом.

Запишите изображение [Direct2D](./direct2d-portal.md) в кадр. В этом фрагменте кода мы записываем [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , содержащий растровое содержимое Direct2D. Однако можно предоставить любой интерфейс, реализующий [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).


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
> Параметр [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) должен быть создан на [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) , который был передан в [**IWICImagingFactory2:: креатеимажеенкодер**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).

 

Зафиксируйте ресурсы WIC и Stream, чтобы завершить операцию.


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
> Некоторые реализации [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) не реализуют метод [**commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) и возвращают **E \_ нотимпл**.

 

Теперь у вас есть файл, содержащий образ [Direct2D](./direct2d-portal.md) .

## <a name="complete-example"></a>Полный пример

Здесь приведен полный код для этого примера.

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



 

 