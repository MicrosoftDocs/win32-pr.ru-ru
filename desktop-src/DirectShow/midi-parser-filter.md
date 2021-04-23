---
description: Фильтр средства синтаксического анализа MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Фильтр средства синтаксического анализа MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908432"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="a87da-103">Фильтр средства синтаксического анализа MIDI</span><span class="sxs-lookup"><span data-stu-id="a87da-103">MIDI Parser Filter</span></span>

<span data-ttu-id="a87da-104">Фильтр средства синтаксического анализа MIDI считывает данные MIDI, найденные в. MID и. Файлы RMI.</span><span class="sxs-lookup"><span data-stu-id="a87da-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="a87da-105">Фильтр принимает поток из источника [Async File](file-source--async--filter.md) или [файла URL-адреса](file-source--url--filter.md) , фильтрует и выводит примеры MIDI в модуль [**подготовки MIDI**](midi-renderer-filter.md) для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a87da-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



| <span data-ttu-id="a87da-106">Метка</span><span class="sxs-lookup"><span data-stu-id="a87da-106">Label</span></span> | <span data-ttu-id="a87da-107">Значение</span><span class="sxs-lookup"><span data-stu-id="a87da-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a87da-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="a87da-108">Filter Interfaces</span></span>                        | <span data-ttu-id="a87da-109">[**Иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="a87da-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="a87da-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="a87da-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="a87da-111">\_Поток MEDIATYPE, медиасубтипе \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="a87da-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="a87da-112">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="a87da-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="a87da-113">[**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a87da-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="a87da-114">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="a87da-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="a87da-115">MEDIATYPE \_ MIDI, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="a87da-115">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="a87da-116">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="a87da-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a87da-117">[**Имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="a87da-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="a87da-118">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="a87da-118">Filter CLSID</span></span>                             | <span data-ttu-id="a87da-119">\_МИДИПАРСЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="a87da-119">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="a87da-120">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="a87da-120">Property Page CLSID</span></span>                      | <span data-ttu-id="a87da-121">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="a87da-121">No property page</span></span>                                                                                         |
| <span data-ttu-id="a87da-122">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="a87da-122">Executable</span></span>                               | <span data-ttu-id="a87da-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="a87da-123">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="a87da-124">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="a87da-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="a87da-125">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="a87da-125">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="a87da-126">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="a87da-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a87da-127">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="a87da-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="a87da-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a87da-128">Remarks</span></span>

<span data-ttu-id="a87da-129">Дополнительные сведения см. в разделе Модуль [**подготовки MIDI**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a87da-129">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a87da-130">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a87da-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a87da-131">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="a87da-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



