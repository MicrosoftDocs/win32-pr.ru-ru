---
description: 'Этот фильтр декодирует следующие форматы звука:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Microsoft MPEG-1/DD/AAC Audio декодер (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682249"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a><span data-ttu-id="cef54-103">Декодер звука Microsoft MPEG-1/DD/AAC</span><span class="sxs-lookup"><span data-stu-id="cef54-103">Microsoft MPEG-1/DD/AAC Audio Decoder</span></span>

<span data-ttu-id="cef54-104">Этот фильтр декодирует следующие форматы звука:</span><span class="sxs-lookup"><span data-stu-id="cef54-104">This filter decodes the following audio formats:</span></span>

-   <span data-ttu-id="cef54-105">Звуковые слои MPEG-1 I и II.</span><span class="sxs-lookup"><span data-stu-id="cef54-105">MPEG-1 audio layers I and II.</span></span>
-   <span data-ttu-id="cef54-106">Обратная совместимость MPEG-2 аудио, слои I и II (ISO/IEC 13818-3), моно и стерео.</span><span class="sxs-lookup"><span data-stu-id="cef54-106">Backward-compatible MPEG-2 audio, layers I and II (ISO/IEC 13818-3), mono and stereo only.</span></span>
-   <span data-ttu-id="cef54-107">Расширенный профиль (LC) с низким уровнем сложности (AAC).</span><span class="sxs-lookup"><span data-stu-id="cef54-107">Advanced Audio Coding (AAC) Low Complexity (LC) profile.</span></span>
-   <span data-ttu-id="cef54-108">High-Efficiency AAC (HE-AAC) версии 1 и версии 2.</span><span class="sxs-lookup"><span data-stu-id="cef54-108">High-Efficiency AAC (HE-AAC) version 1 and version 2.</span></span>
-   <span data-ttu-id="cef54-109">Сквозные системы цифрового кинотеатра (DTS) для цифрового выхода.</span><span class="sxs-lookup"><span data-stu-id="cef54-109">Pass-through Digital Theater Systems (DTS) for digital output.</span></span>
-   <span data-ttu-id="cef54-110">ЛПКМ, Mono и стерео, с или без PES.</span><span class="sxs-lookup"><span data-stu-id="cef54-110">LPCM, mono and stereo only, with or without PES headers.</span></span>
-   <span data-ttu-id="cef54-111">Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="cef54-111">Dolby Digital.</span></span>
-   <span data-ttu-id="cef54-112">Dolby Digital Plus, включая преобразование из Dolby Digital Plus в Dolby Digital для цифрового выхода.</span><span class="sxs-lookup"><span data-stu-id="cef54-112">Dolby Digital Plus, including conversion from Dolby Digital Plus to Dolby Digital for digital output.</span></span>

> [!Note]  
> <span data-ttu-id="cef54-113">Реализация технологий Dolby Digital в корпорации Майкрософт ограничена условиями программы цифрового лицензирования Dolby, используемой приложениями Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="cef54-113">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="cef54-114">Этот фильтр не поддерживается на платформах на базе IA-64.</span><span class="sxs-lookup"><span data-stu-id="cef54-114">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="cef54-115">Для декодирования форматов Dolby Digital Plus, AAC и AAC требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cef54-115">Decoding of Dolby Digital Plus, AAC, and HE-AAC formats requires Windows 7.</span></span> <span data-ttu-id="cef54-116">Декодирование Dolby Digital или Dolby Digital Plus не поддерживается в Windows 7 Домашняя базовая или Windows 7 Начальная.</span><span class="sxs-lookup"><span data-stu-id="cef54-116">Decoding of Dolby Digital or Dolby Digital Plus is not supported on Windows 7 Home Basic or Windows 7 Starter.</span></span>

<span data-ttu-id="cef54-117">В реестре понятное имя этого фильтра — "Microsoft ДТВ-DVD Audio декодер".</span><span class="sxs-lookup"><span data-stu-id="cef54-117">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Audio Decoder".</span></span>



<span data-ttu-id="cef54-118">Сведения о фильтре</span><span class="sxs-lookup"><span data-stu-id="cef54-118">Filter Information</span></span>

