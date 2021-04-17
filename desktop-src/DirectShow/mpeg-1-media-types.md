---
description: В этом разделе перечислены типы носителей, используемые для данных MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Типы мультимедиа MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684750"
---
# <a name="mpeg-1-media-types"></a><span data-ttu-id="338c8-103">Типы мультимедиа MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-103">MPEG-1 Media Types</span></span>

<span data-ttu-id="338c8-104">В этом разделе перечислены типы носителей, используемые для данных MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="338c8-104">This section lists the media types used for MPEG-1 data.</span></span>

## <a name="mpeg-1-system-stream"></a><span data-ttu-id="338c8-105">Системный поток MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-105">MPEG-1 System Stream</span></span>



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| <span data-ttu-id="338c8-106">Основной тип</span><span class="sxs-lookup"><span data-stu-id="338c8-106">Major type</span></span>            | <span data-ttu-id="338c8-107">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="338c8-107">MEDIATYPE\_Stream</span></span>                               |
| <span data-ttu-id="338c8-108">Subtype</span><span class="sxs-lookup"><span data-stu-id="338c8-108">Subtype</span></span>               | <span data-ttu-id="338c8-109">МЕДИАСУБТИПЕ \_ MPEG1System</span><span class="sxs-lookup"><span data-stu-id="338c8-109">MEDIASUBTYPE\_MPEG1System</span></span>                       |
| <span data-ttu-id="338c8-110">Тип формата</span><span class="sxs-lookup"><span data-stu-id="338c8-110">Format Type</span></span>           | <span data-ttu-id="338c8-111">ФОРМАТ \_ мпегстреамс</span><span class="sxs-lookup"><span data-stu-id="338c8-111">FORMAT\_MPEGStreams</span></span>                             |
| <span data-ttu-id="338c8-112">Структура формата</span><span class="sxs-lookup"><span data-stu-id="338c8-112">Format Structure</span></span>      | [<span data-ttu-id="338c8-113">**\_мпегсистемтипе**</span><span class="sxs-lookup"><span data-stu-id="338c8-113">**AM\_MPEGSYSTEMTYPE**</span></span>](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| <span data-ttu-id="338c8-114">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="338c8-114">Media Sample Contents</span></span> | <span data-ttu-id="338c8-115">Байтовый поток; без выравнивания</span><span class="sxs-lookup"><span data-stu-id="338c8-115">Byte stream; no alignment</span></span>                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a><span data-ttu-id="338c8-116">Системный поток MPEG-1 с компакт-диска видео</span><span class="sxs-lookup"><span data-stu-id="338c8-116">MPEG-1 System Stream from Video CD</span></span>



|                       |                            |
|-----------------------|----------------------------|
| <span data-ttu-id="338c8-117">Основной тип</span><span class="sxs-lookup"><span data-stu-id="338c8-117">Major type</span></span>            | <span data-ttu-id="338c8-118">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="338c8-118">MEDIATYPE\_Stream</span></span>          |
| <span data-ttu-id="338c8-119">Subtype</span><span class="sxs-lookup"><span data-stu-id="338c8-119">Subtype</span></span>               | <span data-ttu-id="338c8-120">МЕДИАСУБТИПЕ \_ MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="338c8-120">MEDIASUBTYPE\_MPEG1VideoCD</span></span> |
| <span data-ttu-id="338c8-121">Тип формата</span><span class="sxs-lookup"><span data-stu-id="338c8-121">Format Type</span></span>           | <span data-ttu-id="338c8-122">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="338c8-122">GUID\_NULL</span></span>                 |
| <span data-ttu-id="338c8-123">Структура формата</span><span class="sxs-lookup"><span data-stu-id="338c8-123">Format Structure</span></span>      | <span data-ttu-id="338c8-124">Нет</span><span class="sxs-lookup"><span data-stu-id="338c8-124">None</span></span>                       |
| <span data-ttu-id="338c8-125">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="338c8-125">Media Sample Contents</span></span> | <span data-ttu-id="338c8-126">Байтовый поток; без выравнивания.</span><span class="sxs-lookup"><span data-stu-id="338c8-126">Byte stream; no alignment.</span></span> |



 

## <a name="mpeg-1-audio-packet"></a><span data-ttu-id="338c8-127">Звуковой пакет MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-127">MPEG-1 Audio Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="338c8-128">Основной тип</span><span class="sxs-lookup"><span data-stu-id="338c8-128">Major type</span></span>            | <span data-ttu-id="338c8-129">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="338c8-129">MEDIATYPE\_Audio</span></span>                               |
| <span data-ttu-id="338c8-130">Subtype</span><span class="sxs-lookup"><span data-stu-id="338c8-130">Subtype</span></span>               | <span data-ttu-id="338c8-131">МЕДИАСУБТИПЕ \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="338c8-131">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="338c8-132">Тип формата</span><span class="sxs-lookup"><span data-stu-id="338c8-132">Format Type</span></span>           | <span data-ttu-id="338c8-133">ФОРМАТ \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="338c8-133">FORMAT\_WaveFormatEx</span></span>                           |
| <span data-ttu-id="338c8-134">Структура формата</span><span class="sxs-lookup"><span data-stu-id="338c8-134">Format Structure</span></span>      | [<span data-ttu-id="338c8-135">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="338c8-135">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| <span data-ttu-id="338c8-136">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="338c8-136">Media Sample Contents</span></span> | <span data-ttu-id="338c8-137">Один пакет MPEG-1, включая заголовок пакета.</span><span class="sxs-lookup"><span data-stu-id="338c8-137">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-audio-payload"></a><span data-ttu-id="338c8-138">Полезные данные звука MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-138">MPEG-1 Audio Payload</span></span>



|                       |                                            |
|-----------------------|--------------------------------------------|
| <span data-ttu-id="338c8-139">Основной тип</span><span class="sxs-lookup"><span data-stu-id="338c8-139">Major type</span></span>            | <span data-ttu-id="338c8-140">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="338c8-140">MEDIATYPE\_Audio</span></span>                           |
| <span data-ttu-id="338c8-141">Subtype</span><span class="sxs-lookup"><span data-stu-id="338c8-141">Subtype</span></span>               | <span data-ttu-id="338c8-142">МЕДИАСУБТИПЕ \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="338c8-142">MEDIASUBTYPE\_MPEG1Payload</span></span>                 |
| <span data-ttu-id="338c8-143">Тип формата</span><span class="sxs-lookup"><span data-stu-id="338c8-143">Format Type</span></span>           | <span data-ttu-id="338c8-144">ФОРМАТ \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="338c8-144">FORMAT\_WaveFormatEx</span></span>                       |
| <span data-ttu-id="338c8-145">Структура формата</span><span class="sxs-lookup"><span data-stu-id="338c8-145">Format Structure</span></span>      | [<span data-ttu-id="338c8-146">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="338c8-146">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| <span data-ttu-id="338c8-147">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="338c8-147">Media Sample Contents</span></span> | <span data-ttu-id="338c8-148">Звуковые данные MPEG-1 с согласованием по байтам.</span><span class="sxs-lookup"><span data-stu-id="338c8-148">Byte-aligned MPEG-1 audio data.</span></span>            |



 

## <a name="mpeg-1-video-packet"></a><span data-ttu-id="338c8-149">Пакет видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-149">MPEG-1 Video Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="338c8-150">Основной тип</span><span class="sxs-lookup"><span data-stu-id="338c8-150">Major type</span></span>            | <span data-ttu-id="338c8-151">\_Видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="338c8-151">MEDIATYPE\_Video</span></span>                               |
| <span data-ttu-id="338c8-152">Subtype</span><span class="sxs-lookup"><span data-stu-id="338c8-152">Subtype</span></span>               | <span data-ttu-id="338c8-153">МЕДИАСУБТИПЕ \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="338c8-153">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="338c8-154">Тип формата</span><span class="sxs-lookup"><span data-stu-id="338c8-154">Format Type</span></span>           | <span data-ttu-id="338c8-155">ФОРМАТ \_ мпегвидео</span><span class="sxs-lookup"><span data-stu-id="338c8-155">FORMAT\_MPEGVideo</span></span>                              |
| <span data-ttu-id="338c8-156">Структура формата</span><span class="sxs-lookup"><span data-stu-id="338c8-156">Format Structure</span></span>      | [<span data-ttu-id="338c8-157">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="338c8-157">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| <span data-ttu-id="338c8-158">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="338c8-158">Media Sample Contents</span></span> | <span data-ttu-id="338c8-159">Один пакет MPEG-1, включая заголовок пакета.</span><span class="sxs-lookup"><span data-stu-id="338c8-159">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-video-payload"></a><span data-ttu-id="338c8-160">Полезные данные видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-160">MPEG-1 Video payload</span></span>



|                       |                                          |
|-----------------------|------------------------------------------|
| <span data-ttu-id="338c8-161">Основной тип</span><span class="sxs-lookup"><span data-stu-id="338c8-161">Major type</span></span>            | <span data-ttu-id="338c8-162">\_Видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="338c8-162">MEDIATYPE\_Video</span></span>                         |
| <span data-ttu-id="338c8-163">Subtype</span><span class="sxs-lookup"><span data-stu-id="338c8-163">Subtype</span></span>               | <span data-ttu-id="338c8-164">МЕДИАСУБТИПЕ \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="338c8-164">MEDIASUBTYPE\_MPEG1Payload</span></span>               |
| <span data-ttu-id="338c8-165">Тип формата</span><span class="sxs-lookup"><span data-stu-id="338c8-165">Format Type</span></span>           | <span data-ttu-id="338c8-166">ФОРМАТ \_ мпегвидео</span><span class="sxs-lookup"><span data-stu-id="338c8-166">FORMAT\_MPEGVideo</span></span>                        |
| <span data-ttu-id="338c8-167">Структура формата</span><span class="sxs-lookup"><span data-stu-id="338c8-167">Format Structure</span></span>      | [<span data-ttu-id="338c8-168">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="338c8-168">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| <span data-ttu-id="338c8-169">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="338c8-169">Media Sample Contents</span></span> | <span data-ttu-id="338c8-170">Данные видео в формате MPEG-1 с согласованием по байтам.</span><span class="sxs-lookup"><span data-stu-id="338c8-170">Byte-aligned MPEG-1 video data.</span></span>          |



 

## <a name="mpeg-1-native-video-stream"></a><span data-ttu-id="338c8-171">Собственный поток видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-171">MPEG-1 Native Video Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="338c8-172">Основной тип</span><span class="sxs-lookup"><span data-stu-id="338c8-172">Major type</span></span>            | <span data-ttu-id="338c8-173">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="338c8-173">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="338c8-174">Subtype</span><span class="sxs-lookup"><span data-stu-id="338c8-174">Subtype</span></span>               | <span data-ttu-id="338c8-175">МЕДИАСУБТИПЕ \_ MPEG1Video</span><span class="sxs-lookup"><span data-stu-id="338c8-175">MEDIASUBTYPE\_ MPEG1Video</span></span>                      |
| <span data-ttu-id="338c8-176">Тип формата</span><span class="sxs-lookup"><span data-stu-id="338c8-176">Format Type</span></span>           | <span data-ttu-id="338c8-177">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="338c8-177">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="338c8-178">Структура формата</span><span class="sxs-lookup"><span data-stu-id="338c8-178">Format Structure</span></span>      | <span data-ttu-id="338c8-179">Нет</span><span class="sxs-lookup"><span data-stu-id="338c8-179">None</span></span>                                           |
| <span data-ttu-id="338c8-180">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="338c8-180">Media Sample Contents</span></span> | <span data-ttu-id="338c8-181">Массив байтов видеопотока (без системного уровня).</span><span class="sxs-lookup"><span data-stu-id="338c8-181">Array of video stream bytes (no system layer).</span></span> |



 

## <a name="mpeg-1-native-audio-stream"></a><span data-ttu-id="338c8-182">Машинный поток MPEG-1 Native Audio</span><span class="sxs-lookup"><span data-stu-id="338c8-182">MPEG-1 Native Audio Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="338c8-183">Основной тип</span><span class="sxs-lookup"><span data-stu-id="338c8-183">Major type</span></span>            | <span data-ttu-id="338c8-184">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="338c8-184">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="338c8-185">Subtype</span><span class="sxs-lookup"><span data-stu-id="338c8-185">Subtype</span></span>               | <span data-ttu-id="338c8-186">МЕДИАСУБТИПЕ \_ MPEG1Audio</span><span class="sxs-lookup"><span data-stu-id="338c8-186">MEDIASUBTYPE\_ MPEG1Audio</span></span>                      |
| <span data-ttu-id="338c8-187">Тип формата</span><span class="sxs-lookup"><span data-stu-id="338c8-187">Format Type</span></span>           | <span data-ttu-id="338c8-188">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="338c8-188">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="338c8-189">Структура формата</span><span class="sxs-lookup"><span data-stu-id="338c8-189">Format Structure</span></span>      | <span data-ttu-id="338c8-190">Нет</span><span class="sxs-lookup"><span data-stu-id="338c8-190">None</span></span>                                           |
| <span data-ttu-id="338c8-191">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="338c8-191">Media Sample Contents</span></span> | <span data-ttu-id="338c8-192">Массив байтов звукового потока (без системного уровня).</span><span class="sxs-lookup"><span data-stu-id="338c8-192">Array of audio stream bytes (no system layer).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="338c8-193">Комментарии</span><span class="sxs-lookup"><span data-stu-id="338c8-193">Remarks</span></span>

<span data-ttu-id="338c8-194">Фильтры MPEG-1 для DirectShow поддерживают эти типы следующим образом.</span><span class="sxs-lookup"><span data-stu-id="338c8-194">The DirectShow MPEG-1 filters support these types as follows.</span></span>



| <span data-ttu-id="338c8-195">Фильтр</span><span class="sxs-lookup"><span data-stu-id="338c8-195">Filter</span></span>               | <span data-ttu-id="338c8-196">Направление</span><span class="sxs-lookup"><span data-stu-id="338c8-196">Direction</span></span> | <span data-ttu-id="338c8-197">Поддерживаемые типы носителей</span><span class="sxs-lookup"><span data-stu-id="338c8-197">Supported media types</span></span>                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="338c8-198">Разделитель MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-198">MPEG-1 Splitter</span></span>      | <span data-ttu-id="338c8-199">Входные данные</span><span class="sxs-lookup"><span data-stu-id="338c8-199">Input</span></span>     | <span data-ttu-id="338c8-200">Система MPEG-1 System Стреаммпег-1 системный поток с компакт-диска видео</span><span class="sxs-lookup"><span data-stu-id="338c8-200">MPEG-1 system streamMPEG-1 system stream from Video CD</span></span><br/>                                                 |
| <span data-ttu-id="338c8-201">Разделитель MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-201">MPEG-1 Splitter</span></span>      | <span data-ttu-id="338c8-202">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="338c8-202">Output</span></span>    | <span data-ttu-id="338c8-203">Звуковая полезная нагрузка MPEG-1 Audio Паккетмпег-1</span><span class="sxs-lookup"><span data-stu-id="338c8-203">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/> <span data-ttu-id="338c8-204">Пакет видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-204">MPEG-1 Video packet</span></span><br/> <span data-ttu-id="338c8-205">Полезные данные видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="338c8-205">MPEG-1 Video payload</span></span><br/> |
| <span data-ttu-id="338c8-206">Программный аудиокодек</span><span class="sxs-lookup"><span data-stu-id="338c8-206">Software Audio Codec</span></span> | <span data-ttu-id="338c8-207">Входные данные</span><span class="sxs-lookup"><span data-stu-id="338c8-207">Input</span></span>     | <span data-ttu-id="338c8-208">Звуковая полезная нагрузка MPEG-1 Audio Паккетмпег-1</span><span class="sxs-lookup"><span data-stu-id="338c8-208">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/>                                                                |
| <span data-ttu-id="338c8-209">Программный кодек для видео</span><span class="sxs-lookup"><span data-stu-id="338c8-209">Software Video Codec</span></span> | <span data-ttu-id="338c8-210">Входные данные</span><span class="sxs-lookup"><span data-stu-id="338c8-210">Input</span></span>     | <span data-ttu-id="338c8-211">Полезные данные видео MPEG-1 Video Паккетмпег-1</span><span class="sxs-lookup"><span data-stu-id="338c8-211">MPEG-1 Video packetMPEG-1 Video payload</span></span><br/>                                                                |
| <span data-ttu-id="338c8-212">Программный аудиокодек</span><span class="sxs-lookup"><span data-stu-id="338c8-212">Software Audio Codec</span></span> | <span data-ttu-id="338c8-213">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="338c8-213">Output</span></span>    | <span data-ttu-id="338c8-214">Звук PCM</span><span class="sxs-lookup"><span data-stu-id="338c8-214">PCM audio</span></span>                                                                                                         |
| <span data-ttu-id="338c8-215">Программный кодек для видео</span><span class="sxs-lookup"><span data-stu-id="338c8-215">Software Video Codec</span></span> | <span data-ttu-id="338c8-216">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="338c8-216">Output</span></span>    | <span data-ttu-id="338c8-217">Несжатое видео (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span><span class="sxs-lookup"><span data-stu-id="338c8-217">Uncompressed video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span></span>                                    |



 

<span data-ttu-id="338c8-218">Типы мультимедийных пакетов и полезных данных MPEG-1 содержат полный заголовок последовательности, чтобы данные можно было воспроизводить из середины файла без заголовка последовательности для инициализации воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="338c8-218">MPEG-1 Video packet and payload media types contain a complete sequence header so that data can be played from the middle of a file without needing a sequence header to initialize the video playback.</span></span>

<span data-ttu-id="338c8-219">Заголовок последовательности видео добавляется к типу данных видео для видео в формате MPEG, чтобы воспроизведение начиналось с середины потока.</span><span class="sxs-lookup"><span data-stu-id="338c8-219">The video sequence header is appended to the video data type for MPEG video so that play can begin from the middle of a stream.</span></span> <span data-ttu-id="338c8-220">Длина этого поля составляет до 140 байт; Он включает начальный код заголовка последовательности (0x000001B3) в начале, а также все матрицы дискретизация, обнаруженные в первой заголовке последовательности.</span><span class="sxs-lookup"><span data-stu-id="338c8-220">The length of this field is up to 140 bytes; it includes the sequence header start code (0x000001B3) at the start, along with any quantization matrices found in the first sequence header encountered.</span></span>

 

 




