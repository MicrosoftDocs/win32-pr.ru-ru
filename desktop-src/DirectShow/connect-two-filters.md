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
# <a name="connect-two-filters"></a><span data-ttu-id="aaae6-103">Соединение двух фильтров</span><span class="sxs-lookup"><span data-stu-id="aaae6-103">Connect Two Filters</span></span>

<span data-ttu-id="aaae6-104">В этом разделе показаны некоторые вспомогательные функции для подключения фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="aaae6-104">This topic shows some helper functions for connecting DirectShow filters.</span></span>

<span data-ttu-id="aaae6-105">Чтобы подключить два фильтра, необходимо найти неподключенный выходной контакт на вышестоящем фильтре и несоединенный входной ПИН-код в подчиненном фильтре.</span><span class="sxs-lookup"><span data-stu-id="aaae6-105">To connect two filters, you must find an unconnected output pin on the upstream filter, and an unconnected input pin on the downstream filter.</span></span>

<span data-ttu-id="aaae6-106">Если у вас уже есть указатели на оба контакта, вызовите метод [**играфбуилдер:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , чтобы соединить их.</span><span class="sxs-lookup"><span data-stu-id="aaae6-106">If you already have pointers to both pins, call the [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) method to connect them.</span></span> <span data-ttu-id="aaae6-107">Если ПИН-коды не могут напрямую подключиться друг к другу, метод **играфбуилдер:: Connect** может вставить дополнительные фильтры для завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="aaae6-107">If the pins cannot connect directly to each other, the **IGraphBuilder::Connect** method might insert additional filters, to complete the connection.</span></span> <span data-ttu-id="aaae6-108">Дополнительные сведения см. в статье [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="aaae6-108">For more information, see [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="aaae6-109">Если у вас есть указатель на фильтры, но не на ПИН-коды, то для поиска ПИН-кодов необходимо использовать метод [**ибасефилтер:: енумпинс**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) .</span><span class="sxs-lookup"><span data-stu-id="aaae6-109">If you have a pointer to the filters but not the pins, you must use the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the pins.</span></span> <span data-ttu-id="aaae6-110">(См. раздел [перечисление ПИН](enumerating-pins.md)-кодов.) Этот метод демонстрируется в вспомогательных функциях этого раздела.</span><span class="sxs-lookup"><span data-stu-id="aaae6-110">(See [Enumerating Pins](enumerating-pins.md).) The helper functions in this topic demonstrate this technique.</span></span>

### <a name="output-pin-to-filter"></a><span data-ttu-id="aaae6-111">Вывод закрепления для фильтрации</span><span class="sxs-lookup"><span data-stu-id="aaae6-111">Output Pin to Filter</span></span>

<span data-ttu-id="aaae6-112">Следующая функция принимает два параметра: указатель на закрепление вывода и указатель на фильтр.</span><span class="sxs-lookup"><span data-stu-id="aaae6-112">The following function takes two parameters: A pointer to an output pin, and a pointer to a filter.</span></span> <span data-ttu-id="aaae6-113">Функция соединяет закрепление вывода с первым доступным входным закреплением в фильтре.</span><span class="sxs-lookup"><span data-stu-id="aaae6-113">The function connects the output pin to the first available input pin on the filter.</span></span>


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



<span data-ttu-id="aaae6-114">Эта функция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="aaae6-114">This function does the following:</span></span>

1.  <span data-ttu-id="aaae6-115">Вызывает `FindUnconnectedPin` функцию, чтобы получить несоединенный входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="aaae6-115">Calls the `FindUnconnectedPin` function to get an unconnected input pin.</span></span> <span data-ttu-id="aaae6-116">Эта функция показана в разделе [Поиск неподключенного ПИН-кода в фильтре](find-an-unconnected-pin-on-a-filter.md).</span><span class="sxs-lookup"><span data-stu-id="aaae6-116">This function is shown in the topic [Find an Unconnected Pin on a Filter](find-an-unconnected-pin-on-a-filter.md).</span></span>
2.  <span data-ttu-id="aaae6-117">Вызывает [**играфбуилдер:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) для соединения двух ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="aaae6-117">Calls [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) to connect the two pins.</span></span>

### <a name="filter-to-input-pin"></a><span data-ttu-id="aaae6-118">Фильтр входного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="aaae6-118">Filter to Input Pin</span></span>

<span data-ttu-id="aaae6-119">Следующая функция принимает указатель на фильтр и указатель на входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="aaae6-119">The next function takes a pointer to a filter and a pointer to an input pin.</span></span> <span data-ttu-id="aaae6-120">Он подключает входной ПИН-код к первому доступному выходному контакту в фильтре.</span><span class="sxs-lookup"><span data-stu-id="aaae6-120">It connects the input pin to the first available output pin on the filter.</span></span>


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



### <a name="filter-to-filter"></a><span data-ttu-id="aaae6-121">Фильтр для фильтрации</span><span class="sxs-lookup"><span data-stu-id="aaae6-121">Filter to Filter</span></span>

<span data-ttu-id="aaae6-122">Третья функция принимает указатель на вышестоящий фильтр и указатель на нисходящий фильтр и пытается подключить оба фильтра.</span><span class="sxs-lookup"><span data-stu-id="aaae6-122">The third function takes a pointer to an upstream filter and a pointer to a downstream filter, and tries to connect both filters.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="aaae6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="aaae6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaae6-124">Общие методы Graph-Building</span><span class="sxs-lookup"><span data-stu-id="aaae6-124">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="aaae6-125">**ICaptureGraphBuilder2:: RenderStream**</span><span class="sxs-lookup"><span data-stu-id="aaae6-125">**ICaptureGraphBuilder2::RenderStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



