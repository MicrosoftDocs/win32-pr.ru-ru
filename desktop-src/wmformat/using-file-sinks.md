---
title: Использование файловых приемников
description: Использование файловых приемников
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Расширенный формат систем (ASF), приемники файлов
- ASF (Расширенный системный формат), приемники файлов
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- приемники, приемники файлов
- приемники файлов, сведения
- приемники файлов, создание
- приемники файлов, остановка
- приемники файлов, запуск
- приемники файлов, закрытие
- приемники, статистика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104133578"
---
# <a name="using-file-sinks"></a><span data-ttu-id="86d0c-114">Использование файловых приемников</span><span class="sxs-lookup"><span data-stu-id="86d0c-114">Using File Sinks</span></span>

<span data-ttu-id="86d0c-115">В обычных обстоятельствах можно просто передать имя выходного файла с помощью метода [**ивмвритер:: сетаутпутфиленаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) , и объект модуля записи автоматически запишет файл на диск.</span><span class="sxs-lookup"><span data-stu-id="86d0c-115">Under normal circumstances, you can simply pass the writer an output file name using the [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) method, and the writer object will write the file to disk automatically.</span></span> <span data-ttu-id="86d0c-116">В этом случае модуль записи фактически создает и управляет объектом приемника файла модуля записи, который обрабатывает запись файла на диск.</span><span class="sxs-lookup"><span data-stu-id="86d0c-116">In this case, the writer is actually creating and controlling a writer file sink object that handles writing the file to disk.</span></span> <span data-ttu-id="86d0c-117">Объект приемника файла модуля записи управляет потоком данных из объекта модуля записи в один файл.</span><span class="sxs-lookup"><span data-stu-id="86d0c-117">A writer file sink object controls the flow of data from the writer object to a single file.</span></span>

<span data-ttu-id="86d0c-118">Можно создать собственные приемники файлов, чтобы получить больший контроль над тем, как приемник записывает файл.</span><span class="sxs-lookup"><span data-stu-id="86d0c-118">You can create your own file sinks to get more control over how the sink writes the file.</span></span> <span data-ttu-id="86d0c-119">Кроме того, можно получить доступ к приемнику файла модуля записи по умолчанию, созданному модулем записи в ответ на вызов **сетаутпутфиленаме**.</span><span class="sxs-lookup"><span data-stu-id="86d0c-119">You can also access the default writer file sink created by the writer in response to a call to **SetOutputFilename**.</span></span>

## <a name="creating-file-sinks"></a><span data-ttu-id="86d0c-120">Создание приемников файлов</span><span class="sxs-lookup"><span data-stu-id="86d0c-120">Creating File Sinks</span></span>

