---
description: Фильтр модуля подготовки звука (звук)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Фильтр модуля подготовки звука (звук)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682312"
---
# <a name="audio-renderer-waveout-filter"></a><span data-ttu-id="3480f-103">Фильтр модуля подготовки звука (звук)</span><span class="sxs-lookup"><span data-stu-id="3480f-103">Audio Renderer (WaveOut) Filter</span></span>

<span data-ttu-id="3480f-104">Этот фильтр использует \* API-интерфейс для вывода звуковых сигналов.</span><span class="sxs-lookup"><span data-stu-id="3480f-104">This filter uses the waveOut\* API to render waveform audio.</span></span> <span data-ttu-id="3480f-105">Однако [Фильтр рендеринга DirectSound](directsound-renderer-filter.md) предоставляет те же функциональные возможности, что и DirectSound.</span><span class="sxs-lookup"><span data-stu-id="3480f-105">However, the [DirectSound Renderer Filter](directsound-renderer-filter.md) provides the same functionality using DirectSound.</span></span> <span data-ttu-id="3480f-106">По умолчанию диспетчер графов фильтров использует модуль подготовки DirectSound вместо этого фильтра.</span><span class="sxs-lookup"><span data-stu-id="3480f-106">By default, the Filter Graph Manager uses the DirectSound Renderer instead of this filter.</span></span> <span data-ttu-id="3480f-107">Микширование звука отключено в модуле подготовки аудио, поэтому если во время воспроизведения необходимо смешивать несколько звуковых потоков, используйте модуль подготовки DirectSound.</span><span class="sxs-lookup"><span data-stu-id="3480f-107">Audio mixing is disabled in the waveOut Audio Renderer, so if you need to mix multiple audio streams during playback, use the DirectSound renderer.</span></span>

<span data-ttu-id="3480f-108">Этот фильтр не проверяет подтип аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="3480f-108">This filter does not check the audio stream's subtype.</span></span> <span data-ttu-id="3480f-109">Структура [**вавеформат**](/windows/win32/api/mmreg/ns-mmreg-waveformat) или [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , переданная в формате, содержит сведения, необходимые для соединения.</span><span class="sxs-lookup"><span data-stu-id="3480f-109">The [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) or [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure passed in the format contains the information needed for the connection.</span></span>

<span data-ttu-id="3480f-110">Этот фильтр поддерживает ряд частот выборки, которые зависят от звукового драйвера.</span><span class="sxs-lookup"><span data-stu-id="3480f-110">This filter supports a range of sample rates that depends on the audio driver.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3480f-111">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="3480f-111">Filter Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="3480f-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>иамаудиорендерерстатс</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span></span></li>
<li><span data-ttu-id="3480f-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>иамклоккславе</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span></span></li>
<li><span data-ttu-id="3480f-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>иамдиректсаунд</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span></span></li>
<li><span data-ttu-id="3480f-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>иамресаурцеконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span></span></li>
<li><span data-ttu-id="3480f-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="3480f-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>ибасикаудио</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span></span></li>
<li><span data-ttu-id="3480f-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="3480f-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="3480f-120">IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3480f-120">IPersistPropertyBag</span></span></li>
<li><span data-ttu-id="3480f-121">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="3480f-121">IPersistStream</span></span></li>
<li><span data-ttu-id="3480f-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="3480f-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>иреференцеклокк</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3480f-124">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="3480f-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="3480f-125"><strong>MEDIATYPE_Audio</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-125"><strong>MEDIATYPE_Audio</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3480f-126">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="3480f-126">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="3480f-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="3480f-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="3480f-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="3480f-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3480f-130">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="3480f-130">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="3480f-131">Не применяется</span><span class="sxs-lookup"><span data-stu-id="3480f-131">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3480f-132">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="3480f-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="3480f-133">Не применяется</span><span class="sxs-lookup"><span data-stu-id="3480f-133">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3480f-134">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="3480f-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="3480f-135"><strong>CLSID_AudioRender</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-135"><strong>CLSID_AudioRender</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3480f-136">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="3480f-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="3480f-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3480f-138">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="3480f-138">Executable</span></span></td>
<td><span data-ttu-id="3480f-139">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="3480f-139">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3480f-140"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="3480f-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="3480f-141"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-141"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3480f-142"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="3480f-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="3480f-143"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3480f-143"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3480f-144">См. также</span><span class="sxs-lookup"><span data-stu-id="3480f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3480f-145">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="3480f-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
