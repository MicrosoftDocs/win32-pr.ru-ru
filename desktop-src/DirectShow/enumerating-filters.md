---
description: Перечисление фильтров
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: Перечисление фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d584ddf74a13b06e99d9a7e0a34ac802c6da881d87cb163411100ea7772e1df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819667"
---
# <a name="enumerating-filters"></a>Перечисление фильтров

диспетчер Graph фильтра поддерживает метод [**ифилтерграф:: енумфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) , который перечисляет все фильтры в графе фильтра. Он возвращает указатель на интерфейс [**иенумфилтерс**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) . Метод [**иенумфилтерс:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) получает указатели интерфейса [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .

В следующем примере показана функция, которая перечисляет фильтры в графе и отображает окно сообщения с именем каждого фильтра. Для получения имени фильтра используется метод [**ибасефилтер:: куерифилтеринфо**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) . Обратите внимание на места, в которых функция вызывает функцию **Release** в интерфейсе для уменьшения числа ссылок.


```C++
HRESULT EnumFilters (IFilterGraph *pGraph) 
{
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        FILTER_INFO FilterInfo;
        hr = pFilter->QueryFilterInfo(&FilterInfo);
        if (FAILED(hr))
        {
            MessageBox(NULL, TEXT("Could not get the filter info"),
                TEXT("Error"), MB_OK | MB_ICONERROR);
            continue;  // Maybe the next one will work.
        }

#ifdef UNICODE
        MessageBox(NULL, FilterInfo.achName, TEXT("Filter Name"), MB_OK);
#else
        char szName[MAX_FILTER_NAME];
        int cch = WideCharToMultiByte(CP_ACP, 0, FilterInfo.achName,
            MAX_FILTER_NAME, szName, MAX_FILTER_NAME, 0, 0);
        if (cch > 0)
            MessageBox(NULL, szName, TEXT("Filter Name"), MB_OK);
#endif

        // The FILTER_INFO structure holds a pointer to the Filter Graph
        // Manager, with a reference count that must be released.
        if (FilterInfo.pGraph != NULL)
        {
            FilterInfo.pGraph->Release();
        }
        pFilter->Release();
    }

    pEnum->Release();
    return S_OK;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Перечисление объектов в фильтре Graph](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



