---
description: В этом разделе перечислены типы носителей, используемые для данных MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Типы мультимедиа MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e44db1f4423365efb7814d61b35c1985142aa14
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910032"
---
# <a name="mpeg-1-media-types"></a><span data-ttu-id="b3190-103">Типы мультимедиа MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-103">MPEG-1 Media Types</span></span>

<span data-ttu-id="b3190-104">В этом разделе перечислены типы носителей, используемые для данных MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="b3190-104">This section lists the media types used for MPEG-1 data.</span></span>

## <a name="mpeg-1-system-stream"></a><span data-ttu-id="b3190-105">Системный поток MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-105">MPEG-1 System Stream</span></span>



| <span data-ttu-id="b3190-106">Метка</span><span class="sxs-lookup"><span data-stu-id="b3190-106">Label</span></span> | <span data-ttu-id="b3190-107">Значение</span><span class="sxs-lookup"><span data-stu-id="b3190-107">Value</span></span> |
|-----------------------|-------------------------------------------------|
| <span data-ttu-id="b3190-108">Основной тип</span><span class="sxs-lookup"><span data-stu-id="b3190-108">Major type</span></span>            | <span data-ttu-id="b3190-109">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="b3190-109">MEDIATYPE\_Stream</span></span>                               |
| <span data-ttu-id="b3190-110">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3190-110">Subtype</span></span>               | <span data-ttu-id="b3190-111">МЕДИАСУБТИПЕ \_ MPEG1System</span><span class="sxs-lookup"><span data-stu-id="b3190-111">MEDIASUBTYPE\_MPEG1System</span></span>                       |
| <span data-ttu-id="b3190-112">Тип формата</span><span class="sxs-lookup"><span data-stu-id="b3190-112">Format Type</span></span>           | <span data-ttu-id="b3190-113">ФОРМАТ \_ мпегстреамс</span><span class="sxs-lookup"><span data-stu-id="b3190-113">FORMAT\_MPEGStreams</span></span>                             |
| <span data-ttu-id="b3190-114">Структура формата</span><span class="sxs-lookup"><span data-stu-id="b3190-114">Format Structure</span></span>      | [<span data-ttu-id="b3190-115">**\_мпегсистемтипе**</span><span class="sxs-lookup"><span data-stu-id="b3190-115">**AM\_MPEGSYSTEMTYPE**</span></span>](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| <span data-ttu-id="b3190-116">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="b3190-116">Media Sample Contents</span></span> | <span data-ttu-id="b3190-117">Байтовый поток; без выравнивания</span><span class="sxs-lookup"><span data-stu-id="b3190-117">Byte stream; no alignment</span></span>                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a><span data-ttu-id="b3190-118">Системный поток MPEG-1 с компакт-диска видео</span><span class="sxs-lookup"><span data-stu-id="b3190-118">MPEG-1 System Stream from Video CD</span></span>



| <span data-ttu-id="b3190-119">Метка</span><span class="sxs-lookup"><span data-stu-id="b3190-119">Label</span></span> | <span data-ttu-id="b3190-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b3190-120">Value</span></span> |
|-----------------------|----------------------------|
| <span data-ttu-id="b3190-121">Основной тип</span><span class="sxs-lookup"><span data-stu-id="b3190-121">Major type</span></span>            | <span data-ttu-id="b3190-122">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="b3190-122">MEDIATYPE\_Stream</span></span>          |
| <span data-ttu-id="b3190-123">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3190-123">Subtype</span></span>               | <span data-ttu-id="b3190-124">МЕДИАСУБТИПЕ \_ MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="b3190-124">MEDIASUBTYPE\_MPEG1VideoCD</span></span> |
| <span data-ttu-id="b3190-125">Тип формата</span><span class="sxs-lookup"><span data-stu-id="b3190-125">Format Type</span></span>           | <span data-ttu-id="b3190-126">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="b3190-126">GUID\_NULL</span></span>                 |
| <span data-ttu-id="b3190-127">Структура формата</span><span class="sxs-lookup"><span data-stu-id="b3190-127">Format Structure</span></span>      | <span data-ttu-id="b3190-128">None</span><span class="sxs-lookup"><span data-stu-id="b3190-128">None</span></span>                       |
| <span data-ttu-id="b3190-129">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="b3190-129">Media Sample Contents</span></span> | <span data-ttu-id="b3190-130">Байтовый поток; без выравнивания.</span><span class="sxs-lookup"><span data-stu-id="b3190-130">Byte stream; no alignment.</span></span> |



 

## <a name="mpeg-1-audio-packet"></a><span data-ttu-id="b3190-131">Звуковой пакет MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-131">MPEG-1 Audio Packet</span></span>



| <span data-ttu-id="b3190-132">Метка</span><span class="sxs-lookup"><span data-stu-id="b3190-132">Label</span></span> | <span data-ttu-id="b3190-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b3190-133">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="b3190-134">Основной тип</span><span class="sxs-lookup"><span data-stu-id="b3190-134">Major type</span></span>            | <span data-ttu-id="b3190-135">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="b3190-135">MEDIATYPE\_Audio</span></span>                               |
| <span data-ttu-id="b3190-136">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3190-136">Subtype</span></span>               | <span data-ttu-id="b3190-137">МЕДИАСУБТИПЕ \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="b3190-137">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="b3190-138">Тип формата</span><span class="sxs-lookup"><span data-stu-id="b3190-138">Format Type</span></span>           | <span data-ttu-id="b3190-139">ФОРМАТ \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="b3190-139">FORMAT\_WaveFormatEx</span></span>                           |
| <span data-ttu-id="b3190-140">Структура формата</span><span class="sxs-lookup"><span data-stu-id="b3190-140">Format Structure</span></span>      | [<span data-ttu-id="b3190-141">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="b3190-141">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| <span data-ttu-id="b3190-142">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="b3190-142">Media Sample Contents</span></span> | <span data-ttu-id="b3190-143">Один пакет MPEG-1, включая заголовок пакета.</span><span class="sxs-lookup"><span data-stu-id="b3190-143">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-audio-payload"></a><span data-ttu-id="b3190-144">Полезные данные звука MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-144">MPEG-1 Audio Payload</span></span>



| <span data-ttu-id="b3190-145">Метка</span><span class="sxs-lookup"><span data-stu-id="b3190-145">Label</span></span> | <span data-ttu-id="b3190-146">Значение</span><span class="sxs-lookup"><span data-stu-id="b3190-146">Value</span></span> |
|-----------------------|--------------------------------------------|
| <span data-ttu-id="b3190-147">Основной тип</span><span class="sxs-lookup"><span data-stu-id="b3190-147">Major type</span></span>            | <span data-ttu-id="b3190-148">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="b3190-148">MEDIATYPE\_Audio</span></span>                           |
| <span data-ttu-id="b3190-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3190-149">Subtype</span></span>               | <span data-ttu-id="b3190-150">МЕДИАСУБТИПЕ \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="b3190-150">MEDIASUBTYPE\_MPEG1Payload</span></span>                 |
| <span data-ttu-id="b3190-151">Тип формата</span><span class="sxs-lookup"><span data-stu-id="b3190-151">Format Type</span></span>           | <span data-ttu-id="b3190-152">ФОРМАТ \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="b3190-152">FORMAT\_WaveFormatEx</span></span>                       |
| <span data-ttu-id="b3190-153">Структура формата</span><span class="sxs-lookup"><span data-stu-id="b3190-153">Format Structure</span></span>      | [<span data-ttu-id="b3190-154">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="b3190-154">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| <span data-ttu-id="b3190-155">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="b3190-155">Media Sample Contents</span></span> | <span data-ttu-id="b3190-156">Звуковые данные MPEG-1 с согласованием по байтам.</span><span class="sxs-lookup"><span data-stu-id="b3190-156">Byte-aligned MPEG-1 audio data.</span></span>            |



 

## <a name="mpeg-1-video-packet"></a><span data-ttu-id="b3190-157">Пакет видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-157">MPEG-1 Video Packet</span></span>



| <span data-ttu-id="b3190-158">Метка</span><span class="sxs-lookup"><span data-stu-id="b3190-158">Label</span></span> | <span data-ttu-id="b3190-159">Значение</span><span class="sxs-lookup"><span data-stu-id="b3190-159">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="b3190-160">Основной тип</span><span class="sxs-lookup"><span data-stu-id="b3190-160">Major type</span></span>            | <span data-ttu-id="b3190-161">\_Видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="b3190-161">MEDIATYPE\_Video</span></span>                               |
| <span data-ttu-id="b3190-162">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3190-162">Subtype</span></span>               | <span data-ttu-id="b3190-163">МЕДИАСУБТИПЕ \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="b3190-163">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="b3190-164">Тип формата</span><span class="sxs-lookup"><span data-stu-id="b3190-164">Format Type</span></span>           | <span data-ttu-id="b3190-165">ФОРМАТ \_ мпегвидео</span><span class="sxs-lookup"><span data-stu-id="b3190-165">FORMAT\_MPEGVideo</span></span>                              |
| <span data-ttu-id="b3190-166">Структура формата</span><span class="sxs-lookup"><span data-stu-id="b3190-166">Format Structure</span></span>      | [<span data-ttu-id="b3190-167">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="b3190-167">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| <span data-ttu-id="b3190-168">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="b3190-168">Media Sample Contents</span></span> | <span data-ttu-id="b3190-169">Один пакет MPEG-1, включая заголовок пакета.</span><span class="sxs-lookup"><span data-stu-id="b3190-169">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-video-payload"></a><span data-ttu-id="b3190-170">Полезные данные видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-170">MPEG-1 Video payload</span></span>



| <span data-ttu-id="b3190-171">Метка</span><span class="sxs-lookup"><span data-stu-id="b3190-171">Label</span></span> | <span data-ttu-id="b3190-172">Значение</span><span class="sxs-lookup"><span data-stu-id="b3190-172">Value</span></span> |
|-----------------------|------------------------------------------|
| <span data-ttu-id="b3190-173">Основной тип</span><span class="sxs-lookup"><span data-stu-id="b3190-173">Major type</span></span>            | <span data-ttu-id="b3190-174">\_Видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="b3190-174">MEDIATYPE\_Video</span></span>                         |
| <span data-ttu-id="b3190-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3190-175">Subtype</span></span>               | <span data-ttu-id="b3190-176">МЕДИАСУБТИПЕ \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="b3190-176">MEDIASUBTYPE\_MPEG1Payload</span></span>               |
| <span data-ttu-id="b3190-177">Тип формата</span><span class="sxs-lookup"><span data-stu-id="b3190-177">Format Type</span></span>           | <span data-ttu-id="b3190-178">ФОРМАТ \_ мпегвидео</span><span class="sxs-lookup"><span data-stu-id="b3190-178">FORMAT\_MPEGVideo</span></span>                        |
| <span data-ttu-id="b3190-179">Структура формата</span><span class="sxs-lookup"><span data-stu-id="b3190-179">Format Structure</span></span>      | [<span data-ttu-id="b3190-180">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="b3190-180">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| <span data-ttu-id="b3190-181">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="b3190-181">Media Sample Contents</span></span> | <span data-ttu-id="b3190-182">Данные видео в формате MPEG-1 с согласованием по байтам.</span><span class="sxs-lookup"><span data-stu-id="b3190-182">Byte-aligned MPEG-1 video data.</span></span>          |



 

## <a name="mpeg-1-native-video-stream"></a><span data-ttu-id="b3190-183">Собственный поток видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-183">MPEG-1 Native Video Stream</span></span>



| <span data-ttu-id="b3190-184">Метка</span><span class="sxs-lookup"><span data-stu-id="b3190-184">Label</span></span> | <span data-ttu-id="b3190-185">Значение</span><span class="sxs-lookup"><span data-stu-id="b3190-185">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="b3190-186">Основной тип</span><span class="sxs-lookup"><span data-stu-id="b3190-186">Major type</span></span>            | <span data-ttu-id="b3190-187">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="b3190-187">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="b3190-188">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3190-188">Subtype</span></span>               | <span data-ttu-id="b3190-189">МЕДИАСУБТИПЕ \_ MPEG1Video</span><span class="sxs-lookup"><span data-stu-id="b3190-189">MEDIASUBTYPE\_ MPEG1Video</span></span>                      |
| <span data-ttu-id="b3190-190">Тип формата</span><span class="sxs-lookup"><span data-stu-id="b3190-190">Format Type</span></span>           | <span data-ttu-id="b3190-191">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="b3190-191">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="b3190-192">Структура формата</span><span class="sxs-lookup"><span data-stu-id="b3190-192">Format Structure</span></span>      | <span data-ttu-id="b3190-193">None</span><span class="sxs-lookup"><span data-stu-id="b3190-193">None</span></span>                                           |
| <span data-ttu-id="b3190-194">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="b3190-194">Media Sample Contents</span></span> | <span data-ttu-id="b3190-195">Массив байтов видеопотока (без системного уровня).</span><span class="sxs-lookup"><span data-stu-id="b3190-195">Array of video stream bytes (no system layer).</span></span> |



 

## <a name="mpeg-1-native-audio-stream"></a><span data-ttu-id="b3190-196">Машинный поток MPEG-1 Native Audio</span><span class="sxs-lookup"><span data-stu-id="b3190-196">MPEG-1 Native Audio Stream</span></span>



| <span data-ttu-id="b3190-197">Метка</span><span class="sxs-lookup"><span data-stu-id="b3190-197">Label</span></span> | <span data-ttu-id="b3190-198">Значение</span><span class="sxs-lookup"><span data-stu-id="b3190-198">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="b3190-199">Основной тип</span><span class="sxs-lookup"><span data-stu-id="b3190-199">Major type</span></span>            | <span data-ttu-id="b3190-200">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="b3190-200">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="b3190-201">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3190-201">Subtype</span></span>               | <span data-ttu-id="b3190-202">МЕДИАСУБТИПЕ \_ MPEG1Audio</span><span class="sxs-lookup"><span data-stu-id="b3190-202">MEDIASUBTYPE\_ MPEG1Audio</span></span>                      |
| <span data-ttu-id="b3190-203">Тип формата</span><span class="sxs-lookup"><span data-stu-id="b3190-203">Format Type</span></span>           | <span data-ttu-id="b3190-204">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="b3190-204">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="b3190-205">Структура формата</span><span class="sxs-lookup"><span data-stu-id="b3190-205">Format Structure</span></span>      | <span data-ttu-id="b3190-206">None</span><span class="sxs-lookup"><span data-stu-id="b3190-206">None</span></span>                                           |
| <span data-ttu-id="b3190-207">Пример содержимого носителя</span><span class="sxs-lookup"><span data-stu-id="b3190-207">Media Sample Contents</span></span> | <span data-ttu-id="b3190-208">Массив байтов звукового потока (без системного уровня).</span><span class="sxs-lookup"><span data-stu-id="b3190-208">Array of audio stream bytes (no system layer).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b3190-209">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3190-209">Remarks</span></span>

<span data-ttu-id="b3190-210">Фильтры MPEG-1 для DirectShow поддерживают эти типы следующим образом.</span><span class="sxs-lookup"><span data-stu-id="b3190-210">The DirectShow MPEG-1 filters support these types as follows.</span></span>



| <span data-ttu-id="b3190-211">Фильтр</span><span class="sxs-lookup"><span data-stu-id="b3190-211">Filter</span></span>               | <span data-ttu-id="b3190-212">Направление</span><span class="sxs-lookup"><span data-stu-id="b3190-212">Direction</span></span> | <span data-ttu-id="b3190-213">Поддерживаемые типы носителей</span><span class="sxs-lookup"><span data-stu-id="b3190-213">Supported media types</span></span>                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3190-214">Разделитель MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-214">MPEG-1 Splitter</span></span>      | <span data-ttu-id="b3190-215">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b3190-215">Input</span></span>     | <span data-ttu-id="b3190-216">Система MPEG-1 System Стреаммпег-1 системный поток с компакт-диска видео</span><span class="sxs-lookup"><span data-stu-id="b3190-216">MPEG-1 system streamMPEG-1 system stream from Video CD</span></span><br/>                                                 |
| <span data-ttu-id="b3190-217">Разделитель MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-217">MPEG-1 Splitter</span></span>      | <span data-ttu-id="b3190-218">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="b3190-218">Output</span></span>    | <span data-ttu-id="b3190-219">Звуковая полезная нагрузка MPEG-1 Audio Паккетмпег-1</span><span class="sxs-lookup"><span data-stu-id="b3190-219">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/> <span data-ttu-id="b3190-220">Пакет видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-220">MPEG-1 Video packet</span></span><br/> <span data-ttu-id="b3190-221">Полезные данные видео MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b3190-221">MPEG-1 Video payload</span></span><br/> |
| <span data-ttu-id="b3190-222">Программный аудиокодек</span><span class="sxs-lookup"><span data-stu-id="b3190-222">Software Audio Codec</span></span> | <span data-ttu-id="b3190-223">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b3190-223">Input</span></span>     | <span data-ttu-id="b3190-224">Звуковая полезная нагрузка MPEG-1 Audio Паккетмпег-1</span><span class="sxs-lookup"><span data-stu-id="b3190-224">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/>                                                                |
| <span data-ttu-id="b3190-225">Программный кодек для видео</span><span class="sxs-lookup"><span data-stu-id="b3190-225">Software Video Codec</span></span> | <span data-ttu-id="b3190-226">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b3190-226">Input</span></span>     | <span data-ttu-id="b3190-227">Полезные данные видео MPEG-1 Video Паккетмпег-1</span><span class="sxs-lookup"><span data-stu-id="b3190-227">MPEG-1 Video packetMPEG-1 Video payload</span></span><br/>                                                                |
| <span data-ttu-id="b3190-228">Программный аудиокодек</span><span class="sxs-lookup"><span data-stu-id="b3190-228">Software Audio Codec</span></span> | <span data-ttu-id="b3190-229">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="b3190-229">Output</span></span>    | <span data-ttu-id="b3190-230">Звук PCM</span><span class="sxs-lookup"><span data-stu-id="b3190-230">PCM audio</span></span>                                                                                                         |
| <span data-ttu-id="b3190-231">Программный кодек для видео</span><span class="sxs-lookup"><span data-stu-id="b3190-231">Software Video Codec</span></span> | <span data-ttu-id="b3190-232">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="b3190-232">Output</span></span>    | <span data-ttu-id="b3190-233">Несжатое видео (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span><span class="sxs-lookup"><span data-stu-id="b3190-233">Uncompressed video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span></span>                                    |



 

<span data-ttu-id="b3190-234">Типы мультимедийных пакетов и полезных данных MPEG-1 содержат полный заголовок последовательности, чтобы данные можно было воспроизводить из середины файла без заголовка последовательности для инициализации воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="b3190-234">MPEG-1 Video packet and payload media types contain a complete sequence header so that data can be played from the middle of a file without needing a sequence header to initialize the video playback.</span></span>

<span data-ttu-id="b3190-235">Заголовок последовательности видео добавляется к типу данных видео для видео в формате MPEG, чтобы воспроизведение начиналось с середины потока.</span><span class="sxs-lookup"><span data-stu-id="b3190-235">The video sequence header is appended to the video data type for MPEG video so that play can begin from the middle of a stream.</span></span> <span data-ttu-id="b3190-236">Длина этого поля составляет до 140 байт; Он включает начальный код заголовка последовательности (0x000001B3) в начале, а также все матрицы дискретизация, обнаруженные в первой заголовке последовательности.</span><span class="sxs-lookup"><span data-stu-id="b3190-236">The length of this field is up to 140 bytes; it includes the sequence header start code (0x000001B3) at the start, along with any quantization matrices found in the first sequence header encountered.</span></span>

 

 




