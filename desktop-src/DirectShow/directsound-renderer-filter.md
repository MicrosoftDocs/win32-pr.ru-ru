---
description: Фильтр модуля подготовки DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Фильтр модуля подготовки DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139322"
---
# <a name="directsound-renderer-filter"></a><span data-ttu-id="2f219-103">Фильтр модуля подготовки DirectSound</span><span class="sxs-lookup"><span data-stu-id="2f219-103">DirectSound Renderer Filter</span></span>

<span data-ttu-id="2f219-104">Этот фильтр отображает звук с помощью DirectSound.</span><span class="sxs-lookup"><span data-stu-id="2f219-104">This filter renders audio using DirectSound.</span></span> <span data-ttu-id="2f219-105">Этот фильтр сейчас является модулем подготовки звука для звукозаписи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f219-105">This filter is currently the default audio renderer for waveform sound.</span></span>

<span data-ttu-id="2f219-106">В дополнение к базовым возможностям отрисовки звука этот фильтр может обрабатывать вызовы API DirectSound.</span><span class="sxs-lookup"><span data-stu-id="2f219-106">In addition to its basic sound-rendering capabilities, this filter can process DirectSound API calls.</span></span> <span data-ttu-id="2f219-107">Используйте методы [**иамдиректсаунд**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) , чтобы установить и извлечь окно, которое будет выполнять воспроизведение звука.</span><span class="sxs-lookup"><span data-stu-id="2f219-107">Use the [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) methods to set and retrieve the window that will handle the sound playback.</span></span> <span data-ttu-id="2f219-108">Модуль подготовки звука DirectSound является фильтром рендеринга звука по умолчанию для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2f219-108">The DirectSound Audio Renderer is the default audio rendering filter for DirectShow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f219-109">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="2f219-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="2f219-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>Иамаудиорендерерстатс</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>иамклоккславе</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>иамдиректсаунд</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>иамресаурцеконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="2f219-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f219-111">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="2f219-111">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="2f219-112">Основной тип: MEDIATYPE_AudioSubtypes:</span><span class="sxs-lookup"><span data-stu-id="2f219-112">Major Type: MEDIATYPE_AudioSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="2f219-113">MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="2f219-113">MEDIASUBTYPE_PCM</span></span></li>
<li><span data-ttu-id="2f219-114">MEDIASUBTYPE_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="2f219-114">MEDIASUBTYPE_IEEE_FLOAT</span></span></li>
<li><span data-ttu-id="2f219-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="2f219-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span></span></li>
<li><span data-ttu-id="2f219-116">MEDIASUBTYPE_RAW_SPORT</span><span class="sxs-lookup"><span data-stu-id="2f219-116">MEDIASUBTYPE_RAW_SPORT</span></span></li>
<li><span data-ttu-id="2f219-117">MEDIASUBTYPE_SPDIF_TAG_241h</span><span class="sxs-lookup"><span data-stu-id="2f219-117">MEDIASUBTYPE_SPDIF_TAG_241h</span></span></li>
<li><span data-ttu-id="2f219-118">MEDIASUBTYPE_DRM_Audio</span><span class="sxs-lookup"><span data-stu-id="2f219-118">MEDIASUBTYPE_DRM_Audio</span></span></li>
</ul>
<span data-ttu-id="2f219-119">Тип формата: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="2f219-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f219-120">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="2f219-120">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="2f219-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ипинконнектион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="2f219-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f219-122">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="2f219-122">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="2f219-123">Не применяется</span><span class="sxs-lookup"><span data-stu-id="2f219-123">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f219-124">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="2f219-124">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="2f219-125">Не применяется</span><span class="sxs-lookup"><span data-stu-id="2f219-125">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f219-126">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="2f219-126">Filter CLSID</span></span></td>
<td><span data-ttu-id="2f219-127">CLSID_DSoundRender</span><span class="sxs-lookup"><span data-stu-id="2f219-127">CLSID_DSoundRender</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f219-128">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="2f219-128">Property Page CLSID</span></span></td>
<td><span data-ttu-id="2f219-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span><span class="sxs-lookup"><span data-stu-id="2f219-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f219-130">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="2f219-130">Executable</span></span></td>
<td><span data-ttu-id="2f219-131">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="2f219-131">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f219-132"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="2f219-132"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="2f219-133">MERIT_PREFERRED</span><span class="sxs-lookup"><span data-stu-id="2f219-133">MERIT_PREFERRED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f219-134"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="2f219-134"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="2f219-135">CLSID_AudioRendererCategory</span><span class="sxs-lookup"><span data-stu-id="2f219-135">CLSID_AudioRendererCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="2f219-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f219-136">Remarks</span></span>

<span data-ttu-id="2f219-137">Этот фильтр выступает в качестве оболочки для звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="2f219-137">This filter acts as a wrapper for an audio device.</span></span> <span data-ttu-id="2f219-138">Чтобы перечислить звуковые устройства, доступные в системе пользователя, используйте интерфейс [**икреатедевенум**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) с категорией модуля подготовки звука (CLSID \_ аудиорендереркатегори).</span><span class="sxs-lookup"><span data-stu-id="2f219-138">To enumerate the audio devices available on the user's system, use the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface with the audio renderer category (CLSID\_AudioRendererCategory).</span></span> <span data-ttu-id="2f219-139">Для каждого звукового устройства категория модуля подготовки звука содержит два экземпляра фильтра.</span><span class="sxs-lookup"><span data-stu-id="2f219-139">For each audio device, the audio renderer category contains two filter instances.</span></span> <span data-ttu-id="2f219-140">Один из них соответствует модулю рендеринга DirectSound, а второй соответствует фильтру модуля [подготовки звука (Wave)](audio-renderer--waveout--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="2f219-140">One of these corresponds to the DirectSound Renderer, and the other corresponds to the [Audio Renderer (WaveOut)](audio-renderer--waveout--filter.md) filter.</span></span> <span data-ttu-id="2f219-141">Экземпляр DirectSound имеет понятное имя "DirectSound: *DeviceName*,", где *DeviceName* — имя устройства.</span><span class="sxs-lookup"><span data-stu-id="2f219-141">The DirectSound instance has the friendly name "DirectSound: *DeviceName*," where *DeviceName* is the name of the device.</span></span> <span data-ttu-id="2f219-142">Экземпляр Wave имеет понятное имя *DeviceName*.</span><span class="sxs-lookup"><span data-stu-id="2f219-142">The WaveOut instance has the friendly name *DeviceName*.</span></span>

