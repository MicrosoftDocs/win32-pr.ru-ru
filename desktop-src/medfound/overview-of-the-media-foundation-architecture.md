---
description: В этом разделе описывается общий дизайн Microsoft Media Foundation. Сведения об использовании Media Foundation для конкретных задач программирования см. в разделе Media Foundation Guide по программированию.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Общие сведения об архитектуре Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104566061"
---
# <a name="overview-of-the-media-foundation-architecture"></a><span data-ttu-id="dae87-104">Общие сведения об архитектуре Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dae87-104">Overview of the Media Foundation Architecture</span></span>

<span data-ttu-id="dae87-105">В этом разделе описывается общий дизайн Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dae87-105">This topic describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="dae87-106">Сведения об использовании Media Foundation для конкретных задач программирования см. в разделе [Media Foundation Guide по программированию](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="dae87-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

<span data-ttu-id="dae87-107">На следующей схеме показано высокоуровневое представление архитектуры Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dae87-107">The following diagram shows a high-level view of the Media Foundation architecture.</span></span>

![на схеме показан общий обзор архитектуры Media Foundation.](images/mfarch01.png)

<span data-ttu-id="dae87-109">Media Foundation предоставляет две различные модели программирования.</span><span class="sxs-lookup"><span data-stu-id="dae87-109">Media Foundation provides two distinct programming models.</span></span> <span data-ttu-id="dae87-110">Первая модель, показанная в левой части диаграммы, использует сквозной конвейер для данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dae87-110">The first model, shown on the left side of the diagram, uses an end-to-end pipeline for media data.</span></span> <span data-ttu-id="dae87-111">Приложение инициализирует конвейер, например, предоставляя URL-адрес файла для воспроизведения, а затем вызывает методы для управления потоковой передачей.</span><span class="sxs-lookup"><span data-stu-id="dae87-111">The application initializes the pipeline—for example, by providing the URL of a file to play—and then calls methods to control streaming.</span></span> <span data-ttu-id="dae87-112">Во второй модели, показанной в правой части схемы, приложение либо извлекает данные из источника, либо передает их в назначение (или и то, и другое).</span><span class="sxs-lookup"><span data-stu-id="dae87-112">In the second model, shown on the right side of the diagram, the application either pulls data from a source, or pushes it to a destination (or both).</span></span> <span data-ttu-id="dae87-113">Эта модель особенно полезна, если необходимо обработать данные, так как приложение имеет прямой доступ к потоку данных.</span><span class="sxs-lookup"><span data-stu-id="dae87-113">This model is particularly useful if you need to process the data, because the application has direct access to the data stream.</span></span>

### <a name="primitives-and-platform"></a><span data-ttu-id="dae87-114">Примитивы и платформа</span><span class="sxs-lookup"><span data-stu-id="dae87-114">Primitives and Platform</span></span>

<span data-ttu-id="dae87-115">Начиная с нижней части диаграммы, *примитивы* являются вспомогательными объектами, используемыми во Media Foundation API:</span><span class="sxs-lookup"><span data-stu-id="dae87-115">Starting from the bottom of the diagram, the *primitives* are helper objects used throughout the Media Foundation API:</span></span>

-   <span data-ttu-id="dae87-116">[Атрибуты](attributes-and-properties.md) — это универсальный способ хранения информации внутри объекта в виде списка пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="dae87-116">[Attributes](attributes-and-properties.md) are a generic way to store information inside an object, as a list of key/value pairs.</span></span>
-   <span data-ttu-id="dae87-117">[Типы носителей](media-types.md) описывают формат потока данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dae87-117">[Media Types](media-types.md) describe the format of a media data stream.</span></span>
-   <span data-ttu-id="dae87-118">[Буферы мультимедиа](media-buffers.md) содержат фрагменты данных мультимедиа, такие как видеокадры и образцы аудио, и используются для передачи данных между объектами.</span><span class="sxs-lookup"><span data-stu-id="dae87-118">[Media Buffers](media-buffers.md) hold chunks of media data, such as video frames and audio samples, and are used to transport data between objects.</span></span>
-   <span data-ttu-id="dae87-119">[Примеры носителей](media-samples.md) — это контейнеры для буферов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dae87-119">[Media Samples](media-samples.md) are containers for media buffers.</span></span> <span data-ttu-id="dae87-120">Они также содержат метаданные о буферах, например метки времени.</span><span class="sxs-lookup"><span data-stu-id="dae87-120">They also contain metadata about the buffers, such as time stamps.</span></span>

<span data-ttu-id="dae87-121">[Интерфейсы api Media Foundation платформы](media-foundation-platform-apis.md) предоставляют некоторые основные функции, используемые конвейером Media Foundation, например асинхронные обратные вызовы и рабочие очереди.</span><span class="sxs-lookup"><span data-stu-id="dae87-121">The [Media Foundation Platform APIs](media-foundation-platform-apis.md) provide some core functionality that is used by the Media Foundation pipeline, such as asynchronous callbacks and work queues.</span></span> <span data-ttu-id="dae87-122">Некоторым приложениям может потребоваться вызывать эти API напрямую; Кроме того, они понадобятся вам при реализации пользовательского источника, преобразования или приемника для Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dae87-122">Certain applications might need to call these APIs directly; also, you will need them if you implement a custom source, transform, or sink for Media Foundation.</span></span>

