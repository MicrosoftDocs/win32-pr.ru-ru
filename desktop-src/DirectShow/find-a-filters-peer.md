---
description: Поиск однорангового узла фильтров
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Поиск однорангового узла фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2f20a7145d2365e7ee1ec261ea861ddc5fa1eb01d0c3b2503f6f53fa25815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401768"
---
# <a name="find-a-filters-peer"></a>Поиск однорангового узла фильтров

Используя фильтр, можно просмотреть граф, находя фильтры, к которым он подключен. Начните с перечисления ПИН-кодов фильтра. Для каждого ПИН-кода проверьте, подключен ли ПИН-код к другому ПИН-коду. Если это так, запросите другой ПИН-код для фильтра владельца. Вы можете проанализировать граф в вышестоящем направлении, перечисляя входные сигналы фильтра или в направлении вверх, перечисляя контакты вывода.

Следующая функция выполняет поиск подключенного фильтра в режиме «в потоке» или «подчиненный». Он возвращает первый найденный фильтр сопоставления:


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



Функция вызывает [**ибасефилтер:: енумпинс**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) для перечисления ПИН-кодов первого фильтра. Для каждого ПИН-кода вызывается метод [**Ипин:: куеридиректион**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) , чтобы проверить, соответствует ли ПИН-код указанному направлению (входные или выходные данные). Если это так, функция определяет, подключен ли этот ПИН-код к другому ПИН-коду, вызвав метод [**Ипин:: коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) . Наконец, он вызывает [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) на подключенном ПИН-коде. Этот метод возвращает структуру, которая содержит, помимо прочего, указатель на фильтр владельца этого ПИН-кода. Этот указатель возвращается вызывающему объекту в параметре *ппнекст* . Вызывающий объект должен освободить указатель.

В следующем коде показано, как вызвать эту функцию:


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



Фильтр может быть подключен к двум или более фильтрам в любом направлении. Например, это может быть фильтр разделителя с несколькими фильтрами, нисходящими от него. Или это может быть фильтр мультиплексора с несколькими фильтрами, переходящих из него. Поэтому может потребоваться объединить их в список.

В следующем коде показан один из возможных способов реализации такой функции. в нем используется класс DirectShow [**кженериклист**](cgenericlist.md) . Вы можете написать эквивалентную функцию, используя другую структуру данных.


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



Чтобы усложнить важность, фильтр может иметь несколько закрепленных соединений с одним фильтром. Чтобы избежать помещения дубликатов в список, запросите каждый **ибасефилтер** указатель для **IUnknown** и сравните указатели **IUnknown** . По правилам модели COM два указателя интерфейса ссылаются на один и тот же объект, только если они возвращают идентичные указатели **IUnknown** . В предыдущем примере функция Аддфилтеруникуе обрабатывает эти сведения.

В следующем примере показано, как использовать функцию Жетпирфилтерс:


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Общие методы Graph-Building](general-graph-building-techniques.md)
</dt> </dl>

 

 



