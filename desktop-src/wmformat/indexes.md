---
title: Индексы
description: Индексы
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Пакет SDK для формата Windows Media, индексы
- Расширенный системный формат (ASF), индексы
- ASF (Расширенный системный формат), индексы
- Пакет SDK Windows Media Format, временные индексы
- Расширенный системный формат (ASF), временные индексы
- ASF (Расширенный системный формат), временные индексы
- Windows Media Format SDK, индексы на основе кадров
- Расширенный формат систем (ASF), индексы на основе кадров
- ASF (Расширенный системный формат), индексы на основе кадров
- Windows Media Format SDK, коды времени SMPTE
- Расширенный формат систем (ASF), коды времени SMPTE
- ASF (Расширенный системный формат), коды времени SMPTE
- индексы, сведения
- временные индексы
- индексы на основе кадров
- Коды времени SMPTE, индексы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888932"
---
# <a name="indexes"></a><span data-ttu-id="04db7-119">Индексы</span><span class="sxs-lookup"><span data-stu-id="04db7-119">Indexes</span></span>

<span data-ttu-id="04db7-120">Распространенным требованием для приложений, считывающих цифровые файлы мультимедиа, является возможность поиска в определенной точке содержимого.</span><span class="sxs-lookup"><span data-stu-id="04db7-120">A common requirement for applications that read digital media files is the ability to seek to a specific point in the content.</span></span> <span data-ttu-id="04db7-121">Поиск может быть затруднительным, поскольку нет никакой гарантии, что различные потоки в файле имеют выборки с одновременным временем начала.</span><span class="sxs-lookup"><span data-stu-id="04db7-121">Seeking can be difficult because there is no guarantee that the various streams in a file have samples with concurrent start times.</span></span> <span data-ttu-id="04db7-122">Эта проблема решена с использованием *индексов*.</span><span class="sxs-lookup"><span data-stu-id="04db7-122">This problem is addressed with the use of *indexes*.</span></span> <span data-ttu-id="04db7-123">Индекс — это объект в ASF-файле, который выдает образцы видео со временем презентации.</span><span class="sxs-lookup"><span data-stu-id="04db7-123">An index is an object in an ASF file that equates video samples with their presentation times.</span></span> <span data-ttu-id="04db7-124">Для звуковых потоков не требуется индекс, так как звуковые данные более тесно подключены к времени презентации, чем данные видео.</span><span class="sxs-lookup"><span data-stu-id="04db7-124">No index is required for audio streams because audio data is more closely connected with presentation time than video data is.</span></span>

<span data-ttu-id="04db7-125">Объект индексатора пакета SDK Windows Media Format может создавать три различных типа индексов: временные индексы, индексы на основе кадров и индексы кода времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="04db7-125">The indexer object of the Windows Media Format SDK can create three different types of indexes: temporal indexes, frame-based indexes, and SMPTE time code indexes.</span></span>

<span data-ttu-id="04db7-126">Временные индексы являются наиболее распространенным типом.</span><span class="sxs-lookup"><span data-stu-id="04db7-126">Temporal indexes are the most common type.</span></span> <span data-ttu-id="04db7-127">Они просто приравнивают видеороликов в соответствии со временем презентации.</span><span class="sxs-lookup"><span data-stu-id="04db7-127">They simply equate video samples with the corresponding presentation times.</span></span>

<span data-ttu-id="04db7-128">Индекс на основе кадров соответствует видеороликам с номерами видеокадров и временем презентации.</span><span class="sxs-lookup"><span data-stu-id="04db7-128">A frame-based index equates video samples with video frame numbers and presentation times.</span></span> <span data-ttu-id="04db7-129">Номера кадров особенно полезны в приложениях, которые редактируют видео.</span><span class="sxs-lookup"><span data-stu-id="04db7-129">Frame numbers are particularly useful in applications that edit video.</span></span>

<span data-ttu-id="04db7-130">Индекс кода времени SMTP — это редкий тип индекса.</span><span class="sxs-lookup"><span data-stu-id="04db7-130">A SMTPE time code index is the rarest type of index.</span></span> <span data-ttu-id="04db7-131">Он использует код времени SMPTE в качестве базиса для индекса и может использоваться только для потоков, которые имеют отметки времени SMPTE, включенные в выборку.</span><span class="sxs-lookup"><span data-stu-id="04db7-131">It uses SMPTE time code as the basis of the index and can be used only on streams that have SMPTE time stamps included with their samples.</span></span> <span data-ttu-id="04db7-132">Дополнительные сведения о коде времени SMPTE см. в разделе [поддержка кода времени SMPTE](smpte-time-code-support.md).</span><span class="sxs-lookup"><span data-stu-id="04db7-132">For more information about SMPTE time code, see [SMPTE Time Code Support](smpte-time-code-support.md).</span></span>

<span data-ttu-id="04db7-133">Файл ASF может содержать индекс каждого типа для каждого потока видео, который он содержит.</span><span class="sxs-lookup"><span data-stu-id="04db7-133">An ASF file can contain an index of each type for each video stream it contains.</span></span> <span data-ttu-id="04db7-134">По умолчанию для каждого видеопотока в файлах, созданных объектом модуля записи, добавляется временный индекс.</span><span class="sxs-lookup"><span data-stu-id="04db7-134">As a default, a temporal index is included for each video stream in files created by the writer object.</span></span> <span data-ttu-id="04db7-135">Вы можете изменить параметры автоматического индексирования для файлов в соответствии с вашими потребностями.</span><span class="sxs-lookup"><span data-stu-id="04db7-135">You can change the automatic indexing settings for your files to suit your needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04db7-136">См. также</span><span class="sxs-lookup"><span data-stu-id="04db7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04db7-137">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="04db7-137">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="04db7-138">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="04db7-138">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="04db7-139">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="04db7-139">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="04db7-140">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="04db7-140">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




