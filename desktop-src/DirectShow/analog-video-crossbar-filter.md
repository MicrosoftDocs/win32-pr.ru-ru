---
description: Фильтр аналогового микшера видео
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Фильтр аналогового микшера видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909602"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="e9daa-103">Фильтр аналогового микшера видео</span><span class="sxs-lookup"><span data-stu-id="e9daa-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="e9daa-104">Фильтр аналогового микшера видео представляет микшер видео на устройстве видеозаписи, поддерживающем WDM (WDM).</span><span class="sxs-lookup"><span data-stu-id="e9daa-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="e9daa-105">Этот фильтр является фильтром оболочки для микширования на устройствах потоковой передачи WDM.</span><span class="sxs-lookup"><span data-stu-id="e9daa-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="e9daa-106">Понятное имя фильтра берется с устройства.</span><span class="sxs-lookup"><span data-stu-id="e9daa-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="e9daa-107">Каждый выходной ПИН-код представляет собой аппаратный путь для аналогового видео басебанд.</span><span class="sxs-lookup"><span data-stu-id="e9daa-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="e9daa-108">Один из входных контактов поступает из ТВ-тюнера ( [фильтра ТВ-тюнера](tv-tuner-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="e9daa-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="e9daa-109">Другие входные ПИН-коды поддерживают видео-или звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="e9daa-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="e9daa-110">Фильтр поддерживает все типы мультимедиа и форматы, которые поддерживаются в подчиненных соединениях.</span><span class="sxs-lookup"><span data-stu-id="e9daa-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="e9daa-111">Этот фильтр нельзя создать напрямую с помощью CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="e9daa-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="e9daa-112">Интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) автоматически добавляет этот фильтр к графу по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="e9daa-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="e9daa-113">Дополнительные сведения о фильтрах оболочки и устройствах потоковой передачи WDM см. [в статье как устройства участвуют в графе фильтра](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="e9daa-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



| <span data-ttu-id="e9daa-114">Метка</span><span class="sxs-lookup"><span data-stu-id="e9daa-114">Label</span></span> | <span data-ttu-id="e9daa-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e9daa-115">Value</span></span> |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9daa-116">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="e9daa-116">Filter Interfaces</span></span>                        | <span data-ttu-id="e9daa-117">[**Иамкроссбар**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ИспеЦифипропертипажес, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="e9daa-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="e9daa-118">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="e9daa-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="e9daa-119">MEDIATYPE \_ аналогаудио, MediaType \_ аналогвидео</span><span class="sxs-lookup"><span data-stu-id="e9daa-119">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="e9daa-120">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="e9daa-120">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="e9daa-121">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="e9daa-121">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="e9daa-122">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="e9daa-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="e9daa-123">MEDIATYPE \_ аналогаудио, MediaType \_ аналогвидео</span><span class="sxs-lookup"><span data-stu-id="e9daa-123">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="e9daa-124">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="e9daa-124">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="e9daa-125">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="e9daa-125">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="e9daa-126">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="e9daa-126">Filter CLSID</span></span>                             | <span data-ttu-id="e9daa-127">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="e9daa-127">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="e9daa-128">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="e9daa-128">Property Page CLSID</span></span>                      | <span data-ttu-id="e9daa-129">\_КРОССБАРФИЛТЕРПРОПЕРТИПАЖЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="e9daa-129">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="e9daa-130">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="e9daa-130">Executable</span></span>                               | <span data-ttu-id="e9daa-131">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="e9daa-131">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="e9daa-132">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="e9daa-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="e9daa-133">Зависит от драйвера.</span><span class="sxs-lookup"><span data-stu-id="e9daa-133">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="e9daa-134">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="e9daa-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="e9daa-135">\_кскатегори \_ микшер</span><span class="sxs-lookup"><span data-stu-id="e9daa-135">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="e9daa-136">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e9daa-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9daa-137">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="e9daa-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="e9daa-138">Работа с микшерами</span><span class="sxs-lookup"><span data-stu-id="e9daa-138">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



