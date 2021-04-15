---
description: Модуль чтения исходного кода является альтернативой использованию сеанса мультимедиа и конвейера Microsoft Media Foundation для обработки данных мультимедиа.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Модуль чтения исходного кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543799"
---
# <a name="source-reader"></a><span data-ttu-id="9dc62-103">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="9dc62-103">Source Reader</span></span>

<span data-ttu-id="9dc62-104">Модуль чтения исходного кода является альтернативой использованию [сеанса мультимедиа](media-session.md) и конвейера Microsoft Media Foundation для обработки данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dc62-104">The Source Reader is an alternative to using the [Media Session](media-session.md) and the Microsoft Media Foundation pipeline to process media data.</span></span>

## <a name="why-use-the-source-reader"></a><span data-ttu-id="9dc62-105">Зачем использовать модуль чтения исходного кода?</span><span class="sxs-lookup"><span data-stu-id="9dc62-105">Why Use the Source Reader?</span></span>

<span data-ttu-id="9dc62-106">Media Foundation предоставляет конвейер, оптимизированный для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9dc62-106">Media Foundation provides a pipeline that is optimized for playback.</span></span> <span data-ttu-id="9dc62-107">Конвейер является сквозным, то есть обрабатывает поток данных из источника (например, видеофайл) на место назначения (например, графическое отображение).</span><span class="sxs-lookup"><span data-stu-id="9dc62-107">The pipeline is end-to-end, meaning it handles data flow from the source (such as a video file) all the way to the destination (such as the graphics display).</span></span> <span data-ttu-id="9dc62-108">Однако если вы хотите считывать или изменять данные по мере прохождения конвейера, необходимо написать пользовательский подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="9dc62-108">However, if you want to read or modify the data as it goes through the pipeline, you must write a custom plug-in.</span></span> <span data-ttu-id="9dc62-109">Для этого требуется довольно глубокая информация о конвейере Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9dc62-109">That requires a fairly deep knowledge of the Media Foundation pipeline.</span></span> <span data-ttu-id="9dc62-110">Для некоторых задач Создание нового подключаемого модуля требует слишком больших издержек.</span><span class="sxs-lookup"><span data-stu-id="9dc62-110">For certain tasks, creating a new plug-in is too much overhead.</span></span> <span data-ttu-id="9dc62-111">Модуль чтения исходного кода предназначен для такого типа ситуаций, когда требуется получить необработанные данные из источника без дополнительной нагрузки на весь конвейер.</span><span class="sxs-lookup"><span data-stu-id="9dc62-111">The source reader is designed for this type of situation, when you want to get the raw data from a source without the overhead of the entire pipeline.</span></span>

