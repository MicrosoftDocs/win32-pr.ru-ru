---
description: Фильтр рисования AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Фильтр рисования AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6d6b318b7a1f7e762fc0806186114fb9256f5c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139439"
---
# <a name="avi-draw-filter"></a><span data-ttu-id="81792-103">Фильтр рисования AVI</span><span class="sxs-lookup"><span data-stu-id="81792-103">AVI Draw Filter</span></span>

<span data-ttu-id="81792-104">Фильтр рисования AVI автоматически извлекается в граф воспроизведения вместо [распаковки AVI](avi-decompressor-filter.md) при выводе видео во внешний монитор телевизора NTSC.</span><span class="sxs-lookup"><span data-stu-id="81792-104">The AVI Draw filter is pulled automatically into a playback graph instead of the [AVI Decompressor](avi-decompressor-filter.md) when video is being output to an external NTSC television monitor.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81792-105">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="81792-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="81792-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="81792-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81792-107">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="81792-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="81792-108">Основной тип: MEDIATYPE_VideoSubtypes:</span><span class="sxs-lookup"><span data-stu-id="81792-108">Major Type: MEDIATYPE_VideoSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="81792-109">MEDIASUBTYPE_MJPG</span><span class="sxs-lookup"><span data-stu-id="81792-109">MEDIASUBTYPE_MJPG</span></span></li>
<li><span data-ttu-id="81792-110">MEDIASUBTYPE_TVMJ</span><span class="sxs-lookup"><span data-stu-id="81792-110">MEDIASUBTYPE_TVMJ</span></span></li>
<li><span data-ttu-id="81792-111">MEDIASUBTYPE_WAKE</span><span class="sxs-lookup"><span data-stu-id="81792-111">MEDIASUBTYPE_WAKE</span></span></li>
<li><span data-ttu-id="81792-112">MEDIASUBTYPE_CFCC</span><span class="sxs-lookup"><span data-stu-id="81792-112">MEDIASUBTYPE_CFCC</span></span></li>
<li><span data-ttu-id="81792-113">MEDIASUBTYPE_IJPG</span><span class="sxs-lookup"><span data-stu-id="81792-113">MEDIASUBTYPE_IJPG</span></span></li>
<li><span data-ttu-id="81792-114">MEDIASUBTYPE_Plum</span><span class="sxs-lookup"><span data-stu-id="81792-114">MEDIASUBTYPE_Plum</span></span></li>
<li><span data-ttu-id="81792-115">MEDIASUBTYPE_DVCS</span><span class="sxs-lookup"><span data-stu-id="81792-115">MEDIASUBTYPE_DVCS</span></span></li>
<li><span data-ttu-id="81792-116">MEDIASUBTYPE_DVSD</span><span class="sxs-lookup"><span data-stu-id="81792-116">MEDIASUBTYPE_DVSD</span></span></li>
<li><span data-ttu-id="81792-117">MEDIASUBTYPE_MDVF</span><span class="sxs-lookup"><span data-stu-id="81792-117">MEDIASUBTYPE_MDVF</span></span></li>
<li><span data-ttu-id="81792-118">Тип формата: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="81792-118">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81792-119">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="81792-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="81792-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="81792-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81792-121">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="81792-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="81792-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="81792-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81792-123">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="81792-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="81792-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>иоверлайнотифи</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="81792-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81792-125">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="81792-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="81792-126">CLSID_AVIDraw</span><span class="sxs-lookup"><span data-stu-id="81792-126">CLSID_AVIDraw</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81792-127">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="81792-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="81792-128">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="81792-128">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81792-129">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="81792-129">Executable</span></span></td>
<td><span data-ttu-id="81792-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="81792-130">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81792-131"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="81792-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="81792-132">MERIT_NORMAL + 100</span><span class="sxs-lookup"><span data-stu-id="81792-132">MERIT_NORMAL + 100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81792-133"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="81792-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="81792-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="81792-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="81792-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81792-135">Remarks</span></span>

<span data-ttu-id="81792-136">Поскольку фильтр рисования AVI и [фильтр записи VFW](vfw-capture-filter.md) подключаются к одному и тому же оборудованию, они не могут находиться в одном графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="81792-136">Since the AVI Draw filter and the [VFW Capture Filter](vfw-capture-filter.md) both connect to the same hardware, they cannot be in the same filter graph.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81792-137">См. также</span><span class="sxs-lookup"><span data-stu-id="81792-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81792-138">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="81792-138">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




