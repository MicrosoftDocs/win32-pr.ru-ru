---
description: 'Microsoft Media Foundation декодер AAC — это Media Foundation преобразование, которое декодирует следующие дополнительные профили расширенного кодирования звука (AAC) и высокоэффективных профилей AAC (HE-AAC):'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Декодер AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701473"
---
# <a name="aac-decoder"></a><span data-ttu-id="eef9a-103">Декодер AAC</span><span class="sxs-lookup"><span data-stu-id="eef9a-103">AAC Decoder</span></span>

<span data-ttu-id="eef9a-104">Microsoft Media Foundation декодер AAC — это [Media Foundation преобразование](media-foundation-transforms.md) , которое декодирует следующие дополнительные профили расширенного кодирования звука (AAC) и высокоэффективных профилей AAC (HE-AAC):</span><span class="sxs-lookup"><span data-stu-id="eef9a-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="eef9a-105">Профиль низкой сложности MPEG-2 AAC (LC) (многоканальный).</span><span class="sxs-lookup"><span data-stu-id="eef9a-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="eef9a-106">MPEG-4 HE-AAC v1 (многоканальный) с AAC-LC Core.</span><span class="sxs-lookup"><span data-stu-id="eef9a-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="eef9a-107">MPEG-4 HE-AAC v2 (стерео) с AAC-LC Core.</span><span class="sxs-lookup"><span data-stu-id="eef9a-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="eef9a-108">Декодер AAC поддерживает как необработанные AAC потоки без заголовков, так и AAC в потоке передачи звуковых данных (ADTS).</span><span class="sxs-lookup"><span data-stu-id="eef9a-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="eef9a-109">Начиная с Windows 8, декодер AAC также поддерживает декодирование потоков потокового транспорта MPEG-4 с уровнем мультиплексирования (ЛАТМ) и уровнем синхронизации (УРОВНЯМИ гарантии).</span><span class="sxs-lookup"><span data-stu-id="eef9a-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="eef9a-110">Он также может преобразовать поток ЛАТМ/УРОВНЯМИ гарантии в ADTS.</span><span class="sxs-lookup"><span data-stu-id="eef9a-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="media-types"></a><span data-ttu-id="eef9a-111">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="eef9a-111">Media Types</span></span>

<span data-ttu-id="eef9a-112">Декодер AAC поддерживает следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="eef9a-112">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="eef9a-113">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="eef9a-113">Input Types</span></span>

