---
title: Архитектура сопоставителя MIDI
description: Архитектура сопоставителя MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- Цифровой интерфейс MIDI, сопоставитель MIDI
- MIDI (цифровой интерфейс музыкального инструмента), сопоставитель MIDI
- Сопоставитель MIDI, архитектура
- Средство сопоставления MIDI, программа установки
- Схема установки MIDI
- Сопоставитель MIDI, сопоставление каналов
- Сопоставитель MIDI, карты исправлений
- Сопоставитель MIDI, карты ключей
- Схема канала
- карты исправлений
- карты ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331568"
---
# <a name="the-midi-mapper-architecture"></a><span data-ttu-id="c7f47-114">Архитектура сопоставителя MIDI</span><span class="sxs-lookup"><span data-stu-id="c7f47-114">The MIDI Mapper Architecture</span></span>

<span data-ttu-id="c7f47-115">Средство сопоставления MIDI использует карту установки MIDI для определения способа преобразования и перенаправления получаемых сообщений.</span><span class="sxs-lookup"><span data-stu-id="c7f47-115">The MIDI Mapper uses a MIDI setup map to determine how to translate and redirect the messages it receives.</span></span> <span data-ttu-id="c7f47-116">Карта установки MIDI состоит из следующих типов карт.</span><span class="sxs-lookup"><span data-stu-id="c7f47-116">A MIDI setup map consists of the following types of maps.</span></span>

-   [<span data-ttu-id="c7f47-117">Схема канала</span><span class="sxs-lookup"><span data-stu-id="c7f47-117">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="c7f47-118">Карты исправлений</span><span class="sxs-lookup"><span data-stu-id="c7f47-118">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="c7f47-119">Карты ключей</span><span class="sxs-lookup"><span data-stu-id="c7f47-119">Key Maps</span></span>](key-maps.md)

<span data-ttu-id="c7f47-120">На следующем рисунке показаны роли канала, исправления и карты ключей в карте установки MIDI.</span><span class="sxs-lookup"><span data-stu-id="c7f47-120">The following illustration shows the roles of channel, patch, and key maps in a MIDI setup map.</span></span>

![роли карт каналов, исправлений и ключей в образе карты установки MIDI](images/mmap-a02.gif)

 

 




