---
description: Идентификаторы GUID для подтипов звука
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: Идентификаторы GUID для подтипов звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496851"
---
# <a name="audio-subtype-guids"></a><span data-ttu-id="8724e-103">Идентификаторы GUID для подтипов звука</span><span class="sxs-lookup"><span data-stu-id="8724e-103">Audio Subtype GUIDs</span></span>

<span data-ttu-id="8724e-104">Определены следующие идентификаторы GUID для звуковых подтипов.</span><span class="sxs-lookup"><span data-stu-id="8724e-104">The following audio subtype GUIDs are defined.</span></span> <span data-ttu-id="8724e-105">Чтобы указать подтип, задайте атрибут [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) для типа носителя.</span><span class="sxs-lookup"><span data-stu-id="8724e-105">To specify the subtype, set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="8724e-106">За исключением указанных случаев, эти константы определены в файле заголовка мфапи. h.</span><span class="sxs-lookup"><span data-stu-id="8724e-106">Except where noted, these constants are defined in the header file mfapi.h.</span></span>

<span data-ttu-id="8724e-107">Если используются эти подтипы, задайте для атрибута " [ \_ \_ основной \_ тип MF MT](mf-mt-major-type-attribute.md) " значение **мфмедиатипе \_ Audio**.</span><span class="sxs-lookup"><span data-stu-id="8724e-107">When these subtypes are used, set the [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8724e-108">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="8724e-108">GUID</span></span></th>
<th><span data-ttu-id="8724e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8724e-109">Description</span></span></th>
<th><span data-ttu-id="8724e-110">Тег Format (FOURCC)</span><span class="sxs-lookup"><span data-stu-id="8724e-110">Format Tag (FOURCC)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8724e-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span></span></td>
<td><span data-ttu-id="8724e-112">Расширенное аудио кодирование (AAC).</span><span class="sxs-lookup"><span data-stu-id="8724e-112">Advanced Audio Coding (AAC).</span></span><br/> <span data-ttu-id="8724e-113">Этот подтип используется для AAC, содержащихся в AVI-файле, с тегом формата, равным 0x00FF.</span><span class="sxs-lookup"><span data-stu-id="8724e-113">This subtype is used for AAC contained in an AVI file with an audio format tag equal to 0x00FF.</span></span> <br/> <span data-ttu-id="8724e-114">Дополнительные сведения см. в разделе <a href="aac-decoder.md"><strong>декодер AAC</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8724e-114">For more information, see <a href="aac-decoder.md"><strong>AAC Decoder</strong></a>.</span></span><br/> <span data-ttu-id="8724e-115">Определено в вмкодекдсп. h</span><span class="sxs-lookup"><span data-stu-id="8724e-115">Defined in wmcodecdsp.h</span></span><br/></td>
<td><span data-ttu-id="8724e-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="8724e-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-117"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-117"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="8724e-118">Расширенное аудио кодирование (AAC).</span><span class="sxs-lookup"><span data-stu-id="8724e-118">Advanced Audio Coding (AAC).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8724e-119">Эквивалентно MEDIASUBTYPE_MPEG_HEAAC, определенному в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="8724e-119">Equivalent to MEDIASUBTYPE_MPEG_HEAAC, defined in wmcodecdsp.h.</span></span>
</blockquote>
<br/> <span data-ttu-id="8724e-120">Поток может содержать необработанные данные AAC или AAC данные в потоке передачи звуковых данных (ADTS).</span><span class="sxs-lookup"><span data-stu-id="8724e-120">The stream can contain raw AAC data or AAC data in an Audio Data Transport Stream (ADTS) stream.</span></span><br/> <span data-ttu-id="8724e-121">Дополнительные сведения можно найти в разделе</span><span class="sxs-lookup"><span data-stu-id="8724e-121">For more information, see:</span></span><br/>
<ul>
<li><span data-ttu-id="8724e-122"><a href="aac-decoder.md"><strong>Декодер AAC</strong></a></span><span class="sxs-lookup"><span data-stu-id="8724e-122"><a href="aac-decoder.md"><strong>AAC Decoder</strong></a></span></span></li>
<li><span data-ttu-id="8724e-123"><a href="mpeg-4-file-source.md">Источник файла MPEG-4</a></span><span class="sxs-lookup"><span data-stu-id="8724e-123"><a href="mpeg-4-file-source.md">MPEG-4 File Source</a></span></span></li>
</ul></td>
<td><span data-ttu-id="8724e-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span><span class="sxs-lookup"><span data-stu-id="8724e-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-125"><strong>MFAudioFormat_ADTS</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-125"><strong>MFAudioFormat_ADTS</strong></span></span></td>
<td><span data-ttu-id="8724e-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8724e-126">Not used.</span></span></td>
<td><span data-ttu-id="8724e-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span><span class="sxs-lookup"><span data-stu-id="8724e-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-128"><strong>MFAudioFormat_ALAC</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-128"><strong>MFAudioFormat_ALAC</strong></span></span></td>
<td><span data-ttu-id="8724e-129">Аудиокодек Apple без потерь</span><span class="sxs-lookup"><span data-stu-id="8724e-129">Apple Lossless Audio Codec</span></span><br/> <span data-ttu-id="8724e-130">Поддерживается в Windows 10 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8724e-130">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="8724e-131">WAVE_FORMAT_ALAC (0x6C61)</span><span class="sxs-lookup"><span data-stu-id="8724e-131">WAVE_FORMAT_ALAC (0x6C61)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-132"><strong>MFAudioFormat_AMR_NB</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-132"><strong>MFAudioFormat_AMR_NB</strong></span></span></td>
<td><span data-ttu-id="8724e-133">Адаптативе с несколькими скоростями</span><span class="sxs-lookup"><span data-stu-id="8724e-133">Adaptative Multi-Rate audio</span></span><br/> <span data-ttu-id="8724e-134">Поддерживается в Windows 8.1 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8724e-134">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="8724e-135">WAVE_FORMAT_AMR_NB</span><span class="sxs-lookup"><span data-stu-id="8724e-135">WAVE_FORMAT_AMR_NB</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-136"><strong>MFAudioFormat_AMR_WB</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-136"><strong>MFAudioFormat_AMR_WB</strong></span></span></td>
<td><span data-ttu-id="8724e-137">Адаптативе Multi-Rate Wideband Audio</span><span class="sxs-lookup"><span data-stu-id="8724e-137">Adaptative Multi-Rate Wideband audio</span></span><br/> <span data-ttu-id="8724e-138">Поддерживается в Windows 8.1 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8724e-138">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="8724e-139">WAVE_FORMAT_AMR_WB</span><span class="sxs-lookup"><span data-stu-id="8724e-139">WAVE_FORMAT_AMR_WB</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-140"><strong>MFAudioFormat_AMR_WP</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-140"><strong>MFAudioFormat_AMR_WP</strong></span></span></td>
<td><span data-ttu-id="8724e-141">Поддерживается в Windows 8.1 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8724e-141">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="8724e-142">WAVE_FORMAT_AMR_WP</span><span class="sxs-lookup"><span data-stu-id="8724e-142">WAVE_FORMAT_AMR_WP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-143"><strong>MFAudioFormat_Dolby_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-143"><strong>MFAudioFormat_Dolby_AC3</strong></span></span></td>
<td><span data-ttu-id="8724e-144">Dolby Digital (AC-3).</span><span class="sxs-lookup"><span data-stu-id="8724e-144">Dolby Digital (AC-3).</span></span><br/> <span data-ttu-id="8724e-145">То же значение GUID, что и <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, которое определено в ксууидс. h</span><span class="sxs-lookup"><span data-stu-id="8724e-145">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, which is defined in ksuuids.h</span></span><br/></td>
<td><span data-ttu-id="8724e-146">Нет.</span><span class="sxs-lookup"><span data-stu-id="8724e-146">None.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span></span></td>
<td><span data-ttu-id="8724e-148">Dolby AC-3 аудио через Sony/Philips Digital Interface (S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="8724e-148">Dolby AC-3 audio over Sony/Philips Digital Interface (S/PDIF).</span></span><br/> <span data-ttu-id="8724e-149">Это значение идентификатора GUID идентично приведенным ниже подтипам:</span><span class="sxs-lookup"><span data-stu-id="8724e-149">This GUID value is identical to the following subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="8724e-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, определенный в ксмедиа. h.</span><span class="sxs-lookup"><span data-stu-id="8724e-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, defined in ksmedia.h.</span></span></li>
<li><span data-ttu-id="8724e-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, определенные в UUID. h.</span><span class="sxs-lookup"><span data-stu-id="8724e-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, defined in uuids.h.</span></span></li>
</ul></td>
<td><span data-ttu-id="8724e-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span><span class="sxs-lookup"><span data-stu-id="8724e-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span></span></td>
<td><span data-ttu-id="8724e-154">Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="8724e-154">Dolby Digital Plus.</span></span><br/> <span data-ttu-id="8724e-155">То же значение GUID, что и <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, которое определено в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="8724e-155">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, which is defined in wmcodecdsp.h.</span></span><br/></td>
<td><span data-ttu-id="8724e-156">Нет</span><span class="sxs-lookup"><span data-stu-id="8724e-156">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-157"><strong>MFAudioFormat_DRM</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-157"><strong>MFAudioFormat_DRM</strong></span></span></td>
<td><span data-ttu-id="8724e-158">Зашифрованные звуковые данные, используемые с защищенным звуковым путем.</span><span class="sxs-lookup"><span data-stu-id="8724e-158">Encrypted audio data used with secure audio path.</span></span></td>
<td><span data-ttu-id="8724e-159">WAVE_FORMAT_DRM (0x0009)</span><span class="sxs-lookup"><span data-stu-id="8724e-159">WAVE_FORMAT_DRM (0x0009)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-160"><strong>MFAudioFormat_DTS</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-160"><strong>MFAudioFormat_DTS</strong></span></span></td>
<td><span data-ttu-id="8724e-161">Звук системы цифрового кинотеатра (DTS).</span><span class="sxs-lookup"><span data-stu-id="8724e-161">Digital Theater Systems (DTS) audio.</span></span></td>
<td><span data-ttu-id="8724e-162">WAVE_FORMAT_DTS (0x0008)</span><span class="sxs-lookup"><span data-stu-id="8724e-162">WAVE_FORMAT_DTS (0x0008)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-163"><strong>MFAudioFormat_FLAC</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-163"><strong>MFAudioFormat_FLAC</strong></span></span></td>
<td><span data-ttu-id="8724e-164">Бесплатный аудиокодек без потерь</span><span class="sxs-lookup"><span data-stu-id="8724e-164">Free Lossless Audio Codec</span></span><br/> <span data-ttu-id="8724e-165">Поддерживается в Windows 10 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8724e-165">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="8724e-166">WAVE_FORMAT_FLAC (0xF1AC)</span><span class="sxs-lookup"><span data-stu-id="8724e-166">WAVE_FORMAT_FLAC (0xF1AC)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-167"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-167"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="8724e-168">Несжатое аудио с плавающей запятой IEEE.</span><span class="sxs-lookup"><span data-stu-id="8724e-168">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="8724e-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span><span class="sxs-lookup"><span data-stu-id="8724e-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span></span></td>
<td><span data-ttu-id="8724e-171">Несжатое аудио с плавающей запятой IEEE.</span><span class="sxs-lookup"><span data-stu-id="8724e-171">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="8724e-172">Нет</span><span class="sxs-lookup"><span data-stu-id="8724e-172">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-173"><strong>MFAudioFormat_MP3</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-173"><strong>MFAudioFormat_MP3</strong></span></span></td>
<td><span data-ttu-id="8724e-174">Звуковой слой MPEG-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="8724e-174">MPEG Audio Layer-3 (MP3).</span></span></td>
<td><span data-ttu-id="8724e-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span><span class="sxs-lookup"><span data-stu-id="8724e-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-176"><strong>MFAudioFormat_MPEG</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-176"><strong>MFAudioFormat_MPEG</strong></span></span></td>
<td><span data-ttu-id="8724e-177">Полезные данные звука MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="8724e-177">MPEG-1 audio payload.</span></span></td>
<td><span data-ttu-id="8724e-178">WAVE_FORMAT_MPEG (0x0050)</span><span class="sxs-lookup"><span data-stu-id="8724e-178">WAVE_FORMAT_MPEG (0x0050)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-179"><strong>MFAudioFormat_MSP1</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-179"><strong>MFAudioFormat_MSP1</strong></span></span></td>
<td><span data-ttu-id="8724e-180">Голосовой кодек Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="8724e-180">Windows Media Audio 9 Voice codec.</span></span></td>
<td><span data-ttu-id="8724e-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span><span class="sxs-lookup"><span data-stu-id="8724e-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-182"><strong>MFAudioFormat_Opus</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-182"><strong>MFAudioFormat_Opus</strong></span></span></td>
<td><span data-ttu-id="8724e-183">Opus</span><span class="sxs-lookup"><span data-stu-id="8724e-183">Opus</span></span><br/> <span data-ttu-id="8724e-184">Поддерживается в Windows 10 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8724e-184">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="8724e-185">WAVE_FORMAT_OPUS (0x704F)</span><span class="sxs-lookup"><span data-stu-id="8724e-185">WAVE_FORMAT_OPUS (0x704F)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-186"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-186"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="8724e-187">Несжатый звук PCM.</span><span class="sxs-lookup"><span data-stu-id="8724e-187">Uncompressed PCM audio.</span></span></td>
<td><span data-ttu-id="8724e-188">WAVE_FORMAT_PCM (1)</span><span class="sxs-lookup"><span data-stu-id="8724e-188">WAVE_FORMAT_PCM (1)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-189"><strong>MFAudioFormat_QCELP</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-189"><strong>MFAudioFormat_QCELP</strong></span></span></td>
<td><span data-ttu-id="8724e-190">КЦЕЛП (линейный прогноз для кода Qualcomm).</span><span class="sxs-lookup"><span data-stu-id="8724e-190">QCELP (Qualcomm Code Excited Linear Prediction) audio.</span></span></td>
<td><span data-ttu-id="8724e-191">Нет</span><span class="sxs-lookup"><span data-stu-id="8724e-191">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-192"><strong>MFAudioFormat_WMASPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-192"><strong>MFAudioFormat_WMASPDIF</strong></span></span></td>
<td><span data-ttu-id="8724e-193">Кодек Windows Media Audio 9 Professional через S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="8724e-193">Windows Media Audio 9 Professional codec over S/PDIF.</span></span></td>
<td><span data-ttu-id="8724e-194">WAVE_FORMAT_WMASPDIF (0x0164)</span><span class="sxs-lookup"><span data-stu-id="8724e-194">WAVE_FORMAT_WMASPDIF (0x0164)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span></span></td>
<td><span data-ttu-id="8724e-196">Кодек Windows Media Audio 9 без потерь или кодек Windows Media Audio 9,1.</span><span class="sxs-lookup"><span data-stu-id="8724e-196">Windows Media Audio 9 Lossless codec or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="8724e-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span><span class="sxs-lookup"><span data-stu-id="8724e-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8724e-198"><strong>MFAudioFormat_WMAudioV8</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-198"><strong>MFAudioFormat_WMAudioV8</strong></span></span></td>
<td><span data-ttu-id="8724e-199">Кодек Windows Media Audio 8, кодек Windows Media Audio 9 или кодек Windows Media Audio 9,1.</span><span class="sxs-lookup"><span data-stu-id="8724e-199">Windows Media Audio 8 codec, Windows Media Audio 9 codec, or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="8724e-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span><span class="sxs-lookup"><span data-stu-id="8724e-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8724e-201"><strong>MFAudioFormat_WMAudioV9</strong></span><span class="sxs-lookup"><span data-stu-id="8724e-201"><strong>MFAudioFormat_WMAudioV9</strong></span></span></td>
<td><span data-ttu-id="8724e-202">Кодек Windows Media Audio 9 Professional или кодек Windows Media Audio 9,1 Professional.</span><span class="sxs-lookup"><span data-stu-id="8724e-202">Windows Media Audio 9 Professional codec or Windows Media Audio 9.1 Professional codec.</span></span></td>
<td><span data-ttu-id="8724e-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span><span class="sxs-lookup"><span data-stu-id="8724e-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8724e-204">Теги формата, перечисленные в третьем столбце этой таблицы, используются в структуре **вавеформатекс** и определены в файле заголовка ммрег. h.</span><span class="sxs-lookup"><span data-stu-id="8724e-204">The format tags listed in the third column of this table are used in the **WAVEFORMATEX** structure, and are defined in the header file mmreg.h.</span></span>

<span data-ttu-id="8724e-205">При наличии тега звукового формата можно создать идентификатор GUID для звукового подтипа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8724e-205">Given an audio format tag, you can create an audio subtype GUID as follows:</span></span>

1.  <span data-ttu-id="8724e-206">Начните со значения **мфаудиоформат \_ base**, которое определено в мфаф. i.</span><span class="sxs-lookup"><span data-stu-id="8724e-206">Start with the value **MFAudioFormat\_Base**, which is defined in mfaph.i.</span></span>
2.  <span data-ttu-id="8724e-207">Замените первый **DWORD** этого GUID тегом Format.</span><span class="sxs-lookup"><span data-stu-id="8724e-207">Replace the first **DWORD** of this GUID with the format tag.</span></span>

<span data-ttu-id="8724e-208">Чтобы определить новую константу GUID, которая следует за этим шаблоном, можно использовать макрос [**define \_ MEDIATYPE \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) .</span><span class="sxs-lookup"><span data-stu-id="8724e-208">You can use the [**DEFINE\_MEDIATYPE\_GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) macro to define a new GUID constant that follows this pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8724e-209">См. также</span><span class="sxs-lookup"><span data-stu-id="8724e-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8724e-210">Типы звуковых носителей</span><span class="sxs-lookup"><span data-stu-id="8724e-210">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="8724e-211">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="8724e-211">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="8724e-212">GUID типа носителя</span><span class="sxs-lookup"><span data-stu-id="8724e-212">Media Type GUIDs</span></span>](media-type-guids.md)
</dt> <dt>

[<span data-ttu-id="8724e-213">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="8724e-213">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




