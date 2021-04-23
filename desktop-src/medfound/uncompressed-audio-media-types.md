---
description: Несжатые типы звуковых носителей
ms.assetid: 130a18a9-1c86-4d16-a8ae-ed57bf50f9bb
title: Несжатые типы звуковых носителей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d15f7211ef16d4280476f93744650b88742073
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693838"
---
# <a name="uncompressed-audio-media-types"></a><span data-ttu-id="7b699-103">Несжатые типы звуковых носителей</span><span class="sxs-lookup"><span data-stu-id="7b699-103">Uncompressed Audio Media Types</span></span>

<span data-ttu-id="7b699-104">Чтобы создать полный несжатый звуковой тип, установите для указателя интерфейса [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) по крайней мере следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="7b699-104">To create a complete uncompressed audio type, set at least the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="7b699-105">attribute</span><span class="sxs-lookup"><span data-stu-id="7b699-105">Attribute</span></span>                                                                                    | <span data-ttu-id="7b699-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7b699-106">Description</span></span>                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b699-107">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7b699-107">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="7b699-108">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="7b699-108">Major type.</span></span> <span data-ttu-id="7b699-109">Задайте значение Мфмедиатипе \_ Audio.</span><span class="sxs-lookup"><span data-stu-id="7b699-109">Set to MFMediaType\_Audio.</span></span>                                                                                       |
| [<span data-ttu-id="7b699-110">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="7b699-110">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="7b699-111">Подтип.</span><span class="sxs-lookup"><span data-stu-id="7b699-111">Subtype.</span></span> <span data-ttu-id="7b699-112">См. раздел [идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7b699-112">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>                                                                 |
| [<span data-ttu-id="7b699-113">**\_ \_ каналы аудиосигнала MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b699-113">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="7b699-114">Число аудиоканалов.</span><span class="sxs-lookup"><span data-stu-id="7b699-114">Number of audio channels.</span></span>                                                                                                    |
| [<span data-ttu-id="7b699-115">**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="7b699-115">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="7b699-116">Количество звуковых выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="7b699-116">Number of audio samples per second.</span></span>                                                                                          |
| [<span data-ttu-id="7b699-117">**\_ \_ Выравнивание звукового \_ блока MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="7b699-117">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="7b699-118">Выравнивание блокировки.</span><span class="sxs-lookup"><span data-stu-id="7b699-118">Block alignment.</span></span>                                                                                                             |
| [<span data-ttu-id="7b699-119">**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**</span><span class="sxs-lookup"><span data-stu-id="7b699-119">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="7b699-120">Среднее число байтов в секунду.</span><span class="sxs-lookup"><span data-stu-id="7b699-120">Average number of bytes per second.</span></span>                                                                                          |
| [<span data-ttu-id="7b699-121">**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**</span><span class="sxs-lookup"><span data-stu-id="7b699-121">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="7b699-122">Число битов на аудио выборка.</span><span class="sxs-lookup"><span data-stu-id="7b699-122">Number of bits per audio sample.</span></span>                                                                                             |
| [<span data-ttu-id="7b699-123">**MF \_ — \_ все \_ \_ независимые примеры**</span><span class="sxs-lookup"><span data-stu-id="7b699-123">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="7b699-124">Указывает, является ли каждый звуковой образец независимым.</span><span class="sxs-lookup"><span data-stu-id="7b699-124">Specifies whether each audio sample is independent.</span></span> <span data-ttu-id="7b699-125">Задайте значение **true** для \_ форматов PCM мфаудиоформат и мфаудиоформат \_ float.</span><span class="sxs-lookup"><span data-stu-id="7b699-125">Set to **TRUE** for MFAudioFormat\_PCM and MFAudioFormat\_Float formats.</span></span> |



 

<span data-ttu-id="7b699-126">Кроме того, для некоторых звуковых форматов требуются следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="7b699-126">In addition, the following attributes are required for some audio formats.</span></span>



| <span data-ttu-id="7b699-127">attribute</span><span class="sxs-lookup"><span data-stu-id="7b699-127">Attribute</span></span>                                                                                      | <span data-ttu-id="7b699-128">Описание</span><span class="sxs-lookup"><span data-stu-id="7b699-128">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b699-129">**\_ \_ \_ допустимый бит для звука MF MT \_ \_ на \_ выборку**</span><span class="sxs-lookup"><span data-stu-id="7b699-129">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md) | <span data-ttu-id="7b699-130">Количество допустимых битов звуковых данных в каждом звуковом примере.</span><span class="sxs-lookup"><span data-stu-id="7b699-130">Number of valid bits of audio data in each audio sample.</span></span> <span data-ttu-id="7b699-131">Установите этот атрибут, если в звуковых примерах есть заполнение, т. е. Если число допустимых битов в каждом звуковом примере меньше размера выборки.</span><span class="sxs-lookup"><span data-stu-id="7b699-131">Set this attribute if the audio samples have padding—that is, if the number of valid bits in each audio sample is less than the sample size.</span></span> |
| [<span data-ttu-id="7b699-132">**\_ \_ \_ Маска канала MF MT \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="7b699-132">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                     | <span data-ttu-id="7b699-133">Назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="7b699-133">The assignment of audio channels to speaker positions.</span></span> <span data-ttu-id="7b699-134">Задайте этот атрибут для многоканальных звуковых потоков, например 5,1.</span><span class="sxs-lookup"><span data-stu-id="7b699-134">Set this attribute for multichannel audio streams, such as 5.1.</span></span> <span data-ttu-id="7b699-135">Этот атрибут не требуется для Mono или стерео аудио.</span><span class="sxs-lookup"><span data-stu-id="7b699-135">This attribute is not required for mono or stereo audio.</span></span>                       |



 

### <a name="example-code"></a><span data-ttu-id="7b699-136">Пример кода</span><span class="sxs-lookup"><span data-stu-id="7b699-136">Example Code</span></span>

<span data-ttu-id="7b699-137">В следующем коде показано, как создать тип мультимедиа для несжатого звука PCM.</span><span class="sxs-lookup"><span data-stu-id="7b699-137">The following code shows how to create a media type for uncompressed PCM audio.</span></span>


```C++
HRESULT CreatePCMAudioType(
    UINT32 sampleRate,        // Samples per second
    UINT32 bitsPerSample,     // Bits per sample
    UINT32 cChannels,         // Number of channels
    IMFMediaType **ppType     // Receives a pointer to the media type.
    )
{
    HRESULT hr = S_OK;

    IMFMediaType *pType = NULL;

    // Calculate derived values.
    UINT32 blockAlign = cChannels * (bitsPerSample / 8);
    UINT32 bytesPerSecond = blockAlign * sampleRate;

    // Create the empty media type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set attributes on the type.
    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_NUM_CHANNELS, cChannels);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_SAMPLES_PER_SECOND, sampleRate);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, blockAlign);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_AVG_BYTES_PER_SECOND, bytesPerSecond);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BITS_PER_SAMPLE, bitsPerSample);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the type to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="7b699-138">В следующем примере в качестве входных данных используется закодированный звуковой формат и создается соответствующий тип звука PCM.</span><span class="sxs-lookup"><span data-stu-id="7b699-138">The next example takes an encoded audio format as input, and creates a matching PCM audio type.</span></span> <span data-ttu-id="7b699-139">Например, этот тип подходит для установки в кодировщике или декодере.</span><span class="sxs-lookup"><span data-stu-id="7b699-139">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
//-------------------------------------------------------------------
// ConvertAudioTypeToPCM
//
// Given an audio media type (which might describe a compressed audio
// format), returns a media type that describes the equivalent
// uncompressed PCM format.
//-------------------------------------------------------------------

HRESULT ConvertAudioTypeToPCM(
    IMFMediaType *pType,        // Pointer to an encoded audio type.
    IMFMediaType **ppType       // Receives a matching PCM audio type.
    )
{
    HRESULT hr = S_OK;

    GUID majortype = { 0 };
    GUID subtype = { 0 };

    UINT32 cChannels = 0;
    UINT32 samplesPerSec = 0;
    UINT32 bitsPerSample = 0;

    hr = pType->GetMajorType(&majortype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (majortype != MFMediaType_Audio)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Get the audio subtype.
    hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (subtype == MFAudioFormat_PCM)
    {
        // This is already a PCM audio type. Return the same pointer.

        *ppType = pType;
        (*ppType)->AddRef();

        return S_OK;
    }

    // Get the sample rate and other information from the audio format.

    cChannels = MFGetAttributeUINT32(pType, MF_MT_AUDIO_NUM_CHANNELS, 0);
    samplesPerSec = MFGetAttributeUINT32(pType, MF_MT_AUDIO_SAMPLES_PER_SECOND, 0);
    bitsPerSample = MFGetAttributeUINT32(pType, MF_MT_AUDIO_BITS_PER_SAMPLE, 16);

    // Note: Some encoded audio formats do not contain a value for bits/sample.
    // In that case, use a default value of 16. Most codecs will accept this value.

    if (cChannels == 0 || samplesPerSec == 0)
    {
        return MF_E_INVALIDTYPE;
    }

    // Create the corresponding PCM audio type.
    hr = CreatePCMAudioType(samplesPerSec, bitsPerSample, cChannels, ppType);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="7b699-140">См. также</span><span class="sxs-lookup"><span data-stu-id="7b699-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b699-141">Типы звуковых носителей</span><span class="sxs-lookup"><span data-stu-id="7b699-141">Audio Media Types</span></span>](audio-media-types.md)
</dt> </dl>

 

 



