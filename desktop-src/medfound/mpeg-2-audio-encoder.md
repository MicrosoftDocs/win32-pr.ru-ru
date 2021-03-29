---
description: Microsoft Media Foundation кодировщик MPEG-2 — это Media Foundation преобразование, которое кодирует моно или стерео аудио в MPEG-1 Audio (ISO/IEC 11172-3) или MPEG-2 Audio (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Кодировщик MPEG-2 Audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898190"
---
# <a name="mpeg-2-audio-encoder"></a><span data-ttu-id="86e25-103">Кодировщик MPEG-2 Audio</span><span class="sxs-lookup"><span data-stu-id="86e25-103">MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="86e25-104">Microsoft Media Foundation кодировщик MPEG-2 — это [Media Foundation преобразование](media-foundation-transforms.md) , которое кодирует моно или стерео аудио в MPEG-1 Audio (ISO/IEC 11172-3) или MPEG-2 Audio (ISO/IEC 13818-3).</span><span class="sxs-lookup"><span data-stu-id="86e25-104">The Microsoft Media Foundation MPEG-2 audio encoder is a [Media Foundation transform](media-foundation-transforms.md) that encodes mono or stereo audio to MPEG-1 audio (ISO/IEC 11172-3) or MPEG-2 audio (ISO/IEC 13818-3).</span></span>

<span data-ttu-id="86e25-105">Кодировщик поддерживает звук уровня 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="86e25-105">The encoder supports Layer 1 and Layer 2 audio.</span></span> <span data-ttu-id="86e25-106">Он не поддерживает MPEG-Layer 3 (MP3) Audio.</span><span class="sxs-lookup"><span data-stu-id="86e25-106">It does not support MPEG-Layer 3 (MP3) audio.</span></span> <span data-ttu-id="86e25-107">Для MPEG-2 кодировщик поддерживает часть частоты дискретизации (LSF) звука MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="86e25-107">For MPEG-2, the encoder supports the Low Sampling Frequencies (LSF) portion of MPEG-2 audio.</span></span> <span data-ttu-id="86e25-108">Он не поддерживает многоканальные расширения.</span><span class="sxs-lookup"><span data-stu-id="86e25-108">It does not support the multichannel extensions.</span></span> <span data-ttu-id="86e25-109">В MFT выводится простейший поток MPEG.</span><span class="sxs-lookup"><span data-stu-id="86e25-109">The MFT outputs an MPEG elementary stream.</span></span> <span data-ttu-id="86e25-110">Он не может создавать пакетные элементарные потоки, потоки программы или потоки транспорта.</span><span class="sxs-lookup"><span data-stu-id="86e25-110">It cannot generate packetized elementary streams, program streams, or transport streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="86e25-111">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="86e25-111">Class Identifier</span></span>

<span data-ttu-id="86e25-112">Идентификатор класса (CLSID) кодировщика МЕПГ-2 — это **CLSID \_ CMPEG2AudioEncoderMFT**, определенный в файле заголовка вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="86e25-112">The class identifier (CLSID) of the MEPG-2 audio encoder is **CLSID\_CMPEG2AudioEncoderMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="86e25-113">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="86e25-113">Output Types</span></span>

<span data-ttu-id="86e25-114">Тип выходных данных должен быть задан первым, перед входным типом.</span><span class="sxs-lookup"><span data-stu-id="86e25-114">The output type must be set first, before the input type.</span></span> <span data-ttu-id="86e25-115">В следующей таблице перечислены обязательные и необязательные атрибуты для выходного типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="86e25-115">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86e25-116">attribute</span><span class="sxs-lookup"><span data-stu-id="86e25-116">Attribute</span></span></th>
<th><span data-ttu-id="86e25-117">Описание</span><span class="sxs-lookup"><span data-stu-id="86e25-117">Description</span></span></th>
<th><span data-ttu-id="86e25-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="86e25-118">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86e25-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="86e25-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="86e25-120">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="86e25-120">Major type.</span></span></td>
<td><span data-ttu-id="86e25-121">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-121">Required.</span></span> <span data-ttu-id="86e25-122">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="86e25-122">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86e25-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="86e25-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="86e25-124">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="86e25-124">Audio subtype.</span></span></td>
<td><span data-ttu-id="86e25-125">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-125">Required.</span></span> <span data-ttu-id="86e25-126">Необходимо <strong>MFAudioFormat_MPEG</strong>.</span><span class="sxs-lookup"><span data-stu-id="86e25-126">Must be <strong>MFAudioFormat_MPEG</strong>.</span></span> <span data-ttu-id="86e25-127">Этот подтип используется как для MPEG-1, так и для звука MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="86e25-127">This subtype is used for both MPEG-1 and MPEG-2 audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86e25-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="86e25-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="86e25-129">Выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="86e25-129">Samples per second.</span></span></td>
<td><span data-ttu-id="86e25-130">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-130">Required.</span></span> <span data-ttu-id="86e25-131">Для MPEG-1 и MPEG-2 поддерживаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="86e25-131">The following values are supported for both MPEG-1 and MPEG-2:</span></span>
<ul>
<li><span data-ttu-id="86e25-132">32000</span><span class="sxs-lookup"><span data-stu-id="86e25-132">32000</span></span></li>
<li><span data-ttu-id="86e25-133">44100</span><span class="sxs-lookup"><span data-stu-id="86e25-133">44100</span></span></li>
<li><span data-ttu-id="86e25-134">48000</span><span class="sxs-lookup"><span data-stu-id="86e25-134">48000</span></span></li>
</ul>
<span data-ttu-id="86e25-135">Кроме того, для MPEG-2 LSF поддерживаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="86e25-135">In addition, the following values are supported for MPEG-2 LSF:</span></span> <br/>
<ul>
<li><span data-ttu-id="86e25-136">16000</span><span class="sxs-lookup"><span data-stu-id="86e25-136">16000</span></span></li>
<li><span data-ttu-id="86e25-137">22050</span><span class="sxs-lookup"><span data-stu-id="86e25-137">22050</span></span></li>
<li><span data-ttu-id="86e25-138">24 000</span><span class="sxs-lookup"><span data-stu-id="86e25-138">24000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86e25-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="86e25-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="86e25-140">Число каналов.</span><span class="sxs-lookup"><span data-stu-id="86e25-140">Number of channels.</span></span></td>
<td><span data-ttu-id="86e25-141">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-141">Required.</span></span> <span data-ttu-id="86e25-142">Значение должно быть либо 1 (моно), либо 2 (стерео).</span><span class="sxs-lookup"><span data-stu-id="86e25-142">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86e25-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="86e25-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="86e25-144">Указывает назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="86e25-144">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="86e25-145">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="86e25-145">Optional.</span></span> <span data-ttu-id="86e25-146">Если задано, значение должно быть 0x3ым для стерео (передний левый и правый каналы) или 0x4 для Mono (канал Front Center).</span><span class="sxs-lookup"><span data-stu-id="86e25-146">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86e25-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="86e25-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="86e25-148">Скорость потока закодированных потоков MPEG (в байтах в секунду).</span><span class="sxs-lookup"><span data-stu-id="86e25-148">Bit rate of the encoded MPEG stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="86e25-149">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="86e25-149">Optional.</span></span><br/> <span data-ttu-id="86e25-150">Спецификации ISO/IEC 11172-3 и ISO/IEC 13818-3 (LSF) определяют несколько битовых ставок в зависимости от частоты выборки, количества каналов и звукового уровня (1 или 2).</span><span class="sxs-lookup"><span data-stu-id="86e25-150">The ISO/IEC 11172-3 and ISO/IEC 13818-3 (LSF) specifications define several bit rates, depending on the sampling rate, the number of channels, and the audio layer (1 or 2).</span></span> <br/> <span data-ttu-id="86e25-151">Кодировщик по умолчанию имеет звук уровня 2.</span><span class="sxs-lookup"><span data-stu-id="86e25-151">The encoder defaults to Layer 2 audio.</span></span> <span data-ttu-id="86e25-152">Если атрибут <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> не задан, кодировщик использует следующие скорости по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="86e25-152">If the <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> attribute is not set, the encoder uses the following default bit rates:</span></span><br/>
<ul>
<li><span data-ttu-id="86e25-153">Стерео MPEG-1 стереосистема: 224 000 бит/с в секунду (бит/с) = 28 000 байт в секунду.</span><span class="sxs-lookup"><span data-stu-id="86e25-153">MPEG-1 stereo: 224,000 bits per second (bps) = 28,000 bytes per second.</span></span></li>
<li><span data-ttu-id="86e25-154">MPEG-1 моно: 192 000 бит/с = 24 000 байт в секунду.</span><span class="sxs-lookup"><span data-stu-id="86e25-154">MPEG-1 mono: 192,000 bps = 24,000 bytes per second.</span></span></li>
<li><span data-ttu-id="86e25-155">MPEG-2 LSF, моно или стерео: 160 000 бит/с = 20 000 байт в секунду.</span><span class="sxs-lookup"><span data-stu-id="86e25-155">MPEG-2 LSF, mono or stereo: 160,000 bps = 20,000 bytes per second.</span></span></li>
</ul>
<span data-ttu-id="86e25-156">Для этого атрибута можно задать другие значения.</span><span class="sxs-lookup"><span data-stu-id="86e25-156">This attribute can be set to other values.</span></span> <span data-ttu-id="86e25-157">Если значение не является допустимым согласно спецификациям MPEG, то этот тип мультимедиа будет отклонен.</span><span class="sxs-lookup"><span data-stu-id="86e25-157">If the value is not valid according to MPEG specifications, the MFT will reject the media type.</span></span><br/> <span data-ttu-id="86e25-158">Можно также задать скорость передачи данных с помощью интерфейса <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>икодекапи</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="86e25-158">You can also set the bit rate by using the <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> interface.</span></span> <span data-ttu-id="86e25-159">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="86e25-159">See Remarks for more information.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="86e25-160">Если необязательные атрибуты не заданы, кодировщик добавляет их в тип мультимедиа после задания типа.</span><span class="sxs-lookup"><span data-stu-id="86e25-160">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="86e25-161">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="86e25-161">Input Types</span></span>

<span data-ttu-id="86e25-162">В следующей таблице перечислены обязательные и необязательные атрибуты для входного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="86e25-162">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86e25-163">attribute</span><span class="sxs-lookup"><span data-stu-id="86e25-163">Attribute</span></span></th>
<th><span data-ttu-id="86e25-164">Описание</span><span class="sxs-lookup"><span data-stu-id="86e25-164">Description</span></span></th>
<th><span data-ttu-id="86e25-165">Remarks</span><span class="sxs-lookup"><span data-stu-id="86e25-165">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86e25-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="86e25-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="86e25-167">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="86e25-167">Major type.</span></span></td>
<td><span data-ttu-id="86e25-168">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-168">Required.</span></span> <span data-ttu-id="86e25-169">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="86e25-169">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86e25-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="86e25-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="86e25-171">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="86e25-171">Audio subtype.</span></span></td>
<td><span data-ttu-id="86e25-172">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-172">Required.</span></span> <span data-ttu-id="86e25-173">Должен быть <strong>MFAudioFormat_PCM</strong> или <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="86e25-173">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86e25-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="86e25-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="86e25-175">Число битов на аудио выборка.</span><span class="sxs-lookup"><span data-stu-id="86e25-175">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="86e25-176">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-176">Required.</span></span> <span data-ttu-id="86e25-177">Значение должно быть 16, если подтип имеет <strong>MFAudioFormat_PCM</strong>, или 32, если подтип имеет <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="86e25-177">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86e25-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="86e25-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="86e25-179">Выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="86e25-179">Samples per second.</span></span></td>
<td><span data-ttu-id="86e25-180">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-180">Required.</span></span> <span data-ttu-id="86e25-181">Должен соответствовать типу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="86e25-181">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86e25-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="86e25-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="86e25-183">Число каналов.</span><span class="sxs-lookup"><span data-stu-id="86e25-183">Number of channels.</span></span></td>
<td><span data-ttu-id="86e25-184">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-184">Required.</span></span> <span data-ttu-id="86e25-185">Должен соответствовать типу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="86e25-185">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86e25-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="86e25-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="86e25-187">Выравнивание блокировки в байтах.</span><span class="sxs-lookup"><span data-stu-id="86e25-187">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="86e25-188">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-188">Required.</span></span> <span data-ttu-id="86e25-189">Вычислите значение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="86e25-189">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="86e25-190"><strong>MFAudioFormat_PCM</strong>: число каналов × 2.</span><span class="sxs-lookup"><span data-stu-id="86e25-190"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="86e25-191"><strong>MFAudioFormat_Float</strong>: число каналов × 4.</span><span class="sxs-lookup"><span data-stu-id="86e25-191"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86e25-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="86e25-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="86e25-193">Битовая скорость закодированного потока AC3 в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="86e25-193">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="86e25-194">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="86e25-194">Required.</span></span> <span data-ttu-id="86e25-195">Должно равняться выравниванию блока × Samples в секунду.</span><span class="sxs-lookup"><span data-stu-id="86e25-195">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86e25-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="86e25-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="86e25-197">Указывает назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="86e25-197">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="86e25-198">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="86e25-198">Optional.</span></span> <span data-ttu-id="86e25-199">Если параметр задан, значение должно соответствовать типу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="86e25-199">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86e25-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="86e25-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="86e25-201">Количество допустимых битов звуковых данных в каждом звуковом примере.</span><span class="sxs-lookup"><span data-stu-id="86e25-201">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="86e25-202">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="86e25-202">Optional.</span></span> <span data-ttu-id="86e25-203">Если значение задано, оно должно быть идентично значению <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="86e25-203">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="86e25-204">Кодировщик не поддерживает преобразование "выборка" или "стерео/моно".</span><span class="sxs-lookup"><span data-stu-id="86e25-204">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span> <span data-ttu-id="86e25-205">Если необязательные атрибуты не заданы, кодировщик добавляет их в тип мультимедиа после задания типа.</span><span class="sxs-lookup"><span data-stu-id="86e25-205">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="86e25-206">Свойства кодека</span><span class="sxs-lookup"><span data-stu-id="86e25-206">Codec Properties</span></span>

<span data-ttu-id="86e25-207">Кодировщик поддерживает следующие свойства через интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="86e25-207">The encoder supports the following properties through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>



| <span data-ttu-id="86e25-208">Свойство</span><span class="sxs-lookup"><span data-stu-id="86e25-208">Property</span></span>                                                                                | <span data-ttu-id="86e25-209">Описание</span><span class="sxs-lookup"><span data-stu-id="86e25-209">Description</span></span>                                                                                      | <span data-ttu-id="86e25-210">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="86e25-210">Default value</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86e25-211">КОДЕКАПИ \_ авенккоммонмеанбитрате</span><span class="sxs-lookup"><span data-stu-id="86e25-211">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)               | <span data-ttu-id="86e25-212">Указывает среднюю скорость кодирования в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="86e25-212">Specifies the average encoded bit rate, in bits per second.</span></span>                                      | <span data-ttu-id="86e25-213">Как описано в атрибуте [ \_ среднего числа байт в \_ \_ \_ \_ \_ секунду MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) на выходном носителе, введите.</span><span class="sxs-lookup"><span data-stu-id="86e25-213">As described for the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output media type.</span></span>                      |
| [<span data-ttu-id="86e25-214">КОДЕКАПИ \_ авенкмпакодингмоде</span><span class="sxs-lookup"><span data-stu-id="86e25-214">CODECAPI\_AVEncMPACodingMode</span></span>](../directshow/avencmpacodingmode-property.md)                       | <span data-ttu-id="86e25-215">Указывает режим кодирования звука MPEG.</span><span class="sxs-lookup"><span data-stu-id="86e25-215">Specifies the MPEG audio encoding mode.</span></span>                                                          | <span data-ttu-id="86e25-216">Стерео для двухканального аудио-канала или одного канала для каналов с одним каналом.</span><span class="sxs-lookup"><span data-stu-id="86e25-216">Stereo for 2-channel audio, or single channel for 1-channel audio.</span></span><br/> <span data-ttu-id="86e25-217">Для высококанального звука кодировщик также поддерживает двухканальный и совместный стерео.</span><span class="sxs-lookup"><span data-stu-id="86e25-217">For 2-channel audio, the encoder also supports dual channel and joint stereo.</span></span><br/> |
| [<span data-ttu-id="86e25-218">КОДЕКАПИ \_ авенкмпакопиригхт</span><span class="sxs-lookup"><span data-stu-id="86e25-218">CODECAPI\_AVEncMPACopyright</span></span>](../directshow/avencmpacopyright-property.md)                         | <span data-ttu-id="86e25-219">Указывает, следует ли задать бит авторского права в потоке MPEG.</span><span class="sxs-lookup"><span data-stu-id="86e25-219">Specifies whether to set the copyright bit in the MPEG audio stream.</span></span>                             | <span data-ttu-id="86e25-220">Нет авторских прав.</span><span class="sxs-lookup"><span data-stu-id="86e25-220">No copyright.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="86e25-221">КОДЕКАПИ \_ авенкмпаемфасистипе</span><span class="sxs-lookup"><span data-stu-id="86e25-221">CODECAPI\_AVEncMPAEmphasisType</span></span>](../directshow/avencmpaemphasistype-property.md)                   | <span data-ttu-id="86e25-222">Указывает тип фильтра отмены выделения, который должен использоваться при декодировании закодированного потока.</span><span class="sxs-lookup"><span data-stu-id="86e25-222">Specifies the type of de-emphasis filter that should be used when the encoded stream is decoded.</span></span> | <span data-ttu-id="86e25-223">Не указано выделение.</span><span class="sxs-lookup"><span data-stu-id="86e25-223">No emphasis specified.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="86e25-224">авенкмпаенаблередунданципротектион</span><span class="sxs-lookup"><span data-stu-id="86e25-224">AVEncMPAEnableRedundancyProtection</span></span>](../directshow/avencmpaenableredundancyprotection-property.md) | <span data-ttu-id="86e25-225">Указывает, следует ли добавить в заголовок кадра циклическую проверку избыточности (CRC).</span><span class="sxs-lookup"><span data-stu-id="86e25-225">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span>                    | <span data-ttu-id="86e25-226">Контрольная сумма CRC записывается в поток битов.</span><span class="sxs-lookup"><span data-stu-id="86e25-226">A CRC checksum is written to the bit stream.</span></span>                                                                                                                           |
| [<span data-ttu-id="86e25-227">КОДЕКАПИ \_ авенкмпалайер</span><span class="sxs-lookup"><span data-stu-id="86e25-227">CODECAPI\_AVEncMPALayer</span></span>](../directshow/avencmpalayer-property.md)                                 | <span data-ttu-id="86e25-228">Задает звуковой слой MPEG.</span><span class="sxs-lookup"><span data-stu-id="86e25-228">Specifies the MPEG audio layer.</span></span>                                                                  | <span data-ttu-id="86e25-229">Звук уровня 2.</span><span class="sxs-lookup"><span data-stu-id="86e25-229">Layer 2 audio.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="86e25-230">КОДЕКАПИ \_ авенкмпаоригиналбитстреам</span><span class="sxs-lookup"><span data-stu-id="86e25-230">CODECAPI\_AVEncMPAOriginalBitstream</span></span>](../directshow/avencmpaoriginalbitstream-property.md)         | <span data-ttu-id="86e25-231">Указывает, следует ли устанавливать для исходного бита в потоке MPEG.</span><span class="sxs-lookup"><span data-stu-id="86e25-231">Specifies whether to set for the original bit in the MPEG audio stream.</span></span>                          | <span data-ttu-id="86e25-232">"Исходный" бит отключен.</span><span class="sxs-lookup"><span data-stu-id="86e25-232">"Original" bit is off.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="86e25-233">КОДЕКАПИ \_ авенкмпаприватеусербит</span><span class="sxs-lookup"><span data-stu-id="86e25-233">CODECAPI\_AVEncMPAPrivateUserBit</span></span>](../directshow/avencmpaprivateuserbit-property.md)               | <span data-ttu-id="86e25-234">Указывает, следует ли задавать значение для закрытого бита пользователя в потоке MPEG Audio.</span><span class="sxs-lookup"><span data-stu-id="86e25-234">Specifies whether to set for the private user bit in the MPEG audio stream.</span></span>                      | <span data-ttu-id="86e25-235">Закрытый бит пользователя отключен.</span><span class="sxs-lookup"><span data-stu-id="86e25-235">Private user bit is off.</span></span>                                                                                                                                               |



 

