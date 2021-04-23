---
description: Удаление всех фильтров в графе
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Удаление всех фильтров в графе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805878"
---
# <a name="remove-all-the-filters-in-the-graph"></a><span data-ttu-id="f54ee-103">Удаление всех фильтров в графе</span><span class="sxs-lookup"><span data-stu-id="f54ee-103">Remove All the Filters in the Graph</span></span>

<span data-ttu-id="f54ee-104">Самый простой способ удалить все фильтры в графе фильтра — это просто освободить диспетчер графов фильтров и создать новый.</span><span class="sxs-lookup"><span data-stu-id="f54ee-104">The easiest way to remove all of the filters in a filter graph is simply to release the Filter Graph Manager and create a new one.</span></span> <span data-ttu-id="f54ee-105">Обязательно выпустите все указатели, которые ваше приложение будет использовать с любыми интерфейсами в диспетчере графов фильтров, а также указатели на объекты в графе, включая фильтры, ПИН-коды, контрольные часы и т. д.</span><span class="sxs-lookup"><span data-stu-id="f54ee-105">Make sure to release every pointer that your application has to any interfaces on the Filter Graph Managers, as well as pointers to objects in the graph, including filters, pins, the reference clock, and so forth.</span></span>

<span data-ttu-id="f54ee-106">Кроме того, можно удалить фильтры по одному с помощью метода [**ифилтерграф:: ремовефилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :</span><span class="sxs-lookup"><span data-stu-id="f54ee-106">Alternatively, you can remove the filters one at a time, using the [**IFilterGraph::RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) method:</span></span>


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



<span data-ttu-id="f54ee-107">В этом примере используется метод [**ифилтерграф:: енумфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) для перечисления фильтров в графе.</span><span class="sxs-lookup"><span data-stu-id="f54ee-107">This example uses the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method to enumerate the filters in the graph.</span></span> <span data-ttu-id="f54ee-108">Удаление фильтра приводит к тому, что объект перечислителя становится несинхронизированным с графом.</span><span class="sxs-lookup"><span data-stu-id="f54ee-108">Removing a filter causes the enumerator object to become out of sync with the graph.</span></span> <span data-ttu-id="f54ee-109">Чтобы сбросить перечислитель, используйте метод [**иенумфилтерс:: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) .</span><span class="sxs-lookup"><span data-stu-id="f54ee-109">Use the [**IEnumFilters::Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) method to reset the enumerator.</span></span> <span data-ttu-id="f54ee-110">В противном случае любой последующий вызов метода [**иенумфилтерс:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f54ee-110">Otherwise, any subsequent call to [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) will fail.</span></span>

 

 



