---
title: Чтение файлов с помощью синхронного модуля чтения
description: Чтение файлов с помощью синхронного модуля чтения
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows Media Format SDK, чтение файлов
- Пакет SDK для Windows Media Format, синхронные средства чтения
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- Расширенный формат систем (ASF), чтение файлов
- ASF (Расширенный системный формат), чтение файлов
- синхронные читатели, интерфейс Ивмреадеркаллбакк
- Ивмреадеркаллбакк, синхронные читатели
- синхронные читатели, чтение файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412491"
---
# <a name="reading-files-with-the-synchronous-reader"></a><span data-ttu-id="9aa7e-112">Чтение файлов с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="9aa7e-112">Reading Files with the Synchronous Reader</span></span>

<span data-ttu-id="9aa7e-113">Синхронное средство чтения можно использовать для чтения файла ASF с помощью синхронных вызовов вместо асинхронных методов в объекте Reader.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-113">You can use the synchronous reader to read an ASF file using synchronous calls instead of the asynchronous methods in the reader object.</span></span> <span data-ttu-id="9aa7e-114">Использование синхронных вызовов сокращает количество потоков, необходимых для чтения файла.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-114">Using synchronous calls reduces the number of threads required to read a file.</span></span> <span data-ttu-id="9aa7e-115">Асинхронный модуль чтения использует несколько потоков для обработки потоков.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-115">The asynchronous reader uses multiple threads for processing streams.</span></span> <span data-ttu-id="9aa7e-116">Для файлов с несколькими потоками количество используемых потоков может стать очень большим.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-116">For files with multiple streams, the number of threads used can become very large.</span></span> <span data-ttu-id="9aa7e-117">Синхронный читатель использует только один поток.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-117">The synchronous reader uses only one thread.</span></span>

<span data-ttu-id="9aa7e-118">Синхронное средство чтения было спроектировано в соответствии с потребностями создания содержимого и приложений для редактирования файлов.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-118">The synchronous reader was designed to meet the needs of content creation and file editing applications.</span></span> <span data-ttu-id="9aa7e-119">Синхронное средство чтения можно использовать для других приложений, но его функциональные возможности ограничены.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-119">You can use the synchronous reader for other applications, but its functionality is limited.</span></span>

<span data-ttu-id="9aa7e-120">Синхронный читатель может открывать локальные файлы или файлы в сети по UNC-пути (например, " \\ \\ сомешаре \\ сомедиректори \\ somefile. wmv").</span><span class="sxs-lookup"><span data-stu-id="9aa7e-120">The synchronous reader can open files that are local, or files on a network using the UNC path name (such as "\\\\someshare\\somedirectory\\somefile.wmv").</span></span> <span data-ttu-id="9aa7e-121">Вы не можете выполнять потоковую передачу файлов в синхронное средство чтения или открывать файлы из расположения в Интернете.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-121">You cannot stream files to the synchronous reader, or open files from an Internet location.</span></span> <span data-ttu-id="9aa7e-122">Синхронное средство чтения также обеспечивает поддержку использования интерфейса **IStream** com в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-122">The synchronous reader also provides support for using the **IStream** COM interface as a source.</span></span>

<span data-ttu-id="9aa7e-123">Синхронное средство чтения предоставляет больше универсальности для извлечения примеров из файла ASF, чем асинхронный модуль чтения.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-123">The synchronous reader provides more versatility for retrieving samples from an ASF file than the asynchronous reader.</span></span> <span data-ttu-id="9aa7e-124">Синхронный читатель может доставлять образцы по номеру потока, а также по выходным данным.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-124">The synchronous reader can deliver samples by stream number as well as by output.</span></span> <span data-ttu-id="9aa7e-125">Образцы, доставляемые номером потока, могут быть сжаты или распакованы.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-125">Samples delivered by stream number can be compressed or uncompressed.</span></span> <span data-ttu-id="9aa7e-126">Синхронное средство чтения может также переключаться между сжатой и несжатой доставкой во время воспроизведения. Эта функция называется «быстрое редактирование».</span><span class="sxs-lookup"><span data-stu-id="9aa7e-126">The synchronous reader can also switch between compressed and uncompressed delivery during playback; this feature is known as "fast editing."</span></span> <span data-ttu-id="9aa7e-127">Эта функция позволяет приложению редактирования читать содержимое на основе Windows Media и передавать его непосредственно в модуль записи, пока не будет достигнут нужный кадр.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-127">This feature enables an editing application to read Windows Media-based content and pass it directly through to the writer until a desired frame is reached.</span></span> <span data-ttu-id="9aa7e-128">На этом этапе приложение может сообщить модулю чтения о необходимости начать доставку несжатого содержимого, которое затем приложение может изменить и передать в модуль записи для повторного сжатия.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-128">At that point the application can tell the reader to start delivering uncompressed content, which the application can then modify and pass to the writer for recompression.</span></span> <span data-ttu-id="9aa7e-129">Когда приложение закончит изменение указанных кадров, оно может сообщить модулю чтения о необходимости начать доставку сжатых кадров.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-129">When the application has finished modifying the specified frames, it can tell the reader to start delivering compressed frames again.</span></span>

