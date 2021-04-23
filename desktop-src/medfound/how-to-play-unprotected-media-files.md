---
description: В этом руководстве показано, как воспроизвести файлы мультимедиа с помощью объекта сеанса мультимедиа.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Воспроизведение мультимедийных файлов с помощью Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104554665"
---
# <a name="how-to-play-media-files-with-media-foundation"></a><span data-ttu-id="2a285-103">Воспроизведение мультимедийных файлов с помощью Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a285-103">How to Play Media Files with Media Foundation</span></span>

<span data-ttu-id="2a285-104">В этом руководстве показано, как воспроизвести файлы мультимедиа с помощью объекта [сеанса мультимедиа](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="2a285-104">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2a285-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="2a285-105">Prerequisites</span></span>

<span data-ttu-id="2a285-106">Прежде чем читать этот раздел, необходимо ознакомиться со следующими концепциями Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="2a285-106">Before reading this topic, you should be familiar with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="2a285-107">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2a285-107">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="2a285-108">Сопоставитель источников</span><span class="sxs-lookup"><span data-stu-id="2a285-108">Source Resolver</span></span>](source-resolver.md)
-   [<span data-ttu-id="2a285-109">Топологии</span><span class="sxs-lookup"><span data-stu-id="2a285-109">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="2a285-110">Генераторы событий мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2a285-110">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="2a285-111">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="2a285-111">Presentation Descriptors</span></span>](presentation-descriptors.md)

> [!Note]  
> <span data-ttu-id="2a285-112">В этом разделе не описывается воспроизведение файлов, защищенных с помощью управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="2a285-112">This topic does not describe how to play files that are protected by digital rights management (DRM).</span></span> <span data-ttu-id="2a285-113">Сведения о DRM в Microsoft Media Foundation см. в разделе [Воспроизведение защищенных файлов мультимедиа](how-to-play-protected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="2a285-113">For information about DRM in Microsoft Media Foundation, see [How to Play Protected Media Files](how-to-play-protected-media-files.md).</span></span>

 

## <a name="overview"></a><span data-ttu-id="2a285-114">Обзор</span><span class="sxs-lookup"><span data-stu-id="2a285-114">Overview</span></span>

<span data-ttu-id="2a285-115">Для воспроизведения файла мультимедиа с помощью сеанса мультимедиа используются следующие объекты:</span><span class="sxs-lookup"><span data-stu-id="2a285-115">The following objects are used to play a media file with the Media Session:</span></span>

-   <span data-ttu-id="2a285-116">*Источник мультимедиа* — это объект, который анализирует файл мультимедиа или другой источник данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a285-116">A *media source* is an object that parses a media file or other source of media data.</span></span> <span data-ttu-id="2a285-117">Источник мультимедиа создает объекты *потока* для каждого звукового или видеопотока в файле.</span><span class="sxs-lookup"><span data-stu-id="2a285-117">The media source creates *stream* objects for each audio or video stream in the file.</span></span> <span data-ttu-id="2a285-118">*Декодеры* преобразуют закодированные данные мультимедиа в несжатые видео и аудио.</span><span class="sxs-lookup"><span data-stu-id="2a285-118">*Decoders* convert encoded media data into uncompressed video and audio.</span></span>
-   <span data-ttu-id="2a285-119">*Сопоставитель источников* создает источник мультимедиа по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="2a285-119">The *Source Resolver* creates a media source from a URL.</span></span>
-   <span data-ttu-id="2a285-120">[Расширенный обработчик видео](enhanced-video-renderer.md) (Евр) визуализирует видео на экране.</span><span class="sxs-lookup"><span data-stu-id="2a285-120">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) renders video to the screen.</span></span>
-   <span data-ttu-id="2a285-121">[Потоковая прорисовка звука](streaming-audio-renderer.md) (САР) визуализирует звук на динамике или другом устройстве вывода звука.</span><span class="sxs-lookup"><span data-stu-id="2a285-121">The [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) renders audio to a speaker or other audio output device.</span></span>
-   <span data-ttu-id="2a285-122">*Топология* определяет поток данных из источника мультимедиа в Евр и САР.</span><span class="sxs-lookup"><span data-stu-id="2a285-122">A *topology* defines the flow of data from the media source to the EVR and SAR.</span></span>
-   <span data-ttu-id="2a285-123">*Сеанс мультимедиа* управляет потоком данных и отправляет события состояния в приложение.</span><span class="sxs-lookup"><span data-stu-id="2a285-123">The *Media Session* controls the data flow and sends status events to the application.</span></span> <span data-ttu-id="2a285-124">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="2a285-124">The following diagram illustrates this process.</span></span>

![Диаграмма, показывающая воспроизведение с помощью сеанса мультимедиа](images/session-playback.gif)

<span data-ttu-id="2a285-126">Ниже приведена общая структура действий, необходимых для воспроизведения файла мультимедиа с помощью сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a285-126">The following is a general outline of the steps needed to play a media file using the Media Session:</span></span>

1.  <span data-ttu-id="2a285-127">Вызовите функцию [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) для инициализации платформы Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2a285-127">Call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="2a285-128">Вызовите [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) , чтобы создать новый экземпляр сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a285-128">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="2a285-129">Используйте сопоставитель источников для создания источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a285-129">Use the source resolver to create a media source.</span></span> <span data-ttu-id="2a285-130">Дополнительные сведения см. [в разделе Использование сопоставителя источников](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="2a285-130">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>
4.  <span data-ttu-id="2a285-131">Создайте топологию, соединяющую источник мультимедиа с ЕВР и САР.</span><span class="sxs-lookup"><span data-stu-id="2a285-131">Create a topology that connects the media source to the EVR and SAR.</span></span> <span data-ttu-id="2a285-132">На этом шаге приложение создает *частичную* топологию, в которую не входят декодеры.</span><span class="sxs-lookup"><span data-stu-id="2a285-132">In this step, the application creates a *partial* topology that does not include the decoders.</span></span> <span data-ttu-id="2a285-133">Дополнительные сведения см. в разделе [Создание топологий воспроизведения](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="2a285-133">For more information, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="2a285-134">Вызовите [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , чтобы задать топологию для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a285-134">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
6.  <span data-ttu-id="2a285-135">Используйте интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) для получения событий из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a285-135">Use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface to get events from the Media Session.</span></span>
7.  <span data-ttu-id="2a285-136">Вызовите [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) , чтобы начать воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="2a285-136">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start playback.</span></span> <span data-ttu-id="2a285-137">После начала воспроизведения его можно приостановить, вызвав метод [**имфмедиасессион::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), или остановите его, вызвав [**Имфмедиасессион:: Остановите**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="2a285-137">After playback starts, you can pause it by calling [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or stop it by calling [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
8.  <span data-ttu-id="2a285-138">При выходе из приложения ресурсы выпуска:</span><span class="sxs-lookup"><span data-stu-id="2a285-138">When the application exits, release resources:</span></span>

    1.  <span data-ttu-id="2a285-139">Вызовите метод [**имфмедиасессион:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) , чтобы закрыть сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a285-139">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span> <span data-ttu-id="2a285-140">Этот метод является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="2a285-140">This method is asynchronous.</span></span> <span data-ttu-id="2a285-141">По завершении сеанс мультимедиа отправляет событие [месессионклосед](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="2a285-141">When it completes, the Media Session sends an [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="2a285-142">Затем можно выполнить оставшиеся действия.</span><span class="sxs-lookup"><span data-stu-id="2a285-142">Then it is safe to perform the remaining steps.</span></span>
    2.  <span data-ttu-id="2a285-143">Вызовите [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) , чтобы завершить работу источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a285-143">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
    3.  <span data-ttu-id="2a285-144">Вызовите [**имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) , чтобы завершить сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2a285-144">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) to shut down the Media Session.</span></span>
    4.  <span data-ttu-id="2a285-145">Вызовите [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) , чтобы завершить работу платформы Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2a285-145">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>

<span data-ttu-id="2a285-146">В следующих разделах показан полный пример кода:</span><span class="sxs-lookup"><span data-stu-id="2a285-146">The following sections show a complete code example:</span></span>

-   [<span data-ttu-id="2a285-147">Шаг 1. объявление класса Кплайер</span><span class="sxs-lookup"><span data-stu-id="2a285-147">Step 1: Declare the CPlayer Class</span></span>](step-1--declare-the-cplayer-class.md)
-   [<span data-ttu-id="2a285-148">Шаг 2. Создание объекта Кплайер</span><span class="sxs-lookup"><span data-stu-id="2a285-148">Step 2: Create the CPlayer Object</span></span>](step-2--create-the-cplayer-object.md)
-   [<span data-ttu-id="2a285-149">Шаг 3. Открытие файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2a285-149">Step 3: Open a Media File</span></span>](step-3--open-a-media-file.md)
-   [<span data-ttu-id="2a285-150">Шаг 4. Создание сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2a285-150">Step 4: Create the Media Session</span></span>](step-4--create-the-media-session.md)
-   [<span data-ttu-id="2a285-151">Шаг 5. Работа с событиями сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2a285-151">Step 5: Handle Media Session Events</span></span>](step-5--handle-media-session-events.md)
-   [<span data-ttu-id="2a285-152">Шаг 6. Управление воспроизведением</span><span class="sxs-lookup"><span data-stu-id="2a285-152">Step 6: Control Playback</span></span>](step-6--control-playback.md)
-   [<span data-ttu-id="2a285-153">Шаг 7. Завершение сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2a285-153">Step 7: Shut Down the Media Session</span></span>](step-7--shut-down-the-media-session.md)
-   [<span data-ttu-id="2a285-154">Пример воспроизведения сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2a285-154">Media Session Playback Example</span></span>](media-session-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="2a285-155">См. также</span><span class="sxs-lookup"><span data-stu-id="2a285-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a285-156">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2a285-156">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="2a285-157">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="2a285-157">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