<span data-ttu-id="2f219-143">Категория "модуль подготовки звука" содержит два дополнительных экземпляра фильтра с именами "устройство DirectSound по умолчанию" и "устройство вывода по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="2f219-143">The audio renderer category contains two additional filter instances, named "Default DirectSound Device" and "Default WaveOut Device."</span></span> <span data-ttu-id="2f219-144">Они соответствуют звуковому устройству по умолчанию, выбранному пользователем с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="2f219-144">These correspond to the default sound device, as chosen by the user through the Control Panel.</span></span> <span data-ttu-id="2f219-145">Они фактически сопоставляются с одной из пар, описанных в предыдущем абзаце.</span><span class="sxs-lookup"><span data-stu-id="2f219-145">They are actually mappings to one of the pairs described in the previous paragraph.</span></span> <span data-ttu-id="2f219-146">Например, если в системе есть два звуковых устройства, устройство A и устройство B, категория модуля подготовки звука будет содержать следующее:</span><span class="sxs-lookup"><span data-stu-id="2f219-146">For example, if the system has two audio devices, Device A and Device B, the audio renderer category will contain the following:</span></span>

-   <span data-ttu-id="2f219-147">Устройство A</span><span class="sxs-lookup"><span data-stu-id="2f219-147">Device A</span></span>
-   <span data-ttu-id="2f219-148">DirectSound: устройство а</span><span class="sxs-lookup"><span data-stu-id="2f219-148">DirectSound: Device A</span></span>
-   <span data-ttu-id="2f219-149">Устройство B</span><span class="sxs-lookup"><span data-stu-id="2f219-149">Device B</span></span>
-   <span data-ttu-id="2f219-150">DirectSound: устройство B</span><span class="sxs-lookup"><span data-stu-id="2f219-150">DirectSound: Device B</span></span>
-   <span data-ttu-id="2f219-151">Устройство DirectSound по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2f219-151">Default DirectSound Device</span></span>
-   <span data-ttu-id="2f219-152">Устройство для звука по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2f219-152">Default WaveOut Device</span></span>

<span data-ttu-id="2f219-153">Если пользователь выбрал устройство A в качестве устройства по умолчанию, то "устройство DirectSound по умолчанию" эквивалентно "DirectSound: устройство A,", а "устройство для звукового сигнала по умолчанию" эквивалентно "устройство а".</span><span class="sxs-lookup"><span data-stu-id="2f219-153">If the user selected Device A as the default device, then "Default DirectSound Device" is equivalent to "DirectSound: Device A," and "Default WaveOut Device" is equivalent to "Device A."</span></span> <span data-ttu-id="2f219-154">Если пользователь выбирает устройство б в качестве устройства по умолчанию, эти сопоставления изменятся.</span><span class="sxs-lookup"><span data-stu-id="2f219-154">If the user selects Device B as the default device, these mappings will change.</span></span>

<span data-ttu-id="2f219-155">"Устройству DirectSound по умолчанию" назначена неуспешная версия \_ .</span><span class="sxs-lookup"><span data-stu-id="2f219-155">"Default DirectSound Device" is assigned a merit of MERIT\_PREFERRED.</span></span> <span data-ttu-id="2f219-156">У других есть неуспешные \_ \_ \_ работы.</span><span class="sxs-lookup"><span data-stu-id="2f219-156">The others have merit MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="2f219-157">Поэтому интеллектуальное подключение всегда будет выбирать устройство DirectSound по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f219-157">Therefore, Intelligent Connect will always choose the default DirectSound device.</span></span>

<span data-ttu-id="2f219-158">Фильтр модуля обработки DirectSound поддерживает трехмерный звук через интерфейсы DirectSound **IDirectSound3DBuffer** и **IDirectSound3dListener** .</span><span class="sxs-lookup"><span data-stu-id="2f219-158">The DirectSound Renderer filter supports 3D sound through the DirectSound **IDirectSound3DBuffer** and **IDirectSound3dListener** interfaces.</span></span> <span data-ttu-id="2f219-159">Можно также запросить фильтр для текущих версий этих интерфейсов, **IDirectSound3DBuffer8** и **IDirectSound3dListener8**.</span><span class="sxs-lookup"><span data-stu-id="2f219-159">You can also query the filter for the current versions of these interfaces, **IDirectSound3DBuffer8** and **IDirectSound3dListener8**.</span></span> <span data-ttu-id="2f219-160">Перед вызовом методов для этих интерфейсов запустите граф.</span><span class="sxs-lookup"><span data-stu-id="2f219-160">Run the graph before calling methods on these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f219-161">См. также</span><span class="sxs-lookup"><span data-stu-id="2f219-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f219-162">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="2f219-162">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




