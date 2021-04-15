---
description: Фильтр неограниченного ПИН-кода Tee
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Фильтр неограниченного ПИН-кода Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423006"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="8c745-103">Фильтр неограниченного ПИН-кода Tee</span><span class="sxs-lookup"><span data-stu-id="8c745-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="8c745-104">Этот фильтр доставляет образцы, доставляемые на входные контакты, в переменное число заголовков выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8c745-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="8c745-105">При создании экземпляра фильтра он имеет один выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8c745-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="8c745-106">Каждый раз при подключении выходного контакта фильтр создает другой выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8c745-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="8c745-107">Все выходные сигналы имеют тот же тип носителя, что и входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="8c745-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="8c745-108">Версия этого фильтра также предоставляется в виде примера пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="8c745-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="8c745-109">См. [Пример фильтра инфти](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="8c745-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c745-110">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="8c745-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="8c745-111">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="8c745-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="8c745-112">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8c745-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="8c745-113">Любой тип мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8c745-113">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="8c745-114">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8c745-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="8c745-115">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8c745-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="8c745-116">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8c745-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="8c745-117">Любой тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8c745-117">Any media type.</span></span> <span data-ttu-id="8c745-118">Тип выходных данных всегда соответствует типу входных данных для всех закрепления вывода.</span><span class="sxs-lookup"><span data-stu-id="8c745-118">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="8c745-119">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8c745-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="8c745-120">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8c745-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="8c745-121">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="8c745-121">Filter CLSID</span></span>                             | <span data-ttu-id="8c745-122">\_ИНФТИ CLSID</span><span class="sxs-lookup"><span data-stu-id="8c745-122">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="8c745-123">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="8c745-123">Property Page CLSID</span></span>                      | <span data-ttu-id="8c745-124">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="8c745-124">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="8c745-125">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="8c745-125">Executable</span></span>                               | <span data-ttu-id="8c745-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="8c745-126">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="8c745-127">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="8c745-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="8c745-128">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="8c745-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="8c745-129">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="8c745-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8c745-130">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="8c745-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="8c745-131">См. также</span><span class="sxs-lookup"><span data-stu-id="8c745-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c745-132">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="8c745-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



