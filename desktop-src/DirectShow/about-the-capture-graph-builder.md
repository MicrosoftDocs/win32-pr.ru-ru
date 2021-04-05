---
description: О построителе диаграмм записи
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: О построителе диаграмм записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae321665e0eae65a1d464bf87a12ac33e935d7ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990230"
---
# <a name="about-the-capture-graph-builder"></a>О построителе диаграмм записи

Граф фильтра, который выполняет захват видео или звука, называется *диаграммой записи*. Графы записи зачастую сложнее, чем графики воспроизведения файлов. Чтобы упростить создание графов записи в приложениях, DirectShow предоставляет вспомогательный объект, называемый построителем диаграмм записи. Построитель графов записи предоставляет интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , который содержит методы для создания графа записи и управления им. На следующей схеме показан построитель диаграмм записи и интерфейс **ICaptureGraphBuilder2** .

![Использование построителя графа записи](images/cgb01.png)

Начните с вызова CoCreateInstance для создания новых экземпляров построителя графа записи и диспетчера графа фильтров. Затем инициализируйте построитель диаграмм записи путем вызова [**ICaptureGraphBuilder2:: сетфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) с указателем на интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) диспетчера графа фильтров. Этот процесс представлен на схеме ниже.

![Инициализация построителя графа записи](images/cgb03.png)

В следующем коде показана вспомогательная функция для выполнения следующих действий.


```C++
HRESULT InitCaptureGraphBuilder(
  IGraphBuilder **ppGraph,  // Receives the pointer.
  ICaptureGraphBuilder2 **ppBuild  // Receives the pointer.
)
{
    if (!ppGraph || !ppBuild)
    {
        return E_POINTER;
    }
    IGraphBuilder *pGraph = NULL;
    ICaptureGraphBuilder2 *pBuild = NULL;

    // Create the Capture Graph Builder.
    HRESULT hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, (void**)&pBuild );
    if (SUCCEEDED(hr))
    {
        // Create the Filter Graph Manager.
        hr = CoCreateInstance(CLSID_FilterGraph, 0, CLSCTX_INPROC_SERVER,
            IID_IGraphBuilder, (void**)&pGraph);
        if (SUCCEEDED(hr))
        {
            // Initialize the Capture Graph Builder.
            pBuild->SetFiltergraph(pGraph);

            // Return both interface pointers to the caller.
            *ppBuild = pBuild;
            *ppGraph = pGraph; // The caller must release both interfaces.
            return S_OK;
        }
        else
        {
            pBuild->Release();
        }
    }
    return hr; // Failed
}
```



В этом разделе, посвященном записи видео, предполагается, что для создания диаграммы записи используется построитель диаграмм записи. Тем не менее, можно полностью создавать графы записи с помощью методов Играфбуилдер. Однако это очень сложная тема, и методы построителя графа записи являются предпочтительными. Дополнительные сведения см. в [статьях, посвященных расширенному сбору](advanced-capture-topics.md)данных.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения о записи видео в DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



