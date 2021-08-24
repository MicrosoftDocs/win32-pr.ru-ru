---
description: Поиск интерфейса в фильтре или ПИН-коде
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Поиск интерфейса в фильтре или ПИН-коде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17314f7e44e4b2c4f412dd0d152e038203268c29d585cd684ddde9eb34992a2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819566"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a>Поиск интерфейса в фильтре или ПИН-коде

для многих операций в DirectShow приложение вызывает методы в диспетчере Graph фильтра. Однако в некоторых ситуациях приложение должно вызывать метод непосредственно в фильтре или ПИН-коде. Например, многие фильтры предоставляют специализированные интерфейсы, используемые для настройки фильтра.

В случае интерфейса фильтра у вас уже может быть указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра. В этом случае просто используйте **QueryInterface** для получения другого интерфейса. но некоторые фильтры могут быть добавлены на диаграмму фильтром Graph Manager. (дополнительные сведения см. в разделе [интеллектуальные Подключение](intelligent-connect.md).) В этом случае используйте интерфейс [**иенумфилтерс**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) , чтобы прокручивать все фильтры в графе и запрашивать каждый из них в свою очередь. Это показано в следующей функции:


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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Перечисление фильтров](enumerating-filters.md)
</dt> <dt>

[Перечисление ПИН-кодов](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: Финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



