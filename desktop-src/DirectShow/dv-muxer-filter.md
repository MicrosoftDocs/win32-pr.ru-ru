---
description: Фильтр DV мультиплексор
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Фильтр DV мультиплексор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908602"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="15a1f-103">Фильтр DV мультиплексор</span><span class="sxs-lookup"><span data-stu-id="15a1f-103">DV Muxer Filter</span></span>

<span data-ttu-id="15a1f-104">Этот фильтр сочетает цифровой видеопоток (DV), закодированный видео, с одним или двумя звуковыми потоками для получения потока с чередованием.</span><span class="sxs-lookup"><span data-stu-id="15a1f-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="15a1f-105">Чтобы записать поток в файл AVI, подключите этот фильтр к фильтру [мультиплексора AVI](avi-mux-filter.md) и *подключите его к* фильтру [записи файлов](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="15a1f-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="15a1f-106">Дополнительные сведения см. [в статье цифровое видео в DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="15a1f-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



| <span data-ttu-id="15a1f-107">Метка</span><span class="sxs-lookup"><span data-stu-id="15a1f-107">Label</span></span> | <span data-ttu-id="15a1f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="15a1f-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15a1f-109">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="15a1f-109">Filter Interfaces</span></span>                        | <span data-ttu-id="15a1f-110">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="15a1f-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="15a1f-111">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="15a1f-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="15a1f-112">**Видео**: MediaType \_ Video, МЕДИАСУБТИПЕ \_ Двсд, формат \_ видеоинфо **Audio**: MEDIATYPE \_ Audio, медиасубтипе \_ PCM, Format \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="15a1f-112">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="15a1f-113">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="15a1f-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="15a1f-114">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="15a1f-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="15a1f-115">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="15a1f-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="15a1f-116">MEDIATYPE \_ с чередованием, медиасубтипе \_ ДВСД, Format \_ двинфо</span><span class="sxs-lookup"><span data-stu-id="15a1f-116">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="15a1f-117">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="15a1f-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="15a1f-118">[**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="15a1f-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="15a1f-119">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="15a1f-119">Filter CLSID</span></span>                             | <span data-ttu-id="15a1f-120">\_ДВМУКС CLSID</span><span class="sxs-lookup"><span data-stu-id="15a1f-120">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="15a1f-121">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="15a1f-121">Property Page CLSID</span></span>                      | <span data-ttu-id="15a1f-122">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="15a1f-122">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="15a1f-123">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="15a1f-123">Executable</span></span>                               | <span data-ttu-id="15a1f-124">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="15a1f-124">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="15a1f-125">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="15a1f-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="15a1f-126">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="15a1f-126">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="15a1f-127">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="15a1f-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="15a1f-128">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="15a1f-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="15a1f-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15a1f-129">Remarks</span></span>

<span data-ttu-id="15a1f-130">DV мультиплексор может создать два ПИН-кода для ввода звука.</span><span class="sxs-lookup"><span data-stu-id="15a1f-130">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="15a1f-131">Он поддерживает аудио форматы, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="15a1f-131">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="15a1f-132">Звуковой ПИН-код 1</span><span class="sxs-lookup"><span data-stu-id="15a1f-132">Audio Pin 1</span></span>

<span data-ttu-id="15a1f-133">Звуковой ПИН-код 2</span><span class="sxs-lookup"><span data-stu-id="15a1f-133">Audio Pin 2</span></span>

<span data-ttu-id="15a1f-134">Выходной формат</span><span class="sxs-lookup"><span data-stu-id="15a1f-134">Output Format</span></span>

<span data-ttu-id="15a1f-135">Частота выборки (кГц)</span><span class="sxs-lookup"><span data-stu-id="15a1f-135">Sample Rate (kHz)</span></span>

<span data-ttu-id="15a1f-136">Бит/пример</span><span class="sxs-lookup"><span data-stu-id="15a1f-136">Bits/Sample</span></span>

<span data-ttu-id="15a1f-137">Каналы</span><span class="sxs-lookup"><span data-stu-id="15a1f-137">Channels</span></span>

<span data-ttu-id="15a1f-138">Частота выборки</span><span class="sxs-lookup"><span data-stu-id="15a1f-138">Sample Rate</span></span>

<span data-ttu-id="15a1f-139">Бит/пример</span><span class="sxs-lookup"><span data-stu-id="15a1f-139">Bits/Sample</span></span>

<span data-ttu-id="15a1f-140">Каналы</span><span class="sxs-lookup"><span data-stu-id="15a1f-140">Channels</span></span>

<span data-ttu-id="15a1f-141">32</span><span class="sxs-lookup"><span data-stu-id="15a1f-141">32</span></span>

<span data-ttu-id="15a1f-142">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-142">16</span></span>

<span data-ttu-id="15a1f-143">Mono</span><span class="sxs-lookup"><span data-stu-id="15a1f-143">Mono</span></span>

<span data-ttu-id="15a1f-144">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="15a1f-144">Unconnected</span></span>

<span data-ttu-id="15a1f-145">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="15a1f-145">SD 2 Channel</span></span>

<span data-ttu-id="15a1f-146">32</span><span class="sxs-lookup"><span data-stu-id="15a1f-146">32</span></span>

<span data-ttu-id="15a1f-147">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-147">16</span></span>

<span data-ttu-id="15a1f-148">Stereo</span><span class="sxs-lookup"><span data-stu-id="15a1f-148">Stereo</span></span>

<span data-ttu-id="15a1f-149">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="15a1f-149">Unconnected</span></span>

<span data-ttu-id="15a1f-150">Канал SD 4</span><span class="sxs-lookup"><span data-stu-id="15a1f-150">SD 4 Channel</span></span>

<span data-ttu-id="15a1f-151">44,1 или 48</span><span class="sxs-lookup"><span data-stu-id="15a1f-151">44.1 or 48</span></span>

<span data-ttu-id="15a1f-152">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-152">16</span></span>

<span data-ttu-id="15a1f-153">Стерео или моно</span><span class="sxs-lookup"><span data-stu-id="15a1f-153">Stereo or Mono</span></span>

<span data-ttu-id="15a1f-154">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="15a1f-154">Unconnected</span></span>

<span data-ttu-id="15a1f-155">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="15a1f-155">SD 2 Channel</span></span>

<span data-ttu-id="15a1f-156">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="15a1f-156">Unconnected</span></span>

<span data-ttu-id="15a1f-157">32</span><span class="sxs-lookup"><span data-stu-id="15a1f-157">32</span></span>

<span data-ttu-id="15a1f-158">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-158">16</span></span>

<span data-ttu-id="15a1f-159">Стерео или моно</span><span class="sxs-lookup"><span data-stu-id="15a1f-159">Stereo or Mono</span></span>

<span data-ttu-id="15a1f-160">Запрещено</span><span class="sxs-lookup"><span data-stu-id="15a1f-160">Disallowed</span></span>

<span data-ttu-id="15a1f-161">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="15a1f-161">Unconnected</span></span>

<span data-ttu-id="15a1f-162">44,1 или 48</span><span class="sxs-lookup"><span data-stu-id="15a1f-162">44.1 or 48</span></span>

<span data-ttu-id="15a1f-163">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-163">16</span></span>

<span data-ttu-id="15a1f-164">Mono</span><span class="sxs-lookup"><span data-stu-id="15a1f-164">Mono</span></span>

<span data-ttu-id="15a1f-165">Запрещено</span><span class="sxs-lookup"><span data-stu-id="15a1f-165">Disallowed</span></span>

<span data-ttu-id="15a1f-166">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="15a1f-166">Unconnected</span></span>

<span data-ttu-id="15a1f-167">44,1 или 48</span><span class="sxs-lookup"><span data-stu-id="15a1f-167">44.1 or 48</span></span>

<span data-ttu-id="15a1f-168">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-168">16</span></span>

<span data-ttu-id="15a1f-169">Stereo</span><span class="sxs-lookup"><span data-stu-id="15a1f-169">Stereo</span></span>

<span data-ttu-id="15a1f-170">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="15a1f-170">SD 2 Channel</span></span>

<span data-ttu-id="15a1f-171">32</span><span class="sxs-lookup"><span data-stu-id="15a1f-171">32</span></span>

<span data-ttu-id="15a1f-172">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-172">16</span></span>

<span data-ttu-id="15a1f-173">Mono</span><span class="sxs-lookup"><span data-stu-id="15a1f-173">Mono</span></span>

<span data-ttu-id="15a1f-174">32</span><span class="sxs-lookup"><span data-stu-id="15a1f-174">32</span></span>

<span data-ttu-id="15a1f-175">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-175">16</span></span>

<span data-ttu-id="15a1f-176">Mono</span><span class="sxs-lookup"><span data-stu-id="15a1f-176">Mono</span></span>

<span data-ttu-id="15a1f-177">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="15a1f-177">SD 2 Channel</span></span>

<span data-ttu-id="15a1f-178">32</span><span class="sxs-lookup"><span data-stu-id="15a1f-178">32</span></span>

<span data-ttu-id="15a1f-179">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-179">16</span></span>

<span data-ttu-id="15a1f-180">Стерео или моно\*</span><span class="sxs-lookup"><span data-stu-id="15a1f-180">Stereo or Mono\*</span></span>

<span data-ttu-id="15a1f-181">32</span><span class="sxs-lookup"><span data-stu-id="15a1f-181">32</span></span>

<span data-ttu-id="15a1f-182">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-182">16</span></span>

<span data-ttu-id="15a1f-183">Стерео или моно\*</span><span class="sxs-lookup"><span data-stu-id="15a1f-183">Stereo or Mono\*</span></span>

<span data-ttu-id="15a1f-184">Канал SD 4</span><span class="sxs-lookup"><span data-stu-id="15a1f-184">SD 4 Channel</span></span>

<span data-ttu-id="15a1f-185">44,1</span><span class="sxs-lookup"><span data-stu-id="15a1f-185">44.1</span></span>

<span data-ttu-id="15a1f-186">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-186">16</span></span>

<span data-ttu-id="15a1f-187">Mono</span><span class="sxs-lookup"><span data-stu-id="15a1f-187">Mono</span></span>

<span data-ttu-id="15a1f-188">44,1</span><span class="sxs-lookup"><span data-stu-id="15a1f-188">44.1</span></span>

<span data-ttu-id="15a1f-189">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-189">16</span></span>

<span data-ttu-id="15a1f-190">Mono</span><span class="sxs-lookup"><span data-stu-id="15a1f-190">Mono</span></span>

<span data-ttu-id="15a1f-191">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="15a1f-191">SD 2 Channel</span></span>

<span data-ttu-id="15a1f-192">48</span><span class="sxs-lookup"><span data-stu-id="15a1f-192">48</span></span>

<span data-ttu-id="15a1f-193">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-193">16</span></span>

<span data-ttu-id="15a1f-194">Mono</span><span class="sxs-lookup"><span data-stu-id="15a1f-194">Mono</span></span>

<span data-ttu-id="15a1f-195">48</span><span class="sxs-lookup"><span data-stu-id="15a1f-195">48</span></span>

<span data-ttu-id="15a1f-196">16</span><span class="sxs-lookup"><span data-stu-id="15a1f-196">16</span></span>

<span data-ttu-id="15a1f-197">Mono</span><span class="sxs-lookup"><span data-stu-id="15a1f-197">Mono</span></span>

<span data-ttu-id="15a1f-198">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="15a1f-198">SD 2 Channel</span></span>

<span data-ttu-id="15a1f-199">\* Если по крайней мере один входной ПИН-код стерео.</span><span class="sxs-lookup"><span data-stu-id="15a1f-199">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="15a1f-200">В этой таблице звуковой ПИН 1 определяется как первый входной ПИН-код, подключенный к звуковому источнику, а звуковой ПИН-код 2 — вторым входным закреплением, подключенным к источнику аудио.</span><span class="sxs-lookup"><span data-stu-id="15a1f-200">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="15a1f-201">После подключения звукового контакта эта схема нумерации остается в силе, пока не будут отключены оба звуковых контакта.</span><span class="sxs-lookup"><span data-stu-id="15a1f-201">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="15a1f-202">Например, если вы подключаете оба звуковых контакта, а затем отключаете звуковый ПИН-код 1, оставшийся ПИН-код все равно считается ПИН-кодом 2.</span><span class="sxs-lookup"><span data-stu-id="15a1f-202">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="15a1f-203">Звук, передаваемый контакту 1, записывается в первый звуковой блок DV-кадров (CH1), а аудио, предоставляемые для крепления 2, записываются во второй звуковой блок (CH2).</span><span class="sxs-lookup"><span data-stu-id="15a1f-203">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="15a1f-204">Исключение: Если фильтр имеет один стерео вход в 44,1 кГц или 48 кГц, левый звуковой канал записывается в первый аудио блок, а правильный звуковой канал записывается во второй звуковой блок.</span><span class="sxs-lookup"><span data-stu-id="15a1f-204">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="15a1f-205">Для вывода SD 4-Channel OUTPUT: если входные данные являются стерео, то запись Left записывается в ча или ЧК, а правая запись записывается в ЧБ или данные владельца карты.</span><span class="sxs-lookup"><span data-stu-id="15a1f-205">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="15a1f-206">Если входные данные — Mono, звук записывается в ча или ЧК, а ЧБ и данные владельца карты — в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="15a1f-206">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="15a1f-207">Подключив и отключая звуковой ПИН-код 1, можно получить недопустимый формат.</span><span class="sxs-lookup"><span data-stu-id="15a1f-207">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="15a1f-208">В этом случае метод [**имедиафилтер::P Аусе**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) в фильтре возвращает VFW \_ E \_ Not \_ Connected.</span><span class="sxs-lookup"><span data-stu-id="15a1f-208">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="15a1f-209">Это ограничение предотвращает ситуацию, когда первый звуковой блок не имеет звука, а второй звуковой блок имеет звук.</span><span class="sxs-lookup"><span data-stu-id="15a1f-209">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="15a1f-210">Второй блок должен иметь звук, только если у первого блока также есть звук.</span><span class="sxs-lookup"><span data-stu-id="15a1f-210">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="15a1f-211">DV мультиплексор не допускают входные аудиоданные с различными тарифными частотами.</span><span class="sxs-lookup"><span data-stu-id="15a1f-211">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="15a1f-212">Однако такие методы построения графа, как [**играфбуилдер:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , обычно добавляют фильтр [оболочки ACM](acm-wrapper-filter.md) , который преобразует второй аудиопоток в соответствии с частотой выборки первого потока.</span><span class="sxs-lookup"><span data-stu-id="15a1f-212">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="15a1f-213">Если звуковая входная запись составляет 48 кГц или 32 кГц, звуковые выходные данные блокируются.</span><span class="sxs-lookup"><span data-stu-id="15a1f-213">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="15a1f-214">(Блокировка звука 44,1-кГц невозможна.)</span><span class="sxs-lookup"><span data-stu-id="15a1f-214">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="15a1f-215">Если нет подключенных звуковых контактов, выходные данные будут содержать аудиоданные из входящих DV-кадров.</span><span class="sxs-lookup"><span data-stu-id="15a1f-215">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="15a1f-216">Это может быть тишина или допустимые звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="15a1f-216">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15a1f-217">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="15a1f-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15a1f-218">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="15a1f-218">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="15a1f-219">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="15a1f-219">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



