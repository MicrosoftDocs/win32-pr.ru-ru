---
description: Декодер Dolby Audio — это MFT, декодированное в формате Dolby Digital (AC-3) и Dolby Digital Plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Декодер Dolby Audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808098"
---
# <a name="dolby-audio-decoder"></a><span data-ttu-id="b37ca-103">Декодер Dolby Audio</span><span class="sxs-lookup"><span data-stu-id="b37ca-103">Dolby Audio Decoder</span></span>

<span data-ttu-id="b37ca-104">Декодер Dolby Audio — это [Media Foundation преобразование](media-foundation-transforms.md) (MFT), которое декодирует следующие типы потоков:</span><span class="sxs-lookup"><span data-stu-id="b37ca-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that decodes the following stream types:</span></span>

-   <span data-ttu-id="b37ca-105">Dolby Digital, также называемая Dolby AC-3</span><span class="sxs-lookup"><span data-stu-id="b37ca-105">Dolby Digital, also called Dolby AC-3</span></span>
-   <span data-ttu-id="b37ca-106">Dolby Digital Plus, также называемый расширенным AC-3 (E-AC-3)</span><span class="sxs-lookup"><span data-stu-id="b37ca-106">Dolby Digital Plus, also called Enhanced AC-3 (E-AC-3)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b37ca-107">Для версий Windows, предшествовавших Windows 8, реализация технологий Dolby Digital в корпорации Майкрософт ограничена условиями программы цифрового лицензирования Dolby, используемой приложениями Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b37ca-107">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="b37ca-108">Дополнительные сведения об этих форматах см. в документе по расширенному телевидению *цифрового звука (AC-3, E-AC-3) версии B*.</span><span class="sxs-lookup"><span data-stu-id="b37ca-108">For more information about these formats, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

<span data-ttu-id="b37ca-109">Декодер также может преобразовать поток Dolby Digital Plus в цифровой формат Dolby для вывода AC-3 S/ПИДФ или отформатировать поток Dolby Digital Plus для цифрового выхода HDMI.</span><span class="sxs-lookup"><span data-stu-id="b37ca-109">The decoder can also convert a Dolby Digital Plus stream to Dolby Digital format for AC-3 S/PIDF output, or format a Dolby Digital Plus stream for HDMI digital output.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="b37ca-110">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="b37ca-110">Class Identifier</span></span>

<span data-ttu-id="b37ca-111">Идентификатором класса (CLSID) декодера Dolby Audio является **CLSID \_ кмсддплусдекмфт**, определенный в файле заголовка вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="b37ca-111">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDDPlusDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="b37ca-112">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="b37ca-112">Input Types</span></span>

<span data-ttu-id="b37ca-113">Декодер Dolby Audio поддерживает следующие входные подтипы.</span><span class="sxs-lookup"><span data-stu-id="b37ca-113">The Dolby audio decoder supports the following input subtypes.</span></span>



