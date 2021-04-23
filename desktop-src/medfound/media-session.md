---
description: Сеанс мультимедиа — это объект, который управляет потоком данных в конвейере. Его можно использовать как для воспроизводимых, так и для кодирования файлов.
ms.assetid: dac99908-be90-415d-8837-2f97d573feb5
title: Сеанс мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3df4597e5461788f990f620875bce946570ab97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713293"
---
# <a name="media-session"></a><span data-ttu-id="d5028-104">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d5028-104">Media Session</span></span>

<span data-ttu-id="d5028-105">Сеанс мультимедиа — это объект, который управляет потоком данных в конвейере.</span><span class="sxs-lookup"><span data-stu-id="d5028-105">The Media Session is an object that manages data flow in the pipeline.</span></span> <span data-ttu-id="d5028-106">Его можно использовать как для воспроизводимых, так и для кодирования файлов.</span><span class="sxs-lookup"><span data-stu-id="d5028-106">It can be used for both playing and encoding files.</span></span>

<span data-ttu-id="d5028-107">В этом разделе описывается сеанс мультимедиа с точки зрения архитектуры.</span><span class="sxs-lookup"><span data-stu-id="d5028-107">This section describes the Media Session from an architectural standpoint.</span></span> <span data-ttu-id="d5028-108">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="d5028-108">It contains the following sections:</span></span>



| <span data-ttu-id="d5028-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="d5028-109">Topic</span></span>                                                                                        | <span data-ttu-id="d5028-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d5028-110">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5028-111">Сведения о сеансе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d5028-111">About the Media Session</span></span>](about-the-media-session.md)                                       | <span data-ttu-id="d5028-112">Содержит общие сведения о сеансе мультимедиа, о том, как приложение может создать сеанс мультимедиа и как сеанс мультимедиа управляет временем презентации.</span><span class="sxs-lookup"><span data-stu-id="d5028-112">Provides an overview of the Media Session, how an application can create the Media Session, and how the Media Session manages presentation time.</span></span> |
| [<span data-ttu-id="d5028-113">Топологии</span><span class="sxs-lookup"><span data-stu-id="d5028-113">Topologies</span></span>](topologies.md)                                                                 | <span data-ttu-id="d5028-114">Топология — это объект, представляющий поток данных в конвейере.</span><span class="sxs-lookup"><span data-stu-id="d5028-114">A topology is an object that represents the flow of data in the pipeline.</span></span>                                                                        |
| [<span data-ttu-id="d5028-115">События сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d5028-115">Media Session Events</span></span>](media-session-events.md)                                             | <span data-ttu-id="d5028-116">Описание событий, которые приложение может получить из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d5028-116">Describes the events that an application might receive from the Media Session.</span></span>                                                                   |
| [<span data-ttu-id="d5028-117">Управление состояниями представления</span><span class="sxs-lookup"><span data-stu-id="d5028-117">How to Control Presentation States</span></span>](how-to-control-presentation-states.md)                 | <span data-ttu-id="d5028-118">Описание элементов управления транспорта сеанса мультимедиа: воспроизведение, приостановка и остановка.</span><span class="sxs-lookup"><span data-stu-id="d5028-118">Describes the Media Session transport controls: Play, Pause, and Stop.</span></span>                                                                           |
| [<span data-ttu-id="d5028-119">Использование источников мультимедиа с сеансом мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d5028-119">Using Media Sources with the Media Session</span></span>](using-media-sources-with-the-media-session.md) | <span data-ttu-id="d5028-120">Использование источников мультимедиа с сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d5028-120">How to use media sources with the Media Session.</span></span>                                                                                                 |
| [<span data-ttu-id="d5028-121">Управление скоростью</span><span class="sxs-lookup"><span data-stu-id="d5028-121">Rate Control</span></span>](rate-control.md)                                                             | <span data-ttu-id="d5028-122">Описывает, как управлять скоростью воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d5028-122">Describes how to control playback rate.</span></span>                                                                                                          |
| [<span data-ttu-id="d5028-123">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="d5028-123">Video Quality Management</span></span>](video-quality-management.md)                                     | <span data-ttu-id="d5028-124">Описание улучшений конвейера видео в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d5028-124">Describes improvements to the video pipeline in Windows 7.</span></span>                                                                                       |
| [<span data-ttu-id="d5028-125">Сеанс PMP мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d5028-125">PMP Media Session</span></span>](pmp-media-session.md)                                                   | <span data-ttu-id="d5028-126">Описание процедуры создания сеанса мультимедиа в рамках процесса защищенного пути к носителю (PMP).</span><span class="sxs-lookup"><span data-stu-id="d5028-126">Describes how to create the Media Session inside a Protected Media Path (PMP) process.</span></span>                                                           |



 

<span data-ttu-id="d5028-127">В следующих разделах описывается использование сеанса мультимедиа в конкретных сценариях приложений.</span><span class="sxs-lookup"><span data-stu-id="d5028-127">The following topics describe how to use the Media Session in specific application scenarios:</span></span>

-   [<span data-ttu-id="d5028-128">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="d5028-128">Audio/Video Playback</span></span>](audio-video-playback.md)
-   [<span data-ttu-id="d5028-129">Кодировка и разработка файлов</span><span class="sxs-lookup"><span data-stu-id="d5028-129">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)

## <a name="related-topics"></a><span data-ttu-id="d5028-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d5028-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5028-131">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5028-131">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="d5028-132">**имфмедиасессион**</span><span class="sxs-lookup"><span data-stu-id="d5028-132">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> </dl>

 

 



