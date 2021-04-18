---
description: Возможности работы с аудио
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Возможности работы с аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538048"
---
# <a name="audio-capabilities"></a><span data-ttu-id="98aaf-103">Возможности работы с аудио</span><span class="sxs-lookup"><span data-stu-id="98aaf-103">Audio Capabilities</span></span>

<span data-ttu-id="98aaf-104">Для возможностей работы с аудио [**иамстреамконфиг:: жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) возвращает массив пар " [**\_ \_ тип мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) " и " [**аудиоразъемы" для \_ \_ конфигурации \_ аудио потока**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="98aaf-104">For audio capabilities, [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns an array of pairs of [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) and [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structures.</span></span> <span data-ttu-id="98aaf-105">Как и в видео, его можно использовать для предоставления всех видов звуковых возможностей на ПИН-коде, например для скорости передачи данных и того, поддерживает ли он моно или стерео.</span><span class="sxs-lookup"><span data-stu-id="98aaf-105">As with video, you can use this to expose all kinds of audio capabilities on the pin, such as data rate and whether it supports mono or stereo.</span></span>

<span data-ttu-id="98aaf-106">Примеры для видео, относящиеся к Жетстреамкапс, см. в разделе [возможности видео](video-capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="98aaf-106">For video-related examples relating to GetStreamCaps, see [Video Capabilities](video-capabilities.md).</span></span>

<span data-ttu-id="98aaf-107">Предположим, что вы поддерживаете формат волновой модуляции (PCM) (как представлено структурой [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) ) при частоте выборки 11 025, 22 050 и 44 100 в секунду, все 8-или 16-битные моно или стерео.</span><span class="sxs-lookup"><span data-stu-id="98aaf-107">Suppose you support pulse code modulation (PCM) wave format (as represented by the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure) at sampling rates of 11,025, 22,050, and 44,100 samples per second, all at 8- or 16-bit mono or stereo.</span></span> <span data-ttu-id="98aaf-108">В этом случае вы предложит две пары структур.</span><span class="sxs-lookup"><span data-stu-id="98aaf-108">In this case, you would offer two pairs of structures.</span></span> <span data-ttu-id="98aaf-109">Первая пара будет иметь структуру возможностей **с \_ \_ \_ заглушками конфигурации аудио потока** , что означает, что вы можете поддерживать не менее 11 025 для максимум 22 050 выборок в секунду с гранулярностью в 11 025 выборок в секунду (степень детализации — разница между поддерживаемыми значениями); 8-разрядный минимум 16-разрядных максимальных бит на выборку с детализацией по 8 битам на выборку, а также по одному каналу и максимуму на два канала.</span><span class="sxs-lookup"><span data-stu-id="98aaf-109">The first pair would have an **AUDIO\_STREAM\_CONFIG\_CAPS** capability structure saying you support a minimum of 11,025 to a maximum of 22,050 samples per second with a granularity of 11,025 samples per second (granularity is the difference between supported values); an 8-bit minimum to a 16-bit maximum bits per sample with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="98aaf-110">Первый тип носителя пары будет иметь формат PCM по умолчанию в этом диапазоне, например 22 килохертз (кГц), 16-разрядный стерео.</span><span class="sxs-lookup"><span data-stu-id="98aaf-110">The first pair's media type would be your default PCM format in that range, perhaps 22 kilohertz (kHz), 16-bit stereo.</span></span> <span data-ttu-id="98aaf-111">Вторая пара будет возможной возможностью, отображающей 44 100 для минимального и максимального количества выборок в секунду; 8-разрядный (минимальный) и 16-разрядный (максимум) бит на выборку с детализацией по 8 бит на выборку; и 1-канальное минимальное и 2-канальное.</span><span class="sxs-lookup"><span data-stu-id="98aaf-111">Your second pair would be a capability showing 44,100 for both minimum and maximum samples per second; 8-bit (minimum) and 16-bit (maximum) bits per sample, with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="98aaf-112">В качестве типа носителя используется формат по умолчанию 44 кГц, возможно, 16-разрядный стереосистема 44 кГц.</span><span class="sxs-lookup"><span data-stu-id="98aaf-112">The media type would be your default 44 kHz format, perhaps 44 kHz 16-bit stereo.</span></span>

<span data-ttu-id="98aaf-113">Если поддерживаются форматы волн не из PCM, тип мультимедиа, возвращаемый этим методом, может показывать, какие форматы, отличные от PCM, которые поддерживаются (с частотой выборки по умолчанию, скоростью и каналами), а структура возможностей, сопровождающая этот тип носителя, может описать, какие другие тарифы выборки, скорость и каналы поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="98aaf-113">If you support non-PCM wave formats, the media type returned by this method can show which non-PCM formats you support (with a default sample rate, bit rate, and channels) and the capabilities structure accompanying that media type can describe which other sample rates, bit rates, and channels you support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98aaf-114">См. также</span><span class="sxs-lookup"><span data-stu-id="98aaf-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98aaf-115">Предоставление форматов записи и сжатия</span><span class="sxs-lookup"><span data-stu-id="98aaf-115">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
