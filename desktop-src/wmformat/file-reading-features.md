---
title: Функции чтения файлов
description: Функции чтения файлов
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Пакет SDK для формата Windows Media, функции чтения файлов
- Пакет SDK для формата Windows Media, асинхронное чтение файлов
- Пакет SDK для формата Windows Media, синхронное чтение файлов
- Расширенный формат систем (ASF), функции чтения файлов
- ASF (Расширенный системный формат), функции чтения файлов
- Расширенный формат систем (ASF), асинхронное чтение файлов
- ASF (Расширенный системный формат), асинхронное чтение файлов
- Расширенный формат систем (ASF), синхронное чтение файлов
- ASF (Расширенный системный формат), синхронное чтение файлов
- асинхронное чтение файлов
- синхронное чтение файлов
- синхронные средства чтения, функции чтения файлов
- чтение файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332320"
---
# <a name="file-reading-features"></a><span data-ttu-id="72e14-116">Функции чтения файлов</span><span class="sxs-lookup"><span data-stu-id="72e14-116">File Reading Features</span></span>

<span data-ttu-id="72e14-117">Чтение файлов ASF — это одна из основных возможностей пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="72e14-117">Reading ASF files is one of the primary features of the Windows Media Format SDK.</span></span> <span data-ttu-id="72e14-118">Поддерживаются два типа чтения: асинхронные и синхронные.</span><span class="sxs-lookup"><span data-stu-id="72e14-118">Two types of reading are supported: asynchronous and synchronous.</span></span> <span data-ttu-id="72e14-119">Асинхронное чтение файлов обрабатывается объектом Reader.</span><span class="sxs-lookup"><span data-stu-id="72e14-119">Asynchronous file reading is handled by the reader object.</span></span> <span data-ttu-id="72e14-120">Синхронный объект чтения используется для синхронного чтения файлов.</span><span class="sxs-lookup"><span data-stu-id="72e14-120">The synchronous reader object is used to read files synchronously.</span></span> <span data-ttu-id="72e14-121">Дополнительные сведения о различных объектах чтения см. в разделе [объект Reader](reader-object.md) и [синхронный объект Reader](synchronous-reader-object.md).</span><span class="sxs-lookup"><span data-stu-id="72e14-121">For more information about the different reading objects, see [Reader Object](reader-object.md) and [Synchronous Reader Object](synchronous-reader-object.md).</span></span>

<span data-ttu-id="72e14-122">В самом базовом сценарии асинхронного чтения файлов необходимо реализовать метод обратного вызова, который будет вызываться объектом Reader при готовности образцов.</span><span class="sxs-lookup"><span data-stu-id="72e14-122">In the most basic asynchronous file reading scenario, you must implement a callback method that the reader object will call when samples are ready.</span></span> <span data-ttu-id="72e14-123">После того как вы начнете чтение файла, приложение ждет доставки образцов в метод обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="72e14-123">After you begin reading a file, your application waits for the samples to be delivered to your callback method.</span></span> <span data-ttu-id="72e14-124">Асинхронное чтение полезно для приложений проигрывателя и поддерживает функции, недоступные при синхронном чтении.</span><span class="sxs-lookup"><span data-stu-id="72e14-124">Asynchronous reading is useful for player applications, and supports features not available with synchronous reading.</span></span> <span data-ttu-id="72e14-125">Если приложению требуется считывать файлы из сетевой папки или взаимодействовать с сервером, на котором работают службы Windows Media, необходимо использовать объект Reader.</span><span class="sxs-lookup"><span data-stu-id="72e14-125">If your application needs to read files from a network location, or interact with a server running Windows Media Services, you must use the reader object.</span></span> <span data-ttu-id="72e14-126">Недостатком объекта Reader является то, что для каждого доставляемого выхода используется отдельный поток.</span><span class="sxs-lookup"><span data-stu-id="72e14-126">The disadvantage of the reader object is that a separate thread is used for each output delivered.</span></span> <span data-ttu-id="72e14-127">Кроме того, объект Reader не так гибок, как синхронное средство чтения, способное доставлять образцы.</span><span class="sxs-lookup"><span data-stu-id="72e14-127">Additionally, the reader object is not as flexible as the synchronous reader in how it can deliver samples.</span></span>