| <span data-ttu-id="b37ca-114">Subtype</span><span class="sxs-lookup"><span data-stu-id="b37ca-114">Subtype</span></span>                                 | <span data-ttu-id="b37ca-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b37ca-115">Description</span></span>                                                                                                                                                 | <span data-ttu-id="b37ca-116">Header</span><span class="sxs-lookup"><span data-stu-id="b37ca-116">Header</span></span>       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="b37ca-117">**МЕДИАСУБТИПЕ \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="b37ca-117">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>            | <span data-ttu-id="b37ca-118">Dolby Digital Audio.</span><span class="sxs-lookup"><span data-stu-id="b37ca-118">Dolby Digital audio.</span></span>                                                                                                                                        | <span data-ttu-id="b37ca-119">мфапи. h</span><span class="sxs-lookup"><span data-stu-id="b37ca-119">mfapi.h</span></span>      |
| <span data-ttu-id="b37ca-120">**МЕДИАСУБТИПЕ \_ DVM**</span><span class="sxs-lookup"><span data-stu-id="b37ca-120">**MEDIASUBTYPE\_DVM**</span></span>                   | <span data-ttu-id="b37ca-121">Dolby Digital Audio; см. раздел [**аудио подтипы**](../directshow/audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="b37ca-121">Dolby Digital audio; see [**Audio Subtypes**](../directshow/audio-subtypes.md).</span></span> <span data-ttu-id="b37ca-122">Этот подтип можно использовать взаимозаменяемым с **медиасубтипе \_ Dolby \_ AC3**.</span><span class="sxs-lookup"><span data-stu-id="b37ca-122">This subtype can be used interchangeably with **MEDIASUBTYPE\_DOLBY\_AC3**.</span></span><br/> | <span data-ttu-id="b37ca-123">вмкодекдсп. h</span><span class="sxs-lookup"><span data-stu-id="b37ca-123">wmcodecdsp.h</span></span> |
| <span data-ttu-id="b37ca-124">**Мфаудиоформат \_ Dolby \_ Digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="b37ca-124">**MFAudioFormat\_Dolby\_Digital\_Plus**</span></span> | <span data-ttu-id="b37ca-125">Dolby Digital Plus Audio.</span><span class="sxs-lookup"><span data-stu-id="b37ca-125">Dolby Digital Plus audio.</span></span>                                                                                                                                   | <span data-ttu-id="b37ca-126">мфапи. h</span><span class="sxs-lookup"><span data-stu-id="b37ca-126">mfapi.h</span></span>      |



 

<span data-ttu-id="b37ca-127">В следующей таблице перечислены необходимые и необязательные атрибуты для входного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="b37ca-127">The following table lists the requires and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b37ca-128">attribute</span><span class="sxs-lookup"><span data-stu-id="b37ca-128">Attribute</span></span></th>
<th><span data-ttu-id="b37ca-129">Описание</span><span class="sxs-lookup"><span data-stu-id="b37ca-129">Description</span></span></th>
<th><span data-ttu-id="b37ca-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="b37ca-130">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b37ca-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="b37ca-132">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="b37ca-132">Major type.</span></span></td>
<td><span data-ttu-id="b37ca-133">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b37ca-133">Required.</span></span> <span data-ttu-id="b37ca-134">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="b37ca-134">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="b37ca-136">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="b37ca-136">Audio subtype.</span></span></td>
<td><span data-ttu-id="b37ca-137">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b37ca-137">Required.</span></span> <span data-ttu-id="b37ca-138">Дополнительные сведения см. в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="b37ca-138">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="b37ca-140">Частота выборки, в примерах в секунду.</span><span class="sxs-lookup"><span data-stu-id="b37ca-140">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="b37ca-141">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="b37ca-141">Optional.</span></span> <span data-ttu-id="b37ca-142">Допустимые значения: 48000, 44100, 32000, 24000, 22050 и 16000.</span><span class="sxs-lookup"><span data-stu-id="b37ca-142">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="b37ca-143">Если этот атрибут не задан, по умолчанию используется значение 48000.</span><span class="sxs-lookup"><span data-stu-id="b37ca-143">If this attribute is not set, the default value is 48000.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b37ca-144">Потоки Dolby AC-3 ограничиваются тремя самыми высокими тарифами в этом списке.</span><span class="sxs-lookup"><span data-stu-id="b37ca-144">Dolby AC-3 streams are limited to the three highest rates in this list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="b37ca-146">Количество каналов, включая канал с низкой частотой (НИЗКОЧАСТОТный), если он есть.</span><span class="sxs-lookup"><span data-stu-id="b37ca-146">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="b37ca-147">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="b37ca-147">Optional.</span></span> <span data-ttu-id="b37ca-148">Допустимые значения находятся в диапазоне от 1 (моно) до 8 (Конфигурация канала 7,1).</span><span class="sxs-lookup"><span data-stu-id="b37ca-148">Valid values are in the range 1 (mono) to 8 (7.1 channel configuration).</span></span> <span data-ttu-id="b37ca-149">Если этот атрибут не задан, по умолчанию используется значение 2 (стерео).</span><span class="sxs-lookup"><span data-stu-id="b37ca-149">If this attribute is not set, the default value is 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="b37ca-151">Указывает назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="b37ca-151">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="b37ca-152">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="b37ca-152">Optional.</span></span> <span data-ttu-id="b37ca-153">Если указано, значение должно соответствовать числу звуковых каналов.</span><span class="sxs-lookup"><span data-stu-id="b37ca-153">If specified, the value must be consistent with the number of audio channels.</span></span> <span data-ttu-id="b37ca-154">Если атрибут не задан, декодер использует маску канала по умолчанию на основе числа каналов.</span><span class="sxs-lookup"><span data-stu-id="b37ca-154">If the attribute is not set, the decoder uses a default channel mask, based on the number of channels.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b37ca-155">В следующей таблице перечислены поддерживаемые конфигурации канала Dolby.</span><span class="sxs-lookup"><span data-stu-id="b37ca-155">The following table lists the supported Dolby channel configurations.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b37ca-156">Конфигурация канала</span><span class="sxs-lookup"><span data-stu-id="b37ca-156">Channel configuration</span></span></th>
<th><span data-ttu-id="b37ca-157">Число каналов</span><span class="sxs-lookup"><span data-stu-id="b37ca-157">Number of channels</span></span></th>
<th><span data-ttu-id="b37ca-158">Маски каналов</span><span class="sxs-lookup"><span data-stu-id="b37ca-158">Channel masks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b37ca-159">1/0 (моно)</span><span class="sxs-lookup"><span data-stu-id="b37ca-159">1/0 (mono)</span></span></td>
<td><span data-ttu-id="b37ca-160">1</span><span class="sxs-lookup"><span data-stu-id="b37ca-160">1</span></span></td>
<td><span data-ttu-id="b37ca-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-162">2/0 (стерео) или 1 + 1 (два Mono)</span><span class="sxs-lookup"><span data-stu-id="b37ca-162">2/0 (stereo) or 1+1 (dual mono)</span></span></td>
<td><span data-ttu-id="b37ca-163">2</span><span class="sxs-lookup"><span data-stu-id="b37ca-163">2</span></span></td>
<td><span data-ttu-id="b37ca-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-165">3/0</span><span class="sxs-lookup"><span data-stu-id="b37ca-165">3/0</span></span></td>
<td><span data-ttu-id="b37ca-166">3</span><span class="sxs-lookup"><span data-stu-id="b37ca-166">3</span></span></td>
<td><span data-ttu-id="b37ca-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span><span class="sxs-lookup"><span data-stu-id="b37ca-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-168">2/1</span><span class="sxs-lookup"><span data-stu-id="b37ca-168">2/1</span></span></td>
<td><span data-ttu-id="b37ca-169">3</span><span class="sxs-lookup"><span data-stu-id="b37ca-169">3</span></span></td>
<td><span data-ttu-id="b37ca-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-171">3/1</span><span class="sxs-lookup"><span data-stu-id="b37ca-171">3/1</span></span></td>
<td><span data-ttu-id="b37ca-172">4</span><span class="sxs-lookup"><span data-stu-id="b37ca-172">4</span></span></td>
<td><span data-ttu-id="b37ca-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-174">2/2</span><span class="sxs-lookup"><span data-stu-id="b37ca-174">2/2</span></span></td>
<td><span data-ttu-id="b37ca-175">4</span><span class="sxs-lookup"><span data-stu-id="b37ca-175">4</span></span></td>
<td><span data-ttu-id="b37ca-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="b37ca-177">или</span><span class="sxs-lookup"><span data-stu-id="b37ca-177">or</span></span><br/> <span data-ttu-id="b37ca-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-179">3/2</span><span class="sxs-lookup"><span data-stu-id="b37ca-179">3/2</span></span></td>
<td><span data-ttu-id="b37ca-180">5</span><span class="sxs-lookup"><span data-stu-id="b37ca-180">5</span></span></td>
<td><span data-ttu-id="b37ca-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="b37ca-182">или</span><span class="sxs-lookup"><span data-stu-id="b37ca-182">or</span></span><br/> <span data-ttu-id="b37ca-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-184">3/2 + НИЗКОЧАСТОТНЫЙ</span><span class="sxs-lookup"><span data-stu-id="b37ca-184">3/2 + LFE</span></span></td>
<td><span data-ttu-id="b37ca-185">6</span><span class="sxs-lookup"><span data-stu-id="b37ca-185">6</span></span></td>
<td><span data-ttu-id="b37ca-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="b37ca-187">или</span><span class="sxs-lookup"><span data-stu-id="b37ca-187">or</span></span><br/> <span data-ttu-id="b37ca-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="b37ca-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-189">3/2/2 + НИЗКОЧАСТОТНЫЙ</span><span class="sxs-lookup"><span data-stu-id="b37ca-189">3/2/2 + LFE</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b37ca-190">Только Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="b37ca-190">Dolby Digital Plus only.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="b37ca-191">8</span><span class="sxs-lookup"><span data-stu-id="b37ca-191">8</span></span></td>
<td><span data-ttu-id="b37ca-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span><span class="sxs-lookup"><span data-stu-id="b37ca-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b37ca-193">Кроме того, конфигурации каналов 1/0, 2/0, 3/0, 2/1, 3/1 и 2/2 также могут отображаться с каналом НИЗКОЧАСТОТного канала.</span><span class="sxs-lookup"><span data-stu-id="b37ca-193">In addition, channel configurations 1/0, 2/0, 3/0, 2/1, 3/1, and 2/2 may also appear with an LFE channel.</span></span>

## <a name="output-types"></a><span data-ttu-id="b37ca-194">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="b37ca-194">Output Types</span></span>

<span data-ttu-id="b37ca-195">Декодер Dolby Audio поддерживает следующие выходные типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b37ca-195">The Dolby audio decoder supports the following output subtypes.</span></span>



| <span data-ttu-id="b37ca-196">Subtype</span><span class="sxs-lookup"><span data-stu-id="b37ca-196">Subtype</span></span>                                                   | <span data-ttu-id="b37ca-197">Описание</span><span class="sxs-lookup"><span data-stu-id="b37ca-197">Description</span></span>                                                                                                                               | <span data-ttu-id="b37ca-198">Header</span><span class="sxs-lookup"><span data-stu-id="b37ca-198">Header</span></span>    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b37ca-199">**Мфаудиоформат \_ Dolby \_ AC3 \_ SPDIF**</span><span class="sxs-lookup"><span data-stu-id="b37ca-199">**MFAudioFormat\_Dolby\_AC3\_SPDIF**</span></span>                      | <span data-ttu-id="b37ca-200">Звук Dolby AC-3, отформатированный для цифрового выхода S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="b37ca-200">Dolby AC-3 audio formatted for S/PDIF digital output.</span></span>                                                                                     | <span data-ttu-id="b37ca-201">мфапи. h</span><span class="sxs-lookup"><span data-stu-id="b37ca-201">mfapi.h</span></span>   |
| <span data-ttu-id="b37ca-202">**\_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ Digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="b37ca-202">**KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**</span></span> | <span data-ttu-id="b37ca-203">Dolby Digital Plus Audio, форматированный для цифрового выхода HDMI.</span><span class="sxs-lookup"><span data-stu-id="b37ca-203">Dolby Digital Plus audio formatted for HDMI digital output.</span></span>                                                                               | <span data-ttu-id="b37ca-204">ксмедиа. h</span><span class="sxs-lookup"><span data-stu-id="b37ca-204">ksmedia.h</span></span> |
| <span data-ttu-id="b37ca-205">**Мфаудиоформат \_ float**</span><span class="sxs-lookup"><span data-stu-id="b37ca-205">**MFAudioFormat\_Float**</span></span>                                  | <span data-ttu-id="b37ca-206">IEEE 32-разрядный звук PCM с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="b37ca-206">IEEE 32-bit floating-point PCM audio</span></span><br/> <span data-ttu-id="b37ca-207">**Windows 10**: стерео, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="b37ca-207">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="b37ca-208">**Предыдущие версии**: стерео, 5,1</span><span class="sxs-lookup"><span data-stu-id="b37ca-208">**Previous versions**: stereo, 5.1</span></span><br/> | <span data-ttu-id="b37ca-209">мфапи. h</span><span class="sxs-lookup"><span data-stu-id="b37ca-209">mfapi.h</span></span>   |
| <span data-ttu-id="b37ca-210">**Мфаудиоформат \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="b37ca-210">**MFAudioFormat\_PCM**</span></span>                                    | <span data-ttu-id="b37ca-211">16-разрядный звук PCM</span><span class="sxs-lookup"><span data-stu-id="b37ca-211">16-bit PCM audio</span></span><br/> <span data-ttu-id="b37ca-212">**Windows 10**: стерео, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="b37ca-212">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="b37ca-213">**Предыдущие версии**: стерео, 5,1</span><span class="sxs-lookup"><span data-stu-id="b37ca-213">**Previous versions**: stereo, 5.1</span></span><br/>                     | <span data-ttu-id="b37ca-214">мфапи. h</span><span class="sxs-lookup"><span data-stu-id="b37ca-214">mfapi.h</span></span>   |



 

<span data-ttu-id="b37ca-215">В следующей таблице перечислены обязательные и необязательные атрибуты для выходного типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b37ca-215">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b37ca-216">attribute</span><span class="sxs-lookup"><span data-stu-id="b37ca-216">Attribute</span></span></th>
<th><span data-ttu-id="b37ca-217">Описание</span><span class="sxs-lookup"><span data-stu-id="b37ca-217">Description</span></span></th>
<th><span data-ttu-id="b37ca-218">Remarks</span><span class="sxs-lookup"><span data-stu-id="b37ca-218">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b37ca-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="b37ca-220">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="b37ca-220">Major type.</span></span></td>
<td><span data-ttu-id="b37ca-221">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b37ca-221">Required.</span></span> <span data-ttu-id="b37ca-222">Необходимо <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="b37ca-222">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="b37ca-224">Подтип аудио.</span><span class="sxs-lookup"><span data-stu-id="b37ca-224">Audio subtype.</span></span></td>
<td><span data-ttu-id="b37ca-225">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b37ca-225">Required.</span></span> <span data-ttu-id="b37ca-226">Дополнительные сведения см. в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="b37ca-226">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="b37ca-228">Частота выборки, в примерах в секунду.</span><span class="sxs-lookup"><span data-stu-id="b37ca-228">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="b37ca-229">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b37ca-229">Required.</span></span> <span data-ttu-id="b37ca-230">Допустимые значения: 48000, 44100, 32000, 24000, 22050 и 16000.</span><span class="sxs-lookup"><span data-stu-id="b37ca-230">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="b37ca-231">Частота выборки выходных данных должна совпадать с частотой выборки данных.</span><span class="sxs-lookup"><span data-stu-id="b37ca-231">The output sample rate must be identical to the input sample rate.</span></span> <span data-ttu-id="b37ca-232">Декодер не может изменить частоту выборки потока.</span><span class="sxs-lookup"><span data-stu-id="b37ca-232">The decoder cannot change the sampling rate of the stream.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="b37ca-234">Количество каналов, включая канал с низкой частотой (НИЗКОЧАСТОТный), если он есть.</span><span class="sxs-lookup"><span data-stu-id="b37ca-234">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="b37ca-235">Требуется для выходных данных PCM.</span><span class="sxs-lookup"><span data-stu-id="b37ca-235">Required for PCM output.</span></span> <br/> <span data-ttu-id="b37ca-236">Не требуется для цифрового вывода.</span><span class="sxs-lookup"><span data-stu-id="b37ca-236">Not needed for digital output.</span></span> <br/> <span data-ttu-id="b37ca-237">Если входной тип — моно, стерео или Dual-Mono (все без канала НИЗКОЧАСТОТного звучания), единственное допустимое значение — 2 для стерео Output.</span><span class="sxs-lookup"><span data-stu-id="b37ca-237">If the input type is mono, stereo, or dual-mono (all without LFE channel), the only valid value is 2, for stereo output.</span></span> <span data-ttu-id="b37ca-238">В противном случае значение может быть следующим:</span><span class="sxs-lookup"><span data-stu-id="b37ca-238">Otherwise, the value can be:</span></span> <br/>
<ul>
<li><span data-ttu-id="b37ca-239">2 для стерео довнмикс</span><span class="sxs-lookup"><span data-stu-id="b37ca-239">2 for stereo downmix</span></span></li>
<li><span data-ttu-id="b37ca-240">6 для конфигураций каналов 5,1</span><span class="sxs-lookup"><span data-stu-id="b37ca-240">6 for 5.1 channel configurations</span></span></li>
<li><span data-ttu-id="b37ca-241">8 для конфигураций каналов 7,1</span><span class="sxs-lookup"><span data-stu-id="b37ca-241">8 for 7.1 channel configurations</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="b37ca-243">Указывает назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="b37ca-243">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="b37ca-244">Требуется для вывода PCM, если число каналов больше 2.</span><span class="sxs-lookup"><span data-stu-id="b37ca-244">Required for PCM output if the number of channels is greater than 2.</span></span> <span data-ttu-id="b37ca-245">Значение должно быть следующим:</span><span class="sxs-lookup"><span data-stu-id="b37ca-245">The value must be:</span></span><br/>
<ul>
<li><span data-ttu-id="b37ca-246">0x3 для стерео вывода</span><span class="sxs-lookup"><span data-stu-id="b37ca-246">0x3 for stereo output</span></span></li>
<li><span data-ttu-id="b37ca-247">0x3F для выходных данных канала 5,1</span><span class="sxs-lookup"><span data-stu-id="b37ca-247">0x3F for 5.1 channel output</span></span></li>
<li><span data-ttu-id="b37ca-248">0x63F для выходных данных канала 7,1</span><span class="sxs-lookup"><span data-stu-id="b37ca-248">0x63F for 7.1 channel output</span></span></li>
</ul>
<span data-ttu-id="b37ca-249">Не требуется для цифрового вывода.</span><span class="sxs-lookup"><span data-stu-id="b37ca-249">Not needed for digital output.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="b37ca-251">Число битов на аудио выборка.</span><span class="sxs-lookup"><span data-stu-id="b37ca-251">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="b37ca-252">Требуется для выходных данных PCM.</span><span class="sxs-lookup"><span data-stu-id="b37ca-252">Required for PCM output.</span></span> <span data-ttu-id="b37ca-253">Значение должно быть 32 для <strong>MFAudioFormat_Float</strong>и 16 для <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="b37ca-253">The value must be 32 for <strong>MFAudioFormat_Float</strong>, and 16 for <strong>MFAudioFormat_PCM</strong>.</span></span><br/> <span data-ttu-id="b37ca-254">Не требуется для цифрового вывода.</span><span class="sxs-lookup"><span data-stu-id="b37ca-254">Not needed for digital output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="b37ca-256">Количество допустимых битов звуковых данных в каждом звуковом примере.</span><span class="sxs-lookup"><span data-stu-id="b37ca-256">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="b37ca-257">Необязательно для выходных данных PCM.</span><span class="sxs-lookup"><span data-stu-id="b37ca-257">Optional for PCM output.</span></span> <span data-ttu-id="b37ca-258">Если значение задано, оно должно быть идентично значению <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="b37ca-258">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span><br/> <span data-ttu-id="b37ca-259">Не требуется для подтипов цифровых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b37ca-259">Not needed for the digital output subtypes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b37ca-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="b37ca-261">Выравнивание блокировки в байтах.</span><span class="sxs-lookup"><span data-stu-id="b37ca-261">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="b37ca-262">Необязательно для выходных данных PCM.</span><span class="sxs-lookup"><span data-stu-id="b37ca-262">Optional for PCM output.</span></span> <span data-ttu-id="b37ca-263">Не требуется для цифрового вывода.</span><span class="sxs-lookup"><span data-stu-id="b37ca-263">Not needed for digital output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b37ca-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="b37ca-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="b37ca-265">Среднее число байтов в секунду.</span><span class="sxs-lookup"><span data-stu-id="b37ca-265">Average number of bytes per second.</span></span></td>
<td><span data-ttu-id="b37ca-266">Необязательно для выходных данных PCM.</span><span class="sxs-lookup"><span data-stu-id="b37ca-266">Optional for PCM output.</span></span> <span data-ttu-id="b37ca-267">Не требуется для цифрового вывода.</span><span class="sxs-lookup"><span data-stu-id="b37ca-267">Not needed for digital output.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a><span data-ttu-id="b37ca-268">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="b37ca-268">Transform Attributes</span></span>

<span data-ttu-id="b37ca-269">Декодер Dolby Audio реализует метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="b37ca-269">The Dolby audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="b37ca-270">Приложение может использовать этот метод для получения или установки следующих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b37ca-270">The application can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="b37ca-271">attribute</span><span class="sxs-lookup"><span data-stu-id="b37ca-271">Attribute</span></span>                                                                                | <span data-ttu-id="b37ca-272">Описание</span><span class="sxs-lookup"><span data-stu-id="b37ca-272">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b37ca-273">КОДЕКАПИ \_ авдекаудиодуалмоно</span><span class="sxs-lookup"><span data-stu-id="b37ca-273">CODECAPI\_AVDecAudioDualMono</span></span>](../directshow/avdecaudiodualmono-property.md)                        | <span data-ttu-id="b37ca-274">Указывает, кодируется ли звуковой поток Dolby из 2 каналов в формате стерео или Dual-Mono.</span><span class="sxs-lookup"><span data-stu-id="b37ca-274">Specifies whether a 2-channel Dolby audio stream is encoded as stereo or dual-mono.</span></span> <span data-ttu-id="b37ca-275">Перед декодированием первого кадра Dolby значение **еавдекаудиодуалмоно не \_ указано**.</span><span class="sxs-lookup"><span data-stu-id="b37ca-275">Before the first Dolby frame is decoded, the value is **eAVDecAudioDualMono\_UnSpecified**.</span></span> <span data-ttu-id="b37ca-276">После декодирования значение отражает самый последний кадр Dolby.</span><span class="sxs-lookup"><span data-stu-id="b37ca-276">After decoding begins, the value reflects the most recent Dolby frame.</span></span><br/> <span data-ttu-id="b37ca-277">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b37ca-277">Read-only.</span></span> <br/> |
| [<span data-ttu-id="b37ca-278">КОДЕКАПИ \_ авдекаудиодуалмонорепромоде</span><span class="sxs-lookup"><span data-stu-id="b37ca-278">CODECAPI\_AVDecAudioDualMonoReproMode</span></span>](../directshow/avdecaudiodualmonorepromode-property.md)      | <span data-ttu-id="b37ca-279">Указывает, как декодер воссоздает аудио-файлы с двумя моноями.</span><span class="sxs-lookup"><span data-stu-id="b37ca-279">Specifies how the decoder reproduces dual-mono audio.</span></span> <span data-ttu-id="b37ca-280">По умолчанию используется значение **еавдекаудиодуалмонорепромоде \_ Left \_ Mono**.</span><span class="sxs-lookup"><span data-stu-id="b37ca-280">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span> <span data-ttu-id="b37ca-281">Приложение может установить это свойство в любое время.</span><span class="sxs-lookup"><span data-stu-id="b37ca-281">The application can set this property at any time.</span></span><br/> <span data-ttu-id="b37ca-282">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b37ca-282">Read/write.</span></span><br/>                                                                            |
| [<span data-ttu-id="b37ca-283">КОДЕКАПИ \_ авдеккоммонмеанбитрате</span><span class="sxs-lookup"><span data-stu-id="b37ca-283">CODECAPI\_AVDecCommonMeanBitRate</span></span>](../directshow/avdeccommonmeanbitrate.md)                         | <span data-ttu-id="b37ca-284">Для потоков Dolby Digital (AC-3) указывает скорость потока входных потоков в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="b37ca-284">For Dolby Digital (AC-3) streams, specifies the bit rate of the input stream in bits per second.</span></span> <span data-ttu-id="b37ca-285">Для Dolby Digital Plus (E-AC3) значение всегда равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b37ca-285">For Dolby Digital Plus (E-AC3), the value is always zero.</span></span><br/> <span data-ttu-id="b37ca-286">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b37ca-286">Read only.</span></span><br/>                                                                                              |
| [<span data-ttu-id="b37ca-287">КОДЕКАПИ \_ авдекдддинамикранжескалехигх</span><span class="sxs-lookup"><span data-stu-id="b37ca-287">CODECAPI\_AVDecDDDynamicRangeScaleHigh</span></span>](../directshow/avdecdddynamicrangescalehigh-property.md)    | <span data-ttu-id="b37ca-288">Высокоуровневая вырезание, когда декодер выполняет динамическое управление диапазонами.</span><span class="sxs-lookup"><span data-stu-id="b37ca-288">The high-level cut when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="b37ca-289">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b37ca-289">Read/write.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="b37ca-290">КОДЕКАПИ \_ авдекдддинамикранжескалелов</span><span class="sxs-lookup"><span data-stu-id="b37ca-290">CODECAPI\_AVDecDDDynamicRangeScaleLow</span></span>](../directshow/avdecdddynamicrangescalelow-property.md)      | <span data-ttu-id="b37ca-291">Низкоуровневые улучшения, когда декодер выполняет динамический контроль диапазона.</span><span class="sxs-lookup"><span data-stu-id="b37ca-291">The low-level boost when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="b37ca-292">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b37ca-292">Read/write.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="b37ca-293">КОДЕКАПИ \_ авдекддоператионалмоде</span><span class="sxs-lookup"><span data-stu-id="b37ca-293">CODECAPI\_AVDecDDOperationalMode</span></span>](../directshow/avdecddoperationalmode-property.md)                | <span data-ttu-id="b37ca-294">Режим управления сжатием.</span><span class="sxs-lookup"><span data-stu-id="b37ca-294">The compression control mode.</span></span><br/> <span data-ttu-id="b37ca-295">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b37ca-295">Read/write.</span></span><br/>                                                                                                                                                                                                                          |
| [<span data-ttu-id="b37ca-296">КОДЕКАПИ \_ авдекддстереодовнмиксмоде</span><span class="sxs-lookup"><span data-stu-id="b37ca-296">CODECAPI\_AVDecDDStereoDownMixMode</span></span>](codecapi-avdecddstereodownmixmode.md)              | <span data-ttu-id="b37ca-297">Тип стерео довнмикс.</span><span class="sxs-lookup"><span data-stu-id="b37ca-297">The type of stereo downmix.</span></span> <span data-ttu-id="b37ca-298">Это свойство применяется, если входные данные являются многоканальным потоком, а выходные данные — стерео потоком.</span><span class="sxs-lookup"><span data-stu-id="b37ca-298">This property applies when the input is a multichannel stream and the output is a stereo stream.</span></span><br/> <span data-ttu-id="b37ca-299">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b37ca-299">Read/write.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="b37ca-300">Основная таблица MFT \_ поддерживает \_ \_ изменение динамического формата \_</span><span class="sxs-lookup"><span data-stu-id="b37ca-300">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE</span></span>](mft-support-dynamic-format-change-attribute.md) | <span data-ttu-id="b37ca-301">Этот атрибут возвращает **значение false**, указывающее, что декодер должен быть остановлен до установки нового входного типа.</span><span class="sxs-lookup"><span data-stu-id="b37ca-301">This attribute returns **FALSE**, indicating that the decoder must be drained before a new input type is set.</span></span><br/> <span data-ttu-id="b37ca-302">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b37ca-302">Read/write.</span></span><br/>                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="b37ca-303">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b37ca-303">Remarks</span></span>

