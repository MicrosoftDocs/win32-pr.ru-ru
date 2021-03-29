---
description: Воспроизведение файла
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Воспроизведение файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423085"
---
# <a name="how-to-play-a-file"></a><span data-ttu-id="dcf4b-103">Воспроизведение файла</span><span class="sxs-lookup"><span data-stu-id="dcf4b-103">How To Play a File</span></span>

<span data-ttu-id="dcf4b-104">Эта статья призвана предоставить вам версию программирования DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-104">This article is intended to give you the flavor of DirectShow programming.</span></span> <span data-ttu-id="dcf4b-105">Он представляет простое консольное приложение, которое воспроизводит аудио-или видеофайл.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-105">It presents a simple console application that plays an audio or video file.</span></span> <span data-ttu-id="dcf4b-106">Программа состоит всего из нескольких строк, но она демонстрирует некоторые возможности программирования DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-106">The program is only a few lines long, but it demonstrates some of the power of DirectShow programming.</span></span>

<span data-ttu-id="dcf4b-107">Как описано в статье [Введение в программирование приложений DirectShow](introduction-to-directshow-application-programming.md) , приложение DirectShow всегда выполняет те же основные действия:</span><span class="sxs-lookup"><span data-stu-id="dcf4b-107">As the article [Introduction to DirectShow Application Programming](introduction-to-directshow-application-programming.md) describes, a DirectShow application always performs the same basic steps:</span></span>

1.  <span data-ttu-id="dcf4b-108">Создайте экземпляр [диспетчера графа фильтров](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="dcf4b-108">Create an instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="dcf4b-109">Используйте диспетчер графа фильтров для создания графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-109">Use the Filter Graph Manager to build a filter graph.</span></span>
3.  <span data-ttu-id="dcf4b-110">Запустите граф, что приведет к перемещению данных по фильтрам.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-110">Run the graph, causing data to move through the filters.</span></span>

<span data-ttu-id="dcf4b-111">Чтобы скомпилировать и связать код в этом разделе, включите заголовочный файл DShow. h и укажите ссылку на файл статической библиотеки стрмиидс. lib.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-111">To compile and link the code in this topic, include the header file Dshow.h and link to the static library file strmiids.lib.</span></span> <span data-ttu-id="dcf4b-112">Дополнительные сведения см. в разделе [Создание приложений DirectShow](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="dcf4b-112">For more information, see [Building DirectShow Applications](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="dcf4b-113">Начните [**с вызова CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM:</span><span class="sxs-lookup"><span data-stu-id="dcf4b-113">Start by calling [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library:</span></span>


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



<span data-ttu-id="dcf4b-114">Для простоты в этом примере игнорируется возвращаемое значение, но всегда следует проверять значение **HRESULT** из любого вызова метода.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-114">To keep things simple, this example ignores the return value, but you should always check the **HRESULT** value from any method call.</span></span>

<span data-ttu-id="dcf4b-115">Затем вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания диспетчера графа фильтров:</span><span class="sxs-lookup"><span data-stu-id="dcf4b-115">Next, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Filter Graph Manager:</span></span>


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



<span data-ttu-id="dcf4b-116">Как показано, идентификатором класса является CLSID \_ филтерграф.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-116">As shown, the class identifier (CLSID) is CLSID\_FilterGraph.</span></span> <span data-ttu-id="dcf4b-117">Диспетчер графов фильтров предоставляется внутри внутрипроцессного DLL, поэтому контекст выполнения — **КЛСКТКС \_ INPROC \_ Server**.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-117">The Filter Graph Manager is provided by an in-process DLL, so the execution context is **CLSCTX\_INPROC\_SERVER**.</span></span> <span data-ttu-id="dcf4b-118">DirectShow поддерживает модель свободной потоковой модели, поэтому можно также вызвать [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) с флагом **\_ многопотоковой инициализации** .</span><span class="sxs-lookup"><span data-stu-id="dcf4b-118">DirectShow supports the free-threading model, so you can also call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="dcf4b-119">Вызов [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) возвращает интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , который в основном содержит методы для построения графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-119">The call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) returns the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface, which mostly contains methods for building the filter graph.</span></span> <span data-ttu-id="dcf4b-120">Для этого примера необходимы два других интерфейса:</span><span class="sxs-lookup"><span data-stu-id="dcf4b-120">Two other interfaces are needed for this example:</span></span>

-   <span data-ttu-id="dcf4b-121">[**Имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) управляет потоковой передачей.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) controls streaming.</span></span> <span data-ttu-id="dcf4b-122">Он содержит методы для остановки и запуска графа.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-122">It contains methods for stopping and starting the graph.</span></span>
-   <span data-ttu-id="dcf4b-123">[**Имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) имеет методы для получения событий из диспетчера графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) has methods for getting events from the Filter Graph Manager.</span></span> <span data-ttu-id="dcf4b-124">В этом примере интерфейс используется для ожидания завершения воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-124">In this example, the interface is used to wait for playback to complete.</span></span>

