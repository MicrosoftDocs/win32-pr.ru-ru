---
description: Фильтр видеодекодера DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Фильтр видеодекодера DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536500"
---
# <a name="dv-video-decoder-filter"></a><span data-ttu-id="ff263-103">Фильтр видеодекодера DV</span><span class="sxs-lookup"><span data-stu-id="ff263-103">DV Video Decoder Filter</span></span>

<span data-ttu-id="ff263-104">Этот фильтр декодирует поток цифрового видео (DV) в несжатое видео.</span><span class="sxs-lookup"><span data-stu-id="ff263-104">This filter decodes a digital video (DV) stream into uncompressed video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff263-105">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="ff263-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="ff263-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>иипдвдек</strong></a>, <strong>IPersistStream</strong>, <strong>испеЦифипропертипажес</strong></span><span class="sxs-lookup"><span data-stu-id="ff263-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff263-107">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="ff263-107">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="ff263-108">MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="ff263-108">MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="ff263-109">MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="ff263-109">MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="ff263-110">FORMAT_VideoInfo, FORMAT_DvInfo</span><span class="sxs-lookup"><span data-stu-id="ff263-110">FORMAT_VideoInfo, FORMAT_DvInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff263-111">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="ff263-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="ff263-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff263-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff263-113">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="ff263-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="ff263-114"><strong>Основной тип</strong>: MEDIATYPE_Video<strong>подтипы</strong>:</span><span class="sxs-lookup"><span data-stu-id="ff263-114"><strong>Major type</strong>: MEDIATYPE_Video<strong>Subtypes</strong>:</span></span><br/>
<ul>
<li><span data-ttu-id="ff263-115">MEDIASUBTYPE_YUY2</span><span class="sxs-lookup"><span data-stu-id="ff263-115">MEDIASUBTYPE_YUY2</span></span></li>
<li><span data-ttu-id="ff263-116">MEDIASUBTYPE_UYVY</span><span class="sxs-lookup"><span data-stu-id="ff263-116">MEDIASUBTYPE_UYVY</span></span></li>
<li><span data-ttu-id="ff263-117">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="ff263-117">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="ff263-118">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="ff263-118">MEDIASUBTYPE_RGB32</span></span></li>
<li><span data-ttu-id="ff263-119">MEDIASUBTYPE_ARGB32</span><span class="sxs-lookup"><span data-stu-id="ff263-119">MEDIASUBTYPE_ARGB32</span></span></li>
<li><span data-ttu-id="ff263-120">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="ff263-120">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="ff263-121">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="ff263-121">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="ff263-122">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="ff263-122">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="ff263-123">MEDIASUBTYPE_Y41P</span><span class="sxs-lookup"><span data-stu-id="ff263-123">MEDIASUBTYPE_Y41P</span></span></li>
</ul><span data-ttu-id="ff263-124">
<strong>Типы форматов</strong>:</span><span class="sxs-lookup"><span data-stu-id="ff263-124">
<strong>Format types</strong>:</span></span><br/> <span data-ttu-id="ff263-125">Format_VideoInfo, Format_VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="ff263-125">Format_VideoInfo, Format_VideoInfo2</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff263-126">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="ff263-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="ff263-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff263-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff263-128">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="ff263-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="ff263-129">CLSID_DVVideoCodec</span><span class="sxs-lookup"><span data-stu-id="ff263-129">CLSID_DVVideoCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff263-130">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="ff263-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="ff263-131">CLSID_DVDecPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="ff263-131">CLSID_DVDecPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff263-132">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="ff263-132">Executable</span></span></td>
<td><span data-ttu-id="ff263-133">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="ff263-133">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff263-134"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="ff263-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="ff263-135">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="ff263-135">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff263-136"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="ff263-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="ff263-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ff263-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="ff263-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff263-138">Remarks</span></span>

<span data-ttu-id="ff263-139">Используйте интерфейс [**иипдвдек**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) , чтобы задать разрешение декодирования: полный, половинный размер, квартал или один восьмой размер.</span><span class="sxs-lookup"><span data-stu-id="ff263-139">Use the [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) interface to set the decoding resolution to full, half size, quarter size, or one-eighth size.</span></span>

<span data-ttu-id="ff263-140">**Чередование**. более ранние версии декодера всегда разменяют чересстрочную развертку видео.</span><span class="sxs-lookup"><span data-stu-id="ff263-140">**Interlacing**: Earlier versions of the decoder always deinterlace the video.</span></span> <span data-ttu-id="ff263-141">Начиная с DirectX 9,0, декодер DV video может сохранить чересстрочную развертку.</span><span class="sxs-lookup"><span data-stu-id="ff263-141">As of DirectX 9.0, the DV Video Decoder can preserve the interlacing.</span></span> <span data-ttu-id="ff263-142">Это позволяет разрисовать чередование видео с помощью формирователя микширования видео (VMR) для улучшения качества отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ff263-142">This enables the interlaced video to be deinterlaced by the Video Mixing Renderer (VMR), for improved rendering quality.</span></span> <span data-ttu-id="ff263-143">Чтобы использовать эту функцию, нисходящий фильтр должен поддерживать форматы [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , обозначенные этим форматом значения \_ VideoInfo2 в элементе **Форматтипе** структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="ff263-143">To use this feature, the downstream filter must support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, indicated by that value Format\_VideoInfo2 in the **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="ff263-144">В выходных данных полного разрешения флаги разчередования (**двинтерлаце**) в структуре **VIDEOINFOHEADER2** устанавливаются в значение `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , указывающее на поля с чередованием.</span><span class="sxs-lookup"><span data-stu-id="ff263-144">At full resolution output, the deinterlacing flags (**dwInterlace**) in the **VIDEOINFOHEADER2** structure are set to `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave`, indicating interlaced fields.</span></span> <span data-ttu-id="ff263-145">В половине разрешения или ниже **двинтерлаце** устанавливается равным нулю, что означает последовательные кадры.</span><span class="sxs-lookup"><span data-stu-id="ff263-145">At half resolution or lower, **dwInterlace** is set to zero, indicating progressive frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff263-146">См. также</span><span class="sxs-lookup"><span data-stu-id="ff263-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff263-147">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="ff263-147">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="ff263-148">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="ff263-148">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




