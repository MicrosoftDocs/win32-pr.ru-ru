---
description: В этом разделе показаны некоторые вспомогательные функции для подключения фильтров DirectShow.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Соединение двух фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140231"
---
# <a name="connect-two-filters"></a>Соединение двух фильтров

В этом разделе показаны некоторые вспомогательные функции для подключения фильтров DirectShow.

Чтобы подключить два фильтра, необходимо найти неподключенный выходной контакт на вышестоящем фильтре и несоединенный входной ПИН-код в подчиненном фильтре.

Если у вас уже есть указатели на оба контакта, вызовите метод [**играфбуилдер:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , чтобы соединить их. Если ПИН-коды не могут напрямую подключиться друг к другу, метод **играфбуилдер:: Connect** может вставить дополнительные фильтры для завершения подключения. Дополнительные сведения см. в статье [Intelligent Connect](intelligent-connect.md).

Если у вас есть указатель на фильтры, но не на ПИН-коды, то для поиска ПИН-кодов необходимо использовать метод [**ибасефилтер:: енумпинс**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) . (См. раздел [перечисление ПИН](enumerating-pins.md)-кодов.) Этот метод демонстрируется в вспомогательных функциях этого раздела.

### <a name="output-pin-to-filter"></a>Вывод закрепления для фильтрации

Следующая функция принимает два параметра: указатель на закрепление вывода и указатель на фильтр. Функция соединяет закрепление вывода с первым доступным входным закреплением в фильтре.


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



Эта функция выполняет следующие действия:

1.  Вызывает `FindUnconnectedPin` функцию, чтобы получить несоединенный входной ПИН-код. Эта функция показана в разделе [Поиск неподключенного ПИН-кода в фильтре](find-an-unconnected-pin-on-a-filter.md).
2.  Вызывает [**играфбуилдер:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) для соединения двух ПИН-кодов.

### <a name="filter-to-input-pin"></a>Фильтр входного ПИН-кода

Следующая функция принимает указатель на фильтр и указатель на входной ПИН-код. Он подключает входной ПИН-код к первому доступному выходному контакту в фильтре.


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a>Фильтр для фильтрации

Третья функция принимает указатель на вышестоящий фильтр и указатель на нисходящий фильтр и пытается подключить оба фильтра.


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие методы Graph-Building](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



