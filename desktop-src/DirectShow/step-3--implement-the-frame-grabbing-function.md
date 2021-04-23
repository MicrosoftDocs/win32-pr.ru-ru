---
description: Шаг 3. Реализация функции Frame-Grabbing
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Шаг 3. Реализация функции Frame-Grabbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97f585ff365e40ec611a9e11ce365839aa87be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911707"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a><span data-ttu-id="b5735-103">Шаг 3. Реализация функции Frame-Grabbing</span><span class="sxs-lookup"><span data-stu-id="b5735-103">Step 3: Implement the Frame-Grabbing Function</span></span>

<span data-ttu-id="b5735-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="b5735-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b5735-105">В этом разделе описан шаг 3 из [фрагмента плаката](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="b5735-105">This topic is Step 3 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="b5735-106">Следующим шагом является реализация функции GetNext, которая использует средство обнаружения мультимедиа для получения афиши.</span><span class="sxs-lookup"><span data-stu-id="b5735-106">The next step is to implement the GetBitmap function, which uses the Media Detector to grab a poster frame.</span></span> <span data-ttu-id="b5735-107">Внутри этой функции выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b5735-107">Inside this function, perform the following steps:</span></span>

1.  <span data-ttu-id="b5735-108">Создайте средство обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5735-108">Create the Media Detector.</span></span>
2.  <span data-ttu-id="b5735-109">Укажите файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5735-109">Specify a media file.</span></span>
3.  <span data-ttu-id="b5735-110">Проверьте каждый поток в файле.</span><span class="sxs-lookup"><span data-stu-id="b5735-110">Examine each stream in the file.</span></span> <span data-ttu-id="b5735-111">Если это поток видео, получите собственные размеры видео.</span><span class="sxs-lookup"><span data-stu-id="b5735-111">If it is a video stream, get the native dimensions of the video.</span></span>
4.  <span data-ttu-id="b5735-112">Получите рамку афиши, указав время поиска и целевое измерение.</span><span class="sxs-lookup"><span data-stu-id="b5735-112">Obtain a poster frame, specifying the seek time and the target dimension.</span></span>

<span data-ttu-id="b5735-113">Создайте объект детектора мультимедиа, вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):</span><span class="sxs-lookup"><span data-stu-id="b5735-113">Create the Media Detector object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):</span></span>


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



