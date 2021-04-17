---
description: О примерах носителей и распределителях
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: О примерах носителей и распределителях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684739"
---
# <a name="about-media-samples-and-allocators"></a><span data-ttu-id="7858d-103">О примерах носителей и распределителях</span><span class="sxs-lookup"><span data-stu-id="7858d-103">About Media Samples and Allocators</span></span>

<span data-ttu-id="7858d-104">Фильтры обеспечивают доставку данных по ПИН-соединениям.</span><span class="sxs-lookup"><span data-stu-id="7858d-104">Filters deliver data across pin connections.</span></span> <span data-ttu-id="7858d-105">Данные перемещаются из выходного контакта одного фильтра в входной ПИН-код другого фильтра.</span><span class="sxs-lookup"><span data-stu-id="7858d-105">Data moves from the output pin of one filter to the input pin of another filter.</span></span> <span data-ttu-id="7858d-106">Наиболее распространенным способом для доставки данных является вызов метода [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) на входе, хотя также существуют и некоторые другие механизмы.</span><span class="sxs-lookup"><span data-stu-id="7858d-106">The most common way for the output pin to deliver the data is by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input, although a few other mechanisms exist as well.</span></span>

<span data-ttu-id="7858d-107">В зависимости от фильтра память для данных мультимедиа может быть распределена различными способами: в куче, на поверхности DirectDraw, с использованием общей памяти GDI или с помощью другого механизма выделения.</span><span class="sxs-lookup"><span data-stu-id="7858d-107">Depending on the filter, memory for the media data can be allocated in various ways: on the heap, in a DirectDraw surface, using shared GDI memory, or using some other allocation mechanism.</span></span> <span data-ttu-id="7858d-108">Объект, ответственный за выделение памяти, называется *распределителем*, который представляет собой COM-объект, предоставляющий интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="7858d-108">The object responsible for allocating the memory is called an *allocator*, which is a COM object that exposes the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="7858d-109">При подключении двух контактов один из ПИН-кодов должен предоставлять распределитель.</span><span class="sxs-lookup"><span data-stu-id="7858d-109">When two pins connect, one of the pins must provide an allocator.</span></span> <span data-ttu-id="7858d-110">DirectShow определяет последовательность вызовов методов, которая используется для определения того, какой ПИН-код предоставляет распределитель.</span><span class="sxs-lookup"><span data-stu-id="7858d-110">DirectShow defines a sequence of method calls that is used to establish which pin provides the allocator.</span></span> <span data-ttu-id="7858d-111">ПИН-коды также договариваются о количестве буферов, которые будут созданы распределителем, и размере буферов.</span><span class="sxs-lookup"><span data-stu-id="7858d-111">The pins also agree on the number of buffers that the allocator will create, and the size of the buffers.</span></span>

<span data-ttu-id="7858d-112">Перед началом потоковой передачи распределитель создает пул буферов.</span><span class="sxs-lookup"><span data-stu-id="7858d-112">Before streaming begins, the allocator creates a pool of buffers.</span></span> <span data-ttu-id="7858d-113">Во время потоковой передачи вышестоящий фильтр заполняет буферы данными и доставляет их в нисходящий фильтр.</span><span class="sxs-lookup"><span data-stu-id="7858d-113">During streaming, the upstream filter fills buffers with data and delivers them to the downstream filter.</span></span> <span data-ttu-id="7858d-114">Но вышестоящий фильтр не предоставляет необработанные указатели подчиненного фильтра для буферов.</span><span class="sxs-lookup"><span data-stu-id="7858d-114">But the upstream filter does not give the downstream filter raw pointers to the buffers.</span></span> <span data-ttu-id="7858d-115">Вместо этого он использует COM-объекты, называемые *примерами мультимедиа*, которые распределитель создает для управления буферами.</span><span class="sxs-lookup"><span data-stu-id="7858d-115">Instead, it uses COM objects called *media samples*, which the allocator creates to manage the buffers.</span></span> <span data-ttu-id="7858d-116">Примеры носителей предоставляют интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="7858d-116">Media samples expose the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="7858d-117">Пример носителя содержит:</span><span class="sxs-lookup"><span data-stu-id="7858d-117">A media sample contains:</span></span>

