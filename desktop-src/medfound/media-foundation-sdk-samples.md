---
description: В этом разделе описываются примеры приложений, демонстрирующие использование Media Foundation. Encoding Самплесплайбакк SamplesPlug-InsSource Самплесвидео Каптуремисцелланеаус Самплесдепрекатед или устаревшие разделы Самплесрелатед
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Примеры пакетов SDK Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f335b5ba744b098efdb7570aa861ad36fc9216cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820245"
---
# <a name="media-foundation-sdk-samples"></a><span data-ttu-id="21d51-103">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21d51-103">Media Foundation SDK Samples</span></span>

<span data-ttu-id="21d51-104">В этом разделе описываются примеры приложений, демонстрирующие использование Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="21d51-104">This section describes sample applications that demonstrate how to use Media Foundation.</span></span>

-   [<span data-ttu-id="21d51-105">Примеры кодировки</span><span class="sxs-lookup"><span data-stu-id="21d51-105">Encoding Samples</span></span>](#encoding-samples)
-   [<span data-ttu-id="21d51-106">Примеры воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21d51-106">Playback Samples</span></span>](#playback-samples)
-   [<span data-ttu-id="21d51-107">Подключаемые модули</span><span class="sxs-lookup"><span data-stu-id="21d51-107">Plug-Ins</span></span>](#plug-ins)
-   [<span data-ttu-id="21d51-108">Примеры модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="21d51-108">Source Reader Samples</span></span>](#source-reader-samples)
-   [<span data-ttu-id="21d51-109">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="21d51-109">Video Capture</span></span>](#video-capture)
-   [<span data-ttu-id="21d51-110">Прочие примеры</span><span class="sxs-lookup"><span data-stu-id="21d51-110">Miscellaneous Samples</span></span>](#miscellaneous-samples)
-   [<span data-ttu-id="21d51-111">Устаревшие или устаревшие примеры</span><span class="sxs-lookup"><span data-stu-id="21d51-111">Deprecated or Obsolete Samples</span></span>](#deprecated-or-obsolete-samples)
-   [<span data-ttu-id="21d51-112">См. также</span><span class="sxs-lookup"><span data-stu-id="21d51-112">Related topics</span></span>](#related-topics)

## <a name="encoding-samples"></a><span data-ttu-id="21d51-113">Примеры кодировки</span><span class="sxs-lookup"><span data-stu-id="21d51-113">Encoding Samples</span></span>



| <span data-ttu-id="21d51-114">Образец</span><span class="sxs-lookup"><span data-stu-id="21d51-114">Sample</span></span>                            | <span data-ttu-id="21d51-115">Описание</span><span class="sxs-lookup"><span data-stu-id="21d51-115">Description</span></span>                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="21d51-116">Перекодировать</span><span class="sxs-lookup"><span data-stu-id="21d51-116">Transcode</span></span>](transcode-sample.md) | <span data-ttu-id="21d51-117">Показывает, как перекодировать файл мультимедиа в формат Windows Media.</span><span class="sxs-lookup"><span data-stu-id="21d51-117">Shows how to reencode a media file to Windows Media format.</span></span> |



 

## <a name="playback-samples"></a><span data-ttu-id="21d51-118">Примеры воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21d51-118">Playback Samples</span></span>



| <span data-ttu-id="21d51-119">Образец</span><span class="sxs-lookup"><span data-stu-id="21d51-119">Sample</span></span>                                            | <span data-ttu-id="21d51-120">Описание</span><span class="sxs-lookup"><span data-stu-id="21d51-120">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21d51-121">[басикплайбакк](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21d51-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span></span>          | <span data-ttu-id="21d51-122">Воспроизводит аудио и видео файлы с помощью [сеанса мультимедиа](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="21d51-122">Plays audio and video files by using the [Media Session](media-session.md).</span></span> <span data-ttu-id="21d51-123">В этом примере показано, как создавать топологии воспроизведения, управлять сеансом мультимедиа и принимать события сеанса во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="21d51-123">This sample demonstrates how to create playback topologies, control the Media Session, and receive session events during playback.</span></span> |
| <span data-ttu-id="21d51-124">[мфплайер](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21d51-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span></span>                    | <span data-ttu-id="21d51-125">Демонстрирует некоторые функции воспроизведения, которые не включены в пример [басикплайбакк](/previous-versions//bb970475(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="21d51-125">Demonstrates some playback functions that are not included in the [BasicPlayback](/previous-versions//bb970475(v=vs.85)) sample.</span></span>                                                                                              |
| [<span data-ttu-id="21d51-126">протектедплайбакк</span><span class="sxs-lookup"><span data-stu-id="21d51-126">ProtectedPlayback</span></span>](protectedplayback-sample.md) | <span data-ttu-id="21d51-127">Воспроизводит защищенные аудио и видеофайлы.</span><span class="sxs-lookup"><span data-stu-id="21d51-127">Plays protected audio and video files.</span></span> <span data-ttu-id="21d51-128">В этом примере показано, как использовать сеанс защищенного пути к носителю (PMP) и как использовать объекты средства включения содержимого.</span><span class="sxs-lookup"><span data-stu-id="21d51-128">This sample shows how to use the protected media path (PMP) session and how to use content enabler objects.</span></span>                                                              |



 

## <a name="plug-ins"></a><span data-ttu-id="21d51-129">Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="21d51-129">Plug-Ins</span></span>



| <span data-ttu-id="21d51-130">Образец</span><span class="sxs-lookup"><span data-stu-id="21d51-130">Sample</span></span>                                       | <span data-ttu-id="21d51-131">Sub-Area</span><span class="sxs-lookup"><span data-stu-id="21d51-131">Sub-Area</span></span>                         | <span data-ttu-id="21d51-132">Описание</span><span class="sxs-lookup"><span data-stu-id="21d51-132">Description</span></span>                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21d51-133">Показан</span><span class="sxs-lookup"><span data-stu-id="21d51-133">Decoder</span></span>](decoder-sample.md)                | <span data-ttu-id="21d51-134">Преобразование Media Foundation (MFT)</span><span class="sxs-lookup"><span data-stu-id="21d51-134">Media Foundation transform (MFT)</span></span> | <span data-ttu-id="21d51-135">Видеодекодер.</span><span class="sxs-lookup"><span data-stu-id="21d51-135">Video decoder.</span></span>                                                                                         |
| [<span data-ttu-id="21d51-136">еврпресентер</span><span class="sxs-lookup"><span data-stu-id="21d51-136">EVRPresenter</span></span>](evrpresenter-sample.md)      | <span data-ttu-id="21d51-137">Разное</span><span class="sxs-lookup"><span data-stu-id="21d51-137">Miscellaneous</span></span>                    | <span data-ttu-id="21d51-138">Пользовательский Presenter для [расширенного обработчика видео](enhanced-video-renderer.md) (Евр).</span><span class="sxs-lookup"><span data-stu-id="21d51-138">Custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span>                 |
| [<span data-ttu-id="21d51-139">\_АУДИОДЕЛАЙ MFT</span><span class="sxs-lookup"><span data-stu-id="21d51-139">MFT\_AudioDelay</span></span>](mft-audiodelay-sample.md) | <span data-ttu-id="21d51-140">ИСХОДНОЙ</span><span class="sxs-lookup"><span data-stu-id="21d51-140">MFT</span></span>                              | <span data-ttu-id="21d51-141">Преобразование звуковых эффектов.</span><span class="sxs-lookup"><span data-stu-id="21d51-141">Audio effect transform.</span></span> <span data-ttu-id="21d51-142">Показывает, как написать базовый MFT для обработки аудио.</span><span class="sxs-lookup"><span data-stu-id="21d51-142">Shows how to write a basic MFT for audio processing.</span></span>                           |
| [<span data-ttu-id="21d51-143">\_Черновая Таблица MFT</span><span class="sxs-lookup"><span data-stu-id="21d51-143">MFT\_Grayscale</span></span>](mft-grayscale-sample.md)   | <span data-ttu-id="21d51-144">ИСХОДНОЙ</span><span class="sxs-lookup"><span data-stu-id="21d51-144">MFT</span></span>                              | <span data-ttu-id="21d51-145">Видео в градациях серого.</span><span class="sxs-lookup"><span data-stu-id="21d51-145">Grayscale video effect.</span></span> <span data-ttu-id="21d51-146">Показывает, как написать базовый файл MFT для обработки видео.</span><span class="sxs-lookup"><span data-stu-id="21d51-146">Shows how to write a basic MFT for video processing.</span></span>                           |
| [<span data-ttu-id="21d51-147">MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="21d51-147">MPEG1Source</span></span>](mpeg1source-sample.md)        | <span data-ttu-id="21d51-148">Источник мультимедиа</span><span class="sxs-lookup"><span data-stu-id="21d51-148">Media source</span></span>                     | <span data-ttu-id="21d51-149">Анализирует потоки на уровне системы MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="21d51-149">Parses MPEG-1 systems-layer streams.</span></span> <span data-ttu-id="21d51-150">Показывает, как написать пользовательский источник мультимедиа и обработчик потока байтов.</span><span class="sxs-lookup"><span data-stu-id="21d51-150">Shows how to write a custom media source and byte-stream handler.</span></span> |
| [<span data-ttu-id="21d51-151">вавсинк</span><span class="sxs-lookup"><span data-stu-id="21d51-151">WavSink</span></span>](wavsink-sample.md)                | <span data-ttu-id="21d51-152">Приемник мультимедиа</span><span class="sxs-lookup"><span data-stu-id="21d51-152">Media sink</span></span>                       | <span data-ttu-id="21d51-153">Приемник архива, записывающий WAV файлы.</span><span class="sxs-lookup"><span data-stu-id="21d51-153">An archive sink that writes .wav files.</span></span> <span data-ttu-id="21d51-154">Показывает, как написать пользовательский приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="21d51-154">Shows how to write a custom media sink.</span></span>                        |
| [<span data-ttu-id="21d51-155">вавсаурце</span><span class="sxs-lookup"><span data-stu-id="21d51-155">WavSource</span></span>](wavsource-sample.md)            | <span data-ttu-id="21d51-156">Источник мультимедиа</span><span class="sxs-lookup"><span data-stu-id="21d51-156">Media source</span></span>                     | <span data-ttu-id="21d51-157">Выполняет синтаксический анализ WAV файлов.</span><span class="sxs-lookup"><span data-stu-id="21d51-157">Parses .wav files.</span></span> <span data-ttu-id="21d51-158">Показывает, как написать пользовательский источник мультимедиа и обработчик потока байтов.</span><span class="sxs-lookup"><span data-stu-id="21d51-158">Shows how to write a custom media source and byte-stream handler.</span></span>                   |



 

## <a name="source-reader-samples"></a><span data-ttu-id="21d51-159">Примеры модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="21d51-159">Source Reader Samples</span></span>



| <span data-ttu-id="21d51-160">Образец</span><span class="sxs-lookup"><span data-stu-id="21d51-160">Sample</span></span>                                      | <span data-ttu-id="21d51-161">Описание</span><span class="sxs-lookup"><span data-stu-id="21d51-161">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="21d51-162">Аудиоклип</span><span class="sxs-lookup"><span data-stu-id="21d51-162">Audio Clip</span></span>](audio-clip-sample.md)         | <span data-ttu-id="21d51-163">Использует [модуль чтения исходного кода](source-reader.md) для декодирования звука из файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="21d51-163">Uses the [Source Reader](source-reader.md) to decode audio from a media file.</span></span>      |
| [<span data-ttu-id="21d51-164">видеосумбнаил</span><span class="sxs-lookup"><span data-stu-id="21d51-164">VideoThumbnail</span></span>](videothumbnail-sample.md) | <span data-ttu-id="21d51-165">Использует [модуль чтения исходного кода](source-reader.md) для получения отдельных кадров из файла видео.</span><span class="sxs-lookup"><span data-stu-id="21d51-165">Uses the [Source Reader](source-reader.md) to get single frames from a video file.</span></span> |



 

## <a name="video-capture"></a><span data-ttu-id="21d51-166">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="21d51-166">Video Capture</span></span>



| <span data-ttu-id="21d51-167">Образец</span><span class="sxs-lookup"><span data-stu-id="21d51-167">Sample</span></span>                                        | <span data-ttu-id="21d51-168">Описание</span><span class="sxs-lookup"><span data-stu-id="21d51-168">Description</span></span>                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21d51-169">MFCaptureD3D</span><span class="sxs-lookup"><span data-stu-id="21d51-169">MFCaptureD3D</span></span>](mfcaptured3d-sample.md)       | <span data-ttu-id="21d51-170">Демонстрация просмотра видео с устройства видеозаписи с помощью Direct3D для подготовки к просмотру видео.</span><span class="sxs-lookup"><span data-stu-id="21d51-170">Shows how to preview video from a video capture device, using Direct3D to render the video.</span></span> |
| [<span data-ttu-id="21d51-171">мфкаптуретофиле</span><span class="sxs-lookup"><span data-stu-id="21d51-171">MFCaptureToFile</span></span>](mfcapturetofile-sample.md) | <span data-ttu-id="21d51-172">Показывает, как записать видео из видеокамеры в файл.</span><span class="sxs-lookup"><span data-stu-id="21d51-172">Shows how to capture video from a video camera to a file.</span></span>                                   |



 

## <a name="miscellaneous-samples"></a><span data-ttu-id="21d51-173">Прочие примеры</span><span class="sxs-lookup"><span data-stu-id="21d51-173">Miscellaneous Samples</span></span>



| <span data-ttu-id="21d51-174">Образец</span><span class="sxs-lookup"><span data-stu-id="21d51-174">Sample</span></span>                                         | <span data-ttu-id="21d51-175">Описание</span><span class="sxs-lookup"><span data-stu-id="21d51-175">Description</span></span>                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21d51-176">асфпарсер</span><span class="sxs-lookup"><span data-stu-id="21d51-176">ASFParser</span></span>](asfparser-sample.md)              | <span data-ttu-id="21d51-177">Показывает, как анализировать данные из ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="21d51-177">Shows how to parse data from an Advanced Systems Format (ASF) file.</span></span>                                                                                   |
| [<span data-ttu-id="21d51-178">ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="21d51-178">DXVA-HD</span></span>](dxva-hd-sample.md)                  | <span data-ttu-id="21d51-179">Показывает, как использовать высокое определение (ДКСВА-HD) ускорения видео Microsoft DirectX High Definition.</span><span class="sxs-lookup"><span data-stu-id="21d51-179">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>                                                                      |
| [<span data-ttu-id="21d51-180">DXVA2 \_ видеопрок</span><span class="sxs-lookup"><span data-stu-id="21d51-180">DXVA2\_VideoProc</span></span>](dxva2-videoproc-sample.md) | <span data-ttu-id="21d51-181">Использует ускорение видео DirectX (ДКСВА) 2,0 для создания потока видео 4:2:2 YUV.</span><span class="sxs-lookup"><span data-stu-id="21d51-181">Uses DirectX Video Acceleration (DXVA) 2.0 to create a stream of 4:2:2 YUV video.</span></span> <span data-ttu-id="21d51-182">В этом примере показано, как использовать функции обработки видео в ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="21d51-182">This sample shows how to use the video processing features of DXVA.</span></span> |



 

## <a name="deprecated-or-obsolete-samples"></a><span data-ttu-id="21d51-183">Устаревшие или устаревшие примеры</span><span class="sxs-lookup"><span data-stu-id="21d51-183">Deprecated or Obsolete Samples</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21d51-184">Образец</span><span class="sxs-lookup"><span data-stu-id="21d51-184">Sample</span></span></th>
<th><span data-ttu-id="21d51-185">Описание</span><span class="sxs-lookup"><span data-stu-id="21d51-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21d51-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span><span class="sxs-lookup"><span data-stu-id="21d51-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span></span></td>
<td><span data-ttu-id="21d51-187">Демонстрирует некоторые дополнительные возможности воспроизведения API <a href="using-mfplay-for-audio-video-playback.md">мфплай</a> .</span><span class="sxs-lookup"><span data-stu-id="21d51-187">Demonstrates some advanced playback features of the <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> API.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21d51-188"><a href="/previous-versions//bb970336(v=vs.85)">плайбаккфкс</a></span><span class="sxs-lookup"><span data-stu-id="21d51-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span></span></td>
<td><span data-ttu-id="21d51-189">Применяет к видео эффекты градаций серого.</span><span class="sxs-lookup"><span data-stu-id="21d51-189">Applies a grayscale effect to video.</span></span> <span data-ttu-id="21d51-190">Показывает, как вставить МФТС в топологию воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="21d51-190">Shows how to insert MFTs into a playback topology.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="21d51-191">Этот пример больше не включен в пакет SDK.</span><span class="sxs-lookup"><span data-stu-id="21d51-191">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21d51-192"><a href="playlist-sample.md">Списком</a></span><span class="sxs-lookup"><span data-stu-id="21d51-192"><a href="playlist-sample.md">Playlist</a></span></span></td>
<td><span data-ttu-id="21d51-193">Воспроизводит последовательность звуковых файлов с помощью источника Sequencer.</span><span class="sxs-lookup"><span data-stu-id="21d51-193">Plays a sequence of audio files using the sequencer source.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="21d51-194">Этот пример больше не включен в пакет SDK.</span><span class="sxs-lookup"><span data-stu-id="21d51-194">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21d51-195"><a href="simplecapture-sample.md">симплекаптуре</a></span><span class="sxs-lookup"><span data-stu-id="21d51-195"><a href="simplecapture-sample.md">SimpleCapture</a></span></span></td>
<td><span data-ttu-id="21d51-196">Демонстрация предварительного просмотра видео с устройства видеозаписи с помощью API Мфплай.</span><span class="sxs-lookup"><span data-stu-id="21d51-196">Shows how to preview video from a video capture device, using the MFPlay API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21d51-197"><a href="simpleplay-sample.md">симплеплай</a></span><span class="sxs-lookup"><span data-stu-id="21d51-197"><a href="simpleplay-sample.md">SimplePlay</a></span></span></td>
<td><span data-ttu-id="21d51-198">Показывает, как воспроизвести файл мультимедиа с помощью API Мфплай.</span><span class="sxs-lookup"><span data-stu-id="21d51-198">Shows how to play a media file using the MFPlay API.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="21d51-199">См. также</span><span class="sxs-lookup"><span data-stu-id="21d51-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21d51-200">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21d51-200">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="21d51-201">О Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21d51-201">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
