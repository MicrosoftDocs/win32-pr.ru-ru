---
description: В этом разделе описывается создание топологии для воспроизведения звука или видео.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Создание топологий воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692070"
---
# <a name="creating-playback-topologies"></a><span data-ttu-id="96a7c-103">Создание топологий воспроизведения</span><span class="sxs-lookup"><span data-stu-id="96a7c-103">Creating Playback Topologies</span></span>

<span data-ttu-id="96a7c-104">В этом разделе описывается создание топологии для воспроизведения звука или видео.</span><span class="sxs-lookup"><span data-stu-id="96a7c-104">This topic describes how to create a topology for audio or video playback.</span></span> <span data-ttu-id="96a7c-105">Для базового воспроизведения можно создать частичную топологию, в которой исходные узлы подключены непосредственно к выходным узлам.</span><span class="sxs-lookup"><span data-stu-id="96a7c-105">For basic playback, you can create a partial topology, in which the source nodes are connected directly to the output nodes.</span></span> <span data-ttu-id="96a7c-106">Нет необходимости вставлять узлы для промежуточных преобразований, например декодеров или цветовых преобразователей.</span><span class="sxs-lookup"><span data-stu-id="96a7c-106">You do not need to insert any nodes for the intermediate transforms, such as decoders or color converters.</span></span> <span data-ttu-id="96a7c-107">Сеанс мультимедиа будет использовать загрузчик топологии для разрешения топологии, а загрузчик топологии будет вставлять необходимые преобразования.</span><span class="sxs-lookup"><span data-stu-id="96a7c-107">The Media Session will use the topology loader to resolve the topology, and the topology loader will insert the transforms that are required.</span></span>

