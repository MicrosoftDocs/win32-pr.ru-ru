---
description: В этом руководстве для кодирования видео-файла используется модуль записи приемника.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: Учебник. Использование модуля записи приемника для кодирования видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3e6095355e18db6c8335cadcbc4afc56b35406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692776"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a><span data-ttu-id="10e3d-103">Учебник. Использование модуля записи приемника для кодирования видео</span><span class="sxs-lookup"><span data-stu-id="10e3d-103">Tutorial: Using the Sink Writer to Encode Video</span></span>

<span data-ttu-id="10e3d-104">В этом руководстве для кодирования видео-файла используется [модуль записи приемника](sink-writer.md) .</span><span class="sxs-lookup"><span data-stu-id="10e3d-104">This tutorial uses the [Sink Writer](sink-writer.md) to encode a video file.</span></span>

## <a name="define-the-video-format"></a><span data-ttu-id="10e3d-105">Определение формата видео</span><span class="sxs-lookup"><span data-stu-id="10e3d-105">Define the Video Format</span></span>

<span data-ttu-id="10e3d-106">Для простоты в этом учебнике используется фиксированный формат видео, определяемый следующими константами:</span><span class="sxs-lookup"><span data-stu-id="10e3d-106">For simplicity, this tutorial uses a fixed video format, defined by the following constants:</span></span>


```C++
// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;
```



<span data-ttu-id="10e3d-107">Эти константы указывают следующие параметры формата видео:</span><span class="sxs-lookup"><span data-stu-id="10e3d-107">These constants specify the following parameters of the video format:</span></span>

-   <span data-ttu-id="10e3d-108">Размер кадра (ширина и высота)</span><span class="sxs-lookup"><span data-stu-id="10e3d-108">Frame size (width and height)</span></span>
-   <span data-ttu-id="10e3d-109">Кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="10e3d-109">Frames per second.</span></span>
-   <span data-ttu-id="10e3d-110">Скорость кодирования.</span><span class="sxs-lookup"><span data-stu-id="10e3d-110">Encoded bit rate.</span></span>
-   <span data-ttu-id="10e3d-111">Формат кодирования — Windows Media Video 9 (**мфвидеоформат \_ WMV3**).</span><span class="sxs-lookup"><span data-stu-id="10e3d-111">Encoding format, which is Windows Media Video 9 (**MFVideoFormat\_WMV3**).</span></span>
-   <span data-ttu-id="10e3d-112">Формат входных данных (32-разрядный RGB).</span><span class="sxs-lookup"><span data-stu-id="10e3d-112">Input format, which is 32-bit RGB.</span></span>
-   <span data-ttu-id="10e3d-113">Длительность выходного файла.</span><span class="sxs-lookup"><span data-stu-id="10e3d-113">Duration of the output file.</span></span>

<span data-ttu-id="10e3d-114">Программа использует эти константы для создания типов мультимедиа, описывающих формат.</span><span class="sxs-lookup"><span data-stu-id="10e3d-114">The program uses these constants to create the media types that describe the format.</span></span> <span data-ttu-id="10e3d-115">В реальных приложениях обычно поддерживается ряд профилей кодирования.</span><span class="sxs-lookup"><span data-stu-id="10e3d-115">In a real application, you would typically support a range of encoding profiles.</span></span>

## <a name="create-an-uncompressed-video-frame"></a><span data-ttu-id="10e3d-116">Создание несжатого видеокадра</span><span class="sxs-lookup"><span data-stu-id="10e3d-116">Create an Uncompressed Video Frame</span></span>

<span data-ttu-id="10e3d-117">Кроме того, для простоты в этом учебнике в качестве входных данных используется статический кадр видео.</span><span class="sxs-lookup"><span data-stu-id="10e3d-117">Also for simplicity, this tutorial uses a static video frame as input.</span></span> <span data-ttu-id="10e3d-118">Видеокадр содержит сплошной зеленый прямоугольник и создается программным способом.</span><span class="sxs-lookup"><span data-stu-id="10e3d-118">The video frame contains a solid green rectangle and is generated programmatically.</span></span> <span data-ttu-id="10e3d-119">Кадр видео хранится в глобальной переменной как массив **DWORD** s:</span><span class="sxs-lookup"><span data-stu-id="10e3d-119">The video frame is stored in a global variable as an array of **DWORD** s:</span></span>


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



