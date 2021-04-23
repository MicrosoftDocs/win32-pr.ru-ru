---
description: Типы мультимедиа с разделителями MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Типы мультимедиа с разделителями MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e878acaea8bc87bee2bf5c46a6f7e66c7aa0a485
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909431"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="d21ac-103">Типы мультимедиа с разделителями MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d21ac-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="d21ac-104">Фильтр [разделителя MPEG-2](mpeg-2-splitter.md) в настоящее время поддерживает аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="d21ac-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="d21ac-105">Dolby AC-3 поддерживается в виде подпотока, определенного DVD-диском.</span><span class="sxs-lookup"><span data-stu-id="d21ac-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="d21ac-106">Фильтр также поддерживает аудио MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="d21ac-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="d21ac-107">Типы мультимедиа зависят от того, доставляет ли разделитель MPEG-2 ПЕССИМИСТические пакеты или длительные полезные данные.</span><span class="sxs-lookup"><span data-stu-id="d21ac-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="d21ac-108">Видеоролик</span><span class="sxs-lookup"><span data-stu-id="d21ac-108">Video</span></span>

<span data-ttu-id="d21ac-109">Для видео MPEG-2 используются следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="d21ac-109">For MPEG-2 video, the media types are as follows.</span></span>



| <span data-ttu-id="d21ac-110">Метка</span><span class="sxs-lookup"><span data-stu-id="d21ac-110">Label</span></span> | <span data-ttu-id="d21ac-111">Значение</span><span class="sxs-lookup"><span data-stu-id="d21ac-111">Value</span></span> |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="d21ac-112">Вывод в формате экспорта</span><span class="sxs-lookup"><span data-stu-id="d21ac-112">PES output</span></span>                               | <span data-ttu-id="d21ac-113">Выходные данные полезных данных</span><span class="sxs-lookup"><span data-stu-id="d21ac-113">Payload output</span></span>                 |
| <span data-ttu-id="d21ac-114">Основной тип</span><span class="sxs-lookup"><span data-stu-id="d21ac-114">Major Type</span></span>       | <span data-ttu-id="d21ac-115">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="d21ac-115">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="d21ac-116">**\_Видео MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="d21ac-116">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="d21ac-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="d21ac-117">Subtype</span></span>          | <span data-ttu-id="d21ac-118">**\_Видео медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="d21ac-118">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="d21ac-119">**\_Видео медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="d21ac-119">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="d21ac-120">Тип формата</span><span class="sxs-lookup"><span data-stu-id="d21ac-120">Format Type</span></span>      | <span data-ttu-id="d21ac-121">**ФОРМАТ \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="d21ac-121">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="d21ac-122">**ФОРМАТ \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="d21ac-122">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="d21ac-123">Структура формата</span><span class="sxs-lookup"><span data-stu-id="d21ac-123">Format Structure</span></span> | [<span data-ttu-id="d21ac-124">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="d21ac-124">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="d21ac-125">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="d21ac-125">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="d21ac-126">Аудио AC-3</span><span class="sxs-lookup"><span data-stu-id="d21ac-126">AC-3 Audio</span></span>

<span data-ttu-id="d21ac-127">Для звука AC-3 используются следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="d21ac-127">For AC-3 audio, the media types are as follows.</span></span>



