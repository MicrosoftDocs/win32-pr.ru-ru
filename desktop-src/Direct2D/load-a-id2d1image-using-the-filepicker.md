---
title: Как загрузить изображение в эффекты Direct2D с помощью операция filepicker
description: показывает, как использовать Windows филеопенпиккер служба хранилища для загрузки изображения в эффекты Direct2D.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- Операция filepicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bb23faf2b9d50f12219f3b99c07ec835558addc55e67d4843dee049946a60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160535"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a>Как загрузить изображение в эффекты Direct2D с помощью операция filepicker

показывает, как использовать [**Windows:: служба хранилища::P иккерс:: филеопенпиккер**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) для загрузки изображения в [эффекты Direct2D](effects-overview.md). если вы хотите разрешить пользователю выбрать файл изображения из хранилища в приложении Windows Store, рекомендуется использовать [**филеопенпиккер**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Direct2D](./direct2d-portal.md)
-   [Эффекты Direct2D](effects-overview.md)
-   [**Windows:: служба хранилища::P иккерс:: филеопенпиккер**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a>Предварительные требования

-   Для создания эффектов необходим объект [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .
-   Для создания объектов WIC необходим объект [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) .

## <a name="instructions"></a>Инструкции

### <a name="step-1-open-the-file-picker"></a>Шаг 1. Открытие средства выбора файлов

Создайте объект [**филеопенпиккер**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) и задайте *ViewMode*, *сугжестедстартлокатион* и *филетипефилтер* для выбора изображений. Вызовите метод [**пикксинглефилеасинк**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) .


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



После завершения [**пикксинглефилеасинк**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) вы получаете файловый поток из интерфейса [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) , который он возвращает.

### <a name="step-2-get-a-file-stream"></a>Шаг 2. получение файлового потока

Объявите обработчик завершения для запуска после возвращения асинхронной операции выбора файлов. Для получения файла и получения объекта файлового потока используйте метод " [**Results**](/previous-versions//br205815(v=vs.85)) ".


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



На следующем шаге вы преобразуете объект [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) в [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , который можно передать в [WIC](/windows/desktop/wic/-wic-api).

### <a name="step-3-convert-the-file-stream"></a>Шаг 3. Преобразование файлового потока

Используйте функцию [**креатестреамоверрандомакцессстреам**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) для преобразования файлового потока. Windows API среды выполнения представляют потоки с помощью [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), тогда как [WIC](/windows/desktop/wic/-wic-api) использует [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).


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
> Чтобы использовать функцию [**креатестреамоверрандомакцессстреам**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , в проекте необходимо включить *шкоре. h* .

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a>Шаг 4. создание декодера WIC и получение рамки

Создайте объект [**ивикбитмапдекодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) с помощью метода [**IWICImagingFactory:: креатедекодерфромстреам**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .


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



Получите первый кадр изображения из декодера с помощью метода [**ивикбитмапдекодер:: noframes**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a>Шаг 5. создание преобразователя WIC и инициализация

Преобразование изображения в формат цвета BGRA с помощью [WIC](/windows/desktop/wic/-wic-api). [IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) вернет собственный формат пикселей изображения, например, JPEG ХРАНИТСЯ в GUID \_ WICPixelFormat24bppBGR. Однако в целях оптимизации производительности с помощью Direct2D рекомендуется преобразовать в WICPixelFormat32bppPBGRA.

1.  Создайте объект [**ивикформатконвертер**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) с помощью метода [**IWICImagingFactory:: креатеформатконвертер**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  Инициализируйте преобразователь формата, чтобы использовать WICPixelFormat32bppPBGRA и передать кадр растрового изображения.

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

    

Интерфейс [**ивикформатконвертер**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) является производным от интерфейса [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) , поэтому можно передать преобразователь в [Исходный растровый](bitmap-source.md) результат.

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a>Шаг 6. Создание действия и передача IWICBitmapSource

Используйте метод [**креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) для создания объекта ID2D1Effect [исходного растрового изображения](bitmap-source.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) с помощью [](getting-started-with-direct2d.md) [**контекста устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)Direct2D.

Используйте метод [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) , чтобы установить в *качестве \_ \_ исходного свойства \_ \_ \_ источника для растрового изображения D2D1* перекодировки WIC значение [**преобразователя формата**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) [WIC](/windows/desktop/wic/-wic-api) .

> [!Note]  
> [Исходный эффект растрового изображения](bitmap-source.md) не принимает входные данные из метода [**сетинпут**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) , такого как многие [эффекты Direct2D](effects-overview.md). Вместо этого объект [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) задается как свойство.

 


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



Теперь, когда у вас есть [Исходный растровый](bitmap-source.md) результат, его можно использовать в качестве входных данных для любого [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) и создания диаграммы эффектов.

## <a name="complete-example"></a>Полный пример

Ниже приведен полный код для этого примера.


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



 

 