<span data-ttu-id="eef9a-114">Декодер AAC поддерживает следующие подтипы звука:</span><span class="sxs-lookup"><span data-stu-id="eef9a-114">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="eef9a-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="eef9a-115">Subtype</span></span>                     | <span data-ttu-id="eef9a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="eef9a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="eef9a-117">Header</span><span class="sxs-lookup"><span data-stu-id="eef9a-117">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="eef9a-118">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="eef9a-118">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="eef9a-119">Необработанный AAC или ADTS AAC.</span><span class="sxs-lookup"><span data-stu-id="eef9a-119">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="eef9a-120">Для этого подтипа мультимедиа тип носителя предоставляет частоту выборки и число каналов перед применением средств Спектрал (SBR) Replication и параметрической стерео (PS), если они есть.</span><span class="sxs-lookup"><span data-stu-id="eef9a-120">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="eef9a-121">Результатом работы средства SBR является двойная декодированная частота выборки по сравнению с частотой выборки ядра AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="eef9a-121">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="eef9a-122">Результатом работы средства PS является декодирование стерео из потока AAC-LC ядра Mono.</span><span class="sxs-lookup"><span data-stu-id="eef9a-122">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="eef9a-123">Этот подтип эквивалентен **MEDIASUBTYPE_MPEG_HEAAC**, определенному в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="eef9a-123">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="eef9a-124">См. раздел [идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="eef9a-124">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="eef9a-125">Этот подтип выводится с помощью [источника файлов MPEG-4](mpeg-4-file-source.md) и средства синтаксического анализа ADTS.</span><span class="sxs-lookup"><span data-stu-id="eef9a-125">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="eef9a-126">мфапи. h</span><span class="sxs-lookup"><span data-stu-id="eef9a-126">mfapi.h</span></span>      |
| <span data-ttu-id="eef9a-127">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="eef9a-127">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="eef9a-128">Необработанный AAC.</span><span class="sxs-lookup"><span data-stu-id="eef9a-128">Raw AAC.</span></span> <br/> <span data-ttu-id="eef9a-129">Этот подтип используется для AAC, содержащихся в AVI-файле, с тегом формата Audio, равным WAVE_FORMAT_RAW_AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="eef9a-129">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="eef9a-130">Для этого подтипа тип носителя предоставляет частоту выборки и число каналов после применения инструментов SBR и PS, если они есть.</span><span class="sxs-lookup"><span data-stu-id="eef9a-130">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="eef9a-131">вмкодекдсп. h</span><span class="sxs-lookup"><span data-stu-id="eef9a-131">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="eef9a-132">Чтобы настроить декодер AAC, задайте следующие атрибуты для входного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="eef9a-132">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eef9a-133">attribute</span><span class="sxs-lookup"><span data-stu-id="eef9a-133">Attribute</span></span></th>
<th><span data-ttu-id="eef9a-134">Описание</span><span class="sxs-lookup"><span data-stu-id="eef9a-134">Description</span></span></th>
<th><span data-ttu-id="eef9a-135">Remarks</span><span class="sxs-lookup"><span data-stu-id="eef9a-135">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eef9a-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-137">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="eef9a-137">Major type.</span></span></td>
<td><span data-ttu-id="eef9a-138">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="eef9a-138">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eef9a-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-140">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="eef9a-140">Audio subtype.</span></span></td>
<td><span data-ttu-id="eef9a-141">Дополнительные сведения см. в описании выше.</span><span class="sxs-lookup"><span data-stu-id="eef9a-141">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eef9a-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="eef9a-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="eef9a-143">Профиль и уровень звука.</span><span class="sxs-lookup"><span data-stu-id="eef9a-143">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="eef9a-144">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eef9a-144">Optional.</span></span> <span data-ttu-id="eef9a-145">Применяется только к <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="eef9a-145">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="eef9a-146">Значением этого атрибута является поле <strong>аудиопрофилелевелиндикатион</strong> , ОПРЕДЕЛЕННОЕ в стандарте ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="eef9a-146">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="eef9a-147">Если неизвестно, задайте для параметра значение 0 или 0xFE ( &quot; профиль звука не указан &quot; ).</span><span class="sxs-lookup"><span data-stu-id="eef9a-147">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eef9a-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="eef9a-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="eef9a-149">Тип полезных данных.</span><span class="sxs-lookup"><span data-stu-id="eef9a-149">Payload type.</span></span><br/></td>
<td><span data-ttu-id="eef9a-150">Применяется только к <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="eef9a-150">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="eef9a-151">Декодер поддерживает следующие типы полезных данных:</span><span class="sxs-lookup"><span data-stu-id="eef9a-151">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="eef9a-152">0: необработанный AAC.</span><span class="sxs-lookup"><span data-stu-id="eef9a-152">0: Raw AAC.</span></span> <span data-ttu-id="eef9a-153">Поток содержит только элементы raw_data_block (), как определено в формате MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="eef9a-153">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="eef9a-154">1: ADTS.</span><span class="sxs-lookup"><span data-stu-id="eef9a-154">1: ADTS.</span></span> <span data-ttu-id="eef9a-155">Поток содержит adts_sequence (), как определено в формате MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="eef9a-155">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="eef9a-156">Допускается только один raw_data_block () на adts_frame ().</span><span class="sxs-lookup"><span data-stu-id="eef9a-156">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="eef9a-157">3: потоковый транспорт потока с уровнем синхронизации (УРОВНЯМИ гарантии) и уровнем мультиплексирования (ЛАТМ).</span><span class="sxs-lookup"><span data-stu-id="eef9a-157">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="eef9a-158">Из трех типов УРОВНЯМИ гарантии поддерживается только <strong>аудиосинкстреам</strong> .</span><span class="sxs-lookup"><span data-stu-id="eef9a-158">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="eef9a-159">Уровень мультиплексора — <strong>аудиомукселемент</strong>, ограничен одной звуковой программой и одним слоем.</span><span class="sxs-lookup"><span data-stu-id="eef9a-159">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="eef9a-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> является необязательным.</span><span class="sxs-lookup"><span data-stu-id="eef9a-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="eef9a-161">Если этот атрибут не указан, используется значение по умолчанию 0, которое указывает, что поток содержит только элементы raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="eef9a-161">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eef9a-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-163">Требуемая битовая глубина декодированного звука PCM.</span><span class="sxs-lookup"><span data-stu-id="eef9a-163">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="eef9a-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-165">Указывает назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="eef9a-165">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="eef9a-166">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eef9a-166">Optional.</span></span> <span data-ttu-id="eef9a-167">Дополнительные сведения см. в разделе <a href="#format-constraints">ограничения формата</a>.</span><span class="sxs-lookup"><span data-stu-id="eef9a-167">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eef9a-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-169">Количество каналов, включая канал с низкой частотой (НИЗКОЧАСТОТный), если он есть.</span><span class="sxs-lookup"><span data-stu-id="eef9a-169">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="eef9a-170">Интерпретация этого значения зависит от подтипа носителя, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="eef9a-170">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eef9a-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-172">Частота выборки, в примерах в секунду.</span><span class="sxs-lookup"><span data-stu-id="eef9a-172">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="eef9a-173">Интерпретация этого значения зависит от подтипа носителя, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="eef9a-173">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eef9a-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-175">Дополнительные сведения о форматировании.</span><span class="sxs-lookup"><span data-stu-id="eef9a-175">Additional format information.</span></span></td>
<td><span data-ttu-id="eef9a-176">Значение этого атрибута зависит от подтипа.</span><span class="sxs-lookup"><span data-stu-id="eef9a-176">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="eef9a-177"><strong>MFAudioFormat_AAC</strong>: содержит часть структуры <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>хеааквавеинфо</strong></a> , которая появляется после структуры <strong>вавеформатекс</strong> (то есть после элемента <strong>вфкс</strong> ).</span><span class="sxs-lookup"><span data-stu-id="eef9a-177"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="eef9a-178">За ним следуют данные АудиоспеЦификконфиг () в соответствии с определением ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="eef9a-178">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="eef9a-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: содержит данные аудиоспеЦификконфиг ().</span><span class="sxs-lookup"><span data-stu-id="eef9a-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="eef9a-180">Эти данные должны отобразиться; в противном случае декодер отклонит тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="eef9a-180">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="eef9a-181">Длина данных АудиоспеЦификконфиг () составляет 2 байта для AAC-LC или AAC с неявным сигналом SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="eef9a-181">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="eef9a-182">Это более 2 байта для AAC с явной сигнализацией SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="eef9a-182">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="eef9a-183">Значение <strong>аудиубжекттипе</strong> , определенное в аудиоспеЦификконфиг (), должно быть равно 2, что означает AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="eef9a-183">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="eef9a-184">Значение параметра <strong>екстенсионаудиубжекттипе</strong> должно быть равно 5 для SBR или 29 для PS.</span><span class="sxs-lookup"><span data-stu-id="eef9a-184">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="eef9a-185">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="eef9a-185">Output Types</span></span>