<span data-ttu-id="86e25-236">Чтобы получить указатель на интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) , вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в MFT.</span><span class="sxs-lookup"><span data-stu-id="86e25-236">To get a pointer to the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the MFT.</span></span>

<span data-ttu-id="86e25-237">MFT реализует следующие методы [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="86e25-237">The MFT implements the following [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods:</span></span>

-   [<span data-ttu-id="86e25-238">**жетпараметерранже**</span><span class="sxs-lookup"><span data-stu-id="86e25-238">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="86e25-239">**жетпараметервалуес**</span><span class="sxs-lookup"><span data-stu-id="86e25-239">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [<span data-ttu-id="86e25-240">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="86e25-240">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="86e25-241">**Изменяемый**</span><span class="sxs-lookup"><span data-stu-id="86e25-241">**IsModifiable**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [<span data-ttu-id="86e25-242">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="86e25-242">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="86e25-243">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="86e25-243">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

<span data-ttu-id="86e25-244">Все остальные методы [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) возвращают **E \_ нотимпл**.</span><span class="sxs-lookup"><span data-stu-id="86e25-244">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods return **E\_NOTIMPL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e25-245">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86e25-245">Remarks</span></span>

<span data-ttu-id="86e25-246">Каждая звуковая рамка MPEG содержит как 384 (уровень 1), так и 1152 (уровень 2) аудио выборки на канал.</span><span class="sxs-lookup"><span data-stu-id="86e25-246">Each MPEG audio frame contains either 384 (Layer 1) or 1152 (Layer 2) audio samples per channel.</span></span> <span data-ttu-id="86e25-247">Однако каждый входной буфер кодировщика может содержать любое количество примеров PCM.</span><span class="sxs-lookup"><span data-stu-id="86e25-247">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="86e25-248">Размер каждого входного буфера должен быть кратен выравниванию блока.</span><span class="sxs-lookup"><span data-stu-id="86e25-248">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="86e25-249">Кодировщик кэширует входные образцы, пока не будет достаточно для звукового фрейма MPEG.</span><span class="sxs-lookup"><span data-stu-id="86e25-249">The encoder caches input samples until it has enough for an MPEG audio frame.</span></span>

<span data-ttu-id="86e25-250">Каждый выходной буфер содержит один необработанный кадр MPEG.</span><span class="sxs-lookup"><span data-stu-id="86e25-250">Each output buffer contains one raw MPEG frame.</span></span> <span data-ttu-id="86e25-251">Размер каждого выходного буфера зависит от скорости потока и частоты выборки.</span><span class="sxs-lookup"><span data-stu-id="86e25-251">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

### <a name="configuring-the-encoder"></a><span data-ttu-id="86e25-252">Настройка кодировщика</span><span class="sxs-lookup"><span data-stu-id="86e25-252">Configuring the Encoder</span></span>

<span data-ttu-id="86e25-253">Чтобы изменить параметры по умолчанию для кодировщика, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="86e25-253">To change any of the default settings on the encoder, perform the following steps:</span></span>

1.  <span data-ttu-id="86e25-254">Создайте экземпляр файла MFT кодировщика.</span><span class="sxs-lookup"><span data-stu-id="86e25-254">Create an instance of the encoder MFT.</span></span>
2.  <span data-ttu-id="86e25-255">Вызовите метод [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , чтобы получить список предпочтительных типов выходных данных.</span><span class="sxs-lookup"><span data-stu-id="86e25-255">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of the preferred output types.</span></span> <span data-ttu-id="86e25-256">Кодировщик перечислит все частоты выборки для Mono и стерео.</span><span class="sxs-lookup"><span data-stu-id="86e25-256">The encoder enumerates all sample rates for both mono and stereo.</span></span> <span data-ttu-id="86e25-257">Выберите один из этих типов носителей в зависимости от частоты выборки и количества каналов.</span><span class="sxs-lookup"><span data-stu-id="86e25-257">Select one of these media types, based on the sample rate and number of channels.</span></span> <span data-ttu-id="86e25-258">Значение [атрибута \_ \_ \_ Среднее \_ число байт в \_ \_ секунду для звука MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) указывает скорость по умолчанию (в байтах в секунду).</span><span class="sxs-lookup"><span data-stu-id="86e25-258">The [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute indicates the default bit rate, in bytes per second.</span></span>
3.  <span data-ttu-id="86e25-259">Необязательно. можно переопределить скорость по умолчанию, задав новое значение для [среднего числа \_ байт \_ в \_ \_ \_ \_ секунду](mf-mt-audio-avg-bytes-per-second-attribute.md) на выходном типе носителя.</span><span class="sxs-lookup"><span data-stu-id="86e25-259">Optional: You can override the default bit rate by setting a new value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) on the output media type.</span></span> <span data-ttu-id="86e25-260">Допустимые скорости работы зависят от частоты выборки, количества каналов и звукового уровня.</span><span class="sxs-lookup"><span data-stu-id="86e25-260">Valid bit rates depend on the sample rate, number of channels, and audio layer.</span></span>
    > [!Note]  
    > <span data-ttu-id="86e25-261">На этом этапе настройки кодировщику по умолчанию присвоено звуковое сопровождение уровня 2 и принимается только скорость, равная 2 уровням.</span><span class="sxs-lookup"><span data-stu-id="86e25-261">At this point in the configuration process, the encoder defaults to Layer 2 audio and will only accept Layer 2 bit rates.</span></span> <span data-ttu-id="86e25-262">Вы сможете переключить кодировщик на слой 1 на более позднем этапе (см. шаг 7).</span><span class="sxs-lookup"><span data-stu-id="86e25-262">You will be able to switch the encoder to Layer 1 in a later step (see step 7).</span></span> <span data-ttu-id="86e25-263">В этом случае оставьте бит скорости по умолчанию для Now; его можно изменить на шаге 8.</span><span class="sxs-lookup"><span data-stu-id="86e25-263">In that case, leave the default bit rate for now; you can change it again in step 8.</span></span>

     

4.  <span data-ttu-id="86e25-264">Вызовите метод [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , чтобы задать тип выходного носителя.</span><span class="sxs-lookup"><span data-stu-id="86e25-264">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the output media type.</span></span> <span data-ttu-id="86e25-265">Если вы задали собственное значение для [среднего двоичного \_ сигнала MF MT \_ \_ \_ \_ в \_ секунду](mf-mt-audio-avg-bytes-per-second-attribute.md) , а файл MFT отклоняет тип выходного носителя, скорее всего, вы указали недопустимую скорость.</span><span class="sxs-lookup"><span data-stu-id="86e25-265">If you set your own value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) and the MFT rejects the output media type, it is likely because you specified an invalid bit rate.</span></span>
5.  <span data-ttu-id="86e25-266">Вызовите [**имфтрансформ:: жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) , чтобы перечислить входной тип носителя.</span><span class="sxs-lookup"><span data-stu-id="86e25-266">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to enumerate the input media type.</span></span> <span data-ttu-id="86e25-267">Так как частота выборки и количество каналов должны совпадать с типом выходных данных, перечисляются только два параметра: 32-разрядный вход PCM с плавающей точкой и 16-разрядное целочисленное входное значение PCM.</span><span class="sxs-lookup"><span data-stu-id="86e25-267">Because the sample rate and number of channels must be identical to the output type, only two options are enumerated: 32-bit floating-point PCM input and 16-bit integer PCM input.</span></span> <span data-ttu-id="86e25-268">Выберите один из них.</span><span class="sxs-lookup"><span data-stu-id="86e25-268">Select one of these.</span></span>
6.  <span data-ttu-id="86e25-269">Вызовите [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , чтобы задать тип входного носителя.</span><span class="sxs-lookup"><span data-stu-id="86e25-269">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the input media type.</span></span>
7.  <span data-ttu-id="86e25-270">Необязательно. для кодирования звука уровня 1 Установите для свойства [кодекапи \_ Авенкмпалайер](../directshow/avencmpalayer-property.md) значение **еавенкмпалайер \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="86e25-270">Optional: To encode Layer 1 audio, set the [CODECAPI\_AVEncMPALayer](../directshow/avencmpalayer-property.md) property to **eAVEncMPALayer\_1**.</span></span>
8.  <span data-ttu-id="86e25-271">Необязательно. чтобы изменить скорость потока, задайте свойство [кодекапи \_ авенккоммонмеанбитрате](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="86e25-271">Optional: To change the bit rate, set the [CODECAPI\_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <span data-ttu-id="86e25-272">Скорость потока должна быть одной из допустимых битов, перечисленных в спецификациях MPEG-1 или MPEG-2 LSF.</span><span class="sxs-lookup"><span data-stu-id="86e25-272">The bit rate must be one of the valid bit rates listed in the MPEG-1 or MPEG-2 LSF specifications.</span></span> <span data-ttu-id="86e25-273">Кроме того, можно вызвать метод [**икодекапи:: жетпараметервалуес**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) , чтобы получить список допустимых битовых ставок на основе текущих параметров.</span><span class="sxs-lookup"><span data-stu-id="86e25-273">Alternatively, you can call [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) to get a list of valid bit rates, based on the current settings.</span></span>
9.  <span data-ttu-id="86e25-274">Необязательно. с помощью многоканального звука можно задать свойство [кодекапи \_ авенкмпакодингмоде](../directshow/avencmpacodingmode-property.md) , чтобы изменить режим кодирования на Dual-канальное или совместное стерео.</span><span class="sxs-lookup"><span data-stu-id="86e25-274">Optional: With 2-channel audio, you can set the [CODECAPI\_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) property to change the coding mode to dual channel or joint stereo.</span></span> <span data-ttu-id="86e25-275">Чтобы получить допустимые параметры, можно вызвать метод [**икодекапи:: жетпараметерранже**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) .</span><span class="sxs-lookup"><span data-stu-id="86e25-275">You can call [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) to get the valid options.</span></span> <span data-ttu-id="86e25-276">(Для звука с 1 каналом единственным вариантом является Mono.)</span><span class="sxs-lookup"><span data-stu-id="86e25-276">(For 1-channel audio, the only option is mono.)</span></span>
10. <span data-ttu-id="86e25-277">Необязательно. задайте любые другие свойства [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) , перечисленные ранее.</span><span class="sxs-lookup"><span data-stu-id="86e25-277">Optional: Set any of the other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties listed previously.</span></span>

<span data-ttu-id="86e25-278">Важно следовать порядку этих шагов.</span><span class="sxs-lookup"><span data-stu-id="86e25-278">It is important to follow the order of these steps.</span></span> <span data-ttu-id="86e25-279">В частности, перед изменением свойств [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) задайте тип выходного носителя.</span><span class="sxs-lookup"><span data-stu-id="86e25-279">In particular, set the output media type before changing any [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties.</span></span> <span data-ttu-id="86e25-280">Кроме того, необходимо задать свойства **икодекапи** до того, как MFT получит первый входной пример.</span><span class="sxs-lookup"><span data-stu-id="86e25-280">Also, you must set **ICodecAPI** properties before the MFT receives the first input sample.</span></span> <span data-ttu-id="86e25-281">После того как MFT получит входные данные, свойства кодека будут доступны только для чтения, а [**икодекапи:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) возвращает значение **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="86e25-281">After the MFT receives input, the codec properties are read-only, and [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) returns the value **S\_FALSE**.</span></span>

### <a name="supported-bit-rates"></a><span data-ttu-id="86e25-282">Поддерживаемые скорости</span><span class="sxs-lookup"><span data-stu-id="86e25-282">Supported Bit Rates</span></span>

<span data-ttu-id="86e25-283">Кодировщик поддерживает следующие скорости.</span><span class="sxs-lookup"><span data-stu-id="86e25-283">The encoder supports the following bit rates.</span></span>



<span data-ttu-id="86e25-284">MPEG-1</span><span class="sxs-lookup"><span data-stu-id="86e25-284">MPEG-1</span></span>

<span data-ttu-id="86e25-285">MPEG-2</span><span class="sxs-lookup"><span data-stu-id="86e25-285">MPEG-2</span></span>

<span data-ttu-id="86e25-286">Уровень 1</span><span class="sxs-lookup"><span data-stu-id="86e25-286">Layer 1</span></span>

<span data-ttu-id="86e25-287">Уровень 2</span><span class="sxs-lookup"><span data-stu-id="86e25-287">Layer 2</span></span>

<span data-ttu-id="86e25-288">Уровень 1</span><span class="sxs-lookup"><span data-stu-id="86e25-288">Layer 1</span></span>

<span data-ttu-id="86e25-289">Уровень 2</span><span class="sxs-lookup"><span data-stu-id="86e25-289">Layer 2</span></span>

<span data-ttu-id="86e25-290">32</span><span class="sxs-lookup"><span data-stu-id="86e25-290">32</span></span>

<span data-ttu-id="86e25-291">32\*</span><span class="sxs-lookup"><span data-stu-id="86e25-291">32\*</span></span>

<span data-ttu-id="86e25-292">32</span><span class="sxs-lookup"><span data-stu-id="86e25-292">32</span></span>

<span data-ttu-id="86e25-293">8</span><span class="sxs-lookup"><span data-stu-id="86e25-293">8</span></span>

<span data-ttu-id="86e25-294">64</span><span class="sxs-lookup"><span data-stu-id="86e25-294">64</span></span>

<span data-ttu-id="86e25-295">48\*</span><span class="sxs-lookup"><span data-stu-id="86e25-295">48\*</span></span>

<span data-ttu-id="86e25-296">38</span><span class="sxs-lookup"><span data-stu-id="86e25-296">38</span></span>

<span data-ttu-id="86e25-297">16</span><span class="sxs-lookup"><span data-stu-id="86e25-297">16</span></span>

<span data-ttu-id="86e25-298">96</span><span class="sxs-lookup"><span data-stu-id="86e25-298">96</span></span>

<span data-ttu-id="86e25-299">56\*</span><span class="sxs-lookup"><span data-stu-id="86e25-299">56\*</span></span>

<span data-ttu-id="86e25-300">56</span><span class="sxs-lookup"><span data-stu-id="86e25-300">56</span></span>

<span data-ttu-id="86e25-301">24</span><span class="sxs-lookup"><span data-stu-id="86e25-301">24</span></span>

<span data-ttu-id="86e25-302">128</span><span class="sxs-lookup"><span data-stu-id="86e25-302">128</span></span>

<span data-ttu-id="86e25-303">64</span><span class="sxs-lookup"><span data-stu-id="86e25-303">64</span></span>

<span data-ttu-id="86e25-304">64</span><span class="sxs-lookup"><span data-stu-id="86e25-304">64</span></span>

<span data-ttu-id="86e25-305">32</span><span class="sxs-lookup"><span data-stu-id="86e25-305">32</span></span>

<span data-ttu-id="86e25-306">160</span><span class="sxs-lookup"><span data-stu-id="86e25-306">160</span></span>

<span data-ttu-id="86e25-307">80\*</span><span class="sxs-lookup"><span data-stu-id="86e25-307">80\*</span></span>

<span data-ttu-id="86e25-308">80</span><span class="sxs-lookup"><span data-stu-id="86e25-308">80</span></span>

<span data-ttu-id="86e25-309">40</span><span class="sxs-lookup"><span data-stu-id="86e25-309">40</span></span>

<span data-ttu-id="86e25-310">192</span><span class="sxs-lookup"><span data-stu-id="86e25-310">192</span></span>

<span data-ttu-id="86e25-311">96</span><span class="sxs-lookup"><span data-stu-id="86e25-311">96</span></span>

<span data-ttu-id="86e25-312">96</span><span class="sxs-lookup"><span data-stu-id="86e25-312">96</span></span>

<span data-ttu-id="86e25-313">48</span><span class="sxs-lookup"><span data-stu-id="86e25-313">48</span></span>

<span data-ttu-id="86e25-314">224</span><span class="sxs-lookup"><span data-stu-id="86e25-314">224</span></span>

<span data-ttu-id="86e25-315">112</span><span class="sxs-lookup"><span data-stu-id="86e25-315">112</span></span>

<span data-ttu-id="86e25-316">112</span><span class="sxs-lookup"><span data-stu-id="86e25-316">112</span></span>

<span data-ttu-id="86e25-317">56</span><span class="sxs-lookup"><span data-stu-id="86e25-317">56</span></span>

<span data-ttu-id="86e25-318">256</span><span class="sxs-lookup"><span data-stu-id="86e25-318">256</span></span>

<span data-ttu-id="86e25-319">128</span><span class="sxs-lookup"><span data-stu-id="86e25-319">128</span></span>

<span data-ttu-id="86e25-320">128</span><span class="sxs-lookup"><span data-stu-id="86e25-320">128</span></span>

<span data-ttu-id="86e25-321">64</span><span class="sxs-lookup"><span data-stu-id="86e25-321">64</span></span>

<span data-ttu-id="86e25-322">288</span><span class="sxs-lookup"><span data-stu-id="86e25-322">288</span></span>

<span data-ttu-id="86e25-323">160</span><span class="sxs-lookup"><span data-stu-id="86e25-323">160</span></span>

<span data-ttu-id="86e25-324">144</span><span class="sxs-lookup"><span data-stu-id="86e25-324">144</span></span>

<span data-ttu-id="86e25-325">80</span><span class="sxs-lookup"><span data-stu-id="86e25-325">80</span></span>

<span data-ttu-id="86e25-326">320</span><span class="sxs-lookup"><span data-stu-id="86e25-326">320</span></span>

<span data-ttu-id="86e25-327">192</span><span class="sxs-lookup"><span data-stu-id="86e25-327">192</span></span>

<span data-ttu-id="86e25-328">160</span><span class="sxs-lookup"><span data-stu-id="86e25-328">160</span></span>

<span data-ttu-id="86e25-329">96</span><span class="sxs-lookup"><span data-stu-id="86e25-329">96</span></span>

<span data-ttu-id="86e25-330">352</span><span class="sxs-lookup"><span data-stu-id="86e25-330">352</span></span>

<span data-ttu-id="86e25-331">224\*\*</span><span class="sxs-lookup"><span data-stu-id="86e25-331">224\*\*</span></span>

<span data-ttu-id="86e25-332">176</span><span class="sxs-lookup"><span data-stu-id="86e25-332">176</span></span>

<span data-ttu-id="86e25-333">112</span><span class="sxs-lookup"><span data-stu-id="86e25-333">112</span></span>

<span data-ttu-id="86e25-334">384</span><span class="sxs-lookup"><span data-stu-id="86e25-334">384</span></span>

<span data-ttu-id="86e25-335">256\*\*</span><span class="sxs-lookup"><span data-stu-id="86e25-335">256\*\*</span></span>

<span data-ttu-id="86e25-336">192</span><span class="sxs-lookup"><span data-stu-id="86e25-336">192</span></span>

<span data-ttu-id="86e25-337">128</span><span class="sxs-lookup"><span data-stu-id="86e25-337">128</span></span>

<span data-ttu-id="86e25-338">416</span><span class="sxs-lookup"><span data-stu-id="86e25-338">416</span></span>

<span data-ttu-id="86e25-339">230\*\*</span><span class="sxs-lookup"><span data-stu-id="86e25-339">230\*\*</span></span>

<span data-ttu-id="86e25-340">224</span><span class="sxs-lookup"><span data-stu-id="86e25-340">224</span></span>

<span data-ttu-id="86e25-341">144</span><span class="sxs-lookup"><span data-stu-id="86e25-341">144</span></span>

<span data-ttu-id="86e25-342">448</span><span class="sxs-lookup"><span data-stu-id="86e25-342">448</span></span>

<span data-ttu-id="86e25-343">384\*\*</span><span class="sxs-lookup"><span data-stu-id="86e25-343">384\*\*</span></span>

<span data-ttu-id="86e25-344">256</span><span class="sxs-lookup"><span data-stu-id="86e25-344">256</span></span>

<span data-ttu-id="86e25-345">160</span><span class="sxs-lookup"><span data-stu-id="86e25-345">160</span></span>



 

<dl> <span data-ttu-id="86e25-346">\* Только моно</span><span class="sxs-lookup"><span data-stu-id="86e25-346">\* Mono only</span></span>  
<span data-ttu-id="86e25-347">\*\* Только стерео</span><span class="sxs-lookup"><span data-stu-id="86e25-347">\*\* Stereo only</span></span>  
</dl>

### <a name="example-media-types"></a><span data-ttu-id="86e25-348">Примеры типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="86e25-348">Example Media Types</span></span>

<span data-ttu-id="86e25-349">Ниже приведен пример типов мультимедиа, которые необходимы для кодирования 16-разрядного целочисленного PCM 48-кГц при скорости по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86e25-349">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate.</span></span>

<span data-ttu-id="86e25-350">Тип выходного носителя:</span><span class="sxs-lookup"><span data-stu-id="86e25-350">Output media type:</span></span>

| <span data-ttu-id="86e25-351">attribute</span><span class="sxs-lookup"><span data-stu-id="86e25-351">Attribute</span></span>                                                                           | <span data-ttu-id="86e25-352">Значение</span><span class="sxs-lookup"><span data-stu-id="86e25-352">Value</span></span>                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [<span data-ttu-id="86e25-353">\_ \_ основной тип MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="86e25-353">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="86e25-354">**Мфмедиатипе \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="86e25-354">**MFMediaType\_Audio**</span></span>  |
| [<span data-ttu-id="86e25-355">подтип MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="86e25-355">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="86e25-356">**Мфаудиоформат \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="86e25-356">**MFAudioFormat\_MPEG**</span></span> |
| [<span data-ttu-id="86e25-357">\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду</span><span class="sxs-lookup"><span data-stu-id="86e25-357">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="86e25-358">48000</span><span class="sxs-lookup"><span data-stu-id="86e25-358">48000</span></span>                   |
| [<span data-ttu-id="86e25-359">\_ \_ каналы аудиосигнала MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="86e25-359">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="86e25-360">2</span><span class="sxs-lookup"><span data-stu-id="86e25-360">2</span></span>                       |



 

<span data-ttu-id="86e25-361">Тип входного носителя:</span><span class="sxs-lookup"><span data-stu-id="86e25-361">Input media type:</span></span>

| <span data-ttu-id="86e25-362">attribute</span><span class="sxs-lookup"><span data-stu-id="86e25-362">Attribute</span></span>                                                                                | <span data-ttu-id="86e25-363">Значение</span><span class="sxs-lookup"><span data-stu-id="86e25-363">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="86e25-364">\_ \_ основной тип MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="86e25-364">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="86e25-365">**Мфмедиатипе \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="86e25-365">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="86e25-366">подтип MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="86e25-366">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="86e25-367">**Мфаудиоформат \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="86e25-367">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="86e25-368">\_ \_ звуковый бит MF MT \_ \_ на \_ выборку</span><span class="sxs-lookup"><span data-stu-id="86e25-368">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="86e25-369">16</span><span class="sxs-lookup"><span data-stu-id="86e25-369">16</span></span>                     |
| [<span data-ttu-id="86e25-370">\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду</span><span class="sxs-lookup"><span data-stu-id="86e25-370">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="86e25-371">48000</span><span class="sxs-lookup"><span data-stu-id="86e25-371">48000</span></span>                  |
| [<span data-ttu-id="86e25-372">\_ \_ каналы аудиосигнала MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="86e25-372">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="86e25-373">2</span><span class="sxs-lookup"><span data-stu-id="86e25-373">2</span></span>                      |
| [<span data-ttu-id="86e25-374">\_ \_ Выравнивание звукового \_ блока MF MT \_</span><span class="sxs-lookup"><span data-stu-id="86e25-374">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="86e25-375">4</span><span class="sxs-lookup"><span data-stu-id="86e25-375">4</span></span>                      |
| [<span data-ttu-id="86e25-376">\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT</span><span class="sxs-lookup"><span data-stu-id="86e25-376">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="86e25-377">192000</span><span class="sxs-lookup"><span data-stu-id="86e25-377">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="86e25-378">Требования</span><span class="sxs-lookup"><span data-stu-id="86e25-378">Requirements</span></span>



| <span data-ttu-id="86e25-379">Требование</span><span class="sxs-lookup"><span data-stu-id="86e25-379">Requirement</span></span> | <span data-ttu-id="86e25-380">Значение</span><span class="sxs-lookup"><span data-stu-id="86e25-380">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e25-381">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86e25-381">Minimum supported client</span></span><br/> | <span data-ttu-id="86e25-382">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="86e25-382">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="86e25-383">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86e25-383">Minimum supported server</span></span><br/> | <span data-ttu-id="86e25-384">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="86e25-384">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="86e25-385">DLL</span><span class="sxs-lookup"><span data-stu-id="86e25-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e25-386"><dt>Msmpeg2enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e25-386"><dt>Msmpeg2enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e25-387">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86e25-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e25-388">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="86e25-388">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