<span data-ttu-id="dcf4b-125">Оба этих интерфейса предоставляются диспетчером графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-125">Both of these interfaces are exposed by the Filter Graph Manager.</span></span> <span data-ttu-id="dcf4b-126">Используйте возвращенный указатель [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) для запроса этих запросов:</span><span class="sxs-lookup"><span data-stu-id="dcf4b-126">Use the returned [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) pointer to query for them:</span></span>


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="dcf4b-127">Теперь можно построить граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-127">Now you can build the filter graph.</span></span> <span data-ttu-id="dcf4b-128">Для воспроизведения файла это делается одним вызовом метода:</span><span class="sxs-lookup"><span data-stu-id="dcf4b-128">For file playback, this is done by a single method call:</span></span>


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



<span data-ttu-id="dcf4b-129">Метод [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) создает граф фильтра, который может воспроизвести указанный файл.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-129">The [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method builds a filter graph that can play the specified file.</span></span> <span data-ttu-id="dcf4b-130">Первый параметр — это имя файла, представленное в виде строки расширенных символов (2 байта).</span><span class="sxs-lookup"><span data-stu-id="dcf4b-130">The first parameter is the file name, represented as a wide character (2-byte) string.</span></span> <span data-ttu-id="dcf4b-131">Второй параметр зарезервирован и должен равняться **null**.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-131">The second parameter is reserved and must equal **NULL**.</span></span>

<span data-ttu-id="dcf4b-132">Этот метод может завершиться ошибкой, если указанный файл не существует или формат файла не распознан.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-132">This method can fail if the specified file does not exist, or the file format is not recognized.</span></span> <span data-ttu-id="dcf4b-133">При условии, что метод выполнен правильно, граф фильтра теперь готов к воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-133">Assuming that the method succeeds, however, the filter graph is now ready for playback.</span></span> <span data-ttu-id="dcf4b-134">Чтобы запустить граф, вызовите метод [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :</span><span class="sxs-lookup"><span data-stu-id="dcf4b-134">To run the graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method:</span></span>


```C++
hr = pControl->Run();
```



<span data-ttu-id="dcf4b-135">При выполнении графа фильтра данные перемещаются по фильтрам и подготавливаются к просмотру как видео и аудио.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-135">When the filter graph runs, data moves through the filters and is rendered as video and audio.</span></span> <span data-ttu-id="dcf4b-136">Воспроизведение выполняется в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-136">Playback occurs on a separate thread.</span></span> <span data-ttu-id="dcf4b-137">Можно подождать завершения воспроизведения, вызвав метод [**имедиаевент:: ваитфоркомплетион**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :</span><span class="sxs-lookup"><span data-stu-id="dcf4b-137">You can wait for playback to complete by calling the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method:</span></span>


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



<span data-ttu-id="dcf4b-138">Этот метод блокируется до окончания воспроизведения файла или до истечения заданного интервала времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-138">This method blocks until the file is done playing, or until the specified time-out interval elapses.</span></span> <span data-ttu-id="dcf4b-139">Значение INFINITE означает, что приложение блокируется на неограниченное время до завершения воспроизведения файла.</span><span class="sxs-lookup"><span data-stu-id="dcf4b-139">The value INFINITE means the application blocks indefinitely until the file is done playing.</span></span> <span data-ttu-id="dcf4b-140">Более реалистичный пример обработки событий см. в разделе [реагирование на события](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="dcf4b-140">For a more realistic example of event handling, see [Responding to Events](responding-to-events.md).</span></span>

<span data-ttu-id="dcf4b-141">После завершения работы приложения Освободите указатели интерфейса и закройте библиотеку COM:</span><span class="sxs-lookup"><span data-stu-id="dcf4b-141">When the application is finished, release the interface pointers and close the COM library:</span></span>


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a><span data-ttu-id="dcf4b-142">Пример кода</span><span class="sxs-lookup"><span data-stu-id="dcf4b-142">Example Code</span></span>

<span data-ttu-id="dcf4b-143">Ниже приведен полный код для примера, описанного в этой статье:</span><span class="sxs-lookup"><span data-stu-id="dcf4b-143">Here is the complete code for the example described in this article:</span></span>


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="dcf4b-144">См. также</span><span class="sxs-lookup"><span data-stu-id="dcf4b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcf4b-145">Основные задачи DirectShow</span><span class="sxs-lookup"><span data-stu-id="dcf4b-145">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 
