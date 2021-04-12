---
description: Фильтр разделителя потока MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Фильтр разделителя потока MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140466"
---
# <a name="mpeg-1-stream-splitter-filter"></a><span data-ttu-id="b7270-103">Фильтр разделителя потока MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b7270-103">MPEG-1 Stream Splitter Filter</span></span>

<span data-ttu-id="b7270-104">Этот фильтр разделяет системный поток MPEG-1 в его компонентах аудио-и видеопотоках.</span><span class="sxs-lookup"><span data-stu-id="b7270-104">This filter splits an MPEG-1 system stream into its component audio and video streams.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7270-105">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="b7270-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="b7270-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Иаммедиаконтент</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>иамстреамселект</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7270-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7270-107">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="b7270-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="b7270-108">Основной тип: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="b7270-108">Major type: MEDIATYPE_Stream</span></span><br/> <span data-ttu-id="b7270-109">Подтипы</span><span class="sxs-lookup"><span data-stu-id="b7270-109">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="b7270-110">MEDIASUBTYPE_MPEG1System</span><span class="sxs-lookup"><span data-stu-id="b7270-110">MEDIASUBTYPE_MPEG1System</span></span></li>
<li><span data-ttu-id="b7270-111">MEDIASUBTYPE_MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="b7270-111">MEDIASUBTYPE_MPEG1VideoCD</span></span></li>
<li><span data-ttu-id="b7270-112">MEDIASUBTYPE_Audio</span><span class="sxs-lookup"><span data-stu-id="b7270-112">MEDIASUBTYPE_Audio</span></span></li>
<li><span data-ttu-id="b7270-113">MEDIASUBTYPE_Video</span><span class="sxs-lookup"><span data-stu-id="b7270-113">MEDIASUBTYPE_Video</span></span></li>
</ul>
<span data-ttu-id="b7270-114">См. раздел <a href="mpeg-1-media-types.md"> <strong>типы носителей MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7270-114">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7270-115">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="b7270-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="b7270-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7270-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7270-117">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="b7270-117">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="b7270-118">Основной тип: MEDIATYPE_Audio или MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="b7270-118">Major type: MEDIATYPE_Audio or MEDIATYPE_Video</span></span><br/> <span data-ttu-id="b7270-119">Подтип: MEDIASUBTYPE_MPEG1Payload или MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="b7270-119">Subtype: MEDIASUBTYPE_MPEG1Payload or MEDIASUBTYPE_MPEG1Packet</span></span><br/> <span data-ttu-id="b7270-120">См. раздел <a href="mpeg-1-media-types.md"> <strong>типы носителей MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7270-120">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7270-121">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="b7270-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="b7270-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>имедиасикинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7270-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7270-123">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="b7270-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="b7270-124">CLSID_MPEG1Splitter</span><span class="sxs-lookup"><span data-stu-id="b7270-124">CLSID_MPEG1Splitter</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7270-125">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="b7270-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="b7270-126">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="b7270-126">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7270-127">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="b7270-127">Executable</span></span></td>
<td><span data-ttu-id="b7270-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="b7270-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7270-129"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="b7270-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="b7270-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="b7270-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7270-131"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="b7270-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="b7270-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="b7270-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b7270-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7270-133">Remarks</span></span>

<span data-ttu-id="b7270-134">Этот файл поддерживает режим Pull только через [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Он не поддерживает режим принудительной отправки.</span><span class="sxs-lookup"><span data-stu-id="b7270-134">This file supports pull mode via [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) only; it does not support push mode.</span></span>

<span data-ttu-id="b7270-135">Так как содержимое MPEG-1 не индексируется, поиск может быть очень приблизительным.</span><span class="sxs-lookup"><span data-stu-id="b7270-135">Because MPEG-1 content is not indexed, seeking can be very approximate.</span></span> <span data-ttu-id="b7270-136">Обычно это удобно для фиксированной скорости системного потока MPEG-1 (обычно это оборудование, создаваемое для компакт-диска видео).</span><span class="sxs-lookup"><span data-stu-id="b7270-136">It is usually good for a fixed bitrate MPEG-1 system stream (which is usually hardware generated for video CD).</span></span>

<span data-ttu-id="b7270-137">Фильтр поддерживает интерфейс [**иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) для получения метаданных ID3.</span><span class="sxs-lookup"><span data-stu-id="b7270-137">The filter supports the [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) interface for retrieving ID3 metadata.</span></span>

<span data-ttu-id="b7270-138">Не все примеры MPEG имеют отметки времени.</span><span class="sxs-lookup"><span data-stu-id="b7270-138">Not all MPEG samples have time stamps.</span></span> <span data-ttu-id="b7270-139">Отсутствие метки времени в образце MPEG не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b7270-139">The lack of a time stamp on an MPEG sample is not an error.</span></span> <span data-ttu-id="b7270-140">Для разработчиков фильтров это означает, что не следует возвращать код ошибки из метода **Receive** входного ПИН-кода, если [**имедиасампле::-Time**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b7270-140">For filter developers, this means that you should not return an error code from your input pin's **Receive** method if [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) fails.</span></span> <span data-ttu-id="b7270-141">Если **Receive** возвращает любое значение, отличное от S \_ , это приведет к тому, что разделитель перестанет отправлять образцы.</span><span class="sxs-lookup"><span data-stu-id="b7270-141">If **Receive** returns any value other than S\_OK, it will cause the splitter to stop sending samples.</span></span>

<span data-ttu-id="b7270-142">Если файл содержит поток видео, разделитель потока MPEG-1 поддерживает поиск по номеру кадра.</span><span class="sxs-lookup"><span data-stu-id="b7270-142">If the file contains a video stream, the MPEG-1 Stream Splitter supports seeking by frame number.</span></span> <span data-ttu-id="b7270-143">Чтобы включить поиск на основе кадров, вызовите [**имедиасикинг:: сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) в [диспетчере графов фильтров](filter-graph-manager.md) со значением **\_ \_ кадр формата времени**.</span><span class="sxs-lookup"><span data-stu-id="b7270-143">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7270-144">См. также</span><span class="sxs-lookup"><span data-stu-id="b7270-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7270-145">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="b7270-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