-   <span data-ttu-id="7858d-118">Указатель на базовый буфер</span><span class="sxs-lookup"><span data-stu-id="7858d-118">a pointer to the underlying buffer</span></span>
-   <span data-ttu-id="7858d-119">Метка времени</span><span class="sxs-lookup"><span data-stu-id="7858d-119">a time stamp</span></span>
-   <span data-ttu-id="7858d-120">различные флаги</span><span class="sxs-lookup"><span data-stu-id="7858d-120">various flags</span></span>
-   <span data-ttu-id="7858d-121">При необходимости тип мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7858d-121">optionally, a media type</span></span>

<span data-ttu-id="7858d-122">Метка времени определяет время презентации, используемое фильтром модуля подготовки отчетов для планирования подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="7858d-122">The time stamp defines the presentation time, which the renderer filter uses to schedule rendering.</span></span> <span data-ttu-id="7858d-123">Флаги указывают на такие вещи, как наличие перерыва в данных с момента предыдущего примера.</span><span class="sxs-lookup"><span data-stu-id="7858d-123">The flags indicate things like whether there was a break in the data since the previous sample.</span></span> <span data-ttu-id="7858d-124">Тип мультимедиа позволяет фильтрам изменять форматы среднего потока.</span><span class="sxs-lookup"><span data-stu-id="7858d-124">The media type provides a way for filters to change formats mid-stream.</span></span> <span data-ttu-id="7858d-125">Обычно образец не имеет типа мультимедиа, что означает, что этот формат не изменился со времени предыдущего примера.</span><span class="sxs-lookup"><span data-stu-id="7858d-125">Usually, the sample has no media type, which indicates that the format has not changed since the previous sample.</span></span>

<span data-ttu-id="7858d-126">Хотя фильтр использует буфер, он содержит счетчик ссылок на выборку.</span><span class="sxs-lookup"><span data-stu-id="7858d-126">While a filter is using a buffer, it holds reference count on the sample.</span></span> <span data-ttu-id="7858d-127">Распределитель использует счетчик ссылок, чтобы определить, когда он может повторно использовать буфер.</span><span class="sxs-lookup"><span data-stu-id="7858d-127">The allocator uses the reference count to determine when it can re-use the buffer.</span></span> <span data-ttu-id="7858d-128">Это предотвращает перезапись буфера, который по-прежнему используется другим фильтром, в фильтре.</span><span class="sxs-lookup"><span data-stu-id="7858d-128">This prevents a filter from overwriting a buffer that another filter is still using.</span></span> <span data-ttu-id="7858d-129">Пример не возвращает доступ к пулу доступных выборок распределителя, пока не будет выпущен каждый фильтр.</span><span class="sxs-lookup"><span data-stu-id="7858d-129">A sample does not return to the allocator's pool of available samples until every filter has released it.</span></span>

<span data-ttu-id="7858d-130">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7858d-130">For more information, see the following topics:</span></span>

-   <span data-ttu-id="7858d-131">В разделах [Samples and распределительы](samples-and-allocators.md) содержится более подробное описание работы распределительов.</span><span class="sxs-lookup"><span data-stu-id="7858d-131">The topic [Samples and Allocators](samples-and-allocators.md) provides a more detailed description of how allocators work.</span></span>
-   <span data-ttu-id="7858d-132">В разделе [поток данных в графе фильтра](data-flow-in-the-filter-graph.md) представлены общие сведения о потоке данных в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7858d-132">The topic [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) gives a general overview of data flow in DirectShow.</span></span>

<span data-ttu-id="7858d-133">Следующие разделы предназначены для разработчиков, создающих собственные настраиваемые фильтры:</span><span class="sxs-lookup"><span data-stu-id="7858d-133">The following topics are intended for developers who are writing their own custom filters:</span></span>

-   [<span data-ttu-id="7858d-134">Поток данных для разработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="7858d-134">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="7858d-135">Потоки и критические разделы</span><span class="sxs-lookup"><span data-stu-id="7858d-135">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

## <a name="related-topics"></a><span data-ttu-id="7858d-136">См. также</span><span class="sxs-lookup"><span data-stu-id="7858d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7858d-137">Граф фильтра и его компоненты</span><span class="sxs-lookup"><span data-stu-id="7858d-137">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



