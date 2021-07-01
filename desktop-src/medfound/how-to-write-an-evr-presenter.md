---
description: В этой статье описывается, как написать пользовательский объект Presenter для расширенного модуля подготовки видео (Евр).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Написание выступающего Евр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505ba7ec225ac5f1316ad4343a4e1058ff0b6cb8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118779"
---
# <a name="how-to-write-an-evr-presenter"></a><span data-ttu-id="eb1e4-103">Написание выступающего Евр</span><span class="sxs-lookup"><span data-stu-id="eb1e4-103">How to Write an EVR Presenter</span></span>

<span data-ttu-id="eb1e4-104">В этой статье описывается, как написать пользовательский объект Presenter для расширенного модуля подготовки видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-104">This article describes how to write a custom presenter for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="eb1e4-105">Пользовательский выступающий может использоваться как в DirectShow, так и в Media Foundation; интерфейсы и объектная модель одинаковы для обеих технологий, хотя точная последовательность операций может отличаться.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-105">A custom presenter can be used with both DirectShow and Media Foundation; the interfaces and object model are the same for both technologies, although the exact sequence of operations might vary.</span></span>

<span data-ttu-id="eb1e4-106">Пример кода в этом разделе адаптируется из [образца еврпресентер](evrpresenter-sample.md), который предоставляется в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-106">The example code in this topic is adapted from the [EVRPresenter Sample](evrpresenter-sample.md), which is provided in the Windows SDK.</span></span>

