---
title: Чтение файлов с помощью асинхронного модуля чтения
description: Чтение файлов с помощью асинхронного модуля чтения
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Media Format SDK, чтение файлов
- Пакет SDK для Windows Media Format, асинхронный читатель
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- Расширенный формат систем (ASF), чтение файлов
- ASF (Расширенный системный формат), чтение файлов
- асинхронные модули чтения, интерфейс Ивмреадеркаллбакк
- Ивмреадеркаллбакк, асинхронные модули чтения
- асинхронные читатели, чтение файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412492"
---
# <a name="reading-files-with-the-asynchronous-reader"></a><span data-ttu-id="750ff-112">Чтение файлов с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="750ff-112">Reading Files with the Asynchronous Reader</span></span>

<span data-ttu-id="750ff-113">Асинхронный читатель считывает содержимое из файлов ASF, используя несколько потоков и асинхронные вызовы.</span><span class="sxs-lookup"><span data-stu-id="750ff-113">The asynchronous reader reads the content from ASF files using multiple threads and asynchronous calls.</span></span> <span data-ttu-id="750ff-114">Функции, поддерживаемые асинхронным модулем чтения, делают его хорошо подходящим для приложений, которые отображают содержимое для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="750ff-114">The features supported by the asynchronous reader make it well suited for applications that render content to end users.</span></span>

<span data-ttu-id="750ff-115">Основные функции объекта Reader можно разделить на следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="750ff-115">The most basic functionality of the reader object can be broken down into the following steps.</span></span> <span data-ttu-id="750ff-116">На этих этапах "приложение" относится к программе, которую вы пишете с помощью пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="750ff-116">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="750ff-117">Приложение реализует интерфейс [**ивмреадеркаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) для обработки сообщений от модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="750ff-117">The application implements the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) interface to handle messages from the reader.</span></span> <span data-ttu-id="750ff-118">К ним относятся два метода обратного вызова: **OnStatus**, которые получают сообщения, относящиеся к состоянию различных аспектов средства чтения и **OnStatus**, которые получают несжатые образцы из модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="750ff-118">This includes two callback methods: **OnStatus**, which receives messages relating to the status of various aspects of the reader and **OnSample**, which receives uncompressed samples from the reader.</span></span>
2.  <span data-ttu-id="750ff-119">Приложение передает модулю чтения имя файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="750ff-119">The application passes to the reader the name of a file to read.</span></span> <span data-ttu-id="750ff-120">Когда модуль чтения открывает файл, он присваивает каждому потоку номер выхода.</span><span class="sxs-lookup"><span data-stu-id="750ff-120">When the reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="750ff-121">Если файл использует взаимное исключение, модуль чтения назначает один выход для всех взаимоисключающих потоков.</span><span class="sxs-lookup"><span data-stu-id="750ff-121">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
3.  <span data-ttu-id="750ff-122">Приложение получает сведения о конфигурации различных выходных данных из средства чтения.</span><span class="sxs-lookup"><span data-stu-id="750ff-122">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="750ff-123">Собранная информация позволит приложению правильно отображать образцы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="750ff-123">The information gathered will enable the application to properly render media samples.</span></span>
4.  <span data-ttu-id="750ff-124">Приложение сообщает модулю чтения о необходимости начать чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="750ff-124">The application instructs the reader to begin reading data from the file.</span></span> <span data-ttu-id="750ff-125">Модуль чтения начинает доставку несжатых образцов обратного вызова **OnSample** по одному за раз в буферах, упакованных в объекты буфера.</span><span class="sxs-lookup"><span data-stu-id="750ff-125">The reader begins delivering uncompressed samples to the **OnSample** callback one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="750ff-126">Образцы, доставляемые модулем чтения, находятся в порядке времени презентации.</span><span class="sxs-lookup"><span data-stu-id="750ff-126">The samples delivered by the reader are in presentation-time order.</span></span> <span data-ttu-id="750ff-127">Модуль чтения продолжит предоставлять образцы до тех пор, пока приложение не будет остановлено приложением или пока не будет достигнут конец файла.</span><span class="sxs-lookup"><span data-stu-id="750ff-127">The reader will continue delivering samples until stopped by the application or until the end of the file is reached.</span></span>
5.  <span data-ttu-id="750ff-128">Приложение отвечает за отрисовку данных после их доставки модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="750ff-128">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="750ff-129">Пакет SDK для формата Windows Media не предоставляет никаких подпрограмм отрисовки.</span><span class="sxs-lookup"><span data-stu-id="750ff-129">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="750ff-130">Как правило, приложения используют другие пакеты SDK для подготовки данных к просмотру, такие как пакет SDK для Microsoft DirectX® или функции мультимедиа пакета SDK для платформы Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="750ff-130">Typically, applications will use other SDKs to render data, such as the Microsoft DirectX® SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>
6.  <span data-ttu-id="750ff-131">По завершении чтения приложение предписывает читателю закрыть файл.</span><span class="sxs-lookup"><span data-stu-id="750ff-131">When reading is complete, the application instructs the reader to close the file.</span></span>

