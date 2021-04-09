---
title: Взаимное исключение
description: Взаимное исключение
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- Пакет SDK для Windows Media Format, взаимное исключение
- Расширенный формат систем (ASF), взаимное исключение
- ASF (Расширенный системный формат), взаимное исключение
- Windows Media Format SDK, взаимное исключение MBR
- Расширенный формат систем (ASF), взаимное исключение MBR
- ASF (расширенный формат систем), взаимное исключение MBR
- Windows Media Format SDK, несколько битов (MBR)
- Расширенный формат систем (ASF), несколько битов (MBR)
- ASF (Расширенный системный формат), несколько битов (MBR)
- взаимное исключение, сведения
- несколько битов (MBR), взаимное исключение
- MBR (Многоразрядная скорость), взаимное исключение
- взаимное исключение, скорость потока
- взаимное исключение, язык
- взаимное исключение, презентация
- взаимное исключение, неизвестно
- взаимное исключение, функции
- взаимное исключение, дополнительные возможности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889124"
---
# <a name="mutual-exclusion"></a><span data-ttu-id="5484c-121">Взаимное исключение</span><span class="sxs-lookup"><span data-stu-id="5484c-121">Mutual Exclusion</span></span>

<span data-ttu-id="5484c-122">Каждый ASF – файл содержит один или несколько потоков, каждый из которых содержит цифровые данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5484c-122">Every ASF file contains one or more streams, each containing digital media data.</span></span> <span data-ttu-id="5484c-123">В нормальных обстоятельствах каждый поток связан с одним выходом.</span><span class="sxs-lookup"><span data-stu-id="5484c-123">Under normal circumstances, each stream is associated with a single output.</span></span> <span data-ttu-id="5484c-124">При воспроизведении объект Reader предоставляет образцы для каждого выхода.</span><span class="sxs-lookup"><span data-stu-id="5484c-124">On playback, the reader object delivers samples for each output.</span></span> <span data-ttu-id="5484c-125">Таким образом, по умолчанию каждый поток в ASF-файле доставляется модулем чтения при воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="5484c-125">So, as a default, every stream in an ASF file is delivered by the reader on playback.</span></span>

<span data-ttu-id="5484c-126">Бывают ситуации, когда не требуется, чтобы каждый поток доставлялся клиенту.</span><span class="sxs-lookup"><span data-stu-id="5484c-126">There are situations where you do not want every stream delivered to the client.</span></span> <span data-ttu-id="5484c-127">Например, если вы создадите видеофайл с пятью звуковыми потоками, по одному на каждый из пяти языков, вам нужно доставить только один из них за раз.</span><span class="sxs-lookup"><span data-stu-id="5484c-127">For example, if you create a video file with five audio streams, one for each of five languages, you want only one of them to be delivered at a time.</span></span> <span data-ttu-id="5484c-128">Взаимное исключение является компонентом пакета SDK Windows Media Format, который позволяет указать несколько взаимоисключающих потоков, каждый из которых будет одинаковым выходом.</span><span class="sxs-lookup"><span data-stu-id="5484c-128">Mutual exclusion is a feature of the Windows Media Format SDK that enables you to specify a number of mutually exclusive streams that all equate to the same output.</span></span>

<span data-ttu-id="5484c-129">Взаимное исключение определяется в профиле, используемом для создания файла.</span><span class="sxs-lookup"><span data-stu-id="5484c-129">Mutual exclusion is defined in the profile used to create a file.</span></span> <span data-ttu-id="5484c-130">Взаимное исключение настраивается в профиле с помощью взаимоисключающих объектов.</span><span class="sxs-lookup"><span data-stu-id="5484c-130">You configure mutual exclusion in a profile by using mutual exclusion objects.</span></span> <span data-ttu-id="5484c-131">Потоки добавляются в объект взаимного исключения по одному за раз, устанавливают тип и включают объект в профиль.</span><span class="sxs-lookup"><span data-stu-id="5484c-131">You add streams one at a time to the mutual exclusion object, set the type, and include the object in the profile.</span></span>