<span data-ttu-id="eef9a-186">Декодер поддерживает следующие типы выходных данных:</span><span class="sxs-lookup"><span data-stu-id="eef9a-186">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eef9a-187">Subtype</span><span class="sxs-lookup"><span data-stu-id="eef9a-187">Subtype</span></span></th>
<th><span data-ttu-id="eef9a-188">Описание</span><span class="sxs-lookup"><span data-stu-id="eef9a-188">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eef9a-189"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="eef9a-189"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="eef9a-190">Звук IEEE с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="eef9a-190">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eef9a-191"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="eef9a-191"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="eef9a-192">16-разрядный звук PCM.</span><span class="sxs-lookup"><span data-stu-id="eef9a-192">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eef9a-193"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="eef9a-193"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="eef9a-194">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eef9a-194">Requires Windows 8.</span></span> <br/> <span data-ttu-id="eef9a-195">Этот тип выходных данных можно использовать для преобразования потока AAC в формате УРОВНЯМИ гарантии/ЛАТМ в формат ADTS.</span><span class="sxs-lookup"><span data-stu-id="eef9a-195">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="eef9a-196">Чтобы преобразовать поток УРОВНЯМИ гарантии/ЛАТМ в поток ADTS, задайте тип входных данных <strong>MFAudioFormat_AAC</strong> с типом полезных данных 3 (уровнями гарантии).</span><span class="sxs-lookup"><span data-stu-id="eef9a-196">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="eef9a-197">Затем задайте тип выходных данных <strong>MFAudioFormat_AAC</strong> с типом полезных данных 1 (ADTS).</span><span class="sxs-lookup"><span data-stu-id="eef9a-197">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="eef9a-198">Декодер будет переформатировать конаинтер без декодирования битовый поток.</span><span class="sxs-lookup"><span data-stu-id="eef9a-198">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eef9a-199">Декодер не регистрирует <strong>MFAudioFormat_AAC</strong> как тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="eef9a-199">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="eef9a-200">Однако если приложение задает тип входных данных, как описано, метод <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>имфтрансформ:: жетаутпутаваилаблетипе</strong></a> возвращает <strong>MFAudioFormat_AAC</strong> в списке доступных типов вывода.</span><span class="sxs-lookup"><span data-stu-id="eef9a-200">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="eef9a-201">Если входной поток содержит более двух каналов, декодер AAC предоставляет два варианта выходного формата:</span><span class="sxs-lookup"><span data-stu-id="eef9a-201">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="eef9a-202">Та же конфигурация канала, что и у входного типа.</span><span class="sxs-lookup"><span data-stu-id="eef9a-202">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="eef9a-203">Переход на стереосистему.</span><span class="sxs-lookup"><span data-stu-id="eef9a-203">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="eef9a-204">Ограничения формата</span><span class="sxs-lookup"><span data-stu-id="eef9a-204">Format Constraints</span></span>

