---
title: О MIDI
description: О MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Мультимедиа Windows, цифровой интерфейс музыкальных инструментов (MIDI)
- мультимедиа, цифровой интерфейс музыкальных инструментов (MIDI)
- мультимедийный звук, цифровой интерфейс музыкальных инструментов (MIDI)
- аудио, цифровой интерфейс музыкальных инструментов (MIDI)
- Цифровой интерфейс музыкальных инструментов (MIDI), о программе
- MIDI (цифровой интерфейс музыкального инструмента), о программе
- Цифровой интерфейс MIDI, интерфейс управления мультимедиа (MCI)
- MIDI (цифровой интерфейс музыкального инструмента), интерфейс управления мультимедиа (MCI)
- Цифровой интерфейс музыкальных инструментов (MIDI), буферы потоков
- MIDI (цифровой интерфейс музыкального инструмента), буферы потоков
- Цифровой интерфейс MIDI, службы MIDI
- MIDI (цифровой интерфейс музыкального инструмента), службы MIDI
- Интерфейс управления мультимедиа (MCI), цифровой интерфейс музыкального инструмента (MIDI)
- MCI (интерфейс управления мультимедийными файлами), цифровой интерфейс музыкальных инструментов (MIDI)
- буферы потоков, сведения
- Службы MIDI, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774462"
---
# <a name="about-midi"></a><span data-ttu-id="dfb27-119">О MIDI</span><span class="sxs-lookup"><span data-stu-id="dfb27-119">About MIDI</span></span>

<span data-ttu-id="dfb27-120">Интерфейс прикладного программирования (API) Microsoft Win32 предоставляет следующие методы для работы с данными MIDI.</span><span class="sxs-lookup"><span data-stu-id="dfb27-120">The Microsoft Win32 application programming interface (API) provides the following methods for applications to work with MIDI data:</span></span>

-   <span data-ttu-id="dfb27-121">Интерфейс управления мультимедиа (MCI).</span><span class="sxs-lookup"><span data-stu-id="dfb27-121">The Media Control Interface (MCI).</span></span> <span data-ttu-id="dfb27-122">Хотя самый простой способ воспроизвести файл MIDI — использовать класс окна МЦивнд, можно также использовать команды MCI, чтобы создать настраиваемый интерфейс для устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="dfb27-122">Although the simplest way to play a MIDI file is to use the MCIWnd window class, you can also use MCI commands to create a customized interface to a MIDI device.</span></span> <span data-ttu-id="dfb27-123">Дополнительные сведения о классе окна МЦивнд см. в разделе [класс окна мЦивнд](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="dfb27-123">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span> <span data-ttu-id="dfb27-124">Дополнительные сведения о MCI см. в разделе [MCI](mci.md)или [Media Control Interface (MCI)](media-control-interface--mci.md).</span><span class="sxs-lookup"><span data-stu-id="dfb27-124">For more information about MCI, see [MCI](mci.md), or [Media Control Interface (MCI)](media-control-interface--mci.md).</span></span>
-   <span data-ttu-id="dfb27-125">[Буферы потока](stream-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="dfb27-125">[Stream Buffers](stream-buffers.md).</span></span> <span data-ttu-id="dfb27-126">Этот формат позволяет приложению управлять буферами данных MIDI с отметкой времени для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="dfb27-126">This format allows an application to manipulate buffers of time-stamped MIDI data for playback.</span></span> <span data-ttu-id="dfb27-127">Буферы потоков удобны для приложений, которым требуется более точный контроль над выходными данными, чем предложения MCI.</span><span class="sxs-lookup"><span data-stu-id="dfb27-127">Stream buffers are useful to applications that require more precise control over output than MCI offers.</span></span>
-   <span data-ttu-id="dfb27-128">[Службы MIDI](midi-services.md).</span><span class="sxs-lookup"><span data-stu-id="dfb27-128">[MIDI Services](midi-services.md).</span></span> <span data-ttu-id="dfb27-129">Приложения, которым требуется наиболее точный контроль данных MIDI, обычно используют эти низкоуровневые службы.</span><span class="sxs-lookup"><span data-stu-id="dfb27-129">Applications that need the most precise control of MIDI data typically use these low-level services.</span></span>

<span data-ttu-id="dfb27-130">В следующих разделах рассматриваются все эти методы и приводится обзор сопоставителя MIDI.</span><span class="sxs-lookup"><span data-stu-id="dfb27-130">The following topics discuss each of these methods and provides an overview of the MIDI Mapper.</span></span>

-   [<span data-ttu-id="dfb27-131">Средство сопоставления MIDI</span><span class="sxs-lookup"><span data-stu-id="dfb27-131">The MIDI Mapper</span></span>](the-midi-mapper.md)
-   [<span data-ttu-id="dfb27-132">Интерфейс управления мультимедиа (MCI)</span><span class="sxs-lookup"><span data-stu-id="dfb27-132">Media Control Interface (MCI)</span></span>](media-control-interface--mci.md)
-   [<span data-ttu-id="dfb27-133">Буферы потока</span><span class="sxs-lookup"><span data-stu-id="dfb27-133">Stream Buffers</span></span>](stream-buffers.md)
-   [<span data-ttu-id="dfb27-134">Службы MIDI</span><span class="sxs-lookup"><span data-stu-id="dfb27-134">MIDI Services</span></span>](midi-services.md)
-   [<span data-ttu-id="dfb27-135">Воспроизведение файлов MIDI</span><span class="sxs-lookup"><span data-stu-id="dfb27-135">Playing MIDI Files</span></span>](playing-midi-files.md)
-   [<span data-ttu-id="dfb27-136">Запись звука MIDI</span><span class="sxs-lookup"><span data-stu-id="dfb27-136">Recording MIDI Audio</span></span>](recording-midi-audio.md)
-   [<span data-ttu-id="dfb27-137">Обработка данных MIDI из двух источников MIDI</span><span class="sxs-lookup"><span data-stu-id="dfb27-137">Processing MIDI Data from Two MIDI Sources</span></span>](processing-midi-data-from-two-midi-sources.md)
-   [<span data-ttu-id="dfb27-138">Создание файлов MIDI</span><span class="sxs-lookup"><span data-stu-id="dfb27-138">Creating MIDI Files</span></span>](creating-midi-files.md)

 

 




