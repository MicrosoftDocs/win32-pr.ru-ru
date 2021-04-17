---
description: Настройка часов графа
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Настройка часов графа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682173"
---
# <a name="setting-the-graph-clock"></a>Настройка часов графа

При построении графа фильтра диспетчер графа фильтров автоматически выбирает эталонный таймер для диаграммы. Все фильтры в графе синхронизируются со ссылочным временем. В частности, фильтры модуля подготовки отчетов используют контрольные часы для определения времени представления каждого образца.

Как правило, для приложения не требуется переопределять контрольные часы, выбранные диспетчером графа фильтров. Однако это можно сделать, вызвав метод [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) в диспетчере графов фильтров. Этот метод принимает указатель на интерфейс **иреференцеклокк** часов. Вызовите метод, пока граф остановлен.

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные задачи DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> <dt>

[Время и часы в DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



