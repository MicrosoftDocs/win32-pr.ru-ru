---
title: Отправка отдельных сообщений MIDI
description: Отправка отдельных сообщений MIDI
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), отправка сообщений
- MIDI (цифровой интерфейс музыкального инструмента), отправка сообщений
- Воспроизведение файлов MIDI, отправка сообщений
- Отправка сообщений MIDI
- Цифровой интерфейс MIDI, отдельные сообщения
- MIDI (цифровой интерфейс музыкального инструмента), отдельные сообщения
- Воспроизведение файлов MIDI, отдельных сообщений
- отдельные сообщения MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661695"
---
# <a name="sending-individual-midi-messages"></a><span data-ttu-id="14962-111">Отправка отдельных сообщений MIDI</span><span class="sxs-lookup"><span data-stu-id="14962-111">Sending Individual MIDI Messages</span></span>

<span data-ttu-id="14962-112">Вы можете работать с отдельными сообщениями MIDI с помощью следующих функций.</span><span class="sxs-lookup"><span data-stu-id="14962-112">You can work with individual MIDI messages by using the following functions.</span></span>



| <span data-ttu-id="14962-113">Значение</span><span class="sxs-lookup"><span data-stu-id="14962-113">Value</span></span>                                      | <span data-ttu-id="14962-114">Значение</span><span class="sxs-lookup"><span data-stu-id="14962-114">Meaning</span></span>                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14962-115">**мидиаутлонгмсг**</span><span class="sxs-lookup"><span data-stu-id="14962-115">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | <span data-ttu-id="14962-116">Отправляет буфер данных MIDI на указанное устройство вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="14962-116">Sends a buffer of MIDI data to the specified MIDI output device.</span></span> <span data-ttu-id="14962-117">Используйте эту функцию для отправки безсистемных сообщений на устройство MIDI.</span><span class="sxs-lookup"><span data-stu-id="14962-117">Use this function to send system-exclusive messages to a MIDI device.</span></span>                                              |
| [<span data-ttu-id="14962-118">**мидиаутресет**</span><span class="sxs-lookup"><span data-stu-id="14962-118">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | <span data-ttu-id="14962-119">Отключает все заметки на всех каналах для указанного выходного устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="14962-119">Turns off all notes on all channels for a specified MIDI output device.</span></span> <span data-ttu-id="14962-120">Все ожидающие системные буферы и буферы потоков помечаются как выполненные и возвращаются приложению.</span><span class="sxs-lookup"><span data-stu-id="14962-120">Any pending system-exclusive buffers and stream buffers are marked as done and returned to the application.</span></span> |
| [<span data-ttu-id="14962-121">**мидиаутшортмсг**</span><span class="sxs-lookup"><span data-stu-id="14962-121">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | <span data-ttu-id="14962-122">Отправляет сообщение MIDI на указанное устройство вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="14962-122">Sends a MIDI message to a specified MIDI output device.</span></span>                                                                                                                             |



 

<span data-ttu-id="14962-123">Чтобы отправить сообщение MIDI (за исключением сообщений, исключающих системы), используйте [**мидиаутшортмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span><span class="sxs-lookup"><span data-stu-id="14962-123">To send any MIDI message (except for system-exclusive messages), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span></span>

 

 