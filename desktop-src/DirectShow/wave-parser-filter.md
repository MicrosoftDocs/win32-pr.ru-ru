---
description: Фильтр синтаксического анализатора волн
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Фильтр синтаксического анализатора волн
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664695"
---
# <a name="wave-parser-filter"></a><span data-ttu-id="a7507-103">Фильтр синтаксического анализатора волн</span><span class="sxs-lookup"><span data-stu-id="a7507-103">WAVE Parser Filter</span></span>

<span data-ttu-id="a7507-104">Фильтр средства синтаксического анализа WAVE анализирует звуковые данные в формате WAV, Au или AIF.</span><span class="sxs-lookup"><span data-stu-id="a7507-104">The WAVE Parser filter parses WAV-format audio data from .wav, .au, or .aif files.</span></span> <span data-ttu-id="a7507-105">Вышестоящий фильтр должен быть фильтром [источника асинхронного файла](file-source--async--filter.md) , фильтром [источников URL-адресов](file-source--url--filter.md) или совместимым сторонним фильтром исходного кода, который содержит звуковые данные WAV.</span><span class="sxs-lookup"><span data-stu-id="a7507-105">The upstream filter must be the [Async File Source](file-source--async--filter.md) filter, [URL File Source](file-source--url--filter.md) filter, or a compatible third-party asynchronous source filter that contains WAV audio data.</span></span> <span data-ttu-id="a7507-106">Поток вывода — это звуковые данные, которые можно напрямую подключаться к фильтру рендеринга аудио или к промежуточному фильтру преобразования.</span><span class="sxs-lookup"><span data-stu-id="a7507-106">The output stream is audio data, which you can connect directly to an audio rendering filter or to an intervening audio transform filter.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7507-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="a7507-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="a7507-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Иаммедиаконтент</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>иперсистмедиапропертибаг</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7507-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7507-109">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="a7507-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="a7507-110">Основной тип: MEDIATYPE_StreamThe следующие подтипы являются допустимыми:</span><span class="sxs-lookup"><span data-stu-id="a7507-110">Major type: MEDIATYPE_StreamThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="a7507-111">MEDIASUBTYPE_AIFF</span><span class="sxs-lookup"><span data-stu-id="a7507-111">MEDIASUBTYPE_AIFF</span></span></li>
<li><span data-ttu-id="a7507-112">MEDIASUBTYPE_AU</span><span class="sxs-lookup"><span data-stu-id="a7507-112">MEDIASUBTYPE_AU</span></span></li>
<li><span data-ttu-id="a7507-113">MEDIASUBTYPE_WAVE</span><span class="sxs-lookup"><span data-stu-id="a7507-113">MEDIASUBTYPE_WAVE</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7507-114">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="a7507-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="a7507-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7507-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7507-116">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="a7507-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="a7507-117">Основной тип: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM или другой тип сжатия.</span><span class="sxs-lookup"><span data-stu-id="a7507-117">Major type: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM or other compression type.</span></span> <span data-ttu-id="a7507-118">(См. раздел <a href="audio-subtypes.md"><strong>звуковые подтипы</strong></a>.)</span><span class="sxs-lookup"><span data-stu-id="a7507-118">(See <a href="audio-subtypes.md"><strong>Audio Subtypes</strong></a>.)</span></span><br/> <span data-ttu-id="a7507-119">Тип формата: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="a7507-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7507-120">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="a7507-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="a7507-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>имедиасикинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7507-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7507-122">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="a7507-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="a7507-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span><span class="sxs-lookup"><span data-stu-id="a7507-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7507-124">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="a7507-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="a7507-125">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="a7507-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7507-126">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="a7507-126">Executable</span></span></td>
<td><span data-ttu-id="a7507-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="a7507-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7507-128"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="a7507-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="a7507-129">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="a7507-129">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7507-130"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="a7507-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="a7507-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a7507-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a7507-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7507-132">Remarks</span></span>

<span data-ttu-id="a7507-133">Этот фильтр поддерживает следующие типы файлов:</span><span class="sxs-lookup"><span data-stu-id="a7507-133">This filter supports the following file types:</span></span>

-   <span data-ttu-id="a7507-134">ВОЛНА (. wav)</span><span class="sxs-lookup"><span data-stu-id="a7507-134">WAVE (.wav)</span></span>
-   <span data-ttu-id="a7507-135">AIFF и AIFF-C (. AIF)</span><span class="sxs-lookup"><span data-stu-id="a7507-135">AIFF and AIFF-C (.aif)</span></span>
-   <span data-ttu-id="a7507-136">AU (Au)</span><span class="sxs-lookup"><span data-stu-id="a7507-136">AU (.au)</span></span>

<span data-ttu-id="a7507-137">Однако он имеет следующие ограничения в аудио формате:</span><span class="sxs-lookup"><span data-stu-id="a7507-137">However, it has the following limitations on the audio format:</span></span>

-   <span data-ttu-id="a7507-138">Звук должен быть 8-или 16-разрядным линейным PCM.</span><span class="sxs-lookup"><span data-stu-id="a7507-138">The audio must be 8-bit or 16-bit linear PCM.</span></span>
-   <span data-ttu-id="a7507-139">Для файлов AIFF-C звук должен быть распакован, в порядке байтов с обратным порядком (тип сжатия "NONE").</span><span class="sxs-lookup"><span data-stu-id="a7507-139">For AIFF-C files, the audio must be uncompressed, in big-endian byte order (compression type 'NONE').</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7507-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a7507-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7507-141">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="a7507-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




