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
# <a name="find-an-interface-on-a-filter-or-pin"></a>Поиск интерфейса в фильтре или ПИН-коде

Для многих операций в DirectShow приложение вызывает методы в диспетчере графов фильтров. Однако в некоторых ситуациях приложение должно вызывать метод непосредственно в фильтре или ПИН-коде. Например, многие фильтры предоставляют специализированные интерфейсы, используемые для настройки фильтра.

В случае интерфейса фильтра у вас уже может быть указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра. В этом случае просто используйте **QueryInterface** для получения другого интерфейса. Но некоторые фильтры могут быть добавлены к диаграмме диспетчером графов фильтров. (Дополнительные сведения см. в разделе [Intelligent Connect](intelligent-connect.md).) В этом случае используйте интерфейс [**иенумфилтерс**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) , чтобы прокручивать все фильтры в графе и запрашивать каждый из них в свою очередь. Это показано в следующей функции:


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



Чтобы найти интерфейс на ПИН-коде, используйте интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) для прохода по контактам на фильтре. Следующая функция показывает, как это сделать:


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



Следующая функция выполняет поиск интерфейса в фильтре или ПИН-коде:


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



Обратите внимание, что все показанные здесь функции останавливаются при первом успешном выполнении **QueryInterface**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Перечисление фильтров](enumerating-filters.md)
</dt> <dt>

[Перечисление ПИН-кодов](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: Финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



