---
description: В этом разделе описывается использование источника последовательности для воспроизведения последовательности файлов.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Создание списка воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543610"
---
# <a name="how-to-create-a-playlist"></a><span data-ttu-id="59b86-103">Создание списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="59b86-103">How to Create a Playlist</span></span>

<span data-ttu-id="59b86-104">В этом разделе описывается использование источника последовательности для воспроизведения последовательности файлов.</span><span class="sxs-lookup"><span data-stu-id="59b86-104">This topic describes how to use the Sequence Source to play a sequence of files.</span></span>

## <a name="overview"></a><span data-ttu-id="59b86-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="59b86-105">Overview</span></span>

<span data-ttu-id="59b86-106">Чтобы воспроизвести файлы мультимедиа в последовательности, приложение должно добавить топологии в последовательность для создания списка воспроизведения и поставить эти топологии в сеансе мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="59b86-106">To play media files in a sequence, the application must add topologies in a sequence to create a playlist, and queue these topologies on the Media Session for playback.</span></span>

<span data-ttu-id="59b86-107">Источник Sequencer обеспечивает эффективное воспроизведение, инициализируя и загружая следующую топологию, прежде чем сеанс мультимедиа начнет воспроизводить текущую топологию.</span><span class="sxs-lookup"><span data-stu-id="59b86-107">The sequencer source ensures seamless playback by initializing and loading the next topology before the Media Session starts playing the current topology.</span></span> <span data-ttu-id="59b86-108">Это позволяет приложению быстро запускать следующую топологию при необходимости.</span><span class="sxs-lookup"><span data-stu-id="59b86-108">This enables the application to start the next topology quickly whenever it is required.</span></span>

<span data-ttu-id="59b86-109">Сеанс мультимедиа отвечает за передачу данных в приемники и воспроизведение топологий в источнике последовательности.</span><span class="sxs-lookup"><span data-stu-id="59b86-109">The Media Session is responsible for feeding data to the sinks and playing the topologies in the sequence source.</span></span> <span data-ttu-id="59b86-110">Кроме того, сеанс мультимедиа управляет временем презентации для сегментов.</span><span class="sxs-lookup"><span data-stu-id="59b86-110">In addition, the Media Session manages the presentation time for the segments.</span></span>