<span data-ttu-id="b37ca-304">Декодер принимает только необработанные потоки Dolby, как определено параметром/52B.</span><span class="sxs-lookup"><span data-stu-id="b37ca-304">The decoder accepts only raw Dolby streams, as defined by A/52B.</span></span> <span data-ttu-id="b37ca-305">Полезные данные, такие как Пакетированные потоковые простые потоки (PES), не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b37ca-305">Payloads such as Packetized Elementary Streams (PES) are not supported.</span></span> <span data-ttu-id="b37ca-306">Для Dolby Digital Plus декодер декодировать до 5,1 каналов.</span><span class="sxs-lookup"><span data-stu-id="b37ca-306">For Dolby Digital Plus, the decoder decodes up to 5.1 channels.</span></span> <span data-ttu-id="b37ca-307">В Windows 10 потоки каналов 7,1 декодированы без довнмикс.</span><span class="sxs-lookup"><span data-stu-id="b37ca-307">On Windows 10, 7.1 channel streams are decoded without downmix.</span></span> <span data-ttu-id="b37ca-308">В предыдущих версиях ОС, если поток 7,1 каналов, будет декодирован только довнмикс-канал 5,1.</span><span class="sxs-lookup"><span data-stu-id="b37ca-308">On previous OS versions, if the stream is 7.1 channels, only the 5.1 channel downmix will be decoded.</span></span> <span data-ttu-id="b37ca-309">Если поток — Dolby Digital Plus с более чем одним независимым подпотоком, декодирован только независимый подпоток 0.</span><span class="sxs-lookup"><span data-stu-id="b37ca-309">If the stream is Dolby Digital Plus with more than one independent substream, only independent substream 0 is decoded.</span></span> <span data-ttu-id="b37ca-310">Декодер пропускает другие независимые подпотоки.</span><span class="sxs-lookup"><span data-stu-id="b37ca-310">The decoder skips other independent substreams.</span></span> <span data-ttu-id="b37ca-311">Кроме того, декодер пропускает все зависимые подпотоки.</span><span class="sxs-lookup"><span data-stu-id="b37ca-311">In addition, the decoder skips all dependent substreams.</span></span> <span data-ttu-id="b37ca-312">Декодер поддерживает расшифровку и декодирование потоков, защищенных с помощью технологии Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="b37ca-312">The decoder supports decryption and decoding of streams that are protected by Digital Rights Management (DRM) technology.</span></span>