-   [<span data-ttu-id="96a7c-108">Создание топологии</span><span class="sxs-lookup"><span data-stu-id="96a7c-108">Creating the Topology</span></span>](#creating-the-topology)
-   [<span data-ttu-id="96a7c-109">Подключение потоков к приемникам мультимедиа</span><span class="sxs-lookup"><span data-stu-id="96a7c-109">Connecting Streams to Media Sinks</span></span>](#connecting-streams-to-media-sinks)
-   [<span data-ttu-id="96a7c-110">Создание приемника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="96a7c-110">Creating the Media Sink</span></span>](#creating-the-media-sink)
-   [<span data-ttu-id="96a7c-111">Следующие шаги</span><span class="sxs-lookup"><span data-stu-id="96a7c-111">Next Steps</span></span>](#next-steps)
-   [<span data-ttu-id="96a7c-112">См. также</span><span class="sxs-lookup"><span data-stu-id="96a7c-112">Related topics</span></span>](#related-topics)

## <a name="creating-the-topology"></a><span data-ttu-id="96a7c-113">Создание топологии</span><span class="sxs-lookup"><span data-stu-id="96a7c-113">Creating the Topology</span></span>

<span data-ttu-id="96a7c-114">Ниже приведены общие шаги для создания топологии частичного воспроизведения из источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="96a7c-114">Here are the overall steps for creating a partial playback topology from a media source:</span></span>

1.  <span data-ttu-id="96a7c-115">Создайте источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="96a7c-115">Create the media source.</span></span> <span data-ttu-id="96a7c-116">В большинстве случаев для создания источника мультимедиа будет использоваться сопоставитель источников.</span><span class="sxs-lookup"><span data-stu-id="96a7c-116">In most cases, you will use the source resolver to create the media source.</span></span> <span data-ttu-id="96a7c-117">Дополнительные сведения см. в разделе [сопоставитель источников](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="96a7c-117">For more information, see [Source Resolver](source-resolver.md).</span></span>
2.  <span data-ttu-id="96a7c-118">Получение дескриптора презентации источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="96a7c-118">Get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="96a7c-119">Создайте пустую топологию.</span><span class="sxs-lookup"><span data-stu-id="96a7c-119">Create an empty topology.</span></span>
4.  <span data-ttu-id="96a7c-120">Используйте дескриптор представления для перечисления дескрипторов потоков.</span><span class="sxs-lookup"><span data-stu-id="96a7c-120">Use the presentation descriptor to enumerate the stream descriptors.</span></span> <span data-ttu-id="96a7c-121">Для каждого дескриптора потока:</span><span class="sxs-lookup"><span data-stu-id="96a7c-121">For each stream descriptor:</span></span>
    1.  <span data-ttu-id="96a7c-122">Получение основного типа носителя потока, например аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="96a7c-122">Get the stream's major media type, such as audio or video.</span></span>
    2.  <span data-ttu-id="96a7c-123">Проверьте, выбран ли поток в данный момент.</span><span class="sxs-lookup"><span data-stu-id="96a7c-123">Check if the stream is currently selected.</span></span> <span data-ttu-id="96a7c-124">(При необходимости можно выбрать или отменить выбор потока в зависимости от типа носителя.)</span><span class="sxs-lookup"><span data-stu-id="96a7c-124">(Optionally, you can select or deselect a stream, based on the media type.)</span></span>
    3.  <span data-ttu-id="96a7c-125">Если выбран поток, создайте объект активации для приемника мультимедиа на основе типа носителя потока.</span><span class="sxs-lookup"><span data-stu-id="96a7c-125">If the stream is selected, create an activation object for the media sink, based on the stream's media type.</span></span>
    4.  <span data-ttu-id="96a7c-126">Добавьте исходный узел для потока и выходной узел для приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="96a7c-126">Add a source node for the stream and an output node for the media sink.</span></span>
    5.  <span data-ttu-id="96a7c-127">Подключите исходный узел к выходному узлу.</span><span class="sxs-lookup"><span data-stu-id="96a7c-127">Connect the source node to the output node.</span></span>

<span data-ttu-id="96a7c-128">Чтобы упростить этот процесс, пример кода в этом разделе состоит из нескольких функций.</span><span class="sxs-lookup"><span data-stu-id="96a7c-128">To make this process easier to follow, the example code in this topic is organized into several functions.</span></span> <span data-ttu-id="96a7c-129">Функция верхнего уровня называется `CreatePlaybackTopology` .</span><span class="sxs-lookup"><span data-stu-id="96a7c-129">The top-level function is named `CreatePlaybackTopology`.</span></span> <span data-ttu-id="96a7c-130">Он принимает три параметра:</span><span class="sxs-lookup"><span data-stu-id="96a7c-130">It takes three parameters:</span></span>

-   <span data-ttu-id="96a7c-131">Указатель на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="96a7c-131">A pointer to a [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="96a7c-132">Указатель на интерфейс [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) дескриптора презентации.</span><span class="sxs-lookup"><span data-stu-id="96a7c-132">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span> <span data-ttu-id="96a7c-133">Получите этот указатель, вызвав [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="96a7c-133">Get this pointer by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="96a7c-134">Для источников с несколькими презентациями дескрипторы представления для последующих презентаций доставляются в событии [меневпресентатион](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="96a7c-134">For sources with multiple presentations, the presentation descriptors for subsequent presentations are delivered in the [MENewPresentation](menewpresentation.md) event.</span></span>
-   <span data-ttu-id="96a7c-135">Маркер окна приложения.</span><span class="sxs-lookup"><span data-stu-id="96a7c-135">A handle to an application window.</span></span> <span data-ttu-id="96a7c-136">Если источник содержит видео-поток, в этом окне будет показано видео.</span><span class="sxs-lookup"><span data-stu-id="96a7c-136">If the source has a video stream, the video will be displayed in this window.</span></span>

<span data-ttu-id="96a7c-137">Функция возвращает указатель на топологию частичного воспроизведения в параметре *пптопологи* .</span><span class="sxs-lookup"><span data-stu-id="96a7c-137">The function returns a pointer to a partial playback topology in the *ppTopology* parameter.</span></span>


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="96a7c-138">Эта функция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="96a7c-138">This function performs the following steps:</span></span>

1.  <span data-ttu-id="96a7c-139">Вызовите [**мфкреатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) , чтобы создать топологию.</span><span class="sxs-lookup"><span data-stu-id="96a7c-139">Call [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) to create the topology.</span></span> <span data-ttu-id="96a7c-140">Изначально топология не содержит узлов.</span><span class="sxs-lookup"><span data-stu-id="96a7c-140">Initially, the topology does not contain any nodes.</span></span>
2.  <span data-ttu-id="96a7c-141">Вызовите метод [**имфпресентатиондескриптор:: жетстреамдескрипторкаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) , чтобы получить количество потоков в презентации.</span><span class="sxs-lookup"><span data-stu-id="96a7c-141">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the presentation.</span></span>
3.  <span data-ttu-id="96a7c-142">Для каждого потока вызовите функцию, определяемую приложением, `AddBranchToPartialTopology` в ветвь в топологии.</span><span class="sxs-lookup"><span data-stu-id="96a7c-142">For each stream, call the application-defined `AddBranchToPartialTopology` function to a branch in the topology.</span></span> <span data-ttu-id="96a7c-143">Эта функция показана в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="96a7c-143">This function is shown in the next section.</span></span>

## <a name="connecting-streams-to-media-sinks"></a><span data-ttu-id="96a7c-144">Подключение потоков к приемникам мультимедиа</span><span class="sxs-lookup"><span data-stu-id="96a7c-144">Connecting Streams to Media Sinks</span></span>

<span data-ttu-id="96a7c-145">Для каждого выбранного потока добавьте исходный узел и выходной узел, а затем соедините два узла.</span><span class="sxs-lookup"><span data-stu-id="96a7c-145">For each selected stream, add a source node and an output node, then connect the two nodes.</span></span> <span data-ttu-id="96a7c-146">Исходный узел представляет поток.</span><span class="sxs-lookup"><span data-stu-id="96a7c-146">The source node represents the stream.</span></span> <span data-ttu-id="96a7c-147">Выходной узел представляет либо Расширенный модуль [подготовки видео](enhanced-video-renderer.md) (Евр), либо [потоковый рендеринг звука](streaming-audio-renderer.md) (САР).</span><span class="sxs-lookup"><span data-stu-id="96a7c-147">The output node represents either the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) or the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

<span data-ttu-id="96a7c-148">`AddBranchToPartialTopology`Функция, показанная в следующем примере, принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="96a7c-148">The `AddBranchToPartialTopology` function, shown in the next example, takes the following parameters:</span></span>

-   <span data-ttu-id="96a7c-149">Указатель на интерфейс [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) топологии.</span><span class="sxs-lookup"><span data-stu-id="96a7c-149">A pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span>
-   <span data-ttu-id="96a7c-150">Указатель на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="96a7c-150">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="96a7c-151">Указатель на интерфейс [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) дескриптора презентации.</span><span class="sxs-lookup"><span data-stu-id="96a7c-151">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span>
-   <span data-ttu-id="96a7c-152">Отсчитываемый от нуля индекс потока.</span><span class="sxs-lookup"><span data-stu-id="96a7c-152">The zero-based index of the stream.</span></span>
-   <span data-ttu-id="96a7c-153">Маркер окна видео.</span><span class="sxs-lookup"><span data-stu-id="96a7c-153">A handle to the video window.</span></span> <span data-ttu-id="96a7c-154">Этот обработчик используется только для потока видео.</span><span class="sxs-lookup"><span data-stu-id="96a7c-154">This handle is used only for the video stream.</span></span>


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



<span data-ttu-id="96a7c-155">Функция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="96a7c-155">The function does the following:</span></span>

1.  <span data-ttu-id="96a7c-156">Вызывает [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) и передает потоковый индекс.</span><span class="sxs-lookup"><span data-stu-id="96a7c-156">Calls [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and passes in the stream index.</span></span> <span data-ttu-id="96a7c-157">Этот метод возвращает указатель на дескриптор потока для этого потока, а также логическое значение, указывающее, выбран ли поток.</span><span class="sxs-lookup"><span data-stu-id="96a7c-157">This method returns a pointer to the stream descriptor for that stream, along with a Boolean value indicating whether the stream is selected.</span></span>
2.  <span data-ttu-id="96a7c-158">Если поток не выбран, функция завершает работу и возвращает значение S \_ ОК, поскольку приложению не нужно создавать ветвь топологии для потока, если она не выбрана.</span><span class="sxs-lookup"><span data-stu-id="96a7c-158">If the stream is not selected, the function exits and returns S\_OK, because the application does not need to create a topology branch for a stream unless it is selected.</span></span>
3.  <span data-ttu-id="96a7c-159">Если выбран поток, функция завершает ветвь Topology следующим образом:</span><span class="sxs-lookup"><span data-stu-id="96a7c-159">If the stream is selected, the function completes the topology branch as follows:</span></span>
    1.  <span data-ttu-id="96a7c-160">Создает объект активации для приемника, вызывая определяемую приложением функцию Креатемедиасинкактивате.</span><span class="sxs-lookup"><span data-stu-id="96a7c-160">Creates an activation object for the sink, by calling the application-defined CreateMediaSinkActivate function.</span></span> <span data-ttu-id="96a7c-161">Эта функция показана в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="96a7c-161">This function is shown in the next section.</span></span>
    2.  <span data-ttu-id="96a7c-162">Добавляет в топологию исходный узел.</span><span class="sxs-lookup"><span data-stu-id="96a7c-162">Adds a source node to the topology.</span></span> <span data-ttu-id="96a7c-163">Код для этого шага показан в разделе [Создание исходных узлов](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="96a7c-163">Code for this step is shown in the topic [Creating Source Nodes](creating-source-nodes.md).</span></span>
    3.  <span data-ttu-id="96a7c-164">Добавляет выходной узел в топологию.</span><span class="sxs-lookup"><span data-stu-id="96a7c-164">Adds an output node to the topology.</span></span> <span data-ttu-id="96a7c-165">Код для этого шага показан в разделе [Создание выходных узлов](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="96a7c-165">Code for this step is shown in the topic [Creating Output Nodes](creating-output-nodes.md).</span></span>
    4.  <span data-ttu-id="96a7c-166">Подключает два узла путем вызова [**имфтопологиноде:: коннектаутпут**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) на исходном узле.</span><span class="sxs-lookup"><span data-stu-id="96a7c-166">Connects the two nodes by calling [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the source node.</span></span> <span data-ttu-id="96a7c-167">Подключив узлы, приложение указывает, что вышестоящий узел должен доставлять данные в подчиненный узел.</span><span class="sxs-lookup"><span data-stu-id="96a7c-167">By connecting the nodes, the application indicates that the upstream node should deliver data to the downstream node.</span></span> <span data-ttu-id="96a7c-168">Исходный узел имеет один выход, а выходной узел имеет один вход, поэтому оба индекса потоков равны нулю.</span><span class="sxs-lookup"><span data-stu-id="96a7c-168">A source node has one output, and an output node has one input, so both stream indexes are zero.</span></span>

<span data-ttu-id="96a7c-169">Более сложные приложения могут выбирать или отменять выбор потоков вместо использования конфигурации по умолчанию источника.</span><span class="sxs-lookup"><span data-stu-id="96a7c-169">More advanced applications can select or deselect streams, instead of using the source's default configuration.</span></span> <span data-ttu-id="96a7c-170">Источник может иметь несколько потоков, и все они могут быть выбраны по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="96a7c-170">A source could have multiple streams, and any of them might be selected by default.</span></span> <span data-ttu-id="96a7c-171">Дескриптор представления источника мультимедиа имеет набор по умолчанию для выбора потоков.</span><span class="sxs-lookup"><span data-stu-id="96a7c-171">The media source's presentation descriptor has a default set of stream selections.</span></span> <span data-ttu-id="96a7c-172">В простом видеофайле с одним звуковым потоком и видеопотоком источник мультимедиа обычно выбирает оба потока по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="96a7c-172">In a simple video file with a single audio stream and video stream, the media source will usually select both streams by default.</span></span> <span data-ttu-id="96a7c-173">Однако файл может иметь несколько звуковых потоков для разных языков или несколько видеопотоков, закодированных с разной скоростью.</span><span class="sxs-lookup"><span data-stu-id="96a7c-173">However, a file might have multiple audio streams for different languages, or multiple video streams encoded at different bit rates.</span></span> <span data-ttu-id="96a7c-174">В этом случае некоторые из потоков будут отделяться по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="96a7c-174">In that case, some of the streams will be unselected by default.</span></span> <span data-ttu-id="96a7c-175">Приложение может изменить выбор, вызвав [**имфпресентатиондескриптор:: селектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) и [**Имфпресентатиондескриптор::D еселектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) в дескрипторе презентации.</span><span class="sxs-lookup"><span data-stu-id="96a7c-175">The application can change the selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) on the presentation descriptor.</span></span>

## <a name="creating-the-media-sink"></a><span data-ttu-id="96a7c-176">Создание приемника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="96a7c-176">Creating the Media Sink</span></span>

<span data-ttu-id="96a7c-177">Следующая функция создает объект активации для приемника мультимедиа Евр или САР.</span><span class="sxs-lookup"><span data-stu-id="96a7c-177">The next function creates an activation object for the EVR or SAR media sink.</span></span>


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



<span data-ttu-id="96a7c-178">Эта функция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="96a7c-178">This function performs the following steps:</span></span>

1.  <span data-ttu-id="96a7c-179">Вызывает [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) в дескрипторе потока.</span><span class="sxs-lookup"><span data-stu-id="96a7c-179">Calls [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span> <span data-ttu-id="96a7c-180">Этот метод возвращает указатель интерфейса [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="96a7c-180">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface pointer.</span></span>

2.  <span data-ttu-id="96a7c-181">Вызывает [**имфмедиатипехандлер:: жетмажортипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="96a7c-181">Calls [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="96a7c-182">Этот метод возвращает идентификатор GUID основного типа для потока.</span><span class="sxs-lookup"><span data-stu-id="96a7c-182">This method returns the major type GUID for the stream.</span></span>

3.  <span data-ttu-id="96a7c-183">Если тип потока — Audio, функция вызывает [**мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) для создания объекта активации модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="96a7c-183">If the stream type is audio, the function calls [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) to create the audio renderer activation object.</span></span> <span data-ttu-id="96a7c-184">Если тип потока — Video, функция вызывает [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) для создания объекта активации модуля обработки видео.</span><span class="sxs-lookup"><span data-stu-id="96a7c-184">If the stream type is video, the function calls [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the video renderer activation object.</span></span> <span data-ttu-id="96a7c-185">Обе эти функции возвращают указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="96a7c-185">Both of these functions return a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="96a7c-186">Этот указатель используется для инициализации выходного узла для приемника, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="96a7c-186">This pointer is used to initialize the output node for the sink, as shown previously.</span></span>

<span data-ttu-id="96a7c-187">Для любого другого типа потока этот пример возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="96a7c-187">For any other stream type, this example returns an error code.</span></span> <span data-ttu-id="96a7c-188">Кроме того, можно просто отменить выбор потока.</span><span class="sxs-lookup"><span data-stu-id="96a7c-188">Alternatively, you could simply deselect the stream.</span></span>

## <a name="next-steps"></a><span data-ttu-id="96a7c-189">Next Steps</span><span class="sxs-lookup"><span data-stu-id="96a7c-189">Next Steps</span></span>

<span data-ttu-id="96a7c-190">Чтобы воспроизвести один файл мультимедиа за раз, необходимо поставить в очередь топологию в сеансе мультимедиа, вызвав [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="96a7c-190">To play one media file at a time, queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="96a7c-191">Сеанс мультимедиа будет использовать загрузчик топологии для разрешения топологии.</span><span class="sxs-lookup"><span data-stu-id="96a7c-191">The Media Session will use the topology loader to resolve the topology.</span></span> <span data-ttu-id="96a7c-192">Полный пример см. в разделе [Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="96a7c-192">For a complete example, see [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96a7c-193">См. также</span><span class="sxs-lookup"><span data-stu-id="96a7c-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96a7c-194">Как воспроизвести незащищенные файлы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="96a7c-194">How to Play Unprotected Media Files</span></span>](how-to-play-unprotected-media-files.md)
</dt> <dt>

[<span data-ttu-id="96a7c-195">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="96a7c-195">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="96a7c-196">Топологии</span><span class="sxs-lookup"><span data-stu-id="96a7c-196">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



