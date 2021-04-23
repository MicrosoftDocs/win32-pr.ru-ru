---
description: ДКСВА обработка видео включает функции графического оборудования, предназначенные для обработки несжатых видеоизображений. Службы обработки видео включают в себя дечередование и смешение видео.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Обработка видео ДКСВА
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539560"
---
# <a name="dxva-video-processing"></a><span data-ttu-id="6e15a-104">Обработка видео ДКСВА</span><span class="sxs-lookup"><span data-stu-id="6e15a-104">DXVA Video Processing</span></span>

<span data-ttu-id="6e15a-105">ДКСВА обработка видео включает функции графического оборудования, предназначенные для обработки несжатых видеоизображений.</span><span class="sxs-lookup"><span data-stu-id="6e15a-105">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="6e15a-106">Службы обработки видео включают в себя дечередование и смешение видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-106">Video processing services include deinterlacing and video mixing.</span></span>

<span data-ttu-id="6e15a-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="6e15a-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="6e15a-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="6e15a-108">Overview</span></span>](#overview)
-   [<span data-ttu-id="6e15a-109">Создание устройства обработки видео</span><span class="sxs-lookup"><span data-stu-id="6e15a-109">Creating a Video Processing Device</span></span>](#creating-a-video-processing-device)
    -   [<span data-ttu-id="6e15a-110">Получение указателя Идиректксвидеопроцессорсервице</span><span class="sxs-lookup"><span data-stu-id="6e15a-110">Get the IDirectXVideoProcessorService Pointer</span></span>](#get-the-idirectxvideoprocessorservice-pointer)
    -   [<span data-ttu-id="6e15a-111">Перечисление устройств обработки видео</span><span class="sxs-lookup"><span data-stu-id="6e15a-111">Enumerate the Video Processing Devices</span></span>](#enumerate-the-video-processing-devices)
    -   [<span data-ttu-id="6e15a-112">Перечислить форматы Render-Target</span><span class="sxs-lookup"><span data-stu-id="6e15a-112">Enumerate Render-Target Formats</span></span>](#enumerate-render-target-formats)
    -   [<span data-ttu-id="6e15a-113">Запрос возможностей устройства</span><span class="sxs-lookup"><span data-stu-id="6e15a-113">Query the Device Capabilities</span></span>](#query-the-device-capabilities)
    -   [<span data-ttu-id="6e15a-114">Создание устройства</span><span class="sxs-lookup"><span data-stu-id="6e15a-114">Create the Device</span></span>](#create-the-device)
-   [<span data-ttu-id="6e15a-115">Видеопроцесс Блит</span><span class="sxs-lookup"><span data-stu-id="6e15a-115">Video Process Blit</span></span>](#video-process-blit)
    -   [<span data-ttu-id="6e15a-116">Параметры Блит</span><span class="sxs-lookup"><span data-stu-id="6e15a-116">Blit Parameters</span></span>](#blit-parameters)
    -   [<span data-ttu-id="6e15a-117">Примеры входных данных</span><span class="sxs-lookup"><span data-stu-id="6e15a-117">Input Samples</span></span>](#input-samples)
-   [<span data-ttu-id="6e15a-118">Композиция изображений</span><span class="sxs-lookup"><span data-stu-id="6e15a-118">Image Composition</span></span>](#image-composition)
    -   [<span data-ttu-id="6e15a-119">Пример 1. пустых</span><span class="sxs-lookup"><span data-stu-id="6e15a-119">Example 1: Letterboxing</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="6e15a-120">Пример 2. изображения подпотока растяжения</span><span class="sxs-lookup"><span data-stu-id="6e15a-120">Example 2: Stretching Substream Images</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="6e15a-121">Пример 3. несоответствие высоты потока</span><span class="sxs-lookup"><span data-stu-id="6e15a-121">Example 3: Mismatched Stream Heights</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="6e15a-122">Пример 4. целевой прямоугольник меньше поверхности назначения</span><span class="sxs-lookup"><span data-stu-id="6e15a-122">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [<span data-ttu-id="6e15a-123">Пример 5. исходные прямоугольники</span><span class="sxs-lookup"><span data-stu-id="6e15a-123">Example 5: Source Rectangles</span></span>](#example-5-source-rectangles)
    -   [<span data-ttu-id="6e15a-124">Пример 6. пересечение прямоугольников назначения</span><span class="sxs-lookup"><span data-stu-id="6e15a-124">Example 6: Intersecting Destination Rectangles</span></span>](#example-6-intersecting-destination-rectangles)
    -   [<span data-ttu-id="6e15a-125">Пример 7. растяжение и обрезка видео</span><span class="sxs-lookup"><span data-stu-id="6e15a-125">Example 7: Stretching and Cropping Video</span></span>](#example-7-stretching-and-cropping-video)
-   [<span data-ttu-id="6e15a-126">Порядок входных образцов</span><span class="sxs-lookup"><span data-stu-id="6e15a-126">Input Sample Order</span></span>](#input-sample-order)
    -   [<span data-ttu-id="6e15a-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-127">Example 1</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="6e15a-128">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6e15a-128">Example 2</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="6e15a-129">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6e15a-129">Example 3</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="6e15a-130">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6e15a-130">Example 4</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
-   [<span data-ttu-id="6e15a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6e15a-131">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="6e15a-132">Обзор</span><span class="sxs-lookup"><span data-stu-id="6e15a-132">Overview</span></span>

<span data-ttu-id="6e15a-133">Графическое оборудование может использовать графический процессор (GPU) для обработки несжатых видео-изображений.</span><span class="sxs-lookup"><span data-stu-id="6e15a-133">Graphics hardware can use the graphics processing unit (GPU) to process uncompressed video images.</span></span> <span data-ttu-id="6e15a-134">Устройство *обработки видео* — это программный компонент, инкапсулирующий эти функции.</span><span class="sxs-lookup"><span data-stu-id="6e15a-134">A *video processing* device is a software component that encapsulates these functions.</span></span> <span data-ttu-id="6e15a-135">Приложения могут использовать устройство обработки видео для выполнения таких функций, как:</span><span class="sxs-lookup"><span data-stu-id="6e15a-135">Applications can use a video processing device to perform functions such as:</span></span>

-   <span data-ttu-id="6e15a-136">Дечередование и обратная чересстрочности</span><span class="sxs-lookup"><span data-stu-id="6e15a-136">Deinterlacing and inverse telecine</span></span>
-   <span data-ttu-id="6e15a-137">Смешивание подпотоков видео на основном видеоизображении</span><span class="sxs-lookup"><span data-stu-id="6e15a-137">Mixing video substreams onto the main video image</span></span>
-   <span data-ttu-id="6e15a-138">Настройка цвета (в cAmp) и фильтрация изображений</span><span class="sxs-lookup"><span data-stu-id="6e15a-138">Color adjustment (ProcAmp) and image filtering</span></span>
-   <span data-ttu-id="6e15a-139">Масштабирование изображения</span><span class="sxs-lookup"><span data-stu-id="6e15a-139">Image scaling</span></span>
-   <span data-ttu-id="6e15a-140">Преобразование цветового пространства</span><span class="sxs-lookup"><span data-stu-id="6e15a-140">Color-space conversion</span></span>
-   <span data-ttu-id="6e15a-141">Альфа-смешение</span><span class="sxs-lookup"><span data-stu-id="6e15a-141">Alpha blending</span></span>

<span data-ttu-id="6e15a-142">На следующей диаграмме показаны этапы конвейера обработки видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-142">The following diagram shows the stages in the video processing pipeline.</span></span> <span data-ttu-id="6e15a-143">Схема не предназначена для отображения фактической реализации.</span><span class="sxs-lookup"><span data-stu-id="6e15a-143">The diagram is not meant to show an actual implementation.</span></span> <span data-ttu-id="6e15a-144">Например, графический драйвер может сочетать несколько этапов в одну операцию.</span><span class="sxs-lookup"><span data-stu-id="6e15a-144">For example, the graphics driver might combine several stages into a single operation.</span></span> <span data-ttu-id="6e15a-145">Все эти операции можно выполнить в одном вызове устройства обработки видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-145">All of these operations can be performed in a single call to the video processing device.</span></span> <span data-ttu-id="6e15a-146">Некоторые показанные здесь этапы, такие как фильтрация шума и подробностей, могут не поддерживаться драйвером.</span><span class="sxs-lookup"><span data-stu-id="6e15a-146">Some stages shown here, such as noise and detail filtering, might not be supported by the driver.</span></span>

![Диаграмма, на которой показаны этапы обработки видео дксва.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

<span data-ttu-id="6e15a-148">Входные данные для конвейера обработки видео всегда включают *основной* поток видео, который содержит основные данные изображения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-148">The input to the video processing pipeline always includes a *primary* video stream, which contains the main image data.</span></span> <span data-ttu-id="6e15a-149">Основной поток видео определяет частоту кадров для выходного видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-149">The primary video stream determines the frame rate for the output video.</span></span> <span data-ttu-id="6e15a-150">Каждый кадр выходного видео вычисляется относительно входных данных из основного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-150">Each frame of the output video is calculated relative to the input data from the primary video stream.</span></span> <span data-ttu-id="6e15a-151">Пиксели в основном потоке всегда являются непрозрачными, без данных на основе альфа-пикселя.</span><span class="sxs-lookup"><span data-stu-id="6e15a-151">Pixels in the primary stream are always opaque, with no per-pixel alpha data.</span></span> <span data-ttu-id="6e15a-152">Основной видеопоток может быть прогрессивным или чередованием.</span><span class="sxs-lookup"><span data-stu-id="6e15a-152">The primary video stream can be progressive or interlaced.</span></span>

<span data-ttu-id="6e15a-153">При необходимости конвейер обработки видео может получить до 15 подпотоков видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-153">Optionally, the video processing pipeline can receive up to 15 video substreams.</span></span> <span data-ttu-id="6e15a-154">Подпоток содержит дополнительные данные изображения, такие как скрытые субтитры или DVD-диски.</span><span class="sxs-lookup"><span data-stu-id="6e15a-154">A substream contains auxiliary image data, such as closed captions or DVD subpictures.</span></span> <span data-ttu-id="6e15a-155">Эти изображения отображаются в основном видеопотоке и, как правило, не отображаются сами по себе.</span><span class="sxs-lookup"><span data-stu-id="6e15a-155">These images are displayed over the primary video stream, and are generally not meant to be shown by themselves.</span></span> <span data-ttu-id="6e15a-156">Изображения в подпотоке могут содержать альфа-данные для каждого пикселя и всегда прогрессивные кадры.</span><span class="sxs-lookup"><span data-stu-id="6e15a-156">Substream pictures can contain per-pixel alpha data, and are always progressive frames.</span></span> <span data-ttu-id="6e15a-157">Устройство обработки видео Alpha — смешивает изображения подпотока с текущим разотроеным кадром из основного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-157">The video processing device alpha-blends the substream images with the current deinterlaced frame from the primary video stream.</span></span>

<span data-ttu-id="6e15a-158">В оставшейся части этого раздела термин *изображение* используется для входных данных на устройство обработки видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-158">In the remainder of this topic, the term *picture* is used for the input data to a video processing device.</span></span> <span data-ttu-id="6e15a-159">Изображение может состоять из последовательного кадра, одного поля или двух полей с чередованием.</span><span class="sxs-lookup"><span data-stu-id="6e15a-159">A picture might consist of a progressive frame, a single field, or two interleaved fields.</span></span> <span data-ttu-id="6e15a-160">Выходные данные всегда имеют разкадровую рамку.</span><span class="sxs-lookup"><span data-stu-id="6e15a-160">The output is always a deinterlaced frame.</span></span>

<span data-ttu-id="6e15a-161">Видеодрайвер может реализовать несколько устройств обработки видео, чтобы предоставить различные наборы возможностей обработки видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-161">A video driver can implement more than one video processing device, to provide different sets of video processing capabilities.</span></span> <span data-ttu-id="6e15a-162">Устройства идентифицируются по идентификатору GUID.</span><span class="sxs-lookup"><span data-stu-id="6e15a-162">Devices are identified by GUID.</span></span> <span data-ttu-id="6e15a-163">Следующие идентификаторы GUID являются стандартными:</span><span class="sxs-lookup"><span data-stu-id="6e15a-163">The following GUIDs are predefined:</span></span>

-   <span data-ttu-id="6e15a-164">**DXVA2 \_ Видеопрокбобдевице**.</span><span class="sxs-lookup"><span data-stu-id="6e15a-164">**DXVA2\_VideoProcBobDevice**.</span></span> <span data-ttu-id="6e15a-165">Это устройство выполняет дечередование Боба.</span><span class="sxs-lookup"><span data-stu-id="6e15a-165">This device performs bob deinterlacing.</span></span>
-   <span data-ttu-id="6e15a-166">**DXVA2 \_ Видеопрокпрогрессиведевице**.</span><span class="sxs-lookup"><span data-stu-id="6e15a-166">**DXVA2\_VideoProcProgressiveDevice**.</span></span> <span data-ttu-id="6e15a-167">Это устройство используется, если видео содержит только прогрессивные кадры без чередующихся кадров.</span><span class="sxs-lookup"><span data-stu-id="6e15a-167">This device is used if the video contains only progressive frames, with no interlaced frames.</span></span> <span data-ttu-id="6e15a-168">(В некоторых видеоматериалах содержится сочетание последовательных и чередующихся кадров.</span><span class="sxs-lookup"><span data-stu-id="6e15a-168">(Some video content contains a mix of progressive and interlaced frames.</span></span> <span data-ttu-id="6e15a-169">Прогрессивное устройство не может использоваться для этого типа смешанного видеоматериала, так как для чередующихся кадров требуется шаг с чередованием.)</span><span class="sxs-lookup"><span data-stu-id="6e15a-169">The progressive device cannot be used for this kind of "mixed" video content, because a deinterlacing step is required for the interlaced frames.)</span></span>

<span data-ttu-id="6e15a-170">Каждый графический драйвер, поддерживающий обработку видео ДКСВА, должен реализовывать по крайней мере эти два устройства.</span><span class="sxs-lookup"><span data-stu-id="6e15a-170">Every graphics driver that supports DXVA video processing must implement at least these two devices.</span></span> <span data-ttu-id="6e15a-171">Графический драйвер может также предоставлять другие устройства, которые определяются с помощью идентификаторов GUID, определяемых драйвером.</span><span class="sxs-lookup"><span data-stu-id="6e15a-171">The graphics driver may also provide other devices, which are identified by driver-specific GUIDs.</span></span> <span data-ttu-id="6e15a-172">Например, драйвер может реализовать собственный алгоритм дечередования, который обеспечивает более качественные выходные данные, чем Боб.</span><span class="sxs-lookup"><span data-stu-id="6e15a-172">For example, a driver might implement a proprietary deinterlacing algorithm that produces better quality output than bob deinterlacing.</span></span> <span data-ttu-id="6e15a-173">Некоторые алгоритмы разчередования могут потребовать, чтобы изображения прямого или обратной ссылки из первичного потока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-173">Some deinterlacing algorithms may require forward or backward reference pictures from the primary stream.</span></span> <span data-ttu-id="6e15a-174">В этом случае вызывающий объект должен предоставить эти изображения драйверу в правильной последовательности, как описано далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="6e15a-174">If so, the caller must provide these pictures to the driver in the correct sequence, as described later in this section.</span></span>

<span data-ttu-id="6e15a-175">Также предоставляется справочное программное устройство.</span><span class="sxs-lookup"><span data-stu-id="6e15a-175">A reference software device is also provided.</span></span> <span data-ttu-id="6e15a-176">Программное устройство оптимизировано для качества, а не для скорости и может быть недостаточным для обработки видео в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="6e15a-176">The software device is optimized for quality rather than speed, and may not be adequate for real-time video processing.</span></span> <span data-ttu-id="6e15a-177">На справочном программном устройстве используется значение GUID DXVA2 \_ видеопроксофтваредевице.</span><span class="sxs-lookup"><span data-stu-id="6e15a-177">The reference software device uses the GUID value DXVA2\_VideoProcSoftwareDevice.</span></span>

## <a name="creating-a-video-processing-device"></a><span data-ttu-id="6e15a-178">Создание устройства обработки видео</span><span class="sxs-lookup"><span data-stu-id="6e15a-178">Creating a Video Processing Device</span></span>

<span data-ttu-id="6e15a-179">Перед использованием обработки видео ДКСВА приложение должно создать устройство обработки видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-179">Before using DXVA video processing, the application must create a video processing device.</span></span> <span data-ttu-id="6e15a-180">Ниже приведен краткий обзор шагов, которые более подробно описаны в оставшейся части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="6e15a-180">Here is a brief outline of the steps, which are explained in greater detail in the remainder of this section:</span></span>

1.  <span data-ttu-id="6e15a-181">Получает указатель на интерфейс [**идиректксвидеопроцессорсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-181">Get a pointer to the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface.</span></span>
2.  <span data-ttu-id="6e15a-182">Создайте описание формата видео для основного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-182">Create a description of the video format for the primary video stream.</span></span> <span data-ttu-id="6e15a-183">Это описание используется для получения списка устройств обработки видео, поддерживающих формат видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-183">Use this description to get a list of the video processing devices that support the video format.</span></span> <span data-ttu-id="6e15a-184">Устройства идентифицируются по идентификатору GUID.</span><span class="sxs-lookup"><span data-stu-id="6e15a-184">Devices are identified by GUID.</span></span>
3.  <span data-ttu-id="6e15a-185">Для конкретного устройства получите список форматов подготовки к просмотру, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="6e15a-185">For a particular device, get a list of render-target formats supported by the device.</span></span> <span data-ttu-id="6e15a-186">Форматы возвращаются в виде списка значений **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="6e15a-186">The formats are returned as a list of **D3DFORMAT** values.</span></span> <span data-ttu-id="6e15a-187">Если вы планируете смешивать подпотоки, получите также список поддерживаемых форматов подпотоков.</span><span class="sxs-lookup"><span data-stu-id="6e15a-187">If you plan to mix substreams, get a list of the supported substream formats as well.</span></span>
4.  <span data-ttu-id="6e15a-188">Запросите возможности каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="6e15a-188">Query the capabilities of each device.</span></span>
5.  <span data-ttu-id="6e15a-189">Создайте устройство для обработки видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-189">Create the video processing device.</span></span>

<span data-ttu-id="6e15a-190">Иногда можно опустить некоторые из этих шагов.</span><span class="sxs-lookup"><span data-stu-id="6e15a-190">Sometimes you can omit some of these steps.</span></span> <span data-ttu-id="6e15a-191">Например, вместо получения списка форматов для подготовки к просмотру можно просто попытаться создать устройство обработки видео с предпочтительным форматом и проверить успешность его выполнения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-191">For example, instead of getting the list of render-target formats, you could simply try creating the video processing device with your preferred format, and see if it succeeds.</span></span> <span data-ttu-id="6e15a-192">Вероятнее всего, общий формат, такой как D3DFMT \_ X8R8G8B8, может быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="6e15a-192">A common format such as D3DFMT\_X8R8G8B8 is likely to succeed.</span></span>

<span data-ttu-id="6e15a-193">В оставшейся части этого раздела подробно описаны эти действия.</span><span class="sxs-lookup"><span data-stu-id="6e15a-193">The remainder of this section describes these steps in detail.</span></span>

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a><span data-ttu-id="6e15a-194">Получение указателя Идиректксвидеопроцессорсервице</span><span class="sxs-lookup"><span data-stu-id="6e15a-194">Get the IDirectXVideoProcessorService Pointer</span></span>

<span data-ttu-id="6e15a-195">Интерфейс [**идиректксвидеопроцессорсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) получается с устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6e15a-195">The [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface is obtained from the Direct3D device.</span></span> <span data-ttu-id="6e15a-196">Есть два способа получить указатель на этот интерфейс:</span><span class="sxs-lookup"><span data-stu-id="6e15a-196">There are two ways to get a pointer to this interface:</span></span>

-   <span data-ttu-id="6e15a-197">С устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6e15a-197">From a Direct3D device.</span></span>
-   <span data-ttu-id="6e15a-198">Из [Диспетчер устройств Direct3D](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="6e15a-198">From the [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="6e15a-199">Если у вас есть указатель на устройство Direct3D, можно получить указатель [**идиректксвидеопроцессорсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , вызвав функцию [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-199">If you have a pointer to a Direct3D device, you can get an [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer by calling the [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) function.</span></span> <span data-ttu-id="6e15a-200">Передайте указатель на интерфейс **IDirect3DDevice9а** устройства и укажите **IID \_ идиректксвидеопроцессорсервице** для параметра *riid* , как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="6e15a-200">Pass in a pointer to the device's **IDirect3DDevice9** interface, and specify **IID\_IDirectXVideoProcessorService** for the *riid* parameter, as shown in the following code:</span></span>


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



<span data-ttu-id="6e15a-201">в некоторых случаях один объект создает устройство Direct3D, а затем использует его совместно с другими объектами через [Диспетчер устройств Direct3D](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="6e15a-201">n some cases, one object creates the Direct3D device and then shares it with other objects through the [Direct3D Device Manager](direct3d-device-manager.md).</span></span> <span data-ttu-id="6e15a-202">В этом случае можно вызвать [**IDirect3DDeviceManager9:: жетвидеосервице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) в диспетчере устройств, чтобы получить указатель [**идиректксвидеопроцессорсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="6e15a-202">In this situation, you can call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) on the device manager to get the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer, as shown in the following code:</span></span>


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a><span data-ttu-id="6e15a-203">Перечисление устройств обработки видео</span><span class="sxs-lookup"><span data-stu-id="6e15a-203">Enumerate the Video Processing Devices</span></span>

<span data-ttu-id="6e15a-204">Чтобы получить список устройств обработки видео, заполните структуру [**DXVA2 \_ видеодеск**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) форматом основного видеопотока и передайте эту структуру методу [**идиректксвидеопроцессорсервице:: жетвидеопроцессордевицегуидс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-204">To get a list of video processing devices, fill in a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure with the format of the primary video stream, and pass this structure to the [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method.</span></span> <span data-ttu-id="6e15a-205">Метод возвращает массив идентификаторов GUID, по одному для каждого устройства обработки видео, которое можно использовать с этим видеоформатом.</span><span class="sxs-lookup"><span data-stu-id="6e15a-205">The method returns an array of GUIDs, one for each video processing device that can be used with this video format.</span></span>

<span data-ttu-id="6e15a-206">Рассмотрим приложение, которое визуализирует видеопоток в формате YUY2, используя определение BT. 709 для цвета YUV с частотой кадров в 29,97 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="6e15a-206">Consider an application that renders a video stream in YUY2 format, using the BT.709 definition of YUV color, with a frame rate of 29.97 frames per second.</span></span> <span data-ttu-id="6e15a-207">Предположим, что видеоматериал состоит только из последовательных кадров.</span><span class="sxs-lookup"><span data-stu-id="6e15a-207">Assume that the video content consists entirely of progressive frames.</span></span> <span data-ttu-id="6e15a-208">В следующем фрагменте кода показано, как заполнить описание формата и получить идентификаторы GUID устройства:</span><span class="sxs-lookup"><span data-stu-id="6e15a-208">The following code fragment shows how to fill in the format description and get the device GUIDs:</span></span>


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



<span data-ttu-id="6e15a-209">Код для этого примера взят из примера пакета SDK для [DXVA2 \_ видеопрок](dxva2-videoproc-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-209">The code for this example is taken from the [DXVA2\_VideoProc](dxva2-videoproc-sample.md) SDK sample.</span></span>

<span data-ttu-id="6e15a-210">Массив *пгуидс* в этом примере выделяется методом [**жетвидеопроцессордевицегуидс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , поэтому приложение должно освободить массив путем вызова [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="6e15a-210">The *pGuids* array in this example is allocated by the [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method, so the application must free the array by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="6e15a-211">Оставшиеся действия можно выполнить с помощью любого идентификатора GUID устройства, возвращенного этим методом.</span><span class="sxs-lookup"><span data-stu-id="6e15a-211">The remaining steps can be performed using any of the device GUIDs returned by this method.</span></span>

### <a name="enumerate-render-target-formats"></a><span data-ttu-id="6e15a-212">Перечислить форматы Render-Target</span><span class="sxs-lookup"><span data-stu-id="6e15a-212">Enumerate Render-Target Formats</span></span>

<span data-ttu-id="6e15a-213">Чтобы получить список форматов подготовки к просмотру, поддерживаемых устройством, передайте GUID устройства и структуру [**DXVA2 \_ видеодеск**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) в метод [**идиректксвидеопроцессорсервице:: жетвидеопроцессоррендертаржетс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="6e15a-213">To get the list of render-target formats supported by the device, pass the device GUID and the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure to the [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) method, as shown in the following code:</span></span>


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="6e15a-214">Метод возвращает массив значений **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="6e15a-214">The method returns an array of **D3DFORMAT** values.</span></span> <span data-ttu-id="6e15a-215">В этом примере, где тип входных данных — YUY2, типичным списком форматов может быть D3DFMT \_ X8R8G8B8 (32-bit RGB) и D3DMFT \_ YUY2 (входной формат).</span><span class="sxs-lookup"><span data-stu-id="6e15a-215">In this example, where the input type is YUY2, a typical list of formats might be D3DFMT\_X8R8G8B8 (32-bit RGB) and D3DMFT\_YUY2 (the input format).</span></span> <span data-ttu-id="6e15a-216">Однако точный список будет зависеть от драйвера.</span><span class="sxs-lookup"><span data-stu-id="6e15a-216">However, the exact list will depend on the driver.</span></span>

<span data-ttu-id="6e15a-217">Список доступных форматов для подпотоков может изменяться в зависимости от формата целевого объекта подготовки к просмотру и входного формата.</span><span class="sxs-lookup"><span data-stu-id="6e15a-217">The list of available formats for the substreams can vary depending on the render-target format and the input format.</span></span> <span data-ttu-id="6e15a-218">Чтобы получить список форматов подпотоков, передайте GUID устройства, структуру формата и формат целевого объекта в метод [**идиректксвидеопроцессорсервице:: жетвидеопроцессорсубстреамформатс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="6e15a-218">To get the list of substream formats, pass the device GUID, the format structure, and the render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) method, as shown in the following code:</span></span>


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="6e15a-219">Этот метод возвращает другой массив значений **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="6e15a-219">This method returns another array of **D3DFORMAT** values.</span></span> <span data-ttu-id="6e15a-220">Типичными форматами подпотоков являются АЙУВ и AI44.</span><span class="sxs-lookup"><span data-stu-id="6e15a-220">Typical substream formats are AYUV and AI44.</span></span>

### <a name="query-the-device-capabilities"></a><span data-ttu-id="6e15a-221">Запрос возможностей устройства</span><span class="sxs-lookup"><span data-stu-id="6e15a-221">Query the Device Capabilities</span></span>

<span data-ttu-id="6e15a-222">Чтобы получить возможности конкретного устройства, передайте в метод [**идиректксвидеопроцессорсервице:: жетвидеопроцессоркапс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) идентификатор GUID устройства, структуру формата и формат целевого объекта подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="6e15a-222">To get the capabilities of a particular device, pass the device GUID, the format structure, and a render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) method.</span></span> <span data-ttu-id="6e15a-223">Метод заполняет структуру структуры [**DXVA2 \_ видеопроцессоркапс**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) с помощью возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="6e15a-223">The method fills in a [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure structure with the device capabilities.</span></span>


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a><span data-ttu-id="6e15a-224">Создание устройства</span><span class="sxs-lookup"><span data-stu-id="6e15a-224">Create the Device</span></span>

<span data-ttu-id="6e15a-225">Чтобы создать устройство обработки видео, вызовите метод [**идиректксвидеопроцессорсервице:: креатевидеопроцессор**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span><span class="sxs-lookup"><span data-stu-id="6e15a-225">To create the video processing device, call [**IDirectXVideoProcessorService::CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span></span> <span data-ttu-id="6e15a-226">Входными данными для этого метода являются GUID устройства, описание формата, формат целевого объекта подготовки и максимальное количество вложенных потоков, которые планируется смешивать.</span><span class="sxs-lookup"><span data-stu-id="6e15a-226">The input to this method is the device GUID, the format description, the render-target format, and the maximum number of substreams that you plan to mix.</span></span> <span data-ttu-id="6e15a-227">Метод возвращает указатель на интерфейс [**идиректксвидеопроцессор**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) , который представляет устройство обработки видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-227">The method returns a pointer to the [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) interface, which represents the video processing device.</span></span>


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a><span data-ttu-id="6e15a-228">Видеопроцесс Блит</span><span class="sxs-lookup"><span data-stu-id="6e15a-228">Video Process Blit</span></span>

<span data-ttu-id="6e15a-229">Основная операция обработки видео — это *Блит обработки видео*.</span><span class="sxs-lookup"><span data-stu-id="6e15a-229">The main video processing operation is the *video processing blit*.</span></span> <span data-ttu-id="6e15a-230">( *Блит* — это любая операция, объединяющая два или более точечных рисунка в одно растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="6e15a-230">(A *blit* is any operation that combines two or more bitmaps into a single bitmap.</span></span> <span data-ttu-id="6e15a-231">Блит обработка видео сочетает входные рисунки для создания выходного кадра.) Чтобы выполнить Блит обработки видео, вызовите [**идиректксвидеопроцессор:: видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="6e15a-231">A video processing blit combines input pictures to create an output frame.) To perform a video processing blit, call [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="6e15a-232">Этот метод передает набор видеороликов на устройство обработки видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-232">This method passes a set of video samples to the video processing device.</span></span> <span data-ttu-id="6e15a-233">В ответ устройство обработки видео обрабатывает входные изображения и создает один выходной кадр.</span><span class="sxs-lookup"><span data-stu-id="6e15a-233">In response, the video processing device processes the input pictures and generates one output frame.</span></span> <span data-ttu-id="6e15a-234">Обработка может включать в себя дечередование, преобразование цветового пространства и смешивание подпотоков.</span><span class="sxs-lookup"><span data-stu-id="6e15a-234">Processing can include deinterlacing, color-space conversion, and substream mixing.</span></span> <span data-ttu-id="6e15a-235">Выходные данные записываются на конечную поверхность, предоставленную вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="6e15a-235">The output is written to a destination surface provided by the caller.</span></span>

<span data-ttu-id="6e15a-236">Метод [**видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="6e15a-236">The [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method takes the following parameters:</span></span>

-   <span data-ttu-id="6e15a-237">*pRT* указывает на поверхность целевого объекта отрисовки **IDirect3DSurface9** , которая будет принимать обработанный кадр видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-237">*pRT* points to an **IDirect3DSurface9** render target surface that will receive the processed video frame.</span></span>
-   <span data-ttu-id="6e15a-238">*пблтпарамс* указывает на структуру [**DXVA2 \_ видеопроцессблтпарамс**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) , которая задает параметры для Блит.</span><span class="sxs-lookup"><span data-stu-id="6e15a-238">*pBltParams* points to a [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure that specifies the parameters for the blit.</span></span>
-   <span data-ttu-id="6e15a-239">*псамплес* — это адрес массива структур [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-239">*pSamples* is the address of an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="6e15a-240">Эти структуры содержат входные образцы для Блит.</span><span class="sxs-lookup"><span data-stu-id="6e15a-240">These structures contain the input samples for the blit.</span></span>
-   <span data-ttu-id="6e15a-241">*Нумсамплес* задает размер массива *псамплес* .</span><span class="sxs-lookup"><span data-stu-id="6e15a-241">*NumSamples* gives the size of the *pSamples* array.</span></span>
-   <span data-ttu-id="6e15a-242">*Зарезервированный* параметр зарезервирован и должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6e15a-242">The *Reserved* parameter is reserved and should be set to **NULL**.</span></span>

<span data-ttu-id="6e15a-243">В массиве *псамплес* вызывающий объект должен предоставить следующие входные примеры:</span><span class="sxs-lookup"><span data-stu-id="6e15a-243">In the *pSamples* array, the caller must provide the following input samples:</span></span>

-   <span data-ttu-id="6e15a-244">Текущее изображение из основного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-244">The current picture from the primary video stream.</span></span>
-   <span data-ttu-id="6e15a-245">Ссылки на рисунки вперед и назад, если это требуется для алгоритма дечередования.</span><span class="sxs-lookup"><span data-stu-id="6e15a-245">Forward and backward reference pictures, if required by the deinterlacing algorithm.</span></span>
-   <span data-ttu-id="6e15a-246">Ноль или больше изображений подпотока, не более 15 подпотоков.</span><span class="sxs-lookup"><span data-stu-id="6e15a-246">Zero or more substream pictures, up to a maximum of 15 substreams.</span></span>

<span data-ttu-id="6e15a-247">Драйверу требуется, чтобы этот массив наследовался в определенном порядке, как описано в статье [Порядок входных образцов](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="6e15a-247">The driver expects this array to be in a particular order, as described in [Input Sample Order](#input-sample-order).</span></span>

### <a name="blit-parameters"></a><span data-ttu-id="6e15a-248">Параметры Блит</span><span class="sxs-lookup"><span data-stu-id="6e15a-248">Blit Parameters</span></span>

<span data-ttu-id="6e15a-249">Структура [**DXVA2 \_ видеопроцессблтпарамс**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) содержит общие параметры для Блит.</span><span class="sxs-lookup"><span data-stu-id="6e15a-249">The [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure contains general parameters for the blit.</span></span> <span data-ttu-id="6e15a-250">Наиболее важные параметры хранятся в следующих членах структуры:</span><span class="sxs-lookup"><span data-stu-id="6e15a-250">The most important parameters are stored in the following members of the structure:</span></span>

-   <span data-ttu-id="6e15a-251">**Таржетфраме** — время презентации выходного кадра.</span><span class="sxs-lookup"><span data-stu-id="6e15a-251">**TargetFrame** is the presentation time of the output frame.</span></span> <span data-ttu-id="6e15a-252">Для последовательного содержимого это время должно совпадать с временем начала текущего кадра из основного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-252">For progressive content, this time must equal the start time for the current frame from the primary video stream.</span></span> <span data-ttu-id="6e15a-253">Это время указано в примере **Start** элемента структуры [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) для этого входного примера.</span><span class="sxs-lookup"><span data-stu-id="6e15a-253">This time is specified in the **Start** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure for that input sample.</span></span>

    <span data-ttu-id="6e15a-254">Для содержимого с чередованием рамка с двумя полями с чередованием создает два выходных кадра с чередованием.</span><span class="sxs-lookup"><span data-stu-id="6e15a-254">For interlaced content, a frame with two interleaved fields produces two deinterlaced output frames.</span></span> <span data-ttu-id="6e15a-255">В первом выходном кадре время презентации должно совпадать с временем начала текущего изображения в основном видеопотоке, как и в прогрессивном содержимом.</span><span class="sxs-lookup"><span data-stu-id="6e15a-255">On the first output frame, the presentation time must equal the start time of the current picture in the primary video stream, just like progressive content.</span></span> <span data-ttu-id="6e15a-256">Во втором выходном кадре время начала должно равняться средней точке между временем начала текущего изображения в основном видеопотоке и временем начала следующего изображения в потоке.</span><span class="sxs-lookup"><span data-stu-id="6e15a-256">On the second output frame, the start time must equal the midpoint between the start time of the current picture in the primary video stream and the start time of the next picture in the stream.</span></span> <span data-ttu-id="6e15a-257">Например, если входное видео содержит 25 кадров в секунду (50 полей в секунду), выходные кадры будут иметь отметки времени, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6e15a-257">For example, if the input video is 25 frames per second (50 fields per second), the output frames will have the time stamps shown in the following table.</span></span> <span data-ttu-id="6e15a-258">Метки времени отображаются в единицах 100 наносекунд.</span><span class="sxs-lookup"><span data-stu-id="6e15a-258">Time stamps are shown in units of 100 nanoseconds.</span></span>

    

    | <span data-ttu-id="6e15a-259">Рисунок входных данных</span><span class="sxs-lookup"><span data-stu-id="6e15a-259">Input picture</span></span> | <span data-ttu-id="6e15a-260">**Таржетфраме** (1)</span><span class="sxs-lookup"><span data-stu-id="6e15a-260">**TargetFrame** (1)</span></span> | <span data-ttu-id="6e15a-261">**Таржетфраме** (2)</span><span class="sxs-lookup"><span data-stu-id="6e15a-261">**TargetFrame** (2)</span></span> |
    |---------------|---------------------|---------------------|
    | <span data-ttu-id="6e15a-262">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-262">0</span></span>             | <span data-ttu-id="6e15a-263">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-263">0</span></span>                   | <span data-ttu-id="6e15a-264">200 000</span><span class="sxs-lookup"><span data-stu-id="6e15a-264">200000</span></span>              |
    | <span data-ttu-id="6e15a-265">400000</span><span class="sxs-lookup"><span data-stu-id="6e15a-265">400000</span></span>        | <span data-ttu-id="6e15a-266">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-266">0</span></span>                   | <span data-ttu-id="6e15a-267">600 000</span><span class="sxs-lookup"><span data-stu-id="6e15a-267">600000</span></span>              |
    | <span data-ttu-id="6e15a-268">800000</span><span class="sxs-lookup"><span data-stu-id="6e15a-268">800000</span></span>        | <span data-ttu-id="6e15a-269">800000</span><span class="sxs-lookup"><span data-stu-id="6e15a-269">800000</span></span>              | <span data-ttu-id="6e15a-270">1000000</span><span class="sxs-lookup"><span data-stu-id="6e15a-270">1000000</span></span>             |
    | <span data-ttu-id="6e15a-271">1200000</span><span class="sxs-lookup"><span data-stu-id="6e15a-271">1200000</span></span>       | <span data-ttu-id="6e15a-272">1200000</span><span class="sxs-lookup"><span data-stu-id="6e15a-272">1200000</span></span>             | <span data-ttu-id="6e15a-273">1400000</span><span class="sxs-lookup"><span data-stu-id="6e15a-273">1400000</span></span>             |

    

     

    <span data-ttu-id="6e15a-274">Если чередование содержимого состоит из одиночных полей, а не полей с чередованием, то время вывода всегда совпадает со временем ввода, как в случае с прогрессивным содержимым.</span><span class="sxs-lookup"><span data-stu-id="6e15a-274">If interlaced content consists of single fields rather than interleaved fields, the output times always match the input times, as with progressive content.</span></span>

-   <span data-ttu-id="6e15a-275">**Таржетрект** определяет прямоугольную область в области назначения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-275">**TargetRect** defines a rectangular region within the destination surface.</span></span> <span data-ttu-id="6e15a-276">Блит будет записывать выходные данные в этот регион.</span><span class="sxs-lookup"><span data-stu-id="6e15a-276">The blit will write the output to this region.</span></span> <span data-ttu-id="6e15a-277">В частности, каждый пиксель в **таржетрект** будет изменен, и никакие Пиксели за пределами **таржетрект** будут изменены.</span><span class="sxs-lookup"><span data-stu-id="6e15a-277">Specifically, every pixel inside **TargetRect** will be modified, and no pixels outside of **TargetRect** will be modified.</span></span> <span data-ttu-id="6e15a-278">Целевой прямоугольник определяет ограничивающий прямоугольник для всех входных потоков видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-278">The target rectangle defines the bounding rectangle for all of the input video streams.</span></span> <span data-ttu-id="6e15a-279">Размещение отдельных потоков внутри этого прямоугольника осуществляется с помощью параметра *Псамплес* [**Идиректксвидеопроцессор:: видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="6e15a-279">Placement of individual streams within that rectangle is controlled through the *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span>
-   <span data-ttu-id="6e15a-280">**BackgroundColor** задает цвет фона везде, где не отображается изображение видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-280">**BackgroundColor** gives the color of the background wherever no video image appears.</span></span> <span data-ttu-id="6e15a-281">Например, когда изображение видео размером 16 x 9 отображается в области 4 x 3 (пустых), области леттербоксед отображаются с цветом фона.</span><span class="sxs-lookup"><span data-stu-id="6e15a-281">For example, when a 16 x 9 video image is displayed within a 4 x 3 area (letterboxing), the letterboxed regions are displayed with the background color.</span></span> <span data-ttu-id="6e15a-282">Цвет фона применяется только в пределах целевого прямоугольника (**таржетрект**).</span><span class="sxs-lookup"><span data-stu-id="6e15a-282">The background color applies only within the target rectangle (**TargetRect**).</span></span> <span data-ttu-id="6e15a-283">Все пиксели за пределами **таржетрект** не изменяются.</span><span class="sxs-lookup"><span data-stu-id="6e15a-283">Any pixels outside of **TargetRect** are not modified.</span></span>
-   <span data-ttu-id="6e15a-284">**Дестформат** описывает цветовое пространство для выходного видео, например, используется ли цвет ITU-R BT. 709 или BT. 601.</span><span class="sxs-lookup"><span data-stu-id="6e15a-284">**DestFormat** describes the color space for the output video—for example, whether ITU-R BT.709 or BT.601 color is used.</span></span> <span data-ttu-id="6e15a-285">Эти сведения могут повлиять на отображение изображения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-285">This information can affect how the image is displayed.</span></span> <span data-ttu-id="6e15a-286">Дополнительные сведения см. в разделе [Расширенные сведения о цвете](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="6e15a-286">For more information, see [Extended Color Information](extended-color-information.md).</span></span>

<span data-ttu-id="6e15a-287">Другие параметры описаны на справочной странице структуры [**DXVA2 \_ видеопроцессблтпарамс**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-287">Other parameters are described on the reference page for the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="input-samples"></a><span data-ttu-id="6e15a-288">Примеры входных данных</span><span class="sxs-lookup"><span data-stu-id="6e15a-288">Input Samples</span></span>

<span data-ttu-id="6e15a-289">Параметр *псамплес* объекта [**Идиректксвидеопроцессор:: видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) указывает на массив структур [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-289">The *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) points to an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="6e15a-290">Каждая из этих структур содержит сведения о одном входном образце и указателе на поверхность Direct3D, содержащую пример.</span><span class="sxs-lookup"><span data-stu-id="6e15a-290">Each of these structures contains information about one input sample and a pointer to the Direct3D surface that contains the sample.</span></span> <span data-ttu-id="6e15a-291">Каждый пример является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="6e15a-291">Each sample is one of the following:</span></span>

-   <span data-ttu-id="6e15a-292">Текущее изображение из основного потока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-292">The current picture from the primary stream.</span></span>
-   <span data-ttu-id="6e15a-293">Изображение прямой или обратной ссылки из основного потока, используемое для дечередования.</span><span class="sxs-lookup"><span data-stu-id="6e15a-293">A forward or backward reference picture from the primary stream, used for deinterlacing.</span></span>
-   <span data-ttu-id="6e15a-294">Изображение подпотока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-294">A substream picture.</span></span>

<span data-ttu-id="6e15a-295">Точный порядок, в котором образцы должны отображаться в массиве, описывается далее в разделе [Порядок входных примеров](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="6e15a-295">The exact order in which the samples must appear in the array is described later, in the section [Input Sample Order](#input-sample-order).</span></span>

<span data-ttu-id="6e15a-296">Можно предоставить до 15 графических подпотоков, хотя большинству приложений для видео требуется только один подпоток.</span><span class="sxs-lookup"><span data-stu-id="6e15a-296">Up to 15 substream pictures can be provided, although most video applications need only one substream, at the most.</span></span> <span data-ttu-id="6e15a-297">Число подпотоков может изменяться при каждом вызове [**видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="6e15a-297">The number of substreams can change with each call to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="6e15a-298">Изображения из подпотока обозначаются установкой элемента **самплеформат. самплеформат** структуры [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) равным DXVA2 \_ самплесубстреам.</span><span class="sxs-lookup"><span data-stu-id="6e15a-298">Substream pictures are indicated by setting the **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure equal to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="6e15a-299">Для основного видеопотока этот член описывает чересстрочную развертку входного видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-299">For the primary video stream, this member describes the interlacing of the input video.</span></span> <span data-ttu-id="6e15a-300">Дополнительные сведения см. в разделе [**DXVA2 \_ самплеформат**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="6e15a-300">For more information, see [**DXVA2\_SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) enumeration.</span></span>

<span data-ttu-id="6e15a-301">Для основного видеопотока **начальный** и **конечный** элементы структуры [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) дают время начала и окончания входного примера.</span><span class="sxs-lookup"><span data-stu-id="6e15a-301">For the primary video stream, the **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the start and end times of the input sample.</span></span> <span data-ttu-id="6e15a-302">Для изображений подпотока установите эти значения равными нулю, так как время презентации всегда вычисляется из основного потока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-302">For substream pictures, set these values to zero, because the presentation time is always calculated from the primary stream.</span></span> <span data-ttu-id="6e15a-303">Приложение отвечает за отслеживание, когда необходимо представить все изображение подпотока и отправить его в [**видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) в нужное время.</span><span class="sxs-lookup"><span data-stu-id="6e15a-303">The application is responsible for tracking when each substream picture should be presented and submitting it to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) at the proper time.</span></span>

<span data-ttu-id="6e15a-304">Два прямоугольника определяют, как будет располагаться исходное видео для каждого потока:</span><span class="sxs-lookup"><span data-stu-id="6e15a-304">Two rectangles define how the source video is positioned for each stream:</span></span>

-   <span data-ttu-id="6e15a-305">Элемент **SrcRect** структуры [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) указывает *Исходный прямоугольник*, прямоугольную область исходного изображения, которая будет отображаться в составном кадре выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6e15a-305">The **SrcRect** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure specifies the *source rectangle*, a rectangular region of the source picture that will appear in the composited output frame.</span></span> <span data-ttu-id="6e15a-306">Чтобы обрезать изображение, присвойте этому свойству значение меньше размера кадра.</span><span class="sxs-lookup"><span data-stu-id="6e15a-306">To crop the picture, set this to a value smaller than the frame size.</span></span> <span data-ttu-id="6e15a-307">В противном случае задайте значение, равное размеру кадра.</span><span class="sxs-lookup"><span data-stu-id="6e15a-307">Otherwise, set it equal to the frame size.</span></span>
-   <span data-ttu-id="6e15a-308">Элемент **DstRect** той же структуры задает *прямоугольник назначения*, прямоугольную область назначения, в которой будет отображаться кадр видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-308">The **DstRect** member of the same structure specifies the *destination rectangle*, a rectangular region of the destination surface where the video frame will appear.</span></span>

<span data-ttu-id="6e15a-309">Драйвер блитс Пиксели из исходного прямоугольника в прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-309">The driver blits pixels from the source rectangle into the destination rectangle.</span></span> <span data-ttu-id="6e15a-310">Два прямоугольника могут иметь разные размеры или пропорции. драйвер будет масштабировать образ по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="6e15a-310">The two rectangles can have different sizes or aspect ratios; the driver will scale the image as needed.</span></span> <span data-ttu-id="6e15a-311">Более того, каждый входной поток может использовать другой коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="6e15a-311">Moreover, each input stream can use a different scaling factor.</span></span> <span data-ttu-id="6e15a-312">По сути, масштабирование может потребоваться для получения правильных пропорций в выходном кадре.</span><span class="sxs-lookup"><span data-stu-id="6e15a-312">In fact, scaling might be necessary to produce the correct aspect ratio in the output frame.</span></span> <span data-ttu-id="6e15a-313">Драйвер не принимает пропорции пикселя источника в учетную запись, поэтому если в исходном изображении используются неквадратные Пиксели, то приложение может вычислить правильный конечный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="6e15a-313">The driver does not take the source's pixel aspect ratio into account, so if the source image uses non-square pixels, it is up to the application to calculate the correct destination rectangle.</span></span>

<span data-ttu-id="6e15a-314">Предпочтительные форматы подпотока — АЙУВ и AI44.</span><span class="sxs-lookup"><span data-stu-id="6e15a-314">The preferred substream formats are AYUV and AI44.</span></span> <span data-ttu-id="6e15a-315">Последний — это формат с использованием формата в виде палет с 16 цветами.</span><span class="sxs-lookup"><span data-stu-id="6e15a-315">The latter is a palletized format with 16 colors.</span></span> <span data-ttu-id="6e15a-316">Записи палитры задаются в элементе **PAL** структуры [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-316">Palette entries are specified in the **Pal** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span> <span data-ttu-id="6e15a-317">(Если исходный видеоформат изначально выражается как тип носителя Media Foundation, записи палитры хранятся в атрибуте [**Palette- \_ \_ Палитра MF**](mf-mt-palette-attribute.md) .) Для форматов, не являющихся палетами, очистите этот массив до нуля.</span><span class="sxs-lookup"><span data-stu-id="6e15a-317">(If your source video format is originally expressed as a Media Foundation media type, the palette entries are stored in the [**MF\_MT\_PALETTE**](mf-mt-palette-attribute.md) attribute.) For non-palletized formats, clear this array to zero.</span></span>

## <a name="image-composition"></a><span data-ttu-id="6e15a-318">Композиция изображений</span><span class="sxs-lookup"><span data-stu-id="6e15a-318">Image Composition</span></span>

<span data-ttu-id="6e15a-319">Каждая операция Блит определяется следующими тремя прямоугольниками:</span><span class="sxs-lookup"><span data-stu-id="6e15a-319">Every blit operation is defined by the following three rectangles:</span></span>

-   <span data-ttu-id="6e15a-320">*Целевой* прямоугольник (**таржетрект**) определяет область в области назначения, в которой будут отображаться выходные данные.</span><span class="sxs-lookup"><span data-stu-id="6e15a-320">The *target* rectangle (**TargetRect**) defines the region within the destination surface where the output will appear.</span></span> <span data-ttu-id="6e15a-321">Выходное изображение обрезается по этому прямоугольнику.</span><span class="sxs-lookup"><span data-stu-id="6e15a-321">The output image is clipped to this rectangle.</span></span>
-   <span data-ttu-id="6e15a-322">Прямоугольник *назначения* для каждого потока (**DstRect**) определяет, где находится входной поток в составном изображении.</span><span class="sxs-lookup"><span data-stu-id="6e15a-322">The *destination* rectangle for each stream (**DstRect**) defines where the input stream appears in the composited image.</span></span>
-   <span data-ttu-id="6e15a-323">*Исходный* прямоугольник для каждого потока (**SrcRect**) определяет, какая часть исходного изображения отображается.</span><span class="sxs-lookup"><span data-stu-id="6e15a-323">The *source* rectangle for each stream (**SrcRect**) defines which part of the source image appears.</span></span>

<span data-ttu-id="6e15a-324">Целевой и конечный прямоугольники указываются относительно поверхности назначения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-324">The target and destination rectangles are specified relative to the destination surface.</span></span> <span data-ttu-id="6e15a-325">Исходный прямоугольник указывается относительно исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-325">The source rectangle is specified relative to the source image.</span></span> <span data-ttu-id="6e15a-326">Все прямоугольники указываются в пикселях.</span><span class="sxs-lookup"><span data-stu-id="6e15a-326">All rectangles are specified in pixels.</span></span>

![Схема, показывающая исходный, конечный и целевой прямоугольники](images/dxva-vp-rects.gif)

<span data-ttu-id="6e15a-328">Устройство обработки видео Alpha смешивает входные изображения, используя любой из следующих источников альфа-данных:</span><span class="sxs-lookup"><span data-stu-id="6e15a-328">The video processing device alpha blends the input pictures, using any of the following sources of alpha data:</span></span>

-   <span data-ttu-id="6e15a-329">Альфа-данные для каждого пикселя из подпотоков.</span><span class="sxs-lookup"><span data-stu-id="6e15a-329">Per-pixel alpha data from substreams.</span></span>
-   <span data-ttu-id="6e15a-330">Плоское альфа-значение для каждого видеопотока, указанное в элементе **планаралфа** структуры [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-330">A planar alpha value for each video stream, specified in the **PlanarAlpha** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span>
-   <span data-ttu-id="6e15a-331">Плоское альфа-значение составного изображения, заданное в **альфа** -элементе структуры [**DXVA2 \_ видеопроцессблтпарамс**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-331">The planar alpha value of the composited image, specified in the **Alpha** member of the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span> <span data-ttu-id="6e15a-332">Это значение используется для смешения всего составного изображения с цветом фона.</span><span class="sxs-lookup"><span data-stu-id="6e15a-332">This value is used to blend the entire composited image with the background color.</span></span>

<span data-ttu-id="6e15a-333">В этом разделе приводится ряд примеров, демонстрирующих, как устройство обработки видео создает выходное изображение.</span><span class="sxs-lookup"><span data-stu-id="6e15a-333">This section gives a series of examples that show how the video processing device creates the output image.</span></span>

### <a name="example-1-letterboxing"></a><span data-ttu-id="6e15a-334">Пример 1. пустых</span><span class="sxs-lookup"><span data-stu-id="6e15a-334">Example 1: Letterboxing</span></span>

<span data-ttu-id="6e15a-335">В этом примере показано, как леттербокс исходный образ, настроив прямоугольник назначения так, чтобы он был меньше целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6e15a-335">This example shows how to letterbox the source image, by setting the destination rectangle to be smaller than the target rectangle.</span></span> <span data-ttu-id="6e15a-336">Основным видеопотоком в этом примере является изображение 720 × 480, которое должно отображаться с пропорциями 16:9.</span><span class="sxs-lookup"><span data-stu-id="6e15a-336">The primary video stream in this example is a 720 × 480 image, and is meant to be displayed at a 16:9 aspect ratio.</span></span> <span data-ttu-id="6e15a-337">Конечная поверхность — 640 × 480 пикселей (пропорции 4:3).</span><span class="sxs-lookup"><span data-stu-id="6e15a-337">The destination surface is 640 × 480 pixels (4:3 aspect ratio).</span></span> <span data-ttu-id="6e15a-338">Для достижения правильного соотношения сторон конечный прямоугольник должен быть 640 × 360.</span><span class="sxs-lookup"><span data-stu-id="6e15a-338">To achieve the correct aspect ratio, the destination rectangle must be 640 × 360.</span></span> <span data-ttu-id="6e15a-339">Для простоты в этом примере не содержится подпоток.</span><span class="sxs-lookup"><span data-stu-id="6e15a-339">For simplicity, this example does not include a substream.</span></span> <span data-ttu-id="6e15a-340">На следующей диаграмме показаны исходные и конечные прямоугольники.</span><span class="sxs-lookup"><span data-stu-id="6e15a-340">The following diagram shows the source and destination rectangles.</span></span>

![Схема, показывающая пустых.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

<span data-ttu-id="6e15a-342">На предыдущей схеме показаны следующие прямоугольники:</span><span class="sxs-lookup"><span data-stu-id="6e15a-342">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="6e15a-343">Целевой прямоугольник: {0, 0, 640, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-343">Target rectangle: { 0, 0, 640, 480 }</span></span>
-   <span data-ttu-id="6e15a-344">Основное видео:</span><span class="sxs-lookup"><span data-stu-id="6e15a-344">Primary video:</span></span>

    -   <span data-ttu-id="6e15a-345">Исходный прямоугольник: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-345">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="6e15a-346">Конечный прямоугольник: {0, 60, 640, 420}</span><span class="sxs-lookup"><span data-stu-id="6e15a-346">Destination rectangle: { 0, 60, 640, 420 }</span></span>

<span data-ttu-id="6e15a-347">Драйвер будет разбить видео, сжать его до 640 × 360 и Блит кадр в прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-347">The driver will deinterlace the video, shrink the deinterlaced frame to 640 × 360, and blit the frame into the destination rectangle.</span></span> <span data-ttu-id="6e15a-348">Целевой прямоугольник больше, чем прямоугольник назначения, поэтому драйвер будет использовать цвет фона для заполнения горизонтальных полос выше и ниже рамки.</span><span class="sxs-lookup"><span data-stu-id="6e15a-348">The target rectangle is larger than the destination rectangle, so the driver will use the background color to fill the horizontal bars above and below the frame.</span></span> <span data-ttu-id="6e15a-349">Цвет фона задается в структуре [**DXVA2 \_ видеопроцессблтпарамс**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="6e15a-349">The background color is specified in the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="example-2-stretching-substream-images"></a><span data-ttu-id="6e15a-350">Пример 2. изображения подпотока растяжения</span><span class="sxs-lookup"><span data-stu-id="6e15a-350">Example 2: Stretching Substream Images</span></span>

<span data-ttu-id="6e15a-351">Изображения в подпотоке могут дополняться за пределами основного видеоизображения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-351">Substream pictures can extend beyond the primary video picture.</span></span> <span data-ttu-id="6e15a-352">Например, в видео DVD-коде основной видеопоток может иметь пропорции 4:3, в то время как подпоток равен 16:9.</span><span class="sxs-lookup"><span data-stu-id="6e15a-352">In DVD video, for example, the primary video stream can have a 4:3 aspect ratio while the substream is 16:9.</span></span> <span data-ttu-id="6e15a-353">В этом примере оба видеопотока имеют одинаковые исходные размеры (720 × 480), но этот подпоток должен отображаться с пропорциями 16:9.</span><span class="sxs-lookup"><span data-stu-id="6e15a-353">In this example, both video streams have the same source dimensions (720 × 480), but the substream is intended to be shown at a 16:9 aspect ratio.</span></span> <span data-ttu-id="6e15a-354">Для достижения этого пропорций изображение подпотока растягивается по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="6e15a-354">To achieve this aspect ratio, the substream image is stretched horizontally.</span></span> <span data-ttu-id="6e15a-355">Исходный и конечный прямоугольники показаны на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="6e15a-355">The source and destination rectangles are shown in the following diagram.</span></span>

![Диаграмма, демонстрирующая растяжение изображения подпотока.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

<span data-ttu-id="6e15a-357">На предыдущей схеме показаны следующие прямоугольники:</span><span class="sxs-lookup"><span data-stu-id="6e15a-357">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="6e15a-358">Целевой прямоугольник: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-358">Target rectangle: { 0, 0, 854, 480 }</span></span>
-   <span data-ttu-id="6e15a-359">Основное видео:</span><span class="sxs-lookup"><span data-stu-id="6e15a-359">Primary video:</span></span>

    -   <span data-ttu-id="6e15a-360">Исходный прямоугольник: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-360">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="6e15a-361">Конечный прямоугольник: {0, 107, 474, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-361">Destination rectangle: { 0, 107, 474, 480 }</span></span>

-   <span data-ttu-id="6e15a-362">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-362">Substream:</span></span>
    -   <span data-ttu-id="6e15a-363">Исходный прямоугольник: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-363">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="6e15a-364">Прямоугольник назначения: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-364">Destination rectangle: { 0, 0, 854, 480 }</span></span>

<span data-ttu-id="6e15a-365">Эти значения сохраняют высоту изображения и горизонтальное масштабирование обоих изображений.</span><span class="sxs-lookup"><span data-stu-id="6e15a-365">These values preserve the image height and scale both images horizontally.</span></span> <span data-ttu-id="6e15a-366">В регионах, где отображаются оба изображения, они являются альфа-смешением.</span><span class="sxs-lookup"><span data-stu-id="6e15a-366">In the regions where both images appear, they are alpha blended.</span></span> <span data-ttu-id="6e15a-367">Где изображение подпотока ексендс за пределами видео ограничения primay, этот подпоток смешивается с цветом фона.</span><span class="sxs-lookup"><span data-stu-id="6e15a-367">Where the substream picture exends beyond the primay video, the substream is alpha blended with the background color.</span></span> <span data-ttu-id="6e15a-368">Это альфа-смешение учетных записей для измененных цветов в правой части диаграммы.</span><span class="sxs-lookup"><span data-stu-id="6e15a-368">This alpha blending accounts for the altered colors in the right-hand side of the diagram.</span></span>

### <a name="example-3-mismatched-stream-heights"></a><span data-ttu-id="6e15a-369">Пример 3. несоответствие высоты потока</span><span class="sxs-lookup"><span data-stu-id="6e15a-369">Example 3: Mismatched Stream Heights</span></span>

<span data-ttu-id="6e15a-370">В предыдущем примере подпоток и первичный поток имеют одинаковую высоту.</span><span class="sxs-lookup"><span data-stu-id="6e15a-370">In the previous example, the substream and the primary stream are the same height.</span></span> <span data-ttu-id="6e15a-371">Потоки также могут иметь несовпадающие значения высоты, как показано в этом примере.</span><span class="sxs-lookup"><span data-stu-id="6e15a-371">Streams can also have mismatched heights, as shown in this example.</span></span> <span data-ttu-id="6e15a-372">Области в целевом прямоугольнике, где не отображается видео, отображаются с использованием цвета фона — черным в этом примере.</span><span class="sxs-lookup"><span data-stu-id="6e15a-372">Areas within the target rectangle where no video appears are drawn using the background color—black in this example.</span></span> <span data-ttu-id="6e15a-373">Исходный и конечный прямоугольники показаны на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="6e15a-373">The source and destination rectangles are shown in the following diagram.</span></span>

![на схеме показаны несоответствующие значения высоты потока](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

<span data-ttu-id="6e15a-375">На предыдущей схеме показаны следующие прямоугольники:</span><span class="sxs-lookup"><span data-stu-id="6e15a-375">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="6e15a-376">Целевой прямоугольник: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="6e15a-376">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="6e15a-377">Основное видео:</span><span class="sxs-lookup"><span data-stu-id="6e15a-377">Primary video:</span></span>
    -   <span data-ttu-id="6e15a-378">Исходный прямоугольник: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="6e15a-378">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="6e15a-379">Конечный прямоугольник: {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="6e15a-379">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="6e15a-380">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-380">Substream:</span></span>
    -   <span data-ttu-id="6e15a-381">Исходный прямоугольник: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="6e15a-381">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="6e15a-382">Прямоугольник назначения: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="6e15a-382">Destination rectangle: { 25, 0, 125, 85 }</span></span>

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a><span data-ttu-id="6e15a-383">Пример 4. целевой прямоугольник меньше поверхности назначения</span><span class="sxs-lookup"><span data-stu-id="6e15a-383">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>

<span data-ttu-id="6e15a-384">В этом примере показан случай, когда целевой прямоугольник меньше поверхности назначения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-384">This example shows a case where the target rectangle is smaller than the destination surface.</span></span>

![Схема, показывающая Блит в прямоугольник назначения.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

<span data-ttu-id="6e15a-386">На предыдущей схеме показаны следующие прямоугольники:</span><span class="sxs-lookup"><span data-stu-id="6e15a-386">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="6e15a-387">Конечная поверхность: {0, 0, 300, 200}</span><span class="sxs-lookup"><span data-stu-id="6e15a-387">Destination surface: { 0, 0, 300, 200 }</span></span>
-   <span data-ttu-id="6e15a-388">Целевой прямоугольник: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="6e15a-388">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="6e15a-389">Основное видео:</span><span class="sxs-lookup"><span data-stu-id="6e15a-389">Primary video:</span></span>
    -   <span data-ttu-id="6e15a-390">Исходный прямоугольник: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="6e15a-390">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="6e15a-391">Конечный прямоугольник: {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="6e15a-391">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="6e15a-392">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-392">Substream:</span></span>
    -   <span data-ttu-id="6e15a-393">Исходный прямоугольник: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="6e15a-393">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="6e15a-394">Прямоугольник назначения: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="6e15a-394">Destination rectangle: { 25, 0, 125, 85 }</span></span>

<span data-ttu-id="6e15a-395">Пиксели за пределами целевого прямоугольника не изменяются, поэтому цвет фона отображается только в пределах целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6e15a-395">Pixels outside of the target rectangle are not modified, so the background color appears only within the target rectangle.</span></span> <span data-ttu-id="6e15a-396">Пунктирная область указывает части поверхности назначения, которые не затрагиваются Блит.</span><span class="sxs-lookup"><span data-stu-id="6e15a-396">The dotted area indicates portions of the destination surface that are not affected by the blit.</span></span>

### <a name="example-5-source-rectangles"></a><span data-ttu-id="6e15a-397">Пример 5. исходные прямоугольники</span><span class="sxs-lookup"><span data-stu-id="6e15a-397">Example 5: Source Rectangles</span></span>

<span data-ttu-id="6e15a-398">Если указать исходный прямоугольник, который меньше исходного изображения, драйвер будет Блит только эту часть изображения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-398">If you specify a source rectangle that is smaller than the source picture, the driver will blit just that portion of the picture.</span></span> <span data-ttu-id="6e15a-399">В этом примере исходные прямоугольники задают нижнюю правую четвертую квадрант основного видеопотока и нижнюю левую четвертую квадрант подпотока (на схеме отображаются метки хэша).</span><span class="sxs-lookup"><span data-stu-id="6e15a-399">In this example, the source rectangles specify the lower-right quadrant of the primary video stream and the lower-left quadrant of the substream (indicated by hash marks in the diagram).</span></span> <span data-ttu-id="6e15a-400">Прямоугольники назначения имеют те же размеры, что и исходные прямоугольники, поэтому видео не растягивается.</span><span class="sxs-lookup"><span data-stu-id="6e15a-400">The destination rectangles are the same sizes as the source rectangles, so the video is not stretched.</span></span> <span data-ttu-id="6e15a-401">Исходный и конечный прямоугольники показаны на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="6e15a-401">The source and destination rectangles are shown in the following diagram.</span></span>

![Схема, показывающая Блит из двух исходных прямоугольников.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

<span data-ttu-id="6e15a-403">На предыдущей схеме показаны следующие прямоугольники:</span><span class="sxs-lookup"><span data-stu-id="6e15a-403">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="6e15a-404">Целевой прямоугольник: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="6e15a-404">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="6e15a-405">Основное видео:</span><span class="sxs-lookup"><span data-stu-id="6e15a-405">Primary video:</span></span>
    -   <span data-ttu-id="6e15a-406">Размер исходной поверхности: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-406">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="6e15a-407">Исходный прямоугольник: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-407">Source rectangle: { 360, 240, 720, 480 }</span></span>
    -   <span data-ttu-id="6e15a-408">Прямоугольник назначения: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="6e15a-408">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="6e15a-409">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-409">Substream:</span></span>
    -   <span data-ttu-id="6e15a-410">Размер исходной поверхности: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="6e15a-410">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="6e15a-411">Исходный прямоугольник: {0, 288, 320, 576}</span><span class="sxs-lookup"><span data-stu-id="6e15a-411">Source rectangle: { 0, 288, 320, 576 }</span></span>
    -   <span data-ttu-id="6e15a-412">Прямоугольник назначения: {400, 0, 720, 288}</span><span class="sxs-lookup"><span data-stu-id="6e15a-412">Destination rectangle: { 400, 0, 720, 288 }</span></span>

### <a name="example-6-intersecting-destination-rectangles"></a><span data-ttu-id="6e15a-413">Пример 6. пересечение прямоугольников назначения</span><span class="sxs-lookup"><span data-stu-id="6e15a-413">Example 6: Intersecting Destination Rectangles</span></span>

<span data-ttu-id="6e15a-414">Этот пример аналогичен предыдущему, но прямоугольники назначения пересекаются.</span><span class="sxs-lookup"><span data-stu-id="6e15a-414">This example is similar to previous one, but the destination rectangles intersect.</span></span> <span data-ttu-id="6e15a-415">Размеры поверхности те же, что и в предыдущем примере, но исходный и конечный прямоугольники — нет.</span><span class="sxs-lookup"><span data-stu-id="6e15a-415">The surface dimensions are the same as in the previous example, but the source and destination rectangles are not.</span></span> <span data-ttu-id="6e15a-416">Опять же, видео обрезается, но не растягивается.</span><span class="sxs-lookup"><span data-stu-id="6e15a-416">Again, the video is cropped but not stretched.</span></span> <span data-ttu-id="6e15a-417">Исходный и конечный прямоугольники показаны на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="6e15a-417">The source and destination rectangles are shown in the following diagram.</span></span>

![Диаграмма, показывающая пересекающиеся прямоугольники назначения.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

<span data-ttu-id="6e15a-419">На предыдущей схеме показаны следующие прямоугольники:</span><span class="sxs-lookup"><span data-stu-id="6e15a-419">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="6e15a-420">Целевой прямоугольник: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="6e15a-420">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="6e15a-421">Основное видео:</span><span class="sxs-lookup"><span data-stu-id="6e15a-421">Primary video:</span></span>
    -   <span data-ttu-id="6e15a-422">Размер исходной поверхности: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-422">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="6e15a-423">Исходный прямоугольник: {260, 92, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-423">Source rectangle: { 260, 92, 720, 480 }</span></span>
    -   <span data-ttu-id="6e15a-424">Прямоугольник назначения: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="6e15a-424">Destination rectangle: { 0, 0, 460, 388 }</span></span>
-   <span data-ttu-id="6e15a-425">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-425">Substream:</span></span>
    -   <span data-ttu-id="6e15a-426">Размер исходной поверхности: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="6e15a-426">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="6e15a-427">Исходный прямоугольник: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="6e15a-427">Source rectangle: { 0, 0, 460, 388 }</span></span>
    -   <span data-ttu-id="6e15a-428">Прямоугольник назначения: {260, 188, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="6e15a-428">Destination rectangle: { 260, 188, 720, 576 }</span></span>

### <a name="example-7-stretching-and-cropping-video"></a><span data-ttu-id="6e15a-429">Пример 7. растяжение и обрезка видео</span><span class="sxs-lookup"><span data-stu-id="6e15a-429">Example 7: Stretching and Cropping Video</span></span>

<span data-ttu-id="6e15a-430">В этом примере видео растягивается и обрезается.</span><span class="sxs-lookup"><span data-stu-id="6e15a-430">In this example, the video is stretched as well as cropped.</span></span> <span data-ttu-id="6e15a-431">Регион размером 180 × 120 из каждого потока растягивается для покрытия области 360 x 240 в прямоугольнике назначения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-431">A 180 × 120 region from each stream is stretched to cover a 360 × 240 area in the destination rectangle.</span></span>

![Диаграмма, демонстрирующая растяжение и обрезку.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

<span data-ttu-id="6e15a-433">На предыдущей схеме показаны следующие прямоугольники:</span><span class="sxs-lookup"><span data-stu-id="6e15a-433">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="6e15a-434">Целевой прямоугольник: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-434">Target rectangle: { 0, 0, 720, 480 }</span></span>
-   <span data-ttu-id="6e15a-435">Основное видео:</span><span class="sxs-lookup"><span data-stu-id="6e15a-435">Primary video:</span></span>
    -   <span data-ttu-id="6e15a-436">Размер исходной поверхности: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="6e15a-436">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="6e15a-437">Исходный прямоугольник: {180, 120, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="6e15a-437">Source rectangle: { 180, 120, 360, 240 }</span></span>
    -   <span data-ttu-id="6e15a-438">Прямоугольник назначения: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="6e15a-438">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="6e15a-439">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-439">Substream:</span></span>
    -   <span data-ttu-id="6e15a-440">Размер исходной поверхности: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="6e15a-440">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="6e15a-441">Исходный прямоугольник: {0, 0, 180, 120}</span><span class="sxs-lookup"><span data-stu-id="6e15a-441">Source rectangle: { 0, 0, 180, 120 }</span></span>
    -   <span data-ttu-id="6e15a-442">Прямоугольник назначения: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="6e15a-442">Destination rectangle: { 360, 240, 720, 480 }</span></span>

## <a name="input-sample-order"></a><span data-ttu-id="6e15a-443">Порядок входных образцов</span><span class="sxs-lookup"><span data-stu-id="6e15a-443">Input Sample Order</span></span>

<span data-ttu-id="6e15a-444">Параметр *псамплес* метода [**видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) является указателем на массив входных примеров.</span><span class="sxs-lookup"><span data-stu-id="6e15a-444">The *pSamples* parameter of the [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method is a pointer to an array of input samples.</span></span> <span data-ttu-id="6e15a-445">Сначала появятся примеры из основного видеопотока, а затем — изображения подпотока в Z-порядке.</span><span class="sxs-lookup"><span data-stu-id="6e15a-445">Samples from the primary video stream appear first, followed by substream pictures in Z-order.</span></span> <span data-ttu-id="6e15a-446">Образцы должны быть помещены в массив в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="6e15a-446">Samples must be placed into the array in the following order:</span></span>

-   <span data-ttu-id="6e15a-447">Примеры для основного видеопотока отображаются первыми в массиве в временном порядке.</span><span class="sxs-lookup"><span data-stu-id="6e15a-447">Samples for the primary video stream appear first in the array, in temporal order.</span></span> <span data-ttu-id="6e15a-448">В зависимости от режима чередования драйверу может потребоваться один или несколько эталонных образцов из основного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-448">Depending on the deinterlace mode, the driver may require one or more reference samples from the primary video stream.</span></span> <span data-ttu-id="6e15a-449">Члены **нумфорвардрефсамплес** и **Нумбакквардрефсамплес** в структуре [**DXVA2 \_ видеопроцессоркапс**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) определяют, сколько необходимо выборок на прямой и обратной ссылке.</span><span class="sxs-lookup"><span data-stu-id="6e15a-449">The **NumForwardRefSamples** and **NumBackwardRefSamples** members of the [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure specify how many forward and backward reference samples are needed.</span></span> <span data-ttu-id="6e15a-450">Вызывающий объект должен предоставить эти образцы, даже если содержимое видео является прогрессивным и не требует дечередования.</span><span class="sxs-lookup"><span data-stu-id="6e15a-450">The caller must provide these reference samples even if the video content is progressive and does not require deinterlacing.</span></span> <span data-ttu-id="6e15a-451">(Это может произойти, если к неограниченному устройству присвоено последовательное кадровое значение, например, если источник содержит сочетание кадров с чередованием и постепенной развертки.)</span><span class="sxs-lookup"><span data-stu-id="6e15a-451">(This can occur when progressive frames are given to a deinterlacing device, for example when the source contains a mix of both interlaced and progressive frames.)</span></span>
-   <span data-ttu-id="6e15a-452">После образцов для основного видеопотока массив может содержать до 15 примеров вложенных потоков, упорядоченных в Z-порядке, снизу вверх.</span><span class="sxs-lookup"><span data-stu-id="6e15a-452">After the samples for the primary video stream, the array can contain up to 15 substream samples, arranged in Z-order, from bottom to top.</span></span> <span data-ttu-id="6e15a-453">Подпотоки всегда прогрессивны и не нуждаются в справочных рисунках.</span><span class="sxs-lookup"><span data-stu-id="6e15a-453">Substreams are always progressive and do not require reference pictures.</span></span>

<span data-ttu-id="6e15a-454">В любое время основной видеопоток может переключаться между чередованием и последовательным содержимым, а также может меняться число подпотоков.</span><span class="sxs-lookup"><span data-stu-id="6e15a-454">At any time, the primary video stream can switch between interlaced and progressive content, and the number of substreams can change.</span></span>

<span data-ttu-id="6e15a-455">Элемент **самплеформат. самплеформат** в структуре [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) указывает тип изображения.</span><span class="sxs-lookup"><span data-stu-id="6e15a-455">The **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure indicates the type of picture.</span></span> <span data-ttu-id="6e15a-456">Для изображений подпотока задайте для этого параметра значение DXVA2 \_ самплесубстреам.</span><span class="sxs-lookup"><span data-stu-id="6e15a-456">For substream pictures, set this value to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="6e15a-457">Для последовательного изображения это значение равно DXVA2 \_ самплепрогрессивефраме.</span><span class="sxs-lookup"><span data-stu-id="6e15a-457">For progressive pictures, the value is DXVA2\_SampleProgressiveFrame.</span></span> <span data-ttu-id="6e15a-458">Для изображений с чередованием значение зависит от макета поля.</span><span class="sxs-lookup"><span data-stu-id="6e15a-458">For interlaced pictures, the value depends on the field layout.</span></span>

<span data-ttu-id="6e15a-459">Если драйвер требует использования образцов прямого и обратного ссылок, то в начале видеопоследовательности может быть недоступно полное количество выборок.</span><span class="sxs-lookup"><span data-stu-id="6e15a-459">If the driver requires forward and backward reference samples, the full number of samples might not be available at the start of the video sequence.</span></span> <span data-ttu-id="6e15a-460">В этом случае включите в массив *псамплес* записи, но пометьте недостающие примеры как имеющие тип DXVA2 \_ самплеункновн.</span><span class="sxs-lookup"><span data-stu-id="6e15a-460">In that case, include entries for them in the *pSamples* array, but mark the missing samples as having type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="6e15a-461">**Начальное** и **Конечное** элементы структуры [**DXVA2 \_ видеосампле**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) предоставляют временное расположение каждого примера.</span><span class="sxs-lookup"><span data-stu-id="6e15a-461">The **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the temporal location of each sample.</span></span> <span data-ttu-id="6e15a-462">Эти значения используются только для выборки из основного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6e15a-462">These values are used only for samples from the primary video stream.</span></span> <span data-ttu-id="6e15a-463">Для изображений подпотока задайте для обоих элементов нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6e15a-463">For substream pictures, set both members to zero.</span></span>

<span data-ttu-id="6e15a-464">Следующие примеры могут помочь прояснить эти требования.</span><span class="sxs-lookup"><span data-stu-id="6e15a-464">The following examples may help to clarify these requirements.</span></span>

### <a name="example-1"></a><span data-ttu-id="6e15a-465">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-465">Example 1</span></span>

<span data-ttu-id="6e15a-466">Простейший случай возникает, когда нет подпотоков, а алгоритму разчередования не требуются эталонные образцы (**нумфорвардрефсамплес** и **нумбакквардрефсамплес** равны нулю).</span><span class="sxs-lookup"><span data-stu-id="6e15a-466">The simplest case occurs when there are no substreams and the deinterlacing algorithm does not require reference samples (**NumForwardRefSamples** and **NumBackwardRefSamples** are both zero).</span></span> <span data-ttu-id="6e15a-467">Примером такого алгоритма является дечередование Боба.</span><span class="sxs-lookup"><span data-stu-id="6e15a-467">Bob deinterlacing is an example of such an algorithm.</span></span> <span data-ttu-id="6e15a-468">В этом случае массив *псамплес* должен содержать одну поверхность ввода, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6e15a-468">In this case, the *pSamples* array should contain a single input surface, as shown in the following table.</span></span>



| <span data-ttu-id="6e15a-469">Индекс</span><span class="sxs-lookup"><span data-stu-id="6e15a-469">Index</span></span>           | <span data-ttu-id="6e15a-470">Тип поверхности</span><span class="sxs-lookup"><span data-stu-id="6e15a-470">Surface type</span></span>        | <span data-ttu-id="6e15a-471">Временное расположение</span><span class="sxs-lookup"><span data-stu-id="6e15a-471">Temporal location</span></span> |
|-----------------|---------------------|-------------------|
| <span data-ttu-id="6e15a-472">*псамплес* \[ 0,0\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-472">*pSamples*\[0\]</span></span> | <span data-ttu-id="6e15a-473">Изображение с чередованием.</span><span class="sxs-lookup"><span data-stu-id="6e15a-473">Interlaced picture.</span></span> | <span data-ttu-id="6e15a-474">*T*</span><span class="sxs-lookup"><span data-stu-id="6e15a-474">*T*</span></span>               |



 

<span data-ttu-id="6e15a-475">Значение времени *T* считается временем начала текущего кадра видео.</span><span class="sxs-lookup"><span data-stu-id="6e15a-475">The time value *T* is assumed to be the start time of the current video frame.</span></span>

### <a name="example-2"></a><span data-ttu-id="6e15a-476">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6e15a-476">Example 2</span></span>

<span data-ttu-id="6e15a-477">В этом примере приложение смешивает два подпотока с основным потоком.</span><span class="sxs-lookup"><span data-stu-id="6e15a-477">In this example, the application mixes two substreams with the primary stream.</span></span> <span data-ttu-id="6e15a-478">Для алгоритма дечередования не требуются эталонные образцы.</span><span class="sxs-lookup"><span data-stu-id="6e15a-478">The deinterlacing algorithm does not require reference samples.</span></span> <span data-ttu-id="6e15a-479">В следующей таблице показано, как эти образцы упорядочены в массиве *псамплес* .</span><span class="sxs-lookup"><span data-stu-id="6e15a-479">The following table shows how these samples are arranged in the *pSamples* array.</span></span>



| <span data-ttu-id="6e15a-480">Индекс</span><span class="sxs-lookup"><span data-stu-id="6e15a-480">Index</span></span>           | <span data-ttu-id="6e15a-481">Тип поверхности</span><span class="sxs-lookup"><span data-stu-id="6e15a-481">Surface type</span></span>       | <span data-ttu-id="6e15a-482">Временное расположение</span><span class="sxs-lookup"><span data-stu-id="6e15a-482">Temporal location</span></span> | <span data-ttu-id="6e15a-483">Z-порядок</span><span class="sxs-lookup"><span data-stu-id="6e15a-483">Z-order</span></span> |
|-----------------|--------------------|-------------------|---------|
| <span data-ttu-id="6e15a-484">*псамплес* \[ 0,0\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-484">*pSamples*\[0\]</span></span> | <span data-ttu-id="6e15a-485">Изображение с чередованием</span><span class="sxs-lookup"><span data-stu-id="6e15a-485">Interlaced picture</span></span> | <span data-ttu-id="6e15a-486">*T*</span><span class="sxs-lookup"><span data-stu-id="6e15a-486">*T*</span></span>               | <span data-ttu-id="6e15a-487">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-487">0</span></span>       |
| <span data-ttu-id="6e15a-488">*псамплес* \[ одного\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-488">*pSamples*\[1\]</span></span> | <span data-ttu-id="6e15a-489">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-489">Substream</span></span>          | <span data-ttu-id="6e15a-490">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-490">0</span></span>                 | <span data-ttu-id="6e15a-491">1</span><span class="sxs-lookup"><span data-stu-id="6e15a-491">1</span></span>       |
| <span data-ttu-id="6e15a-492">*псамплес* \[ открыт\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-492">*pSamples*\[2\]</span></span> | <span data-ttu-id="6e15a-493">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-493">Substream</span></span>          | <span data-ttu-id="6e15a-494">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-494">0</span></span>                 | <span data-ttu-id="6e15a-495">2</span><span class="sxs-lookup"><span data-stu-id="6e15a-495">2</span></span>       |



 

### <a name="example-3"></a><span data-ttu-id="6e15a-496">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6e15a-496">Example 3</span></span>

<span data-ttu-id="6e15a-497">Теперь предположим, что для алгоритма дечередования требуется один пример обратной ссылки и один пример прямой ссылки.</span><span class="sxs-lookup"><span data-stu-id="6e15a-497">Now suppose that the deinterlacing algorithm requires one backward reference sample and one forward reference sample.</span></span> <span data-ttu-id="6e15a-498">Кроме того, предоставляется два подпотока изображений для всего пяти поверхностей.</span><span class="sxs-lookup"><span data-stu-id="6e15a-498">In addition, two substream pictures are provided, for a total of five surfaces.</span></span> <span data-ttu-id="6e15a-499">В следующей таблице показано правильное упорядочение.</span><span class="sxs-lookup"><span data-stu-id="6e15a-499">The correct ordering is shown in the following table.</span></span>



| <span data-ttu-id="6e15a-500">Индекс</span><span class="sxs-lookup"><span data-stu-id="6e15a-500">Index</span></span>           | <span data-ttu-id="6e15a-501">Тип поверхности</span><span class="sxs-lookup"><span data-stu-id="6e15a-501">Surface type</span></span>                   | <span data-ttu-id="6e15a-502">Временное расположение</span><span class="sxs-lookup"><span data-stu-id="6e15a-502">Temporal location</span></span> | <span data-ttu-id="6e15a-503">Z-порядок</span><span class="sxs-lookup"><span data-stu-id="6e15a-503">Z-order</span></span>        |
|-----------------|--------------------------------|-------------------|----------------|
| <span data-ttu-id="6e15a-504">*псамплес* \[ 0,0\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-504">*pSamples*\[0\]</span></span> | <span data-ttu-id="6e15a-505">Изображение с чередованием (ссылка)</span><span class="sxs-lookup"><span data-stu-id="6e15a-505">Interlaced picture (reference)</span></span> | <span data-ttu-id="6e15a-506">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-506">*T* −1</span></span>            | <span data-ttu-id="6e15a-507">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="6e15a-507">Not applicable</span></span> |
| <span data-ttu-id="6e15a-508">*псамплес* \[ одного\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-508">*pSamples*\[1\]</span></span> | <span data-ttu-id="6e15a-509">Изображение с чередованием</span><span class="sxs-lookup"><span data-stu-id="6e15a-509">Interlaced picture</span></span>             | <span data-ttu-id="6e15a-510">*T*</span><span class="sxs-lookup"><span data-stu-id="6e15a-510">*T*</span></span>               | <span data-ttu-id="6e15a-511">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-511">0</span></span>              |
| <span data-ttu-id="6e15a-512">*псамплес* \[ открыт\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-512">*pSamples*\[2\]</span></span> | <span data-ttu-id="6e15a-513">Изображение с чередованием (ссылка)</span><span class="sxs-lookup"><span data-stu-id="6e15a-513">Interlaced picture (reference)</span></span> | <span data-ttu-id="6e15a-514">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-514">*T* +1</span></span>            | <span data-ttu-id="6e15a-515">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="6e15a-515">Not applicable</span></span> |
| <span data-ttu-id="6e15a-516">*псамплес* \[ 3-5\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-516">*pSamples*\[3\]</span></span> | <span data-ttu-id="6e15a-517">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-517">Substream</span></span>                      | <span data-ttu-id="6e15a-518">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-518">0</span></span>                 | <span data-ttu-id="6e15a-519">1</span><span class="sxs-lookup"><span data-stu-id="6e15a-519">1</span></span>              |
| <span data-ttu-id="6e15a-520">*псамплес* \[ четырех\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-520">*pSamples*\[4\]</span></span> | <span data-ttu-id="6e15a-521">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-521">Substream</span></span>                      | <span data-ttu-id="6e15a-522">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-522">0</span></span>                 | <span data-ttu-id="6e15a-523">2</span><span class="sxs-lookup"><span data-stu-id="6e15a-523">2</span></span>              |



 

<span data-ttu-id="6e15a-524">Время *T* − 1 — это время начала кадра, предшествующее текущему кадру, а *t* + 1 — время начала следующего кадра.</span><span class="sxs-lookup"><span data-stu-id="6e15a-524">The time *T* −1 is the start time of the frame before the current frame, and *T* +1 is the start time of the following frame.</span></span>

<span data-ttu-id="6e15a-525">Если поток видео переключается на прогрессивное содержимое, используя тот же режим чередования, приложение должно предоставить такое же количество выборок, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6e15a-525">If the video stream switches to progressive content, using the same deinterlacing mode, the application must provide the same number of samples, as shown in the following table.</span></span>



| <span data-ttu-id="6e15a-526">Индекс</span><span class="sxs-lookup"><span data-stu-id="6e15a-526">Index</span></span>           | <span data-ttu-id="6e15a-527">Тип поверхности</span><span class="sxs-lookup"><span data-stu-id="6e15a-527">Surface type</span></span>                    | <span data-ttu-id="6e15a-528">Временное расположение</span><span class="sxs-lookup"><span data-stu-id="6e15a-528">Temporal location</span></span> | <span data-ttu-id="6e15a-529">Z-порядок</span><span class="sxs-lookup"><span data-stu-id="6e15a-529">Z-order</span></span>        |
|-----------------|---------------------------------|-------------------|----------------|
| <span data-ttu-id="6e15a-530">*псамплес* \[ 0,0\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-530">*pSamples*\[0\]</span></span> | <span data-ttu-id="6e15a-531">Прогрессивное изображение (ссылка)</span><span class="sxs-lookup"><span data-stu-id="6e15a-531">Progressive picture (reference)</span></span> | <span data-ttu-id="6e15a-532">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-532">*T* −1</span></span>            | <span data-ttu-id="6e15a-533">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="6e15a-533">Not applicable</span></span> |
| <span data-ttu-id="6e15a-534">*псамплес* \[ одного\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-534">*pSamples*\[1\]</span></span> | <span data-ttu-id="6e15a-535">Последовательное изображение</span><span class="sxs-lookup"><span data-stu-id="6e15a-535">Progressive picture</span></span>             | <span data-ttu-id="6e15a-536">*T*</span><span class="sxs-lookup"><span data-stu-id="6e15a-536">*T*</span></span>               | <span data-ttu-id="6e15a-537">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-537">0</span></span>              |
| <span data-ttu-id="6e15a-538">*псамплес* \[ открыт\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-538">*pSamples*\[2\]</span></span> | <span data-ttu-id="6e15a-539">Прогрессивное изображение (ссылка)</span><span class="sxs-lookup"><span data-stu-id="6e15a-539">Progressive picture (reference)</span></span> | <span data-ttu-id="6e15a-540">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-540">*T* +1</span></span>            | <span data-ttu-id="6e15a-541">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="6e15a-541">Not applicable</span></span> |
| <span data-ttu-id="6e15a-542">*псамплес* \[ 3-5\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-542">*pSamples*\[3\]</span></span> | <span data-ttu-id="6e15a-543">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-543">Substream</span></span>                       | <span data-ttu-id="6e15a-544">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-544">0</span></span>                 | <span data-ttu-id="6e15a-545">1</span><span class="sxs-lookup"><span data-stu-id="6e15a-545">1</span></span>              |
| <span data-ttu-id="6e15a-546">*псамплес* \[ четырех\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-546">*pSamples*\[4\]</span></span> | <span data-ttu-id="6e15a-547">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6e15a-547">Substream</span></span>                       | <span data-ttu-id="6e15a-548">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-548">0</span></span>                 | <span data-ttu-id="6e15a-549">2</span><span class="sxs-lookup"><span data-stu-id="6e15a-549">2</span></span>              |



 

### <a name="example-4"></a><span data-ttu-id="6e15a-550">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6e15a-550">Example 4</span></span>

<span data-ttu-id="6e15a-551">В начале последовательности видео образцы ссылок могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="6e15a-551">At the start of a video sequence, forward and backward reference samples might not be available.</span></span> <span data-ttu-id="6e15a-552">В этом случае записи для отсутствующих примеров включаются в массив *псамплес* с типом Sample DXVA2 \_ самплеункновн.</span><span class="sxs-lookup"><span data-stu-id="6e15a-552">When this happens, entries for the missing samples are included in the *pSamples* array, with sample type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="6e15a-553">При условии, что для режима разследовательной развертки требуется один и тот же пример обратной ссылки, первые три вызова [**видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) будут иметь последовательности входных данных, показанные в следующих трех таблицах.</span><span class="sxs-lookup"><span data-stu-id="6e15a-553">Assuming that the deinterlacing mode needs one forward and one backward reference sample, the first three calls to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) would have the sequences of inputs shown in the following three tables.</span></span>



| <span data-ttu-id="6e15a-554">Индекс</span><span class="sxs-lookup"><span data-stu-id="6e15a-554">Index</span></span>           | <span data-ttu-id="6e15a-555">Тип поверхности</span><span class="sxs-lookup"><span data-stu-id="6e15a-555">Surface type</span></span>                   | <span data-ttu-id="6e15a-556">Временное расположение</span><span class="sxs-lookup"><span data-stu-id="6e15a-556">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="6e15a-557">*псамплес* \[ 0,0\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-557">*pSamples*\[0\]</span></span> | <span data-ttu-id="6e15a-558">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="6e15a-558">Unknown</span></span>                        | <span data-ttu-id="6e15a-559">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-559">0</span></span>                 |
| <span data-ttu-id="6e15a-560">*псамплес* \[ одного\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-560">*pSamples*\[1\]</span></span> | <span data-ttu-id="6e15a-561">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="6e15a-561">Unknown</span></span>                        | <span data-ttu-id="6e15a-562">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-562">0</span></span>                 |
| <span data-ttu-id="6e15a-563">*псамплес* \[ открыт\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-563">*pSamples*\[2\]</span></span> | <span data-ttu-id="6e15a-564">Изображение с чередованием (ссылка)</span><span class="sxs-lookup"><span data-stu-id="6e15a-564">Interlaced picture (reference)</span></span> | <span data-ttu-id="6e15a-565">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-565">*T* +1</span></span>            |



 



| <span data-ttu-id="6e15a-566">Индекс</span><span class="sxs-lookup"><span data-stu-id="6e15a-566">Index</span></span>           | <span data-ttu-id="6e15a-567">Тип поверхности</span><span class="sxs-lookup"><span data-stu-id="6e15a-567">Surface type</span></span>                   | <span data-ttu-id="6e15a-568">Временное расположение</span><span class="sxs-lookup"><span data-stu-id="6e15a-568">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="6e15a-569">*псамплес* \[ 0,0\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-569">*pSamples*\[0\]</span></span> | <span data-ttu-id="6e15a-570">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="6e15a-570">Unknown</span></span>                        | <span data-ttu-id="6e15a-571">0</span><span class="sxs-lookup"><span data-stu-id="6e15a-571">0</span></span>                 |
| <span data-ttu-id="6e15a-572">*псамплес* \[ одного\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-572">*pSamples*\[1\]</span></span> | <span data-ttu-id="6e15a-573">Изображение с чередованием</span><span class="sxs-lookup"><span data-stu-id="6e15a-573">Interlaced picture</span></span>             | <span data-ttu-id="6e15a-574">*T*</span><span class="sxs-lookup"><span data-stu-id="6e15a-574">*T*</span></span>               |
| <span data-ttu-id="6e15a-575">*псамплес* \[ открыт\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-575">*pSamples*\[2\]</span></span> | <span data-ttu-id="6e15a-576">Изображение с чередованием (ссылка)</span><span class="sxs-lookup"><span data-stu-id="6e15a-576">Interlaced picture (reference)</span></span> | <span data-ttu-id="6e15a-577">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-577">*T* +1</span></span>            |



 



| <span data-ttu-id="6e15a-578">Индекс</span><span class="sxs-lookup"><span data-stu-id="6e15a-578">Index</span></span>           | <span data-ttu-id="6e15a-579">Тип поверхности</span><span class="sxs-lookup"><span data-stu-id="6e15a-579">Surface type</span></span>                   | <span data-ttu-id="6e15a-580">Временное расположение</span><span class="sxs-lookup"><span data-stu-id="6e15a-580">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="6e15a-581">*псамплес* \[ 0,0\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-581">*pSamples*\[0\]</span></span> | <span data-ttu-id="6e15a-582">Изображение с чередованием</span><span class="sxs-lookup"><span data-stu-id="6e15a-582">Interlaced picture</span></span>             | <span data-ttu-id="6e15a-583">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-583">*T* −1</span></span>            |
| <span data-ttu-id="6e15a-584">*псамплес* \[ одного\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-584">*pSamples*\[1\]</span></span> | <span data-ttu-id="6e15a-585">Изображение с чередованием</span><span class="sxs-lookup"><span data-stu-id="6e15a-585">Interlaced picture</span></span>             | <span data-ttu-id="6e15a-586">*T*</span><span class="sxs-lookup"><span data-stu-id="6e15a-586">*T*</span></span>               |
| <span data-ttu-id="6e15a-587">*псамплес* \[ открыт\]</span><span class="sxs-lookup"><span data-stu-id="6e15a-587">*pSamples*\[2\]</span></span> | <span data-ttu-id="6e15a-588">Изображение с чередованием (ссылка)</span><span class="sxs-lookup"><span data-stu-id="6e15a-588">Interlaced picture (reference)</span></span> | <span data-ttu-id="6e15a-589">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="6e15a-589">*T* +1</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="6e15a-590">См. также</span><span class="sxs-lookup"><span data-stu-id="6e15a-590">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e15a-591">Ускорение видео DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="6e15a-591">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="6e15a-592">\_Пример ВИДЕОПРОК DXVA2</span><span class="sxs-lookup"><span data-stu-id="6e15a-592">DXVA2\_VideoProc Sample</span></span>](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
