---
description: Фильтр оболочки ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Фильтр оболочки ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682319"
---
# <a name="acm-wrapper-filter"></a><span data-ttu-id="35c22-103">Фильтр оболочки ACM</span><span class="sxs-lookup"><span data-stu-id="35c22-103">ACM Wrapper Filter</span></span>

<span data-ttu-id="35c22-104">Фильтр оболочки ACM включает кодеки (ACM) для подключения к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="35c22-104">The ACM Wrapper filter enables Audio Compression Manager (ACM) codecs to join a filter graph.</span></span> <span data-ttu-id="35c22-105">Он может действовать как фильтр распаковки или как фильтр сжатия.</span><span class="sxs-lookup"><span data-stu-id="35c22-105">It can act either as a decompression filter or as a compression filter.</span></span>

<span data-ttu-id="35c22-106">В качестве фильтра распаковки оболочка ACM отображается в категории «фильтры DirectShow» (CLSID \_ легациамфилтеркатегори) и имеет нештатную подмножество \_ .</span><span class="sxs-lookup"><span data-stu-id="35c22-106">As a decompression filter, the ACM Wrapper appears in the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory) and has a merit of MERIT\_NORMAL.</span></span> <span data-ttu-id="35c22-107">Тип носителя подключения для входного ПИН-кода определяет, какой кодек использует фильтр.</span><span class="sxs-lookup"><span data-stu-id="35c22-107">The connection media type on the input pin determines which codec the filter uses.</span></span> <span data-ttu-id="35c22-108">Как правило, приложению не нужно добавлять фильтр к графу фильтра; При необходимости он автоматически извлекается диспетчером графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="35c22-108">Typically, the application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span> <span data-ttu-id="35c22-109">Распаковка применяется только к звуку PCM.</span><span class="sxs-lookup"><span data-stu-id="35c22-109">Decompression is only to PCM audio.</span></span>

<span data-ttu-id="35c22-110">Как фильтр сжатия, оболочка ACM отображается в категории "звуковые компрессоры" (CLSID \_ аудиокомпрессоркатегори) и имеет недостаточное количество \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="35c22-110">As a compression filter, the ACM Wrapper appears in the "Audio Compressors" category (CLSID\_AudioCompressorCategory) and has a merit of MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="35c22-111">Каждый кодек отображается как отдельный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="35c22-111">Each codec appears as a separate instance.</span></span> <span data-ttu-id="35c22-112">Для сжатия нельзя напрямую создать фильтр с помощью CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="35c22-112">For compression, you cannot directly create the filter with CoCreateInstance.</span></span> <span data-ttu-id="35c22-113">Вместо этого необходимо использовать перечислитель системных устройств.</span><span class="sxs-lookup"><span data-stu-id="35c22-113">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="35c22-114">Дополнительные сведения см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="35c22-114">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35c22-115">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="35c22-115">Filter interfaces</span></span></td>
<td><span data-ttu-id="35c22-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, IPersist, IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="35c22-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35c22-117">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="35c22-117">Input pin media types</span></span></td>
<td><span data-ttu-id="35c22-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="35c22-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35c22-119">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="35c22-119">Input pin interfaces</span></span></td>
<td><span data-ttu-id="35c22-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="35c22-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35c22-121">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="35c22-121">Output pin media types</span></span></td>
<td><span data-ttu-id="35c22-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx. возможны следующие сочетания следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="35c22-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Any combination of the following are possible:</span></span><br/>
<ul>
<li><span data-ttu-id="35c22-123">Выборок в секунду (кГц): 44,1, 22,05, 11,025 или 8,0.</span><span class="sxs-lookup"><span data-stu-id="35c22-123">Samples per second (kHz): 44.1, 22.05, 11.025, or 8.0.</span></span></li>
<li><span data-ttu-id="35c22-124">Каналы: стерео или Mono.</span><span class="sxs-lookup"><span data-stu-id="35c22-124">Channels: Stereo or mono.</span></span></li>
<li><span data-ttu-id="35c22-125">Бит на выборку: 8 или 16.</span><span class="sxs-lookup"><span data-stu-id="35c22-125">Bits per sample: 8 or 16.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35c22-126">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="35c22-126">Output pin interfaces</span></span></td>
<td><span data-ttu-id="35c22-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>Иамстреамконфиг</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="35c22-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35c22-128">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="35c22-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="35c22-129">CLSID_ACMWrapper</span><span class="sxs-lookup"><span data-stu-id="35c22-129">CLSID_ACMWrapper</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35c22-130">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="35c22-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="35c22-131">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="35c22-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35c22-132">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="35c22-132">Executable</span></span></td>
<td><span data-ttu-id="35c22-133">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="35c22-133">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35c22-134"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="35c22-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="35c22-135">MERIT_NORMAL или MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="35c22-135">MERIT_NORMAL or MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35c22-136"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="35c22-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="35c22-137">CLSID_LegacyAmFilterCategory или CLSID_AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="35c22-137">CLSID_LegacyAmFilterCategory or CLSID_AudioCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="35c22-138">См. также</span><span class="sxs-lookup"><span data-stu-id="35c22-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35c22-139">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="35c22-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




