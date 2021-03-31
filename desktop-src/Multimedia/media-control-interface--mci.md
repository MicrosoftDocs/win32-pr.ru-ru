---
title: Интерфейс управления мультимедиа (MCI)
description: Интерфейс управления мультимедиа (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Мультимедиа Windows, интерфейс управления мультимедиа (MCI)
- мультимедиа, интерфейс управления мультимедиа (MCI)
- мультимедийный звук, интерфейс управления мультимедиа (MCI)
- аудио, интерфейс управления мультимедиа (MCI)
- Цифровой интерфейс MIDI, интерфейс управления мультимедиа (MCI)
- MIDI (цифровой интерфейс музыкального инструмента), интерфейс управления мультимедиа (MCI)
- Интерфейс управления мультимедиа (MCI), цифровой интерфейс музыкального инструмента (MIDI)
- MCI (интерфейс управления мультимедийными файлами), цифровой интерфейс музыкальных инструментов (MIDI)
- Интерфейс управления мультимедиа (MCI), программа MIDI Sequencer
- MCI (интерфейс управления мультимедиа), программа MIDI Sequencer
- Секвенсор MIDI MCI, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067899"
---
# <a name="media-control-interface-mci"></a><span data-ttu-id="f4ca0-114">Интерфейс управления мультимедиа (MCI)</span><span class="sxs-lookup"><span data-stu-id="f4ca0-114">Media Control Interface (MCI)</span></span>

<span data-ttu-id="f4ca0-115">Секвенсор MIDI MCI — это системный компонент MCI, который воспроизводит файлы MIDI.</span><span class="sxs-lookup"><span data-stu-id="f4ca0-115">The MCI MIDI sequencer is the MCI system component that plays MIDI files.</span></span> <span data-ttu-id="f4ca0-116">Приложения могут легко воспроизводить файлы MIDI с помощью MCI, но MCI накладывает следующие ограничения на возможности MIDI:</span><span class="sxs-lookup"><span data-stu-id="f4ca0-116">Applications can play MIDI files easily using MCI, but MCI imposes the following restrictions on MIDI capabilities:</span></span>

-   <span data-ttu-id="f4ca0-117">MCI поддерживает только выходные данные MIDI.</span><span class="sxs-lookup"><span data-stu-id="f4ca0-117">MCI supports MIDI output only.</span></span>
-   <span data-ttu-id="f4ca0-118">MCI не позволяет закрыть синхронизацию между событиями MIDI и другими событиями в реальном времени (например, видео).</span><span class="sxs-lookup"><span data-stu-id="f4ca0-118">MCI does not allow close synchronization between MIDI events and other real-time events (such as video).</span></span>

<span data-ttu-id="f4ca0-119">Если требуется точная синхронизация MIDI, необходимо использовать буферы потоков или службы MIDI.</span><span class="sxs-lookup"><span data-stu-id="f4ca0-119">If you need accurate MIDI synchronization, you must use the stream buffers or the MIDI services.</span></span> <span data-ttu-id="f4ca0-120">Если требуются возможности ввода MIDI, необходимо использовать службы MIDI.</span><span class="sxs-lookup"><span data-stu-id="f4ca0-120">If you need MIDI input capabilities, you must use the MIDI services.</span></span>

<span data-ttu-id="f4ca0-121">Секвенсор MIDI MCI воспроизводит стандартные файлы MIDI и файлы формата обмена ресурсами (Metallica), известные как файлы RMID.</span><span class="sxs-lookup"><span data-stu-id="f4ca0-121">The MCI MIDI sequencer plays standard MIDI files and resource interchange file format (RIFF) MIDI files, known as RMID files.</span></span> <span data-ttu-id="f4ca0-122">Стандартные файлы MIDI соответствуют [стандартным спецификациям MIDI files 1,0](creating-midi-files.md) .</span><span class="sxs-lookup"><span data-stu-id="f4ca0-122">Standard MIDI files conform to the [Standard MIDI Files 1.0](creating-midi-files.md) specification.</span></span> <span data-ttu-id="f4ca0-123">Так как файлы RMID являются стандартными файлами MIDI с заголовком Metallica, сведения о стандартных файлах MIDI также применяются и к файлам RMID.</span><span class="sxs-lookup"><span data-stu-id="f4ca0-123">Because RMID files are standard MIDI files with a RIFF header, information about standard MIDI files also applies to RMID files.</span></span> <span data-ttu-id="f4ca0-124">Дополнительные сведения о файлах Metallica см. в статье [обмен ресурсами файловый формат служб](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="f4ca0-124">For more information about RIFF files, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

<span data-ttu-id="f4ca0-125">Хотя в настоящее время существует три вида стандартных файлов MIDI, секвенсор MCI воспроизводит только два из них: Format 0 и Format 1 MIDI Files.</span><span class="sxs-lookup"><span data-stu-id="f4ca0-125">Although there are currently three kinds of standard MIDI files, the MCI sequencer plays only two of them: Format 0 and Format 1 MIDI files.</span></span>

<span data-ttu-id="f4ca0-126">Дополнительные сведения об управлении устройствами мультимедиа (включая средства виртуализации) с помощью команд MCI см. в разделе [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="f4ca0-126">For more information about controlling multimedia devices (including sequencers) using MCI commands, see [MCI](mci.md).</span></span>

 

 




