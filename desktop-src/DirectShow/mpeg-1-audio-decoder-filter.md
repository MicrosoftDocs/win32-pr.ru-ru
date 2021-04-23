---
description: Фильтр звукового декодера MPEG-1
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Фильтр звукового декодера MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f2c68243544a8c6a77cbd8101c85d68f393c3d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682293"
---
# <a name="mpeg-1-audio-decoder-filter"></a><span data-ttu-id="219ef-103">Фильтр звукового декодера MPEG-1</span><span class="sxs-lookup"><span data-stu-id="219ef-103">MPEG-1 Audio Decoder Filter</span></span>

<span data-ttu-id="219ef-104">Декодирует слой MPEG-1 и звук уровня II в PCM.</span><span class="sxs-lookup"><span data-stu-id="219ef-104">Decodes MPEG-1 Layer I and Layer II audio to PCM.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="219ef-105">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="219ef-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="219ef-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <strong>испеЦифипропертипажес</strong></span><span class="sxs-lookup"><span data-stu-id="219ef-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="219ef-107">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="219ef-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="219ef-108">MEDIATYPE_Audio, FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="219ef-108">MEDIATYPE_Audio, FORMAT_WaveFormatEx</span></span><br/> <span data-ttu-id="219ef-109">Допустимы следующие подтипы:</span><span class="sxs-lookup"><span data-stu-id="219ef-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="219ef-110">MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="219ef-110">MEDIASUBTYPE_MPEG1Packet</span></span></li>
<li><span data-ttu-id="219ef-111">MEDIASUBTYPE_MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="219ef-111">MEDIASUBTYPE_MPEG1Payload</span></span></li>
<li><span data-ttu-id="219ef-112">MEDIASUBTYPE_MPEG1AudioPayload</span><span class="sxs-lookup"><span data-stu-id="219ef-112">MEDIASUBTYPE_MPEG1AudioPayload</span></span></li>
<li><span data-ttu-id="219ef-113">GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="219ef-113">GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="219ef-114">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="219ef-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="219ef-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="219ef-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="219ef-116">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="219ef-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="219ef-117">MEDIATYPE_Audio, MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="219ef-117">MEDIATYPE_Audio, MEDIASUBTYPE_PCM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="219ef-118">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="219ef-118">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="219ef-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="219ef-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="219ef-120">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="219ef-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="219ef-121">CLSID_CMpegAudioCodec</span><span class="sxs-lookup"><span data-stu-id="219ef-121">CLSID_CMpegAudioCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="219ef-122">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="219ef-122">Property Page CLSID</span></span></td>
<td><span data-ttu-id="219ef-123">CLSID_MpegAudioDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="219ef-123">CLSID_MpegAudioDecoderPropertyPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="219ef-124">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="219ef-124">Executable</span></span></td>
<td><span data-ttu-id="219ef-125">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="219ef-125">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="219ef-126"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="219ef-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="219ef-127">0x03680001</span><span class="sxs-lookup"><span data-stu-id="219ef-127">0x03680001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="219ef-128"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="219ef-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="219ef-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="219ef-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="219ef-130">См. также</span><span class="sxs-lookup"><span data-stu-id="219ef-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="219ef-131">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="219ef-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




