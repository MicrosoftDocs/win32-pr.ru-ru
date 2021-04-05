---
description: Поиск однорангового узла фильтров
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Поиск однорангового узла фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072134"
---
# <a name="find-a-filters-peer"></a><span data-ttu-id="9bdab-103">Поиск однорангового узла фильтров</span><span class="sxs-lookup"><span data-stu-id="9bdab-103">Find a Filters Peer</span></span>

<span data-ttu-id="9bdab-104">Используя фильтр, можно просмотреть граф, находя фильтры, к которым он подключен.</span><span class="sxs-lookup"><span data-stu-id="9bdab-104">Given a filter, you can traverse the graph by finding the filters to which it is connected.</span></span> <span data-ttu-id="9bdab-105">Начните с перечисления ПИН-кодов фильтра.</span><span class="sxs-lookup"><span data-stu-id="9bdab-105">Start by enumerating the filter's pins.</span></span> <span data-ttu-id="9bdab-106">Для каждого ПИН-кода проверьте, подключен ли ПИН-код к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="9bdab-106">For each pin, check whether that pin is connected to another pin.</span></span> <span data-ttu-id="9bdab-107">Если это так, запросите другой ПИН-код для фильтра владельца.</span><span class="sxs-lookup"><span data-stu-id="9bdab-107">If so, query the other pin for it's owning filter.</span></span> <span data-ttu-id="9bdab-108">Вы можете проанализировать граф в вышестоящем направлении, перечисляя входные сигналы фильтра или в направлении вверх, перечисляя контакты вывода.</span><span class="sxs-lookup"><span data-stu-id="9bdab-108">You can walk the graph in the upstream direction by enumerating the filter's input pins, or in the downstream direction by enumerating the output pins.</span></span>

<span data-ttu-id="9bdab-109">Следующая функция выполняет поиск подключенного фильтра в режиме «в потоке» или «подчиненный».</span><span class="sxs-lookup"><span data-stu-id="9bdab-109">The following function searches upstream or downstream for a connected filter.</span></span> <span data-ttu-id="9bdab-110">Он возвращает первый найденный фильтр сопоставления:</span><span class="sxs-lookup"><span data-stu-id="9bdab-110">It returns the first matching filter that it finds:</span></span>


```C++
// Get the first upstream or downstream filter
HRESULT GetNextFilter(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    IBaseFilter **ppNext) // Receives a pointer to the next filter.
{
    if (!pFilter || !ppNext) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                pPin->Release();
                pEnum->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    return E_UNEXPECTED;
                }
                // This is the filter we're looking for.
                *ppNext = PinInfo.pFilter; // Client must release.
                return S_OK;
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    // Did not find a matching filter.
    return E_FAIL;
}
```



<span data-ttu-id="9bdab-111">Функция вызывает [**ибасефилтер:: енумпинс**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) для перечисления ПИН-кодов первого фильтра.</span><span class="sxs-lookup"><span data-stu-id="9bdab-111">The function calls [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) to enumerate the first filter's pins.</span></span> <span data-ttu-id="9bdab-112">Для каждого ПИН-кода вызывается метод [**Ипин:: куеридиректион**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) , чтобы проверить, соответствует ли ПИН-код указанному направлению (входные или выходные данные).</span><span class="sxs-lookup"><span data-stu-id="9bdab-112">For each pin, it calls [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) to check whether the pin matches the specified direction (input or output).</span></span> <span data-ttu-id="9bdab-113">Если это так, функция определяет, подключен ли этот ПИН-код к другому ПИН-коду, вызвав метод [**Ипин:: коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="9bdab-113">If so, the function determines whether that pin is connected to another pin, by calling the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span> <span data-ttu-id="9bdab-114">Наконец, он вызывает [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) на подключенном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="9bdab-114">Finally, it calls [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) on the connected pin.</span></span> <span data-ttu-id="9bdab-115">Этот метод возвращает структуру, которая содержит, помимо прочего, указатель на фильтр владельца этого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="9bdab-115">This method returns a structure that contains, among other things, a pointer to that pin's owning filter.</span></span> <span data-ttu-id="9bdab-116">Этот указатель возвращается вызывающему объекту в параметре *ппнекст* .</span><span class="sxs-lookup"><span data-stu-id="9bdab-116">This pointer is returned to the caller in the *ppNext* parameter.</span></span> <span data-ttu-id="9bdab-117">Вызывающий объект должен освободить указатель.</span><span class="sxs-lookup"><span data-stu-id="9bdab-117">The caller must release the pointer.</span></span>

<span data-ttu-id="9bdab-118">В следующем коде показано, как вызвать эту функцию:</span><span class="sxs-lookup"><span data-stu-id="9bdab-118">The following code shows how to call this function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



