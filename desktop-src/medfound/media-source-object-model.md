---
description: Объектная модель источника мультимедиа
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Объектная модель источника мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351532"
---
# <a name="media-source-object-model"></a><span data-ttu-id="555a4-103">Объектная модель источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="555a4-103">Media Source Object Model</span></span>

<span data-ttu-id="555a4-104">В этом разделе описывается объектная модель для источников мультимедиа в Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="555a4-104">This topic describes the object model for media sources in Microsoft Media Foundation.</span></span> <span data-ttu-id="555a4-105">Источник мультимедиа должен реализовывать два объекта:</span><span class="sxs-lookup"><span data-stu-id="555a4-105">A media source must implement two objects:</span></span>

-   <span data-ttu-id="555a4-106">Дескриптор представления, описывающий содержимое источника, включая количество потоков и формат каждого потока.</span><span class="sxs-lookup"><span data-stu-id="555a4-106">A presentation descriptor, which describes the contents of the source, including the number of streams and the format of each stream.</span></span> <span data-ttu-id="555a4-107">Дополнительные сведения о дескрипторах презентаций см. в разделе [дескрипторы представления](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="555a4-107">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>
-   <span data-ttu-id="555a4-108">Один или несколько потоков мультимедиа, которые создают исходные данные.</span><span class="sxs-lookup"><span data-stu-id="555a4-108">One or more media streams, which generate the source data.</span></span>

<span data-ttu-id="555a4-109">Источник не создает потоки до начала воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="555a4-109">The source does not create the streams until playback starts.</span></span>

## <a name="media-source-interfaces"></a><span data-ttu-id="555a4-110">Интерфейсы источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="555a4-110">Media Source Interfaces</span></span>

<span data-ttu-id="555a4-111">Источник мультимедиа должен предоставлять следующие интерфейсы через **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="555a4-111">A media source must expose the following interfaces through **QueryInterface**.</span></span>



| <span data-ttu-id="555a4-112">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="555a4-112">Interface</span></span>                                                | <span data-ttu-id="555a4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="555a4-113">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="555a4-114">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="555a4-114">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | <span data-ttu-id="555a4-115">Требуется для всех источников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="555a4-115">Required for all media sources.</span></span>                                                                                 |
| [<span data-ttu-id="555a4-116">**имфмедиаевентженератор**</span><span class="sxs-lookup"><span data-stu-id="555a4-116">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="555a4-117">Требуется для всех источников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="555a4-117">Required for all media sources.</span></span> <span data-ttu-id="555a4-118">Интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) наследует этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="555a4-118">The [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface inherits this interface.</span></span> |



 

<span data-ttu-id="555a4-119">При необходимости источник мультимедиа может реализовать интерфейс [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) и реализовать любой из следующих интерфейсов в качестве служб:</span><span class="sxs-lookup"><span data-stu-id="555a4-119">Optionally, a media source can implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface and implement any of the following interfaces as services:</span></span>



| <span data-ttu-id="555a4-120">Интерфейс службы</span><span class="sxs-lookup"><span data-stu-id="555a4-120">Service interface</span></span>                                  | <span data-ttu-id="555a4-121">Описание</span><span class="sxs-lookup"><span data-stu-id="555a4-121">Description</span></span>                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="555a4-122">**имфратеконтрол**</span><span class="sxs-lookup"><span data-stu-id="555a4-122">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | <span data-ttu-id="555a4-123">Управляет скоростью воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="555a4-123">Controls the playback rate.</span></span>                                       |
| [<span data-ttu-id="555a4-124">**имфратесуппорт**</span><span class="sxs-lookup"><span data-stu-id="555a4-124">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | <span data-ttu-id="555a4-125">Сообщает поддерживаемый диапазон поддерживаемых частот воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="555a4-125">Reports the range of playback rates that are supported.</span></span>           |
| [<span data-ttu-id="555a4-126">**имфкуалитядвисе**</span><span class="sxs-lookup"><span data-stu-id="555a4-126">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | <span data-ttu-id="555a4-127">Позволяет менеджеру по качеству настраивать качество звука или видео.</span><span class="sxs-lookup"><span data-stu-id="555a4-127">Enables the quality manager to adjust the audio or video quality.</span></span> |
| [<span data-ttu-id="555a4-128">**имфметадатапровидер**</span><span class="sxs-lookup"><span data-stu-id="555a4-128">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | <span data-ttu-id="555a4-129">Предоставляет метаданные.</span><span class="sxs-lookup"><span data-stu-id="555a4-129">Provides metadata.</span></span>                                                |



 

<span data-ttu-id="555a4-130">Если источник мультимедиа может воспроизводиться по тарифам, отличным от обычной скорости (1,0), он должен предоставлять службу контроля скорости ([**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) и [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span><span class="sxs-lookup"><span data-stu-id="555a4-130">If the media source can play at rates other than normal speed (1.0), it should expose the rate control service ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) and [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span></span> <span data-ttu-id="555a4-131">В противном случае предполагается, что источник поддерживает только воспроизведение с нормальной скоростью.</span><span class="sxs-lookup"><span data-stu-id="555a4-131">Otherwise, it is assumed that the source only supports playback at normal speed.</span></span> <span data-ttu-id="555a4-132">Дополнительные сведения см. в разделе [Реализация управления скоростью](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="555a4-132">For more information, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="555a4-133">Дополнительные сведения об интерфейсах служб и [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)см. в разделе [интерфейсы служб](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="555a4-133">For more information about service interfaces and [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), see [Service Interfaces](service-interfaces.md).</span></span>

## <a name="media-stream-interfaces"></a><span data-ttu-id="555a4-134">Интерфейсы потока мультимедиа</span><span class="sxs-lookup"><span data-stu-id="555a4-134">Media Stream Interfaces</span></span>

<span data-ttu-id="555a4-135">Потоки мультимедиа должны реализовывать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="555a4-135">Media streams must implement the following interfaces.</span></span>



| <span data-ttu-id="555a4-136">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="555a4-136">Interface</span></span>                                                | <span data-ttu-id="555a4-137">Описание</span><span class="sxs-lookup"><span data-stu-id="555a4-137">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="555a4-138">**имфмедиастреам**</span><span class="sxs-lookup"><span data-stu-id="555a4-138">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | <span data-ttu-id="555a4-139">Требуется для всех потоков мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="555a4-139">Required for all media streams.</span></span>                                                                                 |
| [<span data-ttu-id="555a4-140">**имфмедиаевентженератор**</span><span class="sxs-lookup"><span data-stu-id="555a4-140">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="555a4-141">Требуется для всех потоков мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="555a4-141">Required for all media streams.</span></span> <span data-ttu-id="555a4-142">Интерфейс [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) наследует этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="555a4-142">The [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface inherits this interface.</span></span> |



 

<span data-ttu-id="555a4-143">В настоящее время для потоков мультимедиа не определены интерфейсы служб.</span><span class="sxs-lookup"><span data-stu-id="555a4-143">Currently no service interfaces are defined for media streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="555a4-144">См. также</span><span class="sxs-lookup"><span data-stu-id="555a4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="555a4-145">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="555a4-145">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