<span data-ttu-id="b37ca-313">Если тип входного носителя имеет конфигурацию канала, отличную от Mono, стерео или Dual-Mono (без канала НИЗКОЧАСТОТного звучания), декодер предоставляет два варианта конфигураций выходного канала:</span><span class="sxs-lookup"><span data-stu-id="b37ca-313">If the input media type has a channel configuration other than mono, stereo, or dual-mono (all without LFE channel), the decoder provides two options for the output channel configurations:</span></span>

-   <span data-ttu-id="b37ca-314">8-канальный вывод (Конфигурация канала 7,1)</span><span class="sxs-lookup"><span data-stu-id="b37ca-314">8-channel output (7.1 channel configuration)</span></span>
-   <span data-ttu-id="b37ca-315">6-канальный вывод (Конфигурация канала 5,1)</span><span class="sxs-lookup"><span data-stu-id="b37ca-315">6-channel output (5.1 channel configuration)</span></span>
-   <span data-ttu-id="b37ca-316">Стерео довнмикс</span><span class="sxs-lookup"><span data-stu-id="b37ca-316">Stereo downmix</span></span>

<span data-ttu-id="b37ca-317">Если выбрано стерео довнмикс, то тип довнмикс можно задать в MFT с помощью свойства [кодекапи \_ авдекддстереодовнмиксмоде](codecapi-avdecddstereodownmixmode.md) .</span><span class="sxs-lookup"><span data-stu-id="b37ca-317">If stereo downmix is selected, the type of downmix can be set on the MFT by using the [CODECAPI\_AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) property.</span></span>