<span data-ttu-id="750ff-132">Эти действия проиллюстрированы в примере приложения AudioPlayer, а не в других.</span><span class="sxs-lookup"><span data-stu-id="750ff-132">These steps are illustrated in the AudioPlayer sample application, among others.</span></span> <span data-ttu-id="750ff-133">Дополнительные сведения см. в разделе [примеры приложений](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="750ff-133">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="750ff-134">Средство чтения также поддерживает более широкие возможности.</span><span class="sxs-lookup"><span data-stu-id="750ff-134">The reader also supports more advanced functionality.</span></span> <span data-ttu-id="750ff-135">Средство чтения позволяет выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="750ff-135">The reader enables you to do the following:</span></span>

-   <span data-ttu-id="750ff-136">Приостановка воспроизведения файла.</span><span class="sxs-lookup"><span data-stu-id="750ff-136">Pause playback of a file.</span></span>
-   <span data-ttu-id="750ff-137">Получение статистики производительности модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="750ff-137">Retrieve reader performance statistics.</span></span>
-   <span data-ttu-id="750ff-138">Управление выбором потока для взаимоисключающих потоков.</span><span class="sxs-lookup"><span data-stu-id="750ff-138">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="750ff-139">Вручную выделить буферы для вывода.</span><span class="sxs-lookup"><span data-stu-id="750ff-139">Manually allocate buffers for output.</span></span>
-   <span data-ttu-id="750ff-140">Укажите собственные часы.</span><span class="sxs-lookup"><span data-stu-id="750ff-140">Provide your own clock.</span></span>
-   <span data-ttu-id="750ff-141">Получение состояния файловых операций (буферизация, Загрузка или сохранение).</span><span class="sxs-lookup"><span data-stu-id="750ff-141">Retrieve the status of file operations (buffering, download, or save).</span></span>
-   <span data-ttu-id="750ff-142">Откройте файл, используя стандартный COM-интерфейс **IStream**.</span><span class="sxs-lookup"><span data-stu-id="750ff-142">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="750ff-143">Поиск конкретных точек в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="750ff-143">Seek to specific points in an ASF file.</span></span>
-   <span data-ttu-id="750ff-144">Чтение данных профиля из заголовка файла.</span><span class="sxs-lookup"><span data-stu-id="750ff-144">Read profile data from the header of the file.</span></span>

<span data-ttu-id="750ff-145">В следующих разделах подробно описывается использование объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="750ff-145">The following sections describe the use of the reader object in detail.</span></span>

-   [<span data-ttu-id="750ff-146">Реализация сообщений модуля чтения в обратном вызове OnStatus</span><span class="sxs-lookup"><span data-stu-id="750ff-146">To Implement Reader Messages in the OnStatus Callback</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [<span data-ttu-id="750ff-147">Реализация обратного вызова OnSample</span><span class="sxs-lookup"><span data-stu-id="750ff-147">To Implement the OnSample Callback</span></span>](to-implement-the-onsample-callback.md)
-   [<span data-ttu-id="750ff-148">Создание средства чтения и открытие файла</span><span class="sxs-lookup"><span data-stu-id="750ff-148">To Create a Reader and Open a File</span></span>](to-create-a-reader-and-open-a-file.md)
-   [<span data-ttu-id="750ff-149">Получение примеров мультимедиа с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="750ff-149">To Retrieve Media Samples with the Asynchronous Reader</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [<span data-ttu-id="750ff-150">Поиск по времени с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="750ff-150">To Seek By Time Using the Asynchronous Reader</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="750ff-151">Поиск по номеру кадра с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="750ff-151">To Seek By Frame Number Using the Asynchronous Reader</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="750ff-152">Поиск по коду времени SMPTE с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="750ff-152">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="750ff-153">Поиск маркеров</span><span class="sxs-lookup"><span data-stu-id="750ff-153">To Seek to Markers</span></span>](to-seek-to-markers.md)
-   [<span data-ttu-id="750ff-154">Приостановка и остановка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="750ff-154">To Pause or Stop Playback</span></span>](to-pause-or-stop-playback.md)
-   [<span data-ttu-id="750ff-155">Получение статистики производительности читателя</span><span class="sxs-lookup"><span data-stu-id="750ff-155">To Get Reader Performance Statistics</span></span>](to-get-reader-performance-statistics.md)
-   [<span data-ttu-id="750ff-156">Использование ручного выбора потока</span><span class="sxs-lookup"><span data-stu-id="750ff-156">To Use Manual Stream Selection</span></span>](to-use-manual-stream-selection.md)
-   [<span data-ttu-id="750ff-157">Доставка сжатых образцов с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="750ff-157">To Deliver Compressed Samples with the Asynchronous Reader</span></span>](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a><span data-ttu-id="750ff-158">См. также</span><span class="sxs-lookup"><span data-stu-id="750ff-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="750ff-159">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="750ff-159">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="750ff-160">**Объект модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="750ff-160">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