<span data-ttu-id="5484c-132">Пакет SDK для формата Windows Media поддерживает четыре типа взаимного исключения:</span><span class="sxs-lookup"><span data-stu-id="5484c-132">The Windows Media Format SDK recognizes four types of mutual exclusion:</span></span>

-   <span data-ttu-id="5484c-133">Скорость потока</span><span class="sxs-lookup"><span data-stu-id="5484c-133">Bit rate</span></span>
-   <span data-ttu-id="5484c-134">Язык</span><span class="sxs-lookup"><span data-stu-id="5484c-134">Language</span></span>
-   <span data-ttu-id="5484c-135">Уровень представления</span><span class="sxs-lookup"><span data-stu-id="5484c-135">Presentation</span></span>
-   <span data-ttu-id="5484c-136">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="5484c-136">Unknown</span></span>

## <a name="mutual-exclusion-by-bit-rate"></a><span data-ttu-id="5484c-137">Взаимное исключение по скорости разрядности</span><span class="sxs-lookup"><span data-stu-id="5484c-137">Mutual Exclusion by Bit Rate</span></span>

<span data-ttu-id="5484c-138">Взаимное исключение поразрядной скорости — это особый тип взаимного исключения, который чаще всего называется взаимным исключением с несколькими битовыми частотами (MBR).</span><span class="sxs-lookup"><span data-stu-id="5484c-138">Bit rate mutual exclusion is a special type of mutual exclusion and is more commonly referred to as multiple bit rate (MBR) mutual exclusion.</span></span> <span data-ttu-id="5484c-139">Взаимное исключение MBR содержит ряд потоков, исходящих из одних и тех же входных данных, но закодированных с разной скоростью.</span><span class="sxs-lookup"><span data-stu-id="5484c-139">An MBR mutual exclusion contains a number of streams that all originate from the same input, but are encoded at different bit rates.</span></span> <span data-ttu-id="5484c-140">При воспроизведении файла с помощью MBR средство чтения определяет оптимальный поток, используемый в зависимости от доступной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="5484c-140">When playing a file with MBR, the reader determines the best stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="5484c-141">Пакет SDK Windows Media Format поддерживает MBR для аудио-и видеопотоков.</span><span class="sxs-lookup"><span data-stu-id="5484c-141">The Windows Media Format SDK supports MBR for audio and video streams.</span></span> <span data-ttu-id="5484c-142">Пакет SDK также поддерживает Специальный тип видео MBR, который называется размером MBR для нескольких видеороликов.</span><span class="sxs-lookup"><span data-stu-id="5484c-142">The SDK also supports a special type of MBR video called multiple video size MBR.</span></span> <span data-ttu-id="5484c-143">Это похоже на нормальное видео MBR, за исключением того, что отдельные потоки могут иметь разные размеры кадров.</span><span class="sxs-lookup"><span data-stu-id="5484c-143">This is like normal MBR video except that the individual streams can have different frame sizes.</span></span> <span data-ttu-id="5484c-144">Например, у вас могут быть некоторые потоки с размером видео по умолчанию 320 x 240, а также некоторые другие с более высокими скоростями и размером изображения 640 x 480.</span><span class="sxs-lookup"><span data-stu-id="5484c-144">For example, you might have some streams at the default 320 x 240 video size and some others with higher bit rates and 640 x 480 video size.</span></span>

## <a name="mutual-exclusion-by-language"></a><span data-ttu-id="5484c-145">Взаимное исключение по языку</span><span class="sxs-lookup"><span data-stu-id="5484c-145">Mutual Exclusion by Language</span></span>

<span data-ttu-id="5484c-146">Взаимное исключение на основе языка предназначено для использования с содержимым (обычно аудио), записанным на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="5484c-146">Language-based mutual exclusion is designed for use with content (usually audio) recorded in several languages.</span></span> <span data-ttu-id="5484c-147">Взаимное исключение на основе языка включает несколько потоков, исходящих из уникальных входных данных.</span><span class="sxs-lookup"><span data-stu-id="5484c-147">A language-based mutual exclusion includes several streams that originate from unique inputs.</span></span> <span data-ttu-id="5484c-148">Каждый вход имеет одно и то же содержимое, но на другом языке.</span><span class="sxs-lookup"><span data-stu-id="5484c-148">Each input is the same content, but in a different language.</span></span>

