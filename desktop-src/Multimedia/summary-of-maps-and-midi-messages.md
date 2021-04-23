---
title: Сводка по картам и сообщениям MIDI
description: Сводка по картам и сообщениям MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- Цифровой интерфейс MIDI, сопоставитель MIDI
- MIDI (цифровой интерфейс музыкального инструмента), сопоставитель MIDI
- Сопоставитель MIDI, сопоставление каналов
- Сопоставитель MIDI, карты исправлений
- Сопоставитель MIDI, карты ключей
- Схема канала
- карты исправлений
- карты ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778839"
---
# <a name="summary-of-maps-and-midi-messages"></a><span data-ttu-id="f432e-111">Сводка по картам и сообщениям MIDI</span><span class="sxs-lookup"><span data-stu-id="f432e-111">Summary of Maps and MIDI Messages</span></span>

<span data-ttu-id="f432e-112">Ниже приведены байты состояния для сообщений MIDI и типы карт, влияющие на каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="f432e-112">Following are the status bytes for MIDI messages and the map types that affect each message.</span></span>



| <span data-ttu-id="f432e-113">Состояние MIDI</span><span class="sxs-lookup"><span data-stu-id="f432e-113">MIDI status</span></span> | <span data-ttu-id="f432e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f432e-114">Description</span></span>               | <span data-ttu-id="f432e-115">Типы карт</span><span class="sxs-lookup"><span data-stu-id="f432e-115">Map types</span></span>                |
|-------------|---------------------------|--------------------------|
| <span data-ttu-id="f432e-116">0x80-0x8F</span><span class="sxs-lookup"><span data-stu-id="f432e-116">0x80-0x8F</span></span>   | <span data-ttu-id="f432e-117">Заметка отключена</span><span class="sxs-lookup"><span data-stu-id="f432e-117">Note off</span></span>                  | <span data-ttu-id="f432e-118">Карты каналов, карты ключей</span><span class="sxs-lookup"><span data-stu-id="f432e-118">Channel maps, key maps</span></span>   |
| <span data-ttu-id="f432e-119">0x90-0x9F</span><span class="sxs-lookup"><span data-stu-id="f432e-119">0x90-0x9F</span></span>   | <span data-ttu-id="f432e-120">Примечания по </span><span class="sxs-lookup"><span data-stu-id="f432e-120">Note on</span></span>                   | <span data-ttu-id="f432e-121">Карты каналов, карты ключей</span><span class="sxs-lookup"><span data-stu-id="f432e-121">Channel maps, key maps</span></span>   |
| <span data-ttu-id="f432e-122">0X82 — 0xAF</span><span class="sxs-lookup"><span data-stu-id="f432e-122">0xA0-0xAF</span></span>   | <span data-ttu-id="f432e-123">Полифоник — ключ афтертауч</span><span class="sxs-lookup"><span data-stu-id="f432e-123">Polyphonic-key aftertouch</span></span> | <span data-ttu-id="f432e-124">Карты каналов, карты ключей</span><span class="sxs-lookup"><span data-stu-id="f432e-124">Channel maps, key maps</span></span>   |
| <span data-ttu-id="f432e-125">0xB0-0xBF</span><span class="sxs-lookup"><span data-stu-id="f432e-125">0xB0-0xBF</span></span>   | <span data-ttu-id="f432e-126">Изменение элемента управления</span><span class="sxs-lookup"><span data-stu-id="f432e-126">Control change</span></span>            | <span data-ttu-id="f432e-127">Карты каналов, карты исправлений</span><span class="sxs-lookup"><span data-stu-id="f432e-127">Channel maps, patch maps</span></span> |
| <span data-ttu-id="f432e-128">0xC0-0xCF</span><span class="sxs-lookup"><span data-stu-id="f432e-128">0xC0-0xCF</span></span>   | <span data-ttu-id="f432e-129">Изменение программы</span><span class="sxs-lookup"><span data-stu-id="f432e-129">Program change</span></span>            | <span data-ttu-id="f432e-130">Карты каналов, карты исправлений</span><span class="sxs-lookup"><span data-stu-id="f432e-130">Channel maps, patch maps</span></span> |
| <span data-ttu-id="f432e-131">0xD0 — 0xDF</span><span class="sxs-lookup"><span data-stu-id="f432e-131">0xD0-0xDF</span></span>   | <span data-ttu-id="f432e-132">Канал афтертауч</span><span class="sxs-lookup"><span data-stu-id="f432e-132">Channel aftertouch</span></span>        | <span data-ttu-id="f432e-133">Карты каналов</span><span class="sxs-lookup"><span data-stu-id="f432e-133">Channel maps</span></span>             |
| <span data-ttu-id="f432e-134">0xE0 — 0xEF</span><span class="sxs-lookup"><span data-stu-id="f432e-134">0xE0-0xEF</span></span>   | <span data-ttu-id="f432e-135">Шаг — изменение изгиба</span><span class="sxs-lookup"><span data-stu-id="f432e-135">Pitch-bend change</span></span>         | <span data-ttu-id="f432e-136">Карты каналов</span><span class="sxs-lookup"><span data-stu-id="f432e-136">Channel maps</span></span>             |
| <span data-ttu-id="f432e-137">0xF0 — 0xFF</span><span class="sxs-lookup"><span data-stu-id="f432e-137">0xF0-0xFF</span></span>   | <span data-ttu-id="f432e-138">Система</span><span class="sxs-lookup"><span data-stu-id="f432e-138">System</span></span>                    | <span data-ttu-id="f432e-139">Не сопоставлена</span><span class="sxs-lookup"><span data-stu-id="f432e-139">Not mapped</span></span>               |



 

-   <span data-ttu-id="f432e-140">Старшие четыре бита представляют значение состояния.</span><span class="sxs-lookup"><span data-stu-id="f432e-140">The high-order four bits represent the status value.</span></span> <span data-ttu-id="f432e-141">Младшие четыре бита представляют сведения о канале.</span><span class="sxs-lookup"><span data-stu-id="f432e-141">The low-order four bits represent the channel information.</span></span>
-   <span data-ttu-id="f432e-142">Карты исправлений влияют только на контроллер 7 (основной том).</span><span class="sxs-lookup"><span data-stu-id="f432e-142">Patch maps affect only controller 7 (main volume).</span></span>
-   <span data-ttu-id="f432e-143">Системные сообщения отправляются на все устройства, перечисленные в карте каналов.</span><span class="sxs-lookup"><span data-stu-id="f432e-143">System messages are sent to all devices listed in a channel map.</span></span>

 

 




