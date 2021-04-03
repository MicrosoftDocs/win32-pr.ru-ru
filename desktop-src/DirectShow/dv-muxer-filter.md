---
description: Фильтр DV мультиплексор
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Фильтр DV мультиплексор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806700"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="66077-103">Фильтр DV мультиплексор</span><span class="sxs-lookup"><span data-stu-id="66077-103">DV Muxer Filter</span></span>

<span data-ttu-id="66077-104">Этот фильтр сочетает цифровой видеопоток (DV), закодированный видео, с одним или двумя звуковыми потоками для получения потока с чередованием.</span><span class="sxs-lookup"><span data-stu-id="66077-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="66077-105">Чтобы записать поток в файл AVI, подключите этот фильтр к фильтру [мультиплексора AVI](avi-mux-filter.md) и *подключите его к* фильтру [записи файлов](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="66077-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="66077-106">Дополнительные сведения см. [в статье цифровое видео в DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="66077-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66077-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="66077-107">Filter Interfaces</span></span>                        | <span data-ttu-id="66077-108">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="66077-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="66077-109">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="66077-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="66077-110">**Видео**: MediaType \_ Video, МЕДИАСУБТИПЕ \_ Двсд, формат \_ видеоинфо **Audio**: MEDIATYPE \_ Audio, медиасубтипе \_ PCM, Format \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="66077-110">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="66077-111">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="66077-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="66077-112">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="66077-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="66077-113">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="66077-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="66077-114">MEDIATYPE \_ с чередованием, медиасубтипе \_ ДВСД, Format \_ двинфо</span><span class="sxs-lookup"><span data-stu-id="66077-114">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="66077-115">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="66077-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="66077-116">[**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="66077-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="66077-117">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="66077-117">Filter CLSID</span></span>                             | <span data-ttu-id="66077-118">\_ДВМУКС CLSID</span><span class="sxs-lookup"><span data-stu-id="66077-118">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="66077-119">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="66077-119">Property Page CLSID</span></span>                      | <span data-ttu-id="66077-120">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="66077-120">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="66077-121">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="66077-121">Executable</span></span>                               | <span data-ttu-id="66077-122">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="66077-122">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="66077-123">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="66077-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="66077-124">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="66077-124">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="66077-125">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="66077-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="66077-126">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="66077-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="66077-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66077-127">Remarks</span></span>

<span data-ttu-id="66077-128">DV мультиплексор может создать два ПИН-кода для ввода звука.</span><span class="sxs-lookup"><span data-stu-id="66077-128">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="66077-129">Он поддерживает аудио форматы, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="66077-129">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="66077-130">Звуковой ПИН-код 1</span><span class="sxs-lookup"><span data-stu-id="66077-130">Audio Pin 1</span></span>

<span data-ttu-id="66077-131">Звуковой ПИН-код 2</span><span class="sxs-lookup"><span data-stu-id="66077-131">Audio Pin 2</span></span>

<span data-ttu-id="66077-132">Выходной формат</span><span class="sxs-lookup"><span data-stu-id="66077-132">Output Format</span></span>

<span data-ttu-id="66077-133">Частота выборки (кГц)</span><span class="sxs-lookup"><span data-stu-id="66077-133">Sample Rate (kHz)</span></span>

<span data-ttu-id="66077-134">Бит/пример</span><span class="sxs-lookup"><span data-stu-id="66077-134">Bits/Sample</span></span>

<span data-ttu-id="66077-135">Каналы</span><span class="sxs-lookup"><span data-stu-id="66077-135">Channels</span></span>

<span data-ttu-id="66077-136">Частота выборки</span><span class="sxs-lookup"><span data-stu-id="66077-136">Sample Rate</span></span>

<span data-ttu-id="66077-137">Бит/пример</span><span class="sxs-lookup"><span data-stu-id="66077-137">Bits/Sample</span></span>

<span data-ttu-id="66077-138">Каналы</span><span class="sxs-lookup"><span data-stu-id="66077-138">Channels</span></span>

<span data-ttu-id="66077-139">32</span><span class="sxs-lookup"><span data-stu-id="66077-139">32</span></span>

<span data-ttu-id="66077-140">16</span><span class="sxs-lookup"><span data-stu-id="66077-140">16</span></span>

<span data-ttu-id="66077-141">Mono</span><span class="sxs-lookup"><span data-stu-id="66077-141">Mono</span></span>

<span data-ttu-id="66077-142">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="66077-142">Unconnected</span></span>

<span data-ttu-id="66077-143">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="66077-143">SD 2 Channel</span></span>

<span data-ttu-id="66077-144">32</span><span class="sxs-lookup"><span data-stu-id="66077-144">32</span></span>

<span data-ttu-id="66077-145">16</span><span class="sxs-lookup"><span data-stu-id="66077-145">16</span></span>

<span data-ttu-id="66077-146">Stereo</span><span class="sxs-lookup"><span data-stu-id="66077-146">Stereo</span></span>

<span data-ttu-id="66077-147">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="66077-147">Unconnected</span></span>

<span data-ttu-id="66077-148">Канал SD 4</span><span class="sxs-lookup"><span data-stu-id="66077-148">SD 4 Channel</span></span>

<span data-ttu-id="66077-149">44,1 или 48</span><span class="sxs-lookup"><span data-stu-id="66077-149">44.1 or 48</span></span>

<span data-ttu-id="66077-150">16</span><span class="sxs-lookup"><span data-stu-id="66077-150">16</span></span>

<span data-ttu-id="66077-151">Стерео или моно</span><span class="sxs-lookup"><span data-stu-id="66077-151">Stereo or Mono</span></span>

<span data-ttu-id="66077-152">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="66077-152">Unconnected</span></span>

<span data-ttu-id="66077-153">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="66077-153">SD 2 Channel</span></span>

<span data-ttu-id="66077-154">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="66077-154">Unconnected</span></span>

<span data-ttu-id="66077-155">32</span><span class="sxs-lookup"><span data-stu-id="66077-155">32</span></span>

<span data-ttu-id="66077-156">16</span><span class="sxs-lookup"><span data-stu-id="66077-156">16</span></span>

<span data-ttu-id="66077-157">Стерео или моно</span><span class="sxs-lookup"><span data-stu-id="66077-157">Stereo or Mono</span></span>

<span data-ttu-id="66077-158">Запрещено</span><span class="sxs-lookup"><span data-stu-id="66077-158">Disallowed</span></span>

<span data-ttu-id="66077-159">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="66077-159">Unconnected</span></span>

<span data-ttu-id="66077-160">44,1 или 48</span><span class="sxs-lookup"><span data-stu-id="66077-160">44.1 or 48</span></span>

<span data-ttu-id="66077-161">16</span><span class="sxs-lookup"><span data-stu-id="66077-161">16</span></span>

<span data-ttu-id="66077-162">Mono</span><span class="sxs-lookup"><span data-stu-id="66077-162">Mono</span></span>

<span data-ttu-id="66077-163">Запрещено</span><span class="sxs-lookup"><span data-stu-id="66077-163">Disallowed</span></span>

<span data-ttu-id="66077-164">Неподключенный</span><span class="sxs-lookup"><span data-stu-id="66077-164">Unconnected</span></span>

<span data-ttu-id="66077-165">44,1 или 48</span><span class="sxs-lookup"><span data-stu-id="66077-165">44.1 or 48</span></span>

<span data-ttu-id="66077-166">16</span><span class="sxs-lookup"><span data-stu-id="66077-166">16</span></span>

<span data-ttu-id="66077-167">Stereo</span><span class="sxs-lookup"><span data-stu-id="66077-167">Stereo</span></span>

<span data-ttu-id="66077-168">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="66077-168">SD 2 Channel</span></span>

<span data-ttu-id="66077-169">32</span><span class="sxs-lookup"><span data-stu-id="66077-169">32</span></span>

<span data-ttu-id="66077-170">16</span><span class="sxs-lookup"><span data-stu-id="66077-170">16</span></span>

<span data-ttu-id="66077-171">Mono</span><span class="sxs-lookup"><span data-stu-id="66077-171">Mono</span></span>

<span data-ttu-id="66077-172">32</span><span class="sxs-lookup"><span data-stu-id="66077-172">32</span></span>

<span data-ttu-id="66077-173">16</span><span class="sxs-lookup"><span data-stu-id="66077-173">16</span></span>

<span data-ttu-id="66077-174">Mono</span><span class="sxs-lookup"><span data-stu-id="66077-174">Mono</span></span>

<span data-ttu-id="66077-175">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="66077-175">SD 2 Channel</span></span>

<span data-ttu-id="66077-176">32</span><span class="sxs-lookup"><span data-stu-id="66077-176">32</span></span>

<span data-ttu-id="66077-177">16</span><span class="sxs-lookup"><span data-stu-id="66077-177">16</span></span>

<span data-ttu-id="66077-178">Стерео или моно\*</span><span class="sxs-lookup"><span data-stu-id="66077-178">Stereo or Mono\*</span></span>

<span data-ttu-id="66077-179">32</span><span class="sxs-lookup"><span data-stu-id="66077-179">32</span></span>

<span data-ttu-id="66077-180">16</span><span class="sxs-lookup"><span data-stu-id="66077-180">16</span></span>

<span data-ttu-id="66077-181">Стерео или моно\*</span><span class="sxs-lookup"><span data-stu-id="66077-181">Stereo or Mono\*</span></span>

<span data-ttu-id="66077-182">Канал SD 4</span><span class="sxs-lookup"><span data-stu-id="66077-182">SD 4 Channel</span></span>

<span data-ttu-id="66077-183">44,1</span><span class="sxs-lookup"><span data-stu-id="66077-183">44.1</span></span>

<span data-ttu-id="66077-184">16</span><span class="sxs-lookup"><span data-stu-id="66077-184">16</span></span>

<span data-ttu-id="66077-185">Mono</span><span class="sxs-lookup"><span data-stu-id="66077-185">Mono</span></span>

<span data-ttu-id="66077-186">44,1</span><span class="sxs-lookup"><span data-stu-id="66077-186">44.1</span></span>

<span data-ttu-id="66077-187">16</span><span class="sxs-lookup"><span data-stu-id="66077-187">16</span></span>

<span data-ttu-id="66077-188">Mono</span><span class="sxs-lookup"><span data-stu-id="66077-188">Mono</span></span>

<span data-ttu-id="66077-189">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="66077-189">SD 2 Channel</span></span>

<span data-ttu-id="66077-190">48</span><span class="sxs-lookup"><span data-stu-id="66077-190">48</span></span>

<span data-ttu-id="66077-191">16</span><span class="sxs-lookup"><span data-stu-id="66077-191">16</span></span>

<span data-ttu-id="66077-192">Mono</span><span class="sxs-lookup"><span data-stu-id="66077-192">Mono</span></span>

<span data-ttu-id="66077-193">48</span><span class="sxs-lookup"><span data-stu-id="66077-193">48</span></span>

<span data-ttu-id="66077-194">16</span><span class="sxs-lookup"><span data-stu-id="66077-194">16</span></span>

<span data-ttu-id="66077-195">Mono</span><span class="sxs-lookup"><span data-stu-id="66077-195">Mono</span></span>

<span data-ttu-id="66077-196">Канал SD 2</span><span class="sxs-lookup"><span data-stu-id="66077-196">SD 2 Channel</span></span>

<span data-ttu-id="66077-197">\* Если по крайней мере один входной ПИН-код стерео.</span><span class="sxs-lookup"><span data-stu-id="66077-197">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="66077-198">В этой таблице звуковой ПИН 1 определяется как первый входной ПИН-код, подключенный к звуковому источнику, а звуковой ПИН-код 2 — вторым входным закреплением, подключенным к источнику аудио.</span><span class="sxs-lookup"><span data-stu-id="66077-198">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="66077-199">После подключения звукового контакта эта схема нумерации остается в силе, пока не будут отключены оба звуковых контакта.</span><span class="sxs-lookup"><span data-stu-id="66077-199">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="66077-200">Например, если вы подключаете оба звуковых контакта, а затем отключаете звуковый ПИН-код 1, оставшийся ПИН-код все равно считается ПИН-кодом 2.</span><span class="sxs-lookup"><span data-stu-id="66077-200">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="66077-201">Звук, передаваемый контакту 1, записывается в первый звуковой блок DV-кадров (CH1), а аудио, предоставляемые для крепления 2, записываются во второй звуковой блок (CH2).</span><span class="sxs-lookup"><span data-stu-id="66077-201">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="66077-202">Исключение: Если фильтр имеет один стерео вход в 44,1 кГц или 48 кГц, левый звуковой канал записывается в первый аудио блок, а правильный звуковой канал записывается во второй звуковой блок.</span><span class="sxs-lookup"><span data-stu-id="66077-202">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="66077-203">Для вывода SD 4-Channel OUTPUT: если входные данные являются стерео, то запись Left записывается в ча или ЧК, а правая запись записывается в ЧБ или данные владельца карты.</span><span class="sxs-lookup"><span data-stu-id="66077-203">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="66077-204">Если входные данные — Mono, звук записывается в ча или ЧК, а ЧБ и данные владельца карты — в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="66077-204">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="66077-205">Подключив и отключая звуковой ПИН-код 1, можно получить недопустимый формат.</span><span class="sxs-lookup"><span data-stu-id="66077-205">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="66077-206">В этом случае метод [**имедиафилтер::P Аусе**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) в фильтре возвращает VFW \_ E \_ Not \_ Connected.</span><span class="sxs-lookup"><span data-stu-id="66077-206">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="66077-207">Это ограничение предотвращает ситуацию, когда первый звуковой блок не имеет звука, а второй звуковой блок имеет звук.</span><span class="sxs-lookup"><span data-stu-id="66077-207">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="66077-208">Второй блок должен иметь звук, только если у первого блока также есть звук.</span><span class="sxs-lookup"><span data-stu-id="66077-208">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="66077-209">DV мультиплексор не допускают входные аудиоданные с различными тарифными частотами.</span><span class="sxs-lookup"><span data-stu-id="66077-209">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="66077-210">Однако такие методы построения графа, как [**играфбуилдер:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , обычно добавляют фильтр [оболочки ACM](acm-wrapper-filter.md) , который преобразует второй аудиопоток в соответствии с частотой выборки первого потока.</span><span class="sxs-lookup"><span data-stu-id="66077-210">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="66077-211">Если звуковая входная запись составляет 48 кГц или 32 кГц, звуковые выходные данные блокируются.</span><span class="sxs-lookup"><span data-stu-id="66077-211">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="66077-212">(Блокировка звука 44,1-кГц невозможна.)</span><span class="sxs-lookup"><span data-stu-id="66077-212">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="66077-213">Если нет подключенных звуковых контактов, выходные данные будут содержать аудиоданные из входящих DV-кадров.</span><span class="sxs-lookup"><span data-stu-id="66077-213">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="66077-214">Это может быть тишина или допустимые звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="66077-214">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66077-215">См. также</span><span class="sxs-lookup"><span data-stu-id="66077-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66077-216">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="66077-216">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="66077-217">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="66077-217">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