<span data-ttu-id="72e14-128">В синхронном средстве чтения не нужно использовать методы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="72e14-128">With the synchronous reader you do not need to use any callback methods.</span></span> <span data-ttu-id="72e14-129">Вместо этого следует выбрать часть файла для чтения и извлечения образцов по одному с помощью вызовов метода.</span><span class="sxs-lookup"><span data-stu-id="72e14-129">Instead, you select a portion of the file to read and retrieve the samples one at a time with method calls.</span></span> <span data-ttu-id="72e14-130">Синхронный читатель хорошо подходит для приложений, поддерживающих редактирование содержимого, где очень важно использовать быстрый доступ к конкретным образцам.</span><span class="sxs-lookup"><span data-stu-id="72e14-130">The synchronous reader is well suited to the needs of content-editing applications, where quick access to specific samples is essential.</span></span> <span data-ttu-id="72e14-131">Поскольку синхронное средство чтения не использует методы обратного вызова, вы можете создавать приложения для чтения файлов ASF с минимальными затратами на написание кода.</span><span class="sxs-lookup"><span data-stu-id="72e14-131">Because no callback methods are used by the synchronous reader, you can create applications to read ASF files with a minimum of coding overhead.</span></span> <span data-ttu-id="72e14-132">Однако синхронный модуль чтения не может открыть файл из сетевого расположения или взаимодействовать с сервером, на котором работают службы Windows Media, или считывать файлы, защищенные с помощью [*DRM*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="72e14-132">However, the synchronous reader cannot open a file from a network location, or interact with a server running Windows Media Services, or read files protected with [*DRM*](wmformat-glossary.md).</span></span>

<span data-ttu-id="72e14-133">В следующих разделах обсуждаются функции модуля чтения и синхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="72e14-133">The following topics discuss the features of the reader and the synchronous reader.</span></span>



| <span data-ttu-id="72e14-134">Раздел</span><span class="sxs-lookup"><span data-stu-id="72e14-134">Topic</span></span>                                                              | <span data-ttu-id="72e14-135">Описание</span><span class="sxs-lookup"><span data-stu-id="72e14-135">Description</span></span>                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72e14-136">Поддержка примера, выделенного пользователем</span><span class="sxs-lookup"><span data-stu-id="72e14-136">User Allocated Sample Support</span></span>](user-allocated-sample-support.md) | <span data-ttu-id="72e14-137">Обсуждается выделение буфера в модуле чтения и синхронное средство чтения, а также способ распределения пользователей по повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="72e14-137">Discusses buffer allocation in the reader and synchronous reader, and how user allocation can improve performance.</span></span> |
| [<span data-ttu-id="72e14-138">Перечисление формата вывода</span><span class="sxs-lookup"><span data-stu-id="72e14-138">Output Format Enumeration</span></span>](output-format-enumeration.md)         | <span data-ttu-id="72e14-139">Описывает перечисление формата вывода.</span><span class="sxs-lookup"><span data-stu-id="72e14-139">Discusses output format enumeration.</span></span>                                                                               |



 

<span data-ttu-id="72e14-140">Кроме того, следующие разделы из раздела «Написание функций» также применимы к чтению файлов.</span><span class="sxs-lookup"><span data-stu-id="72e14-140">In addition, the following topics from the writing features section also apply to file reading:</span></span>

-   [<span data-ttu-id="72e14-141">Изменение размера видео</span><span class="sxs-lookup"><span data-stu-id="72e14-141">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="72e14-142">Преобразование цветового пространства</span><span class="sxs-lookup"><span data-stu-id="72e14-142">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="72e14-143">Ресамплинг звука</span><span class="sxs-lookup"><span data-stu-id="72e14-143">Audio Resampling</span></span>](audio-resampling.md)

## <a name="related-topics"></a><span data-ttu-id="72e14-144">См. также</span><span class="sxs-lookup"><span data-stu-id="72e14-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72e14-145">**Компоненты**</span><span class="sxs-lookup"><span data-stu-id="72e14-145">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="72e14-146">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="72e14-146">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




