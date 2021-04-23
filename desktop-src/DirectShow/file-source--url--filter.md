---
description: Фильтр источника файлов (URL-адрес)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Фильтр источника файлов (URL-адрес)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909242"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="15daa-103">Фильтр источника файлов (URL-адрес)</span><span class="sxs-lookup"><span data-stu-id="15daa-103">File Source (URL) Filter</span></span>

<span data-ttu-id="15daa-104">Фильтр источников файлов URL-адресов — это универсальный асинхронный фильтр источника, который работает с любым исходным файлом, который может идентифицироваться по универсальному указателю ресурсов (URL), а основной тип носителя — Stream.</span><span class="sxs-lookup"><span data-stu-id="15daa-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="15daa-105">Сюда входят файлы AVI, MOV, MPEG и WAV.</span><span class="sxs-lookup"><span data-stu-id="15daa-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="15daa-106">Для этого требуется, чтобы подчиненный фильтр был синтаксическим анализатором, таким как [Разделитель потока MPEG-1](mpeg-1-stream-splitter-filter.md), [Разделитель AVI](avi-splitter-filter.md)или [средство синтаксического анализа фильмов QuickTime](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="15daa-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



| <span data-ttu-id="15daa-107">Метка</span><span class="sxs-lookup"><span data-stu-id="15daa-107">Label</span></span> | <span data-ttu-id="15daa-108">Значение</span><span class="sxs-lookup"><span data-stu-id="15daa-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15daa-109">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="15daa-109">Filter Interfaces</span></span>                        | <span data-ttu-id="15daa-110">[**Иамопенпрогресс**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="15daa-110">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="15daa-111">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="15daa-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="15daa-112">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="15daa-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="15daa-113">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="15daa-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="15daa-114">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="15daa-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="15daa-115">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="15daa-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="15daa-116">\_Поток MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="15daa-116">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="15daa-117">Подтип зависит от формата мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="15daa-117">The subtype depends on the media format.</span></span> <span data-ttu-id="15daa-118">(МЕДИАСУБТИПЕ \_ Значение NULL, если фильтр не распознает формат.)</span><span class="sxs-lookup"><span data-stu-id="15daa-118">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="15daa-119">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="15daa-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="15daa-120">[**Иамасинкреадертиместампскалинг**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="15daa-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="15daa-121">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="15daa-121">Filter CLSID</span></span>                             | <span data-ttu-id="15daa-122">\_УРЛРЕАДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="15daa-122">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="15daa-123">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="15daa-123">Property Page CLSID</span></span>                      | <span data-ttu-id="15daa-124">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="15daa-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="15daa-125">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="15daa-125">Executable</span></span>                               | <span data-ttu-id="15daa-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="15daa-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="15daa-127">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="15daa-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="15daa-128">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="15daa-128">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="15daa-129">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="15daa-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="15daa-130">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="15daa-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="15daa-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15daa-131">Remarks</span></span>

<span data-ttu-id="15daa-132">Этот фильтр использует URLMon и поддерживает кодовые страницы.</span><span class="sxs-lookup"><span data-stu-id="15daa-132">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15daa-133">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="15daa-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15daa-134">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="15daa-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



