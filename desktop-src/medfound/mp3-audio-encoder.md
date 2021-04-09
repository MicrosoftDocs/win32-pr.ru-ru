---
description: Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: Кодировщик аудио MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080435"
---
# <a name="mp3-audio-encoder"></a><span data-ttu-id="8bd27-103">Кодировщик аудио MP3</span><span class="sxs-lookup"><span data-stu-id="8bd27-103">MP3 Audio Encoder</span></span>

<span data-ttu-id="8bd27-104">Кодировщик Microsoft Media Foundation MP3 Audio — это [Media Foundation преобразование](media-foundation-transforms.md) (MFT), которое КОДИРУЕТ аудио MPEG-1 третьего уровня (MP3).</span><span class="sxs-lookup"><span data-stu-id="8bd27-104">The Microsoft Media Foundation MP3 audio encoder is a [Media Foundation Transform](media-foundation-transforms.md) (MFT) that encodes MPEG-1 layer 3 (MP3) audio.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="8bd27-105">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="8bd27-105">Class Identifier</span></span>

<span data-ttu-id="8bd27-106">Идентификатор класса (CLSID) кодировщика MP3 — это **CLSID \_ MP3ACMCodecWrapper**, определенный в файле заголовка вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="8bd27-106">The class identifier (CLSID) of the MP3 encoder is **CLSID\_MP3ACMCodecWrapper**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="8bd27-107">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="8bd27-107">Media Types</span></span>

<span data-ttu-id="8bd27-108">Кодировщик MP3 поддерживает следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="8bd27-108">The MP3 encoder supports the following media types.</span></span> <span data-ttu-id="8bd27-109">Тип выходных данных должен быть задан перед входным типом.</span><span class="sxs-lookup"><span data-stu-id="8bd27-109">The output type must be set before the input type.</span></span>

### <a name="output-types"></a><span data-ttu-id="8bd27-110">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="8bd27-110">Output Types</span></span>