<span data-ttu-id="eef9a-205">Декодированная частота выборки звука должна быть одной из следующих: после применения SBR (при наличии).</span><span class="sxs-lookup"><span data-stu-id="eef9a-205">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="eef9a-206">8 кГц</span><span class="sxs-lookup"><span data-stu-id="eef9a-206">8 kHz</span></span>
-   <span data-ttu-id="eef9a-207">11,025 кГц</span><span class="sxs-lookup"><span data-stu-id="eef9a-207">11.025 kHz</span></span>
-   <span data-ttu-id="eef9a-208">12 кГц</span><span class="sxs-lookup"><span data-stu-id="eef9a-208">12 kHz</span></span>
-   <span data-ttu-id="eef9a-209">16 кГц</span><span class="sxs-lookup"><span data-stu-id="eef9a-209">16 kHz</span></span>
-   <span data-ttu-id="eef9a-210">22,05 кГц</span><span class="sxs-lookup"><span data-stu-id="eef9a-210">22.05 kHz</span></span>
-   <span data-ttu-id="eef9a-211">24 кГц</span><span class="sxs-lookup"><span data-stu-id="eef9a-211">24 kHz</span></span>
-   <span data-ttu-id="eef9a-212">32 кГц</span><span class="sxs-lookup"><span data-stu-id="eef9a-212">32 kHz</span></span>
-   <span data-ttu-id="eef9a-213">44,1 кГц</span><span class="sxs-lookup"><span data-stu-id="eef9a-213">44.1 kHz</span></span>
-   <span data-ttu-id="eef9a-214">48 кГц</span><span class="sxs-lookup"><span data-stu-id="eef9a-214">48 kHz</span></span>

