---
description: Диспетчер графа фильтров
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Диспетчер графа фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894142"
---
# <a name="filter-graph-manager"></a><span data-ttu-id="ed9ff-103">Диспетчер графа фильтров</span><span class="sxs-lookup"><span data-stu-id="ed9ff-103">Filter Graph Manager</span></span>

<span data-ttu-id="ed9ff-104">Диспетчер графов фильтров создает и управляет графами фильтра.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-104">The Filter Graph Manager builds and controls filter graphs.</span></span> <span data-ttu-id="ed9ff-105">Этот объект является центральным компонентом DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-105">This object is the central component in DirectShow.</span></span> <span data-ttu-id="ed9ff-106">Приложения используют его для создания и управления графами фильтра.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-106">Applications use it to build and control filter graphs.</span></span> <span data-ttu-id="ed9ff-107">Диспетчер графов фильтров также обрабатывает синхронизацию, уведомление о событиях и другие аспекты управления графом фильтра.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-107">The Filter Graph Manager also handles synchronization, event notification, and other aspects of the controlling the filter graph.</span></span> <span data-ttu-id="ed9ff-108">Создайте этот объект, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-108">Create this object by calling **CoCreateInstance**.</span></span>

### <a name="clsid"></a><span data-ttu-id="ed9ff-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="ed9ff-109">CLSID</span></span>

<span data-ttu-id="ed9ff-110">Существует два идентификатора CLSID для создания диспетчера графа фильтров:</span><span class="sxs-lookup"><span data-stu-id="ed9ff-110">There are two CLSIDs for creating the Filter Graph Manager:</span></span>



| <span data-ttu-id="ed9ff-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="ed9ff-111">CLSID</span></span>                      | <span data-ttu-id="ed9ff-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ed9ff-112">Description</span></span>                                                 |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ed9ff-113">\_ФИЛТЕРГРАФ CLSID</span><span class="sxs-lookup"><span data-stu-id="ed9ff-113">CLSID\_FilterGraph</span></span>         | <span data-ttu-id="ed9ff-114">Создает диспетчер графа фильтров в общем рабочем потоке.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-114">Creates the Filter Graph Manager on a shared worker thread.</span></span> |
| <span data-ttu-id="ed9ff-115">\_ФИЛТЕРГРАФНОСРЕАД CLSID</span><span class="sxs-lookup"><span data-stu-id="ed9ff-115">CLSID\_FilterGraphNoThread</span></span> | <span data-ttu-id="ed9ff-116">Создает диспетчер графа фильтров в потоке приложения.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-116">Creates the Filter Graph Manager on the application thread.</span></span> |



 

<span data-ttu-id="ed9ff-117">Как правило, приложения должны использовать CLSID \_ филтерграф.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-117">Generally, applications should use CLSID\_FilterGraph.</span></span> <span data-ttu-id="ed9ff-118">Оба идентификатора CLSID создают один и тот же объект, но используют различные модели потоков:</span><span class="sxs-lookup"><span data-stu-id="ed9ff-118">Both CLSIDs create the same object, but they use different threading models:</span></span>

-   <span data-ttu-id="ed9ff-119">CLSID \_ филтерграф создает диспетчер графа фильтров в рабочем потоке, который совместно используется всеми \_ экземплярами филтерграф CLSID в рамках одного процесса.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-119">CLSID\_FilterGraph creates the Filter Graph Manager on a worker thread, which is shared by all CLSID\_FilterGraph instances within the same process.</span></span> <span data-ttu-id="ed9ff-120">Поток отправляет сообщения, отправленные фильтрами, и управляет временем существования всех окон, созданных фильтрами.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-120">The thread dispatches messages sent by filters, and controls the lifetime of any windows created by filters.</span></span>
-   <span data-ttu-id="ed9ff-121">\_ФИЛТЕРГРАФНОСРЕАД CLSID создает диспетчер графа фильтров в потоке приложения.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-121">CLSID\_FilterGraphNoThread creates the Filter Graph Manager on the application's thread.</span></span> <span data-ttu-id="ed9ff-122">При использовании этого идентификатора CLSID поток, вызывающий **CoCreateInstance** , должен иметь цикл обработки сообщений, который отправляет сообщения; в противном случае могут возникнуть взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="ed9ff-122">If you use this CLSID, the thread that calls **CoCreateInstance** must have a message loop that dispatches messages; otherwise, deadlocks can occur.</span></span> <span data-ttu-id="ed9ff-123">Кроме того, перед выходом из потока приложения он должен освободить диспетчер графов фильтров и все объекты графа (например, фильтры, ПИН-коды, эталонные часы и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ed9ff-123">Also, before the application thread exits, it must release the Filter Graph Manager and all graph objects (such as filters, pins, reference clocks, and so forth).</span></span>

