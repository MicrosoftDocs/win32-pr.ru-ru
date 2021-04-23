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
# <a name="about-the-capture-graph-builder"></a><span data-ttu-id="40f1d-103">О построителе диаграмм записи</span><span class="sxs-lookup"><span data-stu-id="40f1d-103">About the Capture Graph Builder</span></span>

<span data-ttu-id="40f1d-104">Граф фильтра, который выполняет захват видео или звука, называется *диаграммой записи*.</span><span class="sxs-lookup"><span data-stu-id="40f1d-104">A filter graph that performs video or audio capture is called a *capture graph*.</span></span> <span data-ttu-id="40f1d-105">Графы записи зачастую сложнее, чем графики воспроизведения файлов.</span><span class="sxs-lookup"><span data-stu-id="40f1d-105">Capture graphs are often more complicated than file playback graphs.</span></span> <span data-ttu-id="40f1d-106">Чтобы упростить создание графов записи в приложениях, DirectShow предоставляет вспомогательный объект, называемый построителем диаграмм записи.</span><span class="sxs-lookup"><span data-stu-id="40f1d-106">To make it easier for applications to build capture graphs, DirectShow provides a helper object called the Capture Graph Builder.</span></span> <span data-ttu-id="40f1d-107">Построитель графов записи предоставляет интерфейс [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , который содержит методы для создания графа записи и управления им.</span><span class="sxs-lookup"><span data-stu-id="40f1d-107">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, which contains methods for building and controlling a capture graph.</span></span> <span data-ttu-id="40f1d-108">На следующей схеме показан построитель диаграмм записи и интерфейс **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="40f1d-108">The following diagram illustrates the Capture Graph Builder and the **ICaptureGraphBuilder2** interface.</span></span>

![Использование построителя графа записи](images/cgb01.png)

<span data-ttu-id="40f1d-110">Начните с вызова CoCreateInstance для создания новых экземпляров построителя графа записи и диспетчера графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="40f1d-110">Start by calling CoCreateInstance to create new instances of the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="40f1d-111">Затем инициализируйте построитель диаграмм записи путем вызова [**ICaptureGraphBuilder2:: сетфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) с указателем на интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) диспетчера графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="40f1d-111">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="40f1d-112">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="40f1d-112">The following diagram illustrates this process.</span></span>

![Инициализация построителя графа записи](images/cgb03.png)

<span data-ttu-id="40f1d-114">В следующем коде показана вспомогательная функция для выполнения следующих действий.</span><span class="sxs-lookup"><span data-stu-id="40f1d-114">The following code shows a helper function to perform these steps:</span></span>


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



<span data-ttu-id="40f1d-115">В этом разделе, посвященном записи видео, предполагается, что для создания диаграммы записи используется построитель диаграмм записи.</span><span class="sxs-lookup"><span data-stu-id="40f1d-115">Throughout this section on video capture, it is assumed that you are using the Capture Graph Builder to create the capture graph.</span></span> <span data-ttu-id="40f1d-116">Тем не менее, можно полностью создавать графы записи с помощью методов Играфбуилдер.</span><span class="sxs-lookup"><span data-stu-id="40f1d-116">However, it is possible to build capture graphs entirely by using IGraphBuilder methods.</span></span> <span data-ttu-id="40f1d-117">Однако это очень сложная тема, и методы построителя графа записи являются предпочтительными.</span><span class="sxs-lookup"><span data-stu-id="40f1d-117">This is considered an advanced topic, however, and the Capture Graph Builder methods are preferred.</span></span> <span data-ttu-id="40f1d-118">Дополнительные сведения см. в [статьях, посвященных расширенному сбору](advanced-capture-topics.md)данных.</span><span class="sxs-lookup"><span data-stu-id="40f1d-118">For more information, see [Advanced Capture Topics](advanced-capture-topics.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="40f1d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="40f1d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40f1d-120">Сведения о записи видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="40f1d-120">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