<span data-ttu-id="8bd27-111">Задайте следующие атрибуты для выходного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="8bd27-111">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8bd27-112">attribute</span><span class="sxs-lookup"><span data-stu-id="8bd27-112">Attribute</span></span></th>
<th><span data-ttu-id="8bd27-113">Описание</span><span class="sxs-lookup"><span data-stu-id="8bd27-113">Description</span></span></th>
<th><span data-ttu-id="8bd27-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="8bd27-114">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8bd27-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bd27-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="8bd27-116">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="8bd27-116">Major type.</span></span></td>
<td><span data-ttu-id="8bd27-117">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="8bd27-117">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bd27-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bd27-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="8bd27-119">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="8bd27-119">Audio subtype.</span></span></td>
<td><span data-ttu-id="8bd27-120">Необходимо <strong>MFAudioFormat_MP3</strong>.</span><span class="sxs-lookup"><span data-stu-id="8bd27-120">Must be <strong>MFAudioFormat_MP3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bd27-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bd27-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="8bd27-122">Скорость потока в закодированном потоке MP3, в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="8bd27-122">Bit rate of the encoded MP3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="8bd27-123">Кодировщик поддерживает все скорости, определенные стандартом (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 или 320 кбит/с).</span><span class="sxs-lookup"><span data-stu-id="8bd27-123">The encoder supports all bit rates defined by the standard (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, or 320 Kbps).</span></span><br/> <span data-ttu-id="8bd27-124">Скорость по умолчанию составляет 128 кбит/с для стерео и 320 кбит/с для стереосистемы.</span><span class="sxs-lookup"><span data-stu-id="8bd27-124">The default bit rates are 128 Kbps for mono and 320 Kbps for stereo.</span></span><br/> <span data-ttu-id="8bd27-125">Используйте этот атрибут, чтобы указать закодированную скорость.</span><span class="sxs-lookup"><span data-stu-id="8bd27-125">Use this attribute to specify the encoded bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bd27-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bd27-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="8bd27-127">Число каналов.</span><span class="sxs-lookup"><span data-stu-id="8bd27-127">Number of channels.</span></span></td>
<td><span data-ttu-id="8bd27-128">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8bd27-128">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="8bd27-129">1 (моно)</span><span class="sxs-lookup"><span data-stu-id="8bd27-129">1 (mono)</span></span></li>
<li><span data-ttu-id="8bd27-130">2 (стерео)</span><span class="sxs-lookup"><span data-stu-id="8bd27-130">2 (stereo)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bd27-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bd27-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="8bd27-132">Выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="8bd27-132">Samples per second.</span></span></td>
<td><span data-ttu-id="8bd27-133">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8bd27-133">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="8bd27-134">48000 (48 кГц)</span><span class="sxs-lookup"><span data-stu-id="8bd27-134">48000 (48 KHz)</span></span></li>
<li><span data-ttu-id="8bd27-135">44100 (44,1 кГц)</span><span class="sxs-lookup"><span data-stu-id="8bd27-135">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="8bd27-136">32000 (32 кГц)</span><span class="sxs-lookup"><span data-stu-id="8bd27-136">32000 (32 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bd27-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span><span class="sxs-lookup"><span data-stu-id="8bd27-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span></span></td>
<td><span data-ttu-id="8bd27-138">Дополнительные данные кодека.</span><span class="sxs-lookup"><span data-stu-id="8bd27-138">Additional codec data.</span></span></td>
<td><span data-ttu-id="8bd27-139">Этот атрибут содержит 12 байт структуры <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> , которые следуют за элементом <strong>вфкс</strong> этой структуры.</span><span class="sxs-lookup"><span data-stu-id="8bd27-139">This attribute contains the 12 bytes of the <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> structure that follow the <strong>wfx</strong> member of that structure.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8bd27-140">Кроме того, можно заполнить структуру [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) и вызвать [**мфинитмедиатипефромвавеформатекс**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) , чтобы преобразовать структуру в Media Foundation тип носителя.</span><span class="sxs-lookup"><span data-stu-id="8bd27-140">Alternatively, you can fill in an [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure and call [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) to convert the structure to a Media Foundation media type.</span></span>

### <a name="input-types"></a><span data-ttu-id="8bd27-141">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="8bd27-141">Input Types</span></span>

<span data-ttu-id="8bd27-142">Задайте следующие атрибуты для входного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="8bd27-142">Set the following attributes on the input media type.</span></span>



| <span data-ttu-id="8bd27-143">attribute</span><span class="sxs-lookup"><span data-stu-id="8bd27-143">Attribute</span></span>                                                                               | <span data-ttu-id="8bd27-144">Описание</span><span class="sxs-lookup"><span data-stu-id="8bd27-144">Description</span></span>         | <span data-ttu-id="8bd27-145">Remarks</span><span class="sxs-lookup"><span data-stu-id="8bd27-145">Remarks</span></span>                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [<span data-ttu-id="8bd27-146">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="8bd27-146">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="8bd27-147">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="8bd27-147">Major type.</span></span>         | <span data-ttu-id="8bd27-148">Должен быть **мфмедиатипе \_ Audio**.</span><span class="sxs-lookup"><span data-stu-id="8bd27-148">Must be **MFMediaType\_Audio**.</span></span> |
| [<span data-ttu-id="8bd27-149">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="8bd27-149">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="8bd27-150">Подтип.</span><span class="sxs-lookup"><span data-stu-id="8bd27-150">Subtype.</span></span>            | <span data-ttu-id="8bd27-151">Должен быть **мфаудиоформат \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="8bd27-151">Must be **MFAudioFormat\_PCM**.</span></span> |
| [<span data-ttu-id="8bd27-152">**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**</span><span class="sxs-lookup"><span data-stu-id="8bd27-152">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="8bd27-153">Бит на выборку.</span><span class="sxs-lookup"><span data-stu-id="8bd27-153">Bits per sample.</span></span>    | <span data-ttu-id="8bd27-154">Должно быть 16.</span><span class="sxs-lookup"><span data-stu-id="8bd27-154">Must be 16.</span></span>                     |
| [<span data-ttu-id="8bd27-155">**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="8bd27-155">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="8bd27-156">Выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="8bd27-156">Samples per second.</span></span> | <span data-ttu-id="8bd27-157">Должен соответствовать типу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8bd27-157">Must match the output type.</span></span>     |
| [<span data-ttu-id="8bd27-158">**\_ \_ каналы аудиосигнала MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8bd27-158">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="8bd27-159">Число каналов.</span><span class="sxs-lookup"><span data-stu-id="8bd27-159">Number of channels.</span></span> | <span data-ttu-id="8bd27-160">Должен соответствовать типу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8bd27-160">Must match the output type.</span></span>     |



 

<span data-ttu-id="8bd27-161">Кодировщик поддерживает только 16-разрядные целочисленные входные данные PCM.</span><span class="sxs-lookup"><span data-stu-id="8bd27-161">The encoder supports only 16-bit integer PCM input.</span></span> <span data-ttu-id="8bd27-162">Он не поддерживает 32-разрядные входные данные с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="8bd27-162">It does not support 32-bit floating point input.</span></span>

### <a name="media-formats"></a><span data-ttu-id="8bd27-163">Форматы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8bd27-163">Media Formats</span></span>

<span data-ttu-id="8bd27-164">Стандарт MPEG-1 и MPEG-2 определяет звуковые форматы 252 уровня 3.</span><span class="sxs-lookup"><span data-stu-id="8bd27-164">The MPEG-1 and MPEG-2 standard defines 252 layer 3 audio formats.</span></span> <span data-ttu-id="8bd27-165">Кодировщик MP3 поддерживает стандарт с некоторыми исключениями, а также некоторые дополнительные форматы, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="8bd27-165">The MP3 encoder supports the standard with some exceptions, as well as some additional formats, as described below.</span></span> <span data-ttu-id="8bd27-166">Уровень 3 определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8bd27-166">Layer 3 is defined as:</span></span>



| <span data-ttu-id="8bd27-167">Требование</span><span class="sxs-lookup"><span data-stu-id="8bd27-167">Requirement</span></span> | <span data-ttu-id="8bd27-168">Значение</span><span class="sxs-lookup"><span data-stu-id="8bd27-168">Value</span></span> |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8bd27-169">Каналы</span><span class="sxs-lookup"><span data-stu-id="8bd27-169">Channels</span></span>                         | <span data-ttu-id="8bd27-170">моно или стерео</span><span class="sxs-lookup"><span data-stu-id="8bd27-170">mono or stereo</span></span>                                                |
| <span data-ttu-id="8bd27-171">Частота дискретизации MPEG-1 в кГц</span><span class="sxs-lookup"><span data-stu-id="8bd27-171">MPEG-1 sample rates in kHz</span></span>       | <span data-ttu-id="8bd27-172">44,1, 48, 32</span><span class="sxs-lookup"><span data-stu-id="8bd27-172">44.1, 48, 32</span></span>                                                  |
| <span data-ttu-id="8bd27-173">Скорость кодирования MPEG-1 в кбит/с</span><span class="sxs-lookup"><span data-stu-id="8bd27-173">MPEG-1 encoded bit rates in kbps</span></span> | <span data-ttu-id="8bd27-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span><span class="sxs-lookup"><span data-stu-id="8bd27-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span></span> |
| <span data-ttu-id="8bd27-175">Частота дискретизации MPEG-2 в кГц</span><span class="sxs-lookup"><span data-stu-id="8bd27-175">MPEG-2 sample rates in kHz</span></span>       | <span data-ttu-id="8bd27-176">8, 11,025, 12, 16, 22,05, 24</span><span class="sxs-lookup"><span data-stu-id="8bd27-176">8, 11.025, 12, 16, 22.05, 24</span></span>                                  |
| <span data-ttu-id="8bd27-177">Скорость кодирования MPEG-2 в кбит/с</span><span class="sxs-lookup"><span data-stu-id="8bd27-177">MPEG-2 encoded bit rates in kbps</span></span> | <span data-ttu-id="8bd27-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span><span class="sxs-lookup"><span data-stu-id="8bd27-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span></span>          |



 

<span data-ttu-id="8bd27-179">Кодировщик MP3 также поддерживает следующие форматы.</span><span class="sxs-lookup"><span data-stu-id="8bd27-179">The MP3 encoder also supports the following formats.</span></span>



| <span data-ttu-id="8bd27-180">Частота выборки</span><span class="sxs-lookup"><span data-stu-id="8bd27-180">Sample Rate</span></span> | <span data-ttu-id="8bd27-181">Скорость</span><span class="sxs-lookup"><span data-stu-id="8bd27-181">Bit Rate</span></span>     | <span data-ttu-id="8bd27-182">Номер канала</span><span class="sxs-lookup"><span data-stu-id="8bd27-182">Channel Number</span></span> |
|-------------|--------------|----------------|
| <span data-ttu-id="8bd27-183">8000</span><span class="sxs-lookup"><span data-stu-id="8bd27-183">8000</span></span>        | <span data-ttu-id="8bd27-184">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="8bd27-184">18000, 20000</span></span> | <span data-ttu-id="8bd27-185">2</span><span class="sxs-lookup"><span data-stu-id="8bd27-185">2</span></span>              |
| <span data-ttu-id="8bd27-186">11025</span><span class="sxs-lookup"><span data-stu-id="8bd27-186">11025</span></span>       | <span data-ttu-id="8bd27-187">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="8bd27-187">18000, 20000</span></span> | <span data-ttu-id="8bd27-188">1 или 2</span><span class="sxs-lookup"><span data-stu-id="8bd27-188">1 or 2</span></span>         |
| <span data-ttu-id="8bd27-189">12000</span><span class="sxs-lookup"><span data-stu-id="8bd27-189">12000</span></span>       | <span data-ttu-id="8bd27-190">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="8bd27-190">18000, 20000</span></span> | <span data-ttu-id="8bd27-191">1 или 2</span><span class="sxs-lookup"><span data-stu-id="8bd27-191">1 or 2</span></span>         |
| <span data-ttu-id="8bd27-192">16000</span><span class="sxs-lookup"><span data-stu-id="8bd27-192">16000</span></span>       | <span data-ttu-id="8bd27-193">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="8bd27-193">18000, 20000</span></span> | <span data-ttu-id="8bd27-194">1</span><span class="sxs-lookup"><span data-stu-id="8bd27-194">1</span></span>              |
| <span data-ttu-id="8bd27-195">32000</span><span class="sxs-lookup"><span data-stu-id="8bd27-195">32000</span></span>       | <span data-ttu-id="8bd27-196">144000</span><span class="sxs-lookup"><span data-stu-id="8bd27-196">144000</span></span>       | <span data-ttu-id="8bd27-197">1 или 2</span><span class="sxs-lookup"><span data-stu-id="8bd27-197">1 or 2</span></span>         |
| <span data-ttu-id="8bd27-198">44100</span><span class="sxs-lookup"><span data-stu-id="8bd27-198">44100</span></span>       | <span data-ttu-id="8bd27-199">144000</span><span class="sxs-lookup"><span data-stu-id="8bd27-199">144000</span></span>       | <span data-ttu-id="8bd27-200">1 или 2</span><span class="sxs-lookup"><span data-stu-id="8bd27-200">1 or 2</span></span>         |
| <span data-ttu-id="8bd27-201">48000</span><span class="sxs-lookup"><span data-stu-id="8bd27-201">48000</span></span>       | <span data-ttu-id="8bd27-202">144000</span><span class="sxs-lookup"><span data-stu-id="8bd27-202">144000</span></span>       | <span data-ttu-id="8bd27-203">1 или 2</span><span class="sxs-lookup"><span data-stu-id="8bd27-203">1 or 2</span></span>         |



 

<span data-ttu-id="8bd27-204">Кодировщик MP3 не поддерживает следующие форматы, определенные стандартом.</span><span class="sxs-lookup"><span data-stu-id="8bd27-204">The MP3 encoder does not support the following formats defined by the standard.</span></span>



| <span data-ttu-id="8bd27-205">Частота выборки</span><span class="sxs-lookup"><span data-stu-id="8bd27-205">Sample Rate</span></span> | <span data-ttu-id="8bd27-206">Скорость передачи</span><span class="sxs-lookup"><span data-stu-id="8bd27-206">Bit Rates</span></span>                                    | <span data-ttu-id="8bd27-207">Номер канала</span><span class="sxs-lookup"><span data-stu-id="8bd27-207">Channel Number</span></span> |
|-------------|----------------------------------------------|----------------|
| <span data-ttu-id="8bd27-208">12000</span><span class="sxs-lookup"><span data-stu-id="8bd27-208">12000</span></span>       | <span data-ttu-id="8bd27-209">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="8bd27-209">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="8bd27-210">1 или 2</span><span class="sxs-lookup"><span data-stu-id="8bd27-210">1 or 2</span></span>         |
| <span data-ttu-id="8bd27-211">11025</span><span class="sxs-lookup"><span data-stu-id="8bd27-211">11025</span></span>       | <span data-ttu-id="8bd27-212">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="8bd27-212">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="8bd27-213">1 или 2</span><span class="sxs-lookup"><span data-stu-id="8bd27-213">1 or 2</span></span>         |
| <span data-ttu-id="8bd27-214">8000</span><span class="sxs-lookup"><span data-stu-id="8bd27-214">8000</span></span>        | <span data-ttu-id="8bd27-215">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="8bd27-215">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="8bd27-216">1 или 2</span><span class="sxs-lookup"><span data-stu-id="8bd27-216">1 or 2</span></span>         |
| <span data-ttu-id="8bd27-217">8000</span><span class="sxs-lookup"><span data-stu-id="8bd27-217">8000</span></span>        | <span data-ttu-id="8bd27-218">8000, 11025, 12000, 16000, 22050, 24000</span><span class="sxs-lookup"><span data-stu-id="8bd27-218">8000, 11025, 12000, 16000, 22050, 24000</span></span>      | <span data-ttu-id="8bd27-219">2</span><span class="sxs-lookup"><span data-stu-id="8bd27-219">2</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="8bd27-220">Требования</span><span class="sxs-lookup"><span data-stu-id="8bd27-220">Requirements</span></span>



| <span data-ttu-id="8bd27-221">Требование</span><span class="sxs-lookup"><span data-stu-id="8bd27-221">Requirement</span></span> | <span data-ttu-id="8bd27-222">Значение</span><span class="sxs-lookup"><span data-stu-id="8bd27-222">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8bd27-223">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bd27-223">Minimum supported client</span></span><br/> | <span data-ttu-id="8bd27-224">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8bd27-224">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="8bd27-225">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bd27-225">Minimum supported server</span></span><br/> | <span data-ttu-id="8bd27-226">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8bd27-226">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8bd27-227">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bd27-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd27-228">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="8bd27-228">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
