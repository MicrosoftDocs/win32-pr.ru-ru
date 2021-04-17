---
description: Типы мультимедиа с разделителями MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Типы мультимедиа с разделителями MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684754"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="dccf7-103">Типы мультимедиа с разделителями MPEG-2</span><span class="sxs-lookup"><span data-stu-id="dccf7-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="dccf7-104">Фильтр [разделителя MPEG-2](mpeg-2-splitter.md) в настоящее время поддерживает аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="dccf7-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="dccf7-105">Dolby AC-3 поддерживается в виде подпотока, определенного DVD-диском.</span><span class="sxs-lookup"><span data-stu-id="dccf7-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="dccf7-106">Фильтр также поддерживает аудио MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="dccf7-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="dccf7-107">Типы мультимедиа зависят от того, доставляет ли разделитель MPEG-2 ПЕССИМИСТические пакеты или длительные полезные данные.</span><span class="sxs-lookup"><span data-stu-id="dccf7-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="dccf7-108">Видео</span><span class="sxs-lookup"><span data-stu-id="dccf7-108">Video</span></span>

<span data-ttu-id="dccf7-109">Для видео MPEG-2 используются следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="dccf7-109">For MPEG-2 video, the media types are as follows.</span></span>



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="dccf7-110">Вывод в формате экспорта</span><span class="sxs-lookup"><span data-stu-id="dccf7-110">PES output</span></span>                               | <span data-ttu-id="dccf7-111">Выходные данные полезных данных</span><span class="sxs-lookup"><span data-stu-id="dccf7-111">Payload output</span></span>                 |
| <span data-ttu-id="dccf7-112">Основной тип</span><span class="sxs-lookup"><span data-stu-id="dccf7-112">Major Type</span></span>       | <span data-ttu-id="dccf7-113">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="dccf7-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="dccf7-114">**\_Видео MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="dccf7-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="dccf7-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="dccf7-115">Subtype</span></span>          | <span data-ttu-id="dccf7-116">**\_Видео медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="dccf7-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="dccf7-117">**\_Видео медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="dccf7-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="dccf7-118">Тип формата</span><span class="sxs-lookup"><span data-stu-id="dccf7-118">Format Type</span></span>      | <span data-ttu-id="dccf7-119">**ФОРМАТ \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="dccf7-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="dccf7-120">**ФОРМАТ \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="dccf7-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="dccf7-121">Структура формата</span><span class="sxs-lookup"><span data-stu-id="dccf7-121">Format Structure</span></span> | [<span data-ttu-id="dccf7-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="dccf7-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="dccf7-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="dccf7-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="dccf7-124">Аудио AC-3</span><span class="sxs-lookup"><span data-stu-id="dccf7-124">AC-3 Audio</span></span>

<span data-ttu-id="dccf7-125">Для звука AC-3 используются следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="dccf7-125">For AC-3 audio, the media types are as follows.</span></span>



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="dccf7-126">Вывод в формате экспорта</span><span class="sxs-lookup"><span data-stu-id="dccf7-126">PES output</span></span>                           | <span data-ttu-id="dccf7-127">Выходные данные полезных данных</span><span class="sxs-lookup"><span data-stu-id="dccf7-127">Payload output</span></span>               |
| <span data-ttu-id="dccf7-128">Основной тип</span><span class="sxs-lookup"><span data-stu-id="dccf7-128">Major Type</span></span>       | <span data-ttu-id="dccf7-129">MEDIATYPE \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="dccf7-129">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="dccf7-130">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="dccf7-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="dccf7-131">Subtype</span><span class="sxs-lookup"><span data-stu-id="dccf7-131">Subtype</span></span>          | <span data-ttu-id="dccf7-132">МЕДИАСУБТИПЕ \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="dccf7-132">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="dccf7-133">**МЕДИАСУБТИПЕ \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="dccf7-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="dccf7-134">Тип формата</span><span class="sxs-lookup"><span data-stu-id="dccf7-134">Format Type</span></span>      | <span data-ttu-id="dccf7-135">ФОРМАТ \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="dccf7-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="dccf7-136">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="dccf7-137">Структура формата</span><span class="sxs-lookup"><span data-stu-id="dccf7-137">Format Structure</span></span> | <span data-ttu-id="dccf7-138">[**вавеформатекс**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dccf7-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="dccf7-139">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="dccf7-140">Элемент **вформаттаг** структуры **вавеформатекс** для AC-3 в настоящее время имеет **\_ \_ неизвестный формат Wave**, но может измениться.</span><span class="sxs-lookup"><span data-stu-id="dccf7-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="dccf7-141">Звук MPEG-2</span><span class="sxs-lookup"><span data-stu-id="dccf7-141">MPEG-2 Audio</span></span>

