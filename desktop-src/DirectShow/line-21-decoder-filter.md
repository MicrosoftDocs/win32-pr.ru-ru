---
description: Фильтр декодера Line 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Фильтр декодера Line 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672957"
---
# <a name="line-21-decoder-filter"></a><span data-ttu-id="eb549-103">Фильтр декодера Line 21</span><span class="sxs-lookup"><span data-stu-id="eb549-103">Line 21 Decoder Filter</span></span>

<span data-ttu-id="eb549-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="eb549-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="eb549-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="eb549-105">It may be altered or unavailable in subsequent versions.</span></span>

<span data-ttu-id="eb549-106">В этой строке 21 фильтр декодера декодировать строку 21 данные и выводит текст заголовка на точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="eb549-106">This Line 21 Decoder filter decodes line 21 data and draws the caption text onto bitmaps.</span></span>

<span data-ttu-id="eb549-107">Входной ПИН-код подключается к любому поставщику данных Line 21 (обычно это видеодекодер DVD или фильтр [декодера CC](cc-decoder-filter.md) ).</span><span class="sxs-lookup"><span data-stu-id="eb549-107">The input pin connects to any line 21 data provider, typically either a DVD video decoder or the [CC Decoder](cc-decoder-filter.md) filter.</span></span> <span data-ttu-id="eb549-108">Декодер CC предоставляет линии 21 данных из ВБИ аналогового телевизионного сигнала.</span><span class="sxs-lookup"><span data-stu-id="eb549-108">The CC Decoder provides line 21 data from the VBI of an analog television signal.</span></span> <span data-ttu-id="eb549-109">Закрепление вывода подключается к дополнительному ПИН-коду [микшера наложения](overlay-mixer-filter.md) или к другому модулю подготовки видео, например VMR.</span><span class="sxs-lookup"><span data-stu-id="eb549-109">The output pin connects to a secondary pin on the [Overlay Mixer](overlay-mixer-filter.md) or to another video renderer, such as the VMR.</span></span>

<span data-ttu-id="eb549-110">Этот фильтр принимает данные строки 21 в стандартном формате пары байтов или для DVD-диска в качестве пакета для всей группы изображений (GOP).</span><span class="sxs-lookup"><span data-stu-id="eb549-110">This filter accepts line 21 data in the standard byte-pair format or, for DVD, as a packet for the whole group of pictures (GOP).</span></span> <span data-ttu-id="eb549-111">Для каждого GOP в видеопотоке DVD может существовать пользовательский пакет данных, содержащий сведения о заголовке конкретного GOP и строку 21 данных.</span><span class="sxs-lookup"><span data-stu-id="eb549-111">For every GOP in the DVD video stream, there can be a user data packet that has that particular GOP's header information and line 21 data.</span></span> <span data-ttu-id="eb549-112">Формат пар байтов определяется в стандарте EIA/CEA-608-B. Дополнительные сведения см. в этом стандарте.</span><span class="sxs-lookup"><span data-stu-id="eb549-112">The format of the byte pairs is defined in the EIA/CEA-608-B standard; please refer to that standard for more information.</span></span>

<span data-ttu-id="eb549-113">Доступны две версии этого фильтра:</span><span class="sxs-lookup"><span data-stu-id="eb549-113">Two versions of this filter are available:</span></span>



| <span data-ttu-id="eb549-114">Фильтр</span><span class="sxs-lookup"><span data-stu-id="eb549-114">Filter</span></span>            | <span data-ttu-id="eb549-115">CLSID</span><span class="sxs-lookup"><span data-stu-id="eb549-115">CLSID</span></span>                 |
|-------------------|-----------------------|
| <span data-ttu-id="eb549-116">Декодер Line 21</span><span class="sxs-lookup"><span data-stu-id="eb549-116">Line 21 Decoder</span></span>   | <span data-ttu-id="eb549-117">\_LINE21DECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="eb549-117">CLSID\_Line21Decoder</span></span>  |
| <span data-ttu-id="eb549-118">Line 21 декодер 2</span><span class="sxs-lookup"><span data-stu-id="eb549-118">Line 21 Decoder 2</span></span> | <span data-ttu-id="eb549-119">\_LINE21DECODER2 CLSID</span><span class="sxs-lookup"><span data-stu-id="eb549-119">CLSID\_Line21Decoder2</span></span> |



 

