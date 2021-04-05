---
description: Фильтр источника файлов (URL-адрес)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Фильтр источника файлов (URL-адрес)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140390"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="07b14-103">Фильтр источника файлов (URL-адрес)</span><span class="sxs-lookup"><span data-stu-id="07b14-103">File Source (URL) Filter</span></span>

<span data-ttu-id="07b14-104">Фильтр источников файлов URL-адресов — это универсальный асинхронный фильтр источника, который работает с любым исходным файлом, который может идентифицироваться по универсальному указателю ресурсов (URL), а основной тип носителя — Stream.</span><span class="sxs-lookup"><span data-stu-id="07b14-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="07b14-105">Сюда входят файлы AVI, MOV, MPEG и WAV.</span><span class="sxs-lookup"><span data-stu-id="07b14-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="07b14-106">Для этого требуется, чтобы подчиненный фильтр был синтаксическим анализатором, таким как [Разделитель потока MPEG-1](mpeg-1-stream-splitter-filter.md), [Разделитель AVI](avi-splitter-filter.md)или [средство синтаксического анализа фильмов QuickTime](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="07b14-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b14-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="07b14-107">Filter Interfaces</span></span>                        | <span data-ttu-id="07b14-108">[**Иамопенпрогресс**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="07b14-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="07b14-109">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="07b14-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="07b14-110">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="07b14-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="07b14-111">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="07b14-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="07b14-112">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="07b14-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="07b14-113">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="07b14-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="07b14-114">\_Поток MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="07b14-114">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="07b14-115">Подтип зависит от формата мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="07b14-115">The subtype depends on the media format.</span></span> <span data-ttu-id="07b14-116">(МЕДИАСУБТИПЕ \_ Значение NULL, если фильтр не распознает формат.)</span><span class="sxs-lookup"><span data-stu-id="07b14-116">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="07b14-117">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="07b14-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="07b14-118">[**Иамасинкреадертиместампскалинг**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="07b14-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="07b14-119">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="07b14-119">Filter CLSID</span></span>                             | <span data-ttu-id="07b14-120">\_УРЛРЕАДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="07b14-120">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="07b14-121">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="07b14-121">Property Page CLSID</span></span>                      | <span data-ttu-id="07b14-122">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="07b14-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="07b14-123">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="07b14-123">Executable</span></span>                               | <span data-ttu-id="07b14-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="07b14-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="07b14-125">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="07b14-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="07b14-126">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="07b14-126">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="07b14-127">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="07b14-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="07b14-128">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="07b14-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="07b14-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07b14-129">Remarks</span></span>

<span data-ttu-id="07b14-130">Этот фильтр использует URLMon и поддерживает кодовые страницы.</span><span class="sxs-lookup"><span data-stu-id="07b14-130">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07b14-131">См. также</span><span class="sxs-lookup"><span data-stu-id="07b14-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07b14-132">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="07b14-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



