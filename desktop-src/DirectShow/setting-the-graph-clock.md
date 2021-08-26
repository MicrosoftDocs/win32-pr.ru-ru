---
description: настройка часов Graph
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: настройка часов Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab93fcefe4ba88aa7724bf59b775c493313783b2f4ad3801925e16b9a1818c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904144"
---
# <a name="setting-the-graph-clock"></a>настройка часов Graph

при построении графа фильтра диспетчер Graph Manager автоматически выбирает эталонный таймер для графа. Все фильтры в графе синхронизируются со ссылочным временем. В частности, фильтры модуля подготовки отчетов используют контрольные часы для определения времени представления каждого образца.

как правило, для приложения не требуется переопределять фильтр Graphного таймера. однако это можно сделать, вызвав метод [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) в фильтре Graph Manager. Этот метод принимает указатель на интерфейс **иреференцеклокк** часов. Вызовите метод, пока граф остановлен.

Если фильтр предоставляет часы, можно получить указатель **иреференцеклокк** , вызвав **QueryInterface** в фильтре. Кроме того, можно реализовать внешний ссылочный часы, не предоставляемые фильтром, при условии, что внешние часы реализуют **иреференцеклокк**. В следующем примере показано, как задать часы.


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



В этом примере предполагается, что Креатемиприватеклокк является определяемой приложением функцией, которая создает часы и возвращает указатель **иреференцеклокк** .

Можно также установить граф фильтра для запуска без часов, вызвав **сетсинксаурце** со значением **null**. Если часы отсутствуют, граф выполняется как можно быстрее. Без часов фильтры модуля подготовки отчетов не ожидают времени презентации в примере. Вместо этого они отображают каждый пример сразу после его поступления. Настройка графа для запуска без использования часов полезна, если требуется быстро обрабатывать данные, а не просматривать их в режиме реального времени.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[основные задачи DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> <dt>

[Время и часы в DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



