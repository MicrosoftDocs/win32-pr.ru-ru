---
description: Кодировщик Dolby Audio — это Media Foundation преобразование (MFT), которое кодирует моно или стерео Audio в Dolby Digital, также называемое Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Кодировщик цифрового звука Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f901587b816bc17d62f4095e093b661ce55f0009
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153567"
---
# <a name="dolby-digital-audio-encoder"></a><span data-ttu-id="00e60-103">Кодировщик цифрового звука Dolby</span><span class="sxs-lookup"><span data-stu-id="00e60-103">Dolby Digital Audio Encoder</span></span>

<span data-ttu-id="00e60-104">Кодировщик Dolby Audio — это [Media Foundation преобразование](media-foundation-transforms.md) (MFT), которое кодирует моно или стерео Audio в Dolby Digital, также называемое Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="00e60-104">The Dolby audio encoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that encodes mono or stereo audio to Dolby Digital, also called Dolby AC-3.</span></span> <span data-ttu-id="00e60-105">Кодировщик не поддерживает многоканальные входные данные, такие как конфигурация канала 5,1.</span><span class="sxs-lookup"><span data-stu-id="00e60-105">The encoder does not support multi-channel input, such as the 5.1 channel configuration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00e60-106">Для версий Windows, предшествовавших Windows 8, реализация технологий Dolby Digital в корпорации Майкрософт ограничена условиями программы цифрового лицензирования Dolby, используемой приложениями Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="00e60-106">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="00e60-107">Дополнительные сведения о цифровом звуковом стандарте Dolby см. в документе по расширенному телевидению *цифрового звука (AC-3, E-AC-3) версии B*.</span><span class="sxs-lookup"><span data-stu-id="00e60-107">For more information about Dolby Digital audio, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="00e60-108">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="00e60-108">Class Identifier</span></span>

<span data-ttu-id="00e60-109">Идентификатор класса (CLSID) кодировщика Dolby Audio — это **CLSID \_ кмсдолбидигиталенкмфт**, определенный в файле заголовка вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="00e60-109">The class identifier (CLSID) of the Dolby audio encoder is **CLSID\_CMSDolbyDigitalEncMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="00e60-110">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="00e60-110">Output Types</span></span>

