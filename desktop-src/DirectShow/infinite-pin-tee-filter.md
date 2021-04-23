---
description: Фильтр неограниченного ПИН-кода Tee
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Фильтр неограниченного ПИН-кода Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909232"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="8f88e-103">Фильтр неограниченного ПИН-кода Tee</span><span class="sxs-lookup"><span data-stu-id="8f88e-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="8f88e-104">Этот фильтр доставляет образцы, доставляемые на входные контакты, в переменное число заголовков выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8f88e-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="8f88e-105">При создании экземпляра фильтра он имеет один выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8f88e-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="8f88e-106">Каждый раз при подключении выходного контакта фильтр создает другой выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8f88e-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="8f88e-107">Все выходные сигналы имеют тот же тип носителя, что и входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8f88e-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="8f88e-108">Версия этого фильтра также предоставляется в виде примера пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="8f88e-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="8f88e-109">См. [Пример фильтра инфти](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="8f88e-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



| <span data-ttu-id="8f88e-110">Метка</span><span class="sxs-lookup"><span data-stu-id="8f88e-110">Label</span></span> | <span data-ttu-id="8f88e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="8f88e-111">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f88e-112">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="8f88e-112">Filter Interfaces</span></span>                        | [<span data-ttu-id="8f88e-113">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="8f88e-113">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="8f88e-114">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8f88e-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="8f88e-115">Любой тип мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8f88e-115">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="8f88e-116">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8f88e-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="8f88e-117">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8f88e-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="8f88e-118">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8f88e-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="8f88e-119">Любой тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8f88e-119">Any media type.</span></span> <span data-ttu-id="8f88e-120">Тип выходных данных всегда соответствует типу входных данных для всех закрепления вывода.</span><span class="sxs-lookup"><span data-stu-id="8f88e-120">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="8f88e-121">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8f88e-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="8f88e-122">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8f88e-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="8f88e-123">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="8f88e-123">Filter CLSID</span></span>                             | <span data-ttu-id="8f88e-124">\_ИНФТИ CLSID</span><span class="sxs-lookup"><span data-stu-id="8f88e-124">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="8f88e-125">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="8f88e-125">Property Page CLSID</span></span>                      | <span data-ttu-id="8f88e-126">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="8f88e-126">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="8f88e-127">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="8f88e-127">Executable</span></span>                               | <span data-ttu-id="8f88e-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="8f88e-128">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="8f88e-129">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="8f88e-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="8f88e-130">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="8f88e-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="8f88e-131">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="8f88e-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8f88e-132">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="8f88e-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="8f88e-133">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8f88e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f88e-134">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="8f88e-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



