---
description: Кодировщик Microsoft Media Foundation AAC — это Media Foundation преобразование, которое кодирует расширенный профиль (LC) с низким уровнем сложности (AAC), как определено в стандарте ISO/IEC 13818-7 (звук MPEG-2 Audio Part 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Кодировщик AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897525"
---
# <a name="aac-encoder"></a><span data-ttu-id="7840d-103">Кодировщик AAC</span><span class="sxs-lookup"><span data-stu-id="7840d-103">AAC Encoder</span></span>

<span data-ttu-id="7840d-104">Кодировщик Microsoft Media Foundation AAC — это [Media Foundation преобразование](media-foundation-transforms.md) , которое кодирует расширенный профиль (LC) с низким уровнем сложности (AAC), как определено в стандарте ISO/IEC 13818-7 (звук MPEG-2 Audio Part 7).</span><span class="sxs-lookup"><span data-stu-id="7840d-104">The Microsoft Media Foundation AAC encoder is a [Media Foundation Transform](media-foundation-transforms.md) that encodes Advanced Audio Coding (AAC) Low Complexity (LC) profile, as defined by ISO/IEC 13818-7 (MPEG-2 Audio Part 7) .</span></span>

<span data-ttu-id="7840d-105">Кодировщик AAC не поддерживает кодирование для любых других профилей AAC, таких как Main, SSR или ЛТП.</span><span class="sxs-lookup"><span data-stu-id="7840d-105">The AAC encoder does not support encoding to any other AAC profiles, such as Main, SSR, or LTP.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="7840d-106">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="7840d-106">Class Identifier</span></span>

<span data-ttu-id="7840d-107">Идентификатором класса (CLSID) кодировщика AAC является **CLSID \_ аакмфтенкодер**, определенный в файле заголовка вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="7840d-107">The class identifier (CLSID) of the AAC encoder is **CLSID\_AACMFTEncoder**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="7840d-108">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="7840d-108">Media Types</span></span>

<span data-ttu-id="7840d-109">Кодировщик AAC поддерживает следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="7840d-109">The AAC encoder supports the following media types.</span></span> <span data-ttu-id="7840d-110">Можно задать типы в первом порядке ввода или тип вывода.</span><span class="sxs-lookup"><span data-stu-id="7840d-110">You can set the types in either order input type first, or output type first.</span></span>

### <a name="input-types"></a><span data-ttu-id="7840d-111">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="7840d-111">Input Types</span></span>

<span data-ttu-id="7840d-112">Задайте следующие атрибуты для входного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="7840d-112">Set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7840d-113">attribute</span><span class="sxs-lookup"><span data-stu-id="7840d-113">Attribute</span></span></th>
<th><span data-ttu-id="7840d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7840d-114">Description</span></span></th>
<th><span data-ttu-id="7840d-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="7840d-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7840d-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="7840d-117">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="7840d-117">Major type.</span></span></td>
<td><span data-ttu-id="7840d-118">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="7840d-118">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7840d-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="7840d-120">Подтип.</span><span class="sxs-lookup"><span data-stu-id="7840d-120">Subtype.</span></span></td>
<td><span data-ttu-id="7840d-121">Необходимо <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="7840d-121">Must be <strong>MFAudioFormat_PCM</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7840d-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="7840d-123">Бит на выборку.</span><span class="sxs-lookup"><span data-stu-id="7840d-123">Bits per sample.</span></span></td>
<td><span data-ttu-id="7840d-124">Должно быть 16.</span><span class="sxs-lookup"><span data-stu-id="7840d-124">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7840d-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="7840d-126">Выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="7840d-126">Samples per second.</span></span></td>
<td><span data-ttu-id="7840d-127">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7840d-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="7840d-128">44100 (44,1 кГц)</span><span class="sxs-lookup"><span data-stu-id="7840d-128">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="7840d-129">48000 (48 кГц)</span><span class="sxs-lookup"><span data-stu-id="7840d-129">48000 (48 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7840d-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="7840d-131">Число каналов.</span><span class="sxs-lookup"><span data-stu-id="7840d-131">Number of channels.</span></span></td>
<td><span data-ttu-id="7840d-132">Должно быть 1 (моно) или 2 (стерео) или 6 (5,1).</span><span class="sxs-lookup"><span data-stu-id="7840d-132">Must be 1 (mono) or 2 (stereo), or 6 (5.1).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7840d-133">Поддержка 6 звуковых каналов была представлена в Windows 10 и недоступна для более ранних версий Windows.</span><span class="sxs-lookup"><span data-stu-id="7840d-133">Support for 6 audio channels was introduced with Windows 10 and is not available for earlier versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7840d-134">После установки входного типа кодировщик получает следующие значения и добавляет их к типу мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="7840d-134">After the input type is set, the encoder derives the following values and adds them to the media type:</span></span>

-   [<span data-ttu-id="7840d-135">**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**</span><span class="sxs-lookup"><span data-stu-id="7840d-135">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="7840d-136">**\_ \_ Выравнивание звукового \_ блока MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="7840d-136">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="7840d-137">**\_ \_ Средняя скорость MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7840d-137">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a><span data-ttu-id="7840d-138">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="7840d-138">Output Types</span></span>

<span data-ttu-id="7840d-139">Задайте следующие атрибуты для выходного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="7840d-139">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7840d-140">attribute</span><span class="sxs-lookup"><span data-stu-id="7840d-140">Attribute</span></span></th>
<th><span data-ttu-id="7840d-141">Описание</span><span class="sxs-lookup"><span data-stu-id="7840d-141">Description</span></span></th>
<th><span data-ttu-id="7840d-142">Remarks</span><span class="sxs-lookup"><span data-stu-id="7840d-142">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7840d-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="7840d-144">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="7840d-144">Major type.</span></span></td>
<td><span data-ttu-id="7840d-145">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="7840d-145">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7840d-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="7840d-147">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="7840d-147">Audio subtype.</span></span></td>
<td><span data-ttu-id="7840d-148">Необходимо <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="7840d-148">Must be <strong>MFAudioFormat_AAC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7840d-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="7840d-150">Бит на выборку.</span><span class="sxs-lookup"><span data-stu-id="7840d-150">Bits per sample.</span></span></td>
<td><span data-ttu-id="7840d-151">Должно быть 16.</span><span class="sxs-lookup"><span data-stu-id="7840d-151">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7840d-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="7840d-153">Выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="7840d-153">Samples per second.</span></span></td>
<td><span data-ttu-id="7840d-154">Должен соответствовать типу входных данных.</span><span class="sxs-lookup"><span data-stu-id="7840d-154">Must match the input type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7840d-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="7840d-156">Число каналов.</span><span class="sxs-lookup"><span data-stu-id="7840d-156">Number of channels.</span></span></td>
<td><span data-ttu-id="7840d-157">Должен соответствовать типу входных данных.</span><span class="sxs-lookup"><span data-stu-id="7840d-157">Must match the input type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7840d-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="7840d-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="7840d-159">Битовая скорость закодированного потока AAC в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="7840d-159">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="7840d-160">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7840d-160">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="7840d-161">12000</span><span class="sxs-lookup"><span data-stu-id="7840d-161">12000</span></span></li>
<li><span data-ttu-id="7840d-162">16000</span><span class="sxs-lookup"><span data-stu-id="7840d-162">16000</span></span></li>
<li><span data-ttu-id="7840d-163">20 000</span><span class="sxs-lookup"><span data-stu-id="7840d-163">20000</span></span></li>
<li><span data-ttu-id="7840d-164">24 000</span><span class="sxs-lookup"><span data-stu-id="7840d-164">24000</span></span></li>
</ul>
<span data-ttu-id="7840d-165">Значение по умолчанию для Mono и стерео — 12000 (96 Кбит/с).</span><span class="sxs-lookup"><span data-stu-id="7840d-165">The default value for both mono and stereo is 12000 (96 Kbps).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7840d-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="7840d-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="7840d-167">Тип полезных данных AAC.</span><span class="sxs-lookup"><span data-stu-id="7840d-167">The AAC payload type.</span></span></td>
<td><span data-ttu-id="7840d-168">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="7840d-168">Optional.</span></span> <span data-ttu-id="7840d-169">Если задано, значение должно быть равно нулю, что означает, что поток содержит только элементы raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="7840d-169">If set, the value must be zero, indicating that the stream contains raw_data_block elements only.</span></span><br/> <span data-ttu-id="7840d-170">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="7840d-170">Optional.</span></span> <span data-ttu-id="7840d-171">Если атрибут не задан, значение по умолчанию равно нулю, что означает, что поток содержит только элементы raw_data_block (необработанные AAC).</span><span class="sxs-lookup"><span data-stu-id="7840d-171">If the attribute is not set, the default value is zero, indicating that the stream contains raw_data_block elements only (raw AAC).</span></span> <br/> <span data-ttu-id="7840d-172">Если этот атрибут задан, в Windows 7 значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7840d-172">In Windows 7, if this attribute is set, the value must be zero.</span></span><br/> <span data-ttu-id="7840d-173">Начиная с Windows 8, значением может быть 0 (RAW AAC) или 1 (ADTS AAC).</span><span class="sxs-lookup"><span data-stu-id="7840d-173">Starting in Windows 8, the value can be 0 (raw AAC) or 1 (ADTS AAC).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7840d-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="7840d-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="7840d-175">Профиль аудио AAC и уровень.</span><span class="sxs-lookup"><span data-stu-id="7840d-175">The AAC audio profile and level.</span></span></td>
<td><span data-ttu-id="7840d-176">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="7840d-176">Optional.</span></span> <span data-ttu-id="7840d-177">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7840d-177">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="7840d-178">0x29 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7840d-178">0x29 (default)</span></span></li>
<li><span data-ttu-id="7840d-179">0x2A</span><span class="sxs-lookup"><span data-stu-id="7840d-179">0x2A</span></span></li>
<li><span data-ttu-id="7840d-180">0x2B</span><span class="sxs-lookup"><span data-stu-id="7840d-180">0x2B</span></span></li>
<li><span data-ttu-id="7840d-181">0x2C</span><span class="sxs-lookup"><span data-stu-id="7840d-181">0x2C</span></span></li>
<li><span data-ttu-id="7840d-182">0x2E</span><span class="sxs-lookup"><span data-stu-id="7840d-182">0x2E</span></span></li>
<li><span data-ttu-id="7840d-183">0x2F</span><span class="sxs-lookup"><span data-stu-id="7840d-183">0x2F</span></span></li>
<li><span data-ttu-id="7840d-184">0x30</span><span class="sxs-lookup"><span data-stu-id="7840d-184">0x30</span></span></li>
<li><span data-ttu-id="7840d-185">0x31</span><span class="sxs-lookup"><span data-stu-id="7840d-185">0x31</span></span></li>
<li><span data-ttu-id="7840d-186">0x32</span><span class="sxs-lookup"><span data-stu-id="7840d-186">0x32</span></span></li>
<li><span data-ttu-id="7840d-187">0x33</span><span class="sxs-lookup"><span data-stu-id="7840d-187">0x33</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7840d-188">В следующей таблице перечислены значения, которые можно использовать для атрибута MF_MT_AAC_PROFILE_LEVEL_INDICATION.</span><span class="sxs-lookup"><span data-stu-id="7840d-188">The following table lists the values that can be used for the MF_MT_AAC_PROFILE_LEVEL_INDICATION attribute.</span></span>

| <span data-ttu-id="7840d-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION значение</span><span class="sxs-lookup"><span data-stu-id="7840d-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION value</span></span> | <span data-ttu-id="7840d-190">Профиль</span><span class="sxs-lookup"><span data-stu-id="7840d-190">Profile</span></span>                           |
|------------------------------------------|-----------------------------------|
| <span data-ttu-id="7840d-191">0x29</span><span class="sxs-lookup"><span data-stu-id="7840d-191">0x29</span></span>                                     | <span data-ttu-id="7840d-192">Профиль AAC L2</span><span class="sxs-lookup"><span data-stu-id="7840d-192">AAC Profile L2</span></span>                    | 
| <span data-ttu-id="7840d-193">0x2A</span><span class="sxs-lookup"><span data-stu-id="7840d-193">0x2A</span></span>                                     | <span data-ttu-id="7840d-194">AAC профиль 4</span><span class="sxs-lookup"><span data-stu-id="7840d-194">AAC Profile L4</span></span>                    | 
| <span data-ttu-id="7840d-195">0x2B</span><span class="sxs-lookup"><span data-stu-id="7840d-195">0x2B</span></span>                                     | <span data-ttu-id="7840d-196">AAC профиль 5</span><span class="sxs-lookup"><span data-stu-id="7840d-196">AAC Profile L5</span></span>                    | 
| <span data-ttu-id="7840d-197">0x2C</span><span class="sxs-lookup"><span data-stu-id="7840d-197">0x2C</span></span>                                     | <span data-ttu-id="7840d-198">Высокая эффективность v1 AAC профилирование L2</span><span class="sxs-lookup"><span data-stu-id="7840d-198">High Efficiency v1 AAC Profile L2</span></span> | 
| <span data-ttu-id="7840d-199">0x2E</span><span class="sxs-lookup"><span data-stu-id="7840d-199">0x2E</span></span>                                     | <span data-ttu-id="7840d-200">Высокая эффективность v1 AAC профиль уровня 4</span><span class="sxs-lookup"><span data-stu-id="7840d-200">High Efficiency v1 AAC Profile L4</span></span> | 
| <span data-ttu-id="7840d-201">0x2F</span><span class="sxs-lookup"><span data-stu-id="7840d-201">0x2F</span></span>                                     | <span data-ttu-id="7840d-202">Высокопроизводительная версия 1 AAC профиль 5</span><span class="sxs-lookup"><span data-stu-id="7840d-202">High Efficiency v1 AAC Profile L5</span></span> | 
| <span data-ttu-id="7840d-203">0x30</span><span class="sxs-lookup"><span data-stu-id="7840d-203">0x30</span></span>                                     | <span data-ttu-id="7840d-204">Высокопроизводительная версия 2, AAC профиль L2</span><span class="sxs-lookup"><span data-stu-id="7840d-204">High Efficiency v2 AAC Profile L2</span></span> | 
| <span data-ttu-id="7840d-205">0x31</span><span class="sxs-lookup"><span data-stu-id="7840d-205">0x31</span></span>                                     | <span data-ttu-id="7840d-206">Высокопроизводительная версия 2 AAC профиль L3</span><span class="sxs-lookup"><span data-stu-id="7840d-206">High Efficiency v2 AAC Profile L3</span></span> | 
| <span data-ttu-id="7840d-207">0x32</span><span class="sxs-lookup"><span data-stu-id="7840d-207">0x32</span></span>                                     | <span data-ttu-id="7840d-208">Высокопроизводительный v2 AAC профиль уровня 4</span><span class="sxs-lookup"><span data-stu-id="7840d-208">High Efficiency v2 AAC Profile L4</span></span> | 
| <span data-ttu-id="7840d-209">0x33</span><span class="sxs-lookup"><span data-stu-id="7840d-209">0x33</span></span>                                     | <span data-ttu-id="7840d-210">Высокопроизводительный v2 AAC профиль уровня 5</span><span class="sxs-lookup"><span data-stu-id="7840d-210">High Efficiency v2 AAC Profile L5</span></span> | 

 

<span data-ttu-id="7840d-211">После установки типа выходных данных кодировщик AAC обновляет тип, добавляя атрибут [**\_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="7840d-211">After the output type is set, the AAC encoder updates the type by adding the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="7840d-212">Этот атрибут содержит часть структуры [**хеааквавеинфо**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) , которая появляется после структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) (то есть после элемента **вфкс** ).</span><span class="sxs-lookup"><span data-stu-id="7840d-212">This attribute contains the portion of the [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure that appears after the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure (that is, after the **wfx** member).</span></span> <span data-ttu-id="7840d-213">За ним следуют данные АудиоспеЦификконфиг () в соответствии с определением ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="7840d-213">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="7840d-214">Каждый образец выходных данных содержит один сжатый кадр AAC без заголовка.</span><span class="sxs-lookup"><span data-stu-id="7840d-214">Each output sample contains one compressed AAC frame with no header.</span></span> <span data-ttu-id="7840d-215">Этот формат эквивалентен элементу необработанного \_ \_ блока данных (), определенному MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="7840d-215">This format is equivalent to the raw\_data\_block() element defined by MPEG-2.</span></span> <span data-ttu-id="7840d-216">Атрибут [ \_ \_ \_ \_ типа полезных данных MF MT AAC](mf-mt-aac-payload-type.md) , если он есть в выходном типе, должен иметь нулевое значение, чтобы указать этот тип полезной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="7840d-216">The [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) attribute, if present in the output type, must be set to zero to indicate this payload type.</span></span>

<span data-ttu-id="7840d-217">Каждый пример выходных данных содержит один сжатый кадр AAC, соответствующий примерам PCM 1024.</span><span class="sxs-lookup"><span data-stu-id="7840d-217">Each output sample contains one compressed AAC frame corresponding to 1024 PCM samples.</span></span> <span data-ttu-id="7840d-218">Например, при частоте выборки 48 кГц продолжительность одного сжатого кадра составляет 21,33 МС.</span><span class="sxs-lookup"><span data-stu-id="7840d-218">For example, at 48 Khz sampling rate, the duration of one compressed frame is 21.33 msec.</span></span>

<span data-ttu-id="7840d-219">Если [ \_ \_ \_ \_ Тип полезной нагрузки MF MT AAC](mf-mt-aac-payload-type.md) равен нулю (значение по умолчанию), каждый образец вывода содержит один элемент необработанного \_ \_ блока данных (), определенный в стандарте ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="7840d-219">If [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) is zero (the default value), each output sample contains one raw\_data\_block() element as defined by ISO/IEC 13818-7.</span></span>

## <a name="example-media-types"></a><span data-ttu-id="7840d-220">Примеры типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7840d-220">Example Media Types</span></span>

<span data-ttu-id="7840d-221">Ниже приведен пример типов мультимедиа, необходимых для кодирования из стерео аудио AAC с 44,1 кГц, 160-кбит/с в необработанном формате.</span><span class="sxs-lookup"><span data-stu-id="7840d-221">Here is an example of the media types needed to encode from 44.1-kHz, 160-Kbps stereo audio to raw AAC</span></span>

<span data-ttu-id="7840d-222">Тип входного носителя:</span><span class="sxs-lookup"><span data-stu-id="7840d-222">Input media type:</span></span>



| <span data-ttu-id="7840d-223">attribute</span><span class="sxs-lookup"><span data-stu-id="7840d-223">Attribute</span></span>                                                                                    | <span data-ttu-id="7840d-224">Значение</span><span class="sxs-lookup"><span data-stu-id="7840d-224">Value</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="7840d-225">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7840d-225">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="7840d-226">**Мфмедиатипе \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="7840d-226">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="7840d-227">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="7840d-227">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="7840d-228">**Мфаудиоформат \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="7840d-228">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="7840d-229">**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**</span><span class="sxs-lookup"><span data-stu-id="7840d-229">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="7840d-230">16</span><span class="sxs-lookup"><span data-stu-id="7840d-230">16</span></span>                     |
| [<span data-ttu-id="7840d-231">**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="7840d-231">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="7840d-232">44100</span><span class="sxs-lookup"><span data-stu-id="7840d-232">44100</span></span>                  |
| [<span data-ttu-id="7840d-233">**\_ \_ каналы аудиосигнала MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7840d-233">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="7840d-234">2</span><span class="sxs-lookup"><span data-stu-id="7840d-234">2</span></span>                      |
| [<span data-ttu-id="7840d-235">**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**</span><span class="sxs-lookup"><span data-stu-id="7840d-235">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="7840d-236">176400 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-236">176400 (optional)</span></span>      |
| [<span data-ttu-id="7840d-237">**\_ \_ Выравнивание звукового \_ блока MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="7840d-237">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="7840d-238">4 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-238">4 (optional)</span></span>           |
| [<span data-ttu-id="7840d-239">**MF \_ — \_ все \_ \_ независимые примеры**</span><span class="sxs-lookup"><span data-stu-id="7840d-239">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="7840d-240">1 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-240">1 (optional)</span></span>           |
| [<span data-ttu-id="7840d-241">**\_ \_ Средняя скорость MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7840d-241">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                  | <span data-ttu-id="7840d-242">1411200 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-242">1411200 (optional)</span></span>     |
| [<span data-ttu-id="7840d-243">**\_ \_ примеры фиксированного \_ размера MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="7840d-243">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)                   | <span data-ttu-id="7840d-244">1 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-244">1 (optional)</span></span>           |



 

<span data-ttu-id="7840d-245">Тип выходного носителя:</span><span class="sxs-lookup"><span data-stu-id="7840d-245">Output media type:</span></span>



| <span data-ttu-id="7840d-246">attribute</span><span class="sxs-lookup"><span data-stu-id="7840d-246">Attribute</span></span>                                                                                      | <span data-ttu-id="7840d-247">Значение</span><span class="sxs-lookup"><span data-stu-id="7840d-247">Value</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7840d-248">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7840d-248">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="7840d-249">**Мфмедиатипе \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="7840d-249">**MFMediaType\_Audio**</span></span>                                                                          |
| [<span data-ttu-id="7840d-250">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="7840d-250">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="7840d-251">**Мфаудиоформат \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="7840d-251">**MFAudioFormat\_AAC**</span></span>                                                                          |
| [<span data-ttu-id="7840d-252">**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**</span><span class="sxs-lookup"><span data-stu-id="7840d-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="7840d-253">16</span><span class="sxs-lookup"><span data-stu-id="7840d-253">16</span></span>                                                                                              |
| [<span data-ttu-id="7840d-254">**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="7840d-254">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="7840d-255">44100</span><span class="sxs-lookup"><span data-stu-id="7840d-255">44100</span></span>                                                                                           |
| [<span data-ttu-id="7840d-256">**\_ \_ каналы аудиосигнала MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7840d-256">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="7840d-257">2</span><span class="sxs-lookup"><span data-stu-id="7840d-257">2</span></span>                                                                                               |
| [<span data-ttu-id="7840d-258">**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**</span><span class="sxs-lookup"><span data-stu-id="7840d-258">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="7840d-259">20 000</span><span class="sxs-lookup"><span data-stu-id="7840d-259">20000</span></span>                                                                                           |
| [<span data-ttu-id="7840d-260">\_ \_ \_ Тип полезных данных AAC MF MT \_</span><span class="sxs-lookup"><span data-stu-id="7840d-260">MF\_MT\_AAC\_PAYLOAD\_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="7840d-261">0 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-261">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="7840d-262">\_ \_ \_ Указание уровня звукового \_ профиля \_ MF MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="7840d-262">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="7840d-263">0x29 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-263">0x29 (optional)</span></span>                                                                                 |
| [<span data-ttu-id="7840d-264">**\_ \_ Выравнивание звукового \_ блока MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="7840d-264">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="7840d-265">1 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-265">1 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="7840d-266">**MF \_ — \_ все \_ \_ независимые примеры**</span><span class="sxs-lookup"><span data-stu-id="7840d-266">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)           | <span data-ttu-id="7840d-267">0 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-267">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="7840d-268">**\_ \_ Средняя скорость MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7840d-268">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                    | <span data-ttu-id="7840d-269">160000 (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7840d-269">160000 (optional)</span></span>                                                                               |
| [<span data-ttu-id="7840d-270">**\_ \_ данные пользователя MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7840d-270">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="7840d-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} используемых</span><span class="sxs-lookup"><span data-stu-id="7840d-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (optional)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7840d-272">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7840d-272">Remarks</span></span>

<span data-ttu-id="7840d-273">В текущей реализации каждый входной пример должен иметь допустимое время и длительность.</span><span class="sxs-lookup"><span data-stu-id="7840d-273">In the current implementation, every input sample must have a valid time and duration.</span></span> <span data-ttu-id="7840d-274">Чтобы задать время выборки, вызовите [**имфсампле:: сетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="7840d-274">To set the sample time, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="7840d-275">Чтобы задать длительность выборки, вызовите метод [**имфсампле:: сетсампледуратион**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="7840d-275">To set the sample duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="7840d-276">Если время выборки не задано, метод [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) кодировщика возвращает **MF \_ E \_ без \_ образца \_ метки времени**.</span><span class="sxs-lookup"><span data-stu-id="7840d-276">If the sample time is not set, the encoder's [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method returns **MF\_E\_NO\_SAMPLE\_TIMESTAMP**.</span></span> <span data-ttu-id="7840d-277">Если длительность выборки не задана, метод **ProcessInput** возвращает **MF \_ E \_ без \_ выборки \_ длительности**.</span><span class="sxs-lookup"><span data-stu-id="7840d-277">If the sample duration is not set, the **ProcessInput** method returns **MF\_E\_NO\_SAMPLE\_DURATION**.</span></span>

<span data-ttu-id="7840d-278">Длительность выборки может быть рассчитана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7840d-278">Sample duration can be calculated as follows:</span></span>


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



<span data-ttu-id="7840d-279">где *наудиосамплесперчаннел* — число выборки звука PCM на канал во входном буфере, а *нсамплесперсек* — частота выборки, в примерах в секунду.</span><span class="sxs-lookup"><span data-stu-id="7840d-279">where *nAudioSamplesPerChannel* is the number of PCM audio samples per channel in the input buffer, and *nSamplesPerSec* is the sampling rate, in samples per second.</span></span>

> [!Note]  
> <span data-ttu-id="7840d-280">Из-за ошибки в текущей реализации, если длительность выборки равна нулю, вызов [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) выполняется, но последующий вызов [**Имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) будет вызывать исключение деления на ноль.</span><span class="sxs-lookup"><span data-stu-id="7840d-280">Due to a bug in the current implementation, if the sample duration is set to zero, the [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) call succeeds, but a subsequent call to [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) will throw a divide-by-zero exception.</span></span> <span data-ttu-id="7840d-281">Чтобы избежать этой ошибки, задайте допустимую ненулевую длительность для каждого входного образца.</span><span class="sxs-lookup"><span data-stu-id="7840d-281">To avoid this error, set a valid nonzero duration on each input sample.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7840d-282">Требования</span><span class="sxs-lookup"><span data-stu-id="7840d-282">Requirements</span></span>



| <span data-ttu-id="7840d-283">Требование</span><span class="sxs-lookup"><span data-stu-id="7840d-283">Requirement</span></span> | <span data-ttu-id="7840d-284">Значение</span><span class="sxs-lookup"><span data-stu-id="7840d-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7840d-285">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7840d-285">Minimum supported client</span></span><br/> | <span data-ttu-id="7840d-286">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7840d-286">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7840d-287">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7840d-287">Minimum supported server</span></span><br/> | <span data-ttu-id="7840d-288">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7840d-288">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7840d-289">DLL</span><span class="sxs-lookup"><span data-stu-id="7840d-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7840d-290"><dt>Mfaacenc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7840d-290"><dt>Mfaacenc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7840d-291">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7840d-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7840d-292">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="7840d-292">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="7840d-293">**Декодер AAC**</span><span class="sxs-lookup"><span data-stu-id="7840d-293">**AAC Decoder**</span></span>](aac-decoder.md)
</dt> <dt>

[<span data-ttu-id="7840d-294">Типы носителей AAC</span><span class="sxs-lookup"><span data-stu-id="7840d-294">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="7840d-295">Типы звуковых носителей</span><span class="sxs-lookup"><span data-stu-id="7840d-295">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="7840d-296">Поддержка MPEG-4 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7840d-296">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="7840d-297">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7840d-297">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

