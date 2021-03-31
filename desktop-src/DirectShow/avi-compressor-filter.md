---
description: Фильтр сжатия AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Фильтр сжатия AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894070"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="8decc-103">Фильтр сжатия AVI</span><span class="sxs-lookup"><span data-stu-id="8decc-103">AVI Compressor Filter</span></span>

<span data-ttu-id="8decc-104">Фильтр AVI Compression позволяет присоединить к графу фильтров кодеки (ВКМ).</span><span class="sxs-lookup"><span data-stu-id="8decc-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="8decc-105">Каждый кодек отображается как отдельный экземпляр фильтра.</span><span class="sxs-lookup"><span data-stu-id="8decc-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="8decc-106">Этот фильтр нельзя создать напрямую с помощью CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="8decc-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="8decc-107">Вместо этого необходимо использовать перечислитель системных устройств.</span><span class="sxs-lookup"><span data-stu-id="8decc-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="8decc-108">Дополнительные сведения см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="8decc-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="8decc-109">Входной ПИН-код фильтра подключается к фильтрам, которые выводят несжатые видеоданные, такие как фильтры записи видео или [Фильтр AVI-разделителя](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8decc-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="8decc-110">Закрепление вывода фильтра обычно подключается к фильтру МУЛЬТИПЛЕКСОРа, например [фильтру мультиплексора AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8decc-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="8decc-111">Если кодек поддерживает диалоговое окно настройки VFW старого стиля или диалоговое окно "о программе", приложение может отобразить его с помощью интерфейса [**иамвфвкомпрессдиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .</span><span class="sxs-lookup"><span data-stu-id="8decc-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="8decc-112">Программы сжатия MPEG никогда не реализуются как кодеки ВКМ, но только как собственные фильтры DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8decc-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8decc-113">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="8decc-113">Filter Interfaces</span></span>                        | <span data-ttu-id="8decc-114">[**Иамвфвкомпрессдиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, испеЦифипропертипажес</span><span class="sxs-lookup"><span data-stu-id="8decc-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="8decc-115">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8decc-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="8decc-116">\_Устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="8decc-116">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="8decc-117">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8decc-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="8decc-118">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8decc-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="8decc-119">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8decc-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="8decc-120">\_Устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="8decc-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="8decc-121">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8decc-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="8decc-122">[**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8decc-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="8decc-123">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="8decc-123">Filter CLSID</span></span>                             | <span data-ttu-id="8decc-124">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8decc-124">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="8decc-125">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="8decc-125">Property Page CLSID</span></span>                      | <span data-ttu-id="8decc-126">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="8decc-126">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="8decc-127">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="8decc-127">Executable</span></span>                               | <span data-ttu-id="8decc-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="8decc-128">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="8decc-129">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="8decc-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="8decc-130">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="8decc-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="8decc-131">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="8decc-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8decc-132">\_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="8decc-132">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="8decc-133">См. также</span><span class="sxs-lookup"><span data-stu-id="8decc-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8decc-134">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="8decc-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



