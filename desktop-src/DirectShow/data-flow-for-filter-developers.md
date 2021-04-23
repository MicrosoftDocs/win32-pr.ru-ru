---
description: Поток данных для разработчиков фильтров
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Поток данных для разработчиков фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072314"
---
# <a name="data-flow-for-filter-developers"></a><span data-ttu-id="b892f-103">Поток данных для разработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="b892f-103">Data Flow for Filter Developers</span></span>

<span data-ttu-id="b892f-104">В этом разделе подробно описывается перемещение данных с помощью графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="b892f-104">This section describes in detail how data moves through the filter graph.</span></span> <span data-ttu-id="b892f-105">Он посвящен транспорту локальной памяти с помощью интерфейса [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) или [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="b892f-105">It focuses on local memory transport using the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) or [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="b892f-106">Он предназначен для разработчиков, создающих собственные настраиваемые фильтры.</span><span class="sxs-lookup"><span data-stu-id="b892f-106">It is intended for developers who are writing their own custom filters.</span></span> <span data-ttu-id="b892f-107">Общие сведения о том, как Microsoft DirectShow обрабатывает поток данных, см. [в разделе поток данных в графе фильтра](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="b892f-107">For a general introduction to how Microsoft DirectShow handles data flow, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="b892f-108">Большое количество данных перемещается через граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="b892f-108">A lot of data moves through a filter graph.</span></span> <span data-ttu-id="b892f-109">Он делится на две категории: данные мультимедиа и управляющие данные.</span><span class="sxs-lookup"><span data-stu-id="b892f-109">It falls roughly into two categories: media data and control data.</span></span> <span data-ttu-id="b892f-110">Как правило, данные мультимедиа перемещаются в нисходящий поток, а управление данными перемещается вверх.</span><span class="sxs-lookup"><span data-stu-id="b892f-110">In general, media data travels downstream and control data travels upstream.</span></span> <span data-ttu-id="b892f-111">Данные мультимедиа включают видеокадры, образцы аудио, пакеты MPEG и так далее, которые составляют поток, но также включают команды Flush, уведомления конца потока и другие данные, передаваемые в поток.</span><span class="sxs-lookup"><span data-stu-id="b892f-111">Media data includes the video frames, audio samples, MPEG packets, and so forth that make up a stream, but also includes flush commands, end-of-stream notifications, and other data that travels with the stream.</span></span> <span data-ttu-id="b892f-112">Управляющие данные не являются частью потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b892f-112">Control data is not part of the media stream.</span></span> <span data-ttu-id="b892f-113">Примерами управляющих данных являются запросы контроля качества и команды поиска.</span><span class="sxs-lookup"><span data-stu-id="b892f-113">Examples of control data are quality-control requests and seek commands.</span></span>

<span data-ttu-id="b892f-114">Этот раздел содержит следующие статьи.</span><span class="sxs-lookup"><span data-stu-id="b892f-114">This section contains the following articles.</span></span>

-   [<span data-ttu-id="b892f-115">Доставка образцов</span><span class="sxs-lookup"><span data-stu-id="b892f-115">Delivering Samples</span></span>](delivering-samples.md)
-   [<span data-ttu-id="b892f-116">Обработка данных</span><span class="sxs-lookup"><span data-stu-id="b892f-116">Processing Data</span></span>](processing-data.md)
-   [<span data-ttu-id="b892f-117">Уведомления о завершении потока</span><span class="sxs-lookup"><span data-stu-id="b892f-117">End-of-Stream Notifications</span></span>](end-of-stream-notifications.md)
-   [<span data-ttu-id="b892f-118">Новые сегменты</span><span class="sxs-lookup"><span data-stu-id="b892f-118">New Segments</span></span>](new-segments.md)
-   [<span data-ttu-id="b892f-119">Очистки</span><span class="sxs-lookup"><span data-stu-id="b892f-119">Flushing</span></span>](flushing.md)
-   [<span data-ttu-id="b892f-120">Нужна</span><span class="sxs-lookup"><span data-stu-id="b892f-120">Seeking</span></span>](seeking.md)
-   [<span data-ttu-id="b892f-121">Изменения динамического формата</span><span class="sxs-lookup"><span data-stu-id="b892f-121">Dynamic Format Changes</span></span>](dynamic-format-changes.md)

## <a name="related-topics"></a><span data-ttu-id="b892f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b892f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b892f-123">Управление качеством</span><span class="sxs-lookup"><span data-stu-id="b892f-123">Quality-Control Management</span></span>](quality-control-management.md)
</dt> <dt>

[<span data-ttu-id="b892f-124">Потоки и критические разделы</span><span class="sxs-lookup"><span data-stu-id="b892f-124">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> <dt>

[<span data-ttu-id="b892f-125">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="b892f-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