<span data-ttu-id="eb1e4-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="eb1e4-108">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="eb1e4-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="eb1e4-109">Объектная модель Presenter</span><span class="sxs-lookup"><span data-stu-id="eb1e4-109">Presenter Object Model</span></span>](#presenter-object-model)
    -   [<span data-ttu-id="eb1e4-110">Поток данных внутри Евр</span><span class="sxs-lookup"><span data-stu-id="eb1e4-110">Data Flow Inside the EVR</span></span>](#data-flow-inside-the-evr)
    -   [<span data-ttu-id="eb1e4-111">Состояния выступающих</span><span class="sxs-lookup"><span data-stu-id="eb1e4-111">Presenter States</span></span>](#presenter-states)
    -   [<span data-ttu-id="eb1e4-112">Интерфейсы выступающих</span><span class="sxs-lookup"><span data-stu-id="eb1e4-112">Presenter Interfaces</span></span>](#presenter-interfaces)
    -   [<span data-ttu-id="eb1e4-113">Реализация Имфвидеодевицеид</span><span class="sxs-lookup"><span data-stu-id="eb1e4-113">Implementing IMFVideoDeviceID</span></span>](#implementing-imfvideodeviceid)
    -   [<span data-ttu-id="eb1e4-114">Реализация Имфтопологисервицелукупклиент</span><span class="sxs-lookup"><span data-stu-id="eb1e4-114">Implementing IMFTopologyServiceLookupClient</span></span>](#implementing-imftopologyservicelookupclient)
    -   [<span data-ttu-id="eb1e4-115">Реализация Имфвидеопресентер</span><span class="sxs-lookup"><span data-stu-id="eb1e4-115">Implementing IMFVideoPresenter</span></span>](#implementing-imfvideopresenter)
    -   [<span data-ttu-id="eb1e4-116">Реализация Имфклоккстатесинк</span><span class="sxs-lookup"><span data-stu-id="eb1e4-116">Implementing IMFClockStateSink</span></span>](#implementing-imfclockstatesink)
    -   [<span data-ttu-id="eb1e4-117">Реализация Имфратесуппорт</span><span class="sxs-lookup"><span data-stu-id="eb1e4-117">Implementing IMFRateSupport</span></span>](#implementing-imfratesupport)
    -   [<span data-ttu-id="eb1e4-118">Отправка событий в Евр</span><span class="sxs-lookup"><span data-stu-id="eb1e4-118">Sending Events to the EVR</span></span>](#sending-events-to-the-evr)
-   [<span data-ttu-id="eb1e4-119">Форматы согласования</span><span class="sxs-lookup"><span data-stu-id="eb1e4-119">Negotiating Formats</span></span>](#negotiating-formats)
-   [<span data-ttu-id="eb1e4-120">Управление устройством Direct3D</span><span class="sxs-lookup"><span data-stu-id="eb1e4-120">Managing the Direct3D Device</span></span>](#managing-the-direct3d-device)
    -   [<span data-ttu-id="eb1e4-121">Выделение поверхностей Direct3D</span><span class="sxs-lookup"><span data-stu-id="eb1e4-121">Allocating Direct3D Surfaces</span></span>](#allocating-direct3d-surfaces)
    -   [<span data-ttu-id="eb1e4-122">Примеры. Отслеживание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-122">Tracking Samples</span></span>](#tracking-samples)
-   [<span data-ttu-id="eb1e4-123">Обработка выходных данных</span><span class="sxs-lookup"><span data-stu-id="eb1e4-123">Processing Output</span></span>](#processing-output)
    -   [<span data-ttu-id="eb1e4-124">Перерисовка кадров</span><span class="sxs-lookup"><span data-stu-id="eb1e4-124">Repainting Frames</span></span>](#repainting-frames)
    -   [<span data-ttu-id="eb1e4-125">Примеры планирования</span><span class="sxs-lookup"><span data-stu-id="eb1e4-125">Scheduling Samples</span></span>](#scheduling-samples)
    -   [<span data-ttu-id="eb1e4-126">Представление образцов</span><span class="sxs-lookup"><span data-stu-id="eb1e4-126">Presenting Samples</span></span>](#presenting-samples)
    -   [<span data-ttu-id="eb1e4-127">Исходный и конечный прямоугольники</span><span class="sxs-lookup"><span data-stu-id="eb1e4-127">Source and Destination Rectangles</span></span>](#source-and-destination-rectangles)
    -   [<span data-ttu-id="eb1e4-128">Конец потока</span><span class="sxs-lookup"><span data-stu-id="eb1e4-128">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="eb1e4-129">Пошаговое выполнение кадра</span><span class="sxs-lookup"><span data-stu-id="eb1e4-129">Frame Stepping</span></span>](#frame-stepping)
    -   [<span data-ttu-id="eb1e4-130">Реализация пошагового выполнения кадра</span><span class="sxs-lookup"><span data-stu-id="eb1e4-130">Implementing Frame Stepping</span></span>](#implementing-frame-stepping)
-   [<span data-ttu-id="eb1e4-131">Установка параметра Presenter в Евр</span><span class="sxs-lookup"><span data-stu-id="eb1e4-131">Setting the Presenter on the EVR</span></span>](#setting-the-presenter-on-the-evr)
    -   [<span data-ttu-id="eb1e4-132">Настройка выступающего в DirectShow</span><span class="sxs-lookup"><span data-stu-id="eb1e4-132">Setting the Presenter in DirectShow</span></span>](#setting-the-presenter-in-directshow)
    -   [<span data-ttu-id="eb1e4-133">Настройка выступающего в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb1e4-133">Setting the Presenter in Media Foundation</span></span>](#setting-the-presenter-in-media-foundation)
-   [<span data-ttu-id="eb1e4-134">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="eb1e4-134">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="eb1e4-135">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="eb1e4-135">Prerequisites</span></span>

<span data-ttu-id="eb1e4-136">Перед написанием пользовательского Presenter необходимо ознакомиться со следующими технологиями:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-136">Before writing a custom presenter, you should be familiar with the following technologies:</span></span>

-   <span data-ttu-id="eb1e4-137">Расширенный модуль подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-137">The enhanced video renderer.</span></span> <span data-ttu-id="eb1e4-138">См. [Расширенный модуль подготовки видео](enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-138">See [Enhanced Video Renderer](enhanced-video-renderer.md).</span></span>
-   <span data-ttu-id="eb1e4-139">Графическая система Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-139">Direct3D graphics.</span></span> <span data-ttu-id="eb1e4-140">Для написания выступающего не нужно понимать трехмерную графику, но вам необходимо знать, как создать устройство Direct3D и управлять областями Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-140">You don't need to understand 3-D graphics to write a presenter, but you must know how to create a Direct3D device and manage Direct3D surfaces.</span></span> <span data-ttu-id="eb1e4-141">Если вы не знакомы с Direct3D, ознакомьтесь с разделами "устройства Direct3D" и "ресурсы Direct3D" в документации по DirectX Graphics SDK.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-141">If you aren't familiar with Direct3D, read the sections "Direct3D Devices" and "Direct3D Resources" in the DirectX Graphics SDK documentation.</span></span>
-   <span data-ttu-id="eb1e4-142">Графы фильтров DirectShow или конвейер Media Foundation в зависимости от того, какая технология будет использоваться приложением для визуализации видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-142">DirectShow filter graphs or the Media Foundation pipeline, depending on which technology your application will use to render video.</span></span>
-   <span data-ttu-id="eb1e4-143">[Преобразования Media Foundation](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-143">[Media Foundation Transforms](media-foundation-transforms.md).</span></span> <span data-ttu-id="eb1e4-144">Микшер Евр является Media Foundation преобразованием, а выступающий вызывает методы непосредственно в микшере.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-144">The EVR mixer is a Media Foundation transform, and the presenter calls methods directly on the mixer.</span></span>
-   <span data-ttu-id="eb1e4-145">Реализация COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-145">Implementing COM objects.</span></span> <span data-ttu-id="eb1e4-146">Выступающий — это внутрипроцессный COM-объект с произвольным потоком.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-146">The presenter is an in-process, free-threaded COM object.</span></span>

## <a name="presenter-object-model"></a><span data-ttu-id="eb1e4-147">Объектная модель Presenter</span><span class="sxs-lookup"><span data-stu-id="eb1e4-147">Presenter Object Model</span></span>

<span data-ttu-id="eb1e4-148">В этом разделе содержится обзор объектной модели и интерфейсов Presenter.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-148">This section contains an overview the presenter object model and interfaces.</span></span>

### <a name="data-flow-inside-the-evr"></a><span data-ttu-id="eb1e4-149">Поток данных внутри Евр</span><span class="sxs-lookup"><span data-stu-id="eb1e4-149">Data Flow Inside the EVR</span></span>

<span data-ttu-id="eb1e4-150">Евр использует два подключаемых компонента для отрисовки видео: *микшер* и *Presenter*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-150">The EVR uses two plug-in components to render video: the *mixer* and the *presenter*.</span></span> <span data-ttu-id="eb1e4-151">Микшер смешивает видеопотокы и при необходимости разменяет видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-151">The mixer blends the video streams and deinterlaces the video if needed.</span></span> <span data-ttu-id="eb1e4-152">Выступающий рисует (или *представляет*) видео на экране и планируется при прорисовке каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-152">The presenter draws (or *presents*) the video onto the display and schedules when each frame is drawn.</span></span> <span data-ttu-id="eb1e4-153">Приложения могут заменить любой из этих объектов пользовательской реализацией.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-153">Applications can replace either of these objects with a custom implementation.</span></span>

<span data-ttu-id="eb1e4-154">Евр имеет один или несколько входных потоков, а микшер имеет соответствующее количество входных потоков.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-154">The EVR has one or more input streams, and the mixer has a corresponding number of input streams.</span></span> <span data-ttu-id="eb1e4-155">Поток 0 всегда является *ссылочным потоком*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-155">Stream 0 is always the *reference stream*.</span></span> <span data-ttu-id="eb1e4-156">Другие потоки — это *подпотоки*, которые микшер альфа-смешивается на поток ссылок.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-156">The other streams are *substreams*, which the mixer alpha-blends onto the reference stream.</span></span> <span data-ttu-id="eb1e4-157">Ссылочный поток определяет ставку основного кадра для композитного видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-157">The reference stream determines the master frame-rate for the composited video.</span></span> <span data-ttu-id="eb1e4-158">Для каждого опорного кадра микшер принимает самый последний кадр из каждого подпотока, альфа-смешение их со ссылочным кадром и выводит один составной кадр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-158">For each reference frame, the mixer takes the most recent frame from each substream, alpha-blends them onto the reference frame, and outputs a single composited frame.</span></span> <span data-ttu-id="eb1e4-159">Микшер также выполняет дечередование и преобразование цветов из YUV в RGB при необходимости.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-159">The mixer also performs deinterlacing and color conversion from YUV to RGB if needed.</span></span> <span data-ttu-id="eb1e4-160">Евр всегда вставляет микшер в видеоконвейер, независимо от числа входных потоков или формата видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-160">The EVR always inserts the mixer into the video pipeline, regardless of the number of input streams or the video format.</span></span> <span data-ttu-id="eb1e4-161">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-161">The following image illustrates this process.</span></span>

![Схема, показывающая поток ссылок и подпоток, указывающий микшер, указывающий на выступающий, указывающий на дисплей](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

<span data-ttu-id="eb1e4-163">Выступающий выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-163">The presenter performs the following tasks:</span></span>

-   <span data-ttu-id="eb1e4-164">Задает формат вывода для микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-164">Sets the output format on the mixer.</span></span> <span data-ttu-id="eb1e4-165">Перед началом потоковой передачи, выступающий задает тип мультимедиа в выходном потоке микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-165">Before streaming begins, the presenter sets a media type on the mixer's output stream.</span></span> <span data-ttu-id="eb1e4-166">Этот тип мультимедиа определяет формат составного изображения.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-166">This media type defines the format of the composited image.</span></span>
-   <span data-ttu-id="eb1e4-167">Создает устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-167">Creates the Direct3D device.</span></span>
-   <span data-ttu-id="eb1e4-168">Выделяет поверхности Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-168">Allocates Direct3D surfaces.</span></span> <span data-ttu-id="eb1e4-169">Микшер блитс составные кадры на эти поверхности.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-169">The mixer blits the composited frames onto these surfaces.</span></span>
-   <span data-ttu-id="eb1e4-170">Возвращает выходные данные микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-170">Gets the output from the mixer.</span></span>
-   <span data-ttu-id="eb1e4-171">Планирует, когда отображаются кадры.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-171">Schedules when the frames are presented.</span></span> <span data-ttu-id="eb1e4-172">Евр предоставляет часы презентации, и выступающие планирует кадры в соответствии с этим часами.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-172">The EVR provides the presentation clock, and the presenter schedules frames according to this clock.</span></span>
-   <span data-ttu-id="eb1e4-173">Представляет каждый кадр с помощью Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-173">Presents each frame using Direct3D.</span></span>
-   <span data-ttu-id="eb1e4-174">Выполняет пошаговое выполнение и очистку кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-174">Performs frame stepping and scrubbing.</span></span>

### <a name="presenter-states"></a><span data-ttu-id="eb1e4-175">Состояния выступающих</span><span class="sxs-lookup"><span data-stu-id="eb1e4-175">Presenter States</span></span>

<span data-ttu-id="eb1e4-176">В любое время выступающий находится в одном из следующих состояний:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-176">At any time, the presenter is in one of following states:</span></span>

-   <span data-ttu-id="eb1e4-177">*Запущено*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-177">*Started*.</span></span> <span data-ttu-id="eb1e4-178">Часы презентации Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-178">The EVR's presentation clock is running.</span></span> <span data-ttu-id="eb1e4-179">Выступающие планирует видеоматериалы для представления по мере их прибытия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-179">The presenter schedules video frames for presentation as they arrive.</span></span>
-   <span data-ttu-id="eb1e4-180">*Приостановлено*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-180">*Paused*.</span></span> <span data-ttu-id="eb1e4-181">Часы презентации приостановлены.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-181">The presentation clock is suspended.</span></span> <span data-ttu-id="eb1e4-182">В выступающих отсутствуют новые образцы, но хранится очередь запланированных выборок.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-182">The presenter does not present any new samples but maintains its queue of scheduled samples.</span></span> <span data-ttu-id="eb1e4-183">Если поступают новые образцы, они добавляются в очередь.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-183">If new samples are received, the presenter adds them to the queue.</span></span>
-   <span data-ttu-id="eb1e4-184">*Остановлен*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-184">*Stopped*.</span></span> <span data-ttu-id="eb1e4-185">Часы презентации остановлены.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-185">The presentation clock is stopped.</span></span> <span data-ttu-id="eb1e4-186">Выступающий отклоняет все запланированные выборки.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-186">The presenter discards any samples that were scheduled.</span></span>
-   <span data-ttu-id="eb1e4-187">*Завершение работы*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-187">*Shut down*.</span></span> <span data-ttu-id="eb1e4-188">Выступающие освобождает все ресурсы, связанные с потоковой передачей, например, поверхности Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-188">The presenter releases any resources related to streaming, such as Direct3D surfaces.</span></span> <span data-ttu-id="eb1e4-189">Это начальное состояние выступающего и конечное состояние до уничтожения выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-189">This is the presenter's initial state, and the final state before the presenter is destroyed.</span></span>

<span data-ttu-id="eb1e4-190">В примере кода в этом разделе Состояние выступающего представлено перечислением:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-190">In the example code in this topic, the presenter state is represented by an enumeration:</span></span>


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



<span data-ttu-id="eb1e4-191">Некоторые операции недопустимы, пока выступающий находится в состоянии завершения работы.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-191">Some operations are not valid while the presenter is in the shutdown state.</span></span> <span data-ttu-id="eb1e4-192">Пример кода проверяет это состояние, вызывая вспомогательный метод:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-192">The example code checks for this state by calling a helper method:</span></span>


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a><span data-ttu-id="eb1e4-193">Интерфейсы выступающих</span><span class="sxs-lookup"><span data-stu-id="eb1e4-193">Presenter Interfaces</span></span>

<span data-ttu-id="eb1e4-194">Для реализации следующих интерфейсов требуется выступающий.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-194">A presenter is required to implement the following interfaces:</span></span>



| <span data-ttu-id="eb1e4-195">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="eb1e4-195">Interface</span></span>                                                                | <span data-ttu-id="eb1e4-196">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-196">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb1e4-197">**имфклоккстатесинк**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-197">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | <span data-ttu-id="eb1e4-198">Уведомляет выступающий, когда изменяется состояние часов Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-198">Notifies the presenter when the EVR's clock changes state.</span></span> <span data-ttu-id="eb1e4-199">См. раздел [Реализация имфклоккстатесинк](#implementing-imfclockstatesink).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-199">See [Implementing IMFClockStateSink](#implementing-imfclockstatesink).</span></span>                                   |
| [<span data-ttu-id="eb1e4-200">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-200">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | <span data-ttu-id="eb1e4-201">Предоставляет приложению и другим компонентам конвейера способ получения интерфейсов от выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-201">Provides a way for the application and other components in the pipeline to get interfaces from the presenter.</span></span>                                                       |
| [<span data-ttu-id="eb1e4-202">**имфтопологисервицелукупклиент**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-202">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | <span data-ttu-id="eb1e4-203">Позволяет ведущему получать интерфейсы от Евр или микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-203">Enables the presenter to get interfaces from the EVR or the mixer.</span></span> <span data-ttu-id="eb1e4-204">См. раздел [Реализация имфтопологисервицелукупклиент](#implementing-imftopologyservicelookupclient).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-204">See [Implementing IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient).</span></span> |
| [<span data-ttu-id="eb1e4-205">**имфвидеодевицеид**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-205">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | <span data-ttu-id="eb1e4-206">Гарантирует, что выступающий и микшер используют совместимые технологии.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-206">Ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="eb1e4-207">См. раздел [Реализация имфвидеодевицеид](#implementing-imfvideodeviceid).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-207">See [Implementing IMFVideoDeviceID](#implementing-imfvideodeviceid).</span></span>                          |
| [<span data-ttu-id="eb1e4-208">**имфвидеопресентер**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-208">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | <span data-ttu-id="eb1e4-209">Обрабатывает сообщения от Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-209">Processes messages from the EVR.</span></span> <span data-ttu-id="eb1e4-210">См. раздел [Реализация имфвидеопресентер](#implementing-imfvideopresenter).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-210">See [Implementing IMFVideoPresenter](#implementing-imfvideopresenter).</span></span>                                                             |



 

<span data-ttu-id="eb1e4-211">Следующие интерфейсы являются необязательными:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-211">The following interfaces are optional:</span></span>



| <span data-ttu-id="eb1e4-212">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="eb1e4-212">Interface</span></span>                                                | <span data-ttu-id="eb1e4-213">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-213">Description</span></span>                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb1e4-214">**иевртрустедвидеоплугин**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-214">**IEVRTrustedVideoPlugin**</span></span>](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | <span data-ttu-id="eb1e4-215">Позволяет ведущему работать с защищенным носителем.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-215">Enables the presenter to work with protected media.</span></span> <span data-ttu-id="eb1e4-216">Реализуйте этот интерфейс, если ваш Presenter является доверенным компонентом, предназначенным для работы в защищенном пути носителя (PMP).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-216">Implement this interface if your presenter is a trusted component designed to work in the protected media path (PMP).</span></span> |
| [<span data-ttu-id="eb1e4-217">**имфратесуппорт**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-217">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | <span data-ttu-id="eb1e4-218">Сообщает диапазон скорости воспроизведения, поддерживаемый выступающим.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-218">Reports the range of playback rates that the presenter supports.</span></span> <span data-ttu-id="eb1e4-219">См. раздел [Реализация имфратесуппорт](#implementing-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-219">See [Implementing IMFRateSupport](#implementing-imfratesupport).</span></span>                                         |
| [<span data-ttu-id="eb1e4-220">**имфвидеопоситионмаппер**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-220">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | <span data-ttu-id="eb1e4-221">Сопоставляет координаты на выходном видеокадре с координатами на входном видеокадре.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-221">Maps coordinates on the output video frame to coordinates on the input video frame.</span></span>                                                                                       |
| [<span data-ttu-id="eb1e4-222">**икуалпроп**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-222">**IQualProp**</span></span>](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | <span data-ttu-id="eb1e4-223">Сообщает сведения о производительности.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-223">Reports performance information.</span></span> <span data-ttu-id="eb1e4-224">Евр использует эти сведения для управления качеством.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-224">The EVR uses this information for quality-control management.</span></span> <span data-ttu-id="eb1e4-225">Этот интерфейс описан в пакете SDK для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-225">This interface is documented in the DirectShow SDK.</span></span>                        |



 

<span data-ttu-id="eb1e4-226">Вы также можете предоставить интерфейсы для приложения для взаимодействия с выступающим.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-226">You can also provide interfaces for the application to communicate with the presenter.</span></span> <span data-ttu-id="eb1e4-227">Для этой цели в стандартном выступающем реализуется интерфейс [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-227">The standard presenter implements the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface for this purpose.</span></span> <span data-ttu-id="eb1e4-228">Вы можете реализовать этот интерфейс или определить собственный.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-228">You can implement this interface or define your own.</span></span> <span data-ttu-id="eb1e4-229">Приложение получает интерфейсы от Presenter, вызывая [**имфжетсервице::**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Евр в.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-229">The application obtains interfaces from the presenter by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR.</span></span> <span data-ttu-id="eb1e4-230">Если идентификатор GUID службы **MR_VIDEO_RENDER_SERVICE**, ЕВР **передает запрос на** выступающий.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-230">When the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR passes the **GetService** request to the presenter.</span></span>

### <a name="implementing-imfvideodeviceid"></a><span data-ttu-id="eb1e4-231">Реализация Имфвидеодевицеид</span><span class="sxs-lookup"><span data-stu-id="eb1e4-231">Implementing IMFVideoDeviceID</span></span>

<span data-ttu-id="eb1e4-232">Интерфейс [**имфвидеодевицеид**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) содержит один метод [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), который возвращает GUID устройства.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-232">The [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) interface contains one method, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), which returns a device GUID.</span></span> <span data-ttu-id="eb1e4-233">GUID устройства гарантирует, что выступающий и микшер используют совместимые технологии.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-233">The device GUID ensures that the presenter and the mixer use compatible technologies.</span></span> <span data-ttu-id="eb1e4-234">Если идентификаторы GUID устройства не совпадают, инициализация Евр не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-234">If the device GUIDs do not match, the EVR fails to initialize.</span></span>

<span data-ttu-id="eb1e4-235">Стандартный микшер и настоящее устройство используют Direct3D 9 с идентификатором GUID устройства, равным **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-235">The standard mixer and presenter both use Direct3D 9, with the device GUID equal to **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="eb1e4-236">Если вы планируете использовать пользовательский объект Presenter со стандартным микшером, то GUID устройства должен быть **IID_IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-236">If you intend to use your custom presenter with the standard mixer, the presenter's device GUID must be **IID_IDirect3DDevice9**.</span></span> <span data-ttu-id="eb1e4-237">При замене обоих компонентов можно определить новый GUID устройства.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-237">If you replace both components, you could define a new device GUID.</span></span> <span data-ttu-id="eb1e4-238">В оставшейся части этой статьи предполагается, что в выступающих используется Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-238">For the remainder of this article, it is assumed that the presenter uses Direct3D 9.</span></span> <span data-ttu-id="eb1e4-239">Ниже приведена стандартная реализация [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-239">Here is the standard implementation of [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):</span></span>


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



<span data-ttu-id="eb1e4-240">Метод должен быть выполнен, даже когда выступающий завершает работу.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-240">The method should succeed even when the presenter is shut down.</span></span>

### <a name="implementing-imftopologyservicelookupclient"></a><span data-ttu-id="eb1e4-241">Реализация Имфтопологисервицелукупклиент</span><span class="sxs-lookup"><span data-stu-id="eb1e4-241">Implementing IMFTopologyServiceLookupClient</span></span>

<span data-ttu-id="eb1e4-242">Интерфейс [**имфтопологисервицелукупклиент**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) позволяет ведущему получать указатели интерфейса из Евр и из микшера следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-242">The [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) interface enables the presenter to get interface pointers from the EVR and from the mixer as follows:</span></span>

1.  <span data-ttu-id="eb1e4-243">Когда Евр инициализирует выступающий, он вызывает метод [**имфтопологисервицелукупклиент:: инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-243">When the EVR initializes the presenter, it calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="eb1e4-244">Аргумент является указателем на интерфейс [**ИМФТОПОЛОГИСЕРВИЦЕЛУКУП**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-244">The argument is a pointer to the EVR's [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) interface.</span></span>
2.  <span data-ttu-id="eb1e4-245">Выступающий вызывает [**имфтопологисервицелукуп:: лукупсервице**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) , чтобы получить указатели интерфейса из Евр или микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-245">The presenter calls [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) to get interface pointers from either the EVR or the mixer.</span></span>

<span data-ttu-id="eb1e4-246">Метод [**лукупсервице**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) аналогичен методу [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-246">The [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) method is similar to the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="eb1e4-247">Оба метода принимают в качестве входных данных идентификатор GUID службы и идентификатор интерфейса (IID), но **лукупсервице** возвращает массив указателей интерфейса, а функция- **службы** возвращает один указатель.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-247">Both methods take a service GUID and an interface identifier (IID) as input, but **LookupService** returns an array of interface pointers, while **GetService** returns a single pointer.</span></span> <span data-ttu-id="eb1e4-248">Однако на практике размер массива всегда можно задать равным 1.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-248">In practice, however, you can always set the array size to 1.</span></span> <span data-ttu-id="eb1e4-249">Запрашиваемый объект зависит от идентификатора GUID службы:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-249">The object queried depends on the service GUID:</span></span>

-   <span data-ttu-id="eb1e4-250">Если идентификатор GUID службы — **MR_VIDEO_RENDER_SERVICE**, ЕВР запрашивается.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-250">If the service GUID is **MR_VIDEO_RENDER_SERVICE**, the EVR is queried.</span></span>
-   <span data-ttu-id="eb1e4-251">Если идентификатор GUID службы — **MR_VIDEO_MIXER_SERVICE**, запрашивается микшер.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-251">If the service GUID is **MR_VIDEO_MIXER_SERVICE**, the mixer is queried.</span></span>

<span data-ttu-id="eb1e4-252">В реализации [**инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)получите следующие интерфейсы из Евр:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-252">In your implementation of [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), get the following interfaces from the EVR:</span></span>



| <span data-ttu-id="eb1e4-253">Интерфейс Евр</span><span class="sxs-lookup"><span data-stu-id="eb1e4-253">EVR Interface</span></span>                                | <span data-ttu-id="eb1e4-254">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-254">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb1e4-255">**имедиаевентсинк**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-255">**IMediaEventSink**</span></span>](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | <span data-ttu-id="eb1e4-256">Предоставляет выступающий способ отправки сообщений в Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-256">Provides a way for the presenter to send messages to the EVR.</span></span> <span data-ttu-id="eb1e4-257">Этот интерфейс определен в пакете SDK DirectShow, поэтому сообщения следуют шаблону для событий DirectShow, а не Media Foundation событий.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-257">This interface is defined in the DirectShow SDK, so the messages follow the pattern for DirectShow events, not Media Foundation events.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="eb1e4-258">**имфклокк**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-258">**IMFClock**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | <span data-ttu-id="eb1e4-259">Представляет часы Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-259">Represents the EVR's clock.</span></span> <span data-ttu-id="eb1e4-260">Выступающий использует этот интерфейс для планирования образцов для представления.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-260">The presenter uses this interface to schedule samples for presentation.</span></span> <span data-ttu-id="eb1e4-261">Евр может выполняться без часов, поэтому этот интерфейс может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-261">The EVR can run without a clock, so this interface might not be available.</span></span> <span data-ttu-id="eb1e4-262">В противном случае не обращайте внимания на код ошибки из [**лукупсервице**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-262">If not, ignore the error code from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).</span></span><br/> <span data-ttu-id="eb1e4-263">Часы также реализуют интерфейс [**имфтимер**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-263">The clock also implements the [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) interface.</span></span> <span data-ttu-id="eb1e4-264">В конвейере Media Foundation часы реализуют интерфейс [**имфпресентатионклокк**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-264">In the Media Foundation pipeline, the clock implements the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span> <span data-ttu-id="eb1e4-265">Он не реализует этот интерфейс в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-265">It does not implement this interface in DirectShow.</span></span><br/> |



 

<span data-ttu-id="eb1e4-266">Получите следующие интерфейсы из микшера:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-266">Get the following interfaces from the mixer:</span></span>



| <span data-ttu-id="eb1e4-267">Интерфейс микшера</span><span class="sxs-lookup"><span data-stu-id="eb1e4-267">Mixer Interface</span></span>                              | <span data-ttu-id="eb1e4-268">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-268">Description</span></span>                                                |
|----------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="eb1e4-269">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-269">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | <span data-ttu-id="eb1e4-270">Позволяет выступающим взаимодействовать с микшером.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-270">Enables the presenter to communicate with the mixer.</span></span>       |
| [<span data-ttu-id="eb1e4-271">**имфвидеодевицеид**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-271">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | <span data-ttu-id="eb1e4-272">Позволяет выступающему проверить GUID устройства микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-272">Enables the presenter to validate the mixer's device GUID.</span></span> |



 

<span data-ttu-id="eb1e4-273">Следующий код реализует метод [**инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :</span><span class="sxs-lookup"><span data-stu-id="eb1e4-273">The following code implements the [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method :</span></span>


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="eb1e4-274">Если указатели интерфейса, полученные из [**лукупсервице**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) , больше не являются допустимыми, ЕВР вызывает [**Имфтопологисервицелукупклиент:: релеасесервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-274">When the interface pointers obtained from [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) are no longer valid, the EVR calls [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers).</span></span> <span data-ttu-id="eb1e4-275">В этом методе Освободите все указатели интерфейсов и задайте для параметра Состояние выступающего значение Завершение работы:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-275">Inside this method, release all interface pointers and set the presenter state to shut down:</span></span>


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



<span data-ttu-id="eb1e4-276">Евр вызывает [**релеасесервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) по различным причинам, включая:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-276">The EVR calls [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) for various reasons, including:</span></span>

-   <span data-ttu-id="eb1e4-277">Отключение или повторное соединение ПИН-кодов (DirectShow), добавление или удаление приемников потоков (Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-277">Disconnecting or reconnecting pins (DirectShow), or adding or removing stream sinks (Media Foundation).</span></span>
-   <span data-ttu-id="eb1e4-278">Изменение формата.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-278">Changing format.</span></span>
-   <span data-ttu-id="eb1e4-279">Установка новых часов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-279">Setting a new clock.</span></span>
-   <span data-ttu-id="eb1e4-280">Окончательное завершение работы Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-280">Final shutdown of the EVR.</span></span>

<span data-ttu-id="eb1e4-281">В течение времени жизни выступающего Евр может вызывать [**инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) и [**релеасесервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) несколько раз.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-281">During the lifetime of the presenter, the EVR might call [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) and [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) several times.</span></span>

### <a name="implementing-imfvideopresenter"></a><span data-ttu-id="eb1e4-282">Реализация Имфвидеопресентер</span><span class="sxs-lookup"><span data-stu-id="eb1e4-282">Implementing IMFVideoPresenter</span></span>

<span data-ttu-id="eb1e4-283">Интерфейс [**имфвидеопресентер**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) наследует [**имфклоккстатесинк**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) и добавляет два метода:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-283">The [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface inherits [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) and adds two methods:</span></span>



| <span data-ttu-id="eb1e4-284">Метод</span><span class="sxs-lookup"><span data-stu-id="eb1e4-284">Method</span></span>                                                               | <span data-ttu-id="eb1e4-285">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-285">Description</span></span>                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="eb1e4-286">**жеткуррентмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-286">**GetCurrentMediaType**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | <span data-ttu-id="eb1e4-287">Возвращает тип мультимедиа для кадров составного видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-287">Returns the media type of the composited video frames.</span></span> |
| [<span data-ttu-id="eb1e4-288">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-288">**ProcessMessage**</span></span>](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | <span data-ttu-id="eb1e4-289">Сигнализирует ведущему выполнять различные действия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-289">Signals the presenter to perform various actions.</span></span>      |



 

<span data-ttu-id="eb1e4-290">Метод [**жеткуррентмедиатипе**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) Возвращает тип мультимедиа выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-290">The [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) method returns the presenter's media type.</span></span> <span data-ttu-id="eb1e4-291">(Дополнительные сведения о настройке типа мультимедиа см. в разделе [Форматирование согласования](#negotiating-formats).) Тип носителя возвращается как указатель интерфейса [**имфвидеомедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-291">(For details about setting the media type, see [Negotiating Formats](#negotiating-formats).) The media type is returned as an [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) interface pointer.</span></span> <span data-ttu-id="eb1e4-292">В следующем примере предполагается, что выступающий хранит тип мультимедиа как указатель [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-292">The following example assumes that the presenter stores the media type as an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointer.</span></span> <span data-ttu-id="eb1e4-293">Чтобы получить интерфейс **имфвидеомедиатипе** из типа мультимедиа, вызовите метод **QueryInterface**:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-293">To get the **IMFVideoMediaType** interface from the media type, call **QueryInterface**:</span></span>


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="eb1e4-294">Метод [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) является основным механизмом для Евр взаимодействия с выступающим.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-294">The [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method is the primary mechanism for the EVR to communicate with the presenter.</span></span> <span data-ttu-id="eb1e4-295">Определены следующие сообщения.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-295">The following messages are defined.</span></span> <span data-ttu-id="eb1e4-296">Сведения о реализации каждого сообщения приведены в оставшейся части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-296">The details of implementing each message are given in the remainder of this topic.</span></span>



| <span data-ttu-id="eb1e4-297">Сообщение</span><span class="sxs-lookup"><span data-stu-id="eb1e4-297">Message</span></span>                                | <span data-ttu-id="eb1e4-298">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-298">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1e4-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-299">**MFVP_MESSAGE_INVALIDATEMEDIATYPE**</span></span> | <span data-ttu-id="eb1e4-300">Недопустимый тип выходного носителя микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-300">The mixer's output media type is invalid.</span></span> <span data-ttu-id="eb1e4-301">Выступающий должен согласовать новый тип мультимедиа с микшером.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-301">The presenter should negotiate a new media type with the mixer.</span></span> <span data-ttu-id="eb1e4-302">См. раздел [форматы согласования](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-302">See [Negotiating Formats](#negotiating-formats).</span></span>                                                                                         |
| <span data-ttu-id="eb1e4-303">**MFVP_MESSAGE_BEGINSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-303">**MFVP_MESSAGE_BEGINSTREAMING**</span></span>      | <span data-ttu-id="eb1e4-304">Потоковая передача начата.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-304">Streaming has started.</span></span> <span data-ttu-id="eb1e4-305">Это сообщение не требует определенных действий, но его можно использовать для выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-305">No particular action is required by this message, but you can use it to allocate resources.</span></span>                                                                                                                                 |
| <span data-ttu-id="eb1e4-306">**MFVP_MESSAGE_ENDSTREAMING**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-306">**MFVP_MESSAGE_ENDSTREAMING**</span></span>        | <span data-ttu-id="eb1e4-307">Потоковая передача завершена.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-307">Streaming has ended.</span></span> <span data-ttu-id="eb1e4-308">Освободите все ресурсы, выделенные в ответ на **MFVP_MESSAGE_BEGINSTREAMING** сообщение.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-308">Release any resources that you allocated in response to the **MFVP_MESSAGE_BEGINSTREAMING** message.</span></span>                                                                                                                        |
| <span data-ttu-id="eb1e4-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-309">**MFVP_MESSAGE_PROCESSINPUTNOTIFY**</span></span>  | <span data-ttu-id="eb1e4-310">Микшер получил новый входной пример и может создать новый выходной фрейм.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-310">The mixer has received a new input sample and might be able to generate a new output frame.</span></span> <span data-ttu-id="eb1e4-311">Выступающий должен вызвать [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в микшере.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-311">The presenter should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="eb1e4-312">См. раздел [Обработка выходных данных](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-312">See [Processing Output](#processing-output).</span></span> |
| <span data-ttu-id="eb1e4-313">**MFVP_MESSAGE_ENDOFSTREAM**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-313">**MFVP_MESSAGE_ENDOFSTREAM**</span></span>         | <span data-ttu-id="eb1e4-314">Презентация завершена.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-314">The presentation has ended.</span></span> <span data-ttu-id="eb1e4-315">См. [конец потока](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-315">See [End of Stream](#end-of-stream).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="eb1e4-316">**MFVP_MESSAGE_FLUSH**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-316">**MFVP_MESSAGE_FLUSH**</span></span>               | <span data-ttu-id="eb1e4-317">Евр очищает данные в конвейере отрисовки.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-317">The EVR is flushing the data in its rendering pipeline.</span></span> <span data-ttu-id="eb1e4-318">Выступающий должен отбросить все кадры видео, запланированные для презентации.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-318">The presenter should discard any video frames that are scheduled for presentation.</span></span>                                                                                                         |
| <span data-ttu-id="eb1e4-319">**MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-319">**MFVP_MESSAGE_STEP**</span></span>                | <span data-ttu-id="eb1e4-320">Запрашивает у выступающего на шаг вперед N кадров.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-320">Requests the presenter to step forward N frames.</span></span> <span data-ttu-id="eb1e4-321">Выступающий должен отбросить следующие N-1 кадра и отобразить значение n.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-321">The presenter should discard the next N-1 frames and display the Nth frame.</span></span> <span data-ttu-id="eb1e4-322">См. раздел [пошаговое выполнение](#frame-stepping).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-322">See [Frame Stepping](#frame-stepping).</span></span>                                                                                |
| <span data-ttu-id="eb1e4-323">**MFVP_MESSAGE_CANCELSTEP**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-323">**MFVP_MESSAGE_CANCELSTEP**</span></span>          | <span data-ttu-id="eb1e4-324">Отмена пошагового выполнения кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-324">Cancels frame stepping.</span></span>                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a><span data-ttu-id="eb1e4-325">Реализация Имфклоккстатесинк</span><span class="sxs-lookup"><span data-stu-id="eb1e4-325">Implementing IMFClockStateSink</span></span>

<span data-ttu-id="eb1e4-326">Выступающий должен реализовать интерфейс [**имфклоккстатесинк**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) как часть своей реализации [**имфвидеопресентер**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), которая наследует **имфклоккстатесинк**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-326">The presenter must implement the [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) interface as part of its implementation of [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), which inherits **IMFClockStateSink**.</span></span> <span data-ttu-id="eb1e4-327">Евр использует этот интерфейс для уведомления выступающего при каждом изменении состояния часов Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-327">The EVR uses this interface to notify the presenter whenever the EVR's clock changes state.</span></span> <span data-ttu-id="eb1e4-328">Дополнительные сведения о состояниях часов см. в статье [часы представления](presentation-clock.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-328">For more information about the clock states, see [Presentation Clock](presentation-clock.md).</span></span>

<span data-ttu-id="eb1e4-329">Ниже приведены некоторые рекомендации по реализации методов в этом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-329">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="eb1e4-330">При завершении работы Presenter все методы должны завершаться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-330">All of the methods should fail if the presenter is shut down.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb1e4-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>онклоккстарт</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-331"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="eb1e4-332">Установите состояние выступающего в значение Started.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-332">Set the presenter state to started.</span></span></li>
<li><span data-ttu-id="eb1e4-333">Если <em>ллклоккстартоффсет</em> не <strong>PRESENTATION_CURRENT_POSITION</strong>, очистите очередь выступающих образцов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-333">If the <em>llClockStartOffset</em> is not <strong>PRESENTATION_CURRENT_POSITION</strong>, flush the presenter's queue of samples.</span></span> <span data-ttu-id="eb1e4-334">(Это эквивалентно получению сообщения <strong>MFVP_MESSAGE_FLUSH</strong> .)</span><span class="sxs-lookup"><span data-stu-id="eb1e4-334">(This is equivalent to receiving an <strong>MFVP_MESSAGE_FLUSH</strong> message.)</span></span></li>
<li><span data-ttu-id="eb1e4-335">Если предыдущий запрос шага кадра все еще находится в состоянии ожидания, обработайте запрос (см. раздел <a href="#frame-stepping">пошаговое выполнение</a>).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-335">If a previous frame-step request is still pending, process the request (see <a href="#frame-stepping">Frame Stepping</a>).</span></span> <span data-ttu-id="eb1e4-336">В противном случае попробуйте обработать выходные данные микшера (см. раздел <a href="#processing-output">Обработка выходных данных</a>.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-336">Otherwise, try to process output from the mixer (see <a href="#processing-output">Processing Output</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb1e4-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>онклоккстоп</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-337"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="eb1e4-338">Установите состояние выступающего в значение Stopped.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-338">Set the presenter state to stopped.</span></span></li>
<li><span data-ttu-id="eb1e4-339">Очистка очереди выступающих образцов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-339">Flush the presenter's queue of samples.</span></span></li>
<li><span data-ttu-id="eb1e4-340">Отмените все ожидающие операции в кадрах.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-340">Cancel any pending frame-step operation.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb1e4-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>онклоккпаусе</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-341"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></span></span></td>
<td><span data-ttu-id="eb1e4-342">Установка состояния выступающего в состояние "приостановлено".</span><span class="sxs-lookup"><span data-stu-id="eb1e4-342">Set the presenter state to paused.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb1e4-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>онклоккрестарт</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-343"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></span></span></td>
<td><span data-ttu-id="eb1e4-344">Обрабатываются так же, как <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>онклоккстарт</strong></a> , но не удаляют очередь образцов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-344">Treat the same as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> but do not flush the queue of samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb1e4-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>онклокксетрате</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-345"><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="eb1e4-346">Если скорость меняется с нуля на ненулевой, отмените пошаговое выполнение кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-346">If the rate is changing from zero to nonzero, cancel frame stepping.</span></span></li>
<li><span data-ttu-id="eb1e4-347">Хранить новую ставку часов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-347">Store the new clock rate.</span></span> <span data-ttu-id="eb1e4-348">Частота представления зависят от часов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-348">The clock rate affects when samples are presented.</span></span> <span data-ttu-id="eb1e4-349">Дополнительные сведения см. в разделе <a href="#scheduling-samples">примеры планирования</a>.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-349">For more information, see <a href="#scheduling-samples">Scheduling Samples</a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a><span data-ttu-id="eb1e4-350">Реализация Имфратесуппорт</span><span class="sxs-lookup"><span data-stu-id="eb1e4-350">Implementing IMFRateSupport</span></span>

<span data-ttu-id="eb1e4-351">Чтобы обеспечить поддержку скорости воспроизведения, отличной от скорости 1 ×, выступающий должен реализовать интерфейс [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-351">To support playback rates other than 1× speed, the presenter must implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface.</span></span> <span data-ttu-id="eb1e4-352">Ниже приведены некоторые рекомендации по реализации методов в этом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-352">Here are some guidelines for implementing the methods in this interface.</span></span> <span data-ttu-id="eb1e4-353">После завершения работы Presenter все методы должны завершаться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-353">All of the methods should fail after the presenter is shut down.</span></span> <span data-ttu-id="eb1e4-354">Дополнительные сведения об этом интерфейсе см. в разделе [Rate Control](rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-354">For more information about this interface, see [Rate Control](rate-control.md).</span></span>



| <span data-ttu-id="eb1e4-355">Значение</span><span class="sxs-lookup"><span data-stu-id="eb1e4-355">Value</span></span>                                                          | <span data-ttu-id="eb1e4-356">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-356">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb1e4-357">**жетсловестрате**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-357">**GetSlowestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | <span data-ttu-id="eb1e4-358">Возвращает ноль, чтобы не указывать минимальную скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-358">Return zero to indicate no minimum playback rate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="eb1e4-359">**жетфастестрате**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-359">**GetFastestRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | <span data-ttu-id="eb1e4-360">При нетонком воспроизведении скорость воспроизведения не должна превышать частоту обновления монитора: *Максимальная* частота  =  *обновления* (Гц)/ *Частота кадров видео* (кадров/с).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-360">For non-thinned playback, the playback rate should not exceed the refresh rate of the monitor: *maximum rate* = *refresh rate* (Hz) / *video frame rate* (fps).</span></span> <span data-ttu-id="eb1e4-361">Частота кадров видео указывается в типе носителя выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-361">The video frame rate is specified in the presenter's media type.</span></span> <br/> <span data-ttu-id="eb1e4-362">Для тонкого воспроизведения скорость воспроизведения не ограничена; возвращайте значение **FLT_MAX**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-362">For thinned playback, the playback rate is unbounded; return the value **FLT_MAX**.</span></span> <span data-ttu-id="eb1e4-363">На практике источник и декодер будут ограничивающими факторами при тонком воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-363">In practice, the source and the decoder will be the limiting factors during thinned playback.</span></span> <br/> <span data-ttu-id="eb1e4-364">Для обратного воспроизведения возвратите отрицательное значение максимальной скорости.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-364">For reverse playback, return the negative of the maximum rate.</span></span><br/> |
| [<span data-ttu-id="eb1e4-365">**исратесуппортед**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-365">**IsRateSupported**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | <span data-ttu-id="eb1e4-366">Возвращает **MF_E_UNSUPPORTED_RATE** , если абсолютное значение *флрате* превышает максимальную скорость воспроизведения в выступающем.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-366">Return **MF_E_UNSUPPORTED_RATE** if the absolute value of *flRate* exceeds the presenter's maximum playback rate.</span></span> <span data-ttu-id="eb1e4-367">Вычислите максимальную скорость воспроизведения, как описано в [**жетфастестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-367">Calculate the maximum playback rate as described for [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).</span></span>                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="eb1e4-368">В следующем примере показано, как реализовать метод [**жетфастестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) :</span><span class="sxs-lookup"><span data-stu-id="eb1e4-368">The following example shows how to implement the [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) method:</span></span>


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



<span data-ttu-id="eb1e4-369">В предыдущем примере вызывается вспомогательный метод Жетмаксрате для вычисления максимальной скорости прямого воспроизведения:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-369">The previous example calls a helper method, GetMaxRate, to calculate the maximum forward playback rate:</span></span>

<span data-ttu-id="eb1e4-370">В следующем примере показано, как реализовать метод [**исратесуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) :</span><span class="sxs-lookup"><span data-stu-id="eb1e4-370">The following example shows how to implement the [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method:</span></span>


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a><span data-ttu-id="eb1e4-371">Отправка событий в Евр</span><span class="sxs-lookup"><span data-stu-id="eb1e4-371">Sending Events to the EVR</span></span>

<span data-ttu-id="eb1e4-372">Выступающий должен уведомлять Евр различных событий.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-372">The presenter must notify the EVR of various events.</span></span> <span data-ttu-id="eb1e4-373">Для этого используется интерфейс [**ИМЕДИАЕВЕНТСИНК**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) евр, полученный, когда Евр вызывает метод [**Имфтопологисервицелукупклиент:: инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-373">To do so, it uses the EVR's [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) interface, obtained when the EVR calls the presenter's [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) method.</span></span> <span data-ttu-id="eb1e4-374">(Интерфейс **имедиаевентсинк** изначально является интерфейсом DirectShow, но используется как в Евр DirectShow, так и в Media Foundation.) В следующем коде показано, как отправить событие в Евр:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-374">(The **IMediaEventSink** interface is originally a DirectShow interface, but is used in both the DirectShow EVR and the Media Foundation.) The following code shows how to send an event to the EVR:</span></span>


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



<span data-ttu-id="eb1e4-375">В следующей таблице перечислены события, отправляемые выступающим, а также параметры событий.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-375">The following table lists the events that the presenter sends, along with the event parameters.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb1e4-376">Событие</span><span class="sxs-lookup"><span data-stu-id="eb1e4-376">Event</span></span></th>
<th><span data-ttu-id="eb1e4-377">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-377">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb1e4-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-378"><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="eb1e4-379">Выступающий завершил отрисовку всех кадров после сообщения MFVP_MESSAGE_ENDOFSTREAM.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-379">The presenter has finished rendering all frames after the MFVP_MESSAGE_ENDOFSTREAM message.</span></span><br/>
<ul>
<li><span data-ttu-id="eb1e4-380"><em>Param1</em>: HRESULT, указывающий состояние операции.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-380"><em>Param1</em>: HRESULT indicating the status of the operation.</span></span></li>
<li><span data-ttu-id="eb1e4-381"><em>Param2</em>: не используется.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-381"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="eb1e4-382">Дополнительные сведения см. в разделе <a href="#end-of-stream">конец потока</a>.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-382">For more information, see <a href="#end-of-stream">End of Stream</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb1e4-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-383"><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></span></span></td>
<td><span data-ttu-id="eb1e4-384">Устройство Direct3D изменилось.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-384">The Direct3D device has changed.</span></span><br/>
<ul>
<li><span data-ttu-id="eb1e4-385"><em>Param1</em>: не используется.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-385"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="eb1e4-386"><em>Param2</em>: не используется.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-386"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="eb1e4-387">Дополнительные сведения см. <a href="#managing-the-direct3d-device">в разделе Управление устройством Direct3D</a>.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-387">For more information, see <a href="#managing-the-direct3d-device">Managing the Direct3D Device</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb1e4-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-388"><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></span></span></td>
<td><span data-ttu-id="eb1e4-389">Произошла ошибка, для которой требуется остановленная потоковая передача.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-389">An error has occurred that requires streaming to stop.</span></span><br/>
<ul>
<li><span data-ttu-id="eb1e4-390"><em>Param1</em>: <strong>HRESULT</strong> , указывающий возникшую ошибку.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-390"><em>Param1</em>: <strong>HRESULT</strong> indicating the error that occurred.</span></span></li>
<li><span data-ttu-id="eb1e4-391"><em>Param2</em>: не используется.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-391"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb1e4-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-392"><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="eb1e4-393">Указывает время, в течение которого выступающий готовится к просмотру каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-393">Specifies the amount of time that the presenter is taking to render each frame.</span></span> <span data-ttu-id="eb1e4-394">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="eb1e4-394">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="eb1e4-395"><em>Param1</em>: указатель на константное значение <strong>лонглонг</strong> , которое содержит количество времени для обработки кадра в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-395"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the amount of time to process the frame, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="eb1e4-396"><em>Param2</em>: не используется.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-396"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="eb1e4-397">Дополнительные сведения см. в разделе <a href="#processing-output">Обработка выходных данных</a>.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-397">For more information, see <a href="#processing-output">Processing Output</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb1e4-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-398"><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></span></span></td>
<td><span data-ttu-id="eb1e4-399">Указывает текущее время запаздывания в примерах отрисовки.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-399">Specifies the current lag time in rendering samples.</span></span> <span data-ttu-id="eb1e4-400">Если значение положительное, выборка отстает от расписания.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-400">If the value is positive, samples are behind schedule.</span></span> <span data-ttu-id="eb1e4-401">Если значение отрицательное, выборки выполняются заранее по расписанию.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-401">If the value is negative, samples are ahead of schedule.</span></span> <span data-ttu-id="eb1e4-402">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="eb1e4-402">(Optional.)</span></span><br/>
<ul>
<li><span data-ttu-id="eb1e4-403"><em>Param1</em>: указатель на константное значение <strong>лонглонг</strong> , которое содержит время запаздывания в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-403"><em>Param1</em>: Pointer to a constant <strong>LONGLONG</strong> value that contains the lag time, in 100-nanosecond units.</span></span></li>
<li><span data-ttu-id="eb1e4-404"><em>Param2</em>: не используется.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-404"><em>Param2</em>: Not used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb1e4-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-405"><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></span></span></td>
<td><span data-ttu-id="eb1e4-406">Отправляется сразу после <strong>EC_STEP_COMPLETE</strong> , если скорость воспроизведения равна нулю.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-406">Sent immediately after <strong>EC_STEP_COMPLETE</strong> if the playback rate is zero.</span></span> <span data-ttu-id="eb1e4-407">Это событие содержит метку времени отображаемого кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-407">This event contains the time stamp of the frame that was displayed.</span></span><br/>
<ul>
<li><span data-ttu-id="eb1e4-408"><em>Param1</em>: младшие 32 бит метки времени.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-408"><em>Param1</em>: Lower 32 bits of the time stamp.</span></span></li>
<li><span data-ttu-id="eb1e4-409"><em>Param2</em>: верхний 32 бит метки времени.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-409"><em>Param2</em>: Upper 32 bits of the time stamp.</span></span></li>
</ul>
<span data-ttu-id="eb1e4-410">Дополнительные сведения см. в разделе <a href="#frame-stepping">пошаговая отладка кадров</a>.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-410">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb1e4-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eb1e4-411"><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></span></span></td>
<td><span data-ttu-id="eb1e4-412">Выступающий завершил или отменил шаг кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-412">The presenter has completed or canceled a frame step.</span></span><br/>
<ul>
<li><span data-ttu-id="eb1e4-413"><em>Param1</em>: не используется.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-413"><em>Param1</em>: Not used.</span></span></li>
<li><span data-ttu-id="eb1e4-414"><em>Param2</em>: не используется.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-414"><em>Param2</em>: Not used.</span></span></li>
</ul>
<span data-ttu-id="eb1e4-415">Дополнительные сведения см. в разделе <a href="#frame-stepping">пошаговая отладка кадров</a>.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-415">For more information, see <a href="#frame-stepping">Frame Stepping</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eb1e4-416">Предыдущая версия документации неправильно описывала параметр <em>param1</em> .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-416">A previous version of the documentation described <em>Param1</em> incorrectly.</span></span> <span data-ttu-id="eb1e4-417">Этот параметр не используется для этого события.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-417">This parameter is not used for this event.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a><span data-ttu-id="eb1e4-418">Форматы согласования</span><span class="sxs-lookup"><span data-stu-id="eb1e4-418">Negotiating Formats</span></span>

<span data-ttu-id="eb1e4-419">Всякий раз, когда выступающий получает сообщение **MFVP_MESSAGE_INVALIDATEMEDIATYPE** из евр, оно должно задать выходной формат для микшера следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-419">Whenever the presenter receives an **MFVP_MESSAGE_INVALIDATEMEDIATYPE** message from the EVR, it must set the output format on the mixer, as follows:</span></span>

1.  <span data-ttu-id="eb1e4-420">Вызовите [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) в микшере, чтобы получить возможный тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-420">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) on the mixer to get a possible output type.</span></span> <span data-ttu-id="eb1e4-421">Этот тип описывает формат, который микшер может создать при наличии входных потоков и возможностей обработки видео графического устройства.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-421">This type describes a format that the mixer can produce given the input streams and the video processing capabilities of the graphics device.</span></span>
2.  <span data-ttu-id="eb1e4-422">Проверьте, может ли выступающий использовать этот тип мультимедиа в качестве формата подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-422">Check whether the presenter can use this media type as its rendering format.</span></span> <span data-ttu-id="eb1e4-423">Ниже приведены некоторые вещи, которые необходимо проверить, хотя реализация может иметь собственные требования.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-423">Here are some things to check, although your implementation might have its own requirements:</span></span>

    -   <span data-ttu-id="eb1e4-424">Видео должно быть распаковано.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-424">The video must be uncompressed.</span></span>
    -   <span data-ttu-id="eb1e4-425">В видео должны быть только прогрессивные кадры.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-425">The video must have progressive frames only.</span></span> <span data-ttu-id="eb1e4-426">Убедитесь, что атрибут [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) равен **MFVideoInterlace_Progressive**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-426">Check that the [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) attribute equals **MFVideoInterlace_Progressive**.</span></span>
    -   <span data-ttu-id="eb1e4-427">Формат должен быть совместим с устройством Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-427">The format must be compatible with the Direct3D device.</span></span>

    <span data-ttu-id="eb1e4-428">Если тип неприемлем, вернитесь к шагу 1 и получите следующий предложенный тип микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-428">If the type is not acceptable, return to step 1 and get the mixer's next proposed type.</span></span>

3.  <span data-ttu-id="eb1e4-429">Создайте новый тип мультимедиа, который является клоном исходного типа, а затем измените следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-429">Create a new media type that is a clone of the original type and then change the following attributes:</span></span>

    -   <span data-ttu-id="eb1e4-430">Присвойте атрибуту [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) значение, равное ширине и высоте, которые будут выделяться для поверхностей Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-430">Set the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute equal to the width and height that you want for the Direct3D surfaces you will allocate.</span></span>
    -   <span data-ttu-id="eb1e4-431">Присвойте [](mf-mt-pan-scan-enabled-attribute.md) атрибуту MF_MT_PAN_SCAN_ENABLED **значение false**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-431">Set the [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **FALSE**.</span></span>
    -   <span data-ttu-id="eb1e4-432">Установите атрибут [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) РАВНым номиналу дисплея (обычно 1:1).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-432">Set the [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute equal to the PAR of the display (typically 1:1).</span></span>
    -   <span data-ttu-id="eb1e4-433">Установите геометрическое апертуру ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) атрибут) равным прямоугольнику в области Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-433">Set the geometric aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) attribute) equal to a rectangle within the Direct3D surface.</span></span> <span data-ttu-id="eb1e4-434">Когда микшер создает выходной кадр, он блитс исходный образ на этот прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-434">When the mixer generates an output frame, it blits the source image onto this rectangle.</span></span> <span data-ttu-id="eb1e4-435">Геометрическое Апертура может быть большим, чем поверхность, или подпрямоугольником внутри области.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-435">The geometric aperture can be as large as the surface, or it can be a subrectangle within the surface.</span></span> <span data-ttu-id="eb1e4-436">Дополнительные сведения см. в разделе [прямоугольники источника и назначения](#source-and-destination-rectangles).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-436">For more information, see [Source and Destination Rectangles](#source-and-destination-rectangles).</span></span>

4.  <span data-ttu-id="eb1e4-437">Чтобы проверить, примет ли микшер измененный тип вывода, вызовите [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) с флагом **MFT_SET_TYPE_TEST_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-437">To test whether the mixer will accept the modified output type, call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with the **MFT_SET_TYPE_TEST_ONLY** flag.</span></span> <span data-ttu-id="eb1e4-438">Если микшер отклоняет тип, вернитесь к шагу 1 и получите следующий тип.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-438">If the mixer rejects the type, go back to step 1 and get the next type.</span></span>
5.  <span data-ttu-id="eb1e4-439">Выделите пул поверхностей Direct3D, как описано в разделе [выделение поверхностей Direct3D](#allocating-direct3d-surfaces).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-439">Allocate a pool of Direct3D surfaces, as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="eb1e4-440">Микшер будет использовать эти поверхности при рисовании составных кадров видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-440">The mixer will use these surfaces when it draws the composited video frames.</span></span>
6.  <span data-ttu-id="eb1e4-441">Задайте тип выходных данных микшера, вызвав [**сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) без флагов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-441">Set the output type on the mixer by calling [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) with no flags.</span></span> <span data-ttu-id="eb1e4-442">Если в шаге 4 первый вызов **сетаутпуттипе** завершился удачно, метод должен пройти повторно.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-442">If the first call to **SetOutputType** succeeded in step 4, the method should succeed again.</span></span>

<span data-ttu-id="eb1e4-443">Если микшер выполняется из типов, метод [**жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) возвращает **MF_E_NO_MORE_TYPES**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-443">If the mixer runs out of types, the [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method returns **MF_E_NO_MORE_TYPES**.</span></span> <span data-ttu-id="eb1e4-444">Если выступающий не может найти подходящий тип выходных данных для микшера, поток не может быть визуализирован.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-444">If the presenter cannot find a suitable output type for the mixer, the stream cannot be rendered.</span></span> <span data-ttu-id="eb1e4-445">В этом случае DirectShow или Media Foundation могут использовать другой формат потока.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-445">In that case, DirectShow or Media Foundation might try another stream format.</span></span> <span data-ttu-id="eb1e4-446">Таким образом, выступающий может получить несколько **MFVP_MESSAGE_INVALIDATEMEDIATYPE** сообщений в строке, пока не будет найден допустимый тип.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-446">Therefore, the presenter might receive several **MFVP_MESSAGE_INVALIDATEMEDIATYPE** messages in a row until a valid type is found.</span></span>

<span data-ttu-id="eb1e4-447">Микшер автоматически леттербоксес видео, принимая во внимание пропорцию пикселя (номинал) источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-447">The mixer automatically letterboxes the video, taking into account the pixel aspect ratio (PAR) of the source and destination.</span></span> <span data-ttu-id="eb1e4-448">Для достижения лучших результатов ширина и высота поверхности и геометрический апертуры должны быть равны фактическому размеру, который должен отображаться на экране.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-448">For best results, the surface width and height and the geometric aperture should be equal to the actual size that you want the video to appear on the display.</span></span> <span data-ttu-id="eb1e4-449">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-449">The following image illustrates this process.</span></span>

![Схема, демонстрирующая составной Фрам, ведущей к поверхности Direct3D, которая ведет к окну](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

<span data-ttu-id="eb1e4-451">В следующем коде показана структура процесса.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-451">The following code shows the outline of the process.</span></span> <span data-ttu-id="eb1e4-452">Некоторые шаги помещаются в вспомогательные функции, подробные сведения о которых будут зависеть от требований вашего Presenter.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-452">Some of the steps are placed in helper functions, the exact details of which will depend on the requirements of your presenter.</span></span>


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



<span data-ttu-id="eb1e4-453">Дополнительные сведения о типах мультимедиа см. в статье [типы видеороликов](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-453">For more information about video media types, see [Video Media Types](video-media-types.md).</span></span>

## <a name="managing-the-direct3d-device"></a><span data-ttu-id="eb1e4-454">Управление устройством Direct3D</span><span class="sxs-lookup"><span data-stu-id="eb1e4-454">Managing the Direct3D Device</span></span>

<span data-ttu-id="eb1e4-455">Выступающий создает устройство Direct3D и обрабатывает потери устройств во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-455">The presenter creates the Direct3D device and handles any device loss during streaming.</span></span> <span data-ttu-id="eb1e4-456">В выступающих также размещается Диспетчер устройств Direct3D, который предоставляет другим компонентам возможность использовать одно и то же устройство.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-456">The presenter also hosts the Direct3D device manager, which provides a way for other components to use the same device.</span></span> <span data-ttu-id="eb1e4-457">Например, микшер использует устройство Direct3D для смешивания подпотоков, дечередования и настройки цветов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-457">For example, the mixer uses the Direct3D device to mix substreams, deinterlace, and perform color adjustments.</span></span> <span data-ttu-id="eb1e4-458">Декодеры могут использовать устройство Direct3D для декодирования с помощью ускорения видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-458">Decoders can use the Direct3D device for video-accelerated decoding.</span></span> <span data-ttu-id="eb1e4-459">(Дополнительные сведения об ускорении видео см. в статье [DirectX Video ускорение 2,0](directx-video-acceleration-2-0.md).)</span><span class="sxs-lookup"><span data-stu-id="eb1e4-459">(For more information about video acceleration, see [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)</span></span>

<span data-ttu-id="eb1e4-460">Чтобы настроить устройство Direct3D, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-460">To set up the Direct3D device, perform the following steps:</span></span>

1.  <span data-ttu-id="eb1e4-461">Создайте объект Direct3D, вызвав **Direct3DCreate9** или **Direct3DCreate9Ex**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-461">Create the Direct3D object by calling **Direct3DCreate9** or **Direct3DCreate9Ex**.</span></span>
2.  <span data-ttu-id="eb1e4-462">Создайте устройство, вызвав **IDirect3D9:: креатедевице** или **IDirect3D9Ex:: креатедевице**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-462">Create the device by calling **IDirect3D9::CreateDevice** or **IDirect3D9Ex::CreateDevice**.</span></span>
3.  <span data-ttu-id="eb1e4-463">Создайте диспетчер устройств, вызвав [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-463">Create the device manager by calling [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span>
4.  <span data-ttu-id="eb1e4-464">Настройте устройство в диспетчере устройств, вызвав [**IDirect3DDeviceManager9:: ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-464">Set the device on the device manager by calling [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span>

<span data-ttu-id="eb1e4-465">Если другому компоненту конвейера требуется диспетчер устройств, он вызывает [**имфжетсервице::**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Евр в, указывая **MR_VIDEO_ACCELERATION_SERVICE** для идентификатора GUID службы.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-465">If another pipeline component needs the device manager, it calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the EVR, specifying **MR_VIDEO_ACCELERATION_SERVICE** for the service GUID.</span></span> <span data-ttu-id="eb1e4-466">Евр передает запрос выступающему.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-466">The EVR passes the request to the presenter.</span></span> <span data-ttu-id="eb1e4-467">После того как объект получает указатель [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) , он может получить маркер устройства, вызвав [**IDirect3DDeviceManager9:: опендевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-467">After the object gets the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pointer, it can get a handle to the device by calling [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle).</span></span> <span data-ttu-id="eb1e4-468">Когда объекту требуется использовать устройство, он передает его методу [**IDirect3DDeviceManager9:: локкдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) , который возвращает указатель **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-468">When the object needs to use the device, it passes the device handle to the [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method, which returns an **IDirect3DDevice9** pointer.</span></span>

<span data-ttu-id="eb1e4-469">Если после создания устройства выступающий уничтожает устройство и создает новый, он должен вызвать [**ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) еще раз.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-469">After the device is created, if the presenter destroys the device and creates a new one, the presenter must call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) again.</span></span> <span data-ttu-id="eb1e4-470">Метод **ресетдевице** делает недействительными все существующие дескрипторы устройств, что приводит к возвращению [**локкдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) **DXVA2_E_NEW_VIDEO_DEVICE**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-470">The **ResetDevice** method invalidates any existing device handles, which causes [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) to return **DXVA2_E_NEW_VIDEO_DEVICE**.</span></span> <span data-ttu-id="eb1e4-471">Этот код ошибки сигнализирует другим объектам с помощью устройства, что им следует открыть новый обработчик устройства.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-471">This error code signals to other objects using the device that they should open a new device handle.</span></span> <span data-ttu-id="eb1e4-472">Дополнительные сведения об использовании диспетчера устройств см. в разделе [Direct3D Диспетчер устройств](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-472">For more information about using the device manager, see [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="eb1e4-473">Выступающий может создать устройство в оконном режиме или в полноэкранном режиме монопольного доступа.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-473">The presenter can create the device in windowed mode or full-screen exclusive mode.</span></span> <span data-ttu-id="eb1e4-474">Для оконного режима следует предоставить приложению способ указания окна видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-474">For windowed mode, you should provide a way for the application to specify the video window.</span></span> <span data-ttu-id="eb1e4-475">Стандартный выступающий реализует метод [**имфвидеодисплайконтрол:: сетвидеовиндов**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) для этой цели.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-475">The standard presenter implements the [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) method for this purpose.</span></span> <span data-ttu-id="eb1e4-476">Необходимо создать устройство при первом создании Presenter.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-476">You must create the device when the presenter is first created.</span></span> <span data-ttu-id="eb1e4-477">Как правило, в настоящее время вы не узнаете все параметры устройства, например окно или формат заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-477">Typically, you won't know all of the device parameters at this time, such as the window or the back buffer format.</span></span> <span data-ttu-id="eb1e4-478">Вы можете создать временное устройство и заменить его позже&\# . просто не забудьте вызвать [**ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) в диспетчере устройств.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-478">You can create a temporary device and replace it later&\#;just remember to call [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) on the device manager.</span></span>

<span data-ttu-id="eb1e4-479">Если вы создаете новое устройство или вызываете **IDirect3DDevice9:: Reset** или **IDirect3DDevice9Ex:: ресетекс** на существующем устройстве, отправьте событие [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) в Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-479">If you create a new device, or if you call **IDirect3DDevice9::Reset** or **IDirect3DDevice9Ex::ResetEx** on an existing device, send an [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) event to the EVR.</span></span> <span data-ttu-id="eb1e4-480">Это событие уведомляет Евр о необходимости повторного согласования типа носителя.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-480">This event notifies the EVR to renegotiate the media type.</span></span> <span data-ttu-id="eb1e4-481">Евр игнорирует параметры события для этого события.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-481">The EVR ignores the event parameters for this event.</span></span>

### <a name="allocating-direct3d-surfaces"></a><span data-ttu-id="eb1e4-482">Выделение поверхностей Direct3D</span><span class="sxs-lookup"><span data-stu-id="eb1e4-482">Allocating Direct3D Surfaces</span></span>

<span data-ttu-id="eb1e4-483">После того как выступающий задает тип мультимедиа, он может выделить поверхности Direct3D, которые микшер будет использовать для записи кадров видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-483">After the presenter sets the media type, it can allocate the Direct3D surfaces, which the mixer will use to write the video frames.</span></span> <span data-ttu-id="eb1e4-484">Поверхность должна соответствовать типу мультимедиа выступающего:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-484">The surface must match the presenter's media type:</span></span>

-   <span data-ttu-id="eb1e4-485">Формат поверхности должен соответствовать подтипу носителя.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-485">The surface format must match the media subtype.</span></span> <span data-ttu-id="eb1e4-486">Например, если подтип имеет значение **MFVideoFormat_RGB24**, формат поверхности должен быть **D3DFMT_X8R8G8B8**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-486">For example, if the subtype is **MFVideoFormat_RGB24**, the surface format must be **D3DFMT_X8R8G8B8**.</span></span> <span data-ttu-id="eb1e4-487">Дополнительные сведения о подтипах и форматах Direct3D см. в разделе [GUID подтипов видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-487">For more information about subtypes and Direct3D formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="eb1e4-488">Ширина и высота поверхности должны соответствовать измерениям, заданным в атрибуте [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-488">The surface width and height must match the dimensions given in the [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) attribute of the media type.</span></span>

<span data-ttu-id="eb1e4-489">Рекомендуемый способ распределения поверхностей зависит от того, выполняется ли в окне полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-489">The recommended way to allocate surfaces depends on whether the presenter runs windowed or full-screen.</span></span>

<span data-ttu-id="eb1e4-490">Если устройство Direct3D является оконным, можно создать несколько цепочек подкачки, каждый из которых имеет один задний буфер.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-490">If the Direct3D device is windowed, you can create several swap chains, each with a single back buffer.</span></span> <span data-ttu-id="eb1e4-491">Используя этот подход, можно отдельно представлять каждую поверхность, так как представление одной цепочки подкачки не мешает другим цепочкам подкачки.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-491">Using this approach, you can present each surface independently, because presenting one swap chain will not interfere with the other swap chains.</span></span> <span data-ttu-id="eb1e4-492">Микшер может записывать данные на поверхность, в то время как на другую поверхность планируется презентация.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-492">The mixer can write data to a surface while another surface is scheduled for presentation.</span></span>

<span data-ttu-id="eb1e4-493">Сначала определите, сколько цепочек подкачки следует создать.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-493">First, decide how many swap chains to create.</span></span> <span data-ttu-id="eb1e4-494">Рекомендуется как минимум три.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-494">A minimum of three is recommended.</span></span> <span data-ttu-id="eb1e4-495">Для каждой цепочки подкачки выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-495">For each swap chain, do the following:</span></span>

1.  <span data-ttu-id="eb1e4-496">Вызовите метод **IDirect3DDevice9:: креатеаддитионалсвапчаин** , чтобы создать цепочку буферов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-496">Call **IDirect3DDevice9::CreateAdditionalSwapChain** to create the swap chain.</span></span>
2.  <span data-ttu-id="eb1e4-497">Вызовите **IDirect3DSwapChain9:: жетбаккбуффер** , чтобы получить указатель на поверхность буфера обратной цепочки.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-497">Call **IDirect3DSwapChain9::GetBackBuffer** to get a pointer to the swap chain's back buffer surface.</span></span>
3.  <span data-ttu-id="eb1e4-498">Вызовите [**мфкреатевидеосамплефромсурфаце**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) и передайте указатель на поверхность.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-498">Call [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) and pass in a pointer to the surface.</span></span> <span data-ttu-id="eb1e4-499">Эта функция возвращает указатель на видеообъект образца видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-499">This function returns a pointer to a video sample object.</span></span> <span data-ttu-id="eb1e4-500">Пример объекта Video реализует интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , и он использует этот интерфейс для передачи поверхности в микшер, когда выступающий вызывает метод микшера [**Имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-500">The video sample object implements the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, and the presenter uses this interface to deliver the surface to the mixer when the presenter calls the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="eb1e4-501">Дополнительные сведения об объекте видео Sample см. в разделе [образцы видео](video-samples.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-501">For more information about the video sample object, see [Video Samples](video-samples.md).</span></span>
4.  <span data-ttu-id="eb1e4-502">Сохранение указателя [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) в очереди.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-502">Store the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer in a queue.</span></span> <span data-ttu-id="eb1e4-503">Выступающие выводит примеры из этой очереди во время обработки, как описано в разделе [Обработка выходных данных](#processing-output).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-503">The presenter will pull samples from this queue during processing as described in [Processing Output](#processing-output).</span></span>
5.  <span data-ttu-id="eb1e4-504">Сохраняет ссылку на указатель **IDirect3DSwapChain9** , чтобы цепочка буферов не была освобождена.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-504">Keep a reference to the **IDirect3DSwapChain9** pointer so the swap chain is not released.</span></span>

<span data-ttu-id="eb1e4-505">В полноэкранном монопольном режиме устройство не может иметь более одной цепочки буферов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-505">In full-screen exclusive mode, the device cannot have more than one swap chain.</span></span> <span data-ttu-id="eb1e4-506">Эта цепочка буфера обмена создается неявно при создании полноэкранного устройства.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-506">This swap chain is created implicitly when you create the full-screen device.</span></span> <span data-ttu-id="eb1e4-507">Цепочка буферов может иметь более одного заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-507">The swap chain can have more than one back buffer.</span></span> <span data-ttu-id="eb1e4-508">К сожалению, тем не менее, если вы предоставляете один задний буфер во время записи в другой задний буфер в той же цепочке буферов, нет простого способа координировать две операции.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-508">Unfortunately, however, if you present one back buffer while you write to another back buffer in the same swap chain, there is no easy way to coordinate the two operations.</span></span> <span data-ttu-id="eb1e4-509">Это обусловлено тем, как Direct3D реализует перелистывание поверхностей.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-509">This is because of the way Direct3D implements surface flipping.</span></span> <span data-ttu-id="eb1e4-510">При вызове Present драйвер графики обновляет указатели поверхности в графической памяти.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-510">When you call Present, the graphics driver updates the surface pointers in graphics memory.</span></span> <span data-ttu-id="eb1e4-511">Если при вызове **присутствовали** указатели **IDirect3DSurface9** , они будут указывать на различные буферы после возврата **текущего** вызова.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-511">If you are holding any **IDirect3DSurface9** pointers when you call **Present**, they will point to different buffers after the **Present** call returns.</span></span>

<span data-ttu-id="eb1e4-512">Самый простой вариант — создать один видеопример для цепочки буферов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-512">The simplest option is to create one video sample for the swap chain.</span></span> <span data-ttu-id="eb1e4-513">Если выбран этот параметр, выполните те же действия, что и для оконного режима.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-513">If you choose this option, follow the same steps given for windowed mode.</span></span> <span data-ttu-id="eb1e4-514">Единственное отличие состоит в том, что пример очереди содержит один пример видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-514">The only difference is that the sample queue contains a single video sample.</span></span> <span data-ttu-id="eb1e4-515">Другой вариант — создать поверхностные поверхности, а затем Блит их в задний буфер.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-515">Another option is to create offscreen surfaces and then blit them to the back buffer.</span></span> <span data-ttu-id="eb1e4-516">Создаваемые поверхности должны поддерживать метод [**идиректксвидеопроцессор:: видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) , который микшер использует для совмещения выходных кадров.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-516">The surfaces that you create must support the [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method, which the mixer uses to composite the output frames.</span></span>

### <a name="tracking-samples"></a><span data-ttu-id="eb1e4-517">Примеры. Отслеживание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-517">Tracking Samples</span></span>

<span data-ttu-id="eb1e4-518">Когда выступающий сначала выделяет образцы видео, он помещает их в очередь.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-518">When the presenter first allocates the video samples, it places them in a queue.</span></span> <span data-ttu-id="eb1e4-519">Выступающий рисует из этой очереди каждый раз, когда ему нужно получить новый кадр из микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-519">The presenter draws from this queue whenever it needs to get a new frame from the mixer.</span></span> <span data-ttu-id="eb1e4-520">Когда микшер выводит кадр, он перемещает пример во вторую очередь.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-520">After the mixer outputs the frame, the presenter moves the sample into a second queue.</span></span> <span data-ttu-id="eb1e4-521">Вторая очередь предназначена для выборок, ожидающих времени показа по расписанию.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-521">The second queue is for samples that are waiting for their scheduled presentation times.</span></span>

<span data-ttu-id="eb1e4-522">Чтобы упростить отслеживание состояния каждого образца, объект видео Sample реализует интерфейс [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-522">To make it easier to track the status of each sample, the video sample object implements the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span> <span data-ttu-id="eb1e4-523">Этот интерфейс можно использовать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-523">You can use this interface as follows:</span></span>

1.  <span data-ttu-id="eb1e4-524">Реализуйте интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) в вашем выступающем.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-524">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface in your presenter.</span></span>
2.  <span data-ttu-id="eb1e4-525">Перед тем как поместить пример в очередь по расписанию, запросите объект видео Sample для интерфейса [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-525">Before you place a sample in the scheduled queue, query the video sample object for the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) interface.</span></span>

3.  <span data-ttu-id="eb1e4-526">Вызовите [**имфтраккедсампле:: сеталлокатор**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) с указателем на интерфейс обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-526">Call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) with a pointer to your callback interface.</span></span>
4.  <span data-ttu-id="eb1e4-527">Когда образец готов к показу, удалите его из очереди запланированных, приготовьте его и освободите все ссылки на этот пример.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-527">When the sample is ready for presentation, remove it from the scheduled queue, present it, and release all references to the sample.</span></span>
5.  <span data-ttu-id="eb1e4-528">В примере вызывается обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-528">The sample invokes the callback.</span></span> <span data-ttu-id="eb1e4-529">(Образец объекта в этом случае не удаляется, так как он содержит счетчик ссылок на себя до вызова обратного вызова.)</span><span class="sxs-lookup"><span data-stu-id="eb1e4-529">(The sample object is not deleted in this case because it holds a reference count on itself until the callback is invoked.)</span></span>
6.  <span data-ttu-id="eb1e4-530">В обратном вызове верните пример в доступную очередь.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-530">Inside the callback, return the sample to the available queue.</span></span>

<span data-ttu-id="eb1e4-531">Выступающий не требуется использовать [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) для наблюдения за примерами; можно реализовать любой метод, который лучше подходит для вашего проекта.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-531">A presenter is not required to use [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) to track samples; you can implement any technique that works best for your design.</span></span> <span data-ttu-id="eb1e4-532">Одно из преимуществ **имфтраккедсампле** заключается в том, что функции планирования и подготовки выступающего можно переместить в вспомогательные объекты, и для этих объектов не требуется специальный механизм для обратного вызова к выступающему, когда они выпускают образцы видео, так как пример объекта предоставляет этот механизм.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-532">One advantage of **IMFTrackedSample** is that you can move the presenter's scheduling and rendering functions into helper objects, and these objects do not need any special mechanism for calling back to the presenter when they release video samples because the sample object provides that mechanism.</span></span>

<span data-ttu-id="eb1e4-533">В следующем коде показано, как задать обратный вызов:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-533">The following code shows how to set the callback:</span></span>


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



<span data-ttu-id="eb1e4-534">В обратном вызове вызовите [**имфасинкресулт:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) в объекте асинхронного результата, чтобы получить указатель на образец:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-534">In the callback, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) on the asynchronous result object to retrieve a pointer to the sample:</span></span>


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock ***/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /*** End lock ***/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a><span data-ttu-id="eb1e4-535">Обработка выходных данных</span><span class="sxs-lookup"><span data-stu-id="eb1e4-535">Processing Output</span></span>

<span data-ttu-id="eb1e4-536">Каждый раз, когда микшер получает новый входной пример, ЕВР отправляет выступающее сообщение **MFVP_MESSAGE_PROCESSINPUTNOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-536">Whenever the mixer receives a new input sample, the EVR sends an **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message to the presenter.</span></span> <span data-ttu-id="eb1e4-537">Это сообщение означает, что микшер может иметь новый кадр видео для доставки.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-537">This message indicates that the mixer might have a new video frame to deliver.</span></span> <span data-ttu-id="eb1e4-538">В ответ выступающий вызывает [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в микшере.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-538">In response, the presenter calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="eb1e4-539">Если метод будет выполнен, выступающий планирует пример для презентации.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-539">If the method succeeds, the presenter schedules the sample for presentation.</span></span>

<span data-ttu-id="eb1e4-540">Чтобы получить выходные данные микшера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-540">To get output from the mixer, perform the following steps:</span></span>

1.  <span data-ttu-id="eb1e4-541">Проверьте состояние часов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-541">Check the clock state.</span></span> <span data-ttu-id="eb1e4-542">Если часы приостановлены, пропустите **MFVP_MESSAGE_PROCESSINPUTNOTIFY** сообщение, если это не первый кадр видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-542">If the clock is paused, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message unless this is the first video frame.</span></span> <span data-ttu-id="eb1e4-543">Если часы выполняются или если это первый кадр видео, продолжайте.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-543">If the clock is running, or if this is the first video frame, continue.</span></span>
2.  <span data-ttu-id="eb1e4-544">Получите пример из очереди доступных образцов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-544">Get a sample from the queue of available samples.</span></span> <span data-ttu-id="eb1e4-545">Если очередь пуста, это означает, что все выделенные образцы в настоящее время запланированы для показа.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-545">If the queue is empty, it means that all allocated samples are currently scheduled for presenting.</span></span> <span data-ttu-id="eb1e4-546">В этом случае проигнорируйте сообщение **MFVP_MESSAGE_PROCESSINPUTNOTIFY** в данный момент.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-546">In that case, ignore the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message at this time.</span></span> <span data-ttu-id="eb1e4-547">Когда следующий образец станет доступным, повторите приведенные здесь действия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-547">When the next sample becomes available, repeat the steps listed here.</span></span>
3.  <span data-ttu-id="eb1e4-548">(Необязательно.) Если часы доступны, получите текущее время (*T1*), вызвав [**Имфклокк:: жеткоррелатедтиме**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-548">(Optional.) If the clock is available, get the current clock time (*T1*) by calling [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span>
4.  <span data-ttu-id="eb1e4-549">Вызовите [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в микшере.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-549">Call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span> <span data-ttu-id="eb1e4-550">Если **ProcessOutput** выполнена, пример содержит видеокадр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-550">If **ProcessOutput** succeeds, the sample contains a video frame.</span></span> <span data-ttu-id="eb1e4-551">Если метод завершается ошибкой, проверьте код возврата.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-551">If the method fails, check the return code.</span></span> <span data-ttu-id="eb1e4-552">Следующие коды ошибок от **ProcessOutput** не являются критическими сбоями:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-552">The following error codes from **ProcessOutput** are not critical failures:</span></span>

    

    | <span data-ttu-id="eb1e4-553">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="eb1e4-553">Error code</span></span>                              | <span data-ttu-id="eb1e4-554">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-554">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="eb1e4-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-555">**MF_E_TRANSFORM_NEED_MORE_INPUT**</span></span> | <span data-ttu-id="eb1e4-556">Перед созданием нового выходного фрейма для микшера требуется больше входных данных.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-556">The mixer needs more input before it can produce a new output frame.</span></span><br/> <span data-ttu-id="eb1e4-557">Если вы получаете этот код ошибки, проверьте, достиг ли Евр конца потока и отвечайте соответствующим образом, как описано в [конце потока](#end-of-stream).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-557">If you get this error code, check whether the EVR has reached the end of the stream and respond accordingly, as described in [End of Stream](#end-of-stream).</span></span> <span data-ttu-id="eb1e4-558">В противном случае пропустите это **MF_E_TRANSFORM_NEED_MORE_INPUT** сообщение.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-558">Otherwise, ignore this **MF_E_TRANSFORM_NEED_MORE_INPUT** message.</span></span> <span data-ttu-id="eb1e4-559">Евр отправит еще один, когда микшер получит больше входных данных.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-559">The EVR will send another one when the mixer gets more input.</span></span><br/> |
    | <span data-ttu-id="eb1e4-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-560">**MF_E_TRANSFORM_STREAM_CHANGE**</span></span>    | <span data-ttu-id="eb1e4-561">Тип выходных данных микшера стал недопустимым, возможно, из-за изменения формата.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-561">The mixer's output type has become invalid, possibly due to a format change upstream.</span></span><br/> <span data-ttu-id="eb1e4-562">Если вы получаете этот код ошибки, установите для типа мультимедиа в качестве носителя **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-562">If you get this error code, set the presenter's media type to **NULL**.</span></span> <span data-ttu-id="eb1e4-563">Евр будет запрашивать новый формат.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-563">The EVR will request a new format.</span></span><br/>                                                                                                                                                                         |
    | <span data-ttu-id="eb1e4-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-564">**MF_E_TRANSFORM_TYPE_NOT_SET**</span></span>    | <span data-ttu-id="eb1e4-565">Для микшера требуется новый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-565">The mixer requires a new media type.</span></span><br/> <span data-ttu-id="eb1e4-566">Если вы получаете этот код ошибки, повторно согласовывайте тип вывода микшера, как описано в разделе [форматы согласования](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-566">If you get this error code, renegotiate the mixer's output type as described in [Negotiating Formats](#negotiating-formats).</span></span><br/>                                                                                                                                                                                                        |

    

     

    <span data-ttu-id="eb1e4-567">Если [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) будет выполнена, продолжайте.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-567">If [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) succeeds, continue.</span></span>

5.  <span data-ttu-id="eb1e4-568">(Необязательно.) Если часы доступны, получите текущее время (*T2*).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-568">(Optional.) If the clock is available, get the current clock time (*T2*).</span></span> <span data-ttu-id="eb1e4-569">Количество задержек, введенных микшером, — (*T2*  -  *T1*).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-569">The amount of latency introduced by the mixer is (*T2* - *T1*).</span></span> <span data-ttu-id="eb1e4-570">Отправка **EC_PROCESSING_LATENCY** события с этим ЗНАЧЕНИЕМ в Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-570">Send an **EC_PROCESSING_LATENCY** event with this value to the EVR.</span></span> <span data-ttu-id="eb1e4-571">Евр использует это значение для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-571">The EVR uses this value for quality control.</span></span> <span data-ttu-id="eb1e4-572">Если часы недоступны, нет причин отправить событие **EC_PROCESSING_LATENCY** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-572">If no clock is available, there is no reason to send the **EC_PROCESSING_LATENCY** event.</span></span>
6.  <span data-ttu-id="eb1e4-573">(Необязательно.) Выполните запрос к образцу для [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) и вызовите [**Имфтраккедсампле:: сеталлокатор**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) , как описано в разделе о [примерах отслеживания](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-573">(Optional.) Query the sample for [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) and call [**IMFTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) as described in [Tracking Samples](#tracking-samples).</span></span>
7.  <span data-ttu-id="eb1e4-574">Запланируйте пример для презентации.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-574">Schedule the sample for presentation.</span></span>

<span data-ttu-id="eb1e4-575">Эта последовательность действий может завершиться до того, как выступающий получит выходные данные микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-575">This sequence of steps can terminate before the presenter gets any output from the mixer.</span></span> <span data-ttu-id="eb1e4-576">Чтобы предотвратить удаление запросов, необходимо повторить те же действия, что и в следующем случае.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-576">To ensure that no requests are dropped, you should repeat the same steps when the following occur:</span></span>

-   <span data-ttu-id="eb1e4-577">Вызывается метод [**имфклоккстатесинк:: онклоккстарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) или **Имфклоккстатесинк:: онклоккстарт** выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-577">The presenter's [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or **IMFClockStateSink::OnClockStart** method is called.</span></span> <span data-ttu-id="eb1e4-578">Это обрабатывает случай, когда микшер игнорирует входные данные, так как часы приостанавливаются (шаг 1).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-578">This handles the case where the mixer ignores input because the clock is paused (step 1).</span></span>
-   <span data-ttu-id="eb1e4-579">Вызывается обратный вызов [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-579">The [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback is invoked.</span></span> <span data-ttu-id="eb1e4-580">Это обрабатывает случай, когда микшер получает входные данные, но все видеоматериалы в выступающем коде используются (шаг 2).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-580">This handles the case where the mixer receives input but all of the presenter's video samples are in use (step 2).</span></span>

<span data-ttu-id="eb1e4-581">В следующих нескольких примерах кода эти действия показаны более подробно.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-581">The next several code examples show these steps in more detail.</span></span> <span data-ttu-id="eb1e4-582">Выступающий вызывает `ProcessInputNotify` метод (как показано в следующем примере), когда он получает сообщение **MFVP_MESSAGE_PROCESSINPUTNOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-582">The presenter calls the `ProcessInputNotify` method (shown in the following example) when it gets the **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message.</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



<span data-ttu-id="eb1e4-583">Этот `ProcessInputNotify` метод задает логический флаг для записи того факта, что микшер имеет новые входные данные.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-583">This `ProcessInputNotify` method sets a Boolean flag to record the fact that the mixer has new input.</span></span> <span data-ttu-id="eb1e4-584">Затем вызывается `ProcessOutputLoop` метод, показанный в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-584">Then it calls the `ProcessOutputLoop` method, shown in the next example.</span></span> <span data-ttu-id="eb1e4-585">Этот метод пытается извлечь из микшера столько выборок, сколько возможно:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-585">This method attempts to pull as many samples as possible from the mixer:</span></span>


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



<span data-ttu-id="eb1e4-586">`ProcessOutput`Метод, показанный в следующем примере, пытается получить один кадр видео из микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-586">The `ProcessOutput` method, shown in the next example, attempts to get a single video frame from the mixer.</span></span> <span data-ttu-id="eb1e4-587">Если видеокадр недоступен, `ProcessSample` возвращает S_FALSE или код ошибки, который прерывает цикл в `ProcessOutputLoop` .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-587">If no video frame is available, `ProcessSample` returns S_FALSE or an error code, either of which interrupts the loop in `ProcessOutputLoop`.</span></span> <span data-ttu-id="eb1e4-588">Большая часть работы выполняется внутри `ProcessOutput` метода:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-588">Most of the work is done inside the `ProcessOutput` method:</span></span>


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



<span data-ttu-id="eb1e4-589">Некоторые замечания по этому примеру:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-589">Some remarks about this example:</span></span>

-   <span data-ttu-id="eb1e4-590">Предполагается, что *m_SamplePool* переменная является объектом коллекции, в котором хранится очередь доступных видеороликов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-590">The *m_SamplePool* variable is assumed to be a collection object that holds the queue of available video samples.</span></span> <span data-ttu-id="eb1e4-591">`GetSample`Метод объекта возвращает **MF_E_SAMPLEALLOCATOR_EMPTY** , если очередь пуста.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-591">The object's `GetSample` method returns **MF_E_SAMPLEALLOCATOR_EMPTY** if the queue is empty.</span></span>
-   <span data-ttu-id="eb1e4-592">Если метод [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) микшера возвращает MF_E_TRANSFORM_NEED_MORE_INPUT, это означает, что микшер не может получить больше выходных данных, так что выступающий снимает флаг *m_fSampleNotify* .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-592">If the mixer's [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns MF_E_TRANSFORM_NEED_MORE_INPUT, it means the mixer cannot produce any more output, so the presenter clears the *m_fSampleNotify* flag.</span></span>
-   <span data-ttu-id="eb1e4-593">`TrackSample`Метод, который задает обратный вызов [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) , показан в разделе [примеры отслеживания](#tracking-samples).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-593">The `TrackSample` method, which sets the [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback, is shown in the section [Tracking Samples](#tracking-samples).</span></span>

### <a name="repainting-frames"></a><span data-ttu-id="eb1e4-594">Перерисовка кадров</span><span class="sxs-lookup"><span data-stu-id="eb1e4-594">Repainting Frames</span></span>

<span data-ttu-id="eb1e4-595">Иногда выступающим может потребоваться перекрасить последний кадр видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-595">Occasionally the presenter might need to repaint the most recent video frame.</span></span> <span data-ttu-id="eb1e4-596">Например, Стандартный выступающий перерисовывает кадр в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-596">For example, the standard presenter repaints the frame in the following situations:</span></span>

-   <span data-ttu-id="eb1e4-597">В оконном режиме, в ответ на **WM_PAINT** сообщения, полученные окном приложения.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-597">In windowed mode, in response to **WM_PAINT** messages received by the application's window.</span></span> <span data-ttu-id="eb1e4-598">См. раздел [**имфвидеодисплайконтрол:: репаинтвидео**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-598">See [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>
-   <span data-ttu-id="eb1e4-599">Значение, если конечный прямоугольник изменяется, когда приложение вызывает [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-599">If the destination rectangle changes when the application calls [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="eb1e4-600">Выполните следующие действия, чтобы запросить микшер для повторного создания последней рамки:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-600">Use the following steps to request the mixer to re-create the most recent frame:</span></span>

1.  <span data-ttu-id="eb1e4-601">Получите пример видео из очереди.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-601">Get a video sample from the queue.</span></span>
2.  <span data-ttu-id="eb1e4-602">Запросите пример для интерфейса [**имфдесиредсампле**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-602">Query the sample for the [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) interface.</span></span>
3.  <span data-ttu-id="eb1e4-603">Вызовите [**имфдесиредсампле:: сетдесиредсамплетимеанддуратион**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-603">Call [**IMFDesiredSample::SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration).</span></span> <span data-ttu-id="eb1e4-604">Укажите метку времени для последнего кадра видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-604">Specify the time stamp of the most recent video frame.</span></span> <span data-ttu-id="eb1e4-605">(Вам потребуется кэшировать это значение и обновить его для каждого кадра.)</span><span class="sxs-lookup"><span data-stu-id="eb1e4-605">(You will need to cache this value and update it for each frame.)</span></span>
4.  <span data-ttu-id="eb1e4-606">Вызовите [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в микшере.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-606">Call [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) on the mixer.</span></span>

<span data-ttu-id="eb1e4-607">При перерисовки рамки можно проигнорировать часы презентации и сразу приступить к показу кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-607">When repainting a frame, you can ignore the presentation clock and present the frame immediately.</span></span>

### <a name="scheduling-samples"></a><span data-ttu-id="eb1e4-608">Примеры планирования</span><span class="sxs-lookup"><span data-stu-id="eb1e4-608">Scheduling Samples</span></span>

<span data-ttu-id="eb1e4-609">Видеокадры могут достигать Евр в любое время.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-609">Video frames can reach the EVR at any time.</span></span> <span data-ttu-id="eb1e4-610">Выступающий отвечает за представление каждого кадра в нужное время на основе метки времени кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-610">The presenter is responsible for presenting each frame at the correct time, based on the time stamp of the frame.</span></span> <span data-ttu-id="eb1e4-611">Когда выступающий получает новый пример из микшера, он помещает пример в очередь по расписанию.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-611">When the presenter gets a new sample from the mixer, it puts the sample on the scheduled queue.</span></span> <span data-ttu-id="eb1e4-612">В отдельном потоке, выступающий постоянно получает первый пример из заголовка очереди и определяет, нужно ли:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-612">On a separate thread, the presenter continually gets the first sample from the head of the queue and determines whether to:</span></span>

-   <span data-ttu-id="eb1e4-613">Представьте пример.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-613">Present the sample.</span></span>
-   <span data-ttu-id="eb1e4-614">Не заключайте пример в очередь, так как он находится на раннем этапе.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-614">Keep the sample on the queue because it is early.</span></span>
-   <span data-ttu-id="eb1e4-615">Удалите пример, так как он просрочен.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-615">Discard the sample because it is late.</span></span> <span data-ttu-id="eb1e4-616">Несмотря на то, что по возможности не следует удалять кадры, может потребоваться, если выступающие непрерывно не попадают.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-616">Although you should avoid dropping frames if possible, you might need to if the presenter is continually falling behind.</span></span>

<span data-ttu-id="eb1e4-617">Чтобы получить метку времени для видеокадра, вызовите [**имфсампле:: жетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) в примере с видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-617">To get the time stamp for a video frame, call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the video sample.</span></span> <span data-ttu-id="eb1e4-618">Метка времени относится к часам представления Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-618">The time stamp is relative to the EVR's presentation clock.</span></span> <span data-ttu-id="eb1e4-619">Чтобы получить текущее время, вызовите метод [**имфклокк:: жеткоррелатедтиме**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-619">To get the current clock time, call [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).</span></span> <span data-ttu-id="eb1e4-620">Если Евр не имеет часов представления или если образец не имеет отметки времени, вы можете предоставить пример сразу же после его получения.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-620">If the EVR does not have a presentation clock, or if a sample does not have a time stamp, you can present the sample immediately after you get it.</span></span>

<span data-ttu-id="eb1e4-621">Чтобы получить длительность каждого образца, вызовите метод [**имфсампле:: жетсампледуратион**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-621">To get the duration of each sample, call [**IMFSample::GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration).</span></span> <span data-ttu-id="eb1e4-622">Если выборка не имеет длительности, можно использовать функцию [**мффрамератетоаверажетимеперфраме**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) для вычисления длительности по частоте кадров.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-622">If the sample does not have a duration, you can use the [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) function to calculate the duration from the frame rate.</span></span>

<span data-ttu-id="eb1e4-623">При планировании выборок учитывайте следующее.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-623">When you schedule samples, keep in mind the following:</span></span>

-   <span data-ttu-id="eb1e4-624">Если скорость воспроизведения увеличивается или снижается по сравнению с обычной скоростью, часы запускаются с более высокой или низкой скоростью.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-624">If the playback rate is faster or slower than normal speed, the clock runs at a faster or slower rate.</span></span> <span data-ttu-id="eb1e4-625">Это означает, что метка времени в образце всегда дает правильное целевое время относительно часов представления.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-625">That means the time stamp on a sample always gives the correct target time relative to the presentation clock.</span></span> <span data-ttu-id="eb1e4-626">Однако при переводе времени презентации в другое время (например, счетчик производительности с высоким разрешением) необходимо масштабировать время в зависимости от тактовой частоты.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-626">However, if you translate presentation times into some other clock time (for example, the high-resolution performace counter), then you must scale the times based on the clock speed.</span></span> <span data-ttu-id="eb1e4-627">При изменении тактовой частоты Евр вызывает метод [**имфклоккстатесинк:: онклокксетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-627">If the clock speed changes, the EVR calls the presenter's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>
-   <span data-ttu-id="eb1e4-628">Скорость воспроизведения может быть отрицательной для воспроизведения на противоположном.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-628">The playback rate can be negative for reverse playback.</span></span> <span data-ttu-id="eb1e4-629">Если скорость воспроизведения отрицательна, часы презентации выполняются назад.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-629">When the playback rate is negative, the presentation clock runs backward.</span></span> <span data-ttu-id="eb1e4-630">Иными словами, время *n* + 1 происходит раньше, чем время *n*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-630">In other words, time *N* + 1 occurs before time *N*.</span></span>

<span data-ttu-id="eb1e4-631">В следующем примере вычисляется, как на ранней или поздней стадии выполняется выборка относительно часов представления.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-631">The following example calculates how early or late a sample is, relative to the presentation clock:</span></span>


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



<span data-ttu-id="eb1e4-632">Часы презентации обычно управляются системными часами или модулем подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-632">The presentation clock is usually driven by the system clock or the audio renderer.</span></span> <span data-ttu-id="eb1e4-633">(Модуль подготовки звука наследует время от скорости, с которой звуковая карта потребляет звук.) Как правило, часы представления не синхронизируются с частотой обновления монитора.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-633">(The audio renderer derives the time from the rate at which the sound card consumes audio.) In general, the presentation clock is not synchronized with the refresh rate of the monitor.</span></span>

<span data-ttu-id="eb1e4-634">Если параметры представления Direct3D указывают **D3DPRESENT_INTERVAL_DEFAULT** или **D3DPRESENT_INTERVAL_ONE** для интервала презентации, операция **представления** ожидает вертикальной перетрассировки монитора.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-634">If your Direct3D presentation parameters specify **D3DPRESENT_INTERVAL_DEFAULT** or **D3DPRESENT_INTERVAL_ONE** for the presentation interval, the **Present** operation waits for the monitor's vertical retrace.</span></span> <span data-ttu-id="eb1e4-635">Это простой способ предотвратить разрыв, но снижает точность алгоритма планирования.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-635">This is an easy way to prevent tearing, but reduces the accuracy of your scheduling algorithm.</span></span> <span data-ttu-id="eb1e4-636">И наоборот, если интервал презентации **D3DPRESENT_INTERVAL_IMMEDIATE**, то метод **Present** выполняется немедленно, что приводит к разрыву, если только алгоритм планирования не будет достаточно точным, пока вы не назначите **его только в** течение вертикального периода повторной трассировки.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-636">Conversely, if the presentation interval is **D3DPRESENT_INTERVAL_IMMEDIATE**, the **Present** method executes immediately, which causes tearing unless your scheduling algorithm is accurate enough that you call **Present** only during the vertical retrace period.</span></span>

<span data-ttu-id="eb1e4-637">Следующие функции помогут получить точные сведения о времени:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-637">The following functions can help you get accurate timing information:</span></span>

-   <span data-ttu-id="eb1e4-638">**IDirect3DDevice9:: жетрастерстатус** возвращает сведения о растровом элементе, включая текущую строку развертки, а также то, находится ли точечный символ в вертикальной пустой точке.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-638">**IDirect3DDevice9::GetRasterStatus** returns information about the raster, including the current scan line and whether the raster is in the vertical blank period.</span></span>
-   <span data-ttu-id="eb1e4-639">**Двмжеткомпоситионтимингинфо** возвращает сведения о времени для диспетчера окон рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-639">**DwmGetCompositionTimingInfo** returns timing information for the desktop window manager.</span></span> <span data-ttu-id="eb1e4-640">Эта информация полезна, если включена Композиция рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-640">This information is useful if desktop composition is enabled.</span></span>

### <a name="presenting-samples"></a><span data-ttu-id="eb1e4-641">Представление образцов</span><span class="sxs-lookup"><span data-stu-id="eb1e4-641">Presenting Samples</span></span>

<span data-ttu-id="eb1e4-642">В этом разделе предполагается, что вы создали отдельную цепочку подкачки для каждой поверхности, как описано в статье [выделение поверхностей Direct3D](#allocating-direct3d-surfaces).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-642">This section assumes that you created a separate swap chain for each surface as described in [Allocating Direct3D Surfaces](#allocating-direct3d-surfaces).</span></span> <span data-ttu-id="eb1e4-643">Чтобы показать пример, получите цепочку подкачки из примера видео следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-643">To present a sample, get the swap chain from the video sample as follows:</span></span>

1.  <span data-ttu-id="eb1e4-644">Чтобы получить буфер, вызовите [**имфсампле:: жетбуффербиндекс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) в примере видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-644">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) on the video sample to get the buffer.</span></span>
2.  <span data-ttu-id="eb1e4-645">Запросите буфер для интерфейса [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-645">Query the buffer for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
3.  <span data-ttu-id="eb1e4-646">Вызовите [**имфжетсервице:: Get Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , чтобы получить интерфейс **IDirect3DSurface9** поверхности Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-646">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the **IDirect3DSurface9** interface of the Direct3D surface.</span></span> <span data-ttu-id="eb1e4-647">(Этот шаг и предыдущий шаг можно объединить в один, вызвав [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span><span class="sxs-lookup"><span data-stu-id="eb1e4-647">(You can combine this step and the previous step into one by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)</span></span>
4.  <span data-ttu-id="eb1e4-648">Вызовите **IDirect3DSurface9::-Contain** на поверхности, чтобы получить указатель на цепочку буферов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-648">Call **IDirect3DSurface9::GetContainer** on the surface to get a pointer to the swap chain.</span></span>
5.  <span data-ttu-id="eb1e4-649">Вызов **IDirect3DSwapChain9::P** повторной отправки в цепочке буферов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-649">Call **IDirect3DSwapChain9::Present** on the swap chain.</span></span>

<span data-ttu-id="eb1e4-650">Следующий код показывает эти действия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-650">The following code shows these steps:</span></span>


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a><span data-ttu-id="eb1e4-651">Исходный и конечный прямоугольники</span><span class="sxs-lookup"><span data-stu-id="eb1e4-651">Source and Destination Rectangles</span></span>

<span data-ttu-id="eb1e4-652">*Исходный прямоугольник* — это часть отображаемого видеокадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-652">The *source rectangle* is the portion of the video frame to display.</span></span> <span data-ttu-id="eb1e4-653">Он определяется относительно нормализованной системы координат, в которой весь кадр видео занимает прямоугольник с координатами {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-653">It is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="eb1e4-654">*Прямоугольник назначения* — это область в области назначения, в которой рисуется кадр видео.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-654">The *destination rectangle* is the area within the destination surface where the video frame is drawn.</span></span> <span data-ttu-id="eb1e4-655">Стандартный выступающий позволяет приложению устанавливать эти прямоугольники путем вызова [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-655">The standard presenter enables an application to set these rectangles by calling [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="eb1e4-656">Существует несколько вариантов применения исходного и целевого прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-656">There are several options for applying source and destination rectangles.</span></span> <span data-ttu-id="eb1e4-657">Первый вариант — Разрешить микшеру применять их:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-657">The first option is to let the mixer apply them:</span></span>

-   <span data-ttu-id="eb1e4-658">Задайте исходный прямоугольник с помощью атрибута [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-658">Set the source rectangle using the [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) attribute.</span></span> <span data-ttu-id="eb1e4-659">Микшер будет применять исходный прямоугольник, когда он блитс видео на поверхность назначения.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-659">The mixer will apply the source rectangle when it blits the video to the destination surface.</span></span> <span data-ttu-id="eb1e4-660">Исходный прямоугольник по умолчанию — это весь фрейм.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-660">The mixer's default source rectangle is the entire frame.</span></span>
-   <span data-ttu-id="eb1e4-661">Установите прямоугольник назначения в качестве геометрического апертуры в выходном типе микшера.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-661">Set the destination rectangle as the geometric aperture in the mixer's output type.</span></span> <span data-ttu-id="eb1e4-662">Дополнительные сведения см. в статье о [форматах согласования](#negotiating-formats).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-662">For more information, see [Negotiating Formats](#negotiating-formats).</span></span>

<span data-ttu-id="eb1e4-663">Второй вариант — применить прямоугольники при **IDirect3DSwapChain9::P** повторно, указав параметры *псаурцерект* и *пдестрект* в методе **Present** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-663">The second option is to apply the rectangles when you **IDirect3DSwapChain9::Present** by specifying the *pSourceRect* and *pDestRect* parameters in the **Present** method.</span></span> <span data-ttu-id="eb1e4-664">Эти параметры можно комбинировать.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-664">You can combine these options.</span></span> <span data-ttu-id="eb1e4-665">Например, можно задать исходный прямоугольник в микшере, но применить прямоугольник назначения в методе **Present** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-665">For example, you could set the source rectangle on the mixer but apply the destination rectangle in the **Present** method.</span></span>

<span data-ttu-id="eb1e4-666">Если приложение изменяет конечный прямоугольник или изменяет размер окна, может потребоваться выделить новые поверхности.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-666">If the application changes the destination rectangle or resizes the window, you might need to allocate new surfaces.</span></span> <span data-ttu-id="eb1e4-667">Если это так, необходимо соблюдать осторожность при синхронизации этой операции с потоком планирования.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-667">If so, you must be careful to synchronize this operation with your scheduling thread.</span></span> <span data-ttu-id="eb1e4-668">Очистите очередь планирования и отбросить старые примеры перед выделением новых поверхностей.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-668">Flush the scheduling queue and discard the old samples before allocating new surfaces.</span></span>

### <a name="end-of-stream"></a><span data-ttu-id="eb1e4-669">Конец потока</span><span class="sxs-lookup"><span data-stu-id="eb1e4-669">End of Stream</span></span>

<span data-ttu-id="eb1e4-670">После завершения каждого входного потока в Евр Евр отправляет выступающее сообщение **MFVP_MESSAGE_ENDOFSTREAM** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-670">When every input stream on the EVR has ended, the EVR sends an **MFVP_MESSAGE_ENDOFSTREAM** message to the presenter.</span></span> <span data-ttu-id="eb1e4-671">Однако в момент получения сообщения может быть осталось несколько кадров видео, которые будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-671">At the point when you receive the message, however, there might be a few video frames remaining to be processed.</span></span> <span data-ttu-id="eb1e4-672">Прежде чем реагировать на сообщение в конце потока, необходимо прекратить все выходные данные микшера и Показать все остальные кадры.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-672">Before you respond to the end-of-stream message, you must drain all of the output from the mixer and present all of the remaining frames.</span></span> <span data-ttu-id="eb1e4-673">После представления последнего кадра Отправьте событие **EC_COMPLETE** в Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-673">After the last frame is presented, send an **EC_COMPLETE** event to the EVR.</span></span>

<span data-ttu-id="eb1e4-674">В следующем примере показан метод, который отправляет событие **EC_COMPLETE** , если выполняются различные условия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-674">The next example shows a method that sends the **EC_COMPLETE** event if various conditions are met.</span></span> <span data-ttu-id="eb1e4-675">В противном случае он возвращает S_OK без отправки события:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-675">Otherwise, it returns S_OK without sending the event:</span></span>


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



<span data-ttu-id="eb1e4-676">Этот метод проверяет следующие состояния:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-676">This method checks the following states:</span></span>

-   <span data-ttu-id="eb1e4-677">Если переменная *m_fSampleNotify* имеет **значение true**, это означает, что микшер содержит один или несколько кадров, которые еще не были обработаны.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-677">If the *m_fSampleNotify* variable is **TRUE**, it means the mixer has one or more frames that have not been processed yet.</span></span> <span data-ttu-id="eb1e4-678">(Дополнительные сведения см. в разделе [Обработка выходных данных](#processing-output).)</span><span class="sxs-lookup"><span data-stu-id="eb1e4-678">(For details, see [Processing Output](#processing-output).)</span></span>
-   <span data-ttu-id="eb1e4-679">Переменная *m_fEndStreaming* является логическим флагом, начальным значением которого является **false**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-679">The *m_fEndStreaming* variable is a Boolean flag whose initial value **FALSE**.</span></span> <span data-ttu-id="eb1e4-680">Выступающий устанавливает для флага **значение true** , когда Евр отправляет сообщение **MFVP_MESSAGE_ENDOFSTREAM** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-680">The presenter sets the flag to **TRUE** when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message.</span></span>
-   <span data-ttu-id="eb1e4-681">`AreSamplesPending`Предполагается, что метод возвращает **значение true** , если один или несколько кадров ожидают выполнения в запланированной очереди.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-681">The `AreSamplesPending` method is assumed to return **TRUE** as long as one or more frames are waiting in the scheduled queue.</span></span>

<span data-ttu-id="eb1e4-682">В методе [**имфвидеопресентер::P роцессмессаже**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) задайте для *m_fEndStreaming* **значение true** и вызовите, `CheckEndOfStream` когда Евр отправляет сообщение **MFVP_MESSAGE_ENDOFSTREAM** :</span><span class="sxs-lookup"><span data-stu-id="eb1e4-682">In the [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) method, set *m_fEndStreaming* to **TRUE** and call `CheckEndOfStream` when the EVR sends the **MFVP_MESSAGE_ENDOFSTREAM** message:</span></span>


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



<span data-ttu-id="eb1e4-683">Кроме того, вызовите, `CheckEndOfStream` Если метод [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) микшера возвращает **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-683">In addition, call `CheckEndOfStream` if the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method returns **MF_E_TRANSFORM_NEED_MORE_INPUT**.</span></span> <span data-ttu-id="eb1e4-684">Этот код ошибки означает, что микшер не содержит дополнительных входных образцов (см. раздел [Обработка выходных данных](#processing-output)).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-684">This error code indicates that the mixer has no more input samples (see [Processing Output](#processing-output)).</span></span>

## <a name="frame-stepping"></a><span data-ttu-id="eb1e4-685">Пошаговое выполнение кадра</span><span class="sxs-lookup"><span data-stu-id="eb1e4-685">Frame Stepping</span></span>

<span data-ttu-id="eb1e4-686">Евр предназначен для поддержки пошагового выполнения кадров в DirectShow и очистки в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-686">The EVR is designed to support frame stepping in DirectShow and scrubbing in Media Foundation.</span></span> <span data-ttu-id="eb1e4-687">Пошаговое выполнение и очистка кадров концептуально похожи.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-687">Frame stepping and scrubbing are conceptually similar.</span></span> <span data-ttu-id="eb1e4-688">В обоих случаях приложение запрашивает один видеокадр за раз.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-688">In both cases, the application requests one video frame at a time.</span></span> <span data-ttu-id="eb1e4-689">На внутреннем уровне выступающий использует тот же механизм для реализации обеих функций.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-689">Internally, the presenter uses the same mechanism to implement both features.</span></span>

<span data-ttu-id="eb1e4-690">Пошаговое выполнение пакета в DirectShow работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-690">Frame stepping in DirectShow works as follows:</span></span>

-   <span data-ttu-id="eb1e4-691">Приложение вызывает [**ивидеофраместеп:: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-691">The application calls [**IVideoFrameStep::Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step).</span></span> <span data-ttu-id="eb1e4-692">Число шагов указывается в параметре *двстепс* .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-692">The number of steps is given in the *dwSteps* parameter.</span></span> <span data-ttu-id="eb1e4-693">Евр отправляет выступающее сообщение **MFVP_MESSAGE_STEP** , где параметр сообщения (*улпарам*) — это число шагов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-693">The EVR sends an **MFVP_MESSAGE_STEP** message to the presenter, where the message parameter (*ulParam*) is the number of steps.</span></span>
-   <span data-ttu-id="eb1e4-694">Если приложение вызывает [**ивидеофраместеп:: канцелстеп**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) или изменяет состояние графа (запущено, приостановлено или остановлено), ЕВР отправляет сообщение **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-694">If the application calls [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) or changes the graph state (running, paused, or stopped), the EVR sends an **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="eb1e4-695">Очистка в Media Foundation работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-695">Scrubbing in Media Foundation works as follows:</span></span>

-   <span data-ttu-id="eb1e4-696">Приложение устанавливает скорость воспроизведения равным нулю, вызывая [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-696">The application sets the playback rate to zero by calling [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span>
-   <span data-ttu-id="eb1e4-697">Чтобы отобразить новый кадр, приложение вызывает [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) с требуемой позицией.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-697">To render a new frame, the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the desired position.</span></span> <span data-ttu-id="eb1e4-698">Евр отправляет сообщение **MFVP_MESSAGE_STEP** с *улпарам* , равным 1.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-698">The EVR sends an **MFVP_MESSAGE_STEP** message with *ulParam* equal to 1.</span></span>
-   <span data-ttu-id="eb1e4-699">Чтобы отключить очистку, приложение устанавливает для скорости воспроизведения ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-699">To stop scrubbing, the application sets the playback rate to a nonzero value.</span></span> <span data-ttu-id="eb1e4-700">Евр отправляет сообщение **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-700">The EVR sends the **MFVP_MESSAGE_CANCELSTEP** message.</span></span>

<span data-ttu-id="eb1e4-701">После получения сообщения **MFVP_MESSAGE_STEP** Выступающий ожидает прибытия целевого кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-701">After receiving the **MFVP_MESSAGE_STEP** message, the presenter waits for the target frame to arrive.</span></span> <span data-ttu-id="eb1e4-702">Если число шагов равно *N*, то выступающий отклоняет следующие примеры (*n* – 1) и представляет *N* -й пример.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-702">If the number of steps is *N*, the presenter discards the next (*N* - 1) samples and presents the *N* th sample.</span></span> <span data-ttu-id="eb1e4-703">Когда выступающий завершает шаг кадра, он отправляет событие [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) в Евр с параметром *lParam1* , имеющим значение **false**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-703">When the presenter completes the frame step, it sends an [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event to the EVR with *lParam1* set to **FALSE**.</span></span> <span data-ttu-id="eb1e4-704">Кроме того, если скорость воспроизведения равна нулю, выступающий отправляет событие [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-704">In addition, if the playback rate is zero, the presenter sends an [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) event.</span></span> <span data-ttu-id="eb1e4-705">Если Евр отменяет выполнение кадра в то время, когда операция с кадрами все еще находится в состоянии ожидания, выступающий отправляет событие **EC_STEP_COMPLETE** с параметром *lParam1* , имеющим значение **true**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-705">If the EVR cancels frame stepping while a frame-step operation is still pending, the presenter sends an **EC_STEP_COMPLETE** event with *lParam1* set to **TRUE**.</span></span>

<span data-ttu-id="eb1e4-706">Приложение может выполнить шаг или очистку несколько раз, поэтому перед получением **MFVP_MESSAGE_CANCELSTEP** сообщения выступающий может получить несколько **MFVP_MESSAGE_STEP** сообщений.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-706">The application can frame step or scrub multiple times, so the presenter might receive multiple **MFVP_MESSAGE_STEP** messages before it gets an **MFVP_MESSAGE_CANCELSTEP** message.</span></span> <span data-ttu-id="eb1e4-707">Кроме того, выступающий может получить сообщение **MFVP_MESSAGE_STEP** до начала или во время выполнения часов.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-707">Also, the presenter can receive the **MFVP_MESSAGE_STEP** message before the clock starts or while the clock is running.</span></span>

### <a name="implementing-frame-stepping"></a><span data-ttu-id="eb1e4-708">Реализация пошагового выполнения кадра</span><span class="sxs-lookup"><span data-stu-id="eb1e4-708">Implementing Frame Stepping</span></span>

<span data-ttu-id="eb1e4-709">В этом разделе описывается алгоритм для реализации пошагового выполнения кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-709">This section describes an algorithm to implement frame stepping.</span></span> <span data-ttu-id="eb1e4-710">Алгоритм пошагового выполнения кадров использует следующие переменные:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-710">The frame stepping algorithm uses the following variables:</span></span>

-   <span data-ttu-id="eb1e4-711">*step_count*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-711">*step_count*.</span></span> <span data-ttu-id="eb1e4-712">Целое число без знака, указывающее количество шагов в текущей операции пошагового выполнения кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-712">An unsigned integer that specifies the number of steps in the current frame stepping operation.</span></span>
-   <span data-ttu-id="eb1e4-713">*step_queue*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-713">*step_queue*.</span></span> <span data-ttu-id="eb1e4-714">Очередь указателей [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-714">A queue of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointers.</span></span>
-   <span data-ttu-id="eb1e4-715">*step_state*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-715">*step_state*.</span></span> <span data-ttu-id="eb1e4-716">В любое время выступающий может находиться в одном из следующих состояний по отношению к пошаговому выполнению кадров:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-716">At any time, the presenter can be in one of the following states with respect to frame stepping:</span></span> 

    | <span data-ttu-id="eb1e4-717">Состояние</span><span class="sxs-lookup"><span data-stu-id="eb1e4-717">State</span></span>         | <span data-ttu-id="eb1e4-718">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-718">Description</span></span>                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="eb1e4-719">NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="eb1e4-719">NOT_STEPPING</span></span> | <span data-ttu-id="eb1e4-720">Не пошаговое выполнение кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-720">Not frame stepping.</span></span>                                                                                                                                                                                             |
    | <span data-ttu-id="eb1e4-721">ОЖИДАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb1e4-721">WAITING</span></span>       | <span data-ttu-id="eb1e4-722">Выступающий получил сообщение **MFVP_MESSAGE_STEP** , но часы не запущены.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-722">The presenter has received the **MFVP_MESSAGE_STEP** message, but the clock has not started.</span></span>                                                                                                                  |
    | <span data-ttu-id="eb1e4-723">PENDING</span><span class="sxs-lookup"><span data-stu-id="eb1e4-723">PENDING</span></span>       | <span data-ttu-id="eb1e4-724">Выступающий получил сообщение **MFVP_MESSAGE_STEP** , и часы начали, но выступающий ожидает получения целевого кадра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-724">The presenter has received the **MFVP_MESSAGE_STEP** message and the clock has started, but the presenter is waiting to receive the target frame.</span></span>                                                             |
    | <span data-ttu-id="eb1e4-725">ПЛАНИРУЕТ</span><span class="sxs-lookup"><span data-stu-id="eb1e4-725">SCHEDULED</span></span>     | <span data-ttu-id="eb1e4-726">Докладчик получил целевой кадр и запланировал его для презентации, но этот кадр не был представлен.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-726">The presenter has received the target frame and has scheduled it for presentation, but the frame has not been presented.</span></span>                                                                                        |
    | <span data-ttu-id="eb1e4-727">ЗАВЕРШЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb1e4-727">COMPLETE</span></span>      | <span data-ttu-id="eb1e4-728">Докладчик представил целевой кадр и отправил [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) событие и ожидает следующего сообщения **MFVP_MESSAGE_STEP** или **MFVP_MESSAGE_CANCELSTEP** .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-728">The presenter has presented the target frame and sent the [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) event, and is waiting for the next **MFVP_MESSAGE_STEP** or **MFVP_MESSAGE_CANCELSTEP** message.</span></span> |

    

     

    <span data-ttu-id="eb1e4-729">Эти состояния не зависят от состояний выступающего, перечисленных в разделе [состояние Presenter](#presenter-states).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-729">These states are independent of the presenter states listed in the section [Presenter States](#presenter-states).</span></span>

<span data-ttu-id="eb1e4-730">Для алгоритма пошагового прохода определены следующие процедуры:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-730">The following procedures are defined for the frame-stepping algorithm:</span></span>

<span data-ttu-id="eb1e4-731">Процедура Препарефраместеп</span><span class="sxs-lookup"><span data-stu-id="eb1e4-731">PrepareFrameStep Procedure</span></span>

1.  <span data-ttu-id="eb1e4-732">*Step_count* приращения.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-732">Increment *step_count*.</span></span>
2.  <span data-ttu-id="eb1e4-733">Задайте для *step_state* значение ожидание.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-733">Set *step_state* to WAITING.</span></span>
3.  <span data-ttu-id="eb1e4-734">Если часы выполняются, вызовите Стартфраместеп.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-734">If the clock is running, call StartFrameStep.</span></span>

<span data-ttu-id="eb1e4-735">Процедура Стартфраместеп</span><span class="sxs-lookup"><span data-stu-id="eb1e4-735">StartFrameStep Procedure</span></span>

1.  <span data-ttu-id="eb1e4-736">Если *step_state* равно ожидания, присвойте *step_state* ожидания.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-736">If *step_state* equals WAITING, set *step_state* to PENDING.</span></span> <span data-ttu-id="eb1e4-737">Для каждого примера в *step_queue* вызовите деливерфраместепсампле.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-737">For each sample in *step_queue*, call DeliverFrameStepSample.</span></span>
2.  <span data-ttu-id="eb1e4-738">Если *step_state* равно NOT_STEPPING, удалите все образцы из *step_queue* и запланируйте их для представления.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-738">If *step_state* equals NOT_STEPPING, remove any samples from *step_queue* and schedule them for presentation.</span></span>

<span data-ttu-id="eb1e4-739">Процедура Комплетефраместеп</span><span class="sxs-lookup"><span data-stu-id="eb1e4-739">CompleteFrameStep Procedure</span></span>

1.  <span data-ttu-id="eb1e4-740">Задайте для *step_state* значение завершено.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-740">Set *step_state* to COMPLETE.</span></span>
2.  <span data-ttu-id="eb1e4-741">Отправьте событие EC_STEP_COMPLETE с *lParam1*  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-741">Send the EC_STEP_COMPLETE event with *lParam1* = **FALSE**.</span></span>
3.  <span data-ttu-id="eb1e4-742">Если ставка часов равна нулю, отправьте событие **EC_SCRUB_TIME** с помощью образца Time.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-742">If the clock rate is zero, send the **EC_SCRUB_TIME** event with the sample time.</span></span>

<span data-ttu-id="eb1e4-743">Процедура Деливерфраместепсампле</span><span class="sxs-lookup"><span data-stu-id="eb1e4-743">DeliverFrameStepSample Procedure</span></span>

1.  <span data-ttu-id="eb1e4-744">Если ставка часов равна нулю и время дискретизации выборки *времени*  +    <  , отбросить пример.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-744">If the clock rate is zero and *sample time* + *sample duration* < *clock time*, discard the sample.</span></span> <span data-ttu-id="eb1e4-745">Выйти.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-745">Exit.</span></span>
2.  <span data-ttu-id="eb1e4-746">Если *step_state* равно "запланировано" или "завершено", добавьте пример в *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-746">If *step_state* equals SCHEDULED or COMPLETE, add the sample to *step_queue*.</span></span> <span data-ttu-id="eb1e4-747">Выйти.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-747">Exit.</span></span>
3.  <span data-ttu-id="eb1e4-748">Декремента *step_count*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-748">Decrement *step_count*.</span></span>
4.  <span data-ttu-id="eb1e4-749">Если *step_count* > 0, удалите пример.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-749">If *step_count* > 0, discard the sample.</span></span> <span data-ttu-id="eb1e4-750">Выйти.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-750">Exit.</span></span>
5.  <span data-ttu-id="eb1e4-751">Если *step_state* равно ожидания, добавьте пример в *step_queue*.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-751">If *step_state* equals WAITING, add the sample to *step_queue*.</span></span> <span data-ttu-id="eb1e4-752">Выйти.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-752">Exit.</span></span>
6.  <span data-ttu-id="eb1e4-753">Запланируйте пример для презентации.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-753">Schedule the sample for presentation.</span></span>
7.  <span data-ttu-id="eb1e4-754">Задайте для *step_state* значение запланировано.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-754">Set *step_state* to SCHEDULED.</span></span>

<span data-ttu-id="eb1e4-755">Процедура Канцелфраместеп</span><span class="sxs-lookup"><span data-stu-id="eb1e4-755">CancelFrameStep Procedure</span></span>

1.  <span data-ttu-id="eb1e4-756">Задайте для *step_state* значение NOT_STEPPING</span><span class="sxs-lookup"><span data-stu-id="eb1e4-756">Set *step_state* to NOT_STEPPING</span></span>
2.  <span data-ttu-id="eb1e4-757">Сброс *step_count* к нулю.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-757">Reset *step_count* to zero.</span></span>
3.  <span data-ttu-id="eb1e4-758">Если предыдущее значение *step_state* было ожидающим, ожидающим или запланированным, отправьте EC_STEP_COMPLETE с *lParam1*  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-758">If the previous value of *step_state* was WAITING, PENDING, or SCHEDULED, send EC_STEP_COMPLETE with *lParam1* = **TRUE**.</span></span>

<span data-ttu-id="eb1e4-759">Вызовите эти процедуры следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-759">Call these procedures as follows:</span></span>



| <span data-ttu-id="eb1e4-760">Сообщение или метод выступающего</span><span class="sxs-lookup"><span data-stu-id="eb1e4-760">Presenter message or method</span></span>                                                   | <span data-ttu-id="eb1e4-761">Процедура</span><span class="sxs-lookup"><span data-stu-id="eb1e4-761">Procedure</span></span>           |
|-------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="eb1e4-762">Сообщение **MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-762">**MFVP_MESSAGE_STEP** message</span></span>                                               | `PrepareFrameStep`  |
| <span data-ttu-id="eb1e4-763">Сообщение **MFVP_MESSAGE_STEP**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-763">**MFVP_MESSAGE_STEP** message</span></span>                                               | `CancelStep`        |
| [<span data-ttu-id="eb1e4-764">**Имфклоккстатесинк:: Онклоккстарт**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-764">**IMFClockStateSink::OnClockStart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [<span data-ttu-id="eb1e4-765">**Имфклоккстатесинк:: Онклоккрестарт**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-765">**IMFClockStateSink::OnClockRestart**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| <span data-ttu-id="eb1e4-766">Обратный вызов [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)</span><span class="sxs-lookup"><span data-stu-id="eb1e4-766">[**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) callback</span></span>                         | `CompleteFrameStep` |
| [<span data-ttu-id="eb1e4-767">**Имфклоккстатесинк:: Онклоккстоп**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-767">**IMFClockStateSink::OnClockStop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [<span data-ttu-id="eb1e4-768">**Имфклоккстатесинк:: Онклокксетрате**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-768">**IMFClockStateSink::OnClockSetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

<span data-ttu-id="eb1e4-769">В следующей блок-схеме показаны процедуры пошагового выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-769">The following flow chart shows the frame-stepping procedures.</span></span>

![на блоковой диаграмме показаны пути, которые начинаются с \- шага сообщения мфвп \- и \- сообщения мфвп \- процессинпутнотифи и заканчиваются на "штат = Complete".](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a><span data-ttu-id="eb1e4-771">Установка параметра Presenter в Евр</span><span class="sxs-lookup"><span data-stu-id="eb1e4-771">Setting the Presenter on the EVR</span></span>

<span data-ttu-id="eb1e4-772">После реализации выступающего, следующим шагом является настройка Евр для его использования.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-772">After implementing the presenter, the next step is to configure the EVR to use it.</span></span>

### <a name="setting-the-presenter-in-directshow"></a><span data-ttu-id="eb1e4-773">Настройка выступающего в DirectShow</span><span class="sxs-lookup"><span data-stu-id="eb1e4-773">Setting the Presenter in DirectShow</span></span>

<span data-ttu-id="eb1e4-774">В приложении DirectShow установите параметр Presenter для Евр следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb1e4-774">In a DirectShow application, set the presenter on the EVR as follows:</span></span>

1.  <span data-ttu-id="eb1e4-775">Создайте фильтр евр, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-775">Create the EVR filter by calling **CoCreateInstance**.</span></span> <span data-ttu-id="eb1e4-776">Идентификатор CLSID — **CLSID_EnhancedVideoRenderer**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-776">The CLSID is **CLSID_EnhancedVideoRenderer**.</span></span>
2.  <span data-ttu-id="eb1e4-777">Добавьте Евр в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-777">Add the EVR to the filter graph.</span></span>
3.  <span data-ttu-id="eb1e4-778">Создайте экземпляр Presenter.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-778">Create an instance of your presenter.</span></span> <span data-ttu-id="eb1e4-779">Ваш выступающий может поддерживать создание стандартных объектов COM через **IClassFactory**, но это необязательно.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-779">Your presenter can support standard COM object creation through **IClassFactory**, but this is not mandatory.</span></span>
4.  <span data-ttu-id="eb1e4-780">Запросите фильтр Евр для интерфейса [**имфвидеорендерер**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-780">Query the EVR filter for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
5.  <span data-ttu-id="eb1e4-781">Вызовите [**имфвидеорендерер:: инитиализерендерер**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-781">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

### <a name="setting-the-presenter-in-media-foundation"></a><span data-ttu-id="eb1e4-782">Настройка выступающего в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb1e4-782">Setting the Presenter in Media Foundation</span></span>

<span data-ttu-id="eb1e4-783">В Media Foundation есть несколько вариантов в зависимости от того, создается ли приемник мультимедиа Евр или объект активации Евр.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-783">In Media Foundation, you have several options, depending on whether you create the EVR media sink or the EVR activation object.</span></span> <span data-ttu-id="eb1e4-784">Дополнительные сведения об объектах активации см. в разделе [объекты активации](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-784">For more information about activation objects, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="eb1e4-785">Для приемника мультимедиа Евр выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-785">For the EVR media sink, do the following:</span></span>

1.  <span data-ttu-id="eb1e4-786">Вызовите [**мфкреатевидеорендерер**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) , чтобы создать приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-786">Call [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) to create the media sink.</span></span>
2.  <span data-ttu-id="eb1e4-787">Создайте экземпляр Presenter.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-787">Create an instance of your presenter.</span></span>
3.  <span data-ttu-id="eb1e4-788">Запросите приемник мультимедиа Евр для интерфейса [**имфвидеорендерер**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-788">Query the EVR media sink for the [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) interface.</span></span>
4.  <span data-ttu-id="eb1e4-789">Вызовите [**имфвидеорендерер:: инитиализерендерер**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="eb1e4-789">Call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>

<span data-ttu-id="eb1e4-790">Для объекта активации Евр выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-790">For the EVR activation object, do the following:</span></span>

1.  <span data-ttu-id="eb1e4-791">Вызовите [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) , чтобы создать объект активации.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-791">Call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the activation object.</span></span>
2.  <span data-ttu-id="eb1e4-792">Задайте один из следующих атрибутов для объекта активации.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-792">Set one of the following attributes on the activation object:</span></span> 

    | <span data-ttu-id="eb1e4-793">attribute</span><span class="sxs-lookup"><span data-stu-id="eb1e4-793">Attribute</span></span>                                                                                                         | <span data-ttu-id="eb1e4-794">Описание</span><span class="sxs-lookup"><span data-stu-id="eb1e4-794">Description</span></span>                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="eb1e4-795">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-795">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**</span></span>](mf-activate-custom-video-presenter-activate-attribute.md) | <span data-ttu-id="eb1e4-796">Указатель на объект активации для выступающего объекта.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-796">Pointer to an activation object for the presenter.</span></span><br/> <span data-ttu-id="eb1e4-797">При использовании этого флага необходимо предоставить объект активации для своего выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-797">With this flag, you must provide an activation object for your presenter.</span></span> <span data-ttu-id="eb1e4-798">Объект активации должен реализовывать интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="eb1e4-798">The activation object must implement the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span><br/> |
    | [<span data-ttu-id="eb1e4-799">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span><span class="sxs-lookup"><span data-stu-id="eb1e4-799">**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**</span></span>](mf-activate-custom-video-presenter-clsid-attribute.md)       | <span data-ttu-id="eb1e4-800">Идентификатор CLSID выступающего.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-800">CLSID of the presenter.</span></span><br/> <span data-ttu-id="eb1e4-801">Этот флаг должен поддерживать создание стандартного объекта COM с помощью **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-801">With this flag, your presenter must support standard COM object creation through **IClassFactory**.</span></span><br/>                                                                                         |

    

     

3.  <span data-ttu-id="eb1e4-802">При необходимости задайте атрибут [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) для объекта активации.</span><span class="sxs-lookup"><span data-stu-id="eb1e4-802">Optionally, set the [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) attribute on the activation object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb1e4-803">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="eb1e4-803">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb1e4-804">Улучшенный модуль подготовки видео</span><span class="sxs-lookup"><span data-stu-id="eb1e4-804">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="eb1e4-805">Пример Еврпресентер</span><span class="sxs-lookup"><span data-stu-id="eb1e4-805">EVRPresenter Sample</span></span>](evrpresenter-sample.md)
</dt> </dl>

 

 
