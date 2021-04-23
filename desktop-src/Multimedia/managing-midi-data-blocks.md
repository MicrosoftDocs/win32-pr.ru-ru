---
title: Управление блоками данных MIDI
description: Управление блоками данных MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- Цифровой интерфейс MIDI, Управление блоками данных
- MIDI (цифровой интерфейс музыкального инструмента), Управление блоками данных
- Службы MIDI, Управление блоками данных
- Управление блоками данных MIDI
- Цифровой интерфейс музыкальных инструментов (MIDI), обработка сообщений драйвера
- MIDI (цифровой интерфейс музыкального инструмента), обработка сообщений драйвера
- Службы MIDI, обработка сообщений драйвера
- Обработка сообщений драйвера
- Цифровой интерфейс MIDI, блоки данных
- MIDI (цифровой интерфейс музыкального инструмента), блоки данных
- Службы MIDI, блоки данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987403"
---
# <a name="managing-midi-data-blocks"></a><span data-ttu-id="d9004-114">Управление блоками данных MIDI</span><span class="sxs-lookup"><span data-stu-id="d9004-114">Managing MIDI Data Blocks</span></span>

<span data-ttu-id="d9004-115">Приложения, использующие блоки данных для передачи безсистемных сообщений (с помощью функций [**мидиаутлонгмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) и [**мидиинаддбуффер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) и буферов потоков (с помощью функции [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ), должны постоянно предоставлять драйвер устройства блоками данных до завершения воспроизведения или записи.</span><span class="sxs-lookup"><span data-stu-id="d9004-115">Applications that use data blocks for passing system-exclusive messages (using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) and [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) functions) and stream buffers (using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function) must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="d9004-116">Даже если используется один блок данных, приложение должно иметь возможность определить, завершена ли работа драйвера устройства с блоком данных, чтобы освободить память, связанную с блоком данных и структурой заголовков.</span><span class="sxs-lookup"><span data-stu-id="d9004-116">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so it can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="d9004-117">Для определения завершения работы драйвера устройства с блоком данных можно использовать три метода:</span><span class="sxs-lookup"><span data-stu-id="d9004-117">Three methods can be used to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="d9004-118">Укажите функцию обратного вызова для получения сообщения, отправленного драйвером после завершения работы с блоком данных.</span><span class="sxs-lookup"><span data-stu-id="d9004-118">Specify a callback function to receive a message sent by the driver when it is finished with a data block.</span></span> <span data-ttu-id="d9004-119">Чтобы получить входные данные MIDI с отметкой времени, необходимо использовать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d9004-119">To get time-stamped MIDI input data, you must use a callback function.</span></span>
-   <span data-ttu-id="d9004-120">Используйте обратный вызов события (только для выходных данных).</span><span class="sxs-lookup"><span data-stu-id="d9004-120">Use an event callback (for output only).</span></span>
-   <span data-ttu-id="d9004-121">Используйте обратный вызов окна или потока для получения сообщения, отправленного драйвером после завершения работы с блоком данных.</span><span class="sxs-lookup"><span data-stu-id="d9004-121">Use a window or thread callback to receive a message sent by the driver when it is finished with a data block.</span></span>

<span data-ttu-id="d9004-122">Если приложение не получает блок данных к драйверу устройства при необходимости, может произойти пропускная запись при воспроизведении или утрата входящей записанной информации.</span><span class="sxs-lookup"><span data-stu-id="d9004-122">If an application does not get a data block to the device driver when it is needed, an audible gap in playback or a loss of incoming recorded information can occur.</span></span> <span data-ttu-id="d9004-123">Как минимум, приложение должно использовать схему двойной буферизации, чтобы оставаться по крайней мере один блок данных перед драйвером устройства.</span><span class="sxs-lookup"><span data-stu-id="d9004-123">At a minimum, an application should use a double-buffering scheme to stay at least one data block ahead of the device driver.</span></span>

## <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="d9004-124">Использование функции обратного вызова для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="d9004-124">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="d9004-125">Вы можете написать собственную функцию обратного вызова для обработки сообщений, отправленных драйвером устройства.</span><span class="sxs-lookup"><span data-stu-id="d9004-125">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="d9004-126">Чтобы использовать функцию обратного вызова, укажите флаг функции ОБРАТНОго вызова \_ в параметре *dwFlags* и адрес функции обратного вызова в параметре *Двкаллбакк* функции [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) или [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="d9004-126">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *dwFlags* parameter and the address of the callback function in the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="d9004-127">Сообщения, отправленные в функцию обратного вызова, похожи на сообщения, отправленные в окно, за исключением того, что они имеют два параметра даублеворд, а не целочисленный параметр без знака и параметр даублеворд.</span><span class="sxs-lookup"><span data-stu-id="d9004-127">Messages sent to a callback function are similar to messages sent to a window, except they have two doubleword parameters instead of an unsigned integer parameter and a doubleword parameter.</span></span> <span data-ttu-id="d9004-128">Дополнительные сведения об этих сообщениях см. в разделе [Отправка сообщений System-Exclusive](sending-system-exclusive-messages.md) и [Управление записью MIDI](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="d9004-128">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

<span data-ttu-id="d9004-129">Используйте один из следующих методов передачи данных экземпляра из приложения в функцию обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="d9004-129">Use one of the following techniques to pass instance data from an application to a callback function:</span></span>

-   <span data-ttu-id="d9004-130">Используйте параметр *двкаллбаккинстанце* функции, которая открывает драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="d9004-130">Use the *dwCallbackInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="d9004-131">Используйте элемент **двусер** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющий блок данных, отправляемый драйверу устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9004-131">Use the **dwUser** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies a data block being sent to a MIDI device driver.</span></span>

<span data-ttu-id="d9004-132">Если требуется более 32 бит данных экземпляра, передайте адрес структуры, содержащей дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d9004-132">If you need more than 32 bits of instance data, pass an address of a structure containing the additional information.</span></span>

## <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="d9004-133">Использование обратного вызова события для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="d9004-133">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="d9004-134">Чтобы использовать обратный вызов события, используйте функцию [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) для получения маркера события и укажите событие обратного вызова \_ в вызове функции [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="d9004-134">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event and specify CALLBACK\_EVENT in the call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="d9004-135">Обратный вызов события задается любым значением, которое может вызвать обратный вызов функции.</span><span class="sxs-lookup"><span data-stu-id="d9004-135">An event callback is set by anything that might cause a function callback.</span></span> <span data-ttu-id="d9004-136">В отличие от функций обратного вызова и обратных вызовов окон или потоков, обратные вызовы событий не получают конкретных закрытых, готовых или открытых уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d9004-136">Unlike callback functions and window or thread callbacks, event callbacks do not receive specific close, done, or open notifications.</span></span> <span data-ttu-id="d9004-137">Таким образом, приложению может потребоваться проверить состояние процесса, ожидающего выполнения после наступления события.</span><span class="sxs-lookup"><span data-stu-id="d9004-137">Therefore, an application may have to check the status of the process it is waiting for after the event occurs.</span></span>

<span data-ttu-id="d9004-138">Дополнительные сведения о обратных вызовах событий см. [в разделе Использование обратного вызова события для управления буферизованным воспроизведением](using-an-callback-to-manage-buffered-playback.md).</span><span class="sxs-lookup"><span data-stu-id="d9004-138">For more information about event callbacks, see [Using an Event Callback to Manage Buffered Playback](using-an-callback-to-manage-buffered-playback.md).</span></span>

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a><span data-ttu-id="d9004-139">Использование обратного вызова окна или потока для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="d9004-139">Using a Window or Thread Callback to Process Driver Messages</span></span>

<span data-ttu-id="d9004-140">Чтобы использовать обратный вызов окна, укажите флаг окна ОБРАТНОго вызова \_ в параметре *dwFlags* и маркер окна в младшем слове параметра *Двкаллбакк* функции [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) или [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="d9004-140">To use a window callback, specify the CALLBACK\_WINDOW flag in the *dwFlags* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="d9004-141">Сообщения драйвера будут отправляться в функцию окна процедуры для окна, идентифицируемого по маркеру в *двкаллбакк*.</span><span class="sxs-lookup"><span data-stu-id="d9004-141">Driver messages will be sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="d9004-142">Аналогично, чтобы использовать обратный вызов потока, укажите флаг потока ОБРАТНОго вызова \_ и идентификатор потока в вызове **Мидиинопен** или **мидиаутопен**.</span><span class="sxs-lookup"><span data-stu-id="d9004-142">Similarly, to use a thread callback, specify the CALLBACK\_THREAD flag and a thread identifier in the call to **midiInOpen** or **midiOutOpen**.</span></span> <span data-ttu-id="d9004-143">В этом случае сообщения будут публиковаться в указанном потоке, а не в окне.</span><span class="sxs-lookup"><span data-stu-id="d9004-143">In this case, messages will be posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="d9004-144">Сообщения, отправленные в ответный вызов окна или потока, относятся к используемому устройству MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9004-144">Messages sent to a window or thread callback are specific to the MIDI device used.</span></span> <span data-ttu-id="d9004-145">Дополнительные сведения об этих сообщениях см. в разделе [Отправка сообщений System-Exclusive](sending-system-exclusive-messages.md) и [Управление записью MIDI](managing-midi-recording.md).</span><span class="sxs-lookup"><span data-stu-id="d9004-145">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9004-146">См. также</span><span class="sxs-lookup"><span data-stu-id="d9004-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9004-147">Службы MIDI</span><span class="sxs-lookup"><span data-stu-id="d9004-147">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 