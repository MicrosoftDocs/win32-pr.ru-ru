---
title: Карты ключей
description: Карты ключей
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- Цифровой интерфейс MIDI, сопоставитель MIDI
- MIDI (цифровой интерфейс музыкального инструмента), сопоставитель MIDI
- Сопоставитель MIDI, карты ключей
- карты ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986327"
---
# <a name="key-maps"></a><span data-ttu-id="caa56-107">Карты ключей</span><span class="sxs-lookup"><span data-stu-id="caa56-107">Key Maps</span></span>

<span data-ttu-id="caa56-108">Каждая запись в таблице преобразования с картой исправлений может иметь связанную карту ключей.</span><span class="sxs-lookup"><span data-stu-id="caa56-108">Each entry in the patch-map translation table can have an associated key map.</span></span> <span data-ttu-id="caa56-109">Карты ключей влияют на сообщения о заметках, заметок и полифоник-Key-афтертауч.</span><span class="sxs-lookup"><span data-stu-id="caa56-109">Key maps affect note-on, note-off, and polyphonic-key-aftertouch messages.</span></span> <span data-ttu-id="caa56-110">В карте ключей имеется таблица перевода с записью для каждого значения ключа MIDI 128.</span><span class="sxs-lookup"><span data-stu-id="caa56-110">A key map has a translation table with an entry for each of the 128 MIDI key values.</span></span> <span data-ttu-id="caa56-111">Например, если запись для значения ключа 60 имеет значение 72, средство сопоставления MIDI изменяет сообщения в формате MIDI, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="caa56-111">For example, if the entry for key value 60 is 72, the MIDI Mapper modifies MIDI note-on messages as shown in the following illustration.</span></span>

![изображение сопоставителя MIDI](images/mmap-a06.gif)

<span data-ttu-id="caa56-113">Карты ключей полезны для синтезаторов, имеющих на основе ключей инструменты, имеющие определенный звук, назначенный каждому ключу.</span><span class="sxs-lookup"><span data-stu-id="caa56-113">Key maps are useful with synthesizers that have key-based percussion instruments with a particular percussion sound assigned to each key.</span></span> <span data-ttu-id="caa56-114">Карты ключей обычно назначаются первому исправлению в картах исправлений на каналах с помощью последствий (10 и 16).</span><span class="sxs-lookup"><span data-stu-id="caa56-114">Key maps are usually assigned to the first patch in the patch maps on the percussion channels (10 and 16).</span></span>

 

 




