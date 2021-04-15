---
description: Фильтр DVD Navigator
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Фильтр DVD Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53bb1c6f46e3dd846ffccda32fece2c2f04c8992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495144"
---
# <a name="dvd-navigator-filter"></a><span data-ttu-id="be154-103">Фильтр DVD Navigator</span><span class="sxs-lookup"><span data-stu-id="be154-103">DVD Navigator Filter</span></span>

<span data-ttu-id="be154-104">Фильтр "Навигатор DVD" является фильтром источников для диаграммы фильтра воспроизведения DVD-Video.</span><span class="sxs-lookup"><span data-stu-id="be154-104">The DVD Navigator filter is the source filter for a DVD-Video playback filter graph.</span></span> <span data-ttu-id="be154-105">Он открывает все необходимые файлы в DVD-Video томе, выполняет переходы по линейным DVD-Video. VOB-файлам и анализирует полученный поток программы MPEG-2, разбивая поток на три (видео, аудио, субтитры) выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="be154-105">It opens all necessary files in a DVD-Video volume, navigates through the linear DVD-Video .vob files, and parses the resulting MPEG-2 program stream, splitting the stream into three (video, audio, subpicture) output pins.</span></span>

<span data-ttu-id="be154-106">Фильтр навигатора по DVD также реализует интерфейсы [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) и [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , позволяющие приложению воспроизведения DVD управлять DVD-Video воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="be154-106">The DVD Navigator filter also implements the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interfaces that enable a DVD playback application to control DVD-Video playback.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="be154-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="be154-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="be154-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>ифилесаурцефилтер</strong></a>, <strong>испеЦифипропертипажес</strong></span><span class="sxs-lookup"><span data-stu-id="be154-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be154-109">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="be154-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="be154-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="be154-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be154-111">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="be154-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="be154-112">Не применяется</span><span class="sxs-lookup"><span data-stu-id="be154-112">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be154-113">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="be154-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="be154-114">Базовые типы:</span><span class="sxs-lookup"><span data-stu-id="be154-114">Base types:</span></span><br/>
<ul>
<li><span data-ttu-id="be154-115">Видео: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="be154-115">Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="be154-116">Аудио: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="be154-116">Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="be154-117">Подизображение: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="be154-117">Subpicture: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="be154-118">Расширенные типы:</span><span class="sxs-lookup"><span data-stu-id="be154-118">Extended types:</span></span><br/> <span data-ttu-id="be154-119">Видео:</span><span class="sxs-lookup"><span data-stu-id="be154-119">Video:</span></span><br/>
<ul>
<li><span data-ttu-id="be154-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="be154-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="be154-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="be154-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="be154-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="be154-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
</ul>
<span data-ttu-id="be154-123">Звук:</span><span class="sxs-lookup"><span data-stu-id="be154-123">Audio:</span></span><br/>
<ul>
<li><span data-ttu-id="be154-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="be154-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="be154-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="be154-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="be154-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="be154-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
</ul>
<span data-ttu-id="be154-127">Субтитров</span><span class="sxs-lookup"><span data-stu-id="be154-127">Subpicture:</span></span><br/>
<ul>
<li><span data-ttu-id="be154-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="be154-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="be154-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="be154-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="be154-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="be154-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="be154-131">Чтобы включить расширенные типы, вызовите метод <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2:: SetOption</strong></a> и установите для свойства</span><span class="sxs-lookup"><span data-stu-id="be154-131">To enable the extended types, call <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> and set the</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be154-132">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="be154-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="be154-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="be154-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be154-134">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="be154-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="be154-135">CLSID_DVDNavigator</span><span class="sxs-lookup"><span data-stu-id="be154-135">CLSID_DVDNavigator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be154-136">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="be154-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="be154-137">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="be154-137">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be154-138">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="be154-138">Executable</span></span></td>
<td><span data-ttu-id="be154-139">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="be154-139">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be154-140"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="be154-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="be154-141">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="be154-141">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be154-142"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="be154-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="be154-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="be154-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="be154-144">См. также</span><span class="sxs-lookup"><span data-stu-id="be154-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be154-145">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="be154-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="be154-146">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="be154-146">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