### <a name="media-pipeline"></a><span data-ttu-id="dae87-123">Конвейер мультимедиа</span><span class="sxs-lookup"><span data-stu-id="dae87-123">Media Pipeline</span></span>

<span data-ttu-id="dae87-124">Конвейер мультимедиа содержит три типа объектов, которые создают или обрабатывают данные мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="dae87-124">The media pipeline contains three types of object that generate or process media data:</span></span>

-   <span data-ttu-id="dae87-125">[Источники мультимедиа](media-sources.md) предоставляют данные в конвейер.</span><span class="sxs-lookup"><span data-stu-id="dae87-125">[Media Sources](media-sources.md) introduce data into the pipeline.</span></span> <span data-ttu-id="dae87-126">Источник мультимедиа может получать данные из локального файла, например из файла видео. из сетевого потока; или с устройства записи оборудования.</span><span class="sxs-lookup"><span data-stu-id="dae87-126">A media source might get data from a local file, such as a video file; from a network stream; or from a hardware capture device.</span></span>
-   <span data-ttu-id="dae87-127">[Media Foundation преобразования](media-foundation-transforms.md) (МФТС) обработка данных из потока.</span><span class="sxs-lookup"><span data-stu-id="dae87-127">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) process data from a stream.</span></span> <span data-ttu-id="dae87-128">Кодировщики и декодеры реализуются как МФТС.</span><span class="sxs-lookup"><span data-stu-id="dae87-128">Encoders and decoders are implemented as MFTs.</span></span>
-   <span data-ttu-id="dae87-129">[Приемники мультимедиа](media-sinks.md) потребляют данные; Например, отображение видео на экране, воспроизведение звука или запись данных в файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dae87-129">[Media Sinks](media-sinks.md) consume the data; for example, by showing video on the display, playing audio, or writing the data to a media file.</span></span>

<span data-ttu-id="dae87-130">Сторонние лица могут реализовать собственные источники, приемники и МФТС; Например, для поддержки новых форматов файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dae87-130">Third parties can implement their own custom sources, sinks, and MFTs; for example, to support new media file formats.</span></span>

<span data-ttu-id="dae87-131">[Сеанс мультимедиа](media-session.md) управляет потоком данных через конвейер и обрабатывает такие задачи, как контроль качества, синхронизация аудио/видео и реагирование на изменения формата.</span><span class="sxs-lookup"><span data-stu-id="dae87-131">The [Media Session](media-session.md) controls the flow of data through the pipeline, and handles tasks such as quality control, audio/video synchronization, and responding to format changes.</span></span>

### <a name="source-reader-and-sink-writer"></a><span data-ttu-id="dae87-132">Считыватель исходного кода и модуль записи приемника</span><span class="sxs-lookup"><span data-stu-id="dae87-132">Source Reader and Sink Writer</span></span>

<span data-ttu-id="dae87-133">[Средство чтения исходного кода](source-reader.md) и [модуль записи приемника](sink-writer.md) предоставляют альтернативный способ использования основных компонентов Media Foundation (источников мультимедиа, преобразований и приемников носителей).</span><span class="sxs-lookup"><span data-stu-id="dae87-133">The [Source Reader](source-reader.md) and [Sink Writer](sink-writer.md) provide an alternative way to use the basic Media Foundation components (media sources, transforms, and media sinks).</span></span> <span data-ttu-id="dae87-134">Модуль чтения исходного кода размещает источник мультимедиа и ноль или более декодеров, в то время как модуль записи приемника содержит приемник мультимедиа и ноль или более кодировщиков.</span><span class="sxs-lookup"><span data-stu-id="dae87-134">The source reader hosts a media source and zero or more decoders, while the sink writer hosts a media sink and zero or more encoders.</span></span> <span data-ttu-id="dae87-135">Модуль чтения исходного кода можно использовать для получения сжатых или несжатых данных из источника мультимедиа и использования модуля записи приемника для кодирования данных и отправки данных в приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dae87-135">You can use the source reader to get compressed or uncompressed data from a media source, and use the sink writer to encode data and send the data to a media sink.</span></span>

> [!Note]  
> <span data-ttu-id="dae87-136">Средство чтения исходного кода и модуль записи приемника доступны в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dae87-136">The source reader and sink writer are available in Windows 7.</span></span>

 

<span data-ttu-id="dae87-137">Эта модель программирования предоставляет приложению больший контроль над потоком данных, а также предоставляет приложению прямой доступ к данным из источника.</span><span class="sxs-lookup"><span data-stu-id="dae87-137">This programming model gives the application more control over the flow of data, and also gives the application direct access to the data from the source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dae87-138">См. также</span><span class="sxs-lookup"><span data-stu-id="dae87-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dae87-139">Media Foundation: основные понятия</span><span class="sxs-lookup"><span data-stu-id="dae87-139">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="dae87-140">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dae87-140">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 



