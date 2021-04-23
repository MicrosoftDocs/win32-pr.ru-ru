---
title: Схема канала
description: Схема канала
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- Цифровой интерфейс MIDI, сопоставитель MIDI
- MIDI (цифровой интерфейс музыкального инструмента), сопоставитель MIDI
- Сопоставитель MIDI, сопоставление каналов
- Схема канала
- Сопоставитель MIDI, сообщения канала
- Сообщения канала MIDI
- сообщения канала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132983"
---
# <a name="the-channel-map"></a><span data-ttu-id="e57a7-110">Схема канала</span><span class="sxs-lookup"><span data-stu-id="e57a7-110">The Channel Map</span></span>

<span data-ttu-id="e57a7-111">Схема канала влияет на все сообщения канала MIDI.</span><span class="sxs-lookup"><span data-stu-id="e57a7-111">The channel map affects all MIDI channel messages.</span></span> <span data-ttu-id="e57a7-112">Сообщения каналов MIDI включают в себя заметку, заметку, полифоник-Key-афтертауч, управление изменениями, программу-изменение, Channel-афтертауч и шаг с изгибом — изменения.</span><span class="sxs-lookup"><span data-stu-id="e57a7-112">MIDI channel messages include note-on, note-off, polyphonic-key-aftertouch, control-change, program-change, channel-aftertouch, and pitch-bend-change messages.</span></span> <span data-ttu-id="e57a7-113">Средство сопоставления MIDI использует одну карту каналов с записью для каждого 16 каналов MIDI.</span><span class="sxs-lookup"><span data-stu-id="e57a7-113">The MIDI Mapper uses a single channel map with an entry for each of the 16 MIDI channels.</span></span> <span data-ttu-id="e57a7-114">Каждая запись схемы канала указывает следующее:</span><span class="sxs-lookup"><span data-stu-id="e57a7-114">Each channel-map entry specifies the following:</span></span>

-   <span data-ttu-id="e57a7-115">Канал назначения для сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="e57a7-115">A destination channel for the MIDI message</span></span>
-   <span data-ttu-id="e57a7-116">Целевое устройство вывода для сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="e57a7-116">A destination output device for the MIDI message</span></span>
-   <span data-ttu-id="e57a7-117">Необязательная схема исправлений с указанием других возможных изменений сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="e57a7-117">An optional patch map specifying other possible modifications for the MIDI message</span></span>

<span data-ttu-id="e57a7-118">Для целевого канала задан один из 16 каналов MIDI.</span><span class="sxs-lookup"><span data-stu-id="e57a7-118">The destination channel is set to one of the 16 MIDI channels.</span></span> <span data-ttu-id="e57a7-119">Сообщения MIDI изменяются для отражения каждого нового назначения канала.</span><span class="sxs-lookup"><span data-stu-id="e57a7-119">MIDI messages are modified to reflect each new channel assignment.</span></span> <span data-ttu-id="e57a7-120">Например, если в записи конечного канала для MIDI Channel 4 задано значение 6, все сообщения MIDI, отправленные на канал 4, будут сопоставлены с каналом 6, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="e57a7-120">For example, if the destination channel entry for MIDI channel 4 is set to 6, all MIDI messages sent to channel 4 will be mapped to channel 6, as shown in the following illustration.</span></span>

![сопоставленный образ MIDI](images/mmap-a05.gif)

<span data-ttu-id="e57a7-122">В этом примере 0x93 байт состояния MIDI сопоставляется с 0x95.</span><span class="sxs-lookup"><span data-stu-id="e57a7-122">In this example, the MIDI status byte 0x93 is mapped to 0x95.</span></span> <span data-ttu-id="e57a7-123">Низкий порядок байтов состояния MIDI указывает номер канала.</span><span class="sxs-lookup"><span data-stu-id="e57a7-123">The low-order of a MIDI status byte specifies the channel number.</span></span> <span data-ttu-id="e57a7-124">Для исходных каналов задано значение активно или неактивно.</span><span class="sxs-lookup"><span data-stu-id="e57a7-124">Source channels are set to either active or inactive.</span></span> <span data-ttu-id="e57a7-125">Сообщения, отправленные в неактивные исходные каналы, игнорируются, поэтому неактивный канал в силе или отключен.</span><span class="sxs-lookup"><span data-stu-id="e57a7-125">Messages sent to inactive source channels are ignored, so an inactive channel is in effect muted or turned off.</span></span>

<span data-ttu-id="e57a7-126">Целевое устройство вывода настроено на одно из доступных выходных устройств MIDI.</span><span class="sxs-lookup"><span data-stu-id="e57a7-126">The destination output device is set to one of the available MIDI output devices.</span></span> <span data-ttu-id="e57a7-127">Устройство вывода MIDI может быть внутренним синтезатором или физическим портом вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="e57a7-127">A MIDI output device can be an internal synthesizer or a physical MIDI output port.</span></span>

<span data-ttu-id="e57a7-128">Системные сообщения MIDI — это сообщения MIDI (с состоянием bytes) от 0xF0 до 0xFF.</span><span class="sxs-lookup"><span data-stu-id="e57a7-128">MIDI system messages are MIDI messages (with status bytes) from 0xF0 to 0xFF.</span></span> <span data-ttu-id="e57a7-129">Нет канала, связанного с системными сообщениями MIDI, поэтому они не могут быть сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="e57a7-129">There is no channel associated with MIDI system messages, so they cannot be mapped.</span></span> <span data-ttu-id="e57a7-130">Системные сообщения MIDI отправляются на все устройства вывода MIDI, перечисленные в карте каналов.</span><span class="sxs-lookup"><span data-stu-id="e57a7-130">MIDI system messages are sent to all MIDI output devices listed in a channel map.</span></span>

 

 




