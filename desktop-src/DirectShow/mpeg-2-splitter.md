---
description: Разделитель MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Разделитель MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262438"
---
# <a name="mpeg-2-splitter"></a><span data-ttu-id="54293-103">Разделитель MPEG-2</span><span class="sxs-lookup"><span data-stu-id="54293-103">MPEG-2 Splitter</span></span>

<span data-ttu-id="54293-104">Начиная с Microsoft® Windows® XP, фильтр разделителя MPEG-2 является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="54293-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="54293-105">Вместо этого используйте [демультиплексор MPEG-2](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="54293-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

<span data-ttu-id="54293-106">На предыдущих платформах используйте разделитель MPEG-2 для потоков программы MPEG-2, доставляемых в режиме опроса, который содержит по крайней мере один из следующих типов потоков: MPEG-2 Video; Звук MPEG-2; AC3 аудио в кодировке, определенную для видео DVD; или в формате PCM, заданном для видео DVD.</span><span class="sxs-lookup"><span data-stu-id="54293-106">On earlier platforms, use the MPEG-2 Splitter for MPEG-2 program streams delivered in pull mode that contain at least one of the following stream types: MPEG-2 video; MPEG-2 audio; AC3 audio encoded as defined for DVD video; or PCM audio encoded as defined for DVD video.</span></span> <span data-ttu-id="54293-107">Этот фильтр анализирует потоки, создает выходной закрепление для каждого потока и выводит сжатые аудио-или видеопакеты MPEG в фильтр декодера MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="54293-107">This filter parses the streams, creates an output pin for each stream, and outputs the compressed MPEG audio or video packets to an MPEG-2 decoder filter.</span></span>

<span data-ttu-id="54293-108">Для программных и транспортных потоков, доставляемых в режиме Push-уведомлений, используйте [демультиплексор MPEG-2](mpeg-2-demultiplexer.md)на всех платформах.</span><span class="sxs-lookup"><span data-stu-id="54293-108">For program and transport streams delivered in push-mode, use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md), on all platforms.</span></span>

> [!Note]  
> <span data-ttu-id="54293-109">Разделитель MPEG-2 не поддерживает поиск в точном фрейме.</span><span class="sxs-lookup"><span data-stu-id="54293-109">The MPEG-2 Splitter does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54293-110">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="54293-110">Filter Interfaces</span></span></td>
<td><span data-ttu-id="54293-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <strong>испеЦифипропертипажес</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>иампарсе</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>иамстреамселект</strong></a></span><span class="sxs-lookup"><span data-stu-id="54293-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54293-112">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="54293-112">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="54293-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="54293-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="54293-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span><span class="sxs-lookup"><span data-stu-id="54293-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span></span></li>
<li><span data-ttu-id="54293-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="54293-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54293-116">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="54293-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="54293-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="54293-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54293-118">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="54293-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="54293-119">Зависит от типа потока.</span><span class="sxs-lookup"><span data-stu-id="54293-119">Depends on the stream type.</span></span> <span data-ttu-id="54293-120">См. раздел <a href="mpeg-2-splitter-media-types.md">типы мультимедиа с разделителями MPEG-2</a></span><span class="sxs-lookup"><span data-stu-id="54293-120">See <a href="mpeg-2-splitter-media-types.md">MPEG-2 Splitter Media Types</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54293-121">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="54293-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="54293-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>имедиасикинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="54293-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54293-123">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="54293-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="54293-124">CLSID_MMSPLITTER</span><span class="sxs-lookup"><span data-stu-id="54293-124">CLSID_MMSPLITTER</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54293-125">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="54293-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="54293-126">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="54293-126">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54293-127">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="54293-127">Executable</span></span></td>
<td><span data-ttu-id="54293-128">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="54293-128">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54293-129"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="54293-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="54293-130">MERIT_NORMAL + 1</span><span class="sxs-lookup"><span data-stu-id="54293-130">MERIT_NORMAL + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54293-131"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="54293-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="54293-132">CLSID_AudioInputDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="54293-132">CLSID_AudioInputDeviceCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="54293-133">См. также</span><span class="sxs-lookup"><span data-stu-id="54293-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54293-134">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="54293-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="54293-135">Использование разделителя MPEG-2</span><span class="sxs-lookup"><span data-stu-id="54293-135">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



