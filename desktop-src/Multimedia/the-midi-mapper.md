---
title: Средство сопоставления MIDI
description: Средство сопоставления MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Мультимедиа Windows, сопоставитель MIDI
- мультимедиа, сопоставитель MIDI
- мультимедиа аудио, сопоставитель MIDI
- аудио, сопоставитель MIDI
- Цифровой интерфейс MIDI, сопоставитель MIDI
- MIDI (цифровой интерфейс музыкального инструмента), сопоставитель MIDI
- Средство сопоставления MIDI, сведения
- Сопоставитель MIDI, источник
- Сопоставитель MIDI, назначение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067800"
---
# <a name="the-midi-mapper"></a><span data-ttu-id="b3e70-112">Средство сопоставления MIDI</span><span class="sxs-lookup"><span data-stu-id="b3e70-112">The MIDI Mapper</span></span>

<span data-ttu-id="b3e70-113">Стандартные службы исправлений MIDI позволяют воспроизводить файлы MIDI, не зависящие от устройства, для приложений.</span><span class="sxs-lookup"><span data-stu-id="b3e70-113">The MIDI Mapper's standard patch services provide device-independent MIDI file playback for applications.</span></span> <span data-ttu-id="b3e70-114">Средство сопоставления MIDI можно использовать с секвенсором MIDI MCI или со службами вывода MIDI низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="b3e70-114">The MIDI Mapper can be used with the MCI MIDI sequencer or with low-level MIDI output services.</span></span>

<span data-ttu-id="b3e70-115">Если не указано иное, все ссылки на номера каналов MIDI используют логические каналы с номерами от 1 до 16.</span><span class="sxs-lookup"><span data-stu-id="b3e70-115">Unless stated otherwise, all references to MIDI channel numbers use the logical channel numbers 1 through 16.</span></span> <span data-ttu-id="b3e70-116">Номера логических каналов соответствуют физическим каналам от 0 до 15, которые фактически являются частью сообщения MIDI.</span><span class="sxs-lookup"><span data-stu-id="b3e70-116">These logical channel numbers correspond to the physical channel numbers 0 through 15 that are actually part of the MIDI message.</span></span> <span data-ttu-id="b3e70-117">Все ссылки на программу MIDI — изменения и значения ключей используют физические значения от 0 до 127.</span><span class="sxs-lookup"><span data-stu-id="b3e70-117">All references to MIDI program-change and key values use the physical values 0 through 127.</span></span> <span data-ttu-id="b3e70-118">Все числа являются десятичными, если не предшествует префикс 0x. в этом случае они являются шестнадцатеричными.</span><span class="sxs-lookup"><span data-stu-id="b3e70-118">All numbers are decimal unless preceded by "0x" prefix, in which case they are hexadecimal.</span></span>

<span data-ttu-id="b3e70-119">В обсуждении средства сопоставления MIDI термин *источник* относится к входной части средства сопоставления MIDI.</span><span class="sxs-lookup"><span data-stu-id="b3e70-119">In the discussion of the MIDI Mapper, the term *source* refers to the input side of the MIDI Mapper.</span></span> <span data-ttu-id="b3e70-120">Термин *назначение* относится к выходной части модуля сопоставления MIDI.</span><span class="sxs-lookup"><span data-stu-id="b3e70-120">The term *destination* refers to the output side of the MIDI Mapper.</span></span> <span data-ttu-id="b3e70-121">Например, исходный канал — это канал MIDI сообщения, отправляемого в сопоставитель MIDI, а Целевой — канал MIDI сообщения, отправленного с сопоставителя MIDI на выходное устройство.</span><span class="sxs-lookup"><span data-stu-id="b3e70-121">For example, a source channel is the MIDI channel of a message sent to the MIDI Mapper, and a destination channel is the MIDI channel of a message sent from the MIDI Mapper to an output device.</span></span>

-   [<span data-ttu-id="b3e70-122">Средство сопоставления MIDI и Windows</span><span class="sxs-lookup"><span data-stu-id="b3e70-122">The MIDI Mapper and Windows</span></span>](the-midi-mapper-and-windows.md)
-   [<span data-ttu-id="b3e70-123">Архитектура сопоставителя MIDI</span><span class="sxs-lookup"><span data-stu-id="b3e70-123">The MIDI Mapper Architecture</span></span>](the-midi-mapper-architecture.md)
-   [<span data-ttu-id="b3e70-124">Схема канала</span><span class="sxs-lookup"><span data-stu-id="b3e70-124">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="b3e70-125">Карты исправлений</span><span class="sxs-lookup"><span data-stu-id="b3e70-125">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="b3e70-126">Скалярный том</span><span class="sxs-lookup"><span data-stu-id="b3e70-126">The Volume Scalar</span></span>](the-volume-scalar.md)
-   [<span data-ttu-id="b3e70-127">Карты ключей</span><span class="sxs-lookup"><span data-stu-id="b3e70-127">Key Maps</span></span>](key-maps.md)
-   [<span data-ttu-id="b3e70-128">Сводка по картам и сообщениям MIDI</span><span class="sxs-lookup"><span data-stu-id="b3e70-128">Summary of Maps and MIDI Messages</span></span>](summary-of-maps-and-midi-messages.md)

 

 




