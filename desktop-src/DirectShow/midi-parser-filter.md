---
description: Фильтр средства синтаксического анализа MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Фильтр средства синтаксического анализа MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989920"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="95a29-103">Фильтр средства синтаксического анализа MIDI</span><span class="sxs-lookup"><span data-stu-id="95a29-103">MIDI Parser Filter</span></span>

<span data-ttu-id="95a29-104">Фильтр средства синтаксического анализа MIDI считывает данные MIDI, найденные в. MID и. Файлы RMI.</span><span class="sxs-lookup"><span data-stu-id="95a29-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="95a29-105">Фильтр принимает поток из источника [Async File](file-source--async--filter.md) или [файла URL-адреса](file-source--url--filter.md) , фильтрует и выводит примеры MIDI в модуль [**подготовки MIDI**](midi-renderer-filter.md) для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="95a29-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a29-106">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="95a29-106">Filter Interfaces</span></span>                        | <span data-ttu-id="95a29-107">[**Иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="95a29-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="95a29-108">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="95a29-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="95a29-109">\_Поток MEDIATYPE, медиасубтипе \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="95a29-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="95a29-110">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="95a29-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="95a29-111">[**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="95a29-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="95a29-112">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="95a29-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="95a29-113">MEDIATYPE \_ MIDI, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="95a29-113">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="95a29-114">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="95a29-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="95a29-115">[**Имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="95a29-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="95a29-116">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="95a29-116">Filter CLSID</span></span>                             | <span data-ttu-id="95a29-117">\_МИДИПАРСЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="95a29-117">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="95a29-118">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="95a29-118">Property Page CLSID</span></span>                      | <span data-ttu-id="95a29-119">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="95a29-119">No property page</span></span>                                                                                         |
| <span data-ttu-id="95a29-120">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="95a29-120">Executable</span></span>                               | <span data-ttu-id="95a29-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="95a29-121">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="95a29-122">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="95a29-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="95a29-123">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="95a29-123">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="95a29-124">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="95a29-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="95a29-125">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="95a29-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="95a29-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95a29-126">Remarks</span></span>

<span data-ttu-id="95a29-127">Дополнительные сведения см. в разделе Модуль [**подготовки MIDI**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="95a29-127">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95a29-128">См. также</span><span class="sxs-lookup"><span data-stu-id="95a29-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95a29-129">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="95a29-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