| <span data-ttu-id="d21ac-128">Метка</span><span class="sxs-lookup"><span data-stu-id="d21ac-128">Label</span></span> | <span data-ttu-id="d21ac-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d21ac-129">Value</span></span> |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="d21ac-130">Вывод в формате экспорта</span><span class="sxs-lookup"><span data-stu-id="d21ac-130">PES output</span></span>                           | <span data-ttu-id="d21ac-131">Выходные данные полезных данных</span><span class="sxs-lookup"><span data-stu-id="d21ac-131">Payload output</span></span>               |
| <span data-ttu-id="d21ac-132">Основной тип</span><span class="sxs-lookup"><span data-stu-id="d21ac-132">Major Type</span></span>       | <span data-ttu-id="d21ac-133">MEDIATYPE \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="d21ac-133">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="d21ac-134">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d21ac-134">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="d21ac-135">Subtype</span><span class="sxs-lookup"><span data-stu-id="d21ac-135">Subtype</span></span>          | <span data-ttu-id="d21ac-136">МЕДИАСУБТИПЕ \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="d21ac-136">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="d21ac-137">**МЕДИАСУБТИПЕ \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="d21ac-137">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="d21ac-138">Тип формата</span><span class="sxs-lookup"><span data-stu-id="d21ac-138">Format Type</span></span>      | <span data-ttu-id="d21ac-139">ФОРМАТ \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="d21ac-139">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="d21ac-140">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-140">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="d21ac-141">Структура формата</span><span class="sxs-lookup"><span data-stu-id="d21ac-141">Format Structure</span></span> | <span data-ttu-id="d21ac-142">[**вавеформатекс**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d21ac-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="d21ac-143">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-143">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="d21ac-144">Элемент **вформаттаг** структуры **вавеформатекс** для AC-3 в настоящее время имеет **\_ \_ неизвестный формат Wave**, но может измениться.</span><span class="sxs-lookup"><span data-stu-id="d21ac-144">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="d21ac-145">Звук MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d21ac-145">MPEG-2 Audio</span></span>

<span data-ttu-id="d21ac-146">Для аудио MPEG-2 используются следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="d21ac-146">For MPEG-2 audio, the media types are as follows.</span></span>



| <span data-ttu-id="d21ac-147">Метка</span><span class="sxs-lookup"><span data-stu-id="d21ac-147">Label</span></span> | <span data-ttu-id="d21ac-148">Значение</span><span class="sxs-lookup"><span data-stu-id="d21ac-148">Value</span></span> |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="d21ac-149">Вывод в формате экспорта</span><span class="sxs-lookup"><span data-stu-id="d21ac-149">PES output</span></span>                    | <span data-ttu-id="d21ac-150">Выходные данные полезных данных</span><span class="sxs-lookup"><span data-stu-id="d21ac-150">Payload output</span></span>                 |
| <span data-ttu-id="d21ac-151">Основной тип</span><span class="sxs-lookup"><span data-stu-id="d21ac-151">Major Type</span></span>       | <span data-ttu-id="d21ac-152">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="d21ac-152">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="d21ac-153">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d21ac-153">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="d21ac-154">Subtype</span><span class="sxs-lookup"><span data-stu-id="d21ac-154">Subtype</span></span>          | <span data-ttu-id="d21ac-155">**МЕДИАСУБТЕ \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d21ac-155">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="d21ac-156">**МЕДИАСУБТИПЕ \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d21ac-156">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="d21ac-157">Тип формата</span><span class="sxs-lookup"><span data-stu-id="d21ac-157">Format Type</span></span>      | <span data-ttu-id="d21ac-158">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-158">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="d21ac-159">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-159">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="d21ac-160">Структура формата</span><span class="sxs-lookup"><span data-stu-id="d21ac-160">Format Structure</span></span> | <span data-ttu-id="d21ac-161">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-161">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="d21ac-162">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-162">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="d21ac-163">Элемент **вформаттаг** структуры **вавеформатекс** для звукового файла MPEG-2 в настоящее **время \_ \_ неизвестен**, но может измениться.</span><span class="sxs-lookup"><span data-stu-id="d21ac-163">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="d21ac-164">Разделитель MPEG-2 предполагает, что для потока многоканального расширения используются потоки от D0 до DF, так как они предназначены для аудио DVD MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="d21ac-164">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="d21ac-165">Таким образом, каждый раз, когда выбран поток C *x* , разделитель перенаправляет пакеты для Stream D *x* .</span><span class="sxs-lookup"><span data-stu-id="d21ac-165">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="d21ac-166">ЛПКМ аудио</span><span class="sxs-lookup"><span data-stu-id="d21ac-166">LPCM Audio</span></span>

<span data-ttu-id="d21ac-167">Для ЛПКМ Audio используются следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="d21ac-167">For LPCM audio, the media types are as follows.</span></span>



| <span data-ttu-id="d21ac-168">Метка</span><span class="sxs-lookup"><span data-stu-id="d21ac-168">Label</span></span> | <span data-ttu-id="d21ac-169">Значение</span><span class="sxs-lookup"><span data-stu-id="d21ac-169">Value</span></span> |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="d21ac-170">Вывод в формате экспорта</span><span class="sxs-lookup"><span data-stu-id="d21ac-170">PES output</span></span>                         | <span data-ttu-id="d21ac-171">Выходные данные полезных данных</span><span class="sxs-lookup"><span data-stu-id="d21ac-171">Payload output</span></span>                     |
| <span data-ttu-id="d21ac-172">Основной тип</span><span class="sxs-lookup"><span data-stu-id="d21ac-172">Major Type</span></span>       | <span data-ttu-id="d21ac-173">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="d21ac-173">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="d21ac-174">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d21ac-174">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="d21ac-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="d21ac-175">Subtype</span></span>          | <span data-ttu-id="d21ac-176">**МЕДИАСУБТИПЕ \_ DVD \_ лпкм \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d21ac-176">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="d21ac-177">**МЕДИАСУБТИПЕ \_ DVD \_ лпкм \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d21ac-177">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="d21ac-178">Тип формата</span><span class="sxs-lookup"><span data-stu-id="d21ac-178">Format Type</span></span>      | <span data-ttu-id="d21ac-179">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-179">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="d21ac-180">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-180">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="d21ac-181">Структура формата</span><span class="sxs-lookup"><span data-stu-id="d21ac-181">Format Structure</span></span> | <span data-ttu-id="d21ac-182">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-182">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="d21ac-183">**вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="d21ac-183">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="d21ac-184">Элемент **вформаттаг** структуры **вавеформатекс** для лпкм Audio в настоящее время имеет **\_ \_ неизвестный формат Wave**, но может измениться.</span><span class="sxs-lookup"><span data-stu-id="d21ac-184">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d21ac-185">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d21ac-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d21ac-186">Типы мультимедиа MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d21ac-186">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