<span data-ttu-id="9aa7e-130">Основные функции синхронного объекта Reader можно разделить на следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-130">The most basic functionality of the synchronous reader object can be broken down into the following steps.</span></span> <span data-ttu-id="9aa7e-131">На этих этапах "приложение" относится к программе, которую вы пишете с помощью пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-131">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="9aa7e-132">Приложение передает синхронному средству чтения имя файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-132">The application passes to the synchronous reader the name of a file to read.</span></span> <span data-ttu-id="9aa7e-133">Когда синхронный модуль чтения открывает файл, он присваивает каждому потоку номер выхода.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-133">When the synchronous reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="9aa7e-134">Если файл использует взаимное исключение, модуль чтения назначает один выход для всех взаимоисключающих потоков.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-134">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
2.  <span data-ttu-id="9aa7e-135">Приложение получает сведения о конфигурации различных выходных данных из средства чтения.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-135">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="9aa7e-136">Собранная информация позволит приложению правильно отображать образцы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-136">The information gathered will enable the application to properly render media samples.</span></span>
3.  <span data-ttu-id="9aa7e-137">Приложение начинает запрашивать образцы, по одному за раз, из синхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-137">The application begins requesting samples, one at a time, from the synchronous reader.</span></span> <span data-ttu-id="9aa7e-138">Синхронный читатель доставляет каждый пример в объект buffer, для которого он доставляет интерфейс [**инссбуффер**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .</span><span class="sxs-lookup"><span data-stu-id="9aa7e-138">The synchronous reader delivers each sample in a buffer object for which it delivers the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface.</span></span>
4.  <span data-ttu-id="9aa7e-139">Приложение отвечает за отрисовку данных после их доставки модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-139">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="9aa7e-140">Пакет SDK для формата Windows Media не предоставляет никаких подпрограмм отрисовки.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-140">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="9aa7e-141">Как правило, приложения используют другие пакеты SDK для визуализации данных, например пакет SDK Microsoft Direct X, или мультимедийные функции пакета SDK для платформы Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-141">Typically, applications will use other SDKs to render data, such as the Microsoft Direct X SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>

<span data-ttu-id="9aa7e-142">Эти шаги показаны в примере приложения Вмсинкреадер.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-142">These steps are illustrated in the WMSyncReader sample application.</span></span> <span data-ttu-id="9aa7e-143">Дополнительные сведения см. в разделе [примеры приложений](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9aa7e-143">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="9aa7e-144">Синхронное средство чтения также поддерживает более сложные функции.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-144">The synchronous reader also supports more advanced functionality.</span></span> <span data-ttu-id="9aa7e-145">Синхронное средство чтения позволяет выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-145">The synchronous reader enables you to do the following:</span></span>

-   <span data-ttu-id="9aa7e-146">Укажите диапазон выборок для получения по времени или по номеру кадра.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-146">Specify a range of samples to retrieve by time or by frame number.</span></span>
-   <span data-ttu-id="9aa7e-147">Управление выбором потока для взаимоисключающих потоков.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-147">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="9aa7e-148">Откройте файл, используя стандартный COM-интерфейс **IStream**.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-148">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="9aa7e-149">Чтение данных профиля из заголовка файла.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-149">Read profile data from the file header.</span></span>
-   <span data-ttu-id="9aa7e-150">Считывает метаданные из заголовка файла.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-150">Read metadata from the file header.</span></span>
-   <span data-ttu-id="9aa7e-151">Переключение между потоковых и выходными примерами во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-151">Switch between stream and output samples during playback.</span></span>
-   <span data-ttu-id="9aa7e-152">Переключение между сжатыми и распакованными примерами потока во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-152">Switch between compressed and uncompressed stream samples during playback.</span></span>

<span data-ttu-id="9aa7e-153">В следующих разделах подробно описывается использование синхронного объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-153">The following sections describe the use of the synchronous reader object in detail.</span></span>

-   [<span data-ttu-id="9aa7e-154">Создание синхронного средства чтения и открытие файла</span><span class="sxs-lookup"><span data-stu-id="9aa7e-154">To Create a Synchronous Reader and Open a File</span></span>](to-create-a-synchronous-reader-and-open-a-file.md)
-   [<span data-ttu-id="9aa7e-155">Поиск номеров потоков и выходных номеров</span><span class="sxs-lookup"><span data-stu-id="9aa7e-155">To Find Stream Numbers and Output Numbers</span></span>](to-find-stream-numbers-and-output-numbers.md)
-   [<span data-ttu-id="9aa7e-156">Получение примеров мультимедиа с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="9aa7e-156">To Retrieve Media Samples with the Synchronous Reader</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="9aa7e-157">Поиск по времени с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="9aa7e-157">To Seek By Time Using the Synchronous Reader</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
-   [<span data-ttu-id="9aa7e-158">Поиск по номеру кадра с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="9aa7e-158">To Seek By Frame Number Using the Synchronous Reader</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [<span data-ttu-id="9aa7e-159">Поиск по коду времени SMPTE с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="9aa7e-159">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [<span data-ttu-id="9aa7e-160">Получение примеров Stream с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="9aa7e-160">To Retrieve Stream Samples with the Synchronous Reader</span></span>](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="9aa7e-161">Извлечение сжатых образцов с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="9aa7e-161">To Retrieve Compressed Samples with the Synchronous Reader</span></span>](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

<span data-ttu-id="9aa7e-162">**Пример кода**</span><span class="sxs-lookup"><span data-stu-id="9aa7e-162">**Example Code**</span></span>

<span data-ttu-id="9aa7e-163">В следующем примере кода показано, как считывать образцы из файла ASF с помощью синхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-163">The following example code shows how to read samples from an ASF file using the synchronous reader.</span></span> <span data-ttu-id="9aa7e-164">Он указывает номер кадра, диапазон выборок для доставки.</span><span class="sxs-lookup"><span data-stu-id="9aa7e-164">It specifies by frame number a range of samples to deliver.</span></span>


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="9aa7e-165">См. также</span><span class="sxs-lookup"><span data-stu-id="9aa7e-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aa7e-166">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="9aa7e-166">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="9aa7e-167">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="9aa7e-167">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="9aa7e-168">**Объект модуля синхронного чтения**</span><span class="sxs-lookup"><span data-stu-id="9aa7e-168">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> </dl>

 

 




