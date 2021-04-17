---
description: Фильтр звукового кодировщика Microsoft MPEG-2 кодирует звуковые слои MPEG-1 I и II, включая поддержку расширений MPEG-2 с низким частотой дискретизации (LSF).
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Кодировщик Microsoft MPEG-2 Audio Encoder (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673019"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a><span data-ttu-id="3c46e-103">Кодировщик Microsoft MPEG-2 Audio Encoder</span><span class="sxs-lookup"><span data-stu-id="3c46e-103">Microsoft MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="3c46e-104">Фильтр звукового кодировщика Microsoft MPEG-2 кодирует звуковые слои MPEG-1 I и II, включая поддержку расширений MPEG-2 с низким частотой дискретизации (LSF).</span><span class="sxs-lookup"><span data-stu-id="3c46e-104">The Microsoft MPEG-2 Audio Encoder filter encodes MPEG-1 audio layers I and II, including support for the MPEG-2 Low Sampling Frequency (LSF) extensions.</span></span>

<span data-ttu-id="3c46e-105">Для кодирования и мультиплексирования потоков аудио/видео используйте фильтр [**кодировщика Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md) , который инкапсулирует функции обоих фильтров и фильтра [**видеокодировщика Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md) .</span><span class="sxs-lookup"><span data-stu-id="3c46e-105">To encode and multiplex audio/video streams, use the [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md) filter, which encapsulates the functions of both this filter and the [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="3c46e-106">Этот фильтр не поддерживается на платформах на базе IA-64.</span><span class="sxs-lookup"><span data-stu-id="3c46e-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="3c46e-107">Сведения о фильтре</span><span class="sxs-lookup"><span data-stu-id="3c46e-107">Filter Information</span></span>

<span data-ttu-id="3c46e-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="3c46e-108">Filter Interfaces</span></span>

[<span data-ttu-id="3c46e-109">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="3c46e-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="3c46e-110">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="3c46e-110">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="3c46e-111">**иенкодерапи**</span><span class="sxs-lookup"><span data-stu-id="3c46e-111">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="3c46e-112">**имедиасикинг**</span><span class="sxs-lookup"><span data-stu-id="3c46e-112">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="3c46e-113">**ивидеоенкодер**</span><span class="sxs-lookup"><span data-stu-id="3c46e-113">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="3c46e-114">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="3c46e-114">Input Pin Media Types</span></span>

<span data-ttu-id="3c46e-115">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="3c46e-115">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="3c46e-116">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="3c46e-116">Input Pin Interfaces</span></span>

[<span data-ttu-id="3c46e-117">**имеминпутпин**</span><span class="sxs-lookup"><span data-stu-id="3c46e-117">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="3c46e-118">**ипин**</span><span class="sxs-lookup"><span data-stu-id="3c46e-118">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="3c46e-119">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="3c46e-119">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="3c46e-120">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="3c46e-120">Output Pin Media Types</span></span>

<span data-ttu-id="3c46e-121">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="3c46e-121">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="3c46e-122">**MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="3c46e-122">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="3c46e-123">**MEDIATYPE \_ Stream**, **\_ \_ Программа медиасубтипе MPEG2**</span><span class="sxs-lookup"><span data-stu-id="3c46e-123">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span><br/> <span data-ttu-id="3c46e-124">**MEDIATYPE \_ Поток**, **\_ \_ транспорт медиасубтипе MPEG2**</span><span class="sxs-lookup"><span data-stu-id="3c46e-124">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span><br/>

<span data-ttu-id="3c46e-125">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="3c46e-125">Output Pin Interfaces</span></span>

[<span data-ttu-id="3c46e-126">**имедиасикинг**</span><span class="sxs-lookup"><span data-stu-id="3c46e-126">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="3c46e-127">**ипин**</span><span class="sxs-lookup"><span data-stu-id="3c46e-127">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="3c46e-128">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="3c46e-128">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="3c46e-129">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="3c46e-129">Filter CLSID</span></span>

<span data-ttu-id="3c46e-130">**Идентификатор CLSID \_ CMPEG2EncoderAudioDS** (объявлено в вмкодекдсп. h)</span><span class="sxs-lookup"><span data-stu-id="3c46e-130">**CLSID\_CMPEG2EncoderAudioDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="3c46e-131">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="3c46e-131">Executable</span></span>

<span data-ttu-id="3c46e-132">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="3c46e-132">msmpeg2enc.dll</span></span>

[<span data-ttu-id="3c46e-133">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="3c46e-133">Merit</span></span>](merit.md)

<span data-ttu-id="3c46e-134">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="3c46e-134">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="3c46e-135">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="3c46e-135">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="3c46e-136">**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="3c46e-136">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="3c46e-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c46e-137">Remarks</span></span>

<span data-ttu-id="3c46e-138">Кодировщик MPEG-2 может формировать следующие типы выходных данных:</span><span class="sxs-lookup"><span data-stu-id="3c46e-138">The MPEG-2 Audio Encoder can produce the following kinds of output:</span></span>

-   <span data-ttu-id="3c46e-139">Простейший поток звука</span><span class="sxs-lookup"><span data-stu-id="3c46e-139">Audio elementary stream</span></span>
-   <span data-ttu-id="3c46e-140">Звук в потоке программы MPEG-2</span><span class="sxs-lookup"><span data-stu-id="3c46e-140">Audio in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="3c46e-141">Звук в транспортном потоке MPEG-2</span><span class="sxs-lookup"><span data-stu-id="3c46e-141">Audio in an MPEG-2 transport stream</span></span>

<span data-ttu-id="3c46e-142">Он поддерживает расширения MPEG-1 с уровнями I и II и MPEG-2 с низкой частотой дискретизации (LSF).</span><span class="sxs-lookup"><span data-stu-id="3c46e-142">It supports MPEG-1 layers I and II and MPEG-2 low sampling frequency (LSF) extensions</span></span>

<span data-ttu-id="3c46e-143">В примерах входных данных должно быть 16 бит на выборку с частотой выборки звука 48, 44,1, 32, 22,05 или 16 кГц.</span><span class="sxs-lookup"><span data-stu-id="3c46e-143">Input samples must 16 bits per sample, with an audio sampling rate of 48, 44.1, 32, 22.05, or 16 KHz.</span></span> <span data-ttu-id="3c46e-144">Кодировщику не удается выполнить повторную выборку аудиопотока; закодированный звук имеет ту же частоту выборки, что и входные данные.</span><span class="sxs-lookup"><span data-stu-id="3c46e-144">The encoder cannot resample the audio stream; the encoded audio has the same sample rate as the input.</span></span>

<span data-ttu-id="3c46e-145">Входные образцы должны быть Mono или стерео.</span><span class="sxs-lookup"><span data-stu-id="3c46e-145">Input samples must be mono or stereo.</span></span> <span data-ttu-id="3c46e-146">В закодированном аудио содержится число каналов в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="3c46e-146">The encoded audio has the number of channels as the input.</span></span>

### <a name="limitations"></a><span data-ttu-id="3c46e-147">Ограничения</span><span class="sxs-lookup"><span data-stu-id="3c46e-147">Limitations</span></span>

<span data-ttu-id="3c46e-148">Кодировщик не поддерживает следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3c46e-148">The encoder does not support the following:</span></span>

-   <span data-ttu-id="3c46e-149">Аудио битстреамс MPEG Layer III.</span><span class="sxs-lookup"><span data-stu-id="3c46e-149">MPEG layer III audio bitstreams.</span></span>
-   <span data-ttu-id="3c46e-150">Многоканальное расширение MPEG-2 битстреамс.</span><span class="sxs-lookup"><span data-stu-id="3c46e-150">MPEG-2 multi-channel extension bitstreams.</span></span>
-   <span data-ttu-id="3c46e-151">MPEG-4 AAC битстреамс.</span><span class="sxs-lookup"><span data-stu-id="3c46e-151">MPEG-4 AAC bitstreams.</span></span>
-   <span data-ttu-id="3c46e-152">Битстреамс (NBC) MPEG-2 без обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="3c46e-152">MPEG-2 non-backward compatible (NBC) bitstreams.</span></span>
-   <span data-ttu-id="3c46e-153">Создание пакетных пакетов простейшего потока (PES).</span><span class="sxs-lookup"><span data-stu-id="3c46e-153">Generation of packetized elementary stream (PES) packets.</span></span>
-   <span data-ttu-id="3c46e-154">Цифровая кодировка Dolby.</span><span class="sxs-lookup"><span data-stu-id="3c46e-154">Dolby Digital encoding.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="3c46e-155">Свойства кодека</span><span class="sxs-lookup"><span data-stu-id="3c46e-155">Codec Properties</span></span>

<span data-ttu-id="3c46e-156">Фильтр поддерживает следующие свойства с помощью [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="3c46e-156">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>

-   [<span data-ttu-id="3c46e-157">**аваудиочаннелкаунт**</span><span class="sxs-lookup"><span data-stu-id="3c46e-157">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)
-   [<span data-ttu-id="3c46e-158">**аваудиосамплерате**</span><span class="sxs-lookup"><span data-stu-id="3c46e-158">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)
-   [<span data-ttu-id="3c46e-159">**авенкаудиоинтервалтоенкоде**</span><span class="sxs-lookup"><span data-stu-id="3c46e-159">**AVEncAudioIntervalToEncode**</span></span>](avencaudiointervaltoencode-property.md)
-   [<span data-ttu-id="3c46e-160">**авенккоммонформатконстраинт**</span><span class="sxs-lookup"><span data-stu-id="3c46e-160">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
-   [<span data-ttu-id="3c46e-161">**авенккоммонмеанбитрате**</span><span class="sxs-lookup"><span data-stu-id="3c46e-161">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="3c46e-162">**авенкмпакодингмоде**</span><span class="sxs-lookup"><span data-stu-id="3c46e-162">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)
-   [<span data-ttu-id="3c46e-163">**авенкмпакопиригхт**</span><span class="sxs-lookup"><span data-stu-id="3c46e-163">**AVEncMPACopyright**</span></span>](avencmpacopyright-property.md)
-   [<span data-ttu-id="3c46e-164">**авенкмпаемфасистипе**</span><span class="sxs-lookup"><span data-stu-id="3c46e-164">**AVEncMPAEmphasisType**</span></span>](avencmpaemphasistype-property.md)
-   [<span data-ttu-id="3c46e-165">**авенкмпаенаблередунданципротектион**</span><span class="sxs-lookup"><span data-stu-id="3c46e-165">**AVEncMPAEnableRedundancyProtection**</span></span>](avencmpaenableredundancyprotection-property.md)
-   [<span data-ttu-id="3c46e-166">**авенкмпалайер**</span><span class="sxs-lookup"><span data-stu-id="3c46e-166">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
-   [<span data-ttu-id="3c46e-167">**авенкмпаоригиналбитстреам**</span><span class="sxs-lookup"><span data-stu-id="3c46e-167">**AVEncMPAOriginalBitstream**</span></span>](avencmpaoriginalbitstream-property.md)
-   [<span data-ttu-id="3c46e-168">**авенкмпаприватеусербит**</span><span class="sxs-lookup"><span data-stu-id="3c46e-168">**AVEncMPAPrivateUserBit**</span></span>](avencmpaprivateuserbit-property.md)

> [!Note]  
> <span data-ttu-id="3c46e-169">В более ранней версии документации неправильно указаны некоторые дополнительные свойства, которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3c46e-169">An earlier version of the documentation incorrectly listed some additional properties that are not supported.</span></span>

 

<span data-ttu-id="3c46e-170">Для обеспечения обратной совместимости фильтр поддерживает следующее свойство через интерфейс **иенкодерапи** :</span><span class="sxs-lookup"><span data-stu-id="3c46e-170">For backward compatibility, the filter supports the following property through the **IEncoderAPI** interface:</span></span>



| <span data-ttu-id="3c46e-171">Свойство</span><span class="sxs-lookup"><span data-stu-id="3c46e-171">Property</span></span>                 | <span data-ttu-id="3c46e-172">Описание</span><span class="sxs-lookup"><span data-stu-id="3c46e-172">Description</span></span>                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c46e-173">**\_скорость енкапипарам**</span><span class="sxs-lookup"><span data-stu-id="3c46e-173">**ENCAPIPARAM\_BITRATE**</span></span> | <span data-ttu-id="3c46e-174">Эквивалентно [**авенккоммонмеанбитрате**](avenccommonmeanbitrate-property.md).</span><span class="sxs-lookup"><span data-stu-id="3c46e-174">Equivalent to [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span></span> |



 

<span data-ttu-id="3c46e-175">Рекомендуется задавать свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="3c46e-175">It is recommended to set properties in the following order:</span></span>

1.  [<span data-ttu-id="3c46e-176">**авенккоммонформатконстраинт**</span><span class="sxs-lookup"><span data-stu-id="3c46e-176">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
2.  [<span data-ttu-id="3c46e-177">**авенкмпалайер**</span><span class="sxs-lookup"><span data-stu-id="3c46e-177">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
3.  [<span data-ttu-id="3c46e-178">**авенккоммонмеанбитрате**</span><span class="sxs-lookup"><span data-stu-id="3c46e-178">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
4.  [<span data-ttu-id="3c46e-179">**авенкмпакодингмоде**</span><span class="sxs-lookup"><span data-stu-id="3c46e-179">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)

<span data-ttu-id="3c46e-180">Задайте остальные свойства в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="3c46e-180">Set the remaining properties in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c46e-181">Требования</span><span class="sxs-lookup"><span data-stu-id="3c46e-181">Requirements</span></span>



| <span data-ttu-id="3c46e-182">Требование</span><span class="sxs-lookup"><span data-stu-id="3c46e-182">Requirement</span></span> | <span data-ttu-id="3c46e-183">Значение</span><span class="sxs-lookup"><span data-stu-id="3c46e-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c46e-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c46e-184">Minimum supported client</span></span><br/> | <span data-ttu-id="3c46e-185">Windows Vista Домашняя расширенная, Windows Vista Ultimate, Windows 7 Домашняя расширенная, Windows 7 Профессиональная, Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="3c46e-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3c46e-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c46e-186">Minimum supported server</span></span><br/> | <span data-ttu-id="3c46e-187">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3c46e-187">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="3c46e-188">Header</span><span class="sxs-lookup"><span data-stu-id="3c46e-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c46e-189"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c46e-189"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="3c46e-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c46e-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c46e-191">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c46e-191">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="3c46e-192">**Типы носителей для демультиплексирования MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="3c46e-192">**MPEG-2 Demultiplexer Media Types**</span></span>](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
