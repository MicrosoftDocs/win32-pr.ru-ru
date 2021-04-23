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
# <a name="add-a-filter-by-clsid"></a><span data-ttu-id="af32b-103">Добавление фильтра по CLSID</span><span class="sxs-lookup"><span data-stu-id="af32b-103">Add a Filter by CLSID</span></span>

<span data-ttu-id="af32b-104">Следующая функция создает фильтр с указанным идентификатором класса (CLSID) и добавляет его в граф фильтра:</span><span class="sxs-lookup"><span data-stu-id="af32b-104">The following function creates a filter with a specified class identifier (CLSID) and adds it to the filter graph:</span></span>


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
> <span data-ttu-id="af32b-105">В этом примере используется функция [саферелеасе](/windows/desktop/medfound/saferelease) для освобождения указателя [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="af32b-105">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>

 

<span data-ttu-id="af32b-106">Функция вызывает [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания фильтра, а затем вызывает [**Ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить фильтр к графу.</span><span class="sxs-lookup"><span data-stu-id="af32b-106">The function calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the filter, and then calls [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span> <span data-ttu-id="af32b-107">В следующем примере кода эта функция используется для добавления фильтра [мультиплексора AVI](avi-mux-filter.md) в граф:</span><span class="sxs-lookup"><span data-stu-id="af32b-107">The following code example uses this function to add the [AVI Mux](avi-mux-filter.md) filter to the graph:</span></span>


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



<span data-ttu-id="af32b-108">Обратите внимание, что некоторые фильтры не могут быть созданы с помощью [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="af32b-108">Note that some filters cannot be created with [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="af32b-109">Это часто случается с фильтрами, которые управляют другими программными компонентами.</span><span class="sxs-lookup"><span data-stu-id="af32b-109">This is often the case with filters that manage other software components.</span></span> <span data-ttu-id="af32b-110">Например, фильтр [AVI компрессор](avi-compressor-filter.md) — это оболочка для видеокодеков, а фильтр [записи видео WDM](wdm-video-capture-filter.md) — оболочка для драйверов записи WDM.</span><span class="sxs-lookup"><span data-stu-id="af32b-110">For example, the [AVI Compressor](avi-compressor-filter.md) filter is a wrapper for video codecs, and the [WDM Video Capture](wdm-video-capture-filter.md) filter is a wrapper for WDM capture drivers.</span></span> <span data-ttu-id="af32b-111">Эти фильтры должны быть созданы с помощью [перечислителя системных устройств](system-device-enumerator.md) или модуля [сопоставления фильтров](filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="af32b-111">These filters must be created using either the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="af32b-112">Дополнительные сведения см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="af32b-112">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af32b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="af32b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af32b-114">Общие методы Graph-Building</span><span class="sxs-lookup"><span data-stu-id="af32b-114">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
