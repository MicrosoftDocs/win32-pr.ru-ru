---
description: Фильтр ТВ-тюнера
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Фильтр ТВ-тюнера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909032"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="b27c2-103">Фильтр ТВ-тюнера</span><span class="sxs-lookup"><span data-stu-id="b27c2-103">TV Tuner Filter</span></span>

<span data-ttu-id="b27c2-104">Фильтр ТВ-тюнера выбирает аналоговый канал вещания или кабель для просмотра.</span><span class="sxs-lookup"><span data-stu-id="b27c2-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="b27c2-105">Один выходной поток — это аппаратный путь для аналогового видео басебанд.</span><span class="sxs-lookup"><span data-stu-id="b27c2-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="b27c2-106">Эти выходные данные должны быть подключены к фильтру аналогового микшера видео.</span><span class="sxs-lookup"><span data-stu-id="b27c2-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="b27c2-107">Входные контакты включают входные данные для кабеля и входной антенны.</span><span class="sxs-lookup"><span data-stu-id="b27c2-107">The input pins include an input for cable and an antenna input.</span></span>



| <span data-ttu-id="b27c2-108">Метка</span><span class="sxs-lookup"><span data-stu-id="b27c2-108">Label</span></span> | <span data-ttu-id="b27c2-109">Значение</span><span class="sxs-lookup"><span data-stu-id="b27c2-109">Value</span></span> |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b27c2-110">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="b27c2-110">Filter Interfaces</span></span>                        | <span data-ttu-id="b27c2-111">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**иамтвтунер**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **испеЦифипропертипажес**, **IPersistPropertyBag**, **иксобжект**, [**икспропертисет**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="b27c2-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="b27c2-112">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="b27c2-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="b27c2-113">Не применяется</span><span class="sxs-lookup"><span data-stu-id="b27c2-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="b27c2-114">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="b27c2-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="b27c2-115">Не применяется</span><span class="sxs-lookup"><span data-stu-id="b27c2-115">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="b27c2-116">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="b27c2-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="b27c2-117">Видео: MEDIATYPE \_ аналогвидео, КСДАТАФОРМАТ \_ подтип \_ None Audio: MEDIATYPE \_ аналогаудио, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="b27c2-117">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="b27c2-118">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="b27c2-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="b27c2-119">**ипин**</span><span class="sxs-lookup"><span data-stu-id="b27c2-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="b27c2-120">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="b27c2-120">Filter CLSID</span></span>                             | <span data-ttu-id="b27c2-121">\_ТВТУНЕРФИЛТЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="b27c2-121">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="b27c2-122">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="b27c2-122">Property Page CLSID</span></span>                      | <span data-ttu-id="b27c2-123">\_ТВТУНЕРФИЛТЕРПРОПЕРТИПАЖЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="b27c2-123">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="b27c2-124">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="b27c2-124">Executable</span></span>                               | <span data-ttu-id="b27c2-125">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="b27c2-125">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="b27c2-126">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="b27c2-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="b27c2-127">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="b27c2-127">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="b27c2-128">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="b27c2-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b27c2-129">\_кскатегори \_ твтунер</span><span class="sxs-lookup"><span data-stu-id="b27c2-129">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="b27c2-130">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b27c2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b27c2-131">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="b27c2-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



