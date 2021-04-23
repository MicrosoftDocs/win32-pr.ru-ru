---
description: Объект потоковой передачи мультимедиа и иерархия интерфейсов
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Объект потоковой передачи мультимедиа и иерархия интерфейсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914228"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a><span data-ttu-id="63768-103">Объект потоковой передачи мультимедиа и иерархия интерфейсов</span><span class="sxs-lookup"><span data-stu-id="63768-103">Multimedia Streaming Object and Interface Hierarchy</span></span>

> [!Note]  
> <span data-ttu-id="63768-104">Эти API-интерфейсы являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="63768-104">These APIs are deprecated.</span></span> <span data-ttu-id="63768-105">Приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="63768-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="63768-106">На следующей диаграмме показана иерархия объектов, используемая в потоковой передаче мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="63768-106">The following diagram shows the object hierarchy used in multimedia streaming.</span></span>

![Иерархия объектов мултимедиастреаминг](images/mmstream02.png)

<span data-ttu-id="63768-108">Архитектура потоковой передачи мультимедиа определяет три общих типа объектов:</span><span class="sxs-lookup"><span data-stu-id="63768-108">The multimedia streaming architecture defines three general type of object:</span></span>

-   <span data-ttu-id="63768-109">Объект **аммултимедиастреам** предоставляет интерфейс [**иаммултимедиастреам**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) .</span><span class="sxs-lookup"><span data-stu-id="63768-109">The **AMMultimediaStream** object exposes the [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) interface.</span></span> <span data-ttu-id="63768-110">На внутреннем уровне этот объект служит оболочкой для графа фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="63768-110">Internally, this object wraps the DirectShow filter graph.</span></span>
-   <span data-ttu-id="63768-111">Объекты *потока мультимедиа* предоставляют интерфейс [**имедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) и являются специфичными для данных.</span><span class="sxs-lookup"><span data-stu-id="63768-111">*Media stream* objects expose the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and are data specific.</span></span> <span data-ttu-id="63768-112">Объект Аммултимедиастреам содержит один или несколько потоков мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="63768-112">The AMMultimediaStream object contains one or more media streams.</span></span>
-   <span data-ttu-id="63768-113">*Образцы объектов Stream* содержат данные для определенного потока.</span><span class="sxs-lookup"><span data-stu-id="63768-113">*Stream sample* objects contain the data for a particular stream.</span></span>

<span data-ttu-id="63768-114">Поддерживаются следующие объекты потока мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="63768-114">The following media stream objects are supported:</span></span>

-   <span data-ttu-id="63768-115">Аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="63768-115">Audio stream.</span></span> <span data-ttu-id="63768-116">Предоставляет интерфейс [**иаудиомедиастреам**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .</span><span class="sxs-lookup"><span data-stu-id="63768-116">Exposes the [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) interface.</span></span>
-   <span data-ttu-id="63768-117">Поток DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="63768-117">DirectDraw stream.</span></span> <span data-ttu-id="63768-118">Представляет поток видео, отображаемый на поверхности DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="63768-118">Represents a video stream that is rendered to a DirectDraw surface.</span></span> <span data-ttu-id="63768-119">Предоставляет интерфейс [**идиректдравмедиастреам**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .</span><span class="sxs-lookup"><span data-stu-id="63768-119">Exposes the [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) interface.</span></span>
-   <span data-ttu-id="63768-120">Поток типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="63768-120">Media type stream.</span></span> <span data-ttu-id="63768-121">Представляет произвольные данные.</span><span class="sxs-lookup"><span data-stu-id="63768-121">Represents arbitrary data.</span></span> <span data-ttu-id="63768-122">Предоставляет интерфейс [**иаммедиатипестреам**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .</span><span class="sxs-lookup"><span data-stu-id="63768-122">Exposes the [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) interface.</span></span>

<span data-ttu-id="63768-123">Каждый объект потока мультимедиа создает свой собственный образец объекта Stream:</span><span class="sxs-lookup"><span data-stu-id="63768-123">Each media stream object creates its own kind of stream sample object:</span></span>

-   <span data-ttu-id="63768-124">Звуковые потоки создают образцы звука, которые предоставляют интерфейс [**иаудиостреамсампле**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="63768-124">Audio streams create audio samples, which expose the [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) interface.</span></span>
-   <span data-ttu-id="63768-125">В потоках DirectDraw создаются примеры DirectDraw, которые предоставляют интерфейс [**идиректдравстреамсампле**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="63768-125">DirectDraw streams create DirectDraw samples, which expose the [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) interface.</span></span>
-   <span data-ttu-id="63768-126">Потоки типа мультимедиа создают образцы типов носителей, которые предоставляют интерфейс [**иаммедиатипесампле**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .</span><span class="sxs-lookup"><span data-stu-id="63768-126">Media type streams create media type samples, which expose the [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) interface.</span></span>

<span data-ttu-id="63768-127">На следующей диаграмме показана иерархия интерфейсов для интерфейсов, перечисленных ранее.</span><span class="sxs-lookup"><span data-stu-id="63768-127">The following diagram shows the interface hierarchy for the interfaces listed previously:</span></span>

![Иерархия интерфейса мултимедиастреаминг](images/mmstream01.png)

 

 



