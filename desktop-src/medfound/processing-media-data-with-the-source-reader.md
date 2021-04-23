---
description: В этом разделе описывается использование модуля чтения исходного кода для обработки данных мультимедиа.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Использование модуля чтения исходного кода для обработки данных мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351182"
---
# <a name="using-the-source-reader-to-process-media-data"></a><span data-ttu-id="7885c-103">Использование модуля чтения исходного кода для обработки данных мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7885c-103">Using the Source Reader to Process Media Data</span></span>

<span data-ttu-id="7885c-104">В этом разделе описывается использование [модуля чтения исходного кода](source-reader.md) для обработки данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7885c-104">This topic describes how to use the [Source Reader](source-reader.md) to process media data.</span></span>

<span data-ttu-id="7885c-105">Чтобы использовать средство чтения исходного кода, выполните следующие основные действия.</span><span class="sxs-lookup"><span data-stu-id="7885c-105">To use the Source Reader, follow these basic steps:</span></span>

1.  <span data-ttu-id="7885c-106">Создайте экземпляр модуля чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="7885c-106">Create an instance of the Source Reader.</span></span>
2.  <span data-ttu-id="7885c-107">Перечисление возможных форматов вывода.</span><span class="sxs-lookup"><span data-stu-id="7885c-107">Enumerate the possible output formats.</span></span>
3.  <span data-ttu-id="7885c-108">Задайте фактический выходной формат для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="7885c-108">Set the actual output format for each stream.</span></span>
4.  <span data-ttu-id="7885c-109">Обработка данных из источника.</span><span class="sxs-lookup"><span data-stu-id="7885c-109">Process data from the source.</span></span>

<span data-ttu-id="7885c-110">В оставшейся части этого раздела подробно описываются эти действия.</span><span class="sxs-lookup"><span data-stu-id="7885c-110">The remainder of this topic describes these steps in detail.</span></span>