<span data-ttu-id="10e3d-120">Следующий код задает зеленый цвет для каждого пикселя в кадре:</span><span class="sxs-lookup"><span data-stu-id="10e3d-120">The following code sets every pixel in the frame to green:</span></span>


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a><span data-ttu-id="10e3d-121">Инициализация модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="10e3d-121">Initialize the Sink Writer</span></span>

<span data-ttu-id="10e3d-122">Чтобы инициализировать модуль записи приемника, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="10e3d-122">To initialize the sink writer, perform the following steps.</span></span>

1.  <span data-ttu-id="10e3d-123">Вызовите [**мфкреатесинквритерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) , чтобы создать новый экземпляр модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="10e3d-123">Call [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) to create a new instance of the sink writer.</span></span>
2.  <span data-ttu-id="10e3d-124">Создайте тип мультимедиа, описывающий закодированное видео.</span><span class="sxs-lookup"><span data-stu-id="10e3d-124">Create a media type that describes the encoded video.</span></span>
3.  <span data-ttu-id="10e3d-125">Передайте этот тип мультимедиа в метод [**имфсинквритер:: аддстреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) .</span><span class="sxs-lookup"><span data-stu-id="10e3d-125">Pass this media type to the [**IMFSinkWriter::AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) method.</span></span>
4.  <span data-ttu-id="10e3d-126">Создайте второй тип мультимедиа, который описывает несжатые входные данные.</span><span class="sxs-lookup"><span data-stu-id="10e3d-126">Create a second media type that describes the uncompressed input.</span></span>
5.  <span data-ttu-id="10e3d-127">Передайте несжатый тип мультимедиа в метод [**имфсинквритер:: сетинпутмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) .</span><span class="sxs-lookup"><span data-stu-id="10e3d-127">Pass the uncompressed media type to the [**IMFSinkWriter::SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) method.</span></span>
6.  <span data-ttu-id="10e3d-128">Вызовите метод [**имфсинквритер:: бегинвритинг**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) .</span><span class="sxs-lookup"><span data-stu-id="10e3d-128">Call the [**IMFSinkWriter::BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) method.</span></span>
7.  <span data-ttu-id="10e3d-129">Теперь модуль записи приемника готов принять примеры входных данных.</span><span class="sxs-lookup"><span data-stu-id="10e3d-129">The sink writer is now ready to accept input samples.</span></span>

<span data-ttu-id="10e3d-130">Эти действия показаны в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="10e3d-130">The following code shows these steps.</span></span>


```C++
HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}
```



<span data-ttu-id="10e3d-131">Большинство действий в предыдущем примере кода задают атрибуты типа мультимедиа для двух типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="10e3d-131">Most of the steps in previous code example are setting the media type attributes for the two media types.</span></span> <span data-ttu-id="10e3d-132">Сведения о типах носителей будут зависеть от исходного содержимого и требуемого профиля кодирования.</span><span class="sxs-lookup"><span data-stu-id="10e3d-132">The details of the media types will depend on your source content and the desired encoding profile.</span></span>

## <a name="send-video-frames-to-the-sink-writer"></a><span data-ttu-id="10e3d-133">Отправка кадров видео в модуль записи приемников</span><span class="sxs-lookup"><span data-stu-id="10e3d-133">Send Video Frames to the Sink Writer</span></span>

