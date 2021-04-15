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
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a><span data-ttu-id="cb787-103">Повторное кодирование изображения JPEG с помощью метаданных</span><span class="sxs-lookup"><span data-stu-id="cb787-103">How-to re-encode a JPEG image with metadata</span></span>

<span data-ttu-id="cb787-104">В следующем примере показано, как повторно закодировать изображение и его метаданные в новый файл того же формата.</span><span class="sxs-lookup"><span data-stu-id="cb787-104">The following example demonstrates how to re-encode an image and its metadata to a new file of the same format.</span></span> <span data-ttu-id="cb787-105">Кроме того, в этом примере добавляются метаданные для демонстрации выражения с одним элементом, используемого модулем записи запроса.</span><span class="sxs-lookup"><span data-stu-id="cb787-105">In addition, this example adds metadata to demonstrate a single-item expression used by a query writer.</span></span>

<span data-ttu-id="cb787-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="cb787-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cb787-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="cb787-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="cb787-108">Часть 1. декодирование изображения</span><span class="sxs-lookup"><span data-stu-id="cb787-108">Part 1: Decode an Image</span></span>](#part-1-decode-an-image)
-   [<span data-ttu-id="cb787-109">Часть 2. Создание и Инициализация кодировщика изображений</span><span class="sxs-lookup"><span data-stu-id="cb787-109">Part 2: Create and Initialize the Image Encoder</span></span>](#part-2-create-and-initialize-the-image-encoder)
-   [<span data-ttu-id="cb787-110">Часть 3. копирование сведений о декодированном кадре</span><span class="sxs-lookup"><span data-stu-id="cb787-110">Part 3: Copy Decoded Frame Information</span></span>](#part-3-copy-decoded-frame-information)
-   [<span data-ttu-id="cb787-111">Часть 4. Копирование метаданных</span><span class="sxs-lookup"><span data-stu-id="cb787-111">Part 4: Copy the Metadata</span></span>](#part-4-copy-the-metadata)
-   [<span data-ttu-id="cb787-112">Часть 5. Добавление дополнительных метаданных</span><span class="sxs-lookup"><span data-stu-id="cb787-112">Part 5: Add Additional Metadata</span></span>](#part-5-add-additional-metadata)
-   [<span data-ttu-id="cb787-113">Часть 6. Завершение закодированного изображения</span><span class="sxs-lookup"><span data-stu-id="cb787-113">Part 6: Finalize the Encoded Image</span></span>](#part-6-finalize-the-encoded-image)
-   [<span data-ttu-id="cb787-114">Код примера повторной кодировки JPEG</span><span class="sxs-lookup"><span data-stu-id="cb787-114">JPEG Re-encode Example Code</span></span>](#jpeg-re-encode-example-code)
-   [<span data-ttu-id="cb787-115">См. также</span><span class="sxs-lookup"><span data-stu-id="cb787-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="cb787-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="cb787-116">Prerequisites</span></span>

<span data-ttu-id="cb787-117">Чтобы понять этот раздел, необходимо ознакомиться с системой метаданных компонента Windows Imaging Component (WIC), как описано в статье [Общие сведения о метаданных WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="cb787-117">To understand this topic, you should be familiar with the Windows Imaging Component (WIC) metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="cb787-118">Также необходимо ознакомиться с компонентами кодеков WIC, как описано в статье [Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="cb787-118">You should also be familiar with the WIC codec components as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="part-1-decode-an-image"></a><span data-ttu-id="cb787-119">Часть 1. декодирование изображения</span><span class="sxs-lookup"><span data-stu-id="cb787-119">Part 1: Decode an Image</span></span>

<span data-ttu-id="cb787-120">Перед копированием данных или метаданных образа в новый файл изображения необходимо сначала создать декодер для существующего образа, который требуется повторно закодировать.</span><span class="sxs-lookup"><span data-stu-id="cb787-120">Before you can copy image data or metadata to a new image file, you must first create a decoder for the existing image that you want to re-encode.</span></span> <span data-ttu-id="cb787-121">В следующем коде показано, как создать декодер WIC для файла изображения test.jpg.</span><span class="sxs-lookup"><span data-stu-id="cb787-121">The following code demonstrates how to create a WIC decoder for the image file test.jpg.</span></span>


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



<span data-ttu-id="cb787-122">Вызов **креатедекодерфромфиленаме** использовал значение WICDecodeMetadataCacheOnDemand из перечисления [**викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) в качестве четвертого параметра.</span><span class="sxs-lookup"><span data-stu-id="cb787-122">The call to **CreateDecoderFromFilename** used the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration as the fourth parameter.</span></span> <span data-ttu-id="cb787-123">Это предписывает декодеру кэшировать метаданные, когда требуются метаданные, путем получения читателя запросов или с помощью базового средства чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="cb787-123">This tells the decoder to cache the metadata when the metadata is needed, either by obtaining a query reader or by using the underlying metadata reader.</span></span> <span data-ttu-id="cb787-124">Использование этого параметра позволяет хранить поток в метаданных, что требуется для быстрой кодировки метаданных и позволяет раскодировать и кодировать изображения JPEG.</span><span class="sxs-lookup"><span data-stu-id="cb787-124">Using this option enables you to retain the stream to the metadata, which is required for performing fast metadata encoding and enables lossless decoding and encoding of JPEG images.</span></span> <span data-ttu-id="cb787-125">Кроме того, можно использовать другое значение **викдекодеоптионс** , WICDecodeMetadataCacheOnLoad, которое кэширует внедренные метаданные изображения сразу после загрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="cb787-125">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

## <a name="part-2-create-and-initialize-the-image-encoder"></a><span data-ttu-id="cb787-126">Часть 2. Создание и Инициализация кодировщика изображений</span><span class="sxs-lookup"><span data-stu-id="cb787-126">Part 2: Create and Initialize the Image Encoder</span></span>

<span data-ttu-id="cb787-127">В следующем коде показано создание кодировщика, который будет использоваться для кодирования ранее декодированного образа.</span><span class="sxs-lookup"><span data-stu-id="cb787-127">The following code demonstrates the creation of the encoder you will use to encode the image you previously decoded.</span></span>


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



<span data-ttu-id="cb787-128">Пифилестреам создается и инициализируется потоком файлов WIC для записи в файл образа "test2.jpg".</span><span class="sxs-lookup"><span data-stu-id="cb787-128">A WIC file stream piFileStream is created and initialized for writing to the image file "test2.jpg".</span></span> <span data-ttu-id="cb787-129">затем Пифилестреам используется для инициализации кодировщика, уведомляя кодировщика, где записывать биты образа после завершения кодирования.</span><span class="sxs-lookup"><span data-stu-id="cb787-129">piFileStream is then used to initialize the encoder, informing the encoder where to write the image bits when the encoding is complete.</span></span>

## <a name="part-3-copy-decoded-frame-information"></a><span data-ttu-id="cb787-130">Часть 3. копирование сведений о декодированном кадре</span><span class="sxs-lookup"><span data-stu-id="cb787-130">Part 3: Copy Decoded Frame Information</span></span>

<span data-ttu-id="cb787-131">Следующий код копирует каждый кадр изображения в новый кадр кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cb787-131">The following code copies each frame of an image to a new frame of the encoder.</span></span> <span data-ttu-id="cb787-132">Эта копия включает в себя размер, разрешение и формат пикселей; все, что необходимо для создания допустимого кадра.</span><span class="sxs-lookup"><span data-stu-id="cb787-132">This copy includes size, resolution, and pixel format; all of which are necessary to create a valid frame.</span></span>

> [!Note]  
> <span data-ttu-id="cb787-133">В изображениях JPEG будет содержаться только один кадр, а цикл ниже не является технически необходимым, но он включен для демонстрации использования нескольких кадров для поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="cb787-133">JPEG images will only have one frame and the loop below is not technically necessary but is included to demonstrate multi-frame usage for formats that support it.</span></span>

 


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



<span data-ttu-id="cb787-134">Следующий код выполняет быструю проверку, чтобы определить, совпадают ли форматы исходного и конечного изображений.</span><span class="sxs-lookup"><span data-stu-id="cb787-134">The following code performs a quick check to determine whether the source and destination image formats are the same.</span></span> <span data-ttu-id="cb787-135">Это необходимо, так как в части 4 показана операция, которая поддерживается только в том случае, если исходный и конечный форматы совпадают.</span><span class="sxs-lookup"><span data-stu-id="cb787-135">This is needed as Part 4 shows an operation that is only supported when the source and destination format are the same.</span></span>


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



## <a name="part-4-copy-the-metadata"></a><span data-ttu-id="cb787-136">Часть 4. Копирование метаданных</span><span class="sxs-lookup"><span data-stu-id="cb787-136">Part 4: Copy the Metadata</span></span>

> [!Note]  
> <span data-ttu-id="cb787-137">Код в этом разделе действителен, только если форматы исходного и конечного изображений совпадают.</span><span class="sxs-lookup"><span data-stu-id="cb787-137">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="cb787-138">Невозможно скопировать все метаданные изображения в одной операции при кодировании в другой формат изображения.</span><span class="sxs-lookup"><span data-stu-id="cb787-138">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="cb787-139">Для сохранения метаданных при повторном кодировании изображения в тот же формат изображения существуют методы, доступные для копирования всех метаданных в одной операции.</span><span class="sxs-lookup"><span data-stu-id="cb787-139">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="cb787-140">Каждая из этих операций соответствует аналогичному шаблону. Каждый из них устанавливает метаданные декодированного кадра непосредственно в новый закодированный кадр.</span><span class="sxs-lookup"><span data-stu-id="cb787-140">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span> <span data-ttu-id="cb787-141">Обратите внимание, что это делается для каждого отдельного кадра изображения.</span><span class="sxs-lookup"><span data-stu-id="cb787-141">Note that this is done for each individual image frame.</span></span>

<span data-ttu-id="cb787-142">Предпочтительным методом копирования метаданных является инициализация модуля записи блока нового кадра с помощью модуля чтения блоков декодированного кадра.</span><span class="sxs-lookup"><span data-stu-id="cb787-142">The preferred method for copying metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="cb787-143">Этот метод показан в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="cb787-143">The following code demonstrates this method.</span></span>


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



<span data-ttu-id="cb787-144">В этом примере вы просто получаете блок Reader и модуль записи блока из исходного фрейма и конечного фрейма соответственно.</span><span class="sxs-lookup"><span data-stu-id="cb787-144">In this example, you simply obtain the block reader and block writer from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="cb787-145">Затем модуль записи блока инициализируется модулем чтения блока.</span><span class="sxs-lookup"><span data-stu-id="cb787-145">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="cb787-146">При этом модуль записи блока инициализируется предварительно заполненными метаданными модуля чтения блока.</span><span class="sxs-lookup"><span data-stu-id="cb787-146">This initializes the block writer with the pre-populated metadata of the block reader.</span></span> <span data-ttu-id="cb787-147">Дополнительные сведения о дополнительных методах копирования метаданных см. в разделе запись метаданных статьи [Обзор чтения и записи метаданных изображения](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="cb787-147">To learn additional methods for copying metadata, see the Writing Metadata section in the [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="cb787-148">Опять же, эта операция работает только в том случае, если исходный и конечный образы имеют одинаковый формат.</span><span class="sxs-lookup"><span data-stu-id="cb787-148">Again, this operation works only when the source and destination images have the same format.</span></span> <span data-ttu-id="cb787-149">Это обусловлено тем, что различные форматы изображений хранят блоки метаданных в разных местах.</span><span class="sxs-lookup"><span data-stu-id="cb787-149">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="cb787-150">Например, файлы формата JPEG и TIFF поддерживают блоки метаданных в формате XMP.</span><span class="sxs-lookup"><span data-stu-id="cb787-150">For instance, both JPEG and Tagged Image File Format (TIFF) support Extensible Metadata Platform (XMP) metadata blocks.</span></span> <span data-ttu-id="cb787-151">В изображениях JPEG блок XMP находится в корневом блоке метаданных, как показано в разделе [Общие сведения о метаданных WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="cb787-151">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="cb787-152">Однако в изображении TIFF блок XMP внедряется в корневой блок IFD.</span><span class="sxs-lookup"><span data-stu-id="cb787-152">However, in a TIFF image, the XMP block is embedded in the root IFD block.</span></span>

## <a name="part-5-add-additional-metadata"></a><span data-ttu-id="cb787-153">Часть 5. Добавление дополнительных метаданных</span><span class="sxs-lookup"><span data-stu-id="cb787-153">Part 5: Add Additional Metadata</span></span>

<span data-ttu-id="cb787-154">В следующем примере показано, как добавить метаданные в целевой образ.</span><span class="sxs-lookup"><span data-stu-id="cb787-154">The following example demonstrates how to add metadata to the destination image.</span></span> <span data-ttu-id="cb787-155">Это делается путем вызова метода **сетметадатабинаме** модуля записи запроса с помощью выражения запроса и данных, хранящихся в [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="cb787-155">This is done by calling the query writer's **SetMetadataByName** method using a query expression and the data stored in a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span>


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



<span data-ttu-id="cb787-156">Дополнительные сведения о выражении запроса см. в разделе [Общие сведения о языке запросов метаданных](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="cb787-156">For more information on the query expression, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="part-6-finalize-the-encoded-image"></a><span data-ttu-id="cb787-157">Часть 6. Завершение закодированного изображения</span><span class="sxs-lookup"><span data-stu-id="cb787-157">Part 6: Finalize the Encoded Image</span></span>

<span data-ttu-id="cb787-158">Завершающим этапом копирования образа является запись пиксельных данных для кадра, фиксация кадра в кодировщике и фиксация кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cb787-158">The final steps for copying the image are to write the pixel data for the frame, commit the frame to the encoder, and commit the encoder.</span></span> <span data-ttu-id="cb787-159">При фиксации кодировщика в файл записывается поток изображения.</span><span class="sxs-lookup"><span data-stu-id="cb787-159">Committing the encoder writes the image stream to the file.</span></span>


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



<span data-ttu-id="cb787-160">Метод **вритесаурце** фрейма используется для записи данных пикселей для изображения.</span><span class="sxs-lookup"><span data-stu-id="cb787-160">The frame's **WriteSource** method is used to write the pixel data for the image.</span></span> <span data-ttu-id="cb787-161">Обратите внимание, что это делается после того, как были записаны метаданные.</span><span class="sxs-lookup"><span data-stu-id="cb787-161">Note that this is done after the metadata has been written.</span></span> <span data-ttu-id="cb787-162">Это необходимо, чтобы гарантировать, что метаданные имеют достаточно места в файле изображения.</span><span class="sxs-lookup"><span data-stu-id="cb787-162">This is necessary to ensure that the metadata has enough space within the image file.</span></span> <span data-ttu-id="cb787-163">После того как данные в пикселях записаны, кадр записывается в поток с помощью метода **фиксации** кадра.</span><span class="sxs-lookup"><span data-stu-id="cb787-163">After the pixel data is written, the frame is written to the stream using the frame's **Commit** method.</span></span> <span data-ttu-id="cb787-164">После обработки всех кадров кодировщик (и, таким образом, образ) завершается с помощью метода **commit** кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cb787-164">After all frames have been processed, the encoder (and thus the image) is finalized using the encoder's **Commit** method.</span></span>

<span data-ttu-id="cb787-165">После фиксации кадра необходимо освободить COM-объекты, созданные в цикле.</span><span class="sxs-lookup"><span data-stu-id="cb787-165">Once you commit the frame, you must release the COM objects created in the loop.</span></span>

## <a name="jpeg-re-encode-example-code"></a><span data-ttu-id="cb787-166">Код примера повторной кодировки JPEG</span><span class="sxs-lookup"><span data-stu-id="cb787-166">JPEG Re-encode Example Code</span></span>

<span data-ttu-id="cb787-167">Ниже приведен код из частей с 1 по 6 в одном блоке конвиениент.</span><span class="sxs-lookup"><span data-stu-id="cb787-167">The following is the code from Parts 1 through 6 in one convienient block.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cb787-168">См. также</span><span class="sxs-lookup"><span data-stu-id="cb787-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cb787-169">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="cb787-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cb787-170">Общие сведения о метаданных компонента WIC</span><span class="sxs-lookup"><span data-stu-id="cb787-170">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="cb787-171">Общие сведения о языке запросов метаданных</span><span class="sxs-lookup"><span data-stu-id="cb787-171">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="cb787-172">Общие сведения о чтении и записи метаданных изображений</span><span class="sxs-lookup"><span data-stu-id="cb787-172">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="cb787-173">Общие сведения о расширяемости метаданных</span><span class="sxs-lookup"><span data-stu-id="cb787-173">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