<span data-ttu-id="00e60-111">Тип выходных данных должен быть задан первым, перед входным типом.</span><span class="sxs-lookup"><span data-stu-id="00e60-111">The output type must be set first, before the input type.</span></span> <span data-ttu-id="00e60-112">В следующей таблице перечислены обязательные и необязательные атрибуты для выходного типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="00e60-112">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00e60-113">attribute</span><span class="sxs-lookup"><span data-stu-id="00e60-113">Attribute</span></span></th>
<th><span data-ttu-id="00e60-114">Описание</span><span class="sxs-lookup"><span data-stu-id="00e60-114">Description</span></span></th>
<th><span data-ttu-id="00e60-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="00e60-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00e60-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="00e60-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="00e60-117">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="00e60-117">Major type.</span></span></td>
<td><span data-ttu-id="00e60-118">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-118">Required.</span></span> <span data-ttu-id="00e60-119">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="00e60-119">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00e60-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="00e60-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="00e60-121">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="00e60-121">Audio subtype.</span></span></td>
<td><span data-ttu-id="00e60-122">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-122">Required.</span></span> <span data-ttu-id="00e60-123">Необходимо <strong>MFAudioFormat_Dolby_AC3</strong>.</span><span class="sxs-lookup"><span data-stu-id="00e60-123">Must be <strong>MFAudioFormat_Dolby_AC3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00e60-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="00e60-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="00e60-125">Выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="00e60-125">Samples per second.</span></span></td>
<td><span data-ttu-id="00e60-126">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-126">Required.</span></span> <span data-ttu-id="00e60-127">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="00e60-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="00e60-128">32000</span><span class="sxs-lookup"><span data-stu-id="00e60-128">32000</span></span></li>
<li><span data-ttu-id="00e60-129">44100</span><span class="sxs-lookup"><span data-stu-id="00e60-129">44100</span></span></li>
<li><span data-ttu-id="00e60-130">48000</span><span class="sxs-lookup"><span data-stu-id="00e60-130">48000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00e60-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="00e60-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="00e60-132">Число каналов.</span><span class="sxs-lookup"><span data-stu-id="00e60-132">Number of channels.</span></span></td>
<td><span data-ttu-id="00e60-133">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-133">Required.</span></span> <span data-ttu-id="00e60-134">Значение должно быть либо 1 (моно), либо 2 (стерео).</span><span class="sxs-lookup"><span data-stu-id="00e60-134">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00e60-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="00e60-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="00e60-136">Указывает назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="00e60-136">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="00e60-137">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="00e60-137">Optional.</span></span> <span data-ttu-id="00e60-138">Если задано, значение должно быть 0x3ым для стерео (передний левый и правый каналы) или 0x4 для Mono (канал Front Center).</span><span class="sxs-lookup"><span data-stu-id="00e60-138">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00e60-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="00e60-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="00e60-140">Скорость потока в закодированном потоке AC-3, в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="00e60-140">Bit rate of the encoded AC-3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="00e60-141">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="00e60-141">Optional.</span></span> <span data-ttu-id="00e60-142">Допустимые значения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="00e60-142">See Remarks for valid values.</span></span> <span data-ttu-id="00e60-143">Если этот атрибут не задан, кодировщик использует битовую скорость по умолчанию, как описано в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="00e60-143">If this attribute is not set, the encoder uses a default bit rate, as described in Remarks.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="00e60-144">Если необязательные атрибуты не заданы, кодировщик добавляет их в тип мультимедиа после задания типа.</span><span class="sxs-lookup"><span data-stu-id="00e60-144">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="00e60-145">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="00e60-145">Input Types</span></span>

<span data-ttu-id="00e60-146">В следующей таблице перечислены обязательные и необязательные атрибуты для входного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="00e60-146">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00e60-147">attribute</span><span class="sxs-lookup"><span data-stu-id="00e60-147">Attribute</span></span></th>
<th><span data-ttu-id="00e60-148">Описание</span><span class="sxs-lookup"><span data-stu-id="00e60-148">Description</span></span></th>
<th><span data-ttu-id="00e60-149">Remarks</span><span class="sxs-lookup"><span data-stu-id="00e60-149">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00e60-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="00e60-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="00e60-151">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="00e60-151">Major type.</span></span></td>
<td><span data-ttu-id="00e60-152">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-152">Required.</span></span> <span data-ttu-id="00e60-153">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="00e60-153">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00e60-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="00e60-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="00e60-155">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="00e60-155">Audio subtype.</span></span></td>
<td><span data-ttu-id="00e60-156">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-156">Required.</span></span> <span data-ttu-id="00e60-157">Должен быть <strong>MFAudioFormat_PCM</strong> или <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="00e60-157">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00e60-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="00e60-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="00e60-159">Число битов на аудио выборка.</span><span class="sxs-lookup"><span data-stu-id="00e60-159">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="00e60-160">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-160">Required.</span></span> <span data-ttu-id="00e60-161">Значение должно быть 16, если подтип имеет <strong>MFAudioFormat_PCM</strong>, или 32, если подтип имеет <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="00e60-161">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00e60-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="00e60-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="00e60-163">Выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="00e60-163">Samples per second.</span></span></td>
<td><span data-ttu-id="00e60-164">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-164">Required.</span></span> <span data-ttu-id="00e60-165">Должен соответствовать типу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="00e60-165">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00e60-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="00e60-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="00e60-167">Число каналов.</span><span class="sxs-lookup"><span data-stu-id="00e60-167">Number of channels.</span></span></td>
<td><span data-ttu-id="00e60-168">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-168">Required.</span></span> <span data-ttu-id="00e60-169">Должен соответствовать типу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="00e60-169">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00e60-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="00e60-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="00e60-171">Выравнивание блокировки в байтах.</span><span class="sxs-lookup"><span data-stu-id="00e60-171">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="00e60-172">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-172">Required.</span></span> <span data-ttu-id="00e60-173">Вычислите значение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="00e60-173">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="00e60-174"><strong>MFAudioFormat_PCM</strong>: число каналов × 2.</span><span class="sxs-lookup"><span data-stu-id="00e60-174"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="00e60-175"><strong>MFAudioFormat_Float</strong>: число каналов × 4.</span><span class="sxs-lookup"><span data-stu-id="00e60-175"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00e60-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="00e60-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="00e60-177">Битовая скорость закодированного потока AC3 в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="00e60-177">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="00e60-178">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="00e60-178">Required.</span></span> <span data-ttu-id="00e60-179">Должно равняться выравниванию блока × Samples в секунду.</span><span class="sxs-lookup"><span data-stu-id="00e60-179">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00e60-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="00e60-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="00e60-181">Указывает назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="00e60-181">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="00e60-182">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="00e60-182">Optional.</span></span> <span data-ttu-id="00e60-183">Если параметр задан, значение должно соответствовать типу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="00e60-183">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00e60-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="00e60-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="00e60-185">Количество допустимых битов звуковых данных в каждом звуковом примере.</span><span class="sxs-lookup"><span data-stu-id="00e60-185">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="00e60-186">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="00e60-186">Optional.</span></span> <span data-ttu-id="00e60-187">Если значение задано, оно должно быть идентично значению <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="00e60-187">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="00e60-188">Кодировщик не поддерживает преобразование "выборка" или "стерео/моно".</span><span class="sxs-lookup"><span data-stu-id="00e60-188">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span>

