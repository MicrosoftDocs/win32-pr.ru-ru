---
description: Фильтр по источнику файлов (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Фильтр по источнику файлов (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494988"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="e5b7e-103">Фильтр по источнику файлов (Async)</span><span class="sxs-lookup"><span data-stu-id="e5b7e-103">File Source (Async) Filter</span></span>

<span data-ttu-id="e5b7e-104">Фильтр "асинхронный источник файлов" открывает и считывает локальные файлы различных форматов данных и передает их в фильтр анализатора.</span><span class="sxs-lookup"><span data-stu-id="e5b7e-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="e5b7e-105">Чтобы загрузить файлы мультимедиа из Интернета по протоколу HTTP, используйте фильтр " [источник файлов (URL-адрес)](file-source--url--filter.md) ".</span><span class="sxs-lookup"><span data-stu-id="e5b7e-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="e5b7e-106">Для чтения файлов ASF используйте фильтр [чтения WM ASF](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b7e-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b7e-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="e5b7e-107">Filter Interfaces</span></span>                        | <span data-ttu-id="e5b7e-108">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="e5b7e-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="e5b7e-109">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="e5b7e-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="e5b7e-110">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="e5b7e-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="e5b7e-111">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="e5b7e-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="e5b7e-112">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="e5b7e-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="e5b7e-113">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="e5b7e-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="e5b7e-114">**MEDIATYPE \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="e5b7e-114">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="e5b7e-115">Подтип зависит от формата мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e5b7e-115">The subtype depends on the media format.</span></span> <span data-ttu-id="e5b7e-116">(**Медиасубтипе \_ null** , если фильтр не распознает формат.)</span><span class="sxs-lookup"><span data-stu-id="e5b7e-116">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="e5b7e-117">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="e5b7e-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="e5b7e-118">[**Иамасинкреадертиместампскалинг**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="e5b7e-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="e5b7e-119">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="e5b7e-119">Filter CLSID</span></span>                             | <span data-ttu-id="e5b7e-120">**\_АСИНКРЕАДЕР CLSID**</span><span class="sxs-lookup"><span data-stu-id="e5b7e-120">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="e5b7e-121">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="e5b7e-121">Property Page CLSID</span></span>                      | <span data-ttu-id="e5b7e-122">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="e5b7e-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="e5b7e-123">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="e5b7e-123">Executable</span></span>                               | <span data-ttu-id="e5b7e-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="e5b7e-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="e5b7e-125">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="e5b7e-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="e5b7e-126">**\_маловероятно**</span><span class="sxs-lookup"><span data-stu-id="e5b7e-126">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="e5b7e-127">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="e5b7e-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="e5b7e-128">**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="e5b7e-128">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e5b7e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e5b7e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5b7e-130">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="e5b7e-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



