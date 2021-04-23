---
description: Фильтр преобразователя цветового пространства
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Фильтр преобразователя цветового пространства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f054ee03dd65cf619a697d4441b4d09279e7b912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494640"
---
# <a name="color-space-converter-filter"></a><span data-ttu-id="7e3a2-103">Фильтр преобразователя цветового пространства</span><span class="sxs-lookup"><span data-stu-id="7e3a2-103">Color Space Converter Filter</span></span>

<span data-ttu-id="7e3a2-104">Этот фильтр преобразования преобразует из одного типа цвета RGB в другой тип RGB, например, между 24-разрядным и 8-разрядным цветом RGB.</span><span class="sxs-lookup"><span data-stu-id="7e3a2-104">This transform filter converts from one RGB color type to another RGB type, such as between 24-bit and 8-bit RGB color.</span></span> <span data-ttu-id="7e3a2-105">Поскольку этот тип преобразования, как правило, более эффективно обрабатывается в рамках декомпрессора видео, в основном используется преобразователь цветового пространства, когда источник потока состоит из несжатых кадров RGB.</span><span class="sxs-lookup"><span data-stu-id="7e3a2-105">Since this type of conversion is generally handled more efficiently within a video decompressor, the main use of the Color Space Converter is when the stream source consists of uncompressed RGB frames.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e3a2-106">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="7e3a2-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="7e3a2-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e3a2-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e3a2-108">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7e3a2-108">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="7e3a2-109">MEDIATYPE_Video FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="7e3a2-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="7e3a2-110">Допустимы следующие подтипы:</span><span class="sxs-lookup"><span data-stu-id="7e3a2-110">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="7e3a2-111">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="7e3a2-111">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="7e3a2-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="7e3a2-112">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="7e3a2-113">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="7e3a2-113">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="7e3a2-114">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="7e3a2-114">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="7e3a2-115">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="7e3a2-115">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e3a2-116">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7e3a2-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="7e3a2-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e3a2-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e3a2-118">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7e3a2-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="7e3a2-119">MEDIATYPE_Video FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="7e3a2-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="7e3a2-120">Допустимы следующие подтипы:</span><span class="sxs-lookup"><span data-stu-id="7e3a2-120">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="7e3a2-121">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="7e3a2-121">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="7e3a2-122">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="7e3a2-122">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="7e3a2-123">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="7e3a2-123">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="7e3a2-124">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="7e3a2-124">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="7e3a2-125">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="7e3a2-125">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e3a2-126">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7e3a2-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="7e3a2-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e3a2-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e3a2-128">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="7e3a2-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="7e3a2-129">CLSID_Colour</span><span class="sxs-lookup"><span data-stu-id="7e3a2-129">CLSID_Colour</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e3a2-130">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="7e3a2-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="7e3a2-131">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="7e3a2-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e3a2-132">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="7e3a2-132">Executable</span></span></td>
<td><span data-ttu-id="7e3a2-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7e3a2-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e3a2-134"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="7e3a2-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="7e3a2-135">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="7e3a2-135">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e3a2-136"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="7e3a2-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="7e3a2-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="7e3a2-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7e3a2-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7e3a2-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e3a2-139">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="7e3a2-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