## <a name="remarks"></a><span data-ttu-id="00e60-189">Remarks</span><span class="sxs-lookup"><span data-stu-id="00e60-189">Remarks</span></span>

<span data-ttu-id="00e60-190">Каждый звуковой кадр Dolby AC-3 содержит 1536 аудио образцов на канал.</span><span class="sxs-lookup"><span data-stu-id="00e60-190">Each Dolby AC-3 audio frame contains 1536 audio samples per channel.</span></span> <span data-ttu-id="00e60-191">Однако каждый входной буфер кодировщика может содержать любое количество примеров PCM.</span><span class="sxs-lookup"><span data-stu-id="00e60-191">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="00e60-192">Размер каждого входного буфера должен быть кратен выравниванию блока.</span><span class="sxs-lookup"><span data-stu-id="00e60-192">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="00e60-193">Кодировщик кэширует входные примеры, пока не будет достаточно для 1536 аудио образцов на канал. на этом этапе кодировщик выводит один кадр AC-3.</span><span class="sxs-lookup"><span data-stu-id="00e60-193">The encoder caches input samples until it has enough for 1536 audio samples per channel; at which point the encoder outputs one AC-3 frame.</span></span>

<span data-ttu-id="00e60-194">Каждый выходной буфер содержит один необработанный кадр AC-3.</span><span class="sxs-lookup"><span data-stu-id="00e60-194">Each output buffer contains one raw AC-3 frame.</span></span> <span data-ttu-id="00e60-195">Длительность будет равна длительности 1536 выборки PCM по текущей частоте выборки (32 МС) в 48 кГц выборка, 34,83 МС в 44,1 кГц и 48 МС в 32 кГц).</span><span class="sxs-lookup"><span data-stu-id="00e60-195">The duration is equivalent to the duration of 1536 PCM samples at the current sampling rate (32 msec) at 48 kHz sample rate, 34.83 msec at 44.1 kHz, and 48 msec at 32 kHz).</span></span> <span data-ttu-id="00e60-196">Размер каждого выходного буфера зависит от скорости потока и частоты выборки.</span><span class="sxs-lookup"><span data-stu-id="00e60-196">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

