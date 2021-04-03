---
description: Добавление фильтра по CLSID
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Добавление фильтра по CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f880ab1cb3b88fbe6d889acdd192bba341ce2acf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140535"
---
# <a name="add-a-filter-by-clsid"></a>Добавление фильтра по CLSID

Следующая функция создает фильтр с указанным идентификатором класса (CLSID) и добавляет его в граф фильтра:


```C++
// Create a filter by CLSID and add it to the graph.

HRESULT AddFilterByCLSID(
    IGraphBuilder *pGraph,      // Pointer to the Filter Graph Manager.
    REFGUID clsid,              // CLSID of the filter to create.
    IBaseFilter **ppF,          // Receives a pointer to the filter.
    LPCWSTR wszName             // A name for the filter (can be NULL).
    )
{
    *ppF = 0;

    IBaseFilter *pFilter = NULL;
    
    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pFilter, wszName);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppF = pFilter;
    (*ppF)->AddRef();

done:
    SafeRelease(&pFilter);
    return hr;
}
```



> [!Note]  
> В этом примере используется функция [саферелеасе](/windows/desktop/medfound/saferelease) для освобождения указателя [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .

 

Функция вызывает [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания фильтра, а затем вызывает [**Ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить фильтр к графу. В следующем примере кода эта функция используется для добавления фильтра [мультиплексора AVI](avi-mux-filter.md) в граф:


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



Обратите внимание, что некоторые фильтры не могут быть созданы с помощью [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Это часто случается с фильтрами, которые управляют другими программными компонентами. Например, фильтр [AVI компрессор](avi-compressor-filter.md) — это оболочка для видеокодеков, а фильтр [записи видео WDM](wdm-video-capture-filter.md) — оболочка для драйверов записи WDM. Эти фильтры должны быть созданы с помощью [перечислителя системных устройств](system-device-enumerator.md) или модуля [сопоставления фильтров](filter-mapper.md). Дополнительные сведения см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие методы Graph-Building](general-graph-building-techniques.md)
</dt> </dl>

 

 
