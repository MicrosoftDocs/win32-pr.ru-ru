---
title: Использование функции обратного вызова для управления воспроизведением в буфере
description: Использование функции обратного вызова для управления воспроизведением в буфере
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- Цифровой интерфейс MIDI, буферизованное воспроизведение
- MIDI (цифровой интерфейс музыкального инструмента), буферизованное воспроизведение
- Воспроизведение файлов MIDI, буферизованное воспроизведение
- Воспроизведение в буфере
- Сообщение MOM_CLOSE
- Сообщение MOM_DONE
- Сообщение MOM_OPEN
- Цифровой интерфейс музыкальных инструментов (MIDI), отправка сообщений
- MIDI (цифровой интерфейс музыкального инструмента), отправка сообщений
- Воспроизведение файлов MIDI, отправка сообщений
- Отправка сообщений MIDI
- Цифровой интерфейс музыкальных инструментов (MIDI), функции обратного вызова
- MIDI (цифровой интерфейс музыкального инструмента), функции обратного вызова
- Воспроизведение файлов MIDI, функции обратного вызова
- Функция обратного вызова Мидиаутпрок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790872"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a><span data-ttu-id="c4624-118">Использование функции обратного вызова для управления воспроизведением в буфере</span><span class="sxs-lookup"><span data-stu-id="c4624-118">Using a Callback Function to Manage Buffered Playback</span></span>

<span data-ttu-id="c4624-119">Вы можете определить собственную функцию обратного вызова для управления буферизованным воспроизведением устройств MIDI Output.</span><span class="sxs-lookup"><span data-stu-id="c4624-119">You can define your own callback function to manage buffered playback of MIDI output devices.</span></span> <span data-ttu-id="c4624-120">Функция обратного вызова описана как [**мидиаутпрок**](/previous-versions//dd798478(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4624-120">The callback function is documented as [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span></span>

<span data-ttu-id="c4624-121">В параметр *вмсг* функции обратного вызова **мидиаутпрок** можно отправить следующие сообщения.</span><span class="sxs-lookup"><span data-stu-id="c4624-121">The following messages can be sent to the *wMsg* parameter of the **MidiOutProc** callback function.</span></span>



| <span data-ttu-id="c4624-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c4624-122">Value</span></span>                           | <span data-ttu-id="c4624-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c4624-123">Meaning</span></span>                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4624-124">**\_закрытие MOM**</span><span class="sxs-lookup"><span data-stu-id="c4624-124">**MOM\_CLOSE**</span></span>](mom-close.md) | <span data-ttu-id="c4624-125">Отправляется, когда устройство закрывается с помощью функции [**мидиаутклосе**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .</span><span class="sxs-lookup"><span data-stu-id="c4624-125">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="c4624-126">**MOM \_**</span><span class="sxs-lookup"><span data-stu-id="c4624-126">**MOM\_DONE**</span></span>](mom-done.md)   | <span data-ttu-id="c4624-127">Посылается, когда драйвер устройства завершает работу с блоком данных, отправленным с помощью функции [**мидиаутлонгмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) или [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) .</span><span class="sxs-lookup"><span data-stu-id="c4624-127">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="c4624-128">**диспетчер MOM \_ открыт**</span><span class="sxs-lookup"><span data-stu-id="c4624-128">**MOM\_OPEN**</span></span>](mom-open.md)   | <span data-ttu-id="c4624-129">Отправляется при открытии устройства с помощью функции [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="c4624-129">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="c4624-130">Эти сообщения похожи на те, которые были отправлены в функции процедур Windows, но параметры различны.</span><span class="sxs-lookup"><span data-stu-id="c4624-130">These messages are similar to those sent to window procedure functions, but the parameters are different.</span></span> <span data-ttu-id="c4624-131">Обработчик открытого MIDI-устройства передается в качестве параметра функции обратного вызова вместе с даублеворд данных экземпляра, передаваемых с помощью **мидиаутопен**.</span><span class="sxs-lookup"><span data-stu-id="c4624-131">A handle of the open MIDI device is passed as a parameter to the callback function, along with the doubleword of instance data passed by using **midiOutOpen**.</span></span>

<span data-ttu-id="c4624-132">После завершения работы драйвера с блоком данных можно очистить и освободить блок данных.</span><span class="sxs-lookup"><span data-stu-id="c4624-132">After the driver is finished with a data block, you can clean up and free the data block.</span></span> <span data-ttu-id="c4624-133">Из-за предлагаемых ограничений функций обратного вызова лучше не делать это в функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c4624-133">Because of the suggested restrictions on callback functions, it is better not to do this from within the callback function.</span></span>

 

 