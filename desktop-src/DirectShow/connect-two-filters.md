---
description: в этом разделе показаны некоторые вспомогательные функции для подключения фильтров DirectShow.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Подключение Два фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83e8608c088fde6d06c0a44621f1c066f177ecf76cbc8ba3f55d31218b49ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954213"
---
# <a name="connect-two-filters"></a>Подключение Два фильтра

в этом разделе показаны некоторые вспомогательные функции для подключения фильтров DirectShow.

Чтобы подключить два фильтра, необходимо найти неподключенный выходной контакт на вышестоящем фильтре и несоединенный входной ПИН-код в подчиненном фильтре.

если у вас уже есть указатели на оба контакта, вызовите метод [**играфбуилдер:: Подключение**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , чтобы соединить их. если пин-коды не могут напрямую подключиться друг к другу, метод **играфбуилдер:: Подключение** может вставлять дополнительные фильтры для завершения подключения. дополнительные сведения см. в статье [интеллектуальные Подключение](intelligent-connect.md).

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
2.  вызывает [**играфбуилдер:: Подключение**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) для соединения двух пин-кодов.

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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Общие методы Graph-Building](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



