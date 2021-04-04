---
description: В этом разделе описывается, как задать формат расширенного потока звука (AAC) в Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Типы носителей AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999857"
---
# <a name="aac-media-types"></a><span data-ttu-id="d50bc-103">Типы носителей AAC</span><span class="sxs-lookup"><span data-stu-id="d50bc-103">AAC Media Types</span></span>

<span data-ttu-id="d50bc-104">В этом разделе описывается, как задать формат расширенного потока звука (AAC) в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d50bc-104">This topic describes how to specify the format of an Advanced Audio Coding (AAC) stream in Media Foundation.</span></span>

<span data-ttu-id="d50bc-105">Для AAC Audio определены два подтипа:</span><span class="sxs-lookup"><span data-stu-id="d50bc-105">Two subtypes are defined for AAC audio:</span></span>



| <span data-ttu-id="d50bc-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="d50bc-106">Subtype</span></span>                     | <span data-ttu-id="d50bc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d50bc-107">Description</span></span>          | <span data-ttu-id="d50bc-108">Header</span><span class="sxs-lookup"><span data-stu-id="d50bc-108">Header</span></span>       |
|-----------------------------|----------------------|--------------|
| <span data-ttu-id="d50bc-109">**Мфаудиоформат \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="d50bc-109">**MFAudioFormat\_AAC**</span></span>      | <span data-ttu-id="d50bc-110">Необработанный AAC или ADTS AAC.</span><span class="sxs-lookup"><span data-stu-id="d50bc-110">Raw AAC or ADTS AAC.</span></span> | <span data-ttu-id="d50bc-111">мфапи. h</span><span class="sxs-lookup"><span data-stu-id="d50bc-111">mfapi.h</span></span>      |
| <span data-ttu-id="d50bc-112">**МЕДИАСУБТИПЕ \_ RAW \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="d50bc-112">**MEDIASUBTYPE\_RAW\_AAC1**</span></span> | <span data-ttu-id="d50bc-113">Необработанный AAC.</span><span class="sxs-lookup"><span data-stu-id="d50bc-113">Raw AAC.</span></span>             | <span data-ttu-id="d50bc-114">вмкодекдсп. h</span><span class="sxs-lookup"><span data-stu-id="d50bc-114">wmcodecdsp.h</span></span> |



 

<dl> <dt>

<span data-ttu-id="d50bc-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>Мфаудиоформат \_ AAC</span><span class="sxs-lookup"><span data-stu-id="d50bc-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat\_AAC</span></span>
</dt> <dd>

<span data-ttu-id="d50bc-116">Для этого подтипа мультимедиа тип носителя предоставляет частоту выборки и число каналов перед применением средств Спектрал (SBR) Replication и параметрической стерео (PS), если они есть.</span><span class="sxs-lookup"><span data-stu-id="d50bc-116">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="d50bc-117">Результатом работы средства SBR является двойная декодированная частота выборки по сравнению с частотой выборки ядра AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="d50bc-117">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="d50bc-118">Результатом работы средства PS является декодирование стерео из потока AAC-LC ядра Mono.</span><span class="sxs-lookup"><span data-stu-id="d50bc-118">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span>