<span data-ttu-id="5484c-149">Для взаимного исключения по языку приложение для чтения должно включать логику для выбора соответствующего языка.</span><span class="sxs-lookup"><span data-stu-id="5484c-149">For mutual exclusion by language to work, the reading application must include logic to select the appropriate language.</span></span> <span data-ttu-id="5484c-150">Если вы напишете приложение для воспроизведения файлов ASF и хотите поддерживать файлы с взаимным исключением на основе языка, следует выбрать соответствующий поток перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5484c-150">If you write an application to play ASF files, and you want to support files with language-based mutual exclusion, you should select the appropriate stream before beginning playback.</span></span>

## <a name="mutual-exclusion-by-presentation"></a><span data-ttu-id="5484c-151">Взаимное исключение по презентации</span><span class="sxs-lookup"><span data-stu-id="5484c-151">Mutual Exclusion by Presentation</span></span>

<span data-ttu-id="5484c-152">Взаимное исключение на основе презентации предоставляется для поддержки потоков видео, содержащих то же содержимое в кодировке с разными пропорциями.</span><span class="sxs-lookup"><span data-stu-id="5484c-152">Presentation-based mutual exclusion is provided to support video streams that contain the same content encoded with different aspect ratios.</span></span> <span data-ttu-id="5484c-153">Как правило, он используется при предоставлении видео в леттербокс версии (пропорции 16:9), а также в формате для экранов телепередач (пропорции 4:3).</span><span class="sxs-lookup"><span data-stu-id="5484c-153">Typically, this is used when providing video in a letterbox version (aspect ratio 16:9) as well as formatted for television screens (aspect ratio 4:3).</span></span>

<span data-ttu-id="5484c-154">Выбор презентации для воспроизведения чаще всего определяется пользователем.</span><span class="sxs-lookup"><span data-stu-id="5484c-154">The selection of a presentation for playback is most often determined by the user.</span></span> <span data-ttu-id="5484c-155">При написании приложения для воспроизведения файлов ASF и необходимости поддержки файлов с взаимным исключением на основе презентации необходимо предоставить пользователю возможность выбрать тип представления для просмотра.</span><span class="sxs-lookup"><span data-stu-id="5484c-155">If you write an application to play ASF files and want to support files with presentation based mutual exclusion, you should present the user with the option of selecting a presentation type for viewing.</span></span>

## <a name="unknown-mutual-exclusion"></a><span data-ttu-id="5484c-156">Неизвестное взаимное исключение</span><span class="sxs-lookup"><span data-stu-id="5484c-156">Unknown Mutual Exclusion</span></span>

<span data-ttu-id="5484c-157">Можно создать взаимное исключение на основе любого требуемого критерия.</span><span class="sxs-lookup"><span data-stu-id="5484c-157">You can create mutual exclusion based on any criteria you like.</span></span> <span data-ttu-id="5484c-158">Все пользовательские типы взаимных исключений следует создавать с помощью неизвестного типа.</span><span class="sxs-lookup"><span data-stu-id="5484c-158">All custom mutual exclusion types should be created using the unknown type.</span></span>

## <a name="advanced-mutual-exclusion-features"></a><span data-ttu-id="5484c-159">Расширенные функции взаимного исключения</span><span class="sxs-lookup"><span data-stu-id="5484c-159">Advanced Mutual Exclusion Features</span></span>

<span data-ttu-id="5484c-160">Можно также использовать взаимное исключение для назначения потоков группам, которые являются взаимоисключающими друг с другом.</span><span class="sxs-lookup"><span data-stu-id="5484c-160">You can also use mutual exclusion to assign streams to groups that are mutually exclusive of one another.</span></span> <span data-ttu-id="5484c-161">Например, может потребоваться использовать звуковые потоки на нескольких языках и назначать каждому из них свой поток видео.</span><span class="sxs-lookup"><span data-stu-id="5484c-161">For example, you might want to have audio streams in multiple languages and assign a different video stream to each.</span></span> <span data-ttu-id="5484c-162">Взаимное исключение используется для группирования каждого звукового потока с соответствующим видеопотоком и делает все группы взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="5484c-162">You use mutual exclusion to group each audio stream with its corresponding video stream and make all groups mutually exclusive.</span></span>

