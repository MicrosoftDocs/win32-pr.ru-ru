---
title: Использование обратного вызова события для управления воспроизведением в буфере
description: Использование обратного вызова события для управления воспроизведением в буфере
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- Цифровой интерфейс MIDI, буферизованное воспроизведение
- MIDI (цифровой интерфейс музыкального инструмента), буферизованное воспроизведение
- Воспроизведение файлов MIDI, буферизованное воспроизведение
- Воспроизведение в буфере
- Функция CreateEvent
- Цифровой интерфейс MIDI, обратный вызов события
- MIDI (цифровой интерфейс музыкального инструмента), обратный вызов события
- Воспроизведение файлов MIDI, обратный вызов события
- обратный вызов события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6f6cc7bec7971c117cb81b2f823d7184bc2fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790213"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a><span data-ttu-id="f2a31-112">Использование обратного вызова события для управления воспроизведением в буфере</span><span class="sxs-lookup"><span data-stu-id="f2a31-112">Using an Event Callback to Manage Buffered Playback</span></span>

<span data-ttu-id="f2a31-113">Чтобы использовать обратный вызов события, используйте функцию [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) для получения маркера события.</span><span class="sxs-lookup"><span data-stu-id="f2a31-113">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event.</span></span> <span data-ttu-id="f2a31-114">При вызове функции [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) укажите событие обратного вызова \_ для параметра *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="f2a31-114">In a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function, specify CALLBACK\_EVENT for the *dwFlags* parameter.</span></span> <span data-ttu-id="f2a31-115">После использования функции [**мидиаутпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) , но перед отправкой событий MIDI на устройство создайте несигнальное событие, вызвав функцию [ресетевент](/windows/win32/api/synchapi/nf-synchapi-resetevent) , указав дескриптор события, полученный с помощью функции **CreateEvent**.</span><span class="sxs-lookup"><span data-stu-id="f2a31-115">After using the [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function but before sending MIDI events to the device, create a nonsignaled event by calling the [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) function, specifying the event handle retrieved by **CreateEvent**.</span></span> <span data-ttu-id="f2a31-116">Затем внутри цикла, который проверяет, \_ установлен ли бит мхдр Done в элементе **DwFlags** структуры [**Мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , используйте функцию [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , указав маркер события и значение времени ожидания бесконечности в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="f2a31-116">Then, inside a loop that checks whether the MHDR\_DONE bit is set in the **dwFlags** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure, use the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying the event handle and a time-out value of INFINITE as parameters.</span></span>

<span data-ttu-id="f2a31-117">Обратный вызов события задается любым значением, которое может вызвать обратный вызов функции.</span><span class="sxs-lookup"><span data-stu-id="f2a31-117">An event callback is set by anything that might cause a function callback.</span></span>

<span data-ttu-id="f2a31-118">Поскольку обратные вызовы событий не получают конкретных закрытых, готовых или открытых уведомлений, приложению может потребоваться проверить состояние процесса, ожидающего выполнения после наступления события.</span><span class="sxs-lookup"><span data-stu-id="f2a31-118">Because event callbacks do not receive specific close, done, or open notifications, an application may need to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="f2a31-119">При возвращении объекта **WaitForSingleObject** может завершиться ряд задач.</span><span class="sxs-lookup"><span data-stu-id="f2a31-119">It is possible that a number of tasks could be completed by the time **WaitForSingleObject** returns.</span></span>

 

 