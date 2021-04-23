---
description: Фильтр по источнику файлов (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Фильтр по источнику файлов (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909702"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="8668c-103">Фильтр по источнику файлов (Async)</span><span class="sxs-lookup"><span data-stu-id="8668c-103">File Source (Async) Filter</span></span>

<span data-ttu-id="8668c-104">Фильтр "асинхронный источник файлов" открывает и считывает локальные файлы различных форматов данных и передает их в фильтр анализатора.</span><span class="sxs-lookup"><span data-stu-id="8668c-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="8668c-105">Чтобы загрузить файлы мультимедиа из Интернета по протоколу HTTP, используйте фильтр " [источник файлов (URL-адрес)](file-source--url--filter.md) ".</span><span class="sxs-lookup"><span data-stu-id="8668c-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="8668c-106">Для чтения файлов ASF используйте фильтр [чтения WM ASF](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8668c-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



| <span data-ttu-id="8668c-107">Метка</span><span class="sxs-lookup"><span data-stu-id="8668c-107">Label</span></span> | <span data-ttu-id="8668c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8668c-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8668c-109">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="8668c-109">Filter Interfaces</span></span>                        | <span data-ttu-id="8668c-110">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="8668c-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="8668c-111">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8668c-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="8668c-112">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8668c-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="8668c-113">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8668c-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="8668c-114">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8668c-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="8668c-115">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8668c-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="8668c-116">**MEDIATYPE \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="8668c-116">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="8668c-117">Подтип зависит от формата мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8668c-117">The subtype depends on the media format.</span></span> <span data-ttu-id="8668c-118">(**Медиасубтипе \_ null** , если фильтр не распознает формат.)</span><span class="sxs-lookup"><span data-stu-id="8668c-118">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="8668c-119">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8668c-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="8668c-120">[**Иамасинкреадертиместампскалинг**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="8668c-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="8668c-121">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="8668c-121">Filter CLSID</span></span>                             | <span data-ttu-id="8668c-122">**\_АСИНКРЕАДЕР CLSID**</span><span class="sxs-lookup"><span data-stu-id="8668c-122">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="8668c-123">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="8668c-123">Property Page CLSID</span></span>                      | <span data-ttu-id="8668c-124">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="8668c-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="8668c-125">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="8668c-125">Executable</span></span>                               | <span data-ttu-id="8668c-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="8668c-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="8668c-127">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="8668c-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="8668c-128">**\_маловероятно**</span><span class="sxs-lookup"><span data-stu-id="8668c-128">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="8668c-129">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="8668c-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8668c-130">**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="8668c-130">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="8668c-131">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8668c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8668c-132">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="8668c-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