<span data-ttu-id="10e3d-134">Чтобы отправить кадр видео в модуль записи приемника, вызовите метод [**имфсинквритер:: вритесампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="10e3d-134">To send a video frame to the sink writer, call the [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method.</span></span> <span data-ttu-id="10e3d-135">Метод **вритесампле** принимает указатель на интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , который представляет *пример объекта мультимедиа* .</span><span class="sxs-lookup"><span data-stu-id="10e3d-135">The **WriteSample** method takes a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which represents a *media sample* object.</span></span> <span data-ttu-id="10e3d-136">Пример носителя содержит объект *буфера мультимедиа* , который, в свою очередь, содержит указатель на кадр видео.</span><span class="sxs-lookup"><span data-stu-id="10e3d-136">The media sample contains a *media buffer* object, which in turn contains a pointer to the video frame.</span></span> <span data-ttu-id="10e3d-137">Дополнительные сведения о примерах и буфере мультимедиа см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="10e3d-137">For more information about media samples and buffer, see the following topics.</span></span>

-   [<span data-ttu-id="10e3d-138">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="10e3d-138">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="10e3d-139">Буферы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="10e3d-139">Media Buffers</span></span>](media-buffers.md)

<span data-ttu-id="10e3d-140">В зависимости от приложения вы можете получить образцы мультимедиа из [модуля чтения исходного кода](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="10e3d-140">Depending on your application, you might get the media samples from the [Source Reader](source-reader.md).</span></span> <span data-ttu-id="10e3d-141">Кроме того, можно создать образцы мультимедиа и напрямую манипулировать данными в буфере.</span><span class="sxs-lookup"><span data-stu-id="10e3d-141">Alternatively, you can create the media samples and directly manipulate the data in the buffer.</span></span> <span data-ttu-id="10e3d-142">В следующем коде показан второй подход.</span><span class="sxs-lookup"><span data-stu-id="10e3d-142">The following code shows the second approach.</span></span> <span data-ttu-id="10e3d-143">Он создает буфер памяти и записывает в буфер один кадр видео.</span><span class="sxs-lookup"><span data-stu-id="10e3d-143">It creates a memory buffer and writes a single video frame to the buffer.</span></span> <span data-ttu-id="10e3d-144">Затем он добавляет этот буфер к примеру носителя и отправляет пример носителя в модуль записи приемника.</span><span class="sxs-lookup"><span data-stu-id="10e3d-144">Then it adds that buffer to a media sample, and sends the media sample to the sink writer.</span></span>


```C++
HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="10e3d-145">Этот код выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="10e3d-145">This code performs the following steps.</span></span>

1.  <span data-ttu-id="10e3d-146">Вызовите [**мфкреатемеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) , чтобы создать объект буфера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="10e3d-146">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer object.</span></span> <span data-ttu-id="10e3d-147">Эта функция выделяет память для буфера.</span><span class="sxs-lookup"><span data-stu-id="10e3d-147">This function allocates the memory for the buffer.</span></span>
2.  <span data-ttu-id="10e3d-148">Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , чтобы заблокировать буфер и получить указатель на память.</span><span class="sxs-lookup"><span data-stu-id="10e3d-148">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to lock the buffer and get a pointer to the memory.</span></span>
3.  <span data-ttu-id="10e3d-149">Вызовите [**мфкопимаже**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) , чтобы скопировать кадр видео в буфер.</span><span class="sxs-lookup"><span data-stu-id="10e3d-149">Call [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) to copy the video frame into the buffer.</span></span>
    > [!Note]  
    > <span data-ttu-id="10e3d-150">В этом конкретном примере использование **memcpy** будет работать так же хорошо.</span><span class="sxs-lookup"><span data-stu-id="10e3d-150">In this particular example, using **memcpy** would work just as well.</span></span> <span data-ttu-id="10e3d-151">Однако функция [**мфкопимаже**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) правильно обрабатывает случай, когда шаг исходного изображения не соответствует целевому буферу.</span><span class="sxs-lookup"><span data-stu-id="10e3d-151">However, the [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) function correctly handles the case where the stride of the source image does not match the target buffer.</span></span> <span data-ttu-id="10e3d-152">Дополнительные сведения см. в разделе [Шаг с изображением](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="10e3d-152">For more information, see [Image Stride](image-stride.md).</span></span>

     

4.  <span data-ttu-id="10e3d-153">Вызовите метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) , чтобы разблокировать буфер.</span><span class="sxs-lookup"><span data-stu-id="10e3d-153">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>
5.  <span data-ttu-id="10e3d-154">Вызовите [**имфмедиабуффер:: сеткуррентленгс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) , чтобы обновить длину допустимых данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="10e3d-154">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the length of the valid data in the buffer.</span></span> <span data-ttu-id="10e3d-155">(В противном случае это значение по умолчанию равно нулю.)</span><span class="sxs-lookup"><span data-stu-id="10e3d-155">(Otherwise, this value defaults to zero.)</span></span>
6.  <span data-ttu-id="10e3d-156">Вызовите [**мфкреатесампле**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) , чтобы создать пример объекта мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="10e3d-156">Call [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) to create a media sample object.</span></span>
7.  <span data-ttu-id="10e3d-157">Вызовите [**имфсампле:: аддбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) , чтобы добавить буфер мультимедиа в пример носителя.</span><span class="sxs-lookup"><span data-stu-id="10e3d-157">Call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) to add the media buffer to the media sample.</span></span>
8.  <span data-ttu-id="10e3d-158">Вызовите [**имфсампле:: сетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) , чтобы задать метку времени для видеокадра.</span><span class="sxs-lookup"><span data-stu-id="10e3d-158">Call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) to set the time stamp for the video frame.</span></span>
9.  <span data-ttu-id="10e3d-159">Вызовите [**имфсампле:: сетсампледуратион**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) , чтобы задать длительность кадра видео.</span><span class="sxs-lookup"><span data-stu-id="10e3d-159">Call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) to set the duration of the video frame.</span></span>
10. <span data-ttu-id="10e3d-160">Вызовите [**имфсинквритер:: вритесампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) , чтобы отправить пример носителя в модуль записи приемника.</span><span class="sxs-lookup"><span data-stu-id="10e3d-160">Call [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) to send the media sample to the sink writer.</span></span>

## <a name="write-the-main-function"></a><span data-ttu-id="10e3d-161">Написание функции Main</span><span class="sxs-lookup"><span data-stu-id="10e3d-161">Write the main Function</span></span>

<span data-ttu-id="10e3d-162">Внутри `main` функции выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="10e3d-162">Inside the `main` function, perform the following steps.</span></span>

1.  <span data-ttu-id="10e3d-163">Вызов [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="10e3d-163">Call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="10e3d-164">Вызовите [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) , чтобы инициализировать Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="10e3d-164">Call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize Microsoft Media Foundation.</span></span>
3.  <span data-ttu-id="10e3d-165">Создайте модуль записи приемника.</span><span class="sxs-lookup"><span data-stu-id="10e3d-165">Create the sink writer.</span></span>
4.  <span data-ttu-id="10e3d-166">Отправка кадров видео в модуль записи приемников.</span><span class="sxs-lookup"><span data-stu-id="10e3d-166">Send video frames to the sink writer.</span></span>
5.  <span data-ttu-id="10e3d-167">Вызовите метод [**имфсинквритер:: Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) , чтобы завершить выходной файл.</span><span class="sxs-lookup"><span data-stu-id="10e3d-167">Call [**IMFSinkWriter::Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) to finalize the output file.</span></span>
6.  <span data-ttu-id="10e3d-168">Освободите указатель на модуль записи приемника.</span><span class="sxs-lookup"><span data-stu-id="10e3d-168">Release the pointer to the sink writer.</span></span>
7.  <span data-ttu-id="10e3d-169">Вызовите [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="10e3d-169">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>
8.  <span data-ttu-id="10e3d-170">Вызов [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="10e3d-170">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>


```C++
void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="example-code"></a><span data-ttu-id="10e3d-171">Пример кода</span><span class="sxs-lookup"><span data-stu-id="10e3d-171">Example Code</span></span>

<span data-ttu-id="10e3d-172">В следующем коде показана полная программа.</span><span class="sxs-lookup"><span data-stu-id="10e3d-172">The following code shows the complete program.</span></span>


```C++
#include <Windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <Mfreadwrite.h>
#include <mferror.h>

#pragma comment(lib, "mfreadwrite")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;

// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];

HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}

HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="10e3d-173">См. также</span><span class="sxs-lookup"><span data-stu-id="10e3d-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10e3d-174">Модуль записи приемников</span><span class="sxs-lookup"><span data-stu-id="10e3d-174">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 