### <a name="interfaces"></a><span data-ttu-id="ed9ff-124">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="ed9ff-124">Interfaces</span></span>

<span data-ttu-id="ed9ff-125">Диспетчер графов фильтров предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="ed9ff-125">The Filter Graph Manager exposes the following interfaces:</span></span>

-   [<span data-ttu-id="ed9ff-126">**иамграфстреамс**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-126">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [<span data-ttu-id="ed9ff-127">**иамстатс**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-127">**IAMStats**</span></span>](/windows/desktop/api/Control/nn-control-iamstats)
-   [<span data-ttu-id="ed9ff-128">**ибасикаудио**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-128">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [<span data-ttu-id="ed9ff-129">**ибасиквидео**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-129">**IBasicVideo**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [<span data-ttu-id="ed9ff-130">**IBasicVideo2**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-130">**IBasicVideo2**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [<span data-ttu-id="ed9ff-131">**ифилтерчаин**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-131">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [<span data-ttu-id="ed9ff-132">**ифилтерграф**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-132">**IFilterGraph**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [<span data-ttu-id="ed9ff-133">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-133">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [<span data-ttu-id="ed9ff-134">**IFilterGraph3**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-134">**IFilterGraph3**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [<span data-ttu-id="ed9ff-135">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-135">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [<span data-ttu-id="ed9ff-136">**играфбуилдер**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-136">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [<span data-ttu-id="ed9ff-137">**играфконфиг**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-137">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [<span data-ttu-id="ed9ff-138">**играфверсион**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-138">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [<span data-ttu-id="ed9ff-139">**имедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-139">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [<span data-ttu-id="ed9ff-140">**имедиаевент**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-140">**IMediaEvent**</span></span>](/windows/desktop/api/Control/nn-control-imediaevent)
-   [<span data-ttu-id="ed9ff-141">**имедиаевентекс**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-141">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [<span data-ttu-id="ed9ff-142">**имедиаевентсинк**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-142">**IMediaEventSink**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [<span data-ttu-id="ed9ff-143">**имедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-143">**IMediaFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [<span data-ttu-id="ed9ff-144">**имедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-144">**IMediaPosition**</span></span>](/windows/desktop/api/Control/nn-control-imediaposition)
-   [<span data-ttu-id="ed9ff-145">**имедиасикинг**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-145">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [<span data-ttu-id="ed9ff-146">**икуеуекомманд**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-146">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [<span data-ttu-id="ed9ff-147">**ирегистерсервицепровидер**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-147">**IRegisterServiceProvider**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [<span data-ttu-id="ed9ff-148">**Метод IResourceManager**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-148">**IResourceManager**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   <span data-ttu-id="ed9ff-149">**IServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-149">**IServiceProvider**</span></span>
-   [<span data-ttu-id="ed9ff-150">**ивидеофраместеп**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-150">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [<span data-ttu-id="ed9ff-151">**ивидеовиндов**</span><span class="sxs-lookup"><span data-stu-id="ed9ff-151">**IVideoWindow**</span></span>](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a><span data-ttu-id="ed9ff-152">См. также</span><span class="sxs-lookup"><span data-stu-id="ed9ff-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed9ff-153">Объекты DirectShow</span><span class="sxs-lookup"><span data-stu-id="ed9ff-153">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



