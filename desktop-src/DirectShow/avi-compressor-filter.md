---
description: Фильтр сжатия AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Фильтр сжатия AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212ab58eb3800e0ad5531ebc5c50d3b054e7866c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909472"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="54534-103">Фильтр сжатия AVI</span><span class="sxs-lookup"><span data-stu-id="54534-103">AVI Compressor Filter</span></span>

<span data-ttu-id="54534-104">Фильтр AVI Compression позволяет присоединить к графу фильтров кодеки (ВКМ).</span><span class="sxs-lookup"><span data-stu-id="54534-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="54534-105">Каждый кодек отображается как отдельный экземпляр фильтра.</span><span class="sxs-lookup"><span data-stu-id="54534-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="54534-106">Этот фильтр нельзя создать напрямую с помощью CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="54534-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="54534-107">Вместо этого необходимо использовать перечислитель системных устройств.</span><span class="sxs-lookup"><span data-stu-id="54534-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="54534-108">Дополнительные сведения см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="54534-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="54534-109">Входной ПИН-код фильтра подключается к фильтрам, которые выводят несжатые видеоданные, такие как фильтры записи видео или [Фильтр AVI-разделителя](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="54534-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="54534-110">Закрепление вывода фильтра обычно подключается к фильтру МУЛЬТИПЛЕКСОРа, например [фильтру мультиплексора AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="54534-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="54534-111">Если кодек поддерживает диалоговое окно настройки VFW старого стиля или диалоговое окно "о программе", приложение может отобразить его с помощью интерфейса [**иамвфвкомпрессдиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .</span><span class="sxs-lookup"><span data-stu-id="54534-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="54534-112">Программы сжатия MPEG никогда не реализуются как кодеки ВКМ, но только как собственные фильтры DirectShow.</span><span class="sxs-lookup"><span data-stu-id="54534-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



| <span data-ttu-id="54534-113">Метка</span><span class="sxs-lookup"><span data-stu-id="54534-113">Label</span></span> | <span data-ttu-id="54534-114">Значение</span><span class="sxs-lookup"><span data-stu-id="54534-114">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54534-115">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="54534-115">Filter Interfaces</span></span>                        | <span data-ttu-id="54534-116">[**Иамвфвкомпрессдиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, испеЦифипропертипажес</span><span class="sxs-lookup"><span data-stu-id="54534-116">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="54534-117">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="54534-117">Input Pin Media Types</span></span>                    | <span data-ttu-id="54534-118">\_Устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="54534-118">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="54534-119">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="54534-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="54534-120">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="54534-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="54534-121">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="54534-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="54534-122">\_Устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="54534-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="54534-123">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="54534-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="54534-124">[**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="54534-124">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="54534-125">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="54534-125">Filter CLSID</span></span>                             | <span data-ttu-id="54534-126">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="54534-126">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="54534-127">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="54534-127">Property Page CLSID</span></span>                      | <span data-ttu-id="54534-128">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="54534-128">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="54534-129">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="54534-129">Executable</span></span>                               | <span data-ttu-id="54534-130">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="54534-130">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="54534-131">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="54534-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="54534-132">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="54534-132">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="54534-133">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="54534-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="54534-134">\_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="54534-134">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="54534-135">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="54534-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54534-136">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="54534-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



