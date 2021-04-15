---
description: В следующем примере показано, как повторно закодировать изображение и его метаданные в новый файл того же формата.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: Повторное кодирование изображения JPEG с помощью метаданных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c023defb760faeab2bc6ea92232fcc916ef15126
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105714075"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a>Повторное кодирование изображения JPEG с помощью метаданных

В следующем примере показано, как повторно закодировать изображение и его метаданные в новый файл того же формата. Кроме того, в этом примере добавляются метаданные для демонстрации выражения с одним элементом, используемого модулем записи запроса.

В этом разделе содержатся следующие подразделы.

-   [Предварительные условия](#prerequisites)
-   [Часть 1. декодирование изображения](#part-1-decode-an-image)
-   [Часть 2. Создание и Инициализация кодировщика изображений](#part-2-create-and-initialize-the-image-encoder)
-   [Часть 3. копирование сведений о декодированном кадре](#part-3-copy-decoded-frame-information)
-   [Часть 4. Копирование метаданных](#part-4-copy-the-metadata)
-   [Часть 5. Добавление дополнительных метаданных](#part-5-add-additional-metadata)
-   [Часть 6. Завершение закодированного изображения](#part-6-finalize-the-encoded-image)
-   [Код примера повторной кодировки JPEG](#jpeg-re-encode-example-code)
-   [См. также](#related-topics)

## <a name="prerequisites"></a>Предварительные условия

Чтобы понять этот раздел, необходимо ознакомиться с системой метаданных компонента Windows Imaging Component (WIC), как описано в статье [Общие сведения о метаданных WIC](-wic-about-metadata.md). Также необходимо ознакомиться с компонентами кодеков WIC, как описано в статье [Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md).

## <a name="part-1-decode-an-image"></a>Часть 1. декодирование изображения

Перед копированием данных или метаданных образа в новый файл изображения необходимо сначала создать декодер для существующего образа, который требуется повторно закодировать. В следующем коде показано, как создать декодер WIC для файла изображения test.jpg.


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



Вызов **креатедекодерфромфиленаме** использовал значение WICDecodeMetadataCacheOnDemand из перечисления [**викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) в качестве четвертого параметра. Это предписывает декодеру кэшировать метаданные, когда требуются метаданные, путем получения читателя запросов или с помощью базового средства чтения метаданных. Использование этого параметра позволяет хранить поток в метаданных, что требуется для быстрой кодировки метаданных и позволяет раскодировать и кодировать изображения JPEG. Кроме того, можно использовать другое значение **викдекодеоптионс** , WICDecodeMetadataCacheOnLoad, которое кэширует внедренные метаданные изображения сразу после загрузки изображения.

## <a name="part-2-create-and-initialize-the-image-encoder"></a>Часть 2. Создание и Инициализация кодировщика изображений

В следующем коде показано создание кодировщика, который будет использоваться для кодирования ранее декодированного образа.


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



Пифилестреам создается и инициализируется потоком файлов WIC для записи в файл образа "test2.jpg". затем Пифилестреам используется для инициализации кодировщика, уведомляя кодировщика, где записывать биты образа после завершения кодирования.

## <a name="part-3-copy-decoded-frame-information"></a>Часть 3. копирование сведений о декодированном кадре

Следующий код копирует каждый кадр изображения в новый кадр кодировщика. Эта копия включает в себя размер, разрешение и формат пикселей; все, что необходимо для создания допустимого кадра.

> [!Note]  
> В изображениях JPEG будет содержаться только один кадр, а цикл ниже не является технически необходимым, но он включен для демонстрации использования нескольких кадров для поддерживаемых форматов.

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



Следующий код выполняет быструю проверку, чтобы определить, совпадают ли форматы исходного и конечного изображений. Это необходимо, так как в части 4 показана операция, которая поддерживается только в том случае, если исходный и конечный форматы совпадают.


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a>Часть 4. Копирование метаданных

> [!Note]  
> Код в этом разделе действителен, только если форматы исходного и конечного изображений совпадают. Невозможно скопировать все метаданные изображения в одной операции при кодировании в другой формат изображения.

 

Для сохранения метаданных при повторном кодировании изображения в тот же формат изображения существуют методы, доступные для копирования всех метаданных в одной операции. Каждая из этих операций соответствует аналогичному шаблону. Каждый из них устанавливает метаданные декодированного кадра непосредственно в новый закодированный кадр. Обратите внимание, что это делается для каждого отдельного кадра изображения.

Предпочтительным методом копирования метаданных является инициализация модуля записи блока нового кадра с помощью модуля чтения блоков декодированного кадра. Этот метод показан в следующем коде.


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



В этом примере вы просто получаете блок Reader и модуль записи блока из исходного фрейма и конечного фрейма соответственно. Затем модуль записи блока инициализируется модулем чтения блока. При этом модуль записи блока инициализируется предварительно заполненными метаданными модуля чтения блока. Дополнительные сведения о дополнительных методах копирования метаданных см. в разделе запись метаданных статьи [Обзор чтения и записи метаданных изображения](-wic-codec-readingwritingmetadata.md).

Опять же, эта операция работает только в том случае, если исходный и конечный образы имеют одинаковый формат. Это обусловлено тем, что различные форматы изображений хранят блоки метаданных в разных местах. Например, файлы формата JPEG и TIFF поддерживают блоки метаданных в формате XMP. В изображениях JPEG блок XMP находится в корневом блоке метаданных, как показано в разделе [Общие сведения о метаданных WIC](-wic-about-metadata.md). Однако в изображении TIFF блок XMP внедряется в корневой блок IFD.

## <a name="part-5-add-additional-metadata"></a>Часть 5. Добавление дополнительных метаданных

В следующем примере показано, как добавить метаданные в целевой образ. Это делается путем вызова метода **сетметадатабинаме** модуля записи запроса с помощью выражения запроса и данных, хранящихся в [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



Дополнительные сведения о выражении запроса см. в разделе [Общие сведения о языке запросов метаданных](-wic-codec-metadataquerylanguage.md).

## <a name="part-6-finalize-the-encoded-image"></a>Часть 6. Завершение закодированного изображения

Завершающим этапом копирования образа является запись пиксельных данных для кадра, фиксация кадра в кодировщике и фиксация кодировщика. При фиксации кодировщика в файл записывается поток изображения.


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



Метод **вритесаурце** фрейма используется для записи данных пикселей для изображения. Обратите внимание, что это делается после того, как были записаны метаданные. Это необходимо, чтобы гарантировать, что метаданные имеют достаточно места в файле изображения. После того как данные в пикселях записаны, кадр записывается в поток с помощью метода **фиксации** кадра. После обработки всех кадров кодировщик (и, таким образом, образ) завершается с помощью метода **commit** кодировщика.

После фиксации кадра необходимо освободить COM-объекты, созданные в цикле.

## <a name="jpeg-re-encode-example-code"></a>Код примера повторной кодировки JPEG

Ниже приведен код из частей с 1 по 6 в одном блоке конвиениент.


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о метаданных компонента WIC](-wic-about-metadata.md)
</dt> <dt>

[Общие сведения о языке запросов метаданных](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Общие сведения о чтении и записи метаданных изображений](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Общие сведения о расширяемости метаданных](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
