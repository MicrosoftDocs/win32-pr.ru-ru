---
description: Поиск интерфейса в фильтре или ПИН-коде
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Поиск интерфейса в фильтре или ПИН-коде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d264a35e0c33ba53f6a8df7f69113f3358a9737
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262296"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a><span data-ttu-id="c5f5f-103">Поиск интерфейса в фильтре или ПИН-коде</span><span class="sxs-lookup"><span data-stu-id="c5f5f-103">Find an Interface on a Filter or Pin</span></span>

<span data-ttu-id="c5f5f-104">Для многих операций в DirectShow приложение вызывает методы в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="c5f5f-104">For many operations in DirectShow, the application calls methods on the Filter Graph Manager.</span></span> <span data-ttu-id="c5f5f-105">Однако в некоторых ситуациях приложение должно вызывать метод непосредственно в фильтре или ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="c5f5f-105">In some situations, however, the application must call a method directly on a filter or pin.</span></span> <span data-ttu-id="c5f5f-106">Например, многие фильтры предоставляют специализированные интерфейсы, используемые для настройки фильтра.</span><span class="sxs-lookup"><span data-stu-id="c5f5f-106">For example, many filters expose specialized interfaces that are used to configure the filter.</span></span>

<span data-ttu-id="c5f5f-107">В случае интерфейса фильтра у вас уже может быть указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра.</span><span class="sxs-lookup"><span data-stu-id="c5f5f-107">In the case of a filter interface, you might already have a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="c5f5f-108">В этом случае просто используйте **QueryInterface** для получения другого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c5f5f-108">In that case, simply use **QueryInterface** to get the other interface.</span></span> <span data-ttu-id="c5f5f-109">Но некоторые фильтры могут быть добавлены к диаграмме диспетчером графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="c5f5f-109">But some filters might be added to the graph by the Filter Graph Manager.</span></span> <span data-ttu-id="c5f5f-110">(Дополнительные сведения см. в разделе [Intelligent Connect](intelligent-connect.md).) В этом случае используйте интерфейс [**иенумфилтерс**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) , чтобы прокручивать все фильтры в графе и запрашивать каждый из них в свою очередь.</span><span class="sxs-lookup"><span data-stu-id="c5f5f-110">(For details, see [Intelligent Connect](intelligent-connect.md).) In that case, use the [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) interface to loop through all the filters in the graph, and query each one in turn.</span></span> <span data-ttu-id="c5f5f-111">Это показано в следующей функции:</span><span class="sxs-lookup"><span data-stu-id="c5f5f-111">The following function demonstrates this:</span></span>


```C++
HRESULT FindFilterInterface(
    IGraphBuilder *pGraph, // Pointer to the Filter Graph Manager.
    REFGUID iid,           // IID of the interface to retrieve.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pGraph || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pF = NULL;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every filter for the interface.
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="c5f5f-112">Чтобы найти интерфейс на ПИН-коде, используйте интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) для прохода по контактам на фильтре.</span><span class="sxs-lookup"><span data-stu-id="c5f5f-112">To find an interface on a pin, use the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on a filter.</span></span> <span data-ttu-id="c5f5f-113">Следующая функция показывает, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="c5f5f-113">The following function shows how to do this:</span></span>


```C++
HRESULT FindPinInterface(
    IBaseFilter *pFilter,  // Pointer to the filter to search.
    REFGUID iid,           // IID of the interface.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pFilter || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumPins *pEnum = 0;
    if (FAILED(pFilter->EnumPins(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every pin for the interface.
    IPin *pPin = 0;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        hr = pPin->QueryInterface(iid, ppUnk);
        pPin->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="c5f5f-114">Следующая функция выполняет поиск интерфейса в фильтре или ПИН-коде:</span><span class="sxs-lookup"><span data-stu-id="c5f5f-114">The next function searches for an interface on a filter or a pin:</span></span>


```C++
HRESULT FindInterfaceAnywhere(
    IGraphBuilder *pGraph, 
    REFGUID iid, 
    void **ppUnk)
{
    if (!pGraph || !ppUnk) return E_POINTER;
    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = 0;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Loop through every filter in the graph.
    IBaseFilter *pF = 0;
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        if (FAILED(hr))
        {
            // The filter does not expose the interface, but maybe
            // one of its pins does.
            hr = FindPinInterface(pF, iid, ppUnk);
        }
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="c5f5f-115">Обратите внимание, что все показанные здесь функции останавливаются при первом успешном выполнении **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c5f5f-115">Note that all of the functions shown here stop at the first successful **QueryInterface**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5f5f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="c5f5f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5f5f-117">Перечисление фильтров</span><span class="sxs-lookup"><span data-stu-id="c5f5f-117">Enumerating Filters</span></span>](enumerating-filters.md)
</dt> <dt>

[<span data-ttu-id="c5f5f-118">Перечисление ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="c5f5f-118">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="c5f5f-119">**ICaptureGraphBuilder2:: Финдинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="c5f5f-119">**ICaptureGraphBuilder2::FindInterface**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



