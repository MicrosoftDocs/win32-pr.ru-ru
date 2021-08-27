---
description: о построителе Graph записи
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: о построителе Graph записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ef82a160ada6e53fe6d2db830efa85118eb699074630905cd41f0b5412ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664526"
---
# <a name="about-the-capture-graph-builder"></a>о построителе Graph записи

Граф фильтра, который выполняет захват видео или звука, называется *диаграммой записи*. Графы записи зачастую сложнее, чем графики воспроизведения файлов. чтобы упростить создание графов записи в приложениях, DirectShow предоставляет вспомогательный объект, называемый построителем Graph отслеживания. построитель Graph для записи предоставляет интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , который содержит методы для создания графа записи и управления им. на следующей схеме показан построитель Graph Capture и интерфейс **ICaptureGraphBuilder2** .

![Использование построителя графа записи](images/cgb01.png)

начните с вызова cocreateinstance для создания новых экземпляров построителя Graph и Filter Graph Manager. затем инициализируйте построитель Graph записи, вызвав [**ICaptureGraphBuilder2:: сетфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) с указателем на интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) диспетчера Graph Manager. Этот процесс представлен на схеме ниже.

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



в этом разделе, посвященном записи видео, предполагается, что для создания диаграммы записи используется построитель Graph для записи. Тем не менее, можно полностью создавать графы записи с помощью методов Играфбуилдер. тем не менее, это будет дополнительная тема, а методы построителя Graph для отслеживания являются предпочтительными. Дополнительные сведения см. в [статьях, посвященных расширенному сбору](advanced-capture-topics.md)данных.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения о захвате видео в DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