<span data-ttu-id="b37ca-318">Если тип выходных данных — **мфаудиоформат \_ Dolby \_ AC3 \_ SPDIF**, то каждый выходной буфер содержит 6 144 байт.</span><span class="sxs-lookup"><span data-stu-id="b37ca-318">If the output type is **MFAudioFormat\_Dolby\_AC3\_SPDIF**, each output buffer contains 6,144 bytes.</span></span> <span data-ttu-id="b37ca-319">Буфер начинается с 8-байтового заголовка S/PDIF, за которым следует сжатый кадр AC-3, за которым следует ноль заполнения до 6 144 байт.</span><span class="sxs-lookup"><span data-stu-id="b37ca-319">The buffer starts with an 8-byte S/PDIF header, followed by a compressed AC-3 frame, followed by zero padding to 6,144 bytes.</span></span>

<span data-ttu-id="b37ca-320">Если тип выходных данных — **ксдатаформат подтип \_ \_ IEC61937 \_ Dolby \_ Digital \_ PLUS**, каждый выходной буфер содержит 24 576 байт.</span><span class="sxs-lookup"><span data-stu-id="b37ca-320">If the output type is **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**, each output buffer contains 24,576 bytes.</span></span> <span data-ttu-id="b37ca-321">Буфер начинается с 8-байтового заголовка S/PDIF, за которым следуют 1 – 6 сжатые кадры Dolby Digital Plus, соответствующие примерам PCM 1 536, за которыми следует ноль заполнения до 24 576 байт.</span><span class="sxs-lookup"><span data-stu-id="b37ca-321">The buffer starts with an 8-byte S/PDIF header, followed by 1–6 compressed Dolby Digital Plus frames corresponding to 1,536 PCM samples, followed by zero padding to 24,576 bytes.</span></span> <span data-ttu-id="b37ca-322">Для выходных данных HDMI упаковывается только независимый подпоток 0.</span><span class="sxs-lookup"><span data-stu-id="b37ca-322">For HDMI output, only independent substream 0 is packed.</span></span>

