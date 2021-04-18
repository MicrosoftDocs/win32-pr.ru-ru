---
title: Получение наилучшей производительности поиска видео
description: Получение наилучшей производительности поиска видео
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media Format SDK, лучшее качество поиска видео
- Улучшенный системный формат (ASF), лучшее качество поиска видео
- ASF (Расширенный системный формат), лучшее качество поиска видео
- Расширенный системный формат (ASF), производительность поиска видео
- ASF (Расширенный системный формат), производительность поиска видео
- Расширенный системный формат (ASF), производительность
- ASF (Расширенный системный формат), производительность
- Поиск видео
- производительность, Поиск видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691288"
---
# <a name="getting-the-best-video-seeking-performance"></a><span data-ttu-id="48969-112">Получение наилучшей производительности поиска видео</span><span class="sxs-lookup"><span data-stu-id="48969-112">Getting the Best Video Seeking Performance</span></span>

<span data-ttu-id="48969-113">Поиск содержимого в файле является очень распространенной операцией, которая может вызвать проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="48969-113">Seeking to content in a file is a very common operation that is potentially a performance issue.</span></span> <span data-ttu-id="48969-114">Видео, закодированное с помощью кодека Windows Media Video 9, состоит в основном из разностных кадров, которые записывают только изменения, связанные с предыдущим кадром.</span><span class="sxs-lookup"><span data-stu-id="48969-114">Video encoded with the Windows Media Video 9 codec is made up primarily of delta frames, which only record the changes in relation to the previous frame.</span></span> <span data-ttu-id="48969-115">Восстановление разностных кадров занимает некоторое время, особенно если ключевые кадры находятся далеко друг от друга.</span><span class="sxs-lookup"><span data-stu-id="48969-115">Reconstructing delta frames takes time, particularly if the key frames are far apart.</span></span> <span data-ttu-id="48969-116">Дополнительные сведения о настройке ключевых кадров для эффективного поиска см. в разделе [Настройка потоков видео для поиска производительности](configuring-video-streams-for-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="48969-116">For more information about configuring key frames for efficient seeking, see [Configuring Video Streams for Seeking Performance](configuring-video-streams-for-seeking-performance.md).</span></span>

<span data-ttu-id="48969-117">Помимо правильной настройки можно повысить производительность при использовании индексирования кадров для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="48969-117">In addition to proper configuration, you can improve seeking performance by using frame indexing for the video stream.</span></span> <span data-ttu-id="48969-118">Поиск по номеру кадра обычно выполняется быстрее, чем при поиске во время презентации.</span><span class="sxs-lookup"><span data-stu-id="48969-118">Seeking to a frame number is typically faster than seeking to a presentation time.</span></span>

<span data-ttu-id="48969-119">При поиске в файле с несколькими потоками следует выбирать только нужные потоки.</span><span class="sxs-lookup"><span data-stu-id="48969-119">If seeking in a file with multiple streams, you should select only the streams that are needed.</span></span> <span data-ttu-id="48969-120">Каждый поток, настроенный для чтения, влияет на производительность поиска, так как все выбранные потоки синхронизируются при поиске в точке файла.</span><span class="sxs-lookup"><span data-stu-id="48969-120">Each stream configured for reading will affect the performance of seeking, because all selected streams are synchronized when you seek to a point in a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48969-121">См. также</span><span class="sxs-lookup"><span data-stu-id="48969-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48969-122">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="48969-122">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="48969-123">**Поиск по номеру кадра с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="48969-123">**To Seek By Frame Number Using the Asynchronous Reader**</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="48969-124">**Поиск по номеру кадра с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="48969-124">**To Seek By Frame Number Using the Synchronous Reader**</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="48969-125">**Поиск по времени с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="48969-125">**To Seek By Time Using the Asynchronous Reader**</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="48969-126">**Поиск по времени с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="48969-126">**To Seek By Time Using the Synchronous Reader**</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




