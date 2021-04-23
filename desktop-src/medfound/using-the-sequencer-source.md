---
description: В этом разделе описывается использование источника Sequencer.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Использование источника Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711387"
---
# <a name="using-the-sequencer-source"></a><span data-ttu-id="805fb-103">Использование источника Sequencer</span><span class="sxs-lookup"><span data-stu-id="805fb-103">Using the Sequencer Source</span></span>

<span data-ttu-id="805fb-104">В этом разделе описывается использование [источника Sequencer](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="805fb-104">This topic describes how to use the [Sequencer Source](sequencer-source.md).</span></span> <span data-ttu-id="805fb-105">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="805fb-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="805fb-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="805fb-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="805fb-107">Добавление топологий</span><span class="sxs-lookup"><span data-stu-id="805fb-107">Adding Topologies</span></span>](#adding-topologies)
-   [<span data-ttu-id="805fb-108">Удаление топологий</span><span class="sxs-lookup"><span data-stu-id="805fb-108">Deleting Topologies</span></span>](#deleting-topologies)
-   [<span data-ttu-id="805fb-109">Пропуск в сегмент</span><span class="sxs-lookup"><span data-stu-id="805fb-109">Skipping to a Segment</span></span>](#skipping-to-a-segment)
-   [<span data-ttu-id="805fb-110">См. также</span><span class="sxs-lookup"><span data-stu-id="805fb-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="805fb-111">Общие сведения о источнике Sequencer см. в разделе [сведения о источнике Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="805fb-111">For a general overview of the sequencer source, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

## <a name="overview"></a><span data-ttu-id="805fb-112">Обзор</span><span class="sxs-lookup"><span data-stu-id="805fb-112">Overview</span></span>

<span data-ttu-id="805fb-113">Источник Sequencer предоставляет следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="805fb-113">The sequencer source exposes the following interfaces.</span></span>



| <span data-ttu-id="805fb-114">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="805fb-114">Interface</span></span>                                                                        | <span data-ttu-id="805fb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="805fb-115">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="805fb-116">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="805fb-116">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | <span data-ttu-id="805fb-117">Предоставляет универсальную функциональность источника носителя.</span><span class="sxs-lookup"><span data-stu-id="805fb-117">Exposes generic media source functionality.</span></span>                                        |
| [<span data-ttu-id="805fb-118">**имфсекуенцерсаурце**</span><span class="sxs-lookup"><span data-stu-id="805fb-118">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | <span data-ttu-id="805fb-119">Позволяет приложению добавлять или удалять топологии.</span><span class="sxs-lookup"><span data-stu-id="805fb-119">Enables the application to add or remove topologies.</span></span>                               |
| [<span data-ttu-id="805fb-120">**имфмедиасаурцетопологипровидер**</span><span class="sxs-lookup"><span data-stu-id="805fb-120">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | <span data-ttu-id="805fb-121">Извлекает следующую топологию в очередь в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="805fb-121">Retrieves the next topology to queue on the Media Session.</span></span>                         |
| [<span data-ttu-id="805fb-122">**имфмедиасаурцепресентатионпровидер**</span><span class="sxs-lookup"><span data-stu-id="805fb-122">**IMFMediaSourcePresentationProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | <span data-ttu-id="805fb-123">Используется сеансом мультимедиа для конечных сегментов.</span><span class="sxs-lookup"><span data-stu-id="805fb-123">Used by the Media Session to end segments.</span></span> <span data-ttu-id="805fb-124">Приложения не используют этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="805fb-124">Applications do not use this interface.</span></span> |
| [<span data-ttu-id="805fb-125">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="805fb-125">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | <span data-ttu-id="805fb-126">Запрашивает источник Sequencer для [интерфейсов служб](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="805fb-126">Queries the sequencer source for [Service Interfaces](service-interfaces.md).</span></span>     |



 

<span data-ttu-id="805fb-127">Чтобы воспроизвести последовательность источников мультимедиа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="805fb-127">To play a sequence of media sources, perform the following steps:</span></span>

1.  <span data-ttu-id="805fb-128">Чтобы создать источник Sequencer, вызовите функцию [**мфкреатесекуенцерсаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) .</span><span class="sxs-lookup"><span data-stu-id="805fb-128">To create the sequencer source, call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function.</span></span>
2.  <span data-ttu-id="805fb-129">Для каждого сегмента Создайте топологию воспроизведения, как описано в разделе [Создание топологий воспроизведения](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="805fb-129">For each segment, create a playback topology, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span> <span data-ttu-id="805fb-130">Чтобы добавить топологию в презентацию, вызовите метод [**имфсекуенцерсаурце:: аппендтопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="805fb-130">To add the topology to the presentation, call [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span>
3.  <span data-ttu-id="805fb-131">Перед началом воспроизведения вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) в источнике Sequencer.</span><span class="sxs-lookup"><span data-stu-id="805fb-131">Before starting playback, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the sequencer source.</span></span> <span data-ttu-id="805fb-132">Этот метод возвращает указатель на дескриптор представления для первого сегмента.</span><span class="sxs-lookup"><span data-stu-id="805fb-132">This method returns a pointer to a presentation descriptor for the first segment.</span></span> <span data-ttu-id="805fb-133">Чтобы получить топологию, связанную с этим сегментом, вызовите **QueryInterface** в источнике Sequencer для интерфейса [**имфмедиасаурцетопологипровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) .</span><span class="sxs-lookup"><span data-stu-id="805fb-133">To get the topology associated with this segment, call **QueryInterface** on the sequencer source for the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface.</span></span> <span data-ttu-id="805fb-134">Передайте дескриптор презентации в метод [**имфмедиасаурцетопологипровидер:: жетмедиасаурцетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="805fb-134">Pass the presentation descriptor to the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="805fb-135">Этот метод возвращает указатель на топологию.</span><span class="sxs-lookup"><span data-stu-id="805fb-135">This method returns a pointer to the topology.</span></span>
4.  <span data-ttu-id="805fb-136">Передайте топологию первого сегмента в сеанс мультимедиа, вызвав метод [**имфмедиасессион:: Сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="805fb-136">Pass the topology for the first segment to the Media Session, by calling the Media Session's [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>
5.  <span data-ttu-id="805fb-137">Запустите воспроизведение, вызвав [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="805fb-137">Start playback by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>
6.  <span data-ttu-id="805fb-138">Когда источник Sequencer готов к выполнению в следующем сегменте, он отправляет событие [меневпресентатион](menewpresentation.md) , данные события которого являются указателем интерфейса [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="805fb-138">When the sequencer source is ready to preroll the next segment, it sends an [MENewPresentation](menewpresentation.md) event whose event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface pointer.</span></span> <span data-ttu-id="805fb-139">Опять же, получите топологию для сегмента, вызвав [**жетмедиасаурцетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) в источнике Sequencer и задав топологию в сеансе мультимедиа, вызвав [**сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="805fb-139">Again, get the topology for the segment by calling [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the sequencer source, and set the topology on the Media Session by calling [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="805fb-140">Нет необходимости повторно запускать источник мультимедиа; Он будет автоматически воспроизводиться до следующего сегмента.</span><span class="sxs-lookup"><span data-stu-id="805fb-140">It is not necessary to re-start the media source; it will automatically play through to the next segment.</span></span>
7.  <span data-ttu-id="805fb-141">Перед завершением работы приложения завершите работу источника Sequencer, вызвав [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="805fb-141">Before the application quits, shut down the sequencer source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>

<span data-ttu-id="805fb-142">В следующем коде показано, как получить топологию и задать ее в сеансе мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="805fb-142">The following code shows how to get the topology and set it on the Media Session:</span></span>


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



<span data-ttu-id="805fb-143">Полный пример кода см. в разделе [Пример исходного кода программы Sequencer](sequencer-source-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="805fb-143">For a complete code example, see [Sequencer Source Example Code](sequencer-source-example-code.md).</span></span>

## <a name="adding-topologies"></a><span data-ttu-id="805fb-144">Добавление топологий</span><span class="sxs-lookup"><span data-stu-id="805fb-144">Adding Topologies</span></span>

<span data-ttu-id="805fb-145">Источник Sequencer содержит два списка топологий: *входной список* и предэлементный *Список*.</span><span class="sxs-lookup"><span data-stu-id="805fb-145">The sequencer source maintains two lists of topologies: the *input list* and the *preroll list*.</span></span>

<span data-ttu-id="805fb-146">Входной список представляет собой коллекцию топологий, соответствующих сегментам списка воспроизведения в том порядке, в котором они были добавлены приложением путем вызова [**имфсекуенцерсаурце:: аппендтопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="805fb-146">The input list is a collection of topologies corresponding to playlist segments, in the order that they were added by the application by calling [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span> <span data-ttu-id="805fb-147">Этот метод назначает каждой топологии уникальный *Идентификатор сегмента* типа **мфсекуенцерелементид**.</span><span class="sxs-lookup"><span data-stu-id="805fb-147">This method assigns each topology a unique *segment identifier* of the type **MFSequencerElementId**.</span></span> <span data-ttu-id="805fb-148">Идентификатор сегмента задается как атрибут для всех узлов топологии источника.</span><span class="sxs-lookup"><span data-stu-id="805fb-148">The segment identifier is set as an attribute for all source topology nodes.</span></span> <span data-ttu-id="805fb-149">Приложение может получить идентификатор сегмента из исходного узла с помощью атрибута [ \_ \_ \_ ELEMENTID топоноде Sequence](mf-toponode-sequence-elementid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="805fb-149">An application can get the segment identifier from a source node by using the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute.</span></span> <span data-ttu-id="805fb-150">Входной список может иметь дублирующиеся топологии, если приложение с именем **аппендтопологи** в одной топологии несколько раз; Однако они идентифицируются по уникальным идентификаторам сегментов.</span><span class="sxs-lookup"><span data-stu-id="805fb-150">The input list can have duplicate topologies if the application called **AppendTopology** on the same topology more than once; however, they are identified by their unique segment identifiers.</span></span>

<span data-ttu-id="805fb-151">Предустановленный список представляет собой коллекцию топологий списка входных данных, которые были инициализированы при подготовке к воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="805fb-151">The preroll list is a collection of input list topologies that have been initialized in preparation for playback.</span></span> <span data-ttu-id="805fb-152">Это позволяет сеансу мультимедиа переходить к следующей топологии без проблем, когда завершается активная топология.</span><span class="sxs-lookup"><span data-stu-id="805fb-152">This enables the Media Session to transition to the next topology seamlessly when the active topology ends.</span></span> <span data-ttu-id="805fb-153">Приложение не может напрямую добавлять или удалять топологии из списка предустановки; Он создается источником Sequencer, если топология из входного списка выбрана для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="805fb-153">The application cannot directly add or remove topologies from the preroll list; it is generated by the sequencer source when a topology from the input list is selected for playback.</span></span> <span data-ttu-id="805fb-154">В результате источник Sequencer добавляет следующую топологию из входного списка в список предустановки.</span><span class="sxs-lookup"><span data-stu-id="805fb-154">This causes the sequencer source to add the next topology from the input list to the preroll list.</span></span> <span data-ttu-id="805fb-155">После этого источник Sequencer асинхронно вызывает событие [меневпресентатион](menewpresentation.md) и передает дескриптор представления для предподготовки топологии в виде данных о событии.</span><span class="sxs-lookup"><span data-stu-id="805fb-155">After doing so, the sequencer source asynchronously raises the [MENewPresentation](menewpresentation.md) event and passes the presentation descriptor for the preroll topology as event data.</span></span> <span data-ttu-id="805fb-156">Приложение должно прослушивать это событие с помощью интерфейса [**Имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) сеанса мультимедиа и поставить в очередь предпробную топологию в сеансе мультимедиа путем вызова [**Имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="805fb-156">The application must listen for this event by using the Media Session's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface and queue the preroll topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="805fb-157">Это необходимо сделать до того, как сеанс мультимедиа завершит воспроизведение активной топологии.</span><span class="sxs-lookup"><span data-stu-id="805fb-157">This must be done before the Media Session completes playback of the active topology.</span></span> <span data-ttu-id="805fb-158">**Сеттопологи** информирует сеанс мультимедиа о следующей топологии, которую необходимо воспроизвести после завершения воспроизведения активной топологии.</span><span class="sxs-lookup"><span data-stu-id="805fb-158">**SetTopology** informs the Media Session about the next topology that it must play after playback of the active topology has ended.</span></span> <span data-ttu-id="805fb-159">Чтобы обеспечить бесперебойную треанситион, приложение должно вызвать **сеттопологи** до того, как сеанс мультимедиа завершится воспроизведением предыдущей топологии.</span><span class="sxs-lookup"><span data-stu-id="805fb-159">To ensure a seamless treansition, the application must call **SetTopology** before the Media Session completes playing the previous topology.</span></span> <span data-ttu-id="805fb-160">В противном случае между сегментами будет разрыв.</span><span class="sxs-lookup"><span data-stu-id="805fb-160">Otherwise, there will be a gap between the segments.</span></span>

<span data-ttu-id="805fb-161">Событие [меневпресентатион](menewpresentation.md) возникает при условии, что после активной топологии имеется топология.</span><span class="sxs-lookup"><span data-stu-id="805fb-161">The [MENewPresentation](menewpresentation.md) event is raised as long as there is a topology following the active topology.</span></span> <span data-ttu-id="805fb-162">Следовательно, если входной список содержит только одну топологию или если активная топология является последней в входном списке, это событие не возникает.</span><span class="sxs-lookup"><span data-stu-id="805fb-162">Consequently, if the input list contains only one topology, or if the active topology is the last one in the input list, this event is not raised.</span></span>

<span data-ttu-id="805fb-163">Список предустановленных данных синхронизируется со списком ввода и обновляется каждый раз при добавлении или удалении топологии из входного списка.</span><span class="sxs-lookup"><span data-stu-id="805fb-163">The preroll list is synchronized with the input list and is refreshed each time a topology is added to or deleted from the input list.</span></span>

## <a name="deleting-topologies"></a><span data-ttu-id="805fb-164">Удаление топологий</span><span class="sxs-lookup"><span data-stu-id="805fb-164">Deleting Topologies</span></span>

<span data-ttu-id="805fb-165">Чтобы удалить топологию из источника Sequencer, приложение должно вызвать метод [**имфсекуенцерсаурце::D елететопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) и указать идентификатор сегмента.</span><span class="sxs-lookup"><span data-stu-id="805fb-165">To remove a topology from the sequencer source, an application must call the [**IMFSequencerSource::DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) method and specify the segment identifier.</span></span>

<span data-ttu-id="805fb-166">Перед вызовом [**делететопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology)приложение должно убедиться, что сеанс мультимедиа не использует топологию, которую приложение хочет удалить.</span><span class="sxs-lookup"><span data-stu-id="805fb-166">Before calling [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), the application must make sure that Media Session is not using the topology that the application wants to delete.</span></span> <span data-ttu-id="805fb-167">Для этого необходимо выполнить оба следующих действия, прежде чем приложение вызовет **делететопологи**:</span><span class="sxs-lookup"><span data-stu-id="805fb-167">To do this, both of the following must occur before the application calls **DeleteTopology**:</span></span>

-   <span data-ttu-id="805fb-168">Получено событие [месессионтопологистатус](mesessiontopologystatus.md) с MF \_ топостатус \_ Completed для топологии, чтобы убедиться, что сеанс мультимедиа завершил воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="805fb-168">[MESessionTopologyStatus](mesessiontopologystatus.md) event with MF\_TOPOSTATUS\_ENDED is received for the topology to ensure that Media Session has completed playback.</span></span>

-   <span data-ttu-id="805fb-169">[Месессионтопологистатус](mesessiontopologystatus.md) with MF \_ топостатус \_ Started \_ Source получен для следующей топологии, чтобы убедиться, что сеанс мультимедиа начал играть в следующую топологию, получено событие [Месессионендед](mesessionended.md) , чтобы убедиться, что сеанс мультимедиа выполняется с последней топологией в источнике Sequencer.</span><span class="sxs-lookup"><span data-stu-id="805fb-169">[MESessionTopologyStatus](mesessiontopologystatus.md) with MF\_TOPOSTATUS\_STARTED\_SOURCE is received for the next topology to ensure that the Media Session has started playing the next topology, [MESessionEnded](mesessionended.md) event is received to ensure that Media Session is done with the last topology in the sequencer source.</span></span>

<span data-ttu-id="805fb-170">Если удаляемый сегмент является активной топологией, воспроизведение останавливается и источник Sequencer вызывает событие [миндофпресентатионсегмент](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="805fb-170">If the segment being deleted is the active topology, playback is stopped and the sequencer source raises the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span> <span data-ttu-id="805fb-171">Если активная топология также является последней топологией, возникает событие [миндофпресентатион](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="805fb-171">If the active topology is also the last topology, the [MEEndOfPresentation](meendofpresentation.md) event is raised.</span></span>

## <a name="skipping-to-a-segment"></a><span data-ttu-id="805fb-172">Пропуск в сегмент</span><span class="sxs-lookup"><span data-stu-id="805fb-172">Skipping to a Segment</span></span>

<span data-ttu-id="805fb-173">Приложение может перейти к определенному сегменту в последовательности, запустив [сеанс мультимедиа](media-session.md) со смещением сегмента, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="805fb-173">An application can skip to a particular segment in the sequence by starting the [Media Session](media-session.md) with a segment offset, as follows:</span></span>

1.  <span data-ttu-id="805fb-174">Вызовите функцию [**мфкреатесекуенцерсегментоффсет**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) , чтобы создать смещение сегмента.</span><span class="sxs-lookup"><span data-stu-id="805fb-174">Call the [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) function to create the segment offset.</span></span> <span data-ttu-id="805fb-175">Укажите идентификатор сегмента в параметре *ДВИД* .</span><span class="sxs-lookup"><span data-stu-id="805fb-175">Specify the identifier of the segment in the *dwId* parameter.</span></span> <span data-ttu-id="805fb-176">(Идентификатор был возвращен методом [**имфсекуенцерсаурце:: аппендтопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) при первом добавлении топологии в источник Sequencer.) Параметр *хнсоффсет* задает смещение времени относительно начала сегмента.</span><span class="sxs-lookup"><span data-stu-id="805fb-176">(The identifier was returned by the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method when you first added the topology to the sequencer source.) The *hnsOffset* parameter specifies a time offset, relative to the start of the segment.</span></span> <span data-ttu-id="805fb-177">В это время начнется воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="805fb-177">Playback will start at this time.</span></span> <span data-ttu-id="805fb-178">Для параметра *пварсегментоффсет* передайте адрес пустого **пропвариант**.</span><span class="sxs-lookup"><span data-stu-id="805fb-178">For the *pvarSegmentOffset* parameter, pass in the address of an empty **PROPVARIANT**.</span></span> <span data-ttu-id="805fb-179">При возврате функции этот **пропвариант** содержит смещение сегмента.</span><span class="sxs-lookup"><span data-stu-id="805fb-179">When the function returns, this **PROPVARIANT** contains the segment offset.</span></span>

2.  <span data-ttu-id="805fb-180">Вызовите метод [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="805fb-180">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method on the Media Session.</span></span> <span data-ttu-id="805fb-181">В качестве значения параметра *пгуидтимеформат* используйте значение идентификатора GUID \_ \_ смещение сегмента формата времени MF \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="805fb-181">For the *pguidTimeFormat* parameter, use the GUID value MF\_TIME\_FORMAT\_SEGMENT\_OFFSET.</span></span> <span data-ttu-id="805fb-182">Это значение указывает на поиск по смещению сегмента.</span><span class="sxs-lookup"><span data-stu-id="805fb-182">This value indicates seeking by segment offset.</span></span> <span data-ttu-id="805fb-183">Для параметра *пварстартпоситион* передайте адрес **пропвариант** , созданный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="805fb-183">For the *pvarStartPosition* parameter, pass the address of the **PROPVARIANT** created in the previous step.</span></span>

<span data-ttu-id="805fb-184">В следующем примере кода показано, как перейти к началу указанного сегмента в последовательности.</span><span class="sxs-lookup"><span data-stu-id="805fb-184">The following code example shows how to skip to the start of a specified segment in a sequence.</span></span>


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="805fb-185">Когда приложение выполняет поиск по сегментам, приложение получает несколько событий, так как источник Sequencer завершает текущий сегмент и готовится к воспроизведению нового сегмента.</span><span class="sxs-lookup"><span data-stu-id="805fb-185">When the application seeks across segments, the application receives several events as the sequencer source ends the current segment and prepares to play the new segment.</span></span> <span data-ttu-id="805fb-186">Поскольку эти события получаются асинхронно, трудно спрогнозировать точную последовательность событий.</span><span class="sxs-lookup"><span data-stu-id="805fb-186">Because these events are received asynchronously, it is difficult to predict the exact sequence of events.</span></span> <span data-ttu-id="805fb-187">Ниже приведены эти события.</span><span class="sxs-lookup"><span data-stu-id="805fb-187">These events are as follows:</span></span>

-   <span data-ttu-id="805fb-188">Источник Sequencer отправляет событие [меневпресентатион](menewpresentation.md) для нового сегмента, в который пропускается сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="805fb-188">The sequencer source sends an [MENewPresentation](menewpresentation.md) event for the new segment to which the Media Session is skipping.</span></span>

-   <span data-ttu-id="805fb-189">Когда источник Sequencer завершает активный сегмент, он отправляет событие [миндофпресентатионсегмент](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="805fb-189">When the sequencer source ends the active segment, it sends the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span>
-   <span data-ttu-id="805fb-190">Затем источник Sequencer отменяет предпробную топологию.</span><span class="sxs-lookup"><span data-stu-id="805fb-190">The sequencer source then cancels the preroll topology.</span></span> <span data-ttu-id="805fb-191">Это приводит к следующим событиям для отмененной топологии:</span><span class="sxs-lookup"><span data-stu-id="805fb-191">This results in the following events for the canceled topology:</span></span>

    -   <span data-ttu-id="805fb-192">Событие [месессионтопологистатус](mesessiontopologystatus.md) с \_ флагом "MF топостатус Ready" \_ .</span><span class="sxs-lookup"><span data-stu-id="805fb-192">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span>
    -   <span data-ttu-id="805fb-193">Событие [месессионтопологистатус](mesessiontopologystatus.md) с \_ \_ флагом источника MF топостатус Started \_ .</span><span class="sxs-lookup"><span data-stu-id="805fb-193">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_STARTED\_SOURCE flag.</span></span>
    -   <span data-ttu-id="805fb-194">Событие [миндофпресентатионсегмент](meendofpresentationsegment.md) с атрибутом " [ \_ \_ топология источника события MF \_ \_ отменено](mf-event-source-topology-canceled-attribute.md) ", чтобы указать, что топология была отменена источником Sequencer.</span><span class="sxs-lookup"><span data-stu-id="805fb-194">[MEEndOfPresentationSegment](meendofpresentationsegment.md) event with the [MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED](mf-event-source-topology-canceled-attribute.md) attribute to indicate that the topology was canceled by the sequencer source.</span></span>

-   <span data-ttu-id="805fb-195">Затем источник Sequencer отправляет события для нового сегмента, включая различные события [месессионтопологистатус](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="805fb-195">Next, the sequencer source sends events for the new segment, including various [MESessionTopologyStatus](mesessiontopologystatus.md) events.</span></span>
-   <span data-ttu-id="805fb-196">Если новый сегмент не является последним в списке, источник Sequencer обновляет предустановленный список и создает еще одну [меневпресентатион](menewpresentation.md) для новой предрулонной топологии.</span><span class="sxs-lookup"><span data-stu-id="805fb-196">If the new segment is not the last on the list, the sequencer source refreshes the preroll list and raises another [MENewPresentation](menewpresentation.md) for the new preroll topology.</span></span> <span data-ttu-id="805fb-197">Сведения о топологиях в предустановочном списке см. в разделе [сведения о источнике Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="805fb-197">For information about topologies in the preroll list, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="805fb-198">Дополнительные сведения о событиях, отправленных источником Sequencer, можно найти в разделе [события источника Sequencer](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="805fb-198">More details about the events sent by the sequencer source can be found in the topic [Sequencer Source Events](sequencer-source-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="805fb-199">См. также</span><span class="sxs-lookup"><span data-stu-id="805fb-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="805fb-200">Создание списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="805fb-200">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="805fb-201">Источник Sequencer</span><span class="sxs-lookup"><span data-stu-id="805fb-201">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



