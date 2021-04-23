---
title: Изменение внутреннего тома MIDI синтезатор
description: Изменение внутреннего тома MIDI синтезатор
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), внутренние синтезаторы
- MIDI (цифровой интерфейс музыкального инструмента), внутренние синтезаторы
- Воспроизведение файлов MIDI, внутренних синтезаторов
- внутренние синтезаторы MIDI
- Цифровой интерфейс MIDI, изменение тома
- MIDI (цифровой интерфейс музыкального инструмента), изменение тома
- Воспроизведение файлов MIDI, изменение тома
- изменение громкости MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987480"
---
# <a name="changing-internal-midi-synthesizer-volume"></a><span data-ttu-id="1a861-111">Изменение внутреннего тома MIDI синтезатор</span><span class="sxs-lookup"><span data-stu-id="1a861-111">Changing Internal MIDI Synthesizer Volume</span></span>

<span data-ttu-id="1a861-112">Windows предоставляет следующие функции для получения и установки уровня громкости внутренних устройств MIDI синтезатора:</span><span class="sxs-lookup"><span data-stu-id="1a861-112">Windows provides the following functions to retrieve and set the volume level of internal MIDI synthesizer devices:</span></span>



| <span data-ttu-id="1a861-113">Значение</span><span class="sxs-lookup"><span data-stu-id="1a861-113">Value</span></span>                                        | <span data-ttu-id="1a861-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1a861-114">Meaning</span></span>                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="1a861-115">**мидиаутжетволуме**</span><span class="sxs-lookup"><span data-stu-id="1a861-115">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | <span data-ttu-id="1a861-116">Извлекает уровень громкости указанного внутреннего устройства MIDI синтезатора.</span><span class="sxs-lookup"><span data-stu-id="1a861-116">Retrieves the volume level of the specified internal MIDI synthesizer device.</span></span> |
| [<span data-ttu-id="1a861-117">**мидиаутсетволуме**</span><span class="sxs-lookup"><span data-stu-id="1a861-117">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | <span data-ttu-id="1a861-118">Задает уровень громкости указанного внутреннего устройства MIDI синтезатора.</span><span class="sxs-lookup"><span data-stu-id="1a861-118">Sets the volume level of the specified internal MIDI synthesizer device.</span></span>      |



 

<span data-ttu-id="1a861-119">Не все выходные устройства MIDI поддерживают изменения томов.</span><span class="sxs-lookup"><span data-stu-id="1a861-119">Not all MIDI output devices support volume changes.</span></span> <span data-ttu-id="1a861-120">Некоторые устройства могут поддерживать отдельные изменения томов как в левом, так и в правой канале.</span><span class="sxs-lookup"><span data-stu-id="1a861-120">Some devices can support individual volume changes on both the left and right channels.</span></span> <span data-ttu-id="1a861-121">Сведения о том, как определить, поддерживает ли определенное устройство изменение тома, см. в разделе [запросы к выходным устройствам MIDI](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="1a861-121">For information on how to determine if a particular device supports volume changes, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

<span data-ttu-id="1a861-122">Если приложение не предназначено для работы с главным приложением управления томами (предоставляет пользователю регулятор громкости для всех аудиоустройств в системе), перед изменением тома следует открыть звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="1a861-122">Unless your application is designed to be a master volume-control application (provides the user with volume control for all audio devices in a system), you should open an audio device before changing its volume.</span></span> <span data-ttu-id="1a861-123">Необходимо также проверить уровень громкости перед его изменением и восстановить предыдущий уровень громкости как можно скорее.</span><span class="sxs-lookup"><span data-stu-id="1a861-123">You should also check the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="1a861-124">Том указан как значение даублеворд.</span><span class="sxs-lookup"><span data-stu-id="1a861-124">Volume is specified as a doubleword value.</span></span> <span data-ttu-id="1a861-125">Верхние 16 битов указывают относительный объем правого канала, а младшие 16 бит указывают относительный объем левого канала.</span><span class="sxs-lookup"><span data-stu-id="1a861-125">The upper 16 bits specify the relative volume of the right channel, and the lower 16 bits specify the relative volume of the left channel.</span></span>

<span data-ttu-id="1a861-126">Для устройств, которые не поддерживают отдельные изменения томов как в левом, так и в правом каналах, младшие 16 бит указывают уровень громкости, а верхние 16 бит игнорируются.</span><span class="sxs-lookup"><span data-stu-id="1a861-126">For devices that do not support individual volume changes on both the left and right channels, the lower 16 bits specify the volume level and the upper 16 bits are ignored.</span></span> <span data-ttu-id="1a861-127">Значения для диапазона уровня тома от 0x0 (тишина) до 0xFFFF (максимальный том) и интерпретируемы как пропорциональны логарифму.</span><span class="sxs-lookup"><span data-stu-id="1a861-127">Values for the volume level range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="1a861-128">Воспринимаемое увеличение громкости при увеличении уровня громкости с 0x5000 до 0x6000 не отличается от 0x4000 до 0x5000.</span><span class="sxs-lookup"><span data-stu-id="1a861-128">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 