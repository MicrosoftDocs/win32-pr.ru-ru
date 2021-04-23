---
description: Предварительный просмотр проекта
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Предварительный просмотр проекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990206"
---
# <a name="previewing-the-project"></a><span data-ttu-id="103e1-103">Предварительный просмотр проекта</span><span class="sxs-lookup"><span data-stu-id="103e1-103">Previewing the Project</span></span>

<span data-ttu-id="103e1-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="103e1-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="103e1-105">Для предварительного просмотра проекта необходим компонент, называемый *модулем подготовки* отчетов, который создает граф фильтра DirectShow из временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="103e1-105">To preview the project, you need a component called a *render engine*, which builds a DirectShow filter graph from a timeline.</span></span> <span data-ttu-id="103e1-106">Граф фильтра фактически визуализирует проект.</span><span class="sxs-lookup"><span data-stu-id="103e1-106">The filter graph is what actually renders the project.</span></span> <span data-ttu-id="103e1-107">Модуль визуализации можно использовать для предварительного просмотра проекта или для записи окончательного выходного файла.</span><span class="sxs-lookup"><span data-stu-id="103e1-107">You can use the render engine to preview a project or to write the final output file.</span></span>

<span data-ttu-id="103e1-108">Эта статья не содержит подробностей о подсистеме визуализации.</span><span class="sxs-lookup"><span data-stu-id="103e1-108">This article does not go into detail about the render engine.</span></span> <span data-ttu-id="103e1-109">Для предварительного просмотра требуется только несколько вызовов метода.</span><span class="sxs-lookup"><span data-stu-id="103e1-109">For preview, you only need a few method calls.</span></span> <span data-ttu-id="103e1-110">Более подробное обсуждение, в том числе запись выходных файлов, можно найти в разделе [Подготовка проекта](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="103e1-110">You can find a more thorough discussion, including how to write output files, in [Rendering a Project](rendering-a-project.md).</span></span> <span data-ttu-id="103e1-111">В следующем примере кода показано, как создать диаграмму предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="103e1-111">The following code example shows how to construct a preview graph.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



<span data-ttu-id="103e1-112">Создайте подсистему отрисовки с помощью функции **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="103e1-112">Create the render engine using the **CoCreateInstance** function.</span></span> <span data-ttu-id="103e1-113">Затем вызывайте следующие методы в интерфейсе [**ирендеренгине**](irenderengine.md) механизма визуализации:</span><span class="sxs-lookup"><span data-stu-id="103e1-113">Then call the following methods on the render engine's [**IRenderEngine**](irenderengine.md) interface:</span></span>

-   <span data-ttu-id="103e1-114">[**Сеттимелинеобжект**](irenderengine-settimelineobject.md).</span><span class="sxs-lookup"><span data-stu-id="103e1-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span></span> <span data-ttu-id="103e1-115">Указывает используемую временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="103e1-115">Specifies the timeline to use.</span></span>
-   <span data-ttu-id="103e1-116">[**Коннектфронтенд**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="103e1-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="103e1-117">Создает диаграмму частичного фильтра с одним выходным закреплением для каждой группы на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="103e1-117">Builds a partial filter graph, with one output pin for each group in the timeline.</span></span>
-   <span data-ttu-id="103e1-118">[**Рендераутпутпинс**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="103e1-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="103e1-119">Завершает диаграмму предварительного просмотра, подключив каждый выходный контакт к обработчику видео или аудио.</span><span class="sxs-lookup"><span data-stu-id="103e1-119">Completes the preview graph by connecting each output pin to a video or audio renderer.</span></span>

<span data-ttu-id="103e1-120">После построения графика можно просмотреть проект, запустив граф, как и любой граф фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="103e1-120">Once the graph is built, you can preview the project by running the graph, as you would with any DirectShow filter graph.</span></span> <span data-ttu-id="103e1-121">Сначала получите указатель на граф фильтра, вызвав метод [**ирендеренгине:: жетфилтерграф**](irenderengine-getfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="103e1-121">First, obtain a pointer to the filter graph by calling the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method.</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



<span data-ttu-id="103e1-122">Запросите граф фильтра для интерфейсов [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) и [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="103e1-122">Query the filter graph for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interfaces.</span></span> <span data-ttu-id="103e1-123">Используйте эти два интерфейса для запуска графа и ожидания завершения воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="103e1-123">Use these two interfaces to run the graph and wait for playback to complete.</span></span> <span data-ttu-id="103e1-124">Описание использования этих интерфейсов см. в разделе [Воспроизведение файла](how-to-play-a-file.md) и [реагирование на события](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="103e1-124">For an explanation of how to use these interfaces, see [How To Play a File](how-to-play-a-file.md) and [Responding to Events](responding-to-events.md).</span></span> <span data-ttu-id="103e1-125">В следующем коде показан один из способов использования этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="103e1-125">The following code shows one way to use these interfaces.</span></span>


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



<span data-ttu-id="103e1-126">Код в этом примере блокирует выполнение программы до завершения воспроизведения из-за бесконечного параметра в вызове метода [**имедиаевент:: ваитфоркомплетион**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) .</span><span class="sxs-lookup"><span data-stu-id="103e1-126">The code in this example blocks program execution until playback completes, because of the INFINITE parameter in the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method call.</span></span> <span data-ttu-id="103e1-127">Однако если во время воспроизведения возникли проблемы, это может привести к тому, что программа перестанет отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="103e1-127">If something goes wrong during playback, however, it could cause the program to stop responding.</span></span> <span data-ttu-id="103e1-128">В реальном приложении используйте цикл обработки сообщений для ожидания завершения воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="103e1-128">In a real application, use a message loop to wait for playback to complete.</span></span> <span data-ttu-id="103e1-129">Также рекомендуется предоставить пользователю способ прерывания воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="103e1-129">It's also recommended that you provide the user with a way to interrupt playback.</span></span>

<span data-ttu-id="103e1-130">По завершении работы с модулем визуализации всегда вызывайте метод [**ирендеренгине:: скрапит**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="103e1-130">When you finish using the render engine, always call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="103e1-131">Этот метод удаляет граф фильтра и освобождает все ресурсы, удерживаемые подсистемой визуализации.</span><span class="sxs-lookup"><span data-stu-id="103e1-131">This method deletes the filter graph and releases any resources held by the render engine.</span></span>


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a><span data-ttu-id="103e1-132">См. также</span><span class="sxs-lookup"><span data-stu-id="103e1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="103e1-133">Загрузка и предварительный просмотр проекта</span><span class="sxs-lookup"><span data-stu-id="103e1-133">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



