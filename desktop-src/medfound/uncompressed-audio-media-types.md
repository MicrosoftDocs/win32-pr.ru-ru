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
# <a name="uncompressed-audio-media-types"></a>Несжатые типы звуковых носителей

Чтобы создать полный несжатый звуковой тип, установите для указателя интерфейса [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) по крайней мере следующие атрибуты.



| attribute                                                                                    | Описание                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md)                                    | Основной тип. Задайте значение Мфмедиатипе \_ Audio.                                                                                       |
| [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)                                           | Подтип. См. раздел [идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md).                                                                 |
| [**\_ \_ каналы аудиосигнала MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | Число аудиоканалов.                                                                                                    |
| [**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**](mf-mt-audio-samples-per-second-attribute.md)      | Количество звуковых выборок в секунду.                                                                                          |
| [**\_ \_ Выравнивание звукового \_ блока MF MT \_**](mf-mt-audio-block-alignment-attribute.md)             | Выравнивание блокировки.                                                                                                             |
| [**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Среднее число байтов в секунду.                                                                                          |
| [**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**](mf-mt-audio-bits-per-sample-attribute.md)            | Число битов на аудио выборка.                                                                                             |
| [**MF \_ — \_ все \_ \_ независимые примеры**](mf-mt-all-samples-independent-attribute.md)         | Указывает, является ли каждый звуковой образец независимым. Задайте значение **true** для \_ форматов PCM мфаудиоформат и мфаудиоформат \_ float. |



 

Кроме того, для некоторых звуковых форматов требуются следующие атрибуты.



| attribute                                                                                      | Описание                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ допустимый бит для звука MF MT \_ \_ на \_ выборку**](mf-mt-audio-valid-bits-per-sample-attribute.md) | Количество допустимых битов звуковых данных в каждом звуковом примере. Установите этот атрибут, если в звуковых примерах есть заполнение, т. е. Если число допустимых битов в каждом звуковом примере меньше размера выборки. |
| [**\_ \_ \_ Маска канала MF MT \_ Audio**](mf-mt-audio-channel-mask-attribute.md)                     | Назначение звуковых каналов для позиционирования динамиков. Задайте этот атрибут для многоканальных звуковых потоков, например 5,1. Этот атрибут не требуется для Mono или стерео аудио.                       |



 

### <a name="example-code"></a>Пример кода

В следующем коде показано, как создать тип мультимедиа для несжатого звука PCM.


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



В следующем примере в качестве входных данных используется закодированный звуковой формат и создается соответствующий тип звука PCM. Например, этот тип подходит для установки в кодировщике или декодере.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы звуковых носителей](audio-media-types.md)
</dt> </dl>

 

 