<span data-ttu-id="dccf7-142">Для аудио MPEG-2 используются следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="dccf7-142">For MPEG-2 audio, the media types are as follows.</span></span>



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="dccf7-143">Вывод в формате экспорта</span><span class="sxs-lookup"><span data-stu-id="dccf7-143">PES output</span></span>                    | <span data-ttu-id="dccf7-144">Выходные данные полезных данных</span><span class="sxs-lookup"><span data-stu-id="dccf7-144">Payload output</span></span>                 |
| <span data-ttu-id="dccf7-145">Основной тип</span><span class="sxs-lookup"><span data-stu-id="dccf7-145">Major Type</span></span>       | <span data-ttu-id="dccf7-146">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="dccf7-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="dccf7-147">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="dccf7-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="dccf7-148">Subtype</span><span class="sxs-lookup"><span data-stu-id="dccf7-148">Subtype</span></span>          | <span data-ttu-id="dccf7-149">**МЕДИАСУБТЕ \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="dccf7-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="dccf7-150">**МЕДИАСУБТИПЕ \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="dccf7-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="dccf7-151">Тип формата</span><span class="sxs-lookup"><span data-stu-id="dccf7-151">Format Type</span></span>      | <span data-ttu-id="dccf7-152">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="dccf7-153">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="dccf7-154">Структура формата</span><span class="sxs-lookup"><span data-stu-id="dccf7-154">Format Structure</span></span> | <span data-ttu-id="dccf7-155">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="dccf7-156">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="dccf7-157">Элемент **вформаттаг** структуры **вавеформатекс** для звукового файла MPEG-2 в настоящее **время \_ \_ неизвестен**, но может измениться.</span><span class="sxs-lookup"><span data-stu-id="dccf7-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="dccf7-158">Разделитель MPEG-2 предполагает, что для потока многоканального расширения используются потоки от D0 до DF, так как они предназначены для аудио DVD MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="dccf7-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="dccf7-159">Таким образом, каждый раз, когда выбран поток C *x* , разделитель перенаправляет пакеты для Stream D *x* .</span><span class="sxs-lookup"><span data-stu-id="dccf7-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="dccf7-160">ЛПКМ аудио</span><span class="sxs-lookup"><span data-stu-id="dccf7-160">LPCM Audio</span></span>

<span data-ttu-id="dccf7-161">Для ЛПКМ Audio используются следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="dccf7-161">For LPCM audio, the media types are as follows.</span></span>



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="dccf7-162">Вывод в формате экспорта</span><span class="sxs-lookup"><span data-stu-id="dccf7-162">PES output</span></span>                         | <span data-ttu-id="dccf7-163">Выходные данные полезных данных</span><span class="sxs-lookup"><span data-stu-id="dccf7-163">Payload output</span></span>                     |
| <span data-ttu-id="dccf7-164">Основной тип</span><span class="sxs-lookup"><span data-stu-id="dccf7-164">Major Type</span></span>       | <span data-ttu-id="dccf7-165">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="dccf7-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="dccf7-166">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="dccf7-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="dccf7-167">Subtype</span><span class="sxs-lookup"><span data-stu-id="dccf7-167">Subtype</span></span>          | <span data-ttu-id="dccf7-168">**МЕДИАСУБТИПЕ \_ DVD \_ лпкм \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="dccf7-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="dccf7-169">**МЕДИАСУБТИПЕ \_ DVD \_ лпкм \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="dccf7-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="dccf7-170">Тип формата</span><span class="sxs-lookup"><span data-stu-id="dccf7-170">Format Type</span></span>      | <span data-ttu-id="dccf7-171">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="dccf7-172">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="dccf7-173">Структура формата</span><span class="sxs-lookup"><span data-stu-id="dccf7-173">Format Structure</span></span> | <span data-ttu-id="dccf7-174">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="dccf7-175">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="dccf7-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="dccf7-176">Элемент **вформаттаг** структуры **вавеформатекс** для лпкм Audio в настоящее время имеет **\_ \_ неизвестный формат Wave**, но может измениться.</span><span class="sxs-lookup"><span data-stu-id="dccf7-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dccf7-177">См. также</span><span class="sxs-lookup"><span data-stu-id="dccf7-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dccf7-178">Типы мультимедиа MPEG-2</span><span class="sxs-lookup"><span data-stu-id="dccf7-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