<span data-ttu-id="b5735-114">Укажите имя файла с помощью метода [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="b5735-114">Specify a file name, using the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method.</span></span> <span data-ttu-id="b5735-115">Этот метод принимает параметр **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="b5735-115">This method takes a **BSTR** parameter.</span></span>


```C++
hr = pDet->put_Filename(bstrFilename);
```



<span data-ttu-id="b5735-116">Получение числа потоков и цикл по каждому потоку, который проверяет тип носителя.</span><span class="sxs-lookup"><span data-stu-id="b5735-116">Get the number of streams, and loop through each stream checking the media type.</span></span> <span data-ttu-id="b5735-117">Метод [**имедиадет:: Get \_ аутпутстреамс**](imediadet-get-outputstreams.md) извлекает количество потоков, а метод [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md) указывает, какой поток следует проверить.</span><span class="sxs-lookup"><span data-stu-id="b5735-117">The [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) method retrieves the number of streams, and the [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) method specifies which stream to examine.</span></span> <span data-ttu-id="b5735-118">Завершите цикл в первом видеопотоке.</span><span class="sxs-lookup"><span data-stu-id="b5735-118">Exit the loop on the first video stream.</span></span>


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



<span data-ttu-id="b5735-119">Если поток видео не найден, функция завершает работу.</span><span class="sxs-lookup"><span data-stu-id="b5735-119">If no video stream was found, the function exits.</span></span>

<span data-ttu-id="b5735-120">В приведенном выше коде метод [**имедиадет:: Get \_ стреамтипе**](imediadet-get-streamtype.md) ВОЗВРАЩАЕТ только основной GUID типа.</span><span class="sxs-lookup"><span data-stu-id="b5735-120">In the previous code, the [**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md) method returns just the major type GUID.</span></span> <span data-ttu-id="b5735-121">Это удобно, если не нужно проверять полный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="b5735-121">This is convenient if you do not need to examine the complete media type.</span></span> <span data-ttu-id="b5735-122">Однако для получения измерений видео необходимо проверить блок формата, чтобы в нем требовался полный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="b5735-122">To get the video dimensions, however, it is necessary to examine the format block, so the full media type is needed.</span></span> <span data-ttu-id="b5735-123">Это можно получить, вызвав метод [**имедиадет:: Get \_ стреаммедиатипе**](imediadet-get-streammediatype.md) , который заполняет структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="b5735-123">You can retrieve that by calling the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method, which fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="b5735-124">Средство обнаружения мультимедиа преобразует все видеопотоки в несжатый формат с помощью блока формата [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="b5735-124">The Media Detector converts all video streams into uncompressed format, with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format block.</span></span>


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



<span data-ttu-id="b5735-125">Метод [**Get \_ стреаммедиатипе**](imediadet-get-streammediatype.md) выделяет блок формата, который вызывающий объект должен освободить.</span><span class="sxs-lookup"><span data-stu-id="b5735-125">The [**get\_StreamMediaType**](imediadet-get-streammediatype.md) method allocates the format block, which the caller must free.</span></span> <span data-ttu-id="b5735-126">В этом примере используется функция [**фримедиатипе**](freemediatype.md) из библиотеки базовых классов.</span><span class="sxs-lookup"><span data-stu-id="b5735-126">This example uses the [**FreeMediaType**](freemediatype.md) function from the base class library.</span></span>

<span data-ttu-id="b5735-127">Теперь все готово для получения рамки афиши.</span><span class="sxs-lookup"><span data-stu-id="b5735-127">Now you are ready to get the poster frame.</span></span> <span data-ttu-id="b5735-128">Сначала вызовите метод [**имедиадет:: жетбитмапбитс**](imediadet-getbitmapbits.md) с **пустым** указателем для буфера:</span><span class="sxs-lookup"><span data-stu-id="b5735-128">First call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method with a **NULL** pointer for the buffer:</span></span>


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



<span data-ttu-id="b5735-129">Этот вызов возвращает необходимый размер буфера в параметре *лсизе* .</span><span class="sxs-lookup"><span data-stu-id="b5735-129">This call returns the required buffer size in the *lSize* parameter.</span></span> <span data-ttu-id="b5735-130">Первый параметр задает время потока для поиска; в этом примере используется нулевое значение времени.</span><span class="sxs-lookup"><span data-stu-id="b5735-130">The first parameter specifies the stream time to seek to; this example uses time zero.</span></span> <span data-ttu-id="b5735-131">Для ширины и высоты в этом примере используются собственные измерения видео, полученные ранее.</span><span class="sxs-lookup"><span data-stu-id="b5735-131">For the width and height, this example uses the native video dimensions obtained earlier.</span></span> <span data-ttu-id="b5735-132">Если указать другие значения, то средство обнаружения мультимедиа растягивает точечный рисунок для соответствия.</span><span class="sxs-lookup"><span data-stu-id="b5735-132">If you specify other values, the Media Detector will stretch the bitmap to match.</span></span>

<span data-ttu-id="b5735-133">Если метод выполнен, выделите буфер и снова вызовите [**жетбитмапбитс**](imediadet-getbitmapbits.md) :</span><span class="sxs-lookup"><span data-stu-id="b5735-133">If the method succeeds, allocate the buffer and call [**GetBitmapBits**](imediadet-getbitmapbits.md) again:</span></span>


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



<span data-ttu-id="b5735-134">Ниже приведена полная функция с более лучшей обработкой ошибок.</span><span class="sxs-lookup"><span data-stu-id="b5735-134">Here is the complete function, with somewhat better error handling.</span></span>


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



<span data-ttu-id="b5735-135">Далее: [Шаг 4. Рисование точечного рисунка в клиентской области](step-4--draw-the-bitmap-on-the-client-area.md)</span><span class="sxs-lookup"><span data-stu-id="b5735-135">Next: [Step 4: Draw the Bitmap on the Client Area](step-4--draw-the-bitmap-on-the-client-area.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5735-136">См. также</span><span class="sxs-lookup"><span data-stu-id="b5735-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5735-137">Зафрагментировать рамку афиши</span><span class="sxs-lookup"><span data-stu-id="b5735-137">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
