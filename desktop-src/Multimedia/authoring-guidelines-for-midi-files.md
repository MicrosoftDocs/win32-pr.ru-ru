---
title: Рекомендации по созданию файлов MIDI
description: Рекомендации по созданию файлов MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), рекомендации по созданию файлов
- MIDI (цифровой интерфейс музыкального инструмента), рекомендации по созданию файлов
- Создание файлов MIDI, рекомендации по созданию файлов
- назначения исправлений MIDI Standard
- стандартные сочетания клавиш MIDI
- Цифровой интерфейс музыкальных инструментов (MIDI), стандартные исправления
- MIDI (цифровой интерфейс музыкального инструмента), стандартные исправления
- Цифровой интерфейс музыкальных инструментов (MIDI), стандартные сочетания клавиш
- MIDI (цифровой интерфейс музыкального инструмента), стандартные сочетания клавиш
- Создание файлов MIDI, стандартные обновления назначений
- Создание файлов MIDI, стандартные сочетания клавиш
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068531"
---
# <a name="authoring-guidelines-for-midi-files"></a><span data-ttu-id="fbee8-114">Рекомендации по созданию файлов MIDI</span><span class="sxs-lookup"><span data-stu-id="fbee8-114">Authoring Guidelines for MIDI Files</span></span>

<span data-ttu-id="fbee8-115">Следуйте этим рекомендациям, чтобы создать независимые от устройства файлы MIDI для Windows:</span><span class="sxs-lookup"><span data-stu-id="fbee8-115">Follow these guidelines to author device-independent MIDI files for Windows:</span></span>

-   <span data-ttu-id="fbee8-116">Используйте [стандартные назначения ИСПРАВЛЕНИЙ MIDI](standard-midi-patch-assignments.md) и [стандартные назначения клавиш MIDI](standard-midi-key-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="fbee8-116">Use the [Standard MIDI Patch Assignments](standard-midi-patch-assignments.md) and [Standard MIDI Key Assignments](standard-midi-key-assignments.md).</span></span>
-   <span data-ttu-id="fbee8-117">Всегда отправлять сообщение об изменении программы в канал, чтобы выбрать исправление перед отправкой других сообщений в этот канал.</span><span class="sxs-lookup"><span data-stu-id="fbee8-117">Always send a program-change message to a channel to select a patch before sending other messages to that channel.</span></span> <span data-ttu-id="fbee8-118">Для двух каналов с последствиями (10 и 16) выберите программу номер 0.</span><span class="sxs-lookup"><span data-stu-id="fbee8-118">For the two percussion channels (10 and 16), select program number 0.</span></span>
-   <span data-ttu-id="fbee8-119">Всегда следует использовать сообщение об изменении программы MIDI с сообщением о контроллере MIDI Main (номер 7), чтобы задать относительный объем исправления.</span><span class="sxs-lookup"><span data-stu-id="fbee8-119">Always follow a MIDI program-change message with a MIDI main-volume controller message (controller number 7) to set the relative volume of the patch.</span></span>
-   <span data-ttu-id="fbee8-120">Используйте значение 80 (0x50) для контроллера основного тома для обычных уровней прослушивания.</span><span class="sxs-lookup"><span data-stu-id="fbee8-120">Use a value of 80 (0x50) for the main-volume controller for normal listening levels.</span></span> <span data-ttu-id="fbee8-121">Для более низкого или громкого уровня можно использовать более низкие или более высокие значения.</span><span class="sxs-lookup"><span data-stu-id="fbee8-121">For quieter or louder levels, you can use lower or higher values.</span></span>
-   <span data-ttu-id="fbee8-122">Используйте только следующие сообщения MIDI: Примечание. скорость, заметка, изменение программы, наклон изгиба, основной том (контроллер 7) и педали (контроллер 64).</span><span class="sxs-lookup"><span data-stu-id="fbee8-122">Use only the following MIDI messages: note-on with velocity, note-off, program change, pitch bend, main volume (controller 7), and damper pedal (controller 64).</span></span> <span data-ttu-id="fbee8-123">Внутренние синтезаторы должны отвечать на эти сообщения, и большинство музыкальных инструментов MIDI также реагируют на них.</span><span class="sxs-lookup"><span data-stu-id="fbee8-123">Internal synthesizers are required to respond to these messages and most MIDI musical instruments respond to them as well.</span></span>

 

 