<span data-ttu-id="eef9a-215">Частоты выборки выше 48 кГц не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="eef9a-215">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="eef9a-216">Декодер поддерживает до 6 каналов звука.</span><span class="sxs-lookup"><span data-stu-id="eef9a-216">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="eef9a-217">Для каждой конфигурации динамика декодер ожидает, чтобы AAC синтаксические элементы отображались в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="eef9a-217">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="eef9a-218">В следующей таблице перечислены поддерживаемые конфигурации динамиков.</span><span class="sxs-lookup"><span data-stu-id="eef9a-218">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="eef9a-219">В третьем столбце таблицы перечислены ожидаемые синтаксические элементы и их порядок, используя следующую нотацию:</span><span class="sxs-lookup"><span data-stu-id="eef9a-219">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="eef9a-220"><SCE1>: Single_channel_element (SCE), связанный с динамиком переднего плана.</span><span class="sxs-lookup"><span data-stu-id="eef9a-220"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="eef9a-221"><SCE2>: SCE, связанный с докладчиком центра.</span><span class="sxs-lookup"><span data-stu-id="eef9a-221"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="eef9a-222"><CPE1>: Channel_pair_element (CPE), связанный с передними динамиками.</span><span class="sxs-lookup"><span data-stu-id="eef9a-222"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="eef9a-223"><CPE2>: CPE, связанный с задними (или боковыми) динамиками</span><span class="sxs-lookup"><span data-stu-id="eef9a-223"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="eef9a-224"><LFE>: Lfe_channel_element (НИЗКОЧАСТОТный).</span><span class="sxs-lookup"><span data-stu-id="eef9a-224"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="eef9a-225">Дополнительные сведения об этих синтаксических элементах см. в статье ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="eef9a-225">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="eef9a-226">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="eef9a-226">Configuration</span></span>       | <span data-ttu-id="eef9a-227">Маска канала</span><span class="sxs-lookup"><span data-stu-id="eef9a-227">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="eef9a-228">AAC синтаксические элементы</span><span class="sxs-lookup"><span data-stu-id="eef9a-228">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="eef9a-229">Mono</span><span class="sxs-lookup"><span data-stu-id="eef9a-229">Mono</span></span>                | <span data-ttu-id="eef9a-230">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="eef9a-230">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="eef9a-231">Стерео или Dual Mono</span><span class="sxs-lookup"><span data-stu-id="eef9a-231">Stereo or dual mono</span></span> | <span data-ttu-id="eef9a-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="eef9a-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="eef9a-233">2/1</span><span class="sxs-lookup"><span data-stu-id="eef9a-233">2/1</span></span>                 | <span data-ttu-id="eef9a-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="eef9a-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="eef9a-235">2/2</span><span class="sxs-lookup"><span data-stu-id="eef9a-235">2/2</span></span>                 | <span data-ttu-id="eef9a-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="eef9a-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="eef9a-237">3/0</span><span class="sxs-lookup"><span data-stu-id="eef9a-237">3/0</span></span>                 | <span data-ttu-id="eef9a-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="eef9a-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="eef9a-239">3/1</span><span class="sxs-lookup"><span data-stu-id="eef9a-239">3/1</span></span>                 | <span data-ttu-id="eef9a-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="eef9a-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="eef9a-241">3/2</span><span class="sxs-lookup"><span data-stu-id="eef9a-241">3/2</span></span>                 | <span data-ttu-id="eef9a-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="eef9a-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="eef9a-243">3/2 + НИЗКОЧАСТОТНЫЙ</span><span class="sxs-lookup"><span data-stu-id="eef9a-243">3/2 + LFE</span></span>           | <span data-ttu-id="eef9a-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="eef9a-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="eef9a-245">Для необработанных AAC каждый входной пример должен содержать ровно один полный сжатый кадр AAC.</span><span class="sxs-lookup"><span data-stu-id="eef9a-245">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="eef9a-246">Для ADTS каждый входной образец может содержать несколько звуковых кадров, а также частичные кадры, т. е. фреймы могут охватывать границы выборки.</span><span class="sxs-lookup"><span data-stu-id="eef9a-246">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="eef9a-247">За каждым заголовком ADTS должен следовать один кадр AAC.</span><span class="sxs-lookup"><span data-stu-id="eef9a-247">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="eef9a-248">Декодер AAC не поддерживает следующие действия:</span><span class="sxs-lookup"><span data-stu-id="eef9a-248">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="eef9a-249">Основной профиль, Sample-Rate масштабируемый профиль (SRS) или профиль долгосрочного прогноза (ЛТП).</span><span class="sxs-lookup"><span data-stu-id="eef9a-249">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="eef9a-250">Формат обмена звуковых данных (АДИФ).</span><span class="sxs-lookup"><span data-stu-id="eef9a-250">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="eef9a-251">Транспортные потоки ЛАТМ/Лаос.</span><span class="sxs-lookup"><span data-stu-id="eef9a-251">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="eef9a-252">Элементы сопряженного канала (Кцес).</span><span class="sxs-lookup"><span data-stu-id="eef9a-252">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="eef9a-253">Декодер пропустит звуковые кадры с помощью Кцес.</span><span class="sxs-lookup"><span data-stu-id="eef9a-253">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="eef9a-254">AAC-LC с 960-примерным размером кадра.</span><span class="sxs-lookup"><span data-stu-id="eef9a-254">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="eef9a-255">Поддерживаются только 1024-образцы кадров.</span><span class="sxs-lookup"><span data-stu-id="eef9a-255">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="eef9a-256">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="eef9a-256">Transform Attributes</span></span>

