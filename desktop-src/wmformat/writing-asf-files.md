---
title: Запись файлов ASF
description: Запись файлов ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media Format SDK, написание файлов ASF
- Windows Media Format SDK, создание файлов ASF
- Windows Media Format SDK, расширенный формат систем (ASF)
- Расширенный системный формат (ASF), запись файлов
- ASF (Расширенный системный формат), запись файлов
- Расширенный системный формат (ASF), создание файлов
- ASF (Расширенный системный формат), создание файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890240"
---
# <a name="writing-asf-files"></a><span data-ttu-id="2fb1b-110">Запись файлов ASF</span><span class="sxs-lookup"><span data-stu-id="2fb1b-110">Writing ASF Files</span></span>

<span data-ttu-id="2fb1b-111">Для создания файлов ASF из цифровых мультимедийных данных можно использовать объект модуля записи пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-111">You can use the writer object of the Windows Media Format SDK to create ASF files from digital media data.</span></span> <span data-ttu-id="2fb1b-112">Чтобы создать экземпляр объекта модуля записи, вызовите функцию [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="2fb1b-112">To create an instance of the writer object, call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="2fb1b-113">Объект модуля записи координирует функциональность ряда компонентов, включая кодеки, которые являются внешними по отношению к пакету SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-113">The writer object coordinates the functionality of a number of components, including codecs, which are external to the Windows Media Format SDK.</span></span>

