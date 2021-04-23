---
title: Карты исправлений
description: Карты исправлений
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- Цифровой интерфейс MIDI, сопоставитель MIDI
- MIDI (цифровой интерфейс музыкального инструмента), сопоставитель MIDI
- Сопоставитель MIDI, карты исправлений
- карты исправлений
- Программа MIDI — сообщения о изменениях
- Сообщения о том, как устройство MIDI
- сообщения изменения программы
- сообщения корпоративного контроллера
- Средство сопоставления MIDI, сообщения о изменениях программы
- Сопоставитель MIDI, сообщения корпоративного контроллера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329619"
---
# <a name="patch-maps"></a><span data-ttu-id="bac46-113">Карты исправлений</span><span class="sxs-lookup"><span data-stu-id="bac46-113">Patch Maps</span></span>

<span data-ttu-id="bac46-114">Каждая запись сопоставления каналов может иметь связанную карту исправлений.</span><span class="sxs-lookup"><span data-stu-id="bac46-114">Each channel map entry can have an associated patch map.</span></span> <span data-ttu-id="bac46-115">Карты исправлений влияют на программу MIDI, изменение и сообщения корпоративного контроллера.</span><span class="sxs-lookup"><span data-stu-id="bac46-115">Patch maps affect MIDI program-change and volume-controller messages.</span></span> <span data-ttu-id="bac46-116">Сообщения об изменениях в программе сообщают синтезатору изменить звук инструмента (исправление) для указанного канала.</span><span class="sxs-lookup"><span data-stu-id="bac46-116">Program-change messages tell a synthesizer to change the instrument sound (patch) for a specified channel.</span></span> <span data-ttu-id="bac46-117">В сообщениях корпоративного контроллера задается том для канала.</span><span class="sxs-lookup"><span data-stu-id="bac46-117">Volume-controller messages set the volume for a channel.</span></span>

<span data-ttu-id="bac46-118">На карте исправлений имеется таблица перевода с записью для каждого значения изменения программы 128.</span><span class="sxs-lookup"><span data-stu-id="bac46-118">A patch map has a translation table with an entry for each of the 128 program-change values.</span></span> <span data-ttu-id="bac46-119">Каждая схема исправлений определяет следующее:</span><span class="sxs-lookup"><span data-stu-id="bac46-119">Each patch map specifies the following:</span></span>

-   <span data-ttu-id="bac46-120">Значение изменения целевой программы.</span><span class="sxs-lookup"><span data-stu-id="bac46-120">A destination program-change value.</span></span>
-   <span data-ttu-id="bac46-121">Скалярный том.</span><span class="sxs-lookup"><span data-stu-id="bac46-121">A volume scalar.</span></span> <span data-ttu-id="bac46-122">(Дополнительные сведения см. [в разделе "скалярность тома](the-volume-scalar.md)".)</span><span class="sxs-lookup"><span data-stu-id="bac46-122">(For more information, see [The Volume Scalar](the-volume-scalar.md).)</span></span>
-   <span data-ttu-id="bac46-123">Необязательная схема ключей.</span><span class="sxs-lookup"><span data-stu-id="bac46-123">An optional key map.</span></span> <span data-ttu-id="bac46-124">(Дополнительные сведения см. в разделе [сопоставления ключей](key-maps.md).)</span><span class="sxs-lookup"><span data-stu-id="bac46-124">(For more information, see [Key Maps](key-maps.md).)</span></span>

<span data-ttu-id="bac46-125">Когда средство сопоставления MIDI получает сообщения об изменении программы, оно заменяется на значение изменения программы в сообщении.</span><span class="sxs-lookup"><span data-stu-id="bac46-125">When program-change messages are received by the MIDI Mapper, the destination program-change value is substituted for the program-change value in the message.</span></span> <span data-ttu-id="bac46-126">Например, если значение изменения программы назначения для программы-Change 16 равно 18, средство сопоставления MIDI изменяет сообщение программы MIDI, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="bac46-126">For example, if the destination program-change value for program-change 16 is 18, the MIDI Mapper modifies the MIDI program-change message as shown in the following illustration.</span></span>

![изображение сопоставителя MIDI](images/mmap-a03.gif)

 

 