<span data-ttu-id="5484c-163">Модуль чтения автоматически выбирает потоки для всех взаимоисключающих исключений.</span><span class="sxs-lookup"><span data-stu-id="5484c-163">The reader automatically selects streams for all mutual exclusions.</span></span> <span data-ttu-id="5484c-164">Для всех типов взаимного исключения, кроме MBR и взаимного исключения на основе языка, читатель всегда выбирает поток по умолчанию, который является первым потоком, добавленным в объект взаимного исключения в профиле.</span><span class="sxs-lookup"><span data-stu-id="5484c-164">For all types of mutual exclusion except MBR and language-based mutual exclusion, the reader always selects the default stream, which is the first stream added to the mutual exclusion object in the profile.</span></span> <span data-ttu-id="5484c-165">Для MBR средство чтения выбирает поток, который лучше подходит для доступной пропускной способности во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5484c-165">For MBR, the reader selects the stream that best suits the available bandwidth at the time of playback.</span></span> <span data-ttu-id="5484c-166">Если вы не хотите использовать поток по умолчанию, можно задать для параметра потокового выбора значение вручную, прежде чем начать чтение файла.</span><span class="sxs-lookup"><span data-stu-id="5484c-166">If you do not want to use the default stream, you can set stream selection to manual before starting to read a file.</span></span>

<span data-ttu-id="5484c-167">Выбор потока вручную применяется ко всему файлу.</span><span class="sxs-lookup"><span data-stu-id="5484c-167">Manual stream selection applies to the entire file.</span></span> <span data-ttu-id="5484c-168">Проблемы могут возникать при наличии взаимного исключения различных типов в одном файле.</span><span class="sxs-lookup"><span data-stu-id="5484c-168">Difficulties can arise when you have mutual exclusions of different types in the same file.</span></span> <span data-ttu-id="5484c-169">Например, файл может содержать как взаимное исключение на основе битовой скорости, так и пользовательское взаимное исключение.</span><span class="sxs-lookup"><span data-stu-id="5484c-169">For example, a file can contain both bit-rate-based mutual exclusion and custom mutual exclusion.</span></span> <span data-ttu-id="5484c-170">Чтобы выбрать поток, отличный от значения по умолчанию в настраиваемом взаимном исключении, необходимо использовать ручной выбор потока.</span><span class="sxs-lookup"><span data-stu-id="5484c-170">To select a stream other than the default in the custom mutual exclusion, you must use manual stream selection.</span></span> <span data-ttu-id="5484c-171">Однако если вы используете ручной выбор потока, модуль чтения не будет автоматически выбирать поток многоразрядной скорости.</span><span class="sxs-lookup"><span data-stu-id="5484c-171">If you use manual stream selection, however, the reader will not automatically select the multiple bit rate stream.</span></span> <span data-ttu-id="5484c-172">Если планируется поддержка нескольких типов взаимного исключения в одном файле, необходимо спланировать эту возможность в приложении.</span><span class="sxs-lookup"><span data-stu-id="5484c-172">You must plan for this eventuality in your application if you plan to support multiple types of mutual exclusion in a single file.</span></span> <span data-ttu-id="5484c-173">Обычно это означает создание собственных подпрограмм выбора потоков для обычно автоматических типов взаимного исключения.</span><span class="sxs-lookup"><span data-stu-id="5484c-173">Typically this means creating your own stream selection routines for normally automatic types of mutual exclusion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5484c-174">См. также</span><span class="sxs-lookup"><span data-stu-id="5484c-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5484c-175">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="5484c-175">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="5484c-176">**Использование взаимного исключения**</span><span class="sxs-lookup"><span data-stu-id="5484c-176">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> </dl>

 

 




