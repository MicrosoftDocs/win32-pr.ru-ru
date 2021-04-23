---
description: Создание графа фильтра VMR-9
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Создание графа фильтра VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894918"
---
# <a name="building-a-vmr-9-filter-graph"></a><span data-ttu-id="c3cbd-103">Создание графа фильтра VMR-9</span><span class="sxs-lookup"><span data-stu-id="c3cbd-103">Building a VMR-9 Filter Graph</span></span>

<span data-ttu-id="c3cbd-104">Так как фильтр визуализации 9 для видео микшера (VMR-9) не является модулем подготовки видео по умолчанию, приложение, использующее VMR-9, должно явно добавить его в граф и подключить.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-104">Because the Video Mixing Renderer 9 Filter (VMR-9) is not the default video renderer, an application that uses the VMR-9 must explicitly add it to the graph and connect it.</span></span> <span data-ttu-id="c3cbd-105">В этом разделе представлены два разных подхода к созданию графов фильтров с помощью фильтра VMR-9.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-105">This section presents two different approaches to building filter graphs with the VMR-9.</span></span>

<span data-ttu-id="c3cbd-106">Использование построителя графа записи</span><span class="sxs-lookup"><span data-stu-id="c3cbd-106">Using the Capture Graph Builder</span></span>

<span data-ttu-id="c3cbd-107">Построитель графов записи — это вспомогательный объект для создания графов настраиваемых фильтров.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-107">The Capture Graph Builder is a helper object for building custom filter graphs.</span></span> <span data-ttu-id="c3cbd-108">Его можно использовать для создания графов VMR-9 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c3cbd-108">You can use it to build VMR-9 graphs as follows:</span></span>

1.  <span data-ttu-id="c3cbd-109">Создание и инициализация построителя графа записи, как описано в разделе [Построитель диаграмм записи](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="c3cbd-109">Create and initialize the Capture Graph Builder, as described in the topic [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
2.  <span data-ttu-id="c3cbd-110">Вызовите CoCreateInstance для создания VMR-9:</span><span class="sxs-lookup"><span data-stu-id="c3cbd-110">Call CoCreateInstance to create the VMR-9:</span></span>
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  <span data-ttu-id="c3cbd-111">Вызовите [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) в диспетчере графа фильтров, чтобы добавить VMR-9 в граф фильтра:</span><span class="sxs-lookup"><span data-stu-id="c3cbd-111">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) on the Filter Graph Manager to add the VMR-9 to the filter graph:</span></span>
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  <span data-ttu-id="c3cbd-112">Вызовите [**играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) , чтобы добавить фильтр источника для файла видео:</span><span class="sxs-lookup"><span data-stu-id="c3cbd-112">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the video file:</span></span>
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  <span data-ttu-id="c3cbd-113">Вызовите метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , чтобы отобразить видеопоток в VMR:</span><span class="sxs-lookup"><span data-stu-id="c3cbd-113">Call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to render the video stream to the VMR:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  <span data-ttu-id="c3cbd-114">При необходимости снова вызовите RenderStream для отрисовки аудиопотока:</span><span class="sxs-lookup"><span data-stu-id="c3cbd-114">Optionally, call RenderStream again to render the audio stream:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

<span data-ttu-id="c3cbd-115">Вы можете смешивать несколько потоков видео, вызывая Аддсаурцефилтер и RenderStream для каждого исходного файла.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-115">You can mix several video streams by calling AddSourceFilter and RenderStream for each source file.</span></span>

<span data-ttu-id="c3cbd-116">Использование диспетчера графа фильтров</span><span class="sxs-lookup"><span data-stu-id="c3cbd-116">Using the Filter Graph Manager</span></span>

<span data-ttu-id="c3cbd-117">Если вы предпочитаете не использовать построитель диаграмм записи, можно создать граф VMR-9, просто используя методы в диспетчере графов фильтров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-117">If you prefer not to use the Capture Graph Builder, you can build a VMR-9 graph simply using methods on the Filter Graph Manager, as follows:</span></span>

1.  <span data-ttu-id="c3cbd-118">Создайте VMR-9 и добавьте его в граф, как показано в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-118">Create the VMR-9 and add it to the graph, as shown in the previous procedure.</span></span>
2.  <span data-ttu-id="c3cbd-119">Используйте Аддсаурцефилтер, чтобы добавить фильтр источника для файла видео, как показано в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-119">Use AddSourceFilter to add a source filter for the video file, as shown in the previous procedure.</span></span>
3.  <span data-ttu-id="c3cbd-120">Если вы хотите подготовить звук, создайте экземпляр фильтра модуля [обработки DirectSound](directsound-renderer-filter.md) и добавьте его в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-120">If you want to render the audio, create an instance of the [DirectSound Renderer](directsound-renderer-filter.md) filter and add it to the filter graph.</span></span>
4.  <span data-ttu-id="c3cbd-121">Используйте метод Ибасефилтер:: Енумпинс, чтобы найти выходной ПИН-код в фильтре источника.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-121">Use the IBaseFilter::EnumPins method to find an output pin on the source filter.</span></span> <span data-ttu-id="c3cbd-122">Дополнительные сведения см. в разделе [перечисление ПИН](enumerating-pins.md) -кодов.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-122">See [Enumerating Pins](enumerating-pins.md) for details.</span></span>
5.  <span data-ttu-id="c3cbd-123">Запросите диспетчер графов фильтров для интерфейса IFilterGraph2.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-123">Query the Filter Graph Manager for the IFilterGraph2 interface.</span></span>
6.  <span data-ttu-id="c3cbd-124">Вызовите [**IFilterGraph2:: рендерекс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) с \_ \_ флагом AM рендерекс рендертоексистингрендерерс.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-124">Call [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) with the AM\_RENDEREX\_RENDERTOEXISTINGRENDERERS flag.</span></span> <span data-ttu-id="c3cbd-125">Этот вызов визуализирует выходной ПИН-код, используя только фильтры модуля подготовки отчетов, уже имеющиеся в графе — в данном случае — VMR-9 и модуль подготовки DirectSound.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-125">This call renders the output pin, using only the renderer filters already in the graph — in this case, the VMR-9 and the DirectSound Renderer.</span></span> <span data-ttu-id="c3cbd-126">Таким образом, логика интеллектуального соединения не добавляет к диаграмме модуль подготовки видео по умолчанию, что приведет к неподключенному объекту VMR-9.</span><span class="sxs-lookup"><span data-stu-id="c3cbd-126">This prevents the Intelligent Connect logic from adding the default video renderer to the graph, which would leave the VMR-9 unconnected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3cbd-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c3cbd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3cbd-128">Построение диаграмм с помощью построителя графа записи</span><span class="sxs-lookup"><span data-stu-id="c3cbd-128">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



