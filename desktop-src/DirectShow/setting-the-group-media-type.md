---
description: Настройка типа носителя группы
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Настройка типа носителя группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365bd2171100a9d4bcfc48d70dbeb94d8a6639dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674541"
---
# <a name="setting-the-group-media-type"></a><span data-ttu-id="909d5-103">Настройка типа носителя группы</span><span class="sxs-lookup"><span data-stu-id="909d5-103">Setting the Group Media Type</span></span>

<span data-ttu-id="909d5-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="909d5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="909d5-105">Все группы должны определять несжатый тип носителя: аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="909d5-105">All groups must define an uncompressed media type, either audio or video.</span></span> <span data-ttu-id="909d5-106">Тип носителя без сжатия — это формат, который зрители видят или прослушивают во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="909d5-106">The uncompressed media type is the format that viewers see or hear during playback.</span></span> <span data-ttu-id="909d5-107">Как правило, окончательный результат будет иметь сжатый формат.</span><span class="sxs-lookup"><span data-stu-id="909d5-107">Typically, the final output will be in a compressed format.</span></span> <span data-ttu-id="909d5-108">Дополнительные сведения см. [в разделе Подготовка проекта к просмотру](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="909d5-108">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="909d5-109">Чтобы задать несжатый формат, создайте структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) и заполните ее соответствующим старшим типом, подтипом и заголовком формата.</span><span class="sxs-lookup"><span data-stu-id="909d5-109">To set the uncompressed format, create an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and fill it with the appropriate major type, subtype, and format header.</span></span> <span data-ttu-id="909d5-110">Для видео выделите структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) для блока Format и задайте ширину, высоту и глубину цвета.</span><span class="sxs-lookup"><span data-stu-id="909d5-110">For video, allocate a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure for the format block, and set the width, height, and bit depth.</span></span> <span data-ttu-id="909d5-111">Для звука необходимо выделить структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) для блока Format и задать частоту выборки, глубину и число каналов.</span><span class="sxs-lookup"><span data-stu-id="909d5-111">For audio, allocate a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure for the format block, and set the sample rate, bit depth, and number of channels.</span></span> <span data-ttu-id="909d5-112">Если задать только основной тип, DES предоставляет значения по умолчанию для других значений.</span><span class="sxs-lookup"><span data-stu-id="909d5-112">If you set just the major type, DES provides reasonable defaults for the other values.</span></span> <span data-ttu-id="909d5-113">На практике необходимо явно задать значения для управления выходными данными.</span><span class="sxs-lookup"><span data-stu-id="909d5-113">In practice, you should set the values explicitly to control the output.</span></span>

<span data-ttu-id="909d5-114">После инициализации структуры типа мультимедиа вызовите метод [**иамтимелинеграуп:: сетмедиатипе**](iamtimelinegroup-setmediatype.md) , чтобы задать тип носителя для группы.</span><span class="sxs-lookup"><span data-stu-id="909d5-114">After you initialize the media type structure, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method to set the media type for the group.</span></span>

<span data-ttu-id="909d5-115">В следующем примере задается 16-разрядное видео RGB, 320 пикселей в ширину на 240 пикселей в высоком формате:</span><span class="sxs-lookup"><span data-stu-id="909d5-115">The following example specifies 16-bit RGB video, 320 pixels wide by 240 pixels high:</span></span>


```C++
AM_MEDIA_TYPE mtGroup;  
mtGroup.majortype = MEDIATYPE_Video;
mtGroup.subtype = MEDIASUBTYPE_RGB555;

// Set format headers.
mtGroup.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(VIDEOINFOHEADER));
if (mtGroup.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}

VIDEOINFOHEADER *pVideoHeader = (VIDEOINFOHEADER*)mtGroup.pbFormat;
ZeroMemory(pVideoHeader, sizeof(VIDEOINFOHEADER));
pVideoHeader->bmiHeader.biBitCount = 16;
pVideoHeader->bmiHeader.biWidth = 320;
pVideoHeader->bmiHeader.biHeight = 240;
pVideoHeader->bmiHeader.biPlanes = 1;
pVideoHeader->bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
pVideoHeader->bmiHeader.biSizeImage = DIBSIZE(pVideoHeader->bmiHeader);

// Set the format type and size.
mtGroup.formattype = FORMAT_VideoInfo;
mtGroup.cbFormat = sizeof(VIDEOINFOHEADER);

// Set the sample size.
mtGroup.bFixedSizeSamples = TRUE;
mtGroup.lSampleSize = DIBSIZE(pVideoHeader->bmiHeader);

// Now use this media type for the group.
pGroup->SetMediaType(&mtGroup);

// Clean up.
CoTaskMemFree(mtGroup.pbFormat);
```



<span data-ttu-id="909d5-116">В следующем примере указана звуковая группа с указанием для типа носителя группы 16-разрядный стерео, 44100 выборок в секунду:</span><span class="sxs-lookup"><span data-stu-id="909d5-116">The next example specifies an audio group, by setting the group media type to 16-bit stereo, 44100 samples per second:</span></span>


```C++
AM_MEDIA_TYPE mt;  
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));

mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.formattype = FORMAT_WaveFormatEx;

// Set format block.
mt.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(WAVEFORMATEX));
if (mt.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}
mt.cbFormat = sizeof(WAVEFORMATEX);

// Fill in the WAVEFORMATEX structure.
WAVEFORMATEX *wave = (WAVEFORMATEX*) mt.pbFormat;
wave->wFormatTag = WAVE_FORMAT_PCM;
wave->nChannels = 2;  // Stereo
wave->nSamplesPerSec = 44100;
wave->wBitsPerSample = 16;
wave->nBlockAlign = wave->nChannels * wave->wBitsPerSample/8;
wave->nAvgBytesPerSec = wave->nSamplesPerSec * wave->nBlockAlign; 
wave->cbSize = 0;

hr = pGroup->SetMediaType(&mt);
CoTaskMemFree(mt.pbFormat);
```



<span data-ttu-id="909d5-117">Для управления типами мультимедиа можно также использовать класс [**кмедиатипе**](cmediatype.md) в [базовых классах DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="909d5-117">You can also use the [**CMediaType**](cmediatype.md) class in the [DirectShow Base Classes](directshow-base-classes.md) to manage media types.</span></span> <span data-ttu-id="909d5-118">Он содержит некоторые полезные вспомогательные методы и автоматически освобождает блок формата.</span><span class="sxs-lookup"><span data-stu-id="909d5-118">It contains some useful helper methods, and automatically releases the format block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="909d5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="909d5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="909d5-120">О типах носителей</span><span class="sxs-lookup"><span data-stu-id="909d5-120">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="909d5-121">Создание временной шкалы</span><span class="sxs-lookup"><span data-stu-id="909d5-121">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