<span data-ttu-id="9dc62-112">На внутреннем уровне средство чтения исходного кода содержит указатель на источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dc62-112">Internally, the source reader holds a pointer to a media source.</span></span> <span data-ttu-id="9dc62-113">*Источник мультимедиа* — это Media Foundation объект, который создает мультимедийные данные из внешнего источника, например файл мультимедиа или устройство видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="9dc62-113">A *media source* is a Media Foundation object that generates media data from an external source, such as a media file or video capture device.</span></span> <span data-ttu-id="9dc62-114">Модуль чтения исходного кода управляет всеми вызовами методов к источнику мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dc62-114">The source reader manages all of the method calls to the media source.</span></span> <span data-ttu-id="9dc62-115">(Дополнительные сведения об источниках мультимедиа см. в разделе [источники мультимедиа](media-sources.md).)</span><span class="sxs-lookup"><span data-stu-id="9dc62-115">(For more information about media sources, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="9dc62-116">Если источник мультимедиа доставляет сжатые данные, для декодирования данных можно использовать модуль чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="9dc62-116">If the media source delivers compressed data, you can use the source reader to decode the data.</span></span> <span data-ttu-id="9dc62-117">В этом случае модуль чтения исходного кода загрузит правильный декодер и будет управлять потоком данных между источником мультимедиа и декодером.</span><span class="sxs-lookup"><span data-stu-id="9dc62-117">In that case, the source reader will load the correct decoder and manage the data flow between the media source and the decoder.</span></span> <span data-ttu-id="9dc62-118">Модуль чтения исходного кода также может выполнять некоторую ограниченную обработку видео: Преобразование цветов из YUV в RGB-32 и программное чередование, хотя эти операции не рекомендуются для отрисовки видео в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="9dc62-118">The source reader can also perform some limited video processing: color conversion from YUV to RGB-32, and software deinterlacing, although these operations are not recommended for real-time video rendering.</span></span> <span data-ttu-id="9dc62-119">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9dc62-119">The following image illustrates this process.</span></span>

![схема модуля чтения исходного кода](images/sourcereader.png)

<span data-ttu-id="9dc62-121">Модуль чтения исходного кода не отправляет данные в место назначения; приложение может использовать данные.</span><span class="sxs-lookup"><span data-stu-id="9dc62-121">The source reader does not send the data to a destination; it is up to the application to consume the data.</span></span> <span data-ttu-id="9dc62-122">Например, модуль чтения исходного кода может читать видеофайл, но не отображает видео на экране.</span><span class="sxs-lookup"><span data-stu-id="9dc62-122">For example, the source reader can read a video file, but it will not render the video to the screen.</span></span> <span data-ttu-id="9dc62-123">Кроме того, модуль чтения исходного кода не управляет часами представления, обрабатывает проблемы времени или синхронизирует видео с аудио.</span><span class="sxs-lookup"><span data-stu-id="9dc62-123">Also, the source reader does not manage a presentation clock, handle timing issues, or synchronize video with audio.</span></span>

<span data-ttu-id="9dc62-124">Используйте модуль чтения исходного кода, если:</span><span class="sxs-lookup"><span data-stu-id="9dc62-124">Consider using the source reader when:</span></span>

-   <span data-ttu-id="9dc62-125">Вы хотите получить данные из файла мультимедиа, не беспокоясь о базовой структуре файлов.</span><span class="sxs-lookup"><span data-stu-id="9dc62-125">You want to get data from a media file without worrying about the underlying file structure.</span></span>
-   <span data-ttu-id="9dc62-126">Вы хотите получить данные с аудио или видео устройства записи.</span><span class="sxs-lookup"><span data-stu-id="9dc62-126">You want to get data from an audio or video capture device.</span></span>
-   <span data-ttu-id="9dc62-127">Задачи обработки данных не учитывают время или не требуются часы презентации.</span><span class="sxs-lookup"><span data-stu-id="9dc62-127">Your data-processing tasks are not time sensitive, or you do not require a presentation clock.</span></span>
-   <span data-ttu-id="9dc62-128">У вас уже есть конвейер мультимедиа, который не основан на Media Foundation и вы хотите внедрить Media Foundation источники мультимедиа в собственный конвейер.</span><span class="sxs-lookup"><span data-stu-id="9dc62-128">You already have a media pipeline that is not based on Media Foundation, and you want to incorporate the Media Foundation media sources into your own pipeline.</span></span>

<span data-ttu-id="9dc62-129">Модуль чтения исходного кода не рекомендуется использовать в следующих ситуациях.</span><span class="sxs-lookup"><span data-stu-id="9dc62-129">The source reader is not recommended in the following situations:</span></span>

-   <span data-ttu-id="9dc62-130">Для защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="9dc62-130">For protected content.</span></span> <span data-ttu-id="9dc62-131">Модуль чтения исходного кода не поддерживает управление цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="9dc62-131">The source reader does not support digital rights management (DRM).</span></span>
-   <span data-ttu-id="9dc62-132">Если вас интересуют сведения о базовой структуре файлов.</span><span class="sxs-lookup"><span data-stu-id="9dc62-132">If you care about the details of the underlying file structure.</span></span> <span data-ttu-id="9dc62-133">Модуль чтения исходного кода скрывает этот тип детализации.</span><span class="sxs-lookup"><span data-stu-id="9dc62-133">The source reader hides that type of detail.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9dc62-134">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9dc62-134">In this section</span></span>



| <span data-ttu-id="9dc62-135">Раздел</span><span class="sxs-lookup"><span data-stu-id="9dc62-135">Topic</span></span>                                                                                                        | <span data-ttu-id="9dc62-136">Описание</span><span class="sxs-lookup"><span data-stu-id="9dc62-136">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dc62-137">Использование модуля чтения исходного кода для обработки данных мультимедиа</span><span class="sxs-lookup"><span data-stu-id="9dc62-137">Using the Source Reader to Process Media Data</span></span>](processing-media-data-with-the-source-reader.md)<br/> | <span data-ttu-id="9dc62-138">В этом разделе описывается использование модуля чтения исходного кода для обработки данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9dc62-138">This topic describes how to use the Source Reader to process media data.</span></span><br/>                                               |
| [<span data-ttu-id="9dc62-139">Использование модуля чтения исходного кода в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="9dc62-139">Using the Source Reader in Asynchronous Mode</span></span>](using-the-source-reader-in-asynchronous-mode.md)<br/>  | <span data-ttu-id="9dc62-140">В этом разделе описывается использование модуля чтения исходного кода в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="9dc62-140">This topic describes how to use the Source Reader in asynchronous mode.</span></span><br/>                                                |
| [<span data-ttu-id="9dc62-141">Учебник. декодирование аудио</span><span class="sxs-lookup"><span data-stu-id="9dc62-141">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)<br/>                                          | <span data-ttu-id="9dc62-142">В этом учебнике показано, как использовать средство чтения исходного кода для декодирования звука из файла мультимедиа и записи звука в ВОЛНовый файл.</span><span class="sxs-lookup"><span data-stu-id="9dc62-142">This tutorial shows how to use the Source Reader to decode audio from a media file and write the audio to a WAVE file.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9dc62-143">См. также</span><span class="sxs-lookup"><span data-stu-id="9dc62-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dc62-144">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9dc62-144">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="9dc62-145">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="9dc62-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="9dc62-146">**имфсаурцереадер**</span><span class="sxs-lookup"><span data-stu-id="9dc62-146">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