<span data-ttu-id="59b86-111">Дополнительные сведения о том, как источник Sequencer управляет топологиями, см. [в разделе сведения о источнике Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="59b86-111">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="59b86-112">В этом пошаговом руководстве содержатся следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="59b86-112">This walk-through contains the following steps:</span></span>

1.  [<span data-ttu-id="59b86-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="59b86-113">Prerequisites</span></span>](#prerequisites)
2.  [<span data-ttu-id="59b86-114">Инициализация Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59b86-114">Initializing Media Foundation</span></span>](#initializing-media-foundation)
3.  [<span data-ttu-id="59b86-115">Создание объектов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59b86-115">Creating Media Foundation Objects</span></span>](#creating-media-foundation-objects)
4.  [<span data-ttu-id="59b86-116">Создание источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="59b86-116">Creating the Media Source</span></span>](#creating-the-media-source)
5.  [<span data-ttu-id="59b86-117">Создание частичных топологий</span><span class="sxs-lookup"><span data-stu-id="59b86-117">Creating Partial Topologies</span></span>](#creating-partial-topologies)
6.  [<span data-ttu-id="59b86-118">Добавление топологий в источник Sequencer</span><span class="sxs-lookup"><span data-stu-id="59b86-118">Adding Topologies to the Sequencer Source</span></span>](#adding-topologies-to-the-sequencer-source)
7.  [<span data-ttu-id="59b86-119">Настройка первой топологии в сеансе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="59b86-119">Setting the First Topology on the Media Session</span></span>](#setting-the-first-topology-on-the-media-session)
8.  [<span data-ttu-id="59b86-120">Постановка следующей топологии в очередь в сеансе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="59b86-120">Queuing the Next Topology on the Media Session</span></span>](#queuing-the-next-topology-on-the-media-session)
9.  [<span data-ttu-id="59b86-121">Освобождение источника Sequencer</span><span class="sxs-lookup"><span data-stu-id="59b86-121">Releasing the Sequencer Source</span></span>](#releasing-the-sequencer-source)

<span data-ttu-id="59b86-122">Приведенные в этом разделе примеры кода являются выдержками из [исходного примера программы Sequencer](sequencer-source-example-code.md), который содержит полный код примера.</span><span class="sxs-lookup"><span data-stu-id="59b86-122">The code examples shown this topic are excerpts from the topic [Sequencer Source Example Code](sequencer-source-example-code.md), which contains the complete example code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="59b86-123">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="59b86-123">Prerequisites</span></span>

<span data-ttu-id="59b86-124">Перед началом этого пошагового руководства ознакомьтесь со следующими концепциями Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="59b86-124">Before starting this walk-through, familiarize yourself with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="59b86-125">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="59b86-125">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="59b86-126">Топологии</span><span class="sxs-lookup"><span data-stu-id="59b86-126">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="59b86-127">Генераторы событий мультимедиа</span><span class="sxs-lookup"><span data-stu-id="59b86-127">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="59b86-128">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="59b86-128">Presentation Descriptors</span></span>](presentation-descriptors.md)

<span data-ttu-id="59b86-129">Также прочитайте [о том, как воспроизводить файлы мультимедиа с помощью Media Foundation](how-to-play-unprotected-media-files.md), так как пример кода, Швон здесь, расширяется по коду в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="59b86-129">Also read [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), because the example code shwon here expands on the code in that topic.</span></span>

## <a name="initializing-media-foundation"></a><span data-ttu-id="59b86-130">Инициализация Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59b86-130">Initializing Media Foundation</span></span>

<span data-ttu-id="59b86-131">Прежде чем можно будет использовать любые Media Foundation интерфейсы или методы, инициализируйте Media Foundation, вызвав функцию [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="59b86-131">Before you can use any Media Foundation interfaces or methods, initialize Media Foundation by calling the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="59b86-132">Дополнительные сведения см. в разделе [инициализация Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="59b86-132">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a><span data-ttu-id="59b86-133">Создание объектов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59b86-133">Creating Media Foundation Objects</span></span>

<span data-ttu-id="59b86-134">Затем создайте следующие объекты Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="59b86-134">Next, create the following Media Foundation objects:</span></span>

-   <span data-ttu-id="59b86-135">Сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59b86-135">Media session.</span></span> <span data-ttu-id="59b86-136">Этот объект предоставляет интерфейс [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , который предоставляет методы для воспроизведения, приостановки и остановки текущей топологии.</span><span class="sxs-lookup"><span data-stu-id="59b86-136">This object exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface, which provides methods to play, pause, and stop the current topology.</span></span>
-   <span data-ttu-id="59b86-137">Источник Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59b86-137">Sequencer source.</span></span> <span data-ttu-id="59b86-138">Этот объект предоставляет интерфейс [**имфсекуенцерсаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , который предоставляет методы для добавления, обновления и удаления топологий в последовательности.</span><span class="sxs-lookup"><span data-stu-id="59b86-138">This object exposes the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface, which provides methods to add, update, and delete topologies in a sequence.</span></span>

1.  <span data-ttu-id="59b86-139">Чтобы создать сеанс мультимедиа, вызовите функцию [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) .</span><span class="sxs-lookup"><span data-stu-id="59b86-139">Call the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function to create the Media Session.</span></span>
2.  <span data-ttu-id="59b86-140">Вызовите метод [**имфмедиаевенткуеуе:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) , чтобы запросить первое событие из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59b86-140">Call [**IMFMediaEventQueue::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) to request the first event from the Media Session.</span></span>
3.  <span data-ttu-id="59b86-141">Вызовите функцию [**мфкреатесекуенцерсаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) , чтобы создать источник Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59b86-141">Call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function to create the sequencer source.</span></span>

<span data-ttu-id="59b86-142">Следующий код создает сеанс мультимедиа и запрашивает первое событие:</span><span class="sxs-lookup"><span data-stu-id="59b86-142">The following code creates the Media Session and requests the first event:</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a><span data-ttu-id="59b86-143">Создание источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="59b86-143">Creating the Media Source</span></span>

<span data-ttu-id="59b86-144">Затем создайте источник мультимедиа для первого сегмента списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="59b86-144">Next, create a media source for the first playlist segment.</span></span> <span data-ttu-id="59b86-145">Используйте [сопоставитель источников](source-resolver.md) для создания источника мультимедиа на основе URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="59b86-145">Use the [Source Resolver](source-resolver.md) to create a media source from a URL.</span></span> <span data-ttu-id="59b86-146">Для этого вызовите функцию [**мфкреатесаурцересолвер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) , чтобы создать сопоставитель источника, а затем вызовите метод [**Имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) , чтобы создать источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59b86-146">To do this, call the [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) function to create a source resolver and then call the [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method to create the media source.</span></span>

<span data-ttu-id="59b86-147">Сведения об источниках мультимедиа см. в статье [источники мультимедиа](media-sources.md).</span><span class="sxs-lookup"><span data-stu-id="59b86-147">For information about media sources, see [Media Sources](media-sources.md).</span></span>

## <a name="creating-partial-topologies"></a><span data-ttu-id="59b86-148">Создание частичных топологий</span><span class="sxs-lookup"><span data-stu-id="59b86-148">Creating Partial Topologies</span></span>

<span data-ttu-id="59b86-149">Каждый сегмент в источнике Sequencer имеет собственную частичную топологию.</span><span class="sxs-lookup"><span data-stu-id="59b86-149">Each segment in the sequencer source has its own partial topology.</span></span> <span data-ttu-id="59b86-150">Затем создайте частичные топологии для источников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59b86-150">Next, create partial topologies for media sources.</span></span> <span data-ttu-id="59b86-151">Для частичной топологии исходные узлы топологии напрямую соединяются с выходными узлами без указания промежуточных преобразований.</span><span class="sxs-lookup"><span data-stu-id="59b86-151">For a partial topology, the topology source nodes are connected directly to the output nodes, without specifying any intermediate transforms.</span></span> <span data-ttu-id="59b86-152">Сеанс мультимедиа использует объект Loader Topology для разрешения топологии.</span><span class="sxs-lookup"><span data-stu-id="59b86-152">The Media Session uses the topology loader object to resolve the topology.</span></span> <span data-ttu-id="59b86-153">После разрешения топологии добавляются необходимые декодеры и другие узлы преобразования.</span><span class="sxs-lookup"><span data-stu-id="59b86-153">After a topology is resolved, the required decoders and other transform nodes are added.</span></span> <span data-ttu-id="59b86-154">Источник Sequencer также может содержать полные топологии.</span><span class="sxs-lookup"><span data-stu-id="59b86-154">The sequencer source can also contain full topologies.</span></span>

<span data-ttu-id="59b86-155">Чтобы создать объект Topology, используйте функцию [**мфкреатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) , а затем используйте интерфейс [**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) для создания узлов потоков.</span><span class="sxs-lookup"><span data-stu-id="59b86-155">To create the topology object, use the [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) function and then use the [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface to create stream nodes.</span></span>

<span data-ttu-id="59b86-156">Полные инструкции по использованию этих программных элементов для создания топологий см. в разделе [Создание топологий воспроизведения](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="59b86-156">For complete instructions on using these programming elements to create topologies, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="59b86-157">Приложение может воспроизвести выбранную часть исходного кода, настроив исходный узел.</span><span class="sxs-lookup"><span data-stu-id="59b86-157">An application can play a selected portion of the native source by configuring the source node.</span></span> <span data-ttu-id="59b86-158">Для этого задайте атрибут [**MF \_ топоноде \_ Медиастарт**](mf-toponode-mediastart-attribute.md) и атрибут [**MF \_ Топоноде \_ медиастоп**](mf-toponode-mediastop-attribute.md) в **\_ \_ \_ узле** топология MF в топологии с саурцестреам узлами.</span><span class="sxs-lookup"><span data-stu-id="59b86-158">To do this, set the [**MF\_TOPONODE\_MEDIASTART**](mf-toponode-mediastart-attribute.md) attribute and the [**MF\_TOPONODE\_MEDIASTOP**](mf-toponode-mediastop-attribute.md) attribute on **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** topology nodes.</span></span> <span data-ttu-id="59b86-159">Укажите время начала и время окончания работы носителя относительно начала исходного источника как типы **UINT64** .</span><span class="sxs-lookup"><span data-stu-id="59b86-159">Specify the media start time and the media stop time relative to the start of the native source as **UINT64** types.</span></span>

## <a name="adding-topologies-to-the-sequencer-source"></a><span data-ttu-id="59b86-160">Добавление топологий в источник Sequencer</span><span class="sxs-lookup"><span data-stu-id="59b86-160">Adding Topologies to the Sequencer Source</span></span>

<span data-ttu-id="59b86-161">Затем добавьте к источнику Sequencer созданные разделяемые топологии.</span><span class="sxs-lookup"><span data-stu-id="59b86-161">Next, add to the sequencer source the partial topologies that you created.</span></span> <span data-ttu-id="59b86-162">Каждому элементу последовательности, называемому *сегментом*, присваивается идентификатор **мфсекуенцерелементид** .</span><span class="sxs-lookup"><span data-stu-id="59b86-162">Each sequence element, called a *segment*, is assigned an **MFSequencerElementId** identifier.</span></span> <span data-ttu-id="59b86-163">Дополнительные сведения о том, как источник Sequencer управляет топологиями, см. [в разделе сведения о источнике Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="59b86-163">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="59b86-164">После добавления всех топологий в источник Sequencer приложение должно отметить последний сегмент в последовательности для завершения воспроизведения в конвейере.</span><span class="sxs-lookup"><span data-stu-id="59b86-164">After all of the topologies are added to the sequencer source, the application must flag the last segment in the sequence to end playback in the pipeline.</span></span> <span data-ttu-id="59b86-165">Без этого флага источник Sequencer требует добавления дополнительных топологий.</span><span class="sxs-lookup"><span data-stu-id="59b86-165">Without this flag, the sequencer source expects more topologies to be added.</span></span>

1.  <span data-ttu-id="59b86-166">Вызовите метод [**имфсекуенцерсаурце:: аппендтопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) , чтобы добавить определенную топологию в источник Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59b86-166">Call the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method to add a specific topology to the sequencer source.</span></span>

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    <span data-ttu-id="59b86-167">[**Аппендтопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) добавляет указанную топологию в последовательность.</span><span class="sxs-lookup"><span data-stu-id="59b86-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) adds the specified topology to the sequence.</span></span> <span data-ttu-id="59b86-168">Этот метод возвращает идентификатор сегмента в параметре *пдвид* .</span><span class="sxs-lookup"><span data-stu-id="59b86-168">This method returns the segment identifier in the *pdwId* parameter.</span></span>

    <span data-ttu-id="59b86-169">Если топология является последней в источнике Sequencer, передайте Секуенцертопологифлагс \_ последним в параметре *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="59b86-169">If the topology is the last one in the sequencer source, pass SequencerTopologyFlags\_Last in the *dwFlags* parameter.</span></span> <span data-ttu-id="59b86-170">Это значение определено в перечислении [**мфсекуенцертопологифлагс**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .</span><span class="sxs-lookup"><span data-stu-id="59b86-170">This value is defined in the [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) enumeration.</span></span>

2.  <span data-ttu-id="59b86-171">Вызовите [**имфсекуенцерсаурце:: упдатетопологифлагс**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) , чтобы обновить флаги топологии, связанной с идентификатором сегмента во входном списке.</span><span class="sxs-lookup"><span data-stu-id="59b86-171">Call [**IMFSequencerSource::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) to update the flags for the topology associated with the segment identifier in the input list.</span></span> <span data-ttu-id="59b86-172">В этом случае вызов указывает, что указанный сегмент является последним сегментом в секвенсоре.</span><span class="sxs-lookup"><span data-stu-id="59b86-172">In this case, the call indicates that the specified segment is the last segment in the sequencer.</span></span> <span data-ttu-id="59b86-173">(Этот вызов необязателен, если последняя топология указана в вызове [**аппендтопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) .)</span><span class="sxs-lookup"><span data-stu-id="59b86-173">(This call is optional if the last topology is specified in the [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) call.)</span></span>

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

<span data-ttu-id="59b86-174">Приложение может заменить топологию сегмента другой топологией, вызвав метод [**имфсекуенцерсаурце:: упдатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) и передав новую топологию в *птопологи*.</span><span class="sxs-lookup"><span data-stu-id="59b86-174">The application can replace a segment's topology with another topology by calling the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) and passing the new topology in *pTopology*.</span></span> <span data-ttu-id="59b86-175">Если в новой топологии есть новые собственные источники, источники добавляются в исходный кэш.</span><span class="sxs-lookup"><span data-stu-id="59b86-175">If there are new native sources in the new topology, the sources are added to the source cache.</span></span> <span data-ttu-id="59b86-176">Список предустановленного обновления также обновляется.</span><span class="sxs-lookup"><span data-stu-id="59b86-176">The preroll list is also refreshed.</span></span>

## <a name="setting-the-first-topology-on-the-media-session"></a><span data-ttu-id="59b86-177">Настройка первой топологии в сеансе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="59b86-177">Setting the First Topology on the Media Session</span></span>

<span data-ttu-id="59b86-178">Затем поочередно ставить первую топологию в источнике последовательности в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59b86-178">Next, queue the first topology in the sequence source on the Media Session.</span></span> <span data-ttu-id="59b86-179">Чтобы получить первую топологию из источника Sequencer, приложение должно вызвать метод [**имфмедиасаурцетопологипровидер:: жетмедиасаурцетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="59b86-179">To get the first topology from the sequencer source, the application must call the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="59b86-180">Этот метод возвращает частичную топологию, которая разрешается сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59b86-180">This method returns the partial topology, which is resolved by the Media Session.</span></span>

<span data-ttu-id="59b86-181">Сведения о частичной топологии см. в разделе [о топологиях](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="59b86-181">For information about partial topologies, see [About Topologies](about-topologies.md).</span></span>

1.  <span data-ttu-id="59b86-182">Получите собственный источник мультимедиа для первой топологии источника последовательности.</span><span class="sxs-lookup"><span data-stu-id="59b86-182">Retrieve the native media source for the first topology of the sequence source.</span></span>
2.  <span data-ttu-id="59b86-183">Создайте дескриптор представления для источника мультимедиа, вызвав метод [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="59b86-183">Create a presentation descriptor for the media source by calling the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>
3.  <span data-ttu-id="59b86-184">Получите связанную топологию для презентации, вызвав метод [**имфмедиасаурцетопологипровидер:: жетмедиасаурцетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="59b86-184">Retrieve the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
4.  <span data-ttu-id="59b86-185">Установите первую топологию в сеансе мультимедиа, вызвав [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="59b86-185">Set the first topology on the Media Session by Calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

    <span data-ttu-id="59b86-186">Вызовите [**сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , указав для параметра *двсеттопологифлагс* значение **null**.</span><span class="sxs-lookup"><span data-stu-id="59b86-186">Call [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the *dwSetTopologyFlags* parameter set to **NULL**.</span></span> <span data-ttu-id="59b86-187">Это указывает сеансу мультимедиа запустить указанную топологию по завершении текущей топологии.</span><span class="sxs-lookup"><span data-stu-id="59b86-187">This instructs the Media Session to start the specified topology when the current topology has been completed.</span></span> <span data-ttu-id="59b86-188">Так как в этом случае указанная топология является первой, а текущая презентация отсутствует, сеанс мультимедиа запускает новую презентацию немедленно.</span><span class="sxs-lookup"><span data-stu-id="59b86-188">Because in this case, the specified topology is the first topology and there is no current presentation, the Media Session starts the new presentation immediately.</span></span>

    <span data-ttu-id="59b86-189">Значение **null** также указывает на то, что сеанс мультимедиа должен разрешить топологию, так как топология, возвращаемая поставщиком топологии, всегда является частичной топологией.</span><span class="sxs-lookup"><span data-stu-id="59b86-189">The **NULL** value also indicates that Media Session must resolve the topology because the topology returned by the topology provider is always a partial topology.</span></span>


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



## <a name="queuing-the-next-topology-on-the-media-session"></a><span data-ttu-id="59b86-190">Постановка следующей топологии в очередь в сеансе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="59b86-190">Queuing the Next Topology on the Media Session</span></span>

<span data-ttu-id="59b86-191">Затем приложению необходимо выполнить обработку события [меневпресентатион](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="59b86-191">Next, the application needs to handle the [MENewPresentation](menewpresentation.md) event.</span></span>

<span data-ttu-id="59b86-192">Источник Sequencer вызывает [меневпресентатион](menewpresentation.md) , когда сеанс мультимедиа начинает воспроизводить сегмент с другим сегментом после него.</span><span class="sxs-lookup"><span data-stu-id="59b86-192">Sequencer source raises [MENewPresentation](menewpresentation.md) when the Media Session starts playing a segment that has another segment following it.</span></span> <span data-ttu-id="59b86-193">Это событие информирует приложение о следующей топологии в источнике последовательности, предоставляя дескриптор представления для следующего сегмента в списке предподготовки.</span><span class="sxs-lookup"><span data-stu-id="59b86-193">This event informs the application about the next topology in the sequence source by providing the presentation descriptor for the next segment in the preroll list.</span></span> <span data-ttu-id="59b86-194">Приложение должно получить связанную топологию с помощью поставщика топологии и поместить его в очередь в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59b86-194">The application must retrieve the associated topology, by using the topology provider, and queue it on the Media Session.</span></span> <span data-ttu-id="59b86-195">Затем источник Sequencer выполняет откат этой топологии, что обеспечивает простой переход между презентациями.</span><span class="sxs-lookup"><span data-stu-id="59b86-195">The sequencer source then prerolls this topology, which ensures a seamless transition between presentations.</span></span>

<span data-ttu-id="59b86-196">Когда приложение выполняет поиск по сегментам, приложение получает несколько событий [меневпресентатион](menewpresentation.md) , так как источник Sequencer обновляет предварительную отрезку и настраивает правильную топологию.</span><span class="sxs-lookup"><span data-stu-id="59b86-196">When the application seeks across segments, the application receives several [MENewPresentation](menewpresentation.md) events as the sequencer source refreshes the preroll list and sets up the correct topology.</span></span> <span data-ttu-id="59b86-197">Приложение должно выполнить обработку каждого события и поставить в очередь топологию, возвращенную в данных события, в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59b86-197">The application must handle each event and queue the topology returned in the event data, on the Media Session.</span></span> <span data-ttu-id="59b86-198">Дополнительные сведения о пропущенных сегментах см. [в разделе Использование источника Sequencer](using-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="59b86-198">For information about skipping segments, see [Using the Sequencer Source](using-the-sequencer-source.md).</span></span>

<span data-ttu-id="59b86-199">Дополнительные сведения о получении уведомлений об источниках Sequencer см. в статье [источники событий Sequencer](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="59b86-199">For information about getting sequencer source notifications, see [Sequencer Source Events](sequencer-source-events.md).</span></span>

1.  <span data-ttu-id="59b86-200">В обработчике событий [меневпресентатион](menewpresentation.md) извлеките дескриптор представления для следующего сегмента из данных события.</span><span class="sxs-lookup"><span data-stu-id="59b86-200">In the [MENewPresentation](menewpresentation.md) event handler, retrieve the presentation descriptor for the next segment from the event data.</span></span>
2.  <span data-ttu-id="59b86-201">Получите связанную топологию для презентации, вызвав метод [**имфмедиасаурцетопологипровидер:: жетмедиасаурцетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="59b86-201">Get the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
3.  <span data-ttu-id="59b86-202">Задайте топологию в сеансе мультимедиа, вызвав метод [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .</span><span class="sxs-lookup"><span data-stu-id="59b86-202">Set the topology on the Media Session by calling the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>

    <span data-ttu-id="59b86-203">Сеанс мультимедиа запускает новую презентацию после завершения текущей презентации.</span><span class="sxs-lookup"><span data-stu-id="59b86-203">The Media Session starts the new presentation when the current presentation has been completed.</span></span>


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a><span data-ttu-id="59b86-204">Освобождение источника Sequencer</span><span class="sxs-lookup"><span data-stu-id="59b86-204">Releasing the Sequencer Source</span></span>

<span data-ttu-id="59b86-205">Наконец, завершите работу источника Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59b86-205">Finally, shut down the sequencer source.</span></span> <span data-ttu-id="59b86-206">Для этого вызовите метод [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) в источнике Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59b86-206">To do so, call the [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) method on the sequencer source.</span></span> <span data-ttu-id="59b86-207">Этот вызов завершает работу всех базовых исходных источников мультимедиа в источнике Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59b86-207">This call shuts down all of the underlying native media sources in the sequencer source.</span></span>

<span data-ttu-id="59b86-208">После освобождения источника Sequencer приложение должно закрыть и завершить сеанс мультимедиа, вызвав [**имфмедиасессион:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) и [**Имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="59b86-208">After releasing the sequencer source, the application should close and shut down the Media Session by calling [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) and [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), in that order.</span></span>

<span data-ttu-id="59b86-209">Чтобы избежать утечек памяти, приложение должно освободить указатели на Media Foundation интерфейсы, когда они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="59b86-209">To avoid memory leaks, the application must release pointers to Media Foundation interfaces when they are no longer needed.</span></span>

## <a name="next-steps"></a><span data-ttu-id="59b86-210">Next Steps</span><span class="sxs-lookup"><span data-stu-id="59b86-210">Next Steps</span></span>

<span data-ttu-id="59b86-211">В этом пошаговом руководстве показано, как создать базовый список воспроизведения с помощью источника Sequencer.</span><span class="sxs-lookup"><span data-stu-id="59b86-211">This walk-through illustrated how to create a basic playlist by using the sequencer source.</span></span> <span data-ttu-id="59b86-212">После создания списка воспроизведения может потребоваться добавить дополнительные функции, такие как пропуск сегмента, изменение состояния воспроизведения и поиск в сегменте.</span><span class="sxs-lookup"><span data-stu-id="59b86-212">After creating the playlist, you might want to add advanced features such as segment skipping, changing the playback state, and seeking within a segment.</span></span> <span data-ttu-id="59b86-213">В следующем списке приведены ссылки на соответствующие разделы.</span><span class="sxs-lookup"><span data-stu-id="59b86-213">The following list provides links to the related topics:</span></span>

-   <span data-ttu-id="59b86-214">[Управление состояниями представления](how-to-control-presentation-states.md). источник Sequencer использует сеанс мультимедиа для обеспечения управления транспортом, например воспроизведения, паузы и остановки.</span><span class="sxs-lookup"><span data-stu-id="59b86-214">[How to Control Presentation States](how-to-control-presentation-states.md): The sequencer source relies on the Media Session to provide transport control such as, Play, Pause, and Stop.</span></span>
-   <span data-ttu-id="59b86-215">[Выполнение очистки](how-to-perform-scrubbing.md) описывает шаги, необходимые для поиска определенной позицией в потоке.</span><span class="sxs-lookup"><span data-stu-id="59b86-215">[How to Perform Scrubbing](how-to-perform-scrubbing.md) describes the steps required to seek to a specific position in a stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59b86-216">См. также</span><span class="sxs-lookup"><span data-stu-id="59b86-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59b86-217">Источник Sequencer</span><span class="sxs-lookup"><span data-stu-id="59b86-217">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



