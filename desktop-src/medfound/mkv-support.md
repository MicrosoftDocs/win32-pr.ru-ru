---
description: В этом разделе описывается поддержка Media Foundation для файлов контейнера мультимедиа матроска (MKV).
title: Поддержка контейнера мультимедиа матроска (MKV)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd860f58087bc8a0f3fe95d278bfa81edc412d0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2021
ms.locfileid: "110154223"
---
# <a name="matroska-media-container-mkv-support"></a><span data-ttu-id="18a69-103">Поддержка контейнера мультимедиа матроска (MKV)</span><span class="sxs-lookup"><span data-stu-id="18a69-103">Matroska Media Container (MKV) support</span></span>

<span data-ttu-id="18a69-104">В этом разделе описывается поддержка Media Foundation для файлов контейнера мультимедиа матроска (MKV).</span><span class="sxs-lookup"><span data-stu-id="18a69-104">This section describes the Media Foundation support for Matroska Media Container (MKV) files.</span></span>

<span data-ttu-id="18a69-105">Формат MKV может поддерживать несколько видеокодеков и аудиокодеков, таких как H. 264 и AAC Audio.</span><span class="sxs-lookup"><span data-stu-id="18a69-105">The MKV format can support multiple video and audio codecs, such as H.264 and AAC audio.</span></span> <span data-ttu-id="18a69-106">В общем случае контейнеры описывают, как располагаются видео и звуковые данные и какие дополнительные сведения используются для описания этих потоков/V.</span><span class="sxs-lookup"><span data-stu-id="18a69-106">In general, containers describe how video and audio data is laid out and what supplementary information is used to describe those A/V streams.</span></span> <span data-ttu-id="18a69-107">Контейнеры также могут включать данные, дополняющие потоки/V, такие как название, языки звуковых потоков, подзаголовок или подзаголовки, шрифты для этих субтитров, изображения, сведения о разделах и меню.</span><span class="sxs-lookup"><span data-stu-id="18a69-107">Containers can also include data that complements A/V streams, such as the title, languages of the audio streams, subtitle or caption tracks, fonts for those subtitles, images, chapter information, and menus.</span></span> <span data-ttu-id="18a69-108">MKV — это очень гибкий формат, поддерживающий многие из этих функций контейнера.</span><span class="sxs-lookup"><span data-stu-id="18a69-108">MKV is a highly flexible format that supports many of these container features.</span></span> <span data-ttu-id="18a69-109">Дополнительные сведения о формате MKV см. в разделе. [https://matroska.org](https://matroska.org/)</span><span class="sxs-lookup"><span data-stu-id="18a69-109">For more info about the MKV format, see [https://matroska.org](https://matroska.org/)</span></span>


## <a name="mkv-container-feature-support"></a><span data-ttu-id="18a69-110">Поддержка функций контейнеров MKV</span><span class="sxs-lookup"><span data-stu-id="18a69-110">MKV container feature support</span></span>
<span data-ttu-id="18a69-111">Функции контейнера MKV поддерживаются в Media Foundation следующими способами.</span><span class="sxs-lookup"><span data-stu-id="18a69-111">MKV container features are supported on the by Media Foundation in the following ways:</span></span>
- <span data-ttu-id="18a69-112">При наличии одной или нескольких видеодорожек будет воспроизводиться первая дорожка.</span><span class="sxs-lookup"><span data-stu-id="18a69-112">If one or more video tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="18a69-113">Если имеется одна или несколько звуковых дорожек, будет воспроизводиться первая дорожка.</span><span class="sxs-lookup"><span data-stu-id="18a69-113">If one or more audio tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="18a69-114">Записи субтитров поддерживаются, но не выбираются (воспроизводятся) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18a69-114">Caption tracks are supported, but are not selected (played) by default.</span></span>
- <span data-ttu-id="18a69-115">Если имеется один или несколько шрифтов или изображений, то заголовки и изображения не будут отображаться, хотя файл будет загружен и воспроизведен.</span><span class="sxs-lookup"><span data-stu-id="18a69-115">If one or more fonts or images are present, captions and images won’t render, although the file will load and play.</span></span>
- <span data-ttu-id="18a69-116">Сведения о меню не поддерживаются и не отображаются, но файл будет загружен и воспроизведен.</span><span class="sxs-lookup"><span data-stu-id="18a69-116">Menu information is not supported and won’t be displayed, but the file will load and play.</span></span>
- <span data-ttu-id="18a69-117">Если файлы с главами относятся к дополнительным файлам, дополнительные файлы не воспроизводятся.</span><span class="sxs-lookup"><span data-stu-id="18a69-117">If files with chapters refer to supplemental files, the supplemental files won’t play.</span></span>
- <span data-ttu-id="18a69-118">Миниатюрные изображения доступны при просмотре файлов на USB-накопителях с помощью обозревателя файлов.</span><span class="sxs-lookup"><span data-stu-id="18a69-118">Thumbnail images are available when browsing for files on USB drives using the file browser.</span></span>

<span data-ttu-id="18a69-119">Этот набор функций должен позволять воспроизводить большинство файлов MKV, если они содержат поддерживаемые кодеки.</span><span class="sxs-lookup"><span data-stu-id="18a69-119">This set of features should allow playback of most MKV files if they contain supported codecs.</span></span>
<span data-ttu-id="18a69-120">Поддерживаются файлы MKV, содержащие видео и звуковые дорожки, закодированные с помощью кодеков, перечисленных в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="18a69-120">MKV files that contain video and audio tracks encoded with the codecs listed in the following section are supported.</span></span>

## <a name="supported-mkv-codecs"></a><span data-ttu-id="18a69-121">Поддерживаемые кодеки MKV</span><span class="sxs-lookup"><span data-stu-id="18a69-121">Supported MKV codecs</span></span>

### <a name="video-codec-support-for-mkv"></a><span data-ttu-id="18a69-122">Поддержка видеокодеков для MKV</span><span class="sxs-lookup"><span data-stu-id="18a69-122">Video codec support for MKV</span></span>

<span data-ttu-id="18a69-123">Идентификатор матроска: V_MPEG4/ИСО/АВК</span><span class="sxs-lookup"><span data-stu-id="18a69-123">Matroska ID: V_MPEG4/ISO/AVC</span></span>

- <span data-ttu-id="18a69-124">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_H264</span><span class="sxs-lookup"><span data-stu-id="18a69-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span></span>
- <span data-ttu-id="18a69-125">Описание: H. 264 Video</span><span class="sxs-lookup"><span data-stu-id="18a69-125">Description: H.264 video</span></span>
- <span data-ttu-id="18a69-126">Идентификаторы FourCC или WAV: H264 Single bitrate</span><span class="sxs-lookup"><span data-stu-id="18a69-126">FourCC or WAV identifiers: H264</span></span>

<span data-ttu-id="18a69-127">Идентификатор матроска: V_MPEG2</span><span class="sxs-lookup"><span data-stu-id="18a69-127">Matroska ID: V_MPEG2</span></span>

- <span data-ttu-id="18a69-128">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span><span class="sxs-lookup"><span data-stu-id="18a69-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span></span>
- <span data-ttu-id="18a69-129">Описание: видео MPEG-2</span><span class="sxs-lookup"><span data-stu-id="18a69-129">Description: MPEG-2 video</span></span>

<span data-ttu-id="18a69-130">Идентификатор матроска: V_MPEG1</span><span class="sxs-lookup"><span data-stu-id="18a69-130">Matroska ID: V_MPEG1</span></span>

- <span data-ttu-id="18a69-131">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MPG1</span><span class="sxs-lookup"><span data-stu-id="18a69-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span></span>
- <span data-ttu-id="18a69-132">Описание: видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="18a69-132">Description: MPEG-1 video</span></span>
- <span data-ttu-id="18a69-133">Идентификаторы FourCC или WAV: MPG1</span><span class="sxs-lookup"><span data-stu-id="18a69-133">FourCC or WAV identifiers: MPG1</span></span>

<span data-ttu-id="18a69-134">Идентификатор матроска: V_MPEG4/MS/V3</span><span class="sxs-lookup"><span data-stu-id="18a69-134">Matroska ID: V_MPEG4/MS/V3</span></span>

- <span data-ttu-id="18a69-135">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MP43</span><span class="sxs-lookup"><span data-stu-id="18a69-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span></span>
- <span data-ttu-id="18a69-136">Описание: кодек Microsoft MPEG 4 версии 3</span><span class="sxs-lookup"><span data-stu-id="18a69-136">Description: Microsoft MPEG 4 codec version 3</span></span>
- <span data-ttu-id="18a69-137">Идентификаторы FourCC или WAV: MP43</span><span class="sxs-lookup"><span data-stu-id="18a69-137">FourCC or WAV identifiers: MP43</span></span>

<span data-ttu-id="18a69-138">Идентификатор матроска: V_MPEG4/ИСО/АСП</span><span class="sxs-lookup"><span data-stu-id="18a69-138">Matroska ID: V_MPEG4/ISO/ASP</span></span>

- <span data-ttu-id="18a69-139">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="18a69-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="18a69-140">Описание: видео MPEG-4 Part 2</span><span class="sxs-lookup"><span data-stu-id="18a69-140">Description: MPEG-4 part 2 video</span></span>
- <span data-ttu-id="18a69-141">Идентификаторы FourCC или WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="18a69-141">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="18a69-142">Идентификатор матроска: V_MS/ВФВ/ФАУРКК</span><span class="sxs-lookup"><span data-stu-id="18a69-142">Matroska ID: V_MS/VFW/FOURCC</span></span>

- <span data-ttu-id="18a69-143">Описание: сопоставляется с несколькими кодеками, которые обычно поддерживаются в формате AVI, доступном в консоли.</span><span class="sxs-lookup"><span data-stu-id="18a69-143">Description: Maps to several codecs usually supported in the AVI format that are available on the console.</span></span>

<span data-ttu-id="18a69-144">Идентификатор матроска: V_THEORA</span><span class="sxs-lookup"><span data-stu-id="18a69-144">Matroska ID: V_THEORA</span></span>

- <span data-ttu-id="18a69-145">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_Theora</span><span class="sxs-lookup"><span data-stu-id="18a69-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span></span>
- <span data-ttu-id="18a69-146">Описание: Сеора</span><span class="sxs-lookup"><span data-stu-id="18a69-146">Description: Theora</span></span>
- <span data-ttu-id="18a69-147">Идентификаторы FourCC или WAV: Сео</span><span class="sxs-lookup"><span data-stu-id="18a69-147">FourCC or WAV identifiers: theo</span></span>

<span data-ttu-id="18a69-148">Идентификатор матроска: V_MPEG4/ИСО/СП</span><span class="sxs-lookup"><span data-stu-id="18a69-148">Matroska ID: V_MPEG4/ISO/SP</span></span>

- <span data-ttu-id="18a69-149">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="18a69-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="18a69-150">Описание: простой профиль ISO MPEG4 (DivX4)</span><span class="sxs-lookup"><span data-stu-id="18a69-150">Description: MPEG4 ISO simple profile (DivX4)</span></span>
- <span data-ttu-id="18a69-151">Идентификаторы FourCC или WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="18a69-151">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="18a69-152">Идентификатор матроска: V_MPEG4/ИСО/ап</span><span class="sxs-lookup"><span data-stu-id="18a69-152">Matroska ID: V_MPEG4/ISO/AP</span></span>

- <span data-ttu-id="18a69-153">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="18a69-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="18a69-154">Описание: Расширенный простой профиль MPEG4 ISO (DivX5, Ксвид, FFMPEG)</span><span class="sxs-lookup"><span data-stu-id="18a69-154">Description: MPEG4 ISO advanced simple profile (DivX5, XviD, FFMPEG)</span></span>
- <span data-ttu-id="18a69-155">Идентификаторы FourCC или WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="18a69-155">FourCC or WAV identifiers: MP4V</span></span>


<span data-ttu-id="18a69-156">Идентификатор матроска: V_MPEGH/ИСО/ХЕВК</span><span class="sxs-lookup"><span data-stu-id="18a69-156">Matroska ID: V_MPEGH/ISO/HEVC</span></span> 

- <span data-ttu-id="18a69-157">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_HEVC</span><span class="sxs-lookup"><span data-stu-id="18a69-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span></span>
- <span data-ttu-id="18a69-158">Описание: HEVC/H. 265</span><span class="sxs-lookup"><span data-stu-id="18a69-158">Description: HEVC/H.265</span></span>
- <span data-ttu-id="18a69-159">Идентификаторы FourCC или WAV:</span><span class="sxs-lookup"><span data-stu-id="18a69-159">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="18a69-160">Идентификатор матроска: V_VP8</span><span class="sxs-lookup"><span data-stu-id="18a69-160">Matroska ID: V_VP8</span></span>

- <span data-ttu-id="18a69-161">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_VP80</span><span class="sxs-lookup"><span data-stu-id="18a69-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span></span>
- <span data-ttu-id="18a69-162">Описание: формат кодека VP8</span><span class="sxs-lookup"><span data-stu-id="18a69-162">Description: VP8 Codec format</span></span>
- <span data-ttu-id="18a69-163">Идентификаторы FourCC или WAV: VP80</span><span class="sxs-lookup"><span data-stu-id="18a69-163">FourCC or WAV identifiers: VP80</span></span>

<span data-ttu-id="18a69-164">Идентификатор матроска: V_VP9</span><span class="sxs-lookup"><span data-stu-id="18a69-164">Matroska ID: V_VP9</span></span>

- <span data-ttu-id="18a69-165">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_VP90</span><span class="sxs-lookup"><span data-stu-id="18a69-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span></span>
- <span data-ttu-id="18a69-166">Описание: формат кодека VP9</span><span class="sxs-lookup"><span data-stu-id="18a69-166">Description: VP9 Codec format</span></span>
- <span data-ttu-id="18a69-167">Идентификаторы FourCC или WAV: VP90</span><span class="sxs-lookup"><span data-stu-id="18a69-167">FourCC or WAV identifiers: VP90</span></span>

<span data-ttu-id="18a69-168">Идентификатор матроска: V_MJPEG</span><span class="sxs-lookup"><span data-stu-id="18a69-168">Matroska ID: V_MJPEG</span></span>

- <span data-ttu-id="18a69-169">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_MJPG</span><span class="sxs-lookup"><span data-stu-id="18a69-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span></span>
- <span data-ttu-id="18a69-170">Описание: перемещение в формате JPEG</span><span class="sxs-lookup"><span data-stu-id="18a69-170">Description: Motion JPEG</span></span>
- <span data-ttu-id="18a69-171">Идентификаторы FourCC или WAV: МЖПГ</span><span class="sxs-lookup"><span data-stu-id="18a69-171">FourCC or WAV identifiers: MJPG</span></span>

<span data-ttu-id="18a69-172">Идентификатор матроска: V_AV1</span><span class="sxs-lookup"><span data-stu-id="18a69-172">Matroska ID: V_AV1</span></span>

- <span data-ttu-id="18a69-173">Media Foundation MSFT MF_MT_SUBTYPE: MFVideoFormat_AV1</span><span class="sxs-lookup"><span data-stu-id="18a69-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span></span>
- <span data-ttu-id="18a69-174">Описание: Аомедиа видео 1</span><span class="sxs-lookup"><span data-stu-id="18a69-174">Description: AOMedia Video 1</span></span>
- <span data-ttu-id="18a69-175">Идентификаторы FourCC или WAV: AV01</span><span class="sxs-lookup"><span data-stu-id="18a69-175">FourCC or WAV identifiers: AV01</span></span>

### <a name="audio-codec-support-for-mkv"></a><span data-ttu-id="18a69-176">Поддержка аудиокодеков для MKV</span><span class="sxs-lookup"><span data-stu-id="18a69-176">Audio codec support for MKV</span></span>

<span data-ttu-id="18a69-177">Идентификатор матроска: A_AAC</span><span class="sxs-lookup"><span data-stu-id="18a69-177">Matroska ID: A_AAC</span></span>

- <span data-ttu-id="18a69-178">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="18a69-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="18a69-179">Описание: расширенное аудио кодирование (AAC)</span><span class="sxs-lookup"><span data-stu-id="18a69-179">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="18a69-180">Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="18a69-180">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="18a69-181">Идентификатор матроска: A_AC3</span><span class="sxs-lookup"><span data-stu-id="18a69-181">Matroska ID: A_AC3</span></span>

- <span data-ttu-id="18a69-182">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span><span class="sxs-lookup"><span data-stu-id="18a69-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span></span>
- <span data-ttu-id="18a69-183">Описание: Dolby AC3</span><span class="sxs-lookup"><span data-stu-id="18a69-183">Description: Dolby AC3</span></span>
- <span data-ttu-id="18a69-184">Идентификаторы FourCC или WAV: WAVE_FORMAT_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="18a69-184">FourCC or WAV identifiers: WAVE_FORMAT_DOLBY_AC3_SPDIF</span></span>

<span data-ttu-id="18a69-185">Идентификатор матроска: A_MPEG/L3</span><span class="sxs-lookup"><span data-stu-id="18a69-185">Matroska ID: A_MPEG/L3</span></span>

- <span data-ttu-id="18a69-186">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_MP3</span><span class="sxs-lookup"><span data-stu-id="18a69-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span></span>
- <span data-ttu-id="18a69-187">Описание: MPEG Audio Layer-3 (MP3)</span><span class="sxs-lookup"><span data-stu-id="18a69-187">Description: MPEG Audio Layer-3 (MP3)</span></span>
- <span data-ttu-id="18a69-188">Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="18a69-188">FourCC or WAV identifiers: WAVE_FORMAT_MPEGLAYER3</span></span>

<span data-ttu-id="18a69-189">Идентификатор матроска: A_MPEG/L1</span><span class="sxs-lookup"><span data-stu-id="18a69-189">Matroska ID: A_MPEG/L1</span></span>

- <span data-ttu-id="18a69-190">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="18a69-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="18a69-191">Описание: полезные данные звука MPEG-1</span><span class="sxs-lookup"><span data-stu-id="18a69-191">Description: MPEG-1 audio payload</span></span>
- <span data-ttu-id="18a69-192">Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="18a69-192">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="18a69-193">Идентификатор матроска: A_PCM/Инт/Биг</span><span class="sxs-lookup"><span data-stu-id="18a69-193">Matroska ID: A_PCM/INT/BIG</span></span>

- <span data-ttu-id="18a69-194">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="18a69-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="18a69-195">Описание: несжатая звукозапись PCM</span><span class="sxs-lookup"><span data-stu-id="18a69-195">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="18a69-196">Идентификаторы FourCC или WAV: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="18a69-196">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="18a69-197">Идентификатор матроска: A_PCM/Инт/лит</span><span class="sxs-lookup"><span data-stu-id="18a69-197">Matroska ID: A_PCM/INT/LIT</span></span>

- <span data-ttu-id="18a69-198">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="18a69-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="18a69-199">Описание: несжатая звукозапись PCM</span><span class="sxs-lookup"><span data-stu-id="18a69-199">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="18a69-200">Идентификаторы FourCC или WAV: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="18a69-200">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="18a69-201">Идентификатор матроска: A_PCM/ФЛОАТ/ИИЕ</span><span class="sxs-lookup"><span data-stu-id="18a69-201">Matroska ID: A_PCM/FLOAT/IEEE</span></span>

- <span data-ttu-id="18a69-202">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Float</span><span class="sxs-lookup"><span data-stu-id="18a69-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span></span>
- <span data-ttu-id="18a69-203">Описание: несжатое аудио с плавающей запятой IEEE</span><span class="sxs-lookup"><span data-stu-id="18a69-203">Description: Uncompressed IEEE floating-point audio</span></span>
- <span data-ttu-id="18a69-204">Идентификаторы FourCC или WAV: WAVE_FORMAT_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="18a69-204">FourCC or WAV identifiers: WAVE_FORMAT_IEEE_FLOAT</span></span>

<span data-ttu-id="18a69-205">Идентификатор матроска: A_ALAC</span><span class="sxs-lookup"><span data-stu-id="18a69-205">Matroska ID: A_ALAC</span></span>

- <span data-ttu-id="18a69-206">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_ALAC</span><span class="sxs-lookup"><span data-stu-id="18a69-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span></span>
- <span data-ttu-id="18a69-207">Описание: аудиокодек Apple без звука</span><span class="sxs-lookup"><span data-stu-id="18a69-207">Description: Apple Lossless Audio Codec</span></span>
- <span data-ttu-id="18a69-208">Идентификаторы FourCC или WAV:</span><span class="sxs-lookup"><span data-stu-id="18a69-208">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="18a69-209">Идентификатор матроска: A_MPEG/L2</span><span class="sxs-lookup"><span data-stu-id="18a69-209">Matroska ID: A_MPEG/L2</span></span>

- <span data-ttu-id="18a69-210">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="18a69-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="18a69-211">Описание: MPEG Audio 1, 2 Layer II</span><span class="sxs-lookup"><span data-stu-id="18a69-211">Description: MPEG Audio 1, 2 Layer II</span></span>
- <span data-ttu-id="18a69-212">Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="18a69-212">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="18a69-213">Идентификатор матроска: A_DTS</span><span class="sxs-lookup"><span data-stu-id="18a69-213">Matroska ID: A_DTS</span></span>

- <span data-ttu-id="18a69-214">Media Foundation MSFT MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span><span class="sxs-lookup"><span data-stu-id="18a69-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span></span>
- <span data-ttu-id="18a69-215">Описание: система Digital режим театра System</span><span class="sxs-lookup"><span data-stu-id="18a69-215">Description: Digital Theatre System</span></span>
- <span data-ttu-id="18a69-216">Идентификаторы FourCC или WAV: WAVE_FORMAT_DTS</span><span class="sxs-lookup"><span data-stu-id="18a69-216">FourCC or WAV identifiers: WAVE_FORMAT_DTS</span></span>

<span data-ttu-id="18a69-217">Идентификатор матроска: A_OPUS</span><span class="sxs-lookup"><span data-stu-id="18a69-217">Matroska ID: A_OPUS</span></span>

- <span data-ttu-id="18a69-218">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Opus</span><span class="sxs-lookup"><span data-stu-id="18a69-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span></span>
- <span data-ttu-id="18a69-219">Описание: опус</span><span class="sxs-lookup"><span data-stu-id="18a69-219">Description: Opus</span></span>
- <span data-ttu-id="18a69-220">Идентификаторы FourCC или WAV: WAVE_FORMAT_OPUS</span><span class="sxs-lookup"><span data-stu-id="18a69-220">FourCC or WAV identifiers: WAVE_FORMAT_OPUS</span></span>

<span data-ttu-id="18a69-221">Идентификатор матроска: A_VORBIS</span><span class="sxs-lookup"><span data-stu-id="18a69-221">Matroska ID: A_VORBIS</span></span>

- <span data-ttu-id="18a69-222">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span><span class="sxs-lookup"><span data-stu-id="18a69-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span></span>
- <span data-ttu-id="18a69-223">Описание: Vorbis</span><span class="sxs-lookup"><span data-stu-id="18a69-223">Description: Vorbis</span></span>
- <span data-ttu-id="18a69-224">Идентификаторы FourCC или WAV:</span><span class="sxs-lookup"><span data-stu-id="18a69-224">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="18a69-225">Идентификатор матроска: A_FLAC</span><span class="sxs-lookup"><span data-stu-id="18a69-225">Matroska ID: A_FLAC</span></span>

- <span data-ttu-id="18a69-226">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_FLAC</span><span class="sxs-lookup"><span data-stu-id="18a69-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span></span>
- <span data-ttu-id="18a69-227">Описание: бесплатный аудиокодек без потерь</span><span class="sxs-lookup"><span data-stu-id="18a69-227">Description: Free Lossless Audio Codec</span></span>
- <span data-ttu-id="18a69-228">Идентификаторы FourCC или WAV: WAVE_FORMAT_FLAC</span><span class="sxs-lookup"><span data-stu-id="18a69-228">FourCC or WAV identifiers: WAVE_FORMAT_FLAC</span></span>

<span data-ttu-id="18a69-229">Идентификатор матроска: A_AAC/MAIN</span><span class="sxs-lookup"><span data-stu-id="18a69-229">Matroska ID: A_AAC/MAIN</span></span>

- <span data-ttu-id="18a69-230">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="18a69-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="18a69-231">Описание: расширенное аудио кодирование (AAC)</span><span class="sxs-lookup"><span data-stu-id="18a69-231">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="18a69-232">Идентификаторы FourCC или WAV: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="18a69-232">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="18a69-233">Идентификатор матроска: A_EAC3</span><span class="sxs-lookup"><span data-stu-id="18a69-233">Matroska ID: A_EAC3</span></span>

- <span data-ttu-id="18a69-234">Media Foundation MSFT MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span><span class="sxs-lookup"><span data-stu-id="18a69-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span></span>
- <span data-ttu-id="18a69-235">Описание: Расширенный AC-3</span><span class="sxs-lookup"><span data-stu-id="18a69-235">Description: Enhanced AC-3</span></span>
- <span data-ttu-id="18a69-236">Идентификаторы FourCC или WAV:</span><span class="sxs-lookup"><span data-stu-id="18a69-236">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="18a69-237">Идентификатор матроска: A_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="18a69-237">Matroska ID: A_TRUEHD</span></span>

- <span data-ttu-id="18a69-238">Media Foundation MSFT MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="18a69-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span></span>
- <span data-ttu-id="18a69-239">Описание: Dolby Труехд</span><span class="sxs-lookup"><span data-stu-id="18a69-239">Description: Dolby TrueHD</span></span>
- <span data-ttu-id="18a69-240">Идентификаторы FourCC или WAV:</span><span class="sxs-lookup"><span data-stu-id="18a69-240">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="18a69-241">Идентификатор матроска: A_MS/АКМ</span><span class="sxs-lookup"><span data-stu-id="18a69-241">Matroska ID: A_MS/ACM</span></span>

- <span data-ttu-id="18a69-242">MSFT Media Foundation MF_MT_SUBTYPE: сопоставляется с несколькими WAVE_FORMAT звуковыми типами, определенными в ммрег. h</span><span class="sxs-lookup"><span data-stu-id="18a69-242">MSFT Media Foundation MF_MT_SUBTYPE: Maps to several WAVE_FORMAT audio types defined in mmreg.h</span></span>


### <a name="subtitles-codec-support-for-mkv"></a><span data-ttu-id="18a69-243">Поддержка кодеков субтитров для MKV</span><span class="sxs-lookup"><span data-stu-id="18a69-243">Subtitles codec support for MKV</span></span>

<span data-ttu-id="18a69-244">Идентификатор матроска: S_TEXT/АСЦИИ</span><span class="sxs-lookup"><span data-stu-id="18a69-244">Matroska ID: S_TEXT/ASCII</span></span>

- <span data-ttu-id="18a69-245">Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="18a69-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="18a69-246">Описание: текст ASCII</span><span class="sxs-lookup"><span data-stu-id="18a69-246">Description: ASCII text</span></span>

<span data-ttu-id="18a69-247">Идентификатор матроска: S_TEXT/UTF8</span><span class="sxs-lookup"><span data-stu-id="18a69-247">Matroska ID: S_TEXT/UTF8</span></span>

- <span data-ttu-id="18a69-248">Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="18a69-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="18a69-249">Описание: обычный текст в кодировке UTF-8</span><span class="sxs-lookup"><span data-stu-id="18a69-249">Description: UTF-8 Plain Text</span></span>

<span data-ttu-id="18a69-250">Идентификатор матроска: S_TEXT/ССА</span><span class="sxs-lookup"><span data-stu-id="18a69-250">Matroska ID: S_TEXT/SSA</span></span>

- <span data-ttu-id="18a69-251">Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="18a69-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="18a69-252">Описание: формат субтитров</span><span class="sxs-lookup"><span data-stu-id="18a69-252">Description: Subtitles Format</span></span>

<span data-ttu-id="18a69-253">Идентификатор матроска: S_TEXT/АСС</span><span class="sxs-lookup"><span data-stu-id="18a69-253">Matroska ID: S_TEXT/ASS</span></span>

- <span data-ttu-id="18a69-254">Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="18a69-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="18a69-255">Описание: формат расширенных субтитров</span><span class="sxs-lookup"><span data-stu-id="18a69-255">Description: Advanced Subtitles Format</span></span>

<span data-ttu-id="18a69-256">Идентификатор матроска: S_VOBSUB</span><span class="sxs-lookup"><span data-stu-id="18a69-256">Matroska ID: S_VOBSUB</span></span>

- <span data-ttu-id="18a69-257">Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span><span class="sxs-lookup"><span data-stu-id="18a69-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span></span>
- <span data-ttu-id="18a69-258">Описание: субтитры Вобсуб</span><span class="sxs-lookup"><span data-stu-id="18a69-258">Description: VobSub subtitles</span></span>

<span data-ttu-id="18a69-259">Идентификатор матроска: S_HDMV/ПГС</span><span class="sxs-lookup"><span data-stu-id="18a69-259">Matroska ID: S_HDMV/PGS</span></span>

- <span data-ttu-id="18a69-260">Media Foundation MSFT MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span><span class="sxs-lookup"><span data-stu-id="18a69-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span></span>
- <span data-ttu-id="18a69-261">Описание: ХДМВ презентации субтитры графики (ПГС)</span><span class="sxs-lookup"><span data-stu-id="18a69-261">Description: HDMV presentation graphics subtitles (PGS)</span></span>


## <a name="technical-details-regarding-codecs"></a><span data-ttu-id="18a69-262">Технические сведения о кодеках</span><span class="sxs-lookup"><span data-stu-id="18a69-262">Technical details regarding codecs</span></span>

<span data-ttu-id="18a69-263">Технические сведения о кодеках см. в следующих статьях.</span><span class="sxs-lookup"><span data-stu-id="18a69-263">See the following for technical details regarding codecs.</span></span>

- [<span data-ttu-id="18a69-264">Спецификации кодека матроска</span><span class="sxs-lookup"><span data-stu-id="18a69-264">Matroska Codec Specs</span></span>](http://www.matroska.org/technical/specs/codecid/index.html)
- [<span data-ttu-id="18a69-265">Идентификаторы GUID для подтипов звука</span><span class="sxs-lookup"><span data-stu-id="18a69-265">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
- [<span data-ttu-id="18a69-266">Идентификаторы GUID для подтипов видео</span><span class="sxs-lookup"><span data-stu-id="18a69-266">Video Subtype GUIDs</span></span>](video-subtype-guids.md)


## <a name="related-topics"></a><span data-ttu-id="18a69-267">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="18a69-267">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18a69-268">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18a69-268">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="18a69-269">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="18a69-269">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