<span data-ttu-id="b37ca-323">Таблица MFT декодера зарегистрирована с флагом **\_ перечисления MFT Enum \_ \_ фиелдофусе**, который указывает, что Таблица MFT, которая должна быть разблокирована приложением перед использованием.</span><span class="sxs-lookup"><span data-stu-id="b37ca-323">The decoder MFT is registered with the flag **MFT\_ENUM\_FLAG\_FIELDOFUSE**, which indicates that the MFT that must be unlocked by the application before use.</span></span> <span data-ttu-id="b37ca-324">Дополнительные сведения см. в разделе [ограничения использования](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b37ca-324">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b37ca-325">Требования</span><span class="sxs-lookup"><span data-stu-id="b37ca-325">Requirements</span></span>



| <span data-ttu-id="b37ca-326">Требование</span><span class="sxs-lookup"><span data-stu-id="b37ca-326">Requirement</span></span> | <span data-ttu-id="b37ca-327">Значение</span><span class="sxs-lookup"><span data-stu-id="b37ca-327">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b37ca-328">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b37ca-328">Minimum supported client</span></span><br/> | <span data-ttu-id="b37ca-329">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="b37ca-329">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="b37ca-330">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b37ca-330">Minimum supported server</span></span><br/> | <span data-ttu-id="b37ca-331">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b37ca-331">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="b37ca-332">DLL</span><span class="sxs-lookup"><span data-stu-id="b37ca-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b37ca-333"><dt>Msauddecmft.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b37ca-333"><dt>Msauddecmft.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b37ca-334">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b37ca-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b37ca-335">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="b37ca-335">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