-   [<span data-ttu-id="7885c-111">Создание модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="7885c-111">Creating the Source Reader</span></span>](#creating-the-source-reader)
-   [<span data-ttu-id="7885c-112">Перечисление выходных форматов</span><span class="sxs-lookup"><span data-stu-id="7885c-112">Enumerating Output Formats</span></span>](#enumerating-output-formats)
-   [<span data-ttu-id="7885c-113">Задание форматов выходных данных</span><span class="sxs-lookup"><span data-stu-id="7885c-113">Setting Output Formats</span></span>](#setting-output-formats)
-   [<span data-ttu-id="7885c-114">Обработка данных мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7885c-114">Processing Media Data</span></span>](#using-the-source-reader-to-process-media-data)
-   [<span data-ttu-id="7885c-115">Сток конвейера данных</span><span class="sxs-lookup"><span data-stu-id="7885c-115">Draining the Data Pipeline</span></span>](#draining-the-data-pipeline)
-   [<span data-ttu-id="7885c-116">Получение длительности файла</span><span class="sxs-lookup"><span data-stu-id="7885c-116">Getting the File Duration</span></span>](#getting-the-file-duration)
-   [<span data-ttu-id="7885c-117">Нужна</span><span class="sxs-lookup"><span data-stu-id="7885c-117">Seeking</span></span>](#seeking)
-   [<span data-ttu-id="7885c-118">Скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="7885c-118">Playback Rate</span></span>](#playback-rate)
-   [<span data-ttu-id="7885c-119">Аппаратное ускорение</span><span class="sxs-lookup"><span data-stu-id="7885c-119">Hardware Acceleration</span></span>](#hardware-acceleration)
-   [<span data-ttu-id="7885c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7885c-120">Related topics</span></span>](#related-topics)

## <a name="creating-the-source-reader"></a><span data-ttu-id="7885c-121">Создание модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="7885c-121">Creating the Source Reader</span></span>

<span data-ttu-id="7885c-122">Чтобы создать экземпляр модуля чтения исходного кода, вызовите одну из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="7885c-122">To create an instance of the Source Reader, call one of the following functions:</span></span>



| <span data-ttu-id="7885c-123">Функция</span><span class="sxs-lookup"><span data-stu-id="7885c-123">Function</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="7885c-124">Описание</span><span class="sxs-lookup"><span data-stu-id="7885c-124">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7885c-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span><span class="sxs-lookup"><span data-stu-id="7885c-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span></span><br/>                                         | <span data-ttu-id="7885c-126">Принимает в качестве входных данных URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7885c-126">Takes a URL as input.</span></span> <span data-ttu-id="7885c-127">Эта функция использует [сопоставитель источника](source-resolver.md) для создания источника мультимедиа из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7885c-127">This function uses the [Source Resolver](source-resolver.md) to create a media source from the URL.</span></span><br/>                                                                       |
| <span data-ttu-id="7885c-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**мфкреатесаурцереадерфромбитестреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span><span class="sxs-lookup"><span data-stu-id="7885c-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span></span><br/>      | <span data-ttu-id="7885c-129">Принимает указатель на байтовый поток.</span><span class="sxs-lookup"><span data-stu-id="7885c-129">Takes a pointer to a byte stream.</span></span> <span data-ttu-id="7885c-130">Эта функция также использует сопоставитель источников для создания источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7885c-130">This function also uses the Source Resolver to create the media source.</span></span><br/>                                                                                        |
| <span data-ttu-id="7885c-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span><span class="sxs-lookup"><span data-stu-id="7885c-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span></span><br/> | <span data-ttu-id="7885c-132">Принимает указатель на источник мультимедиа, который уже был создан.</span><span class="sxs-lookup"><span data-stu-id="7885c-132">Takes a pointer to a media source that has already been created.</span></span> <span data-ttu-id="7885c-133">Эта функция полезна для источников мультимедиа, которые сопоставитель источников не может создавать, таких как устройства записи или пользовательские источники мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7885c-133">This function is useful for media sources that the Source Resolver cannot create, such capture devices or custom media sources.</span></span><br/> |



 

<span data-ttu-id="7885c-134">Как правило, для файлов мультимедиа используется [**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span><span class="sxs-lookup"><span data-stu-id="7885c-134">Typically, for media files, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span></span> <span data-ttu-id="7885c-135">Для устройств, таких как камеры, используйте [**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span><span class="sxs-lookup"><span data-stu-id="7885c-135">For devices, such as webcams, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span></span> <span data-ttu-id="7885c-136">(Дополнительные сведения о захвате устройств в Microsoft Media Foundation см. в разделе [запись звука и видео](audio-video-capture.md).)</span><span class="sxs-lookup"><span data-stu-id="7885c-136">(For more information about capture devices in Microsoft Media Foundation, see [Audio/Video Capture](audio-video-capture.md).)</span></span>

<span data-ttu-id="7885c-137">Каждая из этих функций принимает необязательный указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , который используется для задания различных параметров модуля чтения исходного кода, как описано в справочных разделах по этим функциям.</span><span class="sxs-lookup"><span data-stu-id="7885c-137">Each of these functions takes an optional [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer, which is used to set various options on the Source Reader, as described in the reference topics for these functions.</span></span> <span data-ttu-id="7885c-138">Чтобы получить поведение по умолчанию, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7885c-138">To get the default behavior, set this parameter to **NULL**.</span></span> <span data-ttu-id="7885c-139">Каждая функция возвращает указатель [**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="7885c-139">Each function returns an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer as an output parameter.</span></span> <span data-ttu-id="7885c-140">Перед вызовом любой из этих функций необходимо вызвать функцию **CoInitialize (ex)** и [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="7885c-140">You must call **CoInitialize(Ex)** and [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function before calling any of these functions.</span></span>

<span data-ttu-id="7885c-141">Следующий код создает модуль чтения исходного кода из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7885c-141">The following code creates the Source Reader from a URL.</span></span>


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a><span data-ttu-id="7885c-142">Перечисление выходных форматов</span><span class="sxs-lookup"><span data-stu-id="7885c-142">Enumerating Output Formats</span></span>

<span data-ttu-id="7885c-143">Каждый источник мультимедиа имеет по крайней мере один поток.</span><span class="sxs-lookup"><span data-stu-id="7885c-143">Every media source has at least one stream.</span></span> <span data-ttu-id="7885c-144">Например, видеофайл может содержать поток видео и аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="7885c-144">For example, a video file might contain a video stream and an audio stream.</span></span> <span data-ttu-id="7885c-145">Формат каждого потока описывается с помощью типа мультимедиа, представленного интерфейсом [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="7885c-145">The format of each stream is described using a media type, represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="7885c-146">Дополнительные сведения о типах носителей см. в разделе [типы носителей](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="7885c-146">For more information about media types, see [Media Types](media-types.md).</span></span> <span data-ttu-id="7885c-147">Необходимо проверить тип носителя, чтобы понять формат данных, получаемых от модуля чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="7885c-147">You must examine the media type to understand the format of the data that you get from the Source Reader.</span></span>

<span data-ttu-id="7885c-148">Изначально каждый поток имеет формат по умолчанию, который можно найти, вызвав метод [**имфсаурцереадер:: жеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :</span><span class="sxs-lookup"><span data-stu-id="7885c-148">Initially, every stream has a default format, which you can find by calling the [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) method:</span></span>

<span data-ttu-id="7885c-149">Для каждого потока источник мультимедиа предлагает список возможных типов носителей для этого потока.</span><span class="sxs-lookup"><span data-stu-id="7885c-149">For each stream, the media source offers a list of possible media types for that stream.</span></span> <span data-ttu-id="7885c-150">Количество типов зависит от источника.</span><span class="sxs-lookup"><span data-stu-id="7885c-150">The number of types depends on the source.</span></span> <span data-ttu-id="7885c-151">Если источник представляет файл мультимедиа, обычно существует только один тип для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="7885c-151">If the source represents a media file, there is typically only one type per stream.</span></span> <span data-ttu-id="7885c-152">Веб-камера, с другой стороны, может иметь возможность потоковой передачи видео в нескольких разных форматах.</span><span class="sxs-lookup"><span data-stu-id="7885c-152">A webcam, on the other hand, might be able to stream video in several different formats.</span></span> <span data-ttu-id="7885c-153">В этом случае приложение может выбрать используемый формат из списка типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7885c-153">In that case, the application can select which format to use from the list of media types.</span></span>

<span data-ttu-id="7885c-154">Чтобы получить один из типов мультимедиа для потока, вызовите метод [**имфсаурцереадер:: жетнативемедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) .</span><span class="sxs-lookup"><span data-stu-id="7885c-154">To get one of the media types for a stream, call the [**IMFSourceReader::GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) method.</span></span> <span data-ttu-id="7885c-155">Этот метод принимает два параметра индекса: индекс потока и индекс в списке типов мультимедиа для потока.</span><span class="sxs-lookup"><span data-stu-id="7885c-155">This method takes two index parameters: The index of the stream, and an index into the list of media types for the stream.</span></span> <span data-ttu-id="7885c-156">Чтобы перечислить все типы для потока, увеличьте индекс списка, сохраняя константу индекса потока.</span><span class="sxs-lookup"><span data-stu-id="7885c-156">To enumerate all the types for a stream, increment the list index while keeping the stream index constant.</span></span> <span data-ttu-id="7885c-157">Если индекс списка выходит за пределы диапазона, **жетнативемедиатипе** возвращает **MF E \_ больше \_ \_ \_ типов**.</span><span class="sxs-lookup"><span data-stu-id="7885c-157">When the list index goes out of bounds, **GetNativeMediaType** returns **MF\_E\_NO\_MORE\_TYPES**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



<span data-ttu-id="7885c-158">Чтобы перечислить типы носителей для каждого потока, увеличьте индекс потока.</span><span class="sxs-lookup"><span data-stu-id="7885c-158">To enumerate the media types for every stream, increment the stream index.</span></span> <span data-ttu-id="7885c-159">Если индекс потока выходит за пределы допустимого диапазона, [**жетнативемедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) возвращает **MF \_ E \_ инвалидстреамнумбер**.</span><span class="sxs-lookup"><span data-stu-id="7885c-159">When the stream index goes out of bounds, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) returns **MF\_E\_INVALIDSTREAMNUMBER**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a><span data-ttu-id="7885c-160">Задание форматов выходных данных</span><span class="sxs-lookup"><span data-stu-id="7885c-160">Setting Output Formats</span></span>

<span data-ttu-id="7885c-161">Чтобы изменить формат выходных данных, вызовите метод [**имфсаурцереадер:: сеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) .</span><span class="sxs-lookup"><span data-stu-id="7885c-161">To change the output format, call the [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) method.</span></span> <span data-ttu-id="7885c-162">Этот метод принимает индекс потока и тип мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="7885c-162">This method takes the stream index and a media type:</span></span>

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

<span data-ttu-id="7885c-163">Для типа носителя он зависит от того, требуется ли вставить декодер.</span><span class="sxs-lookup"><span data-stu-id="7885c-163">For the media type, it depends on whether you want to insert a decoder.</span></span>

-   <span data-ttu-id="7885c-164">Чтобы получить данные непосредственно из источника без декодирования, используйте один из типов, возвращаемых функцией [**жетнативемедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span><span class="sxs-lookup"><span data-stu-id="7885c-164">To get data directly from the source without decoding it, use one of the types returned by [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span></span>
-   <span data-ttu-id="7885c-165">Чтобы декодировать поток, создайте новый тип мультимедиа, описывающий требуемый формат без сжатия.</span><span class="sxs-lookup"><span data-stu-id="7885c-165">To decode the stream, create a new media type that describes the desired uncompressed format.</span></span>

<span data-ttu-id="7885c-166">В случае с декодером Создайте тип мультимедиа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7885c-166">In the case of the decoder, create the media type as follows:</span></span>

1.  <span data-ttu-id="7885c-167">Вызовите [**мфкреатемедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) , чтобы создать новый тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7885c-167">Call [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create a new media type.</span></span>
2.  <span data-ttu-id="7885c-168">Задайте атрибут [**" \_ \_ основной \_ тип MF MT**](mf-mt-major-type-attribute.md) ", чтобы указать аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="7885c-168">Set the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to specify audio or video.</span></span>
3.  <span data-ttu-id="7885c-169">Установите атрибут [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) , чтобы указать подтип формата декодирования.</span><span class="sxs-lookup"><span data-stu-id="7885c-169">Set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to specify the subtype of the decoding format.</span></span> <span data-ttu-id="7885c-170">(См. раздел [идентификаторы GUID подтипа аудио](audio-subtype-guids.md) и [GUID подтипа видео](video-subtype-guids.md).)</span><span class="sxs-lookup"><span data-stu-id="7885c-170">(See [Audio Subtype GUIDs](audio-subtype-guids.md) and [Video Subtype GUIDs](video-subtype-guids.md).)</span></span>
4.  <span data-ttu-id="7885c-171">Вызовите [**имфсаурцереадер:: сеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="7885c-171">Call [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span>

<span data-ttu-id="7885c-172">Модуль чтения исходного кода автоматически загрузит декодер.</span><span class="sxs-lookup"><span data-stu-id="7885c-172">The Source Reader will automatically load the decoder.</span></span> <span data-ttu-id="7885c-173">Чтобы получить полные сведения о декодированном формате, вызовите метод [**имфсаурцереадер:: жеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) после вызова [**сеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span><span class="sxs-lookup"><span data-stu-id="7885c-173">To get the complete details of the decoded format, call [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) after the call to [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span></span>

<span data-ttu-id="7885c-174">Следующий код настраивает поток видео для RGB-32 и звукового потока PCM.</span><span class="sxs-lookup"><span data-stu-id="7885c-174">The following code configures the video stream for RGB-32 and the audio stream for PCM audio.</span></span>


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a><span data-ttu-id="7885c-175">Обработка данных мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7885c-175">Processing Media Data</span></span>

<span data-ttu-id="7885c-176">Чтобы получить данные мультимедиа из источника, вызовите метод [**имфсаурцереадер:: реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="7885c-176">To get media data from the source, call the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method, as shown in the following code.</span></span>


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



<span data-ttu-id="7885c-177">Первый параметр — это индекс потока, для которого необходимо получить данные.</span><span class="sxs-lookup"><span data-stu-id="7885c-177">The first parameter is the index of the stream for which you want to get data.</span></span> <span data-ttu-id="7885c-178">Кроме того, можно указать для **\_ \_ средства чтения источника MF \_ любой \_ поток** , чтобы получить следующие доступные данные из любого потока.</span><span class="sxs-lookup"><span data-stu-id="7885c-178">You can also specify **MF\_SOURCE\_READER\_ANY\_STREAM** to get the next available data from any stream.</span></span> <span data-ttu-id="7885c-179">Второй параметр содержит необязательные флаги. Список этих параметров см. в описании [**\_ \_ \_ \_ флага управления считыванием источника MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) .</span><span class="sxs-lookup"><span data-stu-id="7885c-179">The second parameter contains optional flags; see [**MF\_SOURCE\_READER\_CONTROL\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) for a list of these.</span></span> <span data-ttu-id="7885c-180">Третий параметр получает индекс потока, который фактически создает данные.</span><span class="sxs-lookup"><span data-stu-id="7885c-180">The third parameter receives the index of the stream that actually produces the data.</span></span> <span data-ttu-id="7885c-181">Эти сведения понадобятся, если для первого параметра задать значение **MF \_ \_ Stream считывающего \_ потока в любом \_ потоке**.</span><span class="sxs-lookup"><span data-stu-id="7885c-181">You will need this information if you set the first parameter to **MF\_SOURCE\_READER\_ANY\_STREAM**.</span></span> <span data-ttu-id="7885c-182">Четвертый параметр получает флаги состояния, указывающие различные события, которые могут возникнуть при чтении данных, например изменения формата в потоке.</span><span class="sxs-lookup"><span data-stu-id="7885c-182">The fourth parameter receives status flags, indicating various events that can occur while reading the data, such as format changes in the stream.</span></span> <span data-ttu-id="7885c-183">Список флагов состояния см. в разделе [**MF \_ source \_ Reader \_ флаг**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span><span class="sxs-lookup"><span data-stu-id="7885c-183">For a list of status flags, see [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span></span>

<span data-ttu-id="7885c-184">Если источник мультимедиа способен создавать данные для запрошенного потока, последний параметр [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) получает указатель на интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) образца объекта мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7885c-184">If the media source is able to produce data for the requested stream, the last parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of a media sample object.</span></span> <span data-ttu-id="7885c-185">Используйте пример носителя для:</span><span class="sxs-lookup"><span data-stu-id="7885c-185">Use the media sample to:</span></span>

-   <span data-ttu-id="7885c-186">Получение указателя на данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7885c-186">Get a pointer to the media data.</span></span>
-   <span data-ttu-id="7885c-187">Получите время презентации и длительность выборки.</span><span class="sxs-lookup"><span data-stu-id="7885c-187">Get the presentation time and sample duration.</span></span>
-   <span data-ttu-id="7885c-188">Получите атрибуты, описывающие чередование, превосходство полей и другие аспекты образца.</span><span class="sxs-lookup"><span data-stu-id="7885c-188">Get attributes that describe interlacing, field dominance, and other aspects of the sample.</span></span>

<span data-ttu-id="7885c-189">Содержимое данных мультимедиа зависит от формата потока.</span><span class="sxs-lookup"><span data-stu-id="7885c-189">The contents of the media data depend on the format of the stream.</span></span> <span data-ttu-id="7885c-190">Для несжатого видеопотока каждый пример носителя содержит один кадр видео.</span><span class="sxs-lookup"><span data-stu-id="7885c-190">For an uncompressed video stream, each media sample contains a single video frame.</span></span> <span data-ttu-id="7885c-191">Для несжатого звукового потока каждый пример носителя содержит последовательность звуковых кадров.</span><span class="sxs-lookup"><span data-stu-id="7885c-191">For an uncompressed audio stream, each media sample contains a sequence of audio frames.</span></span>

<span data-ttu-id="7885c-192">Метод [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) может возвращать значение **S \_ ОК** , но не возвращает пример носителя в параметре *псампле* .</span><span class="sxs-lookup"><span data-stu-id="7885c-192">The [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method can return **S\_OK** and yet not return a media sample in the *pSample* parameter.</span></span> <span data-ttu-id="7885c-193">Например, при достижении конца файла **реадсампле** устанавливает флаг **MF \_ source \_ реадерф \_ ENDOFSTREAM** в *dwFlags* и задает для *псампле* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7885c-193">For example, when you reach the end of the file, **ReadSample** sets the **MF\_SOURCE\_READERF\_ENDOFSTREAM** flag in *dwFlags* and sets *pSample* to **NULL**.</span></span> <span data-ttu-id="7885c-194">В этом случае метод **реадсампле** возвращает значение **S \_ ОК** , так как не возникла ошибка, даже если параметр *псампле* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7885c-194">In this case, the **ReadSample** method returns **S\_OK** because no error has occurred, even though the *pSample* parameter is set to **NULL**.</span></span> <span data-ttu-id="7885c-195">Поэтому всегда следует проверять значение параметра *псампле* перед его разыменованием.</span><span class="sxs-lookup"><span data-stu-id="7885c-195">Therefore, always check the value of *pSample* before you dereference it.</span></span>

<span data-ttu-id="7885c-196">В следующем коде показано, как вызвать [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) в цикле и проверить сведения, возвращаемые методом, пока не будет достигнут конец файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7885c-196">The following code shows how to call [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in a loop and check the information returned by the method, until the end of the media file is reached.</span></span>


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a><span data-ttu-id="7885c-197">Сток конвейера данных</span><span class="sxs-lookup"><span data-stu-id="7885c-197">Draining the Data Pipeline</span></span>

<span data-ttu-id="7885c-198">Во время обработки данных декодер или другое преобразование могут буферизовать входные образцы.</span><span class="sxs-lookup"><span data-stu-id="7885c-198">During data processing, a decoder or other transform might buffer input samples.</span></span> <span data-ttu-id="7885c-199">На следующей схеме приложение вызывает [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) и получает пример с временем презентации, равным *T1*.</span><span class="sxs-lookup"><span data-stu-id="7885c-199">In the following diagram, the application calls [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) and receives a sample with a presentation time equal to *t1*.</span></span> <span data-ttu-id="7885c-200">Декодер удерживает примеры для *T2* и *T3*.</span><span class="sxs-lookup"><span data-stu-id="7885c-200">The decoder is holding samples for *t2* and *t3*.</span></span>

![Иллюстрация, показывающая буферизацию в декодере.](images/sourcereader02.png)

<span data-ttu-id="7885c-202">При следующем вызове [**Реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)модуль чтения исходного кода может предоставить декодеру *T4* и вернуть приложению значение *T2* .</span><span class="sxs-lookup"><span data-stu-id="7885c-202">On the next call to [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), the Source Reader might give *t4* to the decoder and return *t2* to the application.</span></span>

<span data-ttu-id="7885c-203">Если вы хотите декодировать все образцы, которые в данный момент помещены в буфер декодера, не передавая новые образцы в декодер, установите флаг **\_ \_ \_ \_ слива Контролф для считывания источника MF** в параметре *двконтролфлагс* [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="7885c-203">If you want to decode all of the samples that are currently buffered in the decoder, without passing any new samples to the decoder, set the **MF\_SOURCE\_READER\_CONTROLF\_DRAIN** flag in the *dwControlFlags* parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="7885c-204">Продолжайте делать это в цикле до тех пор, пока **реадсампле** не возвратит указатель образца **null** .</span><span class="sxs-lookup"><span data-stu-id="7885c-204">Continue to do this in a loop until **ReadSample** returns a **NULL** sample pointer.</span></span> <span data-ttu-id="7885c-205">В зависимости от способа выборки буферов декодера это может произойти сразу или после нескольких вызовов **реадсампле**.</span><span class="sxs-lookup"><span data-stu-id="7885c-205">Depending on how the decoder buffers samples, that might happen immediately or after several calls to **ReadSample**.</span></span>

## <a name="getting-the-file-duration"></a><span data-ttu-id="7885c-206">Получение длительности файла</span><span class="sxs-lookup"><span data-stu-id="7885c-206">Getting the File Duration</span></span>

<span data-ttu-id="7885c-207">Чтобы получить длительность файла мультимедиа, вызовите метод [**имфсаурцереадер:: жетпресентатионаттрибуте**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) и запросите атрибут [**Duration MF \_ PD \_**](mf-pd-duration-attribute.md) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="7885c-207">To get the duration of a media file, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method and request the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute, as shown in the following code.</span></span>


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="7885c-208">Показанная здесь функция возвращает длительность в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="7885c-208">The function shown here gets the duration in 100-nanosecond units.</span></span> <span data-ttu-id="7885c-209">Чтобы получить длительность в секундах, разделите на 10 000 000.</span><span class="sxs-lookup"><span data-stu-id="7885c-209">Divide by 10,000,000 to get the duration in seconds.</span></span>

## <a name="seeking"></a><span data-ttu-id="7885c-210">Нужна</span><span class="sxs-lookup"><span data-stu-id="7885c-210">Seeking</span></span>

<span data-ttu-id="7885c-211">Источник мультимедиа, который получает данные из локального файла, обычно может выполнять поиск произвольной позиции в файле.</span><span class="sxs-lookup"><span data-stu-id="7885c-211">A media source that gets data from a local file can usually seek to arbitrary positions in the file.</span></span> <span data-ttu-id="7885c-212">Устройства записи, такие как камеры, обычно не могут выполнять поиск, так как данные находятся в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="7885c-212">Capture devices such as webcams generally cannot seek, because the data is live.</span></span> <span data-ttu-id="7885c-213">Источник, который осуществляет потоковую передачу данных по сети, может выполнять поиск в зависимости от протокола потоковой передачи по сети.</span><span class="sxs-lookup"><span data-stu-id="7885c-213">A source that streams data over a network might be able to seek, depending on the network streaming protocol.</span></span>

<span data-ttu-id="7885c-214">Чтобы узнать, может ли источник мультимедиа искать, вызовите [**имфсаурцереадер:: жетпресентатионаттрибуте**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) и запросите атрибут [ \_ \_ \_ \_ характеристик медиасаурце для модуля чтения источника MF](mf-source-reader-mediasource-characteristics.md) , как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="7885c-214">To find out whether a media source can seek, call [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) and request the [MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS](mf-source-reader-mediasource-characteristics.md) attribute, as shown in the following code:</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



<span data-ttu-id="7885c-215">Эта функция возвращает набор флагов возможностей из источника.</span><span class="sxs-lookup"><span data-stu-id="7885c-215">This function gets a set of capabilities flags from the source.</span></span> <span data-ttu-id="7885c-216">Эти флаги определяются в перечислении [**\_ характеристик мфмедиасаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="7885c-216">These flags are defined in the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span> <span data-ttu-id="7885c-217">Для поиска связаны два флага:</span><span class="sxs-lookup"><span data-stu-id="7885c-217">Two flags relate to seeking:</span></span>



| <span data-ttu-id="7885c-218">Flag</span><span class="sxs-lookup"><span data-stu-id="7885c-218">Flag</span></span>                                                                                                                                      | <span data-ttu-id="7885c-219">Описание</span><span class="sxs-lookup"><span data-stu-id="7885c-219">Description</span></span>                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7885c-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**МФМЕДИАСАУРЦЕ \_ может \_ Искать**</span><span class="sxs-lookup"><span data-stu-id="7885c-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE\_CAN\_SEEK**</span></span><br/>                 | <span data-ttu-id="7885c-221">Источник может искать.</span><span class="sxs-lookup"><span data-stu-id="7885c-221">The source can seek.</span></span><br/>                                                                                                                                                                            |
| <span data-ttu-id="7885c-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**МФМЕДИАСАУРЦЕ \_ имеет \_ низкую \_ Поиск**</span><span class="sxs-lookup"><span data-stu-id="7885c-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE\_HAS\_SLOW\_SEEK**</span></span><br/> | <span data-ttu-id="7885c-223">Поиск может занять длительное время.</span><span class="sxs-lookup"><span data-stu-id="7885c-223">Seeking might take a long time to complete.</span></span> <span data-ttu-id="7885c-224">Например, источнику может потребоваться загрузить весь файл, прежде чем он сможет выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="7885c-224">For example, the source might need to download the entire file before it can seek.</span></span> <span data-ttu-id="7885c-225">(Нет никаких условий для возврата этого флага для источника.)</span><span class="sxs-lookup"><span data-stu-id="7885c-225">(There are no strict criteria for a source to return this flag.)</span></span><br/> |



 

<span data-ttu-id="7885c-226">Следующий код проверяет наличие флага **мфмедиасаурце \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="7885c-226">The following code tests for the **MFMEDIASOURCE\_CAN\_SEEK** flag.</span></span>


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



<span data-ttu-id="7885c-227">Для поиска вызовите метод [**имфсаурцереадер:: сеткуррентпоситион**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="7885c-227">To seek, call the [**IMFSourceReader::SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) method, as shown in the following code.</span></span>


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="7885c-228">Первый параметр дает формат времени, который используется для указания расположения поиска.</span><span class="sxs-lookup"><span data-stu-id="7885c-228">The first parameter gives the time format that you are using to specify the seek position.</span></span> <span data-ttu-id="7885c-229">Все источники мультимедиа в Media Foundation должны поддерживать единицы измерения 100-наносекундных, обозначенные значением **GUID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="7885c-229">All media sources in Media Foundation are required to support 100-nanosecond units, indicated by the value **GUID\_NULL**.</span></span> <span data-ttu-id="7885c-230">Второй параметр — это **пропвариант** , содержащий положение поиска.</span><span class="sxs-lookup"><span data-stu-id="7885c-230">The second parameter is a **PROPVARIANT** that contains the seek position.</span></span> <span data-ttu-id="7885c-231">Для единиц времени с 100-наносекундных типом данных является **лонглонг**.</span><span class="sxs-lookup"><span data-stu-id="7885c-231">For 100-nanosecond time units, the data type is **LONGLONG**.</span></span>

<span data-ttu-id="7885c-232">Учтите, что не каждый источник мультимедиа обеспечивает точное Поиск в кадрах.</span><span class="sxs-lookup"><span data-stu-id="7885c-232">Be aware that not every media source provides frame-accurate seeking.</span></span> <span data-ttu-id="7885c-233">Точность поиска зависит от нескольких факторов, например от интервала опорного кадра, от того, содержит ли файл мультимедиа индекс, а также указывает, имеет ли данные постоянную или переменную скорость.</span><span class="sxs-lookup"><span data-stu-id="7885c-233">The accuracy of seeking depends on several factors, such as the key frame interval, whether the media file contains an index, and whether the data has a constant or variable bit rate.</span></span> <span data-ttu-id="7885c-234">Поэтому после перехода к положению в файле нет никакой гарантии, что метка времени в следующем образце будет точно соответствовать запрошенной должности.</span><span class="sxs-lookup"><span data-stu-id="7885c-234">Therefore, after you seek to a position in a file, there is no guarantee that the time stamp on the next sample will exactly match the requested position.</span></span> <span data-ttu-id="7885c-235">Как правило, фактическая точка не будет позднее запрошенной позиции, поэтому можно отбросить выборку, пока не достигнет нужной точки в потоке.</span><span class="sxs-lookup"><span data-stu-id="7885c-235">Generally, the actual position will not be later than the requested position, so you can discard samples until you reach the desired point in the stream.</span></span>

## <a name="playback-rate"></a><span data-ttu-id="7885c-236">Скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="7885c-236">Playback Rate</span></span>

<span data-ttu-id="7885c-237">Хотя скорость воспроизведения можно задать с помощью модуля чтения исходного кода, обычно это не очень полезно по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="7885c-237">Although you can set the playback rate using the Source Reader, doing is typically not very useful, for the following reasons:</span></span>

-   <span data-ttu-id="7885c-238">Модуль чтения исходного кода не поддерживает обратную воспроизведение, даже если источник мультимедиа делает это.</span><span class="sxs-lookup"><span data-stu-id="7885c-238">The Source Reader does not support reverse playback, even if the media source does.</span></span>
-   <span data-ttu-id="7885c-239">Приложение управляет временем презентации, поэтому приложение может реализовать быстрое или низкое воспроизведение, не устанавливая скорость источника.</span><span class="sxs-lookup"><span data-stu-id="7885c-239">The application controls the presentation times, so the application can implement fast or slow play without setting the rate on the source.</span></span>
-   <span data-ttu-id="7885c-240">Некоторые источники мультимедиа поддерживают режим *тонкого* режима, где источник доставляет меньшее количество выборок — обычно всего лишь ключевые кадры.</span><span class="sxs-lookup"><span data-stu-id="7885c-240">Some media sources support *thinning* mode, where the source delivers fewer samples—typically just the key frames.</span></span> <span data-ttu-id="7885c-241">Однако если вы хотите удалить неключевые кадры, можно проверить каждый пример для атрибута [мфсампликстенсион \_ клеанпоинт](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="7885c-241">However, if you want to drop non-key frames, you can check each sample for the [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>

<span data-ttu-id="7885c-242">Чтобы задать скорость воспроизведения с помощью модуля чтения исходного кода, вызовите метод [**имфсаурцереадер:: жетсервицефорстреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) , чтобы получить интерфейсы [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) и [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) из источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7885c-242">To set the playback rate using the Source Reader, call the [**IMFSourceReader::GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) method to get the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) and [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interfaces from the media source.</span></span>

## <a name="hardware-acceleration"></a><span data-ttu-id="7885c-243">Аппаратное ускорение</span><span class="sxs-lookup"><span data-stu-id="7885c-243">Hardware Acceleration</span></span>

<span data-ttu-id="7885c-244">Модуль чтения исходного кода совместим с ускорением видео Microsoft DirectX (ДКСВА) 2,0 для декодирования видео с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="7885c-244">The Source Reader is compatible with Microsoft DirectX Video Acceleration (DXVA) 2.0 for hardware accelerated video decoding.</span></span> <span data-ttu-id="7885c-245">Чтобы использовать ДКСВА с модулем чтения исходного кода, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7885c-245">To use DXVA with the Source Reader, perform the following steps.</span></span>

1.  <span data-ttu-id="7885c-246">Создайте устройство Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7885c-246">Create a Microsoft Direct3D device.</span></span>
2.  <span data-ttu-id="7885c-247">Вызовите функцию [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) , чтобы создать диспетчер устройств Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7885c-247">Call the [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) function to create the Direct3D device manager.</span></span> <span data-ttu-id="7885c-248">Эта функция возвращает указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="7885c-248">This function gets a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span>
3.  <span data-ttu-id="7885c-249">Вызовите метод [**IDirect3DDeviceManager9:: ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) с указателем на устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7885c-249">Call the [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method with a pointer to the Direct3D device.</span></span>
4.  <span data-ttu-id="7885c-250">Создайте хранилище атрибутов, вызвав функцию [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="7885c-250">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
5.  <span data-ttu-id="7885c-251">Создайте модуль чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="7885c-251">Create the Source Reader.</span></span> <span data-ttu-id="7885c-252">Передайте хранилище атрибутов в параметре *паттрибутес* функции создания.</span><span class="sxs-lookup"><span data-stu-id="7885c-252">Pass the attribute store in the *pAttributes* parameter of the creation function.</span></span>

<span data-ttu-id="7885c-253">При предоставлении устройства Direct3D модуль чтения исходного кода выделяет видеоматериалы, совместимые с API обработчика видео ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="7885c-253">When you provide a Direct3D device, the Source Reader allocates video samples that are compatible with the DXVA video processor API.</span></span> <span data-ttu-id="7885c-254">Вы можете использовать обработку видео ДКСВА для выполнения аппаратного чередования или смешения видео.</span><span class="sxs-lookup"><span data-stu-id="7885c-254">You can use DXVA video processing to perform hardware deinterlacing or video mixing.</span></span> <span data-ttu-id="7885c-255">Дополнительные сведения см. в разделе [Обработка видео дксва](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="7885c-255">For more information, see [DXVA Video Processing](dxva-video-processing.md).</span></span> <span data-ttu-id="7885c-256">Кроме того, если декодер поддерживает ДКСВА 2,0, он будет использовать устройство Direct3D для выполнения декодирования с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="7885c-256">Also, if the decoder supports DXVA 2.0, it will use the Direct3D device to perform hardware-accelerated decoding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7885c-257">Начиная с Windows 8, вместо [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)можно использовать [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="7885c-257">Beginning in Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) can be used instead of the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span></span> <span data-ttu-id="7885c-258">Для приложений Магазина Windows необходимо использовать **имфдксгидевицеманажер**.</span><span class="sxs-lookup"><span data-stu-id="7885c-258">For Windows Store apps, you must use **IMFDXGIDeviceManager**.</span></span> <span data-ttu-id="7885c-259">Дополнительные сведения см. в статье [API-интерфейсы видео Direct3D 11](direct3d-11-video-apis.md).</span><span class="sxs-lookup"><span data-stu-id="7885c-259">For more info, see the [Direct3D 11 Video APIs](direct3d-11-video-apis.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7885c-260">См. также</span><span class="sxs-lookup"><span data-stu-id="7885c-260">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7885c-261">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="7885c-261">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




