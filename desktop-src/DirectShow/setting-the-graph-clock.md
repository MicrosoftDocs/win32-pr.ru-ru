---
description: Настройка часов графа
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Настройка часов графа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682173"
---
# <a name="setting-the-graph-clock"></a><span data-ttu-id="c1b1e-103">Настройка часов графа</span><span class="sxs-lookup"><span data-stu-id="c1b1e-103">Setting the Graph Clock</span></span>

<span data-ttu-id="c1b1e-104">При построении графа фильтра диспетчер графа фильтров автоматически выбирает эталонный таймер для диаграммы.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-104">When you build a filter graph, the Filter Graph Manager automatically chooses a reference clock for the graph.</span></span> <span data-ttu-id="c1b1e-105">Все фильтры в графе синхронизируются со ссылочным временем.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-105">All filters in the graph are synchronized to the reference clock.</span></span> <span data-ttu-id="c1b1e-106">В частности, фильтры модуля подготовки отчетов используют контрольные часы для определения времени представления каждого образца.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-106">In particular, renderer filters use the reference clock to determine the presentation time of each sample.</span></span>

<span data-ttu-id="c1b1e-107">Как правило, для приложения не требуется переопределять контрольные часы, выбранные диспетчером графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-107">There is usually no reason for an application to override the Filter Graph Manager's choice of reference clock.</span></span> <span data-ttu-id="c1b1e-108">Однако это можно сделать, вызвав метод [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-108">However, you can do so by calling the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method on the Filter Graph Manager.</span></span> <span data-ttu-id="c1b1e-109">Этот метод принимает указатель на интерфейс **иреференцеклокк** часов.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-109">This method takes a pointer to the clock's **IReferenceClock** interface.</span></span> <span data-ttu-id="c1b1e-110">Вызовите метод, пока граф остановлен.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-110">Call the method while the graph is stopped.</span></span>

<span data-ttu-id="c1b1e-111">Если фильтр предоставляет часы, можно получить указатель **иреференцеклокк** , вызвав **QueryInterface** в фильтре.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-111">If a filter provides a clock, you can get the **IReferenceClock** pointer by calling **QueryInterface** on the filter.</span></span> <span data-ttu-id="c1b1e-112">Кроме того, можно реализовать внешний ссылочный часы, не предоставляемые фильтром, при условии, что внешние часы реализуют **иреференцеклокк**.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-112">Alternatively, you can implement an external reference clock that is not provided by a filter, as long as your external clock implements **IReferenceClock**.</span></span> <span data-ttu-id="c1b1e-113">В следующем примере показано, как задать часы.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-113">The following example shows how to specify a clock:</span></span>


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



<span data-ttu-id="c1b1e-114">В этом примере предполагается, что Креатемиприватеклокк является определяемой приложением функцией, которая создает часы и возвращает указатель **иреференцеклокк** .</span><span class="sxs-lookup"><span data-stu-id="c1b1e-114">This example assumes that CreateMyPrivateClock is an application-defined function that creates a clock and returns an **IReferenceClock** pointer.</span></span>

<span data-ttu-id="c1b1e-115">Можно также установить граф фильтра для запуска без часов, вызвав **сетсинксаурце** со значением **null**.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-115">You can also set the filter graph to run with no clock, by calling **SetSyncSource** with the value **NULL**.</span></span> <span data-ttu-id="c1b1e-116">Если часы отсутствуют, граф выполняется как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-116">If there is no clock, the graph runs as quickly as possible.</span></span> <span data-ttu-id="c1b1e-117">Без часов фильтры модуля подготовки отчетов не ожидают времени презентации в примере.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-117">With no clock, renderer filters do not wait for a sample's presentation time.</span></span> <span data-ttu-id="c1b1e-118">Вместо этого они отображают каждый пример сразу после его поступления.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-118">Instead, they render each sample as soon as it arrives.</span></span> <span data-ttu-id="c1b1e-119">Настройка графа для запуска без использования часов полезна, если требуется быстро обрабатывать данные, а не просматривать их в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-119">Setting the graph to run without a clock is useful if you want to process data quickly, rather than previewing it in real time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1b1e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c1b1e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1b1e-121">Основные задачи DirectShow</span><span class="sxs-lookup"><span data-stu-id="c1b1e-121">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="c1b1e-122">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="c1b1e-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="c1b1e-123">Время и часы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="c1b1e-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