<span data-ttu-id="eef9a-257">Декодер AAC реализует метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="eef9a-257">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="eef9a-258">Приложения могут использовать этот метод для получения или установки следующих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="eef9a-258">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eef9a-259">attribute</span><span class="sxs-lookup"><span data-stu-id="eef9a-259">Attribute</span></span></th>
<th><span data-ttu-id="eef9a-260">Описание</span><span class="sxs-lookup"><span data-stu-id="eef9a-260">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eef9a-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-262">Указывает, кодируется ли двухканальный аудио-канал как стерео или два Mono.</span><span class="sxs-lookup"><span data-stu-id="eef9a-262">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="eef9a-263">Рассматривать как доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eef9a-263">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eef9a-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-265">Указывает, как декодер воспроизводит два моно аудио.</span><span class="sxs-lookup"><span data-stu-id="eef9a-265">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="eef9a-266">Значение по умолчанию — <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: output CH1 для левого и правого докладчика.</span><span class="sxs-lookup"><span data-stu-id="eef9a-266">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="eef9a-267">Приложения могут установить это свойство, чтобы изменить поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eef9a-267">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eef9a-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eef9a-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="eef9a-269">Декодер AAC не обрабатывает изменения динамического формата и должен быть сброшен или очищен до установки нового типа входного носителя.</span><span class="sxs-lookup"><span data-stu-id="eef9a-269">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="eef9a-270">Рассматривайте этот атрибут как доступный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eef9a-270">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eef9a-271">Декодер AAC неправильно сообщает значение <strong>true</strong> для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="eef9a-271">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="eef9a-272">В Windows 7 декодер неправильно сообщает значение <strong>true</strong> для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="eef9a-272">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="eef9a-273">В Windows 8 декодер сообщает <strong>false</strong>, что является правильным значением</span><span class="sxs-lookup"><span data-stu-id="eef9a-273">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="eef9a-274">Примеры типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="eef9a-274">Example Media Types</span></span>