<span data-ttu-id="d50bc-119">Этот подтип эквивалентен **медиасубтипе \_ MPEG \_ хеаак**, определенному в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="d50bc-119">This subtype is equivalent to **MEDIASUBTYPE\_MPEG\_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="d50bc-120">См. раздел [идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d50bc-120">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="d50bc-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>МЕДИАСУБТИПЕ \_ RAW \_ AAC1</span><span class="sxs-lookup"><span data-stu-id="d50bc-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE\_RAW\_AAC1</span></span>
</dt> <dd>

<span data-ttu-id="d50bc-122">Этот подтип используется для AAC, содержащихся в AVI-файле, с тегом формата Audio, равным \_ \_ RAW \_ -AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="d50bc-122">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE\_FORMAT\_RAW\_AAC1 (0x00FF).</span></span>

<span data-ttu-id="d50bc-123">Для этого подтипа тип носителя предоставляет частоту выборки и число каналов после применения инструментов SBR и PS, если они есть.</span><span class="sxs-lookup"><span data-stu-id="d50bc-123">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span>

</dd> </dl>

<span data-ttu-id="d50bc-124">Следующие атрибуты типа мультимедиа применяются к AAC аудио.</span><span class="sxs-lookup"><span data-stu-id="d50bc-124">The following media type attributes apply to AAC audio.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d50bc-125">attribute</span><span class="sxs-lookup"><span data-stu-id="d50bc-125">Attribute</span></span></th>
<th><span data-ttu-id="d50bc-126">Описание</span><span class="sxs-lookup"><span data-stu-id="d50bc-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d50bc-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d50bc-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="d50bc-128">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="d50bc-128">Major type.</span></span> <span data-ttu-id="d50bc-129">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="d50bc-129">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d50bc-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d50bc-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="d50bc-131">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="d50bc-131">Audio subtype.</span></span> <span data-ttu-id="d50bc-132">Дополнительные сведения см. в описании выше.</span><span class="sxs-lookup"><span data-stu-id="d50bc-132">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d50bc-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="d50bc-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="d50bc-134">Профиль и уровень звука.</span><span class="sxs-lookup"><span data-stu-id="d50bc-134">Audio profile and level.</span></span> <br/> <span data-ttu-id="d50bc-135">Значением этого атрибута является поле <strong>аудиопрофилелевелиндикатион</strong> , ОПРЕДЕЛЕННОЕ в стандарте ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="d50bc-135">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span><br/> <span data-ttu-id="d50bc-136">Если неизвестно, задайте для параметра значение 0 или 0xFE ( &quot; профиль звука не указан &quot; ).</span><span class="sxs-lookup"><span data-stu-id="d50bc-136">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d50bc-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="d50bc-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="d50bc-138">Битовая скорость закодированного потока AAC в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="d50bc-138">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d50bc-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="d50bc-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="d50bc-140">Тип полезных данных.</span><span class="sxs-lookup"><span data-stu-id="d50bc-140">Payload type.</span></span><br/> <span data-ttu-id="d50bc-141">Применяется только к <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="d50bc-141">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span><br/> <span data-ttu-id="d50bc-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d50bc-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="d50bc-143">Если этот атрибут не указан, используется значение по умолчанию 0, которое указывает, что поток содержит только элементы raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="d50bc-143">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d50bc-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d50bc-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="d50bc-145">Битовая глубина декодированного звука PCM.</span><span class="sxs-lookup"><span data-stu-id="d50bc-145">Bit depth of the decoded PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d50bc-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d50bc-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="d50bc-147">Назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="d50bc-147">Assignment of audio channels to speaker positions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d50bc-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d50bc-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="d50bc-149">Количество каналов, включая канал с низкой частотой (НИЗКОЧАСТОТный), если он есть.</span><span class="sxs-lookup"><span data-stu-id="d50bc-149">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/> <span data-ttu-id="d50bc-150">Интерпретация этого значения зависит от подтипа носителя, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="d50bc-150">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d50bc-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="d50bc-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="d50bc-152">Частота выборки, в примерах в секунду.</span><span class="sxs-lookup"><span data-stu-id="d50bc-152">Sample rate, in samples per second.</span></span><br/> <span data-ttu-id="d50bc-153">Интерпретация этого значения зависит от подтипа носителя, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="d50bc-153">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d50bc-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d50bc-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="d50bc-155">Значение этого атрибута зависит от подтипа:</span><span class="sxs-lookup"><span data-stu-id="d50bc-155">The value of this attribute depends on the subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="d50bc-156"><strong>MFAudioFormat_AAC</strong>: содержит часть структуры <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>хеааквавеинфо</strong></a> , которая появляется после структуры <strong>вавеформатекс</strong> (то есть после элемента <strong>вфкс</strong> ).</span><span class="sxs-lookup"><span data-stu-id="d50bc-156"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="d50bc-157">За ним следуют данные АудиоспеЦификконфиг () в соответствии с определением ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="d50bc-157">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="d50bc-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: содержит данные аудиоспеЦификконфиг ().</span><span class="sxs-lookup"><span data-stu-id="d50bc-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d50bc-159">См. также</span><span class="sxs-lookup"><span data-stu-id="d50bc-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d50bc-160">Типы звуковых носителей</span><span class="sxs-lookup"><span data-stu-id="d50bc-160">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="d50bc-161">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d50bc-161">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="d50bc-162">Поддержка MPEG-4 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d50bc-162">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="d50bc-163">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d50bc-163">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