<span data-ttu-id="86d0c-121">Чтобы создать приемник файла и добавить его в модуль записи, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="86d0c-121">To create a file sink and add it to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="86d0c-122">Создайте новый приемник, вызвав функцию [**вмкреатевритерфилесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .</span><span class="sxs-lookup"><span data-stu-id="86d0c-122">Create a new sink by calling the [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) function.</span></span>
2.  <span data-ttu-id="86d0c-123">Укажите имя файла для приемника, вызвав [**ивмвритерфилесинк:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span><span class="sxs-lookup"><span data-stu-id="86d0c-123">Supply a file name for the sink by calling [**IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span></span>
3.  <span data-ttu-id="86d0c-124">Добавьте приемник файла в модуль записи, вызвав [**ивмвритерадванцед:: аддсинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span><span class="sxs-lookup"><span data-stu-id="86d0c-124">Add the file sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span></span>
4.  <span data-ttu-id="86d0c-125">Выполните написание обычным способом.</span><span class="sxs-lookup"><span data-stu-id="86d0c-125">Perform writing in the usual way.</span></span>
5.  <span data-ttu-id="86d0c-126">После завершения записи приемник закроет файл автоматически.</span><span class="sxs-lookup"><span data-stu-id="86d0c-126">After writing is completed, the sink will close the file automatically.</span></span>

## <a name="stopping-and-starting-file-sinks"></a><span data-ttu-id="86d0c-127">Остановка и запуск приемников файлов</span><span class="sxs-lookup"><span data-stu-id="86d0c-127">Stopping and Starting File Sinks</span></span>

<span data-ttu-id="86d0c-128">После начала записи можно прерывать в приемнике файлов, вызвав [**IWMWriterFileSink2:: останавливаться**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span><span class="sxs-lookup"><span data-stu-id="86d0c-128">After writing operations begin, you can stop writing to a file sink by calling [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span></span>

<span data-ttu-id="86d0c-129">Существует множество потенциальных причин, по которым вы захотите прерывать запись в приемник.</span><span class="sxs-lookup"><span data-stu-id="86d0c-129">There are many potential reasons why you would want to stop writing to a sink.</span></span> <span data-ttu-id="86d0c-130">Например, если вы записываете данные из активного источника, вы можете заинтересовать только часть содержимого.</span><span class="sxs-lookup"><span data-stu-id="86d0c-130">For example, if you are recording from a live source, you may only be interested in some of the content.</span></span>

<span data-ttu-id="86d0c-131">Вы можете возобновить запись в приемник файлов, вызвав [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span><span class="sxs-lookup"><span data-stu-id="86d0c-131">You can resume writing to a file sink by calling [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span></span> <span data-ttu-id="86d0c-132">И **останавливают** , и **начинают** использовать время презентации для управления приблизительно при выполнении команды.</span><span class="sxs-lookup"><span data-stu-id="86d0c-132">Both **Stop** and **Start** use presentation times to control approximately when the command is executed.</span></span> <span data-ttu-id="86d0c-133">Методы [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) можно использовать для получения большего контроля над временем начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="86d0c-133">You can use the [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) methods to gain more control over start and stop times.</span></span>

## <a name="closing-file-sinks"></a><span data-ttu-id="86d0c-134">Закрытие приемников файлов</span><span class="sxs-lookup"><span data-stu-id="86d0c-134">Closing File Sinks</span></span>

<span data-ttu-id="86d0c-135">Как правило, приемник файла закрывается автоматически.</span><span class="sxs-lookup"><span data-stu-id="86d0c-135">Normally, a file sink is closed automatically.</span></span> <span data-ttu-id="86d0c-136">Если запись в приемник закончена, но операции записи в другие приемники продолжаются, необходимо явным образом закрыть приемник для экономии ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86d0c-136">If you are finished writing to a sink, but writing operations to other sinks are continuing, you should explicitly close the sink to conserve resources.</span></span> <span data-ttu-id="86d0c-137">Чтобы закрыть приемник файла, вызовите метод [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span><span class="sxs-lookup"><span data-stu-id="86d0c-137">To close a file sink, call [**IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span></span>

## <a name="getting-sink-statistics"></a><span data-ttu-id="86d0c-138">Получение статистики приемника</span><span class="sxs-lookup"><span data-stu-id="86d0c-138">Getting Sink Statistics</span></span>

<span data-ttu-id="86d0c-139">Можно получить размер и длительность файла для открытого приемника, вызвав [**IWMWriterFileSink2:: GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) и [**IWMWriterFileSink2:: жетфиледуратион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) соответственно.</span><span class="sxs-lookup"><span data-stu-id="86d0c-139">You can get the file size and duration for an open sink by calling [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) and [**IWMWriterFileSink2::GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86d0c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="86d0c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86d0c-141">**Интерфейс Ивмвритерфилесинк**</span><span class="sxs-lookup"><span data-stu-id="86d0c-141">**IWMWriterFileSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[<span data-ttu-id="86d0c-142">**Интерфейс IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="86d0c-142">**IWMWriterFileSink2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[<span data-ttu-id="86d0c-143">**Интерфейс IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="86d0c-143">**IWMWriterFileSink3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[<span data-ttu-id="86d0c-144">**Объект приемника файлов модуля записи**</span><span class="sxs-lookup"><span data-stu-id="86d0c-144">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="86d0c-145">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="86d0c-145">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




