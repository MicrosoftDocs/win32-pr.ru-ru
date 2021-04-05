---
description: Фильтр аналогового микшера видео
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Фильтр аналогового микшера видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990076"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="69108-103">Фильтр аналогового микшера видео</span><span class="sxs-lookup"><span data-stu-id="69108-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="69108-104">Фильтр аналогового микшера видео представляет микшер видео на устройстве видеозаписи, поддерживающем WDM (WDM).</span><span class="sxs-lookup"><span data-stu-id="69108-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="69108-105">Этот фильтр является фильтром оболочки для микширования на устройствах потоковой передачи WDM.</span><span class="sxs-lookup"><span data-stu-id="69108-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="69108-106">Понятное имя фильтра берется с устройства.</span><span class="sxs-lookup"><span data-stu-id="69108-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="69108-107">Каждый выходной ПИН-код представляет собой аппаратный путь для аналогового видео басебанд.</span><span class="sxs-lookup"><span data-stu-id="69108-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="69108-108">Один из входных контактов поступает из ТВ-тюнера ( [фильтра ТВ-тюнера](tv-tuner-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="69108-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="69108-109">Другие входные ПИН-коды поддерживают видео-или звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="69108-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="69108-110">Фильтр поддерживает все типы мультимедиа и форматы, которые поддерживаются в подчиненных соединениях.</span><span class="sxs-lookup"><span data-stu-id="69108-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="69108-111">Этот фильтр нельзя создать напрямую с помощью CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="69108-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="69108-112">Интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) автоматически добавляет этот фильтр к графу по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="69108-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="69108-113">Дополнительные сведения о фильтрах оболочки и устройствах потоковой передачи WDM см. [в статье как устройства участвуют в графе фильтра](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="69108-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69108-114">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="69108-114">Filter Interfaces</span></span>                        | <span data-ttu-id="69108-115">[**Иамкроссбар**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ИспеЦифипропертипажес, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="69108-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="69108-116">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="69108-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="69108-117">MEDIATYPE \_ аналогаудио, MediaType \_ аналогвидео</span><span class="sxs-lookup"><span data-stu-id="69108-117">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="69108-118">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="69108-118">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="69108-119">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="69108-119">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="69108-120">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="69108-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="69108-121">MEDIATYPE \_ аналогаудио, MediaType \_ аналогвидео</span><span class="sxs-lookup"><span data-stu-id="69108-121">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="69108-122">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="69108-122">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="69108-123">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="69108-123">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="69108-124">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="69108-124">Filter CLSID</span></span>                             | <span data-ttu-id="69108-125">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="69108-125">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="69108-126">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="69108-126">Property Page CLSID</span></span>                      | <span data-ttu-id="69108-127">\_КРОССБАРФИЛТЕРПРОПЕРТИПАЖЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="69108-127">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="69108-128">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="69108-128">Executable</span></span>                               | <span data-ttu-id="69108-129">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="69108-129">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="69108-130">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="69108-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="69108-131">Зависит от драйвера.</span><span class="sxs-lookup"><span data-stu-id="69108-131">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="69108-132">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="69108-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="69108-133">\_кскатегори \_ микшер</span><span class="sxs-lookup"><span data-stu-id="69108-133">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="69108-134">См. также</span><span class="sxs-lookup"><span data-stu-id="69108-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69108-135">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="69108-135">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="69108-136">Работа с микшерами</span><span class="sxs-lookup"><span data-stu-id="69108-136">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