<span data-ttu-id="eef9a-275">Ниже приведен пример типа входного носителя, необходимого для потока AAC-LC с 6 каналами, 48 кГц, с использованием необработанных полезных данных AAC:</span><span class="sxs-lookup"><span data-stu-id="eef9a-275">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="eef9a-276">attribute</span><span class="sxs-lookup"><span data-stu-id="eef9a-276">Attribute</span></span>                                                                                      | <span data-ttu-id="eef9a-277">Значение</span><span class="sxs-lookup"><span data-stu-id="eef9a-277">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="eef9a-278">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="eef9a-278">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="eef9a-279">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="eef9a-279">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="eef9a-280">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="eef9a-280">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="eef9a-281">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="eef9a-281">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="eef9a-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="eef9a-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="eef9a-283">48000</span><span class="sxs-lookup"><span data-stu-id="eef9a-283">48000</span></span>                                                                                |
| [<span data-ttu-id="eef9a-284">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="eef9a-284">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="eef9a-285">6</span><span class="sxs-lookup"><span data-stu-id="eef9a-285">6</span></span>                                                                                    |
| [<span data-ttu-id="eef9a-286">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="eef9a-286">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="eef9a-287">0</span><span class="sxs-lookup"><span data-stu-id="eef9a-287">0</span></span>                                                                                    |
| [<span data-ttu-id="eef9a-288">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="eef9a-288">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="eef9a-289">{0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span><span class="sxs-lookup"><span data-stu-id="eef9a-289">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="eef9a-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="eef9a-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="eef9a-291">0x2A (необязательно)</span><span class="sxs-lookup"><span data-stu-id="eef9a-291">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="eef9a-292">Первые 12 байт [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) соответствуют следующим элементам структуры [**хеааквавеинфо**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) :</span><span class="sxs-lookup"><span data-stu-id="eef9a-292">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="eef9a-293">**впайлоадтипе** = 0 (необработанный AAC)</span><span class="sxs-lookup"><span data-stu-id="eef9a-293">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="eef9a-294">**ваудиопрофилелевелиндикатион** = 0X2a (профиль AAC, уровень 4)</span><span class="sxs-lookup"><span data-stu-id="eef9a-294">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="eef9a-295">**вструкттипе** = 0</span><span class="sxs-lookup"><span data-stu-id="eef9a-295">**wStructType** = 0</span></span>

<span data-ttu-id="eef9a-296">Последние два байта [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) содержат значение аудиоспеЦификконфиг () в соответствии с определением MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="eef9a-296">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="eef9a-297">АудиоспеЦификконфиг. Аудиубжекттипе = 2 (AAC LC) (5 бит)</span><span class="sxs-lookup"><span data-stu-id="eef9a-297">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="eef9a-298">АудиоспеЦификконфиг. Самплингфрекуенцииндекс = 3 (4 бита)</span><span class="sxs-lookup"><span data-stu-id="eef9a-298">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="eef9a-299">АудиоспеЦификконфиг. Чаннелконфигуратион = 6 (4 бита)</span><span class="sxs-lookup"><span data-stu-id="eef9a-299">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="eef9a-300">ГаспеЦификконфиг. Фрамеленгсфлаг = 0 (1 бит)</span><span class="sxs-lookup"><span data-stu-id="eef9a-300">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="eef9a-301">ГаспеЦификконфиг. Депендсонкорекодер = 0 (1 бит)</span><span class="sxs-lookup"><span data-stu-id="eef9a-301">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="eef9a-302">ГаспеЦификконфиг. Екстенсионфлаг = 0 (1 бит)</span><span class="sxs-lookup"><span data-stu-id="eef9a-302">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="eef9a-303">Учитывая этот тип входных данных, используйте следующий тип выходного носителя для получения 6-канального звука PCM с плавающей запятой, 32-битного из декодера:</span><span class="sxs-lookup"><span data-stu-id="eef9a-303">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="eef9a-304">attribute</span><span class="sxs-lookup"><span data-stu-id="eef9a-304">Attribute</span></span>                                                                                    | <span data-ttu-id="eef9a-305">Значение</span><span class="sxs-lookup"><span data-stu-id="eef9a-305">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="eef9a-306">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="eef9a-306">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="eef9a-307">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="eef9a-307">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="eef9a-308">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="eef9a-308">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="eef9a-309">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="eef9a-309">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="eef9a-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="eef9a-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="eef9a-311">32</span><span class="sxs-lookup"><span data-stu-id="eef9a-311">32</span></span>                       |
| [<span data-ttu-id="eef9a-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="eef9a-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="eef9a-313">48000</span><span class="sxs-lookup"><span data-stu-id="eef9a-313">48000</span></span>                    |
| [<span data-ttu-id="eef9a-314">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="eef9a-314">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="eef9a-315">6</span><span class="sxs-lookup"><span data-stu-id="eef9a-315">6</span></span>                        |
| [<span data-ttu-id="eef9a-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="eef9a-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="eef9a-317">1152000 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="eef9a-317">1152000 (optional)</span></span>       |
| [<span data-ttu-id="eef9a-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="eef9a-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="eef9a-319">24 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="eef9a-319">24 (optional)</span></span>            |
| [<span data-ttu-id="eef9a-320">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="eef9a-320">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="eef9a-321">0x3F (необязательно)</span><span class="sxs-lookup"><span data-stu-id="eef9a-321">0x3f (optional)</span></span>          |



 

<span data-ttu-id="eef9a-322">Если установлена поддержка обновления платформы для Windows Vista, то декодер AAC Audio доступен в Windows Vista, но доступен только в Windows Vista с помощью [средства чтения исходного кода](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="eef9a-322">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eef9a-323">Требования</span><span class="sxs-lookup"><span data-stu-id="eef9a-323">Requirements</span></span>



| <span data-ttu-id="eef9a-324">Требование</span><span class="sxs-lookup"><span data-stu-id="eef9a-324">Requirement</span></span> | <span data-ttu-id="eef9a-325">Значение</span><span class="sxs-lookup"><span data-stu-id="eef9a-325">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef9a-326">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eef9a-326">Minimum supported client</span></span><br/> | <span data-ttu-id="eef9a-327">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eef9a-327">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="eef9a-328">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eef9a-328">Minimum supported server</span></span><br/> | <span data-ttu-id="eef9a-329">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eef9a-329">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="eef9a-330">DLL</span><span class="sxs-lookup"><span data-stu-id="eef9a-330">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eef9a-331"><dt>Msmpeg2adec.dll в Windows 7; </dt> <dt>MSAudDecMFT.dll в Windows 8</dt></span><span class="sxs-lookup"><span data-stu-id="eef9a-331"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef9a-332">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eef9a-332">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef9a-333">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="eef9a-333">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="eef9a-334">Типы носителей AAC</span><span class="sxs-lookup"><span data-stu-id="eef9a-334">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="eef9a-335">Типы звуковых носителей</span><span class="sxs-lookup"><span data-stu-id="eef9a-335">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="eef9a-336">**Декодер звука Microsoft MPEG-1/DD/AAC**</span><span class="sxs-lookup"><span data-stu-id="eef9a-336">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="eef9a-337">Поддержка MPEG-4 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eef9a-337">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="eef9a-338">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eef9a-338">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
