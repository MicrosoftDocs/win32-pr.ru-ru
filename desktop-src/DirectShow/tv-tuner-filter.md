---
description: Фильтр ТВ-тюнера
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Фильтр ТВ-тюнера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348555"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="5618b-103">Фильтр ТВ-тюнера</span><span class="sxs-lookup"><span data-stu-id="5618b-103">TV Tuner Filter</span></span>

<span data-ttu-id="5618b-104">Фильтр ТВ-тюнера выбирает аналоговый канал вещания или кабель для просмотра.</span><span class="sxs-lookup"><span data-stu-id="5618b-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="5618b-105">Один выходной поток — это аппаратный путь для аналогового видео басебанд.</span><span class="sxs-lookup"><span data-stu-id="5618b-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="5618b-106">Эти выходные данные должны быть подключены к фильтру аналогового микшера видео.</span><span class="sxs-lookup"><span data-stu-id="5618b-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="5618b-107">Входные контакты включают входные данные для кабеля и входной антенны.</span><span class="sxs-lookup"><span data-stu-id="5618b-107">The input pins include an input for cable and an antenna input.</span></span>



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5618b-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="5618b-108">Filter Interfaces</span></span>                        | <span data-ttu-id="5618b-109">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**иамтвтунер**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **испеЦифипропертипажес**, **IPersistPropertyBag**, **иксобжект**, [**икспропертисет**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="5618b-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="5618b-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="5618b-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="5618b-111">Не применяется</span><span class="sxs-lookup"><span data-stu-id="5618b-111">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="5618b-112">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="5618b-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="5618b-113">Не применяется</span><span class="sxs-lookup"><span data-stu-id="5618b-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="5618b-114">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="5618b-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="5618b-115">Видео: MEDIATYPE \_ аналогвидео, КСДАТАФОРМАТ \_ подтип \_ None Audio: MEDIATYPE \_ аналогаудио, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="5618b-115">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="5618b-116">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="5618b-116">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="5618b-117">**ипин**</span><span class="sxs-lookup"><span data-stu-id="5618b-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="5618b-118">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="5618b-118">Filter CLSID</span></span>                             | <span data-ttu-id="5618b-119">\_ТВТУНЕРФИЛТЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="5618b-119">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="5618b-120">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="5618b-120">Property Page CLSID</span></span>                      | <span data-ttu-id="5618b-121">\_ТВТУНЕРФИЛТЕРПРОПЕРТИПАЖЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="5618b-121">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="5618b-122">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="5618b-122">Executable</span></span>                               | <span data-ttu-id="5618b-123">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="5618b-123">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="5618b-124">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="5618b-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="5618b-125">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="5618b-125">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="5618b-126">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="5618b-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="5618b-127">\_кскатегори \_ твтунер</span><span class="sxs-lookup"><span data-stu-id="5618b-127">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="5618b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5618b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5618b-129">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="5618b-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



