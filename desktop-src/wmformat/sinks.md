---
title: Приемники
description: Приемники
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Media Format SDK, приемники
- Windows Media Format SDK, приемники файлов
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- Расширенный формат систем (ASF), приемники файлов
- ASF (Расширенный системный формат), приемники файлов
- Windows Media Format SDK, приемники сети
- Windows Media Format SDK, приемники push-уведомлений
- Расширенный формат систем (ASF), сетевые приемники
- ASF (Расширенный системный формат), приемники сети
- Расширенный формат систем (ASF), приемники push-уведомлений
- ASF (Расширенный системный формат), приемники push-уведомлений
- приемники, о
- приемники файлов, сведения
- приемники сети
- приемники push-уведомлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069592"
---
# <a name="sinks"></a><span data-ttu-id="3a31c-119">Приемники</span><span class="sxs-lookup"><span data-stu-id="3a31c-119">Sinks</span></span>

<span data-ttu-id="3a31c-120">Объект модуля записи пакета SDK Windows Media Format доставляет обработанное содержимое в приемники.</span><span class="sxs-lookup"><span data-stu-id="3a31c-120">The writer object of the Windows Media Format SDK delivers processed content to sinks.</span></span> <span data-ttu-id="3a31c-121">Каждый приемник является объектом, который доставляет данные.</span><span class="sxs-lookup"><span data-stu-id="3a31c-121">Each sink is an object that delivers data.</span></span> <span data-ttu-id="3a31c-122">Точка доставки зависит от типа приемника.</span><span class="sxs-lookup"><span data-stu-id="3a31c-122">The point of delivery depends upon the type of sink.</span></span> <span data-ttu-id="3a31c-123">Существует три типа приемников: приемники файлов, приемники сети и приемники push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3a31c-123">There are three types of sinks: file sinks, network sinks, and push sinks.</span></span>

## <a name="file-sinks"></a><span data-ttu-id="3a31c-124">Приемники файлов</span><span class="sxs-lookup"><span data-stu-id="3a31c-124">File Sinks</span></span>

<span data-ttu-id="3a31c-125">Приемники файлов записывают содержимое ASF в файл на локальном или сетевом диске.</span><span class="sxs-lookup"><span data-stu-id="3a31c-125">File sinks write ASF content to a file on a local or network drive.</span></span> <span data-ttu-id="3a31c-126">При использовании объекта модуля записи для записи файла без явного добавления приемника файла модуль записи создаст его, используя имя, передаваемое в [**ивмвритер:: сетаутпутфиленаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span><span class="sxs-lookup"><span data-stu-id="3a31c-126">When you use the writer object to write a file without explicitly adding a file sink, the writer will create one for you using the name you pass to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span></span> <span data-ttu-id="3a31c-127">Объекту модуля записи можно назначить несколько приемников файлов для записи содержимого в несколько файлов одновременно.</span><span class="sxs-lookup"><span data-stu-id="3a31c-127">You can assign multiple file sinks to a writer object to write the content in several files at once.</span></span>

<span data-ttu-id="3a31c-128">С помощью приемника файлов можно управлять множеством аспектов файла.</span><span class="sxs-lookup"><span data-stu-id="3a31c-128">By using a file sink, you can control many aspects of the file.</span></span> <span data-ttu-id="3a31c-129">Следующие функции доступны в приемнике файлов.</span><span class="sxs-lookup"><span data-stu-id="3a31c-129">The following features are available through a file sink.</span></span>

-   <span data-ttu-id="3a31c-130">Мониторинг статистики файлов.</span><span class="sxs-lookup"><span data-stu-id="3a31c-130">File statistics monitoring.</span></span> <span data-ttu-id="3a31c-131">Можно отслеживать размер и длительность создаваемого файла.</span><span class="sxs-lookup"><span data-stu-id="3a31c-131">You can monitor the file size and duration as it is being created.</span></span>
-   <span data-ttu-id="3a31c-132">Создание файла с частичным содержимым.</span><span class="sxs-lookup"><span data-stu-id="3a31c-132">Partial content file creation.</span></span> <span data-ttu-id="3a31c-133">Приемники файлов можно настроить для начала записи содержимого в определенное время и для завершения записи в определенное время.</span><span class="sxs-lookup"><span data-stu-id="3a31c-133">File sinks can be configured to begin writing content at a specific time and to end writing at a specific time.</span></span> <span data-ttu-id="3a31c-134">Это позволяет создавать несколько файлов, содержащих разные разделы одного содержимого, на одном и том же этапе записи.</span><span class="sxs-lookup"><span data-stu-id="3a31c-134">This enables you to create multiple files containing different sections of the same content in the same writing pass.</span></span>

## <a name="network-sinks"></a><span data-ttu-id="3a31c-135">Приемники сети</span><span class="sxs-lookup"><span data-stu-id="3a31c-135">Network Sinks</span></span>

<span data-ttu-id="3a31c-136">Сетевые приемники пересылают содержимое на сетевой адрес.</span><span class="sxs-lookup"><span data-stu-id="3a31c-136">Network sinks broadcast content to a network address.</span></span> <span data-ttu-id="3a31c-137">Чтение клиентов может подключиться к адресу для получения вещания.</span><span class="sxs-lookup"><span data-stu-id="3a31c-137">Reading clients can connect to the address to receive the broadcast.</span></span>

## <a name="push-sinks"></a><span data-ttu-id="3a31c-138">Приемники push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="3a31c-138">Push Sinks</span></span>

<span data-ttu-id="3a31c-139">Приемники push-уведомлений доставляют содержимое из модуля записи на сервер, на котором работают службы Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3a31c-139">Push sinks deliver content from the writer to a server running Windows Media Services.</span></span> <span data-ttu-id="3a31c-140">Приемники push-уведомлений обычно используются в сценариях, где один компьютер кодирует динамическое содержимое и доставляет его на один или несколько серверов для широкого распределения.</span><span class="sxs-lookup"><span data-stu-id="3a31c-140">Push sinks are typically used in scenarios where one computer encodes live content and delivers it to one or more servers for wide distribution.</span></span> <span data-ttu-id="3a31c-141">Использование приемника push-уведомлений позволяет выделить компьютеры для выполнения конкретных задач, экономя пропускную способность и вычислительную мощность на каждом сервере.</span><span class="sxs-lookup"><span data-stu-id="3a31c-141">Using a push sink enables you to dedicate computers to specific tasks, saving bandwidth and processing power on each server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a31c-142">См. также</span><span class="sxs-lookup"><span data-stu-id="3a31c-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a31c-143">**Функции записи файлов**</span><span class="sxs-lookup"><span data-stu-id="3a31c-143">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="3a31c-144">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="3a31c-144">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




