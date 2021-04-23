---
title: Использование окна или потока для управления воспроизведением в буфере
description: Использование окна или потока для управления воспроизведением в буфере
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- Цифровой интерфейс MIDI, буферизованное воспроизведение
- MIDI (цифровой интерфейс музыкального инструмента), буферизованное воспроизведение
- Воспроизведение файлов MIDI, буферизованное воспроизведение
- Воспроизведение в буфере
- Сообщение MM_MOM_CLOSE
- Сообщение MM_MOM_DONE
- Сообщение MM_MOM_OPEN
- Цифровой интерфейс музыкальных инструментов (MIDI), отправка сообщений
- MIDI (цифровой интерфейс музыкального инструмента), отправка сообщений
- Воспроизведение файлов MIDI, отправка сообщений
- Отправка сообщений MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337313"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a><span data-ttu-id="2408a-114">Использование окна или потока для управления воспроизведением в буфере</span><span class="sxs-lookup"><span data-stu-id="2408a-114">Using a Window or Thread to Manage Buffered Playback</span></span>

<span data-ttu-id="2408a-115">Следующие сообщения можно отправить в окно или поток для управления воспроизведением безсистемных сообщений MIDI или буферов потоков.</span><span class="sxs-lookup"><span data-stu-id="2408a-115">The following messages can be sent to a window or thread for managing playback of MIDI system-exclusive messages or stream buffers.</span></span>



| <span data-ttu-id="2408a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2408a-116">Value</span></span>                                  | <span data-ttu-id="2408a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2408a-117">Meaning</span></span>                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2408a-118">**\_закрытие mm MOM \_**</span><span class="sxs-lookup"><span data-stu-id="2408a-118">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md) | <span data-ttu-id="2408a-119">Отправляется, когда устройство закрывается с помощью функции [**мидиаутклосе**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="2408a-119">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="2408a-120">**MM, \_ MOM \_**</span><span class="sxs-lookup"><span data-stu-id="2408a-120">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)   | <span data-ttu-id="2408a-121">Посылается, когда драйвер устройства завершает работу с блоком данных, отправленным с помощью функции [**мидиаутлонгмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) или [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="2408a-121">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="2408a-122">**\_ \_ открытая MOM mm**</span><span class="sxs-lookup"><span data-stu-id="2408a-122">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)   | <span data-ttu-id="2408a-123">Отправляется при открытии устройства с помощью функции [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="2408a-123">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="2408a-124">Параметр *wParam* и параметр *lParam* связаны с каждым из этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="2408a-124">A *wParam* parameter and an *lParam* parameter are associated with each of these messages.</span></span> <span data-ttu-id="2408a-125">Параметр *wParam* всегда задает маркер открытого устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="2408a-125">The *wParam* parameter always specifies the handle of an open MIDI device.</span></span> <span data-ttu-id="2408a-126">Для [**mm \_ MOM \_**](mm-mom-done.md)значение *lParam* указывает адрес структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющей завершенный блок данных.</span><span class="sxs-lookup"><span data-stu-id="2408a-126">For [**MM\_MOM\_DONE**](mm-mom-done.md), *lParam* specifies an address of a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the completed data block.</span></span> <span data-ttu-id="2408a-127">Параметр *lParam* не используется для открытых MOM- [**\_ \_ Close**](mm-mom-close.md) и [**mm \_ MOM \_**](mm-mom-open.md).</span><span class="sxs-lookup"><span data-stu-id="2408a-127">The *lParam* parameter is unused for [**MM\_MOM\_CLOSE**](mm-mom-close.md) and [**MM\_MOM\_OPEN**](mm-mom-open.md).</span></span>

<span data-ttu-id="2408a-128">Наиболее полезное сообщение, вероятно, — MM \_ MOM \_ .</span><span class="sxs-lookup"><span data-stu-id="2408a-128">The most useful message is probably MM\_MOM\_DONE.</span></span> <span data-ttu-id="2408a-129">Если вам не нужно выделять память или инициализировать переменные, вам, скорее всего, не нужно обрабатывать MM \_ MOM \_ Open и mm \_ MOM \_ Close.</span><span class="sxs-lookup"><span data-stu-id="2408a-129">Unless you need to allocate memory or initialize variables, you probably do not need to process MM\_MOM\_OPEN and MM\_MOM\_CLOSE.</span></span> <span data-ttu-id="2408a-130">После завершения воспроизведения блока данных можно очистить и освободить блок данных.</span><span class="sxs-lookup"><span data-stu-id="2408a-130">When playback of a data block is complete, you can clean up and free the data block.</span></span>

 

 