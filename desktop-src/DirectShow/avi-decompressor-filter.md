---
description: Фильтр распаковки AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Фильтр распаковки AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b6fcff61dd867c598e793fb5aa8fbff67dc6cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806341"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="c8a9e-103">Фильтр распаковки AVI</span><span class="sxs-lookup"><span data-stu-id="c8a9e-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="c8a9e-104">Фильтр распаковки AVI включает кодеки (ВКМ) для подключения к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="c8a9e-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="c8a9e-105">Приложению не нужно добавлять фильтр к графу фильтра; При необходимости он автоматически извлекается диспетчером графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="c8a9e-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="c8a9e-106">Когда диспетчер графа фильтров создает граф для отображения AVI-файла, он проверяет значение FOURCC в заголовке файла AVI, чтобы определить, сжимается ли видео-поток.</span><span class="sxs-lookup"><span data-stu-id="c8a9e-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="c8a9e-107">Если это так, диспетчер графов фильтров добавляет распаковку AVI, которая затем ищет в реестре установленный декомпрессор, который может работать с этим файлом.</span><span class="sxs-lookup"><span data-stu-id="c8a9e-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="c8a9e-108">Декомпрессоры MPEG никогда не реализуются как кодеки ВКМ, но только как собственные фильтры DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c8a9e-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="c8a9e-109">В своем вышестоящем ПИН-коде сжатие AVI обычно подключается к [разделителю AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="c8a9e-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="c8a9e-110">При закреплении на выходе он обычно подключается к модулю [прорисовки видео](video-renderer-filter.md) или [фильтру мультиплексора AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="c8a9e-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



|                                          |                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a9e-111">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="c8a9e-111">Filter Interfaces</span></span>                        | [<span data-ttu-id="c8a9e-112">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="c8a9e-112">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="c8a9e-113">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="c8a9e-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="c8a9e-114">Основной тип: MEDIATYPE \_ видеосубтипе: должен соответствовать коду FourCC для типа сжатия.</span><span class="sxs-lookup"><span data-stu-id="c8a9e-114">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="c8a9e-115">Дополнительные сведения см. в разделе [Коды FOURCC](fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c8a9e-115">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="c8a9e-116">Тип формата: формат \_ видеоинфо</span><span class="sxs-lookup"><span data-stu-id="c8a9e-116">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="c8a9e-117">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="c8a9e-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="c8a9e-118">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c8a9e-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="c8a9e-119">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="c8a9e-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="c8a9e-120">\_Устройство MEDIATYPE, медиасубтипе \_ null, Format \_ видеоинфо</span><span class="sxs-lookup"><span data-stu-id="c8a9e-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="c8a9e-121">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="c8a9e-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="c8a9e-122">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c8a9e-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="c8a9e-123">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="c8a9e-123">Filter CLSID</span></span>                             | <span data-ttu-id="c8a9e-124">\_АВИДЕК CLSID</span><span class="sxs-lookup"><span data-stu-id="c8a9e-124">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="c8a9e-125">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="c8a9e-125">Property Page CLSID</span></span>                      | <span data-ttu-id="c8a9e-126">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="c8a9e-126">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="c8a9e-127">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="c8a9e-127">Executable</span></span>                               | <span data-ttu-id="c8a9e-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="c8a9e-128">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="c8a9e-129">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="c8a9e-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="c8a9e-130">неуспешный \_ режим</span><span class="sxs-lookup"><span data-stu-id="c8a9e-130">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="c8a9e-131">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="c8a9e-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="c8a9e-132">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="c8a9e-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="c8a9e-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c8a9e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8a9e-134">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="c8a9e-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




