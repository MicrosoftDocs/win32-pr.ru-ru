---
description: Этот фильтр используется для демультиплексирования транспорта MPEG-2 и программных потоков, которые доставляются в принудительном режиме.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Демультиплексор MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682248"
---
# <a name="mpeg-2-demultiplexer"></a><span data-ttu-id="7b7c4-103">Демультиплексор MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7b7c4-103">MPEG-2 Demultiplexer</span></span>

<span data-ttu-id="7b7c4-104">Этот фильтр используется для демультиплексирования транспорта MPEG-2 и программных потоков, которые доставляются в принудительном режиме.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-104">This filter demultiplexes MPEG-2 transport and program streams that are delivered in push-mode.</span></span> <span data-ttu-id="7b7c4-105">Начиная с Windows XP этот фильтр также поддерживает потоки программы в режиме опроса (воспроизведение файла).</span><span class="sxs-lookup"><span data-stu-id="7b7c4-105">Starting in Windows XP, this filter also supports program streams in pull mode (file playback).</span></span> <span data-ttu-id="7b7c4-106">На более ранних платформах используйте фильтр [разделителя MPEG-2](mpeg-2-splitter.md) для потоков программы в режиме опроса.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-106">On earlier platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter for program streams in pull mode.</span></span> <span data-ttu-id="7b7c4-107">Этот фильтр можно использовать в любом типе графа фильтра, включая граф фильтра BDA Digital TV.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-107">This filter can be used in any type of filter graph, including a BDA digital TV filter graph.</span></span>

> [!Note]  
> <span data-ttu-id="7b7c4-108">Демультиплексор MPEG-2 не поддерживает поиск в точном фрейме.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-108">The MPEG-2 Demultiplexer does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7b7c4-109">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="7b7c4-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="7b7c4-110">Все режимы:</span><span class="sxs-lookup"><span data-stu-id="7b7c4-110">All modes:</span></span><br/>
<ul>
<li><span data-ttu-id="7b7c4-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="7b7c4-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="7b7c4-112"><strong>испеЦифипропертипажес</strong></span><span class="sxs-lookup"><span data-stu-id="7b7c4-112"><strong>ISpecifyPropertyPages</strong></span></span></li>
</ul>
<span data-ttu-id="7b7c4-113">Только режим принудительной отправки:</span><span class="sxs-lookup"><span data-stu-id="7b7c4-113">Push mode only:</span></span><br/>
<ul>
<li><span data-ttu-id="7b7c4-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7b7c4-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="7b7c4-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span><span class="sxs-lookup"><span data-stu-id="7b7c4-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span></span></li>
<li><span data-ttu-id="7b7c4-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>иреференцеклокк</strong></a></span><span class="sxs-lookup"><span data-stu-id="7b7c4-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b7c4-117">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7b7c4-117">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="7b7c4-118">Основной тип: MEDIATYPE_STREAM</span><span class="sxs-lookup"><span data-stu-id="7b7c4-118">Major type: MEDIATYPE_STREAM</span></span><br/> <span data-ttu-id="7b7c4-119">Подтип</span><span class="sxs-lookup"><span data-stu-id="7b7c4-119">Subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="7b7c4-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="7b7c4-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="7b7c4-121">MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="7b7c4-121">MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="7b7c4-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="7b7c4-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="7b7c4-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span><span class="sxs-lookup"><span data-stu-id="7b7c4-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span></span></li>
</ul>
<span data-ttu-id="7b7c4-124">Дополнительные сведения см. в статье <a href="mpeg-2-demultiplexer-media-types.md"><strong>типы мультимедиа для демультиплексирования MPEG-2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-124">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b7c4-125">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7b7c4-125">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="7b7c4-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="7b7c4-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b7c4-127">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7b7c4-127">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="7b7c4-128">Простейшие потоки аудио и видео должны иметь основной тип MEDIATYPE_Audio или MEDIATYPE_Video.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-128">Audio and video elementary streams must have a major type of MEDIATYPE_Audio or MEDIATYPE_Video.</span></span><br/> <span data-ttu-id="7b7c4-129">Дополнительные сведения см. в статье <a href="mpeg-2-demultiplexer-media-types.md"><strong>типы мультимедиа для демультиплексирования MPEG-2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-129">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b7c4-130">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7b7c4-130">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="7b7c4-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, только режим принудительной отправки <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a>: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>иампушсаурце</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="7b7c4-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>Push mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span></span><br/> <span data-ttu-id="7b7c4-132">Только режим опроса: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>имедиасикинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="7b7c4-132">Pull mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b7c4-133">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="7b7c4-133">Filter CLSID</span></span></td>
<td><span data-ttu-id="7b7c4-134">CLSID_MPEG2Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="7b7c4-134">CLSID_MPEG2Demultiplexer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b7c4-135">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="7b7c4-135">Property Page CLSID</span></span></td>
<td><span data-ttu-id="7b7c4-136">Доступно только для тестирования.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-136">Available for testing only.</span></span> <span data-ttu-id="7b7c4-137">Использование интерфейса <strong>испеЦифипропертипажес</strong> для доступа к страницам свойств</span><span class="sxs-lookup"><span data-stu-id="7b7c4-137">Use the <strong>ISpecifyPropertyPages</strong> interface to access the property pages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b7c4-138">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="7b7c4-138">Executable</span></span></td>
<td><span data-ttu-id="7b7c4-139">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="7b7c4-139">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b7c4-140"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="7b7c4-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="7b7c4-141">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="7b7c4-141">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b7c4-142"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="7b7c4-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="7b7c4-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="7b7c4-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="7b7c4-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b7c4-144">Remarks</span></span>

<span data-ttu-id="7b7c4-145">Для вывода простых потоков аудио и видео демультиплексирование должен получить потоки PCR и SCR.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-145">To output audio and video elementary streams, the demux must receive the PCR and SCR streams.</span></span> <span data-ttu-id="7b7c4-146">На стороне входа это означает, что транспортный поток должен содержать таблицы PAT и ПЛТ, определяющие идентификатор процесса для потока PCR; и потоки программ должны содержать по крайней мере один заголовок Pack.</span><span class="sxs-lookup"><span data-stu-id="7b7c4-146">On the input side, this means a transport stream must contain the PAT and PMT tables that define the PID for the PCR stream; and program streams must contain at least one pack header.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b7c4-147">Требования</span><span class="sxs-lookup"><span data-stu-id="7b7c4-147">Requirements</span></span>



| <span data-ttu-id="7b7c4-148">Требование</span><span class="sxs-lookup"><span data-stu-id="7b7c4-148">Requirement</span></span> | <span data-ttu-id="7b7c4-149">Значение</span><span class="sxs-lookup"><span data-stu-id="7b7c4-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7b7c4-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b7c4-150">Minimum supported client</span></span><br/> | <span data-ttu-id="7b7c4-151">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b7c4-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7b7c4-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b7c4-152">Minimum supported server</span></span><br/> | <span data-ttu-id="7b7c4-153">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b7c4-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b7c4-154">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7b7c4-154">End of server support</span></span><br/>    | <span data-ttu-id="7b7c4-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7b7c4-155">Windows Server 2003 R2</span></span><br/>                          |



## <a name="see-also"></a><span data-ttu-id="7b7c4-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b7c4-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b7c4-157">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="7b7c4-157">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="7b7c4-158">Использование демультиплексора MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7b7c4-158">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




