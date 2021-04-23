---
title: Чтение потоков с неквадратными пикселями
description: Чтение потоков с неквадратными пикселями
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Пакет SDK для Windows Media Format, чтение видеопотоков
- Windows Media Format SDK, потоки видео
- Пакет SDK для формата Windows Media, а не квадратные Пиксели
- Windows Media Format SDK, Пиксели (не квадратные)
- Расширенный формат систем (ASF), чтение видеопотоков
- ASF (Расширенный системный формат), чтение видеопотоков
- Расширенный системный формат (ASF), видеопотоки
- ASF (Расширенный системный формат), видеопотоки
- Расширенный формат систем (ASF), а не квадратные Пиксели
- ASF (Расширенный системный формат), неквадратные Пиксели
- Расширенный формат систем (ASF), пикселей (не квадратный)
- ASF (Расширенный системный формат), Пиксели (не квадратный)
- чтение видеопотоков
- потоки видео, чтение
- видеопотоки, не квадратные Пиксели
- неквадратные Пиксели
- Пиксели (не квадратные)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700725"
---
# <a name="reading-streams-with-non-square-pixels"></a><span data-ttu-id="6d3e7-120">Чтение потоков с неквадратными пикселями</span><span class="sxs-lookup"><span data-stu-id="6d3e7-120">Reading Streams with Non-Square Pixels</span></span>

<span data-ttu-id="6d3e7-121">Приложения для чтения, которым необходимо правильно обменять неквадратные Пиксели, должны проверять атрибуты уровня потока в заголовке ASF и расширения модулей данных в каждом примере.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-121">Reader applications that need to correctly handle non-square pixels should examine both the stream-level attributes in the ASF header and the data unit extensions on each sample.</span></span> <span data-ttu-id="6d3e7-122">Существует два варианта, когда выходной прямоугольник должен быть скорректирован для компенсации неквадратных пикселей.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-122">There are two cases when the output rectangle must be adjusted to compensate for non-square pixels.</span></span>

<span data-ttu-id="6d3e7-123">Когда исходное содержимое было захвачено с устройства, например с помощью цифровой видеокамеры с неквадратными пикселями в его ККД, приложение-считыватель должно изменить его прямоугольник вывода, чтобы изображение правильно отображалось на мониторе компьютера с квадратными пикселями.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-123">When the source content has been captured from a device such as a DV (digital video) camera with non-square pixels in its CCD, a reader application must adjust its video output rectangle so that the image displays correctly on a computer monitor with square pixels.</span></span>

<span data-ttu-id="6d3e7-124">Когда приложение для чтения выводит видео, которое будет воспроизводиться на телевизоре NTSC, например через подключение S-Video на видеоадаптере, необходимо настроить прямоугольник видео таким образом, чтобы изображение правильно отображалось на неквадратных пикселях телевизора.</span><span class="sxs-lookup"><span data-stu-id="6d3e7-124">When your reader application outputs video that will be played back on an NTSC television, for example through an S-Video out connection on the video card, you must adjust the video rectangle so that the image displays correctly on the television's non-square pixels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d3e7-125">См. также</span><span class="sxs-lookup"><span data-stu-id="6d3e7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d3e7-126">**Чтение и запись видеопотоков с неквадратными пикселями**</span><span class="sxs-lookup"><span data-stu-id="6d3e7-126">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