<span data-ttu-id="eb549-120">Фильтр версии 1 используется на платформах Microsoft® Windows® 95/98/Me и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="eb549-120">The version 1 filter is used on Microsoft® Windows® 95/98/Me and Windows 2000 platforms.</span></span> <span data-ttu-id="eb549-121">Фильтр версии 2 доступен в Microsoft Windows XP и более поздних версиях и используется каждый раз, когда в графе находится модуль подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="eb549-121">The version 2 filter is available in Microsoft Windows XP and later, and is used whenever the Video Mixing Renderer is in the graph.</span></span>

<span data-ttu-id="eb549-122">Сведения в следующей таблице относятся к обеим версиям фильтра:</span><span class="sxs-lookup"><span data-stu-id="eb549-122">The information in the following table applies to both versions of the filter:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb549-123">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="eb549-123">Filter Interfaces</span></span></td>
<td><span data-ttu-id="eb549-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb549-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb549-125">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="eb549-125">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="eb549-126">Основной тип: MEDIATYPE_AUXLine21DataSubtype:</span><span class="sxs-lookup"><span data-stu-id="eb549-126">Major Type: MEDIATYPE_AUXLine21DataSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="eb549-127">MEDIASUBTYPE_Line21_BytePair (стандартная строка 21)</span><span class="sxs-lookup"><span data-stu-id="eb549-127">MEDIASUBTYPE_Line21_BytePair (standard line 21)</span></span></li>
<li><span data-ttu-id="eb549-128">MEDIASUBTYPE_Line21_GOPPacket (DVD-строка 21)</span><span class="sxs-lookup"><span data-stu-id="eb549-128">MEDIASUBTYPE_Line21_GOPPacket (DVD line 21)</span></span></li>
</ul>
<span data-ttu-id="eb549-129">Тип формата: FORMAT_VideoInfo или GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="eb549-129">Format Type: FORMAT_VideoInfo or GUID_NULL</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb549-130">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="eb549-130">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="eb549-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb549-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb549-132">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="eb549-132">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="eb549-133">Основной тип: MEDIATYPE_VideoSubtype:</span><span class="sxs-lookup"><span data-stu-id="eb549-133">Major type: MEDIATYPE_VideoSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="eb549-134">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="eb549-134">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="eb549-135">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="eb549-135">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="eb549-136">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="eb549-136">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="eb549-137">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="eb549-137">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="eb549-138">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="eb549-138">MEDIASUBTYPE_RGB32</span></span></li>
</ul>
<span data-ttu-id="eb549-139">Тип формата: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="eb549-139">Format Type: FORMAT_VideoInfo</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb549-140">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="eb549-140">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="eb549-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb549-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb549-142">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="eb549-142">Filter CLSID</span></span></td>
<td><span data-ttu-id="eb549-143">См. предыдущую таблицу</span><span class="sxs-lookup"><span data-stu-id="eb549-143">See previous table</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb549-144">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="eb549-144">Property Page CLSID</span></span></td>
<td><span data-ttu-id="eb549-145">Нет</span><span class="sxs-lookup"><span data-stu-id="eb549-145">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb549-146">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="eb549-146">Executable</span></span></td>
<td><span data-ttu-id="eb549-147">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="eb549-147">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb549-148"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="eb549-148"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="eb549-149">Line 21 декодер: MERIT_NORMALLine 21 декодер 2: MERIT_NORMAL + 2</span><span class="sxs-lookup"><span data-stu-id="eb549-149">Line 21 Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb549-150"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="eb549-150"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="eb549-151">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="eb549-151">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="eb549-152">См. также</span><span class="sxs-lookup"><span data-stu-id="eb549-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb549-153">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="eb549-153">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="eb549-154">Субтитры и телетекст</span><span class="sxs-lookup"><span data-stu-id="eb549-154">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> <dt>

[<span data-ttu-id="eb549-155">Конфигурация графа фильтра DVD</span><span class="sxs-lookup"><span data-stu-id="eb549-155">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




