---
title: Чтение и запись видеопотоков с неквадратными пикселями
description: Чтение и запись видеопотоков с неквадратными пикселями
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- Пакет SDK для Windows Media Format, чтение видеопотоков
- Windows Media Format SDK, написание видеопотоков
- Windows Media Format SDK, потоки видео
- Пакет SDK для формата Windows Media, а не квадратные Пиксели
- Windows Media Format SDK, Пиксели (не квадратные)
- Расширенный формат систем (ASF), чтение видеопотоков
- ASF (Расширенный системный формат), чтение видеопотоков
- Расширенный системный формат (ASF), написание видеопотоков
- ASF (Расширенный системный формат), написание видеопотоков
- Расширенный системный формат (ASF), видеопотоки
- ASF (Расширенный системный формат), видеопотоки
- Расширенный формат систем (ASF), а не квадратные Пиксели
- ASF (Расширенный системный формат), неквадратные Пиксели
- Расширенный формат систем (ASF), пикселей (не квадратный)
- ASF (Расширенный системный формат), Пиксели (не квадратный)
- чтение видеопотоков
- Написание видеопотоков
- потоки видео, чтение
- видеопотоки, запись
- видеопотоки, не квадратные Пиксели
- неквадратные Пиксели
- Пиксели (не квадратные)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6b3e3ba67ba42dfc144e7f95ddd042dea0f84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329771"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a><span data-ttu-id="24a36-125">Чтение и запись видеопотоков с неквадратными пикселями</span><span class="sxs-lookup"><span data-stu-id="24a36-125">To Read and Write Video Streams with Non-Square Pixels</span></span>

<span data-ttu-id="24a36-126">Мониторы компьютеров имеют квадратные пиксели, но другие типы экранов видео, включая телевизоры NTSC, имеют прямоугольные или неквадратные Пиксели.</span><span class="sxs-lookup"><span data-stu-id="24a36-126">Computer monitors have square pixels, but other types of video screens, including NTSC televisions, have rectangular or non-square pixels.</span></span> <span data-ttu-id="24a36-127">Кроме того, некоторые устройства ввода, такие как цифровые камеры (DV), настроили несколько устройств с неквадратными пикселями.</span><span class="sxs-lookup"><span data-stu-id="24a36-127">Also, some input devices, such as Digital Video (DV) cameras, have charged couple devices with non-square pixels.</span></span> <span data-ttu-id="24a36-128">При записи файлов, которые основаны на неквадратных пикселях источника, или в других целях, предназначенных для показа на устройствах с неквадратными пикселями, в файл ASF должны быть включены сведения о пропорции пикселей.</span><span class="sxs-lookup"><span data-stu-id="24a36-128">When you are writing files that are either based on non-square pixel source data or else intended for display on devices with non-square pixels, the pixel aspect ratio information must be included in the ASF file.</span></span> <span data-ttu-id="24a36-129">Приложения Reader должны изучить эту информацию и использовать ее для настройки пропорций видеопрямоугольника по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="24a36-129">Reader applications must examine that information and use it to adjust the aspect ratio of the video rectangle as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24a36-130">См. также</span><span class="sxs-lookup"><span data-stu-id="24a36-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24a36-131">**Дополнительные разделы**</span><span class="sxs-lookup"><span data-stu-id="24a36-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="24a36-132">**Чтение потоков с неквадратными пикселями**</span><span class="sxs-lookup"><span data-stu-id="24a36-132">**Reading Streams with Non-Square Pixels**</span></span>](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[<span data-ttu-id="24a36-133">**Запись потоков с неквадратными пикселями**</span><span class="sxs-lookup"><span data-stu-id="24a36-133">**Writing Streams with Non-Square Pixels**</span></span>](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




