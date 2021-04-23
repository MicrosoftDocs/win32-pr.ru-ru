---
title: Службы MIDI
description: Службы MIDI
ms.assetid: 884066c2-6927-4f5b-902b-8baef9a4a0d7
keywords:
- Мультимедиа Windows, службы MIDI
- мультимедиа, службы MIDI
- мультимедиа аудио, службы MIDI
- аудио, службы MIDI
- Цифровой интерфейс MIDI, службы MIDI
- MIDI (цифровой интерфейс музыкального инструмента), службы MIDI
- Службы MIDI, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc412ddec21245e9682a2a2e79e3f8031d2a6918
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412907"
---
# <a name="midi-services"></a><span data-ttu-id="d9265-110">Службы MIDI</span><span class="sxs-lookup"><span data-stu-id="d9265-110">MIDI Services</span></span>

<span data-ttu-id="d9265-111">Большинство приложений смогут использовать секвенсор MIDI MCI или буферы потока (и функцию [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ) для реализации всех необходимых функций MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9265-111">Most applications will be able to use the MCI MIDI sequencer or stream buffers (and the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function) to implement all the MIDI functionality they need.</span></span> <span data-ttu-id="d9265-112">Серьезные разработчики MIDI, которые создают средства создания и виртуализации MIDI, могут использовать сочетание возможностей потока и службы MIDI или использовать только службы MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9265-112">Serious MIDI developers — those producing MIDI authoring or sequencing tools — can use either a combination of the stream capabilities and the MIDI services or use only the MIDI services.</span></span> <span data-ttu-id="d9265-113">В следующих разделах приводятся общие сведения об использовании служб MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9265-113">The following topics provides general information about using the MIDI services.</span></span>

-   [<span data-ttu-id="d9265-114">Запрос устройств MIDI</span><span class="sxs-lookup"><span data-stu-id="d9265-114">Querying MIDI Devices</span></span>](querying-midi-devices.md)
-   [<span data-ttu-id="d9265-115">Открытие и закрытие драйверов устройств</span><span class="sxs-lookup"><span data-stu-id="d9265-115">Opening and Closing Device Drivers</span></span>](opening-and-closing-device-drivers.md)
-   [<span data-ttu-id="d9265-116">Выделение и подготовка блоков данных MIDI</span><span class="sxs-lookup"><span data-stu-id="d9265-116">Allocating and Preparing MIDI Data Blocks</span></span>](allocating-and-preparing-midi-data-blocks.md)
-   [<span data-ttu-id="d9265-117">Управление блоками данных MIDI</span><span class="sxs-lookup"><span data-stu-id="d9265-117">Managing MIDI Data Blocks</span></span>](managing-midi-data-blocks.md)
-   [<span data-ttu-id="d9265-118">Запрос форматов времени</span><span class="sxs-lookup"><span data-stu-id="d9265-118">Requesting Time Formats</span></span>](requesting-time-formats.md)
-   [<span data-ttu-id="d9265-119">Обработка ошибок с помощью функций MIDI</span><span class="sxs-lookup"><span data-stu-id="d9265-119">Handling Errors with MIDI Functions</span></span>](handling-errors-with-midi-functions.md)

 

 