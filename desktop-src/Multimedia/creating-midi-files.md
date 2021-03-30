---
title: Создание файлов MIDI
description: Создание файлов MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Мультимедиа Windows, создание файлов MIDI
- мультимедиа, создание файлов MIDI
- мультимедийные аудио, создание файлов MIDI
- звук, создание файлов MIDI
- Цифровой интерфейс музыкальных инструментов (MIDI), создание файлов
- MIDI (цифровой интерфейс музыкального инструмента), создание файлов
- Создание файлов MIDI, сведения
- Ассоциация производителей MIDI (MMA)
- MMA (Ассоциация производителей MIDI)
- Подробная спецификация MIDI
- Спецификация стандартных файлов MIDI
- Общая спецификация MIDI (GM)
- Спецификация GM (общая MIDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067694"
---
# <a name="creating-midi-files"></a><span data-ttu-id="07cc9-116">Создание файлов MIDI</span><span class="sxs-lookup"><span data-stu-id="07cc9-116">Creating MIDI Files</span></span>

<span data-ttu-id="07cc9-117">Спецификации цифрового интерфейса музыкальных инструментов публикуются с помощью и являются материалом по сопоставлению производителей MIDI (MMA).</span><span class="sxs-lookup"><span data-stu-id="07cc9-117">The Musical Instrument Digital Interface (MIDI) specifications are published by and are copyrighted material of the MIDI Manufacturers Association (MMA).</span></span> <span data-ttu-id="07cc9-118">В следующем списке перечислены спецификации, которые являются наиболее общими интересами.</span><span class="sxs-lookup"><span data-stu-id="07cc9-118">The following list describes the specifications which are of the greatest general interest:</span></span>

## <a name="midi-detailed-specification"></a><span data-ttu-id="07cc9-119">Подробная спецификация MIDI</span><span class="sxs-lookup"><span data-stu-id="07cc9-119">MIDI Detailed Specification</span></span>

<span data-ttu-id="07cc9-120">В подробной спецификации MIDI описываются аппаратные и программные протоколы MIDI.</span><span class="sxs-lookup"><span data-stu-id="07cc9-120">The MIDI Detailed Specification explains the MIDI hardware and software protocols.</span></span> <span data-ttu-id="07cc9-121">Это полезно для разработки мультимедийных приложений, которые реализуют поддержку MIDI с помощью функций MIDI для записи, редактирования и (или) воспроизведения данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="07cc9-121">This is useful to those developing multimedia applications which implement MIDI support by using MIDI functions to record, edit, and/or play MIDI data.</span></span>

## <a name="standard-midi-files-10"></a><span data-ttu-id="07cc9-122">Стандартные файлы MIDI 1,0</span><span class="sxs-lookup"><span data-stu-id="07cc9-122">Standard MIDI Files 1.0</span></span>

<span data-ttu-id="07cc9-123">Стандартная спецификация файлов MIDI определяет способ обмена данными MIDI с отметкой времени между различными приложениями на одной или разных аппаратных платформах.</span><span class="sxs-lookup"><span data-stu-id="07cc9-123">The Standard MIDI Files specification defines a way to interchange time-stamped MIDI data between different applications on the same or different hardware platforms.</span></span> <span data-ttu-id="07cc9-124">Это полезно для разработчиков, занимающихся написанием приложений, считывающих и анализирующих файлы на дисках, содержащих данные MIDI и (или) записывающих файлы MIDI на диск.</span><span class="sxs-lookup"><span data-stu-id="07cc9-124">This is useful to developers writing applications that read and parse disk files containing MIDI data and/or write MIDI data files to disk.</span></span>

## <a name="general-midi-system---level-1"></a><span data-ttu-id="07cc9-125">Общая система MIDI — уровень 1</span><span class="sxs-lookup"><span data-stu-id="07cc9-125">General MIDI System - Level 1</span></span>

<span data-ttu-id="07cc9-126">Общая спецификация MIDI (GM) определяет минимальную конфигурацию MIDI "общей системы MIDI".</span><span class="sxs-lookup"><span data-stu-id="07cc9-126">The General MIDI (GM) specification defines a minimum MIDI configuration of a "General MIDI System".</span></span> <span data-ttu-id="07cc9-127">Эта система состоит из определенного класса устройств воспроизведения MIDI и представляет интерес для разработчиков мультимедиа, создающих файлы MIDI.</span><span class="sxs-lookup"><span data-stu-id="07cc9-127">This system consists of a specific class of MIDI playback devices and is of interest to multimedia developers who author MIDI files.</span></span> <span data-ttu-id="07cc9-128">Большинство звуковых карт для ПК и синтезаторов MIDI, изготовленных сегодня, совместимы с спецификацией GM.</span><span class="sxs-lookup"><span data-stu-id="07cc9-128">Most PC sound cards and MIDI synthesizers manufactured today are compatible with the GM specification.</span></span> <span data-ttu-id="07cc9-129">Файлы MIDI, созданные в соответствии со спецификацией GM, обычно должны быть звуками, как будто они предназначены для звука, независимо от того, какое устройство совместимо.</span><span class="sxs-lookup"><span data-stu-id="07cc9-129">MIDI files which are authored to the GM specification should generally sound as they were intended to sound, no matter which GM-compatible device they are played on.</span></span>

<span data-ttu-id="07cc9-130">Чтобы позволить файлам MIDI быть приемлемым форматом для представления музыки в мультимедийных вычислениях, Windows следует спецификации общей системы MIDI уровня 1.</span><span class="sxs-lookup"><span data-stu-id="07cc9-130">To enable MIDI files to be a viable format for representing music in multimedia computing, Windows follows the General MIDI System Level 1 specification.</span></span> <span data-ttu-id="07cc9-131">В следующих разделах приводятся дополнительные рекомендации по созданию MIDI:</span><span class="sxs-lookup"><span data-stu-id="07cc9-131">The following topics provide additional MIDI authoring guidelines:</span></span>

-   [<span data-ttu-id="07cc9-132">Рекомендации по созданию файлов MIDI</span><span class="sxs-lookup"><span data-stu-id="07cc9-132">Authoring Guidelines for MIDI Files</span></span>](authoring-guidelines-for-midi-files.md)
-   [<span data-ttu-id="07cc9-133">Назначения исправлений MIDI Standard</span><span class="sxs-lookup"><span data-stu-id="07cc9-133">Standard MIDI Patch Assignments</span></span>](standard-midi-patch-assignments.md)
-   [<span data-ttu-id="07cc9-134">Стандартные сочетания клавиш MIDI</span><span class="sxs-lookup"><span data-stu-id="07cc9-134">Standard MIDI Key Assignments</span></span>](standard-midi-key-assignments.md)

 

 