<span data-ttu-id="9bdab-119">Фильтр может быть подключен к двум или более фильтрам в любом направлении.</span><span class="sxs-lookup"><span data-stu-id="9bdab-119">A filter might be connected to two or more filters in either direction.</span></span> <span data-ttu-id="9bdab-120">Например, это может быть фильтр разделителя с несколькими фильтрами, нисходящими от него.</span><span class="sxs-lookup"><span data-stu-id="9bdab-120">For example, it might be a splitter filter, with several filters downstream from it.</span></span> <span data-ttu-id="9bdab-121">Или это может быть фильтр мультиплексора с несколькими фильтрами, переходящих из него.</span><span class="sxs-lookup"><span data-stu-id="9bdab-121">Or it might be a mux filter, with several filters upstream from it.</span></span> <span data-ttu-id="9bdab-122">Поэтому может потребоваться объединить их в список.</span><span class="sxs-lookup"><span data-stu-id="9bdab-122">Therefore, you might want to collect all of them into a list.</span></span>

<span data-ttu-id="9bdab-123">В следующем коде показан один из возможных способов реализации такой функции.</span><span class="sxs-lookup"><span data-stu-id="9bdab-123">The following code shows one possible way to implement such a function.</span></span> <span data-ttu-id="9bdab-124">В нем используется класс [**Кженериклист**](cgenericlist.md) DirectShow. Вы можете написать эквивалентную функцию, используя другую структуру данных.</span><span class="sxs-lookup"><span data-stu-id="9bdab-124">It uses the DirectShow [**CGenericList**](cgenericlist.md) class; you could write an equivalent function using some other data structure.</span></span>


```C++
#include <streams.h>  // Link to the DirectShow base class library
// Define a typedef for a list of filters.
typedef CGenericList<IBaseFilter> CFilterList;

// Forward declaration. Adds a filter to the list unless it's a duplicate.
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew);

// Find all the immediate upstream or downstream peers of a filter.
HRESULT GetPeerFilters(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    CFilterList &FilterList)  // Collect the results in this list.
{
    if (!pFilter) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    pPin->Release();
                    pEnum->Release();
                    return E_UNEXPECTED;
                }
                // Insert the filter into the list.
                AddFilterUnique(FilterList, PinInfo.pFilter);
                PinInfo.pFilter->Release();
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    return S_OK;
}
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew)
{
    if (pNew == NULL) return;

    POSITION pos = FilterList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pF = FilterList.GetNext(pos);
        if (IsEqualObject(pF, pNew))
        {
            return;
        }
    }
    pNew->AddRef();  // The caller must release everything in the list.
    FilterList.AddTail(pNew);
}
```



<span data-ttu-id="9bdab-125">Чтобы усложнить важность, фильтр может иметь несколько закрепленных соединений с одним фильтром.</span><span class="sxs-lookup"><span data-stu-id="9bdab-125">To complicate matters somewhat, a filter can have multiple pin connections to the same filter.</span></span> <span data-ttu-id="9bdab-126">Чтобы избежать помещения дубликатов в список, запросите каждый **ибасефилтер** указатель для **IUnknown** и сравните указатели **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="9bdab-126">To avoid putting duplicates into the list, query each **IBaseFilter** pointer for **IUnknown** and compare the **IUnknown** pointers.</span></span> <span data-ttu-id="9bdab-127">По правилам модели COM два указателя интерфейса ссылаются на один и тот же объект, только если они возвращают идентичные указатели **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="9bdab-127">By the rules of COM, two interface pointers refer to the same object if and only if they return identical **IUnknown** pointers.</span></span> <span data-ttu-id="9bdab-128">В предыдущем примере функция Аддфилтеруникуе обрабатывает эти сведения.</span><span class="sxs-lookup"><span data-stu-id="9bdab-128">In the previous example, the AddFilterUnique function handles this detail.</span></span>

<span data-ttu-id="9bdab-129">В следующем примере показано, как использовать функцию Жетпирфилтерс:</span><span class="sxs-lookup"><span data-stu-id="9bdab-129">The following example shows how to use the GetPeerFilters function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
CFilterList FList(NAME("MyList"));  // List to hold the downstream peers.
hr = GetPeerFilters(pF, PINDIR_OUTPUT, FList);
if (SUCCEEDED(hr))
{
    POSITION pos = FList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pDownstream = FList.GetNext(pos);
        pDownstream->Release();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="9bdab-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9bdab-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bdab-131">Общие методы Graph-Building</span><span class="sxs-lookup"><span data-stu-id="9bdab-131">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 