<span data-ttu-id="2fb1b-114">Основные функциональные возможности объекта модуля записи можно разделить на следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-114">The basic functionality of the writer object can be broken down into the following steps.</span></span> <span data-ttu-id="2fb1b-115">На этом этапе "приложение" относится к программе, которую вы пишете с помощью пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-115">In these steps, "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="2fb1b-116">Приложение предоставляет модулю записи профиль для использования при создании файла ASF.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-116">The application supplies the writer with a profile to use in creating the ASF file.</span></span> <span data-ttu-id="2fb1b-117">Когда модуль записи загружает данные профиля, он назначает номер входного номера каждому соединению профиля.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-117">When the writer loads the profile data, it assigns an input number to each connection of the profile.</span></span>
2.  <span data-ttu-id="2fb1b-118">Приложение предоставляет модулю записи имя выходного файла для записи.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-118">The application supplies the writer with an output file name for the file to be written.</span></span> <span data-ttu-id="2fb1b-119">Модуль записи создает объект приемника файла модуля записи для управления созданием и входом файла.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-119">The writer creates a writer file sink object to manage the file creation and input.</span></span> <span data-ttu-id="2fb1b-120">Дополнительные сведения см. в разделе [объект приемника файла модуля записи](writer-file-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="2fb1b-120">For more information, see [Writer File Sink Object](writer-file-sink-object.md).</span></span>
3.  <span data-ttu-id="2fb1b-121">Модуль записи создает заголовок для нового файла на основе информации в профиле.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-121">The writer creates a header for the new file based on information in the profile.</span></span>
4.  <span data-ttu-id="2fb1b-122">Приложение передает несжатые образцы в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-122">The application passes uncompressed samples to the writer.</span></span> <span data-ttu-id="2fb1b-123">Образцы передаются по одному за раз в буферах, упакованных в объекты буфера.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-123">Samples are passed one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="2fb1b-124">Приложение должно передавать образцы для каждого потока параллельно, чтобы модуль записи получал все примеры в порядке времени презентации.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-124">The application should pass samples for each stream concurrently so that the writer receives all samples in presentation-time order.</span></span>
5.  <span data-ttu-id="2fb1b-125">Модуль записи передает образцы в соответствующий кодек для сжатия.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-125">The writer passes the samples to the appropriate codec for compression.</span></span> <span data-ttu-id="2fb1b-126">Когда модуль записи получает сжатые образцы, он покидает их с помощью примеров из других потоков, чтобы образцы перейдут в файл в порядке времени презентации независимо от потока.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-126">When the writer receives the compressed samples, it interleaves them with samples from the other streams so that samples go into the file in presentation time order irrespective of stream.</span></span> <span data-ttu-id="2fb1b-127">Затем образцы данных вносятся в пакеты и записываются в раздел данных файла.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-127">The sample data is then made into packets and written to the data section of the file.</span></span>
6.  <span data-ttu-id="2fb1b-128">Когда обрабатываются все образцы, модуль записи может добавить в файл индекс, чтобы улучшить поиск производительности.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-128">When all samples are processed, the writer can add an index to the file to enhance seeking performance.</span></span>

<span data-ttu-id="2fb1b-129">Эти действия проиллюстрированы в примере приложения Вмстатс, а не в других.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-129">These steps are illustrated in the WMStats sample application, among others.</span></span> <span data-ttu-id="2fb1b-130">Дополнительные сведения см. в разделе [примеры приложений](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="2fb1b-130">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="2fb1b-131">Модуль записи также поддерживает более широкие возможности, что позволяет выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-131">The writer also supports more advanced functionality, enabling you to do the following:</span></span>

-   <span data-ttu-id="2fb1b-132">Изменение метаданных в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-132">Edit metadata in the header of the file.</span></span>
-   <span data-ttu-id="2fb1b-133">Запись предварительно сжатых образцов.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-133">Write precompressed samples.</span></span>
-   <span data-ttu-id="2fb1b-134">Запись в сетевые приемники для потоковой передачи динамических данных.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-134">Write to network sinks for streaming live data.</span></span>
-   <span data-ttu-id="2fb1b-135">Запись в приемники файлов для дополнительных параметров управления файлами.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-135">Write to file sinks for advanced file control options.</span></span>
-   <span data-ttu-id="2fb1b-136">Запись в приемники push-уведомлений для распространения на серверы, которые будут доставлять содержимое конечным пользователям.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-136">Write to push sinks for distribution to servers that will deliver content to end users.</span></span>
-   <span data-ttu-id="2fb1b-137">Доставьте образцы для просмотра на просмотр для проверки выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-137">Deliver postview samples for verification of output.</span></span>
-   <span data-ttu-id="2fb1b-138">Модуль записи доставки — статистика производительности.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-138">Deliver writer-performance statistics.</span></span>

<span data-ttu-id="2fb1b-139">В следующих разделах подробно описывается использование объекта модуля записи.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-139">The following sections describe the use of the writer object in detail.</span></span>



| <span data-ttu-id="2fb1b-140">Section</span><span class="sxs-lookup"><span data-stu-id="2fb1b-140">Section</span></span>                                                                    | <span data-ttu-id="2fb1b-141">Описание</span><span class="sxs-lookup"><span data-stu-id="2fb1b-141">Description</span></span>                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fb1b-142">Использование профилей с модулем записи</span><span class="sxs-lookup"><span data-stu-id="2fb1b-142">To Use Profiles with the Writer</span></span>](to-use-profiles-with-the-writer.md)     | <span data-ttu-id="2fb1b-143">Описывает, как указать профиль для использования с модулем записи.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-143">Describes how to specify a profile to use with the writer.</span></span>                                             |
| [<span data-ttu-id="2fb1b-144">Работа с входными данными</span><span class="sxs-lookup"><span data-stu-id="2fb1b-144">Working with Inputs</span></span>](working-with-inputs.md)                             | <span data-ttu-id="2fb1b-145">Описывает, как определить и настроить входные параметры в модуле записи.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-145">Describes how to identify and configure the input settings in the writer.</span></span>                              |
| [<span data-ttu-id="2fb1b-146">Изменение метаданных с помощью модуля записи</span><span class="sxs-lookup"><span data-stu-id="2fb1b-146">To Edit Metadata with the Writer</span></span>](to-edit-metadata-with-the-writer.md)   | <span data-ttu-id="2fb1b-147">Описывает использование модуля записи для изменения метаданных нового файла.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-147">Describes how to use the writer to edit metadata for a new file.</span></span>                                       |
| [<span data-ttu-id="2fb1b-148">Написание образцов</span><span class="sxs-lookup"><span data-stu-id="2fb1b-148">To Write Samples</span></span>](to-write-samples.md)                                   | <span data-ttu-id="2fb1b-149">Описывает, как передавать образцы в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-149">Describes how to pass samples to the writer.</span></span>                                                           |
| [<span data-ttu-id="2fb1b-150">Настройка модулей обработки данных</span><span class="sxs-lookup"><span data-stu-id="2fb1b-150">Setting Data Unit Extensions</span></span>](setting-data-unit-extensions.md)           | <span data-ttu-id="2fb1b-151">Описывает добавление расширенных данных в образцы.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-151">Describes how to add extended data to samples.</span></span>                                                         |
| [<span data-ttu-id="2fb1b-152">Написание сжатых образцов</span><span class="sxs-lookup"><span data-stu-id="2fb1b-152">Writing Compressed Samples</span></span>](writing-compressed-samples.md)               | <span data-ttu-id="2fb1b-153">Описывает, как передавать предварительно сжатые образцы в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-153">Describes how to pass pre-compressed samples to the writer.</span></span>                                            |
| [<span data-ttu-id="2fb1b-154">Запись потоков изображений</span><span class="sxs-lookup"><span data-stu-id="2fb1b-154">Writing Image Streams</span></span>](writing-image-streams.md)                         | <span data-ttu-id="2fb1b-155">Описывает настройку входных данных для потока изображений.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-155">Describes how to configure an input for an image stream.</span></span>                                               |
| [<span data-ttu-id="2fb1b-156">Написание примеров видеороликов</span><span class="sxs-lookup"><span data-stu-id="2fb1b-156">Writing Video Image Samples</span></span>](writing-video-image-samples.md)             | <span data-ttu-id="2fb1b-157">Описывает, как настроить образцы видеороликов.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-157">Describes how to configure Video Image samples.</span></span>                                                        |
| [<span data-ttu-id="2fb1b-158">Запись потоков переменной скорости</span><span class="sxs-lookup"><span data-stu-id="2fb1b-158">Writing Variable Bit Rate Streams</span></span>](writing-variable-bit-rate-streams.md) | <span data-ttu-id="2fb1b-159">Описание процесса записи потоков с переменным битом скорости (VBR).</span><span class="sxs-lookup"><span data-stu-id="2fb1b-159">Describes how to write variable bit rate (VBR) streams.</span></span>                                                |
| [<span data-ttu-id="2fb1b-160">Использование кодировки Two-Pass</span><span class="sxs-lookup"><span data-stu-id="2fb1b-160">Using Two-Pass Encoding</span></span>](using-two-pass-encoding.md)                     | <span data-ttu-id="2fb1b-161">Описывает, как кодек выполняет предварительный этап перед записью файла.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-161">Describes how to have the codec perform a preliminary pass before writing the file.</span></span>                    |
| [<span data-ttu-id="2fb1b-162">Принудительная Вставка Key-Frame</span><span class="sxs-lookup"><span data-stu-id="2fb1b-162">To Force Key-Frame Insertion</span></span>](to-force-key-frame-insertion.md)           | <span data-ttu-id="2fb1b-163">Описывает, как вручную заставить кодек кодировать образец как ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-163">Describes how to manually force the codec to encode a sample as a key frame.</span></span>                           |
| [<span data-ttu-id="2fb1b-164">Управление задержкой записи</span><span class="sxs-lookup"><span data-stu-id="2fb1b-164">To Manage Writer Latency</span></span>](to-manage-writer-latency.md)                   | <span data-ttu-id="2fb1b-165">Описывает, как максимально сокращать время, затрачиваемое средством записи на обработку образцов в выходной файл или приемник.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-165">Describes how to minimize the time it takes the writer to process samples into an output file or sink.</span></span> |
| [<span data-ttu-id="2fb1b-166">Работа с приемниками модуля записи</span><span class="sxs-lookup"><span data-stu-id="2fb1b-166">Working with Writer Sinks</span></span>](working-with-writer-sinks.md)                 | <span data-ttu-id="2fb1b-167">Описывает, как использовать приемники модуля записи для доставки содержимого в файлы или сетевые расположения.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-167">Describes how to use writer sinks to deliver your content to files or network locations.</span></span>               |
| [<span data-ttu-id="2fb1b-168">Получение статистики модуля записи</span><span class="sxs-lookup"><span data-stu-id="2fb1b-168">To Get Writer Statistics</span></span>](to-get-writer-statistics.md)                   | <span data-ttu-id="2fb1b-169">Описывает, как получить статистику для модуля записи.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-169">Describes how to get statistics for the writer.</span></span>                                                        |
| [<span data-ttu-id="2fb1b-170">Использование записи для просмотра</span><span class="sxs-lookup"><span data-stu-id="2fb1b-170">To Use Writer Postview</span></span>](to-use-writer-postview.md)                       | <span data-ttu-id="2fb1b-171">Описывает, как получить несжатые образцы при написании файла для проверки.</span><span class="sxs-lookup"><span data-stu-id="2fb1b-171">Describes how to get uncompressed samples as you write a file for verification.</span></span>                        |



 

## <a name="related-topics"></a><span data-ttu-id="2fb1b-172">См. также</span><span class="sxs-lookup"><span data-stu-id="2fb1b-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fb1b-173">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="2fb1b-173">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="2fb1b-174">**Объект приемника файлов модуля записи**</span><span class="sxs-lookup"><span data-stu-id="2fb1b-174">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="2fb1b-175">**Объект приемника сети модуля записи**</span><span class="sxs-lookup"><span data-stu-id="2fb1b-175">**Writer Network Sink Object**</span></span>](writer-network-sink-object.md)
</dt> <dt>

[<span data-ttu-id="2fb1b-176">**Объект модуля записи**</span><span class="sxs-lookup"><span data-stu-id="2fb1b-176">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




