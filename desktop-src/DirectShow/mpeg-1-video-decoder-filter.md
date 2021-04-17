---
description: Фильтр видеодекодера MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Фильтр видеодекодера MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7f48e441226dee33ef949219e8008e15c9d711
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682196"
---
# <a name="mpeg-1-video-decoder-filter"></a><span data-ttu-id="6c122-103">Фильтр видеодекодера MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6c122-103">MPEG-1 Video Decoder Filter</span></span>

<span data-ttu-id="6c122-104">Декодирует видео MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="6c122-104">Decodes MPEG-1 video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c122-105">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="6c122-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="6c122-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <strong>испеЦифипропертипажес</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c122-107">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="6c122-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="6c122-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="6c122-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span></span><br/> <span data-ttu-id="6c122-109">Допустимы следующие подтипы:</span><span class="sxs-lookup"><span data-stu-id="6c122-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="6c122-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span></span></li>
<li><span data-ttu-id="6c122-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c122-112">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="6c122-112">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="6c122-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>имеминпутпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="6c122-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c122-114">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="6c122-114">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="6c122-115">Основной тип: <strong>MEDIATYPE_Video</strong>,</span><span class="sxs-lookup"><span data-stu-id="6c122-115">Major type: <strong>MEDIATYPE_Video</strong>,</span></span><br/> <span data-ttu-id="6c122-116">Тип формата: <strong>FORMAT_VideoInfo</strong> или <strong>FORMAT_VideoInfo2</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-116">Format type: <strong>FORMAT_VideoInfo</strong> or <strong>FORMAT_VideoInfo2</strong></span></span><br/> <span data-ttu-id="6c122-117">Подтипы</span><span class="sxs-lookup"><span data-stu-id="6c122-117">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="6c122-118"><strong>MEDIASUBTYPE_RGB24</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-118"><strong>MEDIASUBTYPE_RGB24</strong></span></span></li>
<li><span data-ttu-id="6c122-119"><strong>MEDIASUBTYPE_RGB32</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-119"><strong>MEDIASUBTYPE_RGB32</strong></span></span></li>
<li><span data-ttu-id="6c122-120"><strong>MEDIASUBTYPE_RGB8</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-120"><strong>MEDIASUBTYPE_RGB8</strong></span></span></li>
<li><span data-ttu-id="6c122-121"><strong>MEDIASUBTYPE_RGB555</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-121"><strong>MEDIASUBTYPE_RGB555</strong></span></span></li>
<li><span data-ttu-id="6c122-122"><strong>MEDIASUBTYPE_RGB565</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-122"><strong>MEDIASUBTYPE_RGB565</strong></span></span></li>
<li><span data-ttu-id="6c122-123"><strong>MEDIASUBTYPE_UYVY</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-123"><strong>MEDIASUBTYPE_UYVY</strong></span></span></li>
<li><span data-ttu-id="6c122-124"><strong>MEDIASUBTYPE_Y41P</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-124"><strong>MEDIASUBTYPE_Y41P</strong></span></span></li>
<li><span data-ttu-id="6c122-125"><strong>MEDIASUBTYPE_YUY2</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-125"><strong>MEDIASUBTYPE_YUY2</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c122-126">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="6c122-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="6c122-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="6c122-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c122-128">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="6c122-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="6c122-129"><strong>CLSID_CMpegVideoCodec</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-129"><strong>CLSID_CMpegVideoCodec</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c122-130">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="6c122-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="6c122-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span><span class="sxs-lookup"><span data-stu-id="6c122-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c122-132">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="6c122-132">Executable</span></span></td>
<td><span data-ttu-id="6c122-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="6c122-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c122-134"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="6c122-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="6c122-135">0x40000001</span><span class="sxs-lookup"><span data-stu-id="6c122-135">0x40000001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c122-136"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="6c122-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="6c122-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="6c122-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="6c122-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c122-138">Remarks</span></span>

<span data-ttu-id="6c122-139">Этот фильтр может декодировать в поверхность DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="6c122-139">This filter can decode into a DirectDraw Surface.</span></span> <span data-ttu-id="6c122-140">Фильтр использует технологию MMX, если компьютер поддерживает технологию MMX.</span><span class="sxs-lookup"><span data-stu-id="6c122-140">The filter uses MMX if the machine supports MMX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c122-141">См. также</span><span class="sxs-lookup"><span data-stu-id="6c122-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c122-142">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="6c122-142">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




