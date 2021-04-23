---
description: Потоки и критические разделы
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Потоки и критические разделы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350335"
---
# <a name="threads-and-critical-sections"></a><span data-ttu-id="b6e93-103">Потоки и критические разделы</span><span class="sxs-lookup"><span data-stu-id="b6e93-103">Threads and Critical Sections</span></span>

<span data-ttu-id="b6e93-104">В этом разделе описываются потоки в фильтрах DirectShow, а также действия, которые необходимо выполнить, чтобы избежать сбоев или взаимоблокировок в настраиваемом фильтре.</span><span class="sxs-lookup"><span data-stu-id="b6e93-104">This section describes threading in DirectShow filters, and the steps you should take to avoid crashes or deadlocks in a custom filter.</span></span>

<span data-ttu-id="b6e93-105">В примерах, приведенных в этом разделе, для иллюстрации кода, который необходимо написать, используется псевдокод.</span><span class="sxs-lookup"><span data-stu-id="b6e93-105">The examples in this section use pseudocode to illustrate the code you will need to write.</span></span> <span data-ttu-id="b6e93-106">Они предполагают, что настраиваемый фильтр использует классы, производные от базовых классов DirectShow, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b6e93-106">They assume that a custom filter is using classes derived from the DirectShow base classes, as follows:</span></span>

-   <span data-ttu-id="b6e93-107">Кминпутпин: является производным от [**кбасеинпутпин**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="b6e93-107">CMyInputPin: Derived from [**CBaseInputPin**](cbaseinputpin.md).</span></span>
-   <span data-ttu-id="b6e93-108">Кмйоутпутпин: является производным от [**кбасеаутпутпин**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="b6e93-108">CMyOutputPin: Derived from [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>
-   <span data-ttu-id="b6e93-109">Кмифилтер: является производным от [**кбасефилтер**](cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="b6e93-109">CMyFilter: Derived from [**CBaseFilter**](cbasefilter.md).</span></span>
-   <span data-ttu-id="b6e93-110">Кминпуталлокатор: распределитель входного контакта, производный от [**кмемаллокатор**](cmemallocator.md).</span><span class="sxs-lookup"><span data-stu-id="b6e93-110">CMyInputAllocator: The input pin's allocator, derived from [**CMemAllocator**](cmemallocator.md).</span></span> <span data-ttu-id="b6e93-111">Не каждому фильтру нужен пользовательский распределитель.</span><span class="sxs-lookup"><span data-stu-id="b6e93-111">Not every filter needs a custom allocator.</span></span> <span data-ttu-id="b6e93-112">Для многих фильтров достаточно класса **кмемаллокатор** .</span><span class="sxs-lookup"><span data-stu-id="b6e93-112">For many filters, the **CMemAllocator** class is sufficient.</span></span>

<span data-ttu-id="b6e93-113">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="b6e93-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="b6e93-114">Потоковая передача и потоки приложений</span><span class="sxs-lookup"><span data-stu-id="b6e93-114">The Streaming and Application Threads</span></span>](the-streaming-and-application-threads.md)
-   [<span data-ttu-id="b6e93-115">Переход в режим приостановки</span><span class="sxs-lookup"><span data-stu-id="b6e93-115">Pausing</span></span>](pausing.md)
-   [<span data-ttu-id="b6e93-116">Получение и доставка примеров</span><span class="sxs-lookup"><span data-stu-id="b6e93-116">Receiving and Delivering Samples</span></span>](receiving-and-delivering-samples.md)
-   [<span data-ttu-id="b6e93-117">Доставка конца потока</span><span class="sxs-lookup"><span data-stu-id="b6e93-117">Delivering the End of Stream</span></span>](delivering-the-end-of-stream.md)
-   [<span data-ttu-id="b6e93-118">Очистка данных</span><span class="sxs-lookup"><span data-stu-id="b6e93-118">Flushing Data</span></span>](flushing-data.md)
-   [<span data-ttu-id="b6e93-119">Остановка</span><span class="sxs-lookup"><span data-stu-id="b6e93-119">Stopping</span></span>](stopping.md)
-   [<span data-ttu-id="b6e93-120">Получение буферов</span><span class="sxs-lookup"><span data-stu-id="b6e93-120">Getting Buffers</span></span>](getting-buffers.md)
-   [<span data-ttu-id="b6e93-121">Потоковая передача потоков и диспетчер графа фильтров</span><span class="sxs-lookup"><span data-stu-id="b6e93-121">Streaming Threads and the Filter Graph Manager</span></span>](streaming-threads-and-the-filter-graph-manager.md)
-   [<span data-ttu-id="b6e93-122">Сводка по потокам фильтров</span><span class="sxs-lookup"><span data-stu-id="b6e93-122">Summary of Filter Threading</span></span>](summary-of-filter-threading.md)

## <a name="related-topics"></a><span data-ttu-id="b6e93-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b6e93-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6e93-124">Поток данных для разработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="b6e93-124">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="b6e93-125">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="b6e93-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



