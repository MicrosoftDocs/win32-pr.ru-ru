---
description: Предварительный просмотр проекта
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Предварительный просмотр проекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd9d299a99a0a7315cec986fbc044d427385647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341732"
---
# <a name="previewing-a-project"></a><span data-ttu-id="0e142-103">Предварительный просмотр проекта</span><span class="sxs-lookup"><span data-stu-id="0e142-103">Previewing a Project</span></span>

<span data-ttu-id="0e142-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="0e142-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0e142-105">Для предварительного просмотра проекта сначала вызовите метод **CoCreateInstance** , чтобы создать экземпляр базового механизма визуализации.</span><span class="sxs-lookup"><span data-stu-id="0e142-105">To preview a project, first call **CoCreateInstance** to create an instance of the Basic Render Engine.</span></span> <span data-ttu-id="0e142-106">Идентификатор класса — CLSID \_ рендеренгине.</span><span class="sxs-lookup"><span data-stu-id="0e142-106">The class identifier is CLSID\_RenderEngine.</span></span> <span data-ttu-id="0e142-107">Затем вызовите метод [**ирендеренгине:: сеттимелинеобжект**](irenderengine-settimelineobject.md) , чтобы указать шкалу времени, которую вы готовите к просмотру.</span><span class="sxs-lookup"><span data-stu-id="0e142-107">Then call the [**IRenderEngine::SetTimelineObject**](irenderengine-settimelineobject.md) method to specify the timeline that you are rendering.</span></span>

<span data-ttu-id="0e142-108">При первом предварительном просмотре временной шкалы выполните следующие вызовы в указанном порядке:</span><span class="sxs-lookup"><span data-stu-id="0e142-108">The first time that you preview the timeline, perform the following calls in the order listed:</span></span>

1.  <span data-ttu-id="0e142-109">Вызовите [**ирендеренгине:: сетрендерранже**](irenderengine-setrenderrange.md) , чтобы указать, какую часть временной шкалы следует просмотреть.</span><span class="sxs-lookup"><span data-stu-id="0e142-109">Call [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md) to specify which portion of the timeline to preview.</span></span> <span data-ttu-id="0e142-110">(необязательно)</span><span class="sxs-lookup"><span data-stu-id="0e142-110">(Optional)</span></span>
2.  <span data-ttu-id="0e142-111">Вызовите [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) , чтобы создать внешний интерфейс графа.</span><span class="sxs-lookup"><span data-stu-id="0e142-111">Call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span>
3.  <span data-ttu-id="0e142-112">Вызовите [**ирендеренгине:: рендераутпутпинс**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="0e142-112">Call [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="0e142-113">Этот метод соединяет каждый выходной закрепление с модулем подготовки видео или модулем подготовки звука, выполняя граф.</span><span class="sxs-lookup"><span data-stu-id="0e142-113">This method connects each output pin to a video renderer or audio renderer, completing the graph.</span></span>

<span data-ttu-id="0e142-114">В следующем примере кода показаны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0e142-114">The following code example shows these steps:</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



<span data-ttu-id="0e142-115">Теперь запустите граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="0e142-115">Now run the filter graph.</span></span> <span data-ttu-id="0e142-116">Сначала вызовите метод [**ирендеренгине:: жетфилтерграф**](irenderengine-getfiltergraph.md) , чтобы получить указатель на интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) диспетчера графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="0e142-116">First, call the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method to retrieve a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="0e142-117">Затем выполните запрос к диспетчеру графа фильтров для интерфейса [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) и вызовите [**Имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="0e142-117">Then query the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface and call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), as shown in the following code:</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



<span data-ttu-id="0e142-118">Используйте интерфейс [**Имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) диспетчера графа фильтров, чтобы дождаться завершения предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="0e142-118">Use the Filter Graph Manager's [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to wait for the preview to complete.</span></span> <span data-ttu-id="0e142-119">Можно также выполнить поиск в графе с помощью интерфейса [**Имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) диспетчера графа фильтров так же, как и графа воспроизведения файлов.</span><span class="sxs-lookup"><span data-stu-id="0e142-119">You can also seek the graph using the Filter Graph Manager's [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, just as you would with a file playback graph.</span></span>

<span data-ttu-id="0e142-120">Чтобы снова выполнить предварительный просмотр проекта, вернитесь на граф к нулевому времени и снова вызовите **команду Run** .</span><span class="sxs-lookup"><span data-stu-id="0e142-120">To preview the project again, seek the graph back to time zero and call **Run** again.</span></span> <span data-ttu-id="0e142-121">При изменении содержимого временной шкалы выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0e142-121">If you change the contents of the timeline, do the following:</span></span>

1.  <span data-ttu-id="0e142-122">Вызовите **сетрендерранже**.</span><span class="sxs-lookup"><span data-stu-id="0e142-122">Call **SetRenderRange**.</span></span> <span data-ttu-id="0e142-123">(необязательно)</span><span class="sxs-lookup"><span data-stu-id="0e142-123">(Optional)</span></span>
2.  <span data-ttu-id="0e142-124">Вызовите **коннектфронтенд**.</span><span class="sxs-lookup"><span data-stu-id="0e142-124">Call **ConnectFrontEnd**.</span></span>
3.  <span data-ttu-id="0e142-125">Если метод **коннектфронтенд** возвращает S \_ warn \_ Аутпутресет, вызовите **рендераутпутпинс**.</span><span class="sxs-lookup"><span data-stu-id="0e142-125">If the **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET, call **RenderOutputPins**.</span></span> <span data-ttu-id="0e142-126">(Если **коннектфронтенд** возвращает S \_ ОК, этот шаг можно пропустить.)</span><span class="sxs-lookup"><span data-stu-id="0e142-126">(If **ConnectFrontEnd** returns S\_OK, you can skip this step.)</span></span>
4.  <span data-ttu-id="0e142-127">Поиск графа обратно в нулевое значение времени.</span><span class="sxs-lookup"><span data-stu-id="0e142-127">Seek the graph back to time zero.</span></span>
5.  <span data-ttu-id="0e142-128">Запустите граф.</span><span class="sxs-lookup"><span data-stu-id="0e142-128">Run the graph.</span></span>

<span data-ttu-id="0e142-129">В следующем примере показаны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0e142-129">The following example shows these steps:</span></span>


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



<span data-ttu-id="0e142-130">Полный пример загрузки и предварительного просмотра файла проекта см. в разделе [Загрузка и предварительный просмотр проекта](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="0e142-130">For a complete example that loads and previews a project file, see [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e142-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0e142-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e142-132">Управление проектами редактирования видео</span><span class="sxs-lookup"><span data-stu-id="0e142-132">Managing Video Editing Projects</span></span>](managing-video-editing-projects.md)
</dt> <dt>

[<span data-ttu-id="0e142-133">Подготовка проекта</span><span class="sxs-lookup"><span data-stu-id="0e142-133">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



