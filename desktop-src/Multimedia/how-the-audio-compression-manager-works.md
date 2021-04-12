---
title: Как работает диспетчер аудиосжатия
description: Как работает диспетчер аудиосжатия
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- мультимедиа аудио, диспетчер аудиосжатия (ACM)
- аудио, диспетчер аудиосжатия (ACM)
- Диспетчер аудиосжатия (ACM), о программе
- ACM (диспетчер аудиосжатия), сведения
- Диспетчер аудиосжатия (ACM), драйверы кодеков
- ACM (диспетчер аудиосжатия), драйверы кодеков
- Диспетчер аудиосжатия (ACM), драйверы преобразователя формата
- ACM (диспетчер аудиосжатия), драйверы преобразователя форматирования
- Диспетчер аудиосжатия (ACM), фильтровать драйверы
- ACM (диспетчер аудиосжатия), Фильтрация драйверов
- Диспетчер аудиосжатия (ACM), драйверы сжатия
- ACM (диспетчер аудиосжатия), драйверы сжатия
- Диспетчер аудиосжатия (ACM), драйверы декомпрессора
- ACM (диспетчер аудиосжатия), драйверы декомпрессора
- драйверы кодеков
- драйверы конвертера формата
- фильтровать драйверы
- драйверы сжатия
- драйверы декомпрессора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330600"
---
# <a name="how-the-audio-compression-manager-works"></a><span data-ttu-id="4c849-122">Как работает диспетчер аудиосжатия</span><span class="sxs-lookup"><span data-stu-id="4c849-122">How the Audio Compression Manager Works</span></span>

<span data-ttu-id="4c849-123">ACM использует существующие обработчики интерфейса драйвера для переопределения алгоритма сопоставления по умолчанию для устройств аудио-аудиосигнала.</span><span class="sxs-lookup"><span data-stu-id="4c849-123">The ACM uses existing driver interface hooks to override the default mapping algorithm for waveform-audio devices.</span></span> <span data-ttu-id="4c849-124">Это позволяет ACM перехватывать вызовы устройств.</span><span class="sxs-lookup"><span data-stu-id="4c849-124">This allows the ACM to intercept device-open calls.</span></span> <span data-ttu-id="4c849-125">После перехвата вызова ACM может выполнять различные задачи для обработки звуковых данных, например вставлять в последовательность внешний компрессор или декомпрессор.</span><span class="sxs-lookup"><span data-stu-id="4c849-125">After a call has been intercepted, the ACM can perform a variety of tasks to process the audio data, such as inserting an external compressor or decompressor into the sequence.</span></span>

<span data-ttu-id="4c849-126">ACM управляет следующими типами драйверов:</span><span class="sxs-lookup"><span data-stu-id="4c849-126">The ACM manages the following types of drivers:</span></span>

-   <span data-ttu-id="4c849-127">Драйверы программы сжатия и декомпрессора (кодек)</span><span class="sxs-lookup"><span data-stu-id="4c849-127">Compressor and decompressor (codec) drivers</span></span>
-   <span data-ttu-id="4c849-128">Драйверы конвертера формата</span><span class="sxs-lookup"><span data-stu-id="4c849-128">Format converter drivers</span></span>
-   <span data-ttu-id="4c849-129">Фильтровать драйверы</span><span class="sxs-lookup"><span data-stu-id="4c849-129">Filter drivers</span></span>

<span data-ttu-id="4c849-130">Программа сжатия и Декомпрессоры меняют один тип формата на другой.</span><span class="sxs-lookup"><span data-stu-id="4c849-130">Compressors and decompressors change one format type to another.</span></span> <span data-ttu-id="4c849-131">Например, программа сжатия или распаковки может изменить файл PCM (импульсный код импульса) на файл ADPCM (адаптивный разностный код пульса).</span><span class="sxs-lookup"><span data-stu-id="4c849-131">For example, a compressor or decompressor can change a PCM (Pulse Code Modulation) file to an ADPCM (Adaptive Differential Pulse Code Modulation) file.</span></span> <span data-ttu-id="4c849-132">Преобразователи формата изменяют формат, но не тип данных.</span><span class="sxs-lookup"><span data-stu-id="4c849-132">Format converters change the format, but not the data type.</span></span> <span data-ttu-id="4c849-133">Например, преобразователь может заменить 16-битные данные 44 кГц на 44-кГц, 8-разрядные данные.</span><span class="sxs-lookup"><span data-stu-id="4c849-133">For example, a converter can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span> <span data-ttu-id="4c849-134">Фильтры не изменяют формат данных вообще, но они изменяют данные звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="4c849-134">Filters do not change the data format at all, but they change the waveform-audio data in some manner.</span></span> <span data-ttu-id="4c849-135">Например, фильтр может сочетать поток данных и эхо самого себя.</span><span class="sxs-lookup"><span data-stu-id="4c849-135">For example, a filter could combine a data stream and an echo of itself.</span></span> <span data-ttu-id="4c849-136">Один драйвер ACM или тег фильтра или тег Format в драйвере также могут поддерживать сочетания предыдущих типов.</span><span class="sxs-lookup"><span data-stu-id="4c849-136">A single ACM driver, or a filter tag or format tag within a driver, might also support combinations of the preceding types.</span></span>

<span data-ttu-id="4c849-137">Для выходных данных волнового аудио ACM передает каждый буфер данных в преобразователь по мере их поступления.</span><span class="sxs-lookup"><span data-stu-id="4c849-137">For waveform-audio output, the ACM passes each buffer of data to the converter as it arrives.</span></span> <span data-ttu-id="4c849-138">Преобразователь Распаковывает данные и возвращает распакованные данные в ACM в теневом буфере.</span><span class="sxs-lookup"><span data-stu-id="4c849-138">The converter decompresses the data and returns the decompressed data to the ACM in a "shadow" buffer.</span></span> <span data-ttu-id="4c849-139">Затем ACM передает Распакованный теневой буфер в драйвер аудио-Audio.</span><span class="sxs-lookup"><span data-stu-id="4c849-139">The ACM then passes the decompressed shadow buffer to the waveform-audio driver.</span></span> <span data-ttu-id="4c849-140">ACM выделяет теневые буферы при получении сообщения подготовки.</span><span class="sxs-lookup"><span data-stu-id="4c849-140">The ACM allocates the shadow buffers whenever it receives a prepare message.</span></span>

<span data-ttu-id="4c849-141">Для входного аудио-сигнала ACM передает в драйвер пустые буферы теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="4c849-141">For waveform-audio input, the ACM passes empty shadow buffers to the driver.</span></span> <span data-ttu-id="4c849-142">Он использует фоновую задачу для получения уведомления после того, как драйвер заполнит буфер теневого буфера.</span><span class="sxs-lookup"><span data-stu-id="4c849-142">It uses a background task to receive a notification after the driver has filled the shadow buffer.</span></span> <span data-ttu-id="4c849-143">Затем ACM передает буферы в драйвер для сжатия.</span><span class="sxs-lookup"><span data-stu-id="4c849-143">The ACM then passes the buffers to the driver for compression.</span></span> <span data-ttu-id="4c849-144">После завершения сжатия драйвер передает данные в приложение.</span><span class="sxs-lookup"><span data-stu-id="4c849-144">After compression is finished, the driver passes the data to the application.</span></span>

 

 