<span data-ttu-id="cef54-119">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="cef54-119">Filter Interfaces</span></span>

[<span data-ttu-id="cef54-120">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="cef54-120">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="cef54-121">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="cef54-121">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="cef54-122">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="cef54-122">Input Pin Media Types</span></span>

<span data-ttu-id="cef54-123">В Windows Vista и более поздних версиях фильтр поддерживает следующие входные типы:</span><span class="sxs-lookup"><span data-stu-id="cef54-123">In Windows Vista and later, the filter supports the following input types:</span></span><br/>

-   <span data-ttu-id="cef54-124">**MEDIATYPE \_ Audio**, **медиасубтипе \_ Dolby \_ AC3** (см. Примечание 1).</span><span class="sxs-lookup"><span data-stu-id="cef54-124">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="cef54-125">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="cef54-125">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="cef54-126">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG1Payload**</span><span class="sxs-lookup"><span data-stu-id="cef54-126">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Payload**</span></span>
-   <span data-ttu-id="cef54-127">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="cef54-127">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="cef54-128">**MEDIATYPE \_ \_Зашифрованный \_ DVD-диск**, **медиасубтипе \_ Dolby \_ AC3** (см. Примечание 1).</span><span class="sxs-lookup"><span data-stu-id="cef54-128">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="cef54-129">**MEDIATYPE \_ \_Зашифрованный \_ DVD-диск**, **медиасубтипе \_ DTS** (см. Примечание 2).</span><span class="sxs-lookup"><span data-stu-id="cef54-129">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="cef54-130">**MEDIATYPE \_ \_зашифрованный \_ DVD-диск**, **медиасубтипе \_ DVD \_ лпкм \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="cef54-130">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="cef54-131">**MEDIATYPE \_ \_Зашифрованный \_ DVD-диск**, **медиасубтипе \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="cef54-131">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="cef54-132">**MEDIATYPE \_ MPEG2 \_ PES**, **медиасубтипе \_ Dolby \_ AC3** (см. Примечание 1).</span><span class="sxs-lookup"><span data-stu-id="cef54-132">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="cef54-133">**MEDIATYPE \_ MPEG2 \_ PES**, **медиасубтипе \_ DTS** (см. Примечание 2).</span><span class="sxs-lookup"><span data-stu-id="cef54-133">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="cef54-134">**MEDIATYPE \_ MPEG2 \_ PES**, **медиасубтипе \_ DVD \_ лпкм \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="cef54-134">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="cef54-135">**MEDIATYPE \_ MPEG2 \_ PES**, **медиасубтипе \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="cef54-135">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="cef54-136">**MEDIATYPE \_ Stream**, **медиасубтипе \_ Dolby \_ AC3** (см. Примечание 1).</span><span class="sxs-lookup"><span data-stu-id="cef54-136">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="cef54-137">**MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="cef54-137">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="cef54-138">**MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="cef54-138">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>

<span data-ttu-id="cef54-139">Начиная с Windows 7, фильтр также поддерживает следующие типы входных данных:</span><span class="sxs-lookup"><span data-stu-id="cef54-139">Starting in Windows 7, the filter also supports the following input types:</span></span><br/>

-   <span data-ttu-id="cef54-140">**MEDIATYPE \_ Audio**, **медиасубтипе \_ Dolby \_ Ддплус** (см. Примечание 1).</span><span class="sxs-lookup"><span data-stu-id="cef54-140">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="cef54-141">**MEDIATYPE \_ Audio**, **медиасубтипе \_ DTS2** (см. Примечание 2).</span><span class="sxs-lookup"><span data-stu-id="cef54-141">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DTS2** (See Note 2.)</span></span>
-   <span data-ttu-id="cef54-142">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ DVD \_ лпкм \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="cef54-142">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="cef54-143">**MEDIATYPE \_ Audio**, **медиасубтипе \_ DVM** (см. Примечание 1).</span><span class="sxs-lookup"><span data-stu-id="cef54-143">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVM** (See Note 1.)</span></span>
-   <span data-ttu-id="cef54-144">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="cef54-144">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="cef54-145">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG \_ уровнями гарантии**</span><span class="sxs-lookup"><span data-stu-id="cef54-145">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>
-   <span data-ttu-id="cef54-146">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ MPEG1AudioPayload**</span><span class="sxs-lookup"><span data-stu-id="cef54-146">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1AudioPayload**</span></span>
-   <span data-ttu-id="cef54-147">**MEDIATYPE \_ Audio**, **медиасубтипе \_ RAW \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="cef54-147">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_RAW\_AAC1**</span></span>
-   <span data-ttu-id="cef54-148">**MEDIATYPE \_ Stream**, **медиасубтипе \_ Dolby \_ Ддплус** (см. Примечание 1).</span><span class="sxs-lookup"><span data-stu-id="cef54-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="cef54-149">**MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="cef54-149">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="cef54-150">**MEDIATYPE \_ Stream**, **медиасубтипе \_ MPEG \_ уровнями гарантии**</span><span class="sxs-lookup"><span data-stu-id="cef54-150">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>

<span data-ttu-id="cef54-151">Тип входных данных может динамически изменяться во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="cef54-151">The input type can change dynamically during streaming.</span></span><br/> <span data-ttu-id="cef54-152">Дополнительные сведения об этих типах носителей см. в разделе [**аудио подтипы**](audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="cef54-152">For more information about these media types, see [**Audio Subtypes**](audio-subtypes.md).</span></span><br/>

> [!Note]  
> 1. <span data-ttu-id="cef54-153">Реализация технологий Dolby Digital в корпорации Майкрософт ограничена условиями программы цифрового лицензирования Dolby, используемой приложениями Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="cef54-153">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

<br/>

> [!Note]  
> 2. <span data-ttu-id="cef54-154">Входные системы цифрового кинотеатра (DTS) поддерживают только выходные данные S/PDIF (DTS через S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="cef54-154">For Digital Theater Systems (DTS) input, only S/PDIF output is supported (DTS over S/PDIF).</span></span> <span data-ttu-id="cef54-155">Декодирование звука не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cef54-155">Audio decoding is not supported.</span></span>

<br/>

<span data-ttu-id="cef54-156">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="cef54-156">Input Pin Interfaces</span></span>

[<span data-ttu-id="cef54-157">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="cef54-157">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="cef54-158">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="cef54-158">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="cef54-159">**имеминпутпин**</span><span class="sxs-lookup"><span data-stu-id="cef54-159">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="cef54-160">**ипин**</span><span class="sxs-lookup"><span data-stu-id="cef54-160">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="cef54-161">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="cef54-161">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="cef54-162">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="cef54-162">Output Pin Media Types</span></span>

<span data-ttu-id="cef54-163">В Windows Vista и более поздних версиях фильтр поддерживает следующие типы выходных данных:</span><span class="sxs-lookup"><span data-stu-id="cef54-163">In Windows Vista and later, the filter supports the following output types:</span></span><br/>

-   <span data-ttu-id="cef54-164">**MEDIATYPE \_ Audio**, **медиасубтипе \_ Dolby \_ AC3 \_ SPDIF** (то же, что **ксдатаформат \_ подтип \_ IEC61937 \_ Dolby \_ Digital**)</span><span class="sxs-lookup"><span data-stu-id="cef54-164">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3\_SPDIF** (same as **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL**)</span></span>
-   <span data-ttu-id="cef54-165">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="cef54-165">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="cef54-166">Начиная с Windows 7, фильтр также поддерживает следующие типы выходных данных:</span><span class="sxs-lookup"><span data-stu-id="cef54-166">Starting in Windows 7, the filter also supports the following output types:</span></span><br/>

-   <span data-ttu-id="cef54-167">**MEDIATYPE \_ Audio**, **ксдатаформат \_ подтип \_ IEC61937 \_ DTS**</span><span class="sxs-lookup"><span data-stu-id="cef54-167">**MEDIATYPE\_Audio**, **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS**</span></span>
-   <span data-ttu-id="cef54-168">**MEDIATYPE \_ Аудио**, **медиасубтипе \_ IEEE \_ float**</span><span class="sxs-lookup"><span data-stu-id="cef54-168">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_IEEE\_FLOAT**</span></span>

<span data-ttu-id="cef54-169">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="cef54-169">Output Pin Interfaces</span></span>

[<span data-ttu-id="cef54-170">**имедиасикинг**</span><span class="sxs-lookup"><span data-stu-id="cef54-170">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="cef54-171">**ипин**</span><span class="sxs-lookup"><span data-stu-id="cef54-171">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="cef54-172">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="cef54-172">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="cef54-173">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="cef54-173">Filter CLSID</span></span>

<span data-ttu-id="cef54-174">**Идентификатор CLSID \_ CMPEG2AudDecoderDS** (объявлено в вмкодекдсп. h)</span><span class="sxs-lookup"><span data-stu-id="cef54-174">**CLSID\_CMPEG2AudDecoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="cef54-175">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="cef54-175">Executable</span></span>

<span data-ttu-id="cef54-176">msmpeg2adec.dll</span><span class="sxs-lookup"><span data-stu-id="cef54-176">msmpeg2adec.dll</span></span>

[<span data-ttu-id="cef54-177">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="cef54-177">Merit</span></span>](merit.md)

<span data-ttu-id="cef54-178">**Неуспешный \_ Обычная** — 1</span><span class="sxs-lookup"><span data-stu-id="cef54-178">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="cef54-179">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="cef54-179">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="cef54-180">**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="cef54-180">**CLSID\_LegacyAmFilterCategory**</span></span>



 

> [!Note]  
> <span data-ttu-id="cef54-181">Более ранняя версия документации объявила, что этот фильтр может декодировать "MPEG-2 Audio".</span><span class="sxs-lookup"><span data-stu-id="cef54-181">An earlier version of the documentation stated that this filter can decode "MPEG-2 audio."</span></span> <span data-ttu-id="cef54-182">Фильтр декодирует только обратно совместимые аудио MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="cef54-182">The filter decodes only backward-compatible MPEG-2 audio.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="cef54-183">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cef54-183">Remarks</span></span>

<span data-ttu-id="cef54-184">Потоки Mono всегда декодированы в стерео.</span><span class="sxs-lookup"><span data-stu-id="cef54-184">Mono streams are always decoded to stereo.</span></span>

<span data-ttu-id="cef54-185">Для потоков с конфигурацией каналов из двух или более динамиков декодер выполняет одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="cef54-185">For streams with a channel configuration of two or more speakers, the decoder does one of the following:</span></span>

-   <span data-ttu-id="cef54-186">До шести каналов с использованием стандартной конфигурации динамика 5,1.</span><span class="sxs-lookup"><span data-stu-id="cef54-186">Up-mixes to six channels, using the common 5.1 speaker configuration.</span></span>
-   <span data-ttu-id="cef54-187">Довнмиксес на стерео.</span><span class="sxs-lookup"><span data-stu-id="cef54-187">Downmixes to stereo.</span></span>

<span data-ttu-id="cef54-188">Чтобы выбрать один из этих вариантов, используйте интерфейс [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , чтобы задать свойство [**авдеккоммонаутпутформат**](avdeccommonoutputformat-property.md) перед соединением ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="cef54-188">To select between these two options, use the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to set the [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property, before connecting the pins.</span></span> <span data-ttu-id="cef54-189">Кроме того, когда приложение создает граф фильтра, оно может задать нужный тип носителя для выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="cef54-189">Alternatively, when the application builds the filter graph, it can set the desired media type on the output pin.</span></span>

### <a name="aac-decoding"></a><span data-ttu-id="cef54-190">Декодирование AAC</span><span class="sxs-lookup"><span data-stu-id="cef54-190">AAC Decoding</span></span>

<span data-ttu-id="cef54-191">Для AAC декодер имеет определенные ограничения формата для сжатых входных данных AAC.</span><span class="sxs-lookup"><span data-stu-id="cef54-191">For AAC, the decoder has certain format constraints on the compressed AAC input.</span></span> <span data-ttu-id="cef54-192">Эти ограничения формата аналогичны Media Foundation [**декодера AAC**](../medfound/aac-decoder.md)и описаны в разделе "[**ограничения формата**](../medfound/aac-decoder.md)".</span><span class="sxs-lookup"><span data-stu-id="cef54-192">These format constraints are the same as the Media Foundation [**AAC Decoder**](../medfound/aac-decoder.md), and are documented in the section "[**Format Constraints**](../medfound/aac-decoder.md)".</span></span>

<span data-ttu-id="cef54-193">Декодер DirectShow также принимает различные типы входных данных, чем декодер Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cef54-193">The DirectShow decoder also accepts different input types than the Media Foundation decoder.</span></span> <span data-ttu-id="cef54-194">Декодер DirectShow поддерживает следующие типы входных данных AAC:</span><span class="sxs-lookup"><span data-stu-id="cef54-194">The DirectShow decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="cef54-195">**Медиасубтипе \_ Необработанные \_ AAC1**: RAW AAC, обычно находятся в формате AVI или матроска (. MKV) файлы.</span><span class="sxs-lookup"><span data-stu-id="cef54-195">**MEDIASUBTYPE\_RAW\_AAC1**: Raw AAC, typically found in AVI or Matroska (.MKV) files.</span></span>
-   <span data-ttu-id="cef54-196">**Медиасубтипе \_ MPEG \_ ADTS \_ AAC**: AAC в потоке передачи звуковых данных (ADTS) для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="cef54-196">**MEDIASUBTYPE\_MPEG\_ADTS\_AAC**: AAC in an Audio Data Transport Stream (ADTS) for streaming.</span></span>
-   <span data-ttu-id="cef54-197">**Медиасубтипе \_ MPEG \_ уровнями гарантии**: транспортный поток с уровнем синхронизации (уровнями гарантии) и уровнем мультиплексирования (латм).</span><span class="sxs-lookup"><span data-stu-id="cef54-197">**MEDIASUBTYPE\_MPEG\_LOAS**: Transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span>

<span data-ttu-id="cef54-198">Декодер Media Foundation поддерживает следующие типы входных данных AAC:</span><span class="sxs-lookup"><span data-stu-id="cef54-198">The Media Foundation decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="cef54-199">Мфаудиоформат \_ AAC (то же, что **медиасубтипе \_ MPEG \_ хеаак**) для воспроизведения файла MP4.</span><span class="sxs-lookup"><span data-stu-id="cef54-199">MFAudioFormat\_AAC (same as **MEDIASUBTYPE\_MPEG\_HEAAC**) for MP4 file playback.</span></span>
-   <span data-ttu-id="cef54-200">**Медиасубтипе \_ Необработанный \_ AAC1**.</span><span class="sxs-lookup"><span data-stu-id="cef54-200">**MEDIASUBTYPE\_RAW\_AAC1**.</span></span>

### <a name="property-sets"></a><span data-ttu-id="cef54-201">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="cef54-201">Property Sets</span></span>

<span data-ttu-id="cef54-202">Входной ПИН-код декодера поддерживает следующие наборы свойств через [**икспропертисет**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="cef54-202">The decoder's input pin supports the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="cef54-203">**Набор свойств защиты копирования DVD-дисков**</span><span class="sxs-lookup"><span data-stu-id="cef54-203">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="cef54-204">[**Набор свойств "частота-изменение**](rate-change-property-set.md)".</span><span class="sxs-lookup"><span data-stu-id="cef54-204">[**Rate-Change Property Set**](rate-change-property-set.md).</span></span>

> [!Note]  
> <span data-ttu-id="cef54-205">Начиная с Windows 7, декодер поддерживает режим хитрости через набор свойств Rate-Change.</span><span class="sxs-lookup"><span data-stu-id="cef54-205">Starting in Windows 7, the decoder supports trick mode through the rate-change property set.</span></span> <span data-ttu-id="cef54-206">Он поддерживает скорости воспроизведения в диапазоне \[ 0,501 – 2,0 \] , где 1,0 — это нормальная скорость воспроизведения, а 2,0 — вдвое нормально.</span><span class="sxs-lookup"><span data-stu-id="cef54-206">It supports playback rates in the range \[0.501 – 2.0\], where 1.0 is normal playback rate, and 2.0 is twice the normal rate.</span></span>

 

### <a name="codec-properties"></a><span data-ttu-id="cef54-207">Свойства кодека</span><span class="sxs-lookup"><span data-stu-id="cef54-207">Codec Properties</span></span>

<span data-ttu-id="cef54-208">Входной ПИН-код декодера поддерживает следующие свойства с помощью [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="cef54-208">The decoder's input pin supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="cef54-209">Свойство</span><span class="sxs-lookup"><span data-stu-id="cef54-209">Property</span></span>                                                          | <span data-ttu-id="cef54-210">Требуется</span><span class="sxs-lookup"><span data-stu-id="cef54-210">Requires</span></span>                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="cef54-211">**аваудиочаннелконфиг**</span><span class="sxs-lookup"><span data-stu-id="cef54-211">**AVAudioChannelConfig**</span></span>](avaudiochannelconfig-property.md)     | <span data-ttu-id="cef54-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-212">Windows Vista</span></span>                                            |
| [<span data-ttu-id="cef54-213">**аваудиочаннелкаунт**</span><span class="sxs-lookup"><span data-stu-id="cef54-213">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)       | <span data-ttu-id="cef54-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-214">Windows Vista</span></span>                                            |
| [<span data-ttu-id="cef54-215">**аваудиосамплерате**</span><span class="sxs-lookup"><span data-stu-id="cef54-215">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)           | <span data-ttu-id="cef54-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-216">Windows Vista</span></span>                                            |
| [<span data-ttu-id="cef54-217">**авддсурраундмоде**</span><span class="sxs-lookup"><span data-stu-id="cef54-217">**AVDDSurroundMode**</span></span>](avddsurroundmode-property.md)             | <span data-ttu-id="cef54-218">Только для Windows Vista; не поддерживается в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="cef54-218">Windows Vista only; not supported in Windows 7 or later.</span></span> |
| [<span data-ttu-id="cef54-219">**авдекаудиодуалмоно**</span><span class="sxs-lookup"><span data-stu-id="cef54-219">**AVDecAudioDualMono**</span></span>](avdecaudiodualmono-property.md)         | <span data-ttu-id="cef54-220">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-220">Windows Vista</span></span>                                            |
| [<span data-ttu-id="cef54-221">**авдеккоммонинпутформат**</span><span class="sxs-lookup"><span data-stu-id="cef54-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md) | <span data-ttu-id="cef54-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-222">Windows Vista</span></span>                                            |
| [<span data-ttu-id="cef54-223">**авдеккоммонмеанбитрате**</span><span class="sxs-lookup"><span data-stu-id="cef54-223">**AVDecCommonMeanBitRate**</span></span>](avdeccommonmeanbitrate.md)          | <span data-ttu-id="cef54-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cef54-224">Windows 7</span></span>                                                |



 

<span data-ttu-id="cef54-225">Фильтр поддерживает следующие свойства с помощью [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="cef54-225">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="cef54-226">Свойство</span><span class="sxs-lookup"><span data-stu-id="cef54-226">Property</span></span>                                                                          | <span data-ttu-id="cef54-227">Требуется</span><span class="sxs-lookup"><span data-stu-id="cef54-227">Requires</span></span>      |
|-----------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="cef54-228">**авдекаакдовнмиксмоде**</span><span class="sxs-lookup"><span data-stu-id="cef54-228">**AVDecAACDownmixMode**</span></span>](avdecaacdownmixmode-property.md)                       | <span data-ttu-id="cef54-229">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cef54-229">Windows 7</span></span>     |
| [<span data-ttu-id="cef54-230">**авдекаудиодуалмонорепромоде**</span><span class="sxs-lookup"><span data-stu-id="cef54-230">**AVDecAudioDualMonoReproMode**</span></span>](avdecaudiodualmonorepromode-property.md)       | <span data-ttu-id="cef54-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-231">Windows Vista</span></span> |
| <span data-ttu-id="cef54-232">[**Авдеккоммонаутпутформат**](avdeccommonoutputformat-property.md) (см. Примечание 3).</span><span class="sxs-lookup"><span data-stu-id="cef54-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (See Note 3.)</span></span> | <span data-ttu-id="cef54-233">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-233">Windows Vista</span></span> |
| [<span data-ttu-id="cef54-234">**авдекдддинамикранжескалехигх**</span><span class="sxs-lookup"><span data-stu-id="cef54-234">**AVDecDDDynamicRangeScaleHigh**</span></span>](avdecdddynamicrangescalehigh-property.md)     | <span data-ttu-id="cef54-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-235">Windows Vista</span></span> |
| [<span data-ttu-id="cef54-236">**авдекдддинамикранжескалелов**</span><span class="sxs-lookup"><span data-stu-id="cef54-236">**AVDecDDDynamicRangeScaleLow**</span></span>](avdecdddynamicrangescalelow-property.md)       | <span data-ttu-id="cef54-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-237">Windows Vista</span></span> |
| [<span data-ttu-id="cef54-238">**авдекддоператионалмоде**</span><span class="sxs-lookup"><span data-stu-id="cef54-238">**AVDecDDOperationalMode**</span></span>](avdecddoperationalmode-property.md)                 | <span data-ttu-id="cef54-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-239">Windows Vista</span></span> |
| [<span data-ttu-id="cef54-240">**авдекммксскласс**</span><span class="sxs-lookup"><span data-stu-id="cef54-240">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                    | <span data-ttu-id="cef54-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cef54-241">Windows Vista</span></span> |
| [<span data-ttu-id="cef54-242">**авдсплауднессекуализатион**</span><span class="sxs-lookup"><span data-stu-id="cef54-242">**AVDSPLoudnessEqualization**</span></span>](avdsploudnessequalization-property.md)           | <span data-ttu-id="cef54-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cef54-243">Windows 7</span></span>     |
| [<span data-ttu-id="cef54-244">**авдспспеакерфилл**</span><span class="sxs-lookup"><span data-stu-id="cef54-244">**AVDSPSpeakerFill**</span></span>](avdspspeakerfill-property.md)                             | <span data-ttu-id="cef54-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cef54-245">Windows 7</span></span>     |



 

> [!Note]  
> 3. <span data-ttu-id="cef54-246">Свойство [**авдеккоммонаутпутформат**](avdeccommonoutputformat-property.md) должно быть установлено до подключения выходного ПИН-кода декодера.</span><span class="sxs-lookup"><span data-stu-id="cef54-246">The [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property must be set before the decoder's output pin is connected.</span></span> <span data-ttu-id="cef54-247">В противном случае изменение не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="cef54-247">Otherwise, the change has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cef54-248">Требования</span><span class="sxs-lookup"><span data-stu-id="cef54-248">Requirements</span></span>



| <span data-ttu-id="cef54-249">Требование</span><span class="sxs-lookup"><span data-stu-id="cef54-249">Requirement</span></span> | <span data-ttu-id="cef54-250">Значение</span><span class="sxs-lookup"><span data-stu-id="cef54-250">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef54-251">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cef54-251">Minimum supported client</span></span><br/> | <span data-ttu-id="cef54-252">Windows Vista Домашняя расширенная, Windows Vista Ultimate, \[ только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cef54-252">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cef54-253">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cef54-253">Minimum supported server</span></span><br/> | <span data-ttu-id="cef54-254">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cef54-254">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cef54-255">Header</span><span class="sxs-lookup"><span data-stu-id="cef54-255">Header</span></span><br/>                   | <dl> <span data-ttu-id="cef54-256"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="cef54-256"><dt>Wmcodecdsp.h</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="cef54-257">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cef54-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef54-258">**Звуковые подтипы**</span><span class="sxs-lookup"><span data-stu-id="cef54-258">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="cef54-259">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="cef54-259">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="cef54-260">**Типы носителей DVD**</span><span class="sxs-lookup"><span data-stu-id="cef54-260">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> </dl>

 

 
