---
description: О типах носителей
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: О типах мультимедиа (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3289a37e95bf5dbd1e5c277b5799a2c7c8c90586
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351232"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="ae153-103">О типах мультимедиа (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="ae153-103">About Media Types (DirectShow)</span></span>

<span data-ttu-id="ae153-104">Поскольку DirectShow является модульной, ей требуется способ описания формата данных в каждой точке графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="ae153-104">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="ae153-105">Например, рассмотрите возможность воспроизведения AVI.</span><span class="sxs-lookup"><span data-stu-id="ae153-105">For example, consider AVI playback.</span></span> <span data-ttu-id="ae153-106">Данные вводятся в граф в виде потока фрагментов Metallica.</span><span class="sxs-lookup"><span data-stu-id="ae153-106">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="ae153-107">Они анализируются по потокам видео и аудио.</span><span class="sxs-lookup"><span data-stu-id="ae153-107">These are parsed into video and audio streams.</span></span> <span data-ttu-id="ae153-108">Поток видео состоит из кадров видео, которые, вероятно, сжимаются.</span><span class="sxs-lookup"><span data-stu-id="ae153-108">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="ae153-109">После декодирования видеопоток представляет собой серию несжатых точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="ae153-109">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="ae153-110">Поток аудио проходит через аналогичный процесс.</span><span class="sxs-lookup"><span data-stu-id="ae153-110">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="ae153-111">Типы носителей: как DirectShow представляет форматы</span><span class="sxs-lookup"><span data-stu-id="ae153-111">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="ae153-112">*Тип мультимедиа* является универсальным и расширяемым способом описания форматов цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ae153-112">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="ae153-113">При подключении двух фильтров они согласовывают тип носителя.</span><span class="sxs-lookup"><span data-stu-id="ae153-113">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="ae153-114">Тип носителя определяет, какой тип данных будет доставлен вышестоящим фильтром в нисходящий фильтр, и физический макет данных.</span><span class="sxs-lookup"><span data-stu-id="ae153-114">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="ae153-115">Если два фильтра не могут согласовать тип носителя, они не будут подключаться.</span><span class="sxs-lookup"><span data-stu-id="ae153-115">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="ae153-116">Для некоторых приложений не придется беспокоиться о типах носителей.</span><span class="sxs-lookup"><span data-stu-id="ae153-116">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="ae153-117">Например, при воспроизведении файла DirectShow обрабатывает всю информацию.</span><span class="sxs-lookup"><span data-stu-id="ae153-117">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="ae153-118">Другим типам приложений может потребоваться работать непосредственно с типами мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ae153-118">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="ae153-119">Типы носителей определяются с помощью [**структуры \_ \_ типов мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="ae153-119">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="ae153-120">Эта структура содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="ae153-120">This structure contains the following information:</span></span>

-   <span data-ttu-id="ae153-121">**Основной тип**: основной тип — это идентификатор GUID, определяющий общую категорию данных.</span><span class="sxs-lookup"><span data-stu-id="ae153-121">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="ae153-122">К основным типам относятся видео, звуковые, непроанализированные байтовые потоки, данные MIDI и т. д.</span><span class="sxs-lookup"><span data-stu-id="ae153-122">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="ae153-123">**Подтип**: подтип — еще один идентификатор GUID, который дополнительно определяет формат.</span><span class="sxs-lookup"><span data-stu-id="ae153-123">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="ae153-124">Например, в основном типе видео существуют подтипы для RGB-24, RGB-32, UYVY и т. д.</span><span class="sxs-lookup"><span data-stu-id="ae153-124">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="ae153-125">В аудио есть звук PCM, полезные данные MPEG-1 и другие.</span><span class="sxs-lookup"><span data-stu-id="ae153-125">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="ae153-126">Подтип предоставляет больше информации, чем основной тип, но не определяет все сведения о формате.</span><span class="sxs-lookup"><span data-stu-id="ae153-126">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="ae153-127">Например, подтипы видео не определяют размер изображения или частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="ae153-127">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="ae153-128">Они определяются блоком format, описанным ниже.</span><span class="sxs-lookup"><span data-stu-id="ae153-128">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="ae153-129">**Блок формата**. блок формата представляет собой блок данных, подробно описывающий формат.</span><span class="sxs-lookup"><span data-stu-id="ae153-129">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="ae153-130">Блок формата выделяется отдельно от структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="ae153-130">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="ae153-131">Элемент **пбформат** структуры **\_ \_ типов мультимедиа** указывает на блок формата.</span><span class="sxs-lookup"><span data-stu-id="ae153-131">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="ae153-132">Элемент **пбформат** типизирован \**void \** _, так как макет блока форматирования изменяется в зависимости от типа носителя.</span><span class="sxs-lookup"><span data-stu-id="ae153-132">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="ae153-133">Например, в звуковом PCM используется структура [_ *вавеформатекс* \*](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ae153-133">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="ae153-134">Видео использует различные структуры, включая [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) и [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="ae153-134">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="ae153-135">Элемент **форматтипе** структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) представляет собой идентификатор GUID, указывающий, какая структура содержится в блоке формата.</span><span class="sxs-lookup"><span data-stu-id="ae153-135">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="ae153-136">Каждой структуре формата назначается идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="ae153-136">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="ae153-137">Элемент **кбформат** задает размер блока Format.</span><span class="sxs-lookup"><span data-stu-id="ae153-137">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="ae153-138">Всегда проверяйте эти значения перед разыменованием указателя **пбформат** .</span><span class="sxs-lookup"><span data-stu-id="ae153-138">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="ae153-139">Если блок формата заполнен, основной тип и подтип содержат избыточные сведения.</span><span class="sxs-lookup"><span data-stu-id="ae153-139">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="ae153-140">Однако основной тип и подтип предоставляют удобный способ для распознавания форматов без полного блока форматирования.</span><span class="sxs-lookup"><span data-stu-id="ae153-140">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="ae153-141">Например, можно указать универсальный 24-разрядный формат RGB (МЕДИАСУБТИПЕ \_ Rgb24), не зная всю информацию, необходимую для структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , например размер изображения и частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="ae153-141">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="ae153-142">Например, фильтр может использовать следующий код для проверки типа мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="ae153-142">For example, a filter might use the following code to check a media type:</span></span>


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



<span data-ttu-id="ae153-143">Структура [**\_ \_ типа файлов мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) также содержит некоторые необязательные поля.</span><span class="sxs-lookup"><span data-stu-id="ae153-143">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="ae153-144">Они могут использоваться для предоставления дополнительных сведений, но для их использования не требуются фильтры.</span><span class="sxs-lookup"><span data-stu-id="ae153-144">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="ae153-145">**лсамплесизе**.</span><span class="sxs-lookup"><span data-stu-id="ae153-145">**lSampleSize**.</span></span> <span data-ttu-id="ae153-146">Если это поле не равно нулю, оно определяет размер каждого образца.</span><span class="sxs-lookup"><span data-stu-id="ae153-146">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="ae153-147">Если он равен нулю, это означает, что размер выборки может измениться с Sample на Sample.</span><span class="sxs-lookup"><span data-stu-id="ae153-147">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="ae153-148">**бфикседсизесамплес**.</span><span class="sxs-lookup"><span data-stu-id="ae153-148">**bFixedSizeSamples**.</span></span> <span data-ttu-id="ae153-149">Если этот логический флаг имеет значение **true**, это означает, что значение в **лсамплесизе** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ae153-149">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="ae153-150">В противном случае следует игнорировать **лсамплесизе**.</span><span class="sxs-lookup"><span data-stu-id="ae153-150">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="ae153-151">**бтемпоралкомпрессион**.</span><span class="sxs-lookup"><span data-stu-id="ae153-151">**bTemporalCompression**.</span></span> <span data-ttu-id="ae153-152">Если этот логический флаг имеет **значение false**, это означает, что все кадры являются ключевыми кадрами.</span><span class="sxs-lookup"><span data-stu-id="ae153-152">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae153-153">См. также</span><span class="sxs-lookup"><span data-stu-id="ae153-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae153-154">Граф фильтра и его компоненты</span><span class="sxs-lookup"><span data-stu-id="ae153-154">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
