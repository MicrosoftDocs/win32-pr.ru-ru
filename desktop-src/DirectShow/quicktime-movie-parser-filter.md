---
description: Фильтр синтаксического анализатора QuickTime Movie
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Фильтр синтаксического анализатора QuickTime Movie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341952"
---
# <a name="quicktime-movie-parser-filter"></a><span data-ttu-id="124ba-103">Фильтр синтаксического анализатора QuickTime Movie</span><span class="sxs-lookup"><span data-stu-id="124ba-103">QuickTime Movie Parser Filter</span></span>

<span data-ttu-id="124ba-104">Этот компонент был удален из Windows Vista и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="124ba-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="124ba-105">Он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="124ba-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="124ba-106">Фильтр синтаксического анализатора QuickTime Movie разделяет данные® Apple® QuickTime в аудио и видео потоки.</span><span class="sxs-lookup"><span data-stu-id="124ba-106">The QuickTime Movie Parser filter splits Apple® QuickTime® data into audio and video streams.</span></span> <span data-ttu-id="124ba-107">Он поддерживает QuickTime 2,0 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="124ba-107">It supports QuickTime 2.0 and earlier.</span></span> <span data-ttu-id="124ba-108">Входной ПИН-код подключается к фильтру источника, такому как фильтр [источника асинхронного файла](file-source--async--filter.md) или фильтр [источника файла URL-адреса](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="124ba-108">The input pin connects to a source filter such as the [Async File Source](file-source--async--filter.md) filter or the [URL File Source](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="124ba-109">Средство синтаксического анализа использует фильтр [AVI распаковки](avi-decompressor-filter.md) или [Qt](qt-decompressor-filter.md) для распаковки файлов QuickTime.</span><span class="sxs-lookup"><span data-stu-id="124ba-109">The Parser uses the [AVI Decompressor](avi-decompressor-filter.md) or [QT Decompressor](qt-decompressor-filter.md) filter to decompress QuickTime files.</span></span> <span data-ttu-id="124ba-110">Фильтр создает один выходной ПИН-код для потока видео и один выходной ПИН-код для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="124ba-110">The filter creates one output pin for the video stream and one output pin for the audio stream.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="124ba-111">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="124ba-111">Filter Interfaces</span></span></td>
<td><span data-ttu-id="124ba-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Иаммедиаконтент</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="124ba-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="124ba-113">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="124ba-113">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="124ba-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span><span class="sxs-lookup"><span data-stu-id="124ba-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="124ba-115">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="124ba-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="124ba-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="124ba-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="124ba-117">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="124ba-117">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="124ba-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="124ba-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></li>
<li><span data-ttu-id="124ba-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="124ba-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="124ba-120">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="124ba-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="124ba-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="124ba-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="124ba-122">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="124ba-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="124ba-123">CLSID_QuickTimeParser</span><span class="sxs-lookup"><span data-stu-id="124ba-123">CLSID_QuickTimeParser</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="124ba-124">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="124ba-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="124ba-125">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="124ba-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="124ba-126">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="124ba-126">Executable</span></span></td>
<td><span data-ttu-id="124ba-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="124ba-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="124ba-128"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="124ba-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="124ba-129">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="124ba-129">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="124ba-130"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="124ba-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="124ba-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="124ba-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="124ba-132">См. также</span><span class="sxs-lookup"><span data-stu-id="124ba-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="124ba-133">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="124ba-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