<span data-ttu-id="00e60-197">Чтобы задать скорость кодирования, установите атрибут " [ \_ \_ \_ Среднее \_ число байт в секунду" \_ для \_ звукового сигнала MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) в типе вывода.</span><span class="sxs-lookup"><span data-stu-id="00e60-197">To specify the encoding bit rate, set the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output type.</span></span> <span data-ttu-id="00e60-198">В следующей таблице показана связь между скоростью кодирования и \_ \_ \_ средним числом звуковых аудиоданных MF \_ \_ в \_ секунду.</span><span class="sxs-lookup"><span data-stu-id="00e60-198">The following table shows the relation between encoding bit rate and MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND.</span></span>



| <span data-ttu-id="00e60-199">Скорость потока (кбит/с)</span><span class="sxs-lookup"><span data-stu-id="00e60-199">Bit rate (kbps)</span></span> | [<span data-ttu-id="00e60-200">\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT</span><span class="sxs-lookup"><span data-stu-id="00e60-200">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="00e60-201">Remarks</span><span class="sxs-lookup"><span data-stu-id="00e60-201">Remarks</span></span>                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="00e60-202">64</span><span class="sxs-lookup"><span data-stu-id="00e60-202">64</span></span>              | <span data-ttu-id="00e60-203">8000</span><span class="sxs-lookup"><span data-stu-id="00e60-203">8000</span></span>                                                                                     | <span data-ttu-id="00e60-204">Только моно.</span><span class="sxs-lookup"><span data-stu-id="00e60-204">Mono only.</span></span>                                              |
| <span data-ttu-id="00e60-205">80</span><span class="sxs-lookup"><span data-stu-id="00e60-205">80</span></span>              | <span data-ttu-id="00e60-206">10000</span><span class="sxs-lookup"><span data-stu-id="00e60-206">10000</span></span>                                                                                    | <span data-ttu-id="00e60-207">Только моно.</span><span class="sxs-lookup"><span data-stu-id="00e60-207">Mono only.</span></span>                                              |
| <span data-ttu-id="00e60-208">96</span><span class="sxs-lookup"><span data-stu-id="00e60-208">96</span></span>              | <span data-ttu-id="00e60-209">12000</span><span class="sxs-lookup"><span data-stu-id="00e60-209">12000</span></span>                                                                                    | <span data-ttu-id="00e60-210">Только моно.</span><span class="sxs-lookup"><span data-stu-id="00e60-210">Mono only.</span></span>                                              |
| <span data-ttu-id="00e60-211">112</span><span class="sxs-lookup"><span data-stu-id="00e60-211">112</span></span>             | <span data-ttu-id="00e60-212">14000</span><span class="sxs-lookup"><span data-stu-id="00e60-212">14000</span></span>                                                                                    | <span data-ttu-id="00e60-213">Только моно.</span><span class="sxs-lookup"><span data-stu-id="00e60-213">Mono only.</span></span>                                              |
| <span data-ttu-id="00e60-214">128</span><span class="sxs-lookup"><span data-stu-id="00e60-214">128</span></span>             | <span data-ttu-id="00e60-215">16000</span><span class="sxs-lookup"><span data-stu-id="00e60-215">16000</span></span>                                                                                    | <span data-ttu-id="00e60-216">Моно или стерео.</span><span class="sxs-lookup"><span data-stu-id="00e60-216">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="00e60-217">160</span><span class="sxs-lookup"><span data-stu-id="00e60-217">160</span></span>             | <span data-ttu-id="00e60-218">20 000</span><span class="sxs-lookup"><span data-stu-id="00e60-218">20000</span></span>                                                                                    | <span data-ttu-id="00e60-219">Моно или стерео.</span><span class="sxs-lookup"><span data-stu-id="00e60-219">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="00e60-220">192</span><span class="sxs-lookup"><span data-stu-id="00e60-220">192</span></span>             | <span data-ttu-id="00e60-221">24 000</span><span class="sxs-lookup"><span data-stu-id="00e60-221">24000</span></span>                                                                                    | <span data-ttu-id="00e60-222">Моно или стерео.</span><span class="sxs-lookup"><span data-stu-id="00e60-222">Mono or stereo.</span></span> <span data-ttu-id="00e60-223">Это значение по умолчанию для Mono.</span><span class="sxs-lookup"><span data-stu-id="00e60-223">This is the default setting for mono.</span></span>   |
| <span data-ttu-id="00e60-224">224</span><span class="sxs-lookup"><span data-stu-id="00e60-224">224</span></span>             | <span data-ttu-id="00e60-225">28000</span><span class="sxs-lookup"><span data-stu-id="00e60-225">28000</span></span>                                                                                    | <span data-ttu-id="00e60-226">Моно или стерео.</span><span class="sxs-lookup"><span data-stu-id="00e60-226">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="00e60-227">256</span><span class="sxs-lookup"><span data-stu-id="00e60-227">256</span></span>             | <span data-ttu-id="00e60-228">32000</span><span class="sxs-lookup"><span data-stu-id="00e60-228">32000</span></span>                                                                                    | <span data-ttu-id="00e60-229">Моно или стерео.</span><span class="sxs-lookup"><span data-stu-id="00e60-229">Mono or stereo.</span></span> <span data-ttu-id="00e60-230">Это значение по умолчанию для стерео.</span><span class="sxs-lookup"><span data-stu-id="00e60-230">This is the default setting for stereo.</span></span> |
| <span data-ttu-id="00e60-231">320</span><span class="sxs-lookup"><span data-stu-id="00e60-231">320</span></span>             | <span data-ttu-id="00e60-232">40 000</span><span class="sxs-lookup"><span data-stu-id="00e60-232">40000</span></span>                                                                                    | <span data-ttu-id="00e60-233">Только стерео.</span><span class="sxs-lookup"><span data-stu-id="00e60-233">Stereo only.</span></span>                                            |
| <span data-ttu-id="00e60-234">384</span><span class="sxs-lookup"><span data-stu-id="00e60-234">384</span></span>             | <span data-ttu-id="00e60-235">48000</span><span class="sxs-lookup"><span data-stu-id="00e60-235">48000</span></span>                                                                                    | <span data-ttu-id="00e60-236">Только стерео.</span><span class="sxs-lookup"><span data-stu-id="00e60-236">Stereo only.</span></span>                                            |
| <span data-ttu-id="00e60-237">448</span><span class="sxs-lookup"><span data-stu-id="00e60-237">448</span></span>             | <span data-ttu-id="00e60-238">56000</span><span class="sxs-lookup"><span data-stu-id="00e60-238">56000</span></span>                                                                                    | <span data-ttu-id="00e60-239">Только стерео.</span><span class="sxs-lookup"><span data-stu-id="00e60-239">Stereo only.</span></span>                                            |



 

<span data-ttu-id="00e60-240">Скорость кодирования по умолчанию устанавливается в 256 кбит/с для стерео и 192 кбит/с для Mono.</span><span class="sxs-lookup"><span data-stu-id="00e60-240">The default encoding bit rate is set at 256 kbps for stereo and 192 kbps for mono.</span></span> <span data-ttu-id="00e60-241">Параметры по умолчанию отражаются в типах носителей, возвращаемых методом [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) кодировщика.</span><span class="sxs-lookup"><span data-stu-id="00e60-241">The default settings are reflected in the media types returned by the encoder's [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

### <a name="example-media-types"></a><span data-ttu-id="00e60-242">Примеры типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="00e60-242">Example Media Types</span></span>

<span data-ttu-id="00e60-243">Ниже приведен пример типов мультимедиа, которые необходимы для кодирования 16-разрядного целочисленного PCM 48-кГц при скорости по умолчанию 256 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="00e60-243">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate of 256 kbps.</span></span>

<span data-ttu-id="00e60-244">Тип выходного носителя:</span><span class="sxs-lookup"><span data-stu-id="00e60-244">Output media type:</span></span>

| <span data-ttu-id="00e60-245">attribute</span><span class="sxs-lookup"><span data-stu-id="00e60-245">Attribute</span></span>                                                                           | <span data-ttu-id="00e60-246">Значение</span><span class="sxs-lookup"><span data-stu-id="00e60-246">Value</span></span>                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="00e60-247">\_ \_ основной тип MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="00e60-247">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="00e60-248">**Мфмедиатипе \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="00e60-248">**MFMediaType\_Audio**</span></span>        |
| [<span data-ttu-id="00e60-249">подтип MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="00e60-249">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="00e60-250">**Мфаудиоформат \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="00e60-250">**MFAudioFormat\_Dolby\_AC3**</span></span> |
| [<span data-ttu-id="00e60-251">\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду</span><span class="sxs-lookup"><span data-stu-id="00e60-251">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="00e60-252">48000</span><span class="sxs-lookup"><span data-stu-id="00e60-252">48000</span></span>                         |
| [<span data-ttu-id="00e60-253">\_ \_ каналы аудиосигнала MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="00e60-253">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="00e60-254">2</span><span class="sxs-lookup"><span data-stu-id="00e60-254">2</span></span>                             |



 

<span data-ttu-id="00e60-255">Тип входного носителя:</span><span class="sxs-lookup"><span data-stu-id="00e60-255">Input media type:</span></span>

| <span data-ttu-id="00e60-256">attribute</span><span class="sxs-lookup"><span data-stu-id="00e60-256">Attribute</span></span>                                                                                | <span data-ttu-id="00e60-257">Значение</span><span class="sxs-lookup"><span data-stu-id="00e60-257">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="00e60-258">\_ \_ основной тип MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="00e60-258">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="00e60-259">**Мфмедиатипе \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="00e60-259">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="00e60-260">подтип MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="00e60-260">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="00e60-261">**Мфаудиоформат \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="00e60-261">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="00e60-262">\_ \_ звуковый бит MF MT \_ \_ на \_ выборку</span><span class="sxs-lookup"><span data-stu-id="00e60-262">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="00e60-263">16</span><span class="sxs-lookup"><span data-stu-id="00e60-263">16</span></span>                     |
| [<span data-ttu-id="00e60-264">\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду</span><span class="sxs-lookup"><span data-stu-id="00e60-264">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="00e60-265">48000</span><span class="sxs-lookup"><span data-stu-id="00e60-265">48000</span></span>                  |
| [<span data-ttu-id="00e60-266">\_ \_ каналы аудиосигнала MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="00e60-266">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="00e60-267">2</span><span class="sxs-lookup"><span data-stu-id="00e60-267">2</span></span>                      |
| [<span data-ttu-id="00e60-268">\_ \_ Выравнивание звукового \_ блока MF MT \_</span><span class="sxs-lookup"><span data-stu-id="00e60-268">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="00e60-269">4</span><span class="sxs-lookup"><span data-stu-id="00e60-269">4</span></span>                      |
| [<span data-ttu-id="00e60-270">\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT</span><span class="sxs-lookup"><span data-stu-id="00e60-270">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="00e60-271">192000</span><span class="sxs-lookup"><span data-stu-id="00e60-271">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="00e60-272">Требования</span><span class="sxs-lookup"><span data-stu-id="00e60-272">Requirements</span></span>



| <span data-ttu-id="00e60-273">Требование</span><span class="sxs-lookup"><span data-stu-id="00e60-273">Requirement</span></span> | <span data-ttu-id="00e60-274">Значение</span><span class="sxs-lookup"><span data-stu-id="00e60-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00e60-275">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00e60-275">Minimum supported client</span></span><br/> | <span data-ttu-id="00e60-276">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="00e60-276">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                       |
| <span data-ttu-id="00e60-277">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00e60-277">Minimum supported server</span></span><br/> | <span data-ttu-id="00e60-278">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="00e60-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="00e60-279">DLL</span><span class="sxs-lookup"><span data-stu-id="00e60-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00e60-280"><dt>Msac3enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00e60-280"><dt>Msac3enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00e60-281">См. также</span><span class="sxs-lookup"><span data-stu-id="00e60-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e60-282">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="00e60-282">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 




