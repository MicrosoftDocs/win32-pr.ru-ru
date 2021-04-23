---
description: Использование фильтра Евр DirectShow
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Использование фильтра Евр DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683212"
---
# <a name="using-the-directshow-evr-filter"></a><span data-ttu-id="b6791-103">Использование фильтра Евр DirectShow</span><span class="sxs-lookup"><span data-stu-id="b6791-103">Using the DirectShow EVR Filter</span></span>

<span data-ttu-id="b6791-104">Чтобы создать расширенный фильтр модуля подготовки видео (Евр), вызовите **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b6791-104">To create the enhanced video renderer (EVR) filter, call **CoCreateInstance**.</span></span> <span data-ttu-id="b6791-105">CLSID — это CLSID \_ енханцедвидеорендерер, определенный в UUID. h.</span><span class="sxs-lookup"><span data-stu-id="b6791-105">The CLSID is CLSID\_EnhancedVideoRenderer, defined in uuids.h.</span></span> <span data-ttu-id="b6791-106">Для использования фильтра Евр не нужно вызывать [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) или [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) .</span><span class="sxs-lookup"><span data-stu-id="b6791-106">You do not have to call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) or [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to use the EVR filter.</span></span>

<span data-ttu-id="b6791-107">Дополнительные сведения об использовании фильтра Евр в приложении DirectShow см. [в статье воспроизведение звука и видео в DirectShow](../directshow/audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b6791-107">For more information about using the EVR filter in a DirectShow application, see [Audio/Video Playback in DirectShow](../directshow/audio-video-playback-in-directshow.md).</span></span>

<span data-ttu-id="b6791-108">Фильтр Евр начинается с одного входного ПИН-кода, который соответствует потоку ссылок.</span><span class="sxs-lookup"><span data-stu-id="b6791-108">The EVR filter starts with one input pin, which corresponds to the reference stream.</span></span> <span data-ttu-id="b6791-109">Чтобы добавить контакты для вложенных потоков, запросите фильтр для интерфейса [**иеврфилтерконфиг**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) и вызовите [**Иеврфилтерконфиг:: сетнумберофстреамс**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="b6791-109">To add pins for substreams, query the filter for the [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) interface and call [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="b6791-110">Вызовите этот метод перед подключением входных ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="b6791-110">Call this method before connecting any input pins.</span></span> <span data-ttu-id="b6791-111">ПИН-код 0 всегда является ссылочным потоком.</span><span class="sxs-lookup"><span data-stu-id="b6791-111">Pin 0 is always the reference stream.</span></span> <span data-ttu-id="b6791-112">Подключайте этот ПИН-код перед любыми другими контактами, так как формат ссылочного потока может ограничить доступные форматы подпотока.</span><span class="sxs-lookup"><span data-stu-id="b6791-112">Connect this pin before any other pins, because the format of the reference stream might limit which substream formats are available.</span></span>

<span data-ttu-id="b6791-113">Перед запуском графа задайте окно обрезки видео и прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="b6791-113">Before starting the graph, set the video clipping window and the destination rectangle.</span></span> <span data-ttu-id="b6791-114">Дополнительные сведения см. [в разделе Использование элементов управления отображением видео](using-the-video-display-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b6791-114">For more information, see [Using the Video Display Controls](using-the-video-display-controls.md).</span></span>

<span data-ttu-id="b6791-115">В отличие от микширования видео (VMR), ЕВР не имеет рабочих режимов (оконных, безоконных и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b6791-115">Unlike the Video Mixing Renderer (VMR), the EVR does not have operational modes (windowed, windowless, and so forth).</span></span> <span data-ttu-id="b6791-116">В частности:</span><span class="sxs-lookup"><span data-stu-id="b6791-116">In particular:</span></span>

-   <span data-ttu-id="b6791-117">Евр не поддерживает оконный режим.</span><span class="sxs-lookup"><span data-stu-id="b6791-117">The EVR does not support windowed mode.</span></span> <span data-ttu-id="b6791-118">Приложение должно предоставить окно обрезки.</span><span class="sxs-lookup"><span data-stu-id="b6791-118">The application must provide the clipping window.</span></span>
-   <span data-ttu-id="b6791-119">Евр не имеет режима без отрисовки.</span><span class="sxs-lookup"><span data-stu-id="b6791-119">The EVR does not have a renderless mode.</span></span> <span data-ttu-id="b6791-120">Чтобы заменить выступающий по умолчанию, вызовите [**имфвидеорендерер:: инитиализерендерер**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="b6791-120">To replace the default presenter, call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>
-   <span data-ttu-id="b6791-121">Евр не имеет режима смешения.</span><span class="sxs-lookup"><span data-stu-id="b6791-121">The EVR does not have a mixing mode.</span></span> <span data-ttu-id="b6791-122">Евр всегда создает микшер.</span><span class="sxs-lookup"><span data-stu-id="b6791-122">The EVR always creates the mixer.</span></span> <span data-ttu-id="b6791-123">Если у вас есть один входной поток, нет необходимости вызывать [**сетнумберофстреамс**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) , чтобы заставить Евр использовать микшер.</span><span class="sxs-lookup"><span data-stu-id="b6791-123">If you have one input stream, it is not necessary to call [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) to force the EVR to use the mixer.</span></span>

## <a name="filter-interfaces"></a><span data-ttu-id="b6791-124">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="b6791-124">Filter Interfaces</span></span>

<span data-ttu-id="b6791-125">Фильтр Евр предоставляет следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b6791-125">The EVR filter exposes the following interfaces.</span></span> <span data-ttu-id="b6791-126">Некоторые из этих интерфейсов описаны в пакете SDK для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b6791-126">Some of these interfaces are documented in the DirectShow SDK.</span></span> <span data-ttu-id="b6791-127">Используйте **QueryInterface** для получения указателей на эти интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="b6791-127">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   <span data-ttu-id="b6791-128">[**Иамцертифиедаутпутпротектион**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span></span>
-   <span data-ttu-id="b6791-129">[**Иамфилтермискфлагс**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span></span>
-   <span data-ttu-id="b6791-130">[**Ибасефилтер**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span></span>
-   [<span data-ttu-id="b6791-131">**иеврфилтерконфиг**</span><span class="sxs-lookup"><span data-stu-id="b6791-131">**IEVRFilterConfig**</span></span>](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   <span data-ttu-id="b6791-132">[**Икспропертисет**](../directshow/ikspropertyset.md) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span></span>
-   <span data-ttu-id="b6791-133">[**Имедиаевентсинк**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span></span>
-   [<span data-ttu-id="b6791-134">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="b6791-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="b6791-135">**имфвидеопоситионмаппер**</span><span class="sxs-lookup"><span data-stu-id="b6791-135">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [<span data-ttu-id="b6791-136">**имфвидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="b6791-136">**IMFVideoRenderer**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   <span data-ttu-id="b6791-137">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="b6791-137">**IPersistStream**</span></span>
-   <span data-ttu-id="b6791-138">[**Икуалитиконтрол**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>
-   <span data-ttu-id="b6791-139">[**Икуалпроп**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span></span>
-   <span data-ttu-id="b6791-140">**испеЦифипропертипажес**</span><span class="sxs-lookup"><span data-stu-id="b6791-140">**ISpecifyPropertyPages**</span></span>

## <a name="input-pin-interfaces"></a><span data-ttu-id="b6791-141">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="b6791-141">Input Pin Interfaces</span></span>

<span data-ttu-id="b6791-142">Входные контакты в фильтре Евр предоставляют следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b6791-142">The input pins on the EVR filter expose the following interfaces.</span></span> <span data-ttu-id="b6791-143">Используйте **QueryInterface** для получения указателей на эти интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="b6791-143">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   [<span data-ttu-id="b6791-144">**иеврвидеостреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="b6791-144">**IEVRVideoStreamControl**</span></span>](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   <span data-ttu-id="b6791-145">[**Имеминпутпин**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span></span>
-   [<span data-ttu-id="b6791-146">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="b6791-146">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   <span data-ttu-id="b6791-147">[**Ипин**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span></span>
-   <span data-ttu-id="b6791-148">[**Икуалитиконтрол**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6791-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>

<span data-ttu-id="b6791-149">Кроме того, можно использовать интерфейс [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) для получения следующего интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b6791-149">In addition, you can use the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface to retrieve the following interface:</span></span>

-   [<span data-ttu-id="b6791-150">**идиректксвидеомемориконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="b6791-150">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a><span data-ttu-id="b6791-151">См. также</span><span class="sxs-lookup"><span data-stu-id="b6791-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6791-152">Воспроизведение звука и видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="b6791-152">Audio/Video Playback in DirectShow</span></span>](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="b6791-153">Улучшенный модуль подготовки видео</span><span class="sxs-lookup"><span data-stu-id="b6791-153">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 
