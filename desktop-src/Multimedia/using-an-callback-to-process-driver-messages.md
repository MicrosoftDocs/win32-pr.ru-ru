---
title: Использование обратного вызова события для обработки сообщений драйвера
description: Использование обратного вызова события для обработки сообщений драйвера
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- звуковая волна, обратный вызов события
- блоки звуковых данных, обратный вызов события
- звуковая волна, обработка сообщений драйвера
- блоки звуковых данных, обработка сообщений драйверов
- Обработка сообщений драйвера
- Функция CreateEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790212"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="dab0f-109">Использование обратного вызова события для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="dab0f-109">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="dab0f-110">Чтобы использовать обратный вызов события, используйте функцию [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) для создания события ручного сброса.</span><span class="sxs-lookup"><span data-stu-id="dab0f-110">To use an event callback, use the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event.</span></span> <span data-ttu-id="dab0f-111">В вызове функции [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) укажите **\_ событие обратного вызова** для параметра *фдвопен* .</span><span class="sxs-lookup"><span data-stu-id="dab0f-111">In the call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function, specify **CALLBACK\_EVENT** for the *fdwOpen* parameter.</span></span> <span data-ttu-id="dab0f-112">После вызова функции [**вавеаутпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , но перед отправкой данных аудио-сигнала на устройство, переведите событие в несигнальное состояние, вызвав функцию [**ресетевент**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) .</span><span class="sxs-lookup"><span data-stu-id="dab0f-112">After you call the [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) function, but before sending waveform-audio data to the device, put the event into a nonsignaled state by calling the [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) function.</span></span> <span data-ttu-id="dab0f-113">Затем внутри цикла, который проверяет, установлен ли **флаг вхдр \_ done** в элементе **dwFlags** структуры [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , вызовите функцию [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , указав в качестве параметров маркер события и значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="dab0f-113">Then, inside a loop that checks whether the **WHDR\_DONE** flag is set in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure, call the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying as parameters the event handle and a time-out value.</span></span>

<span data-ttu-id="dab0f-114">Поскольку обратные вызовы событий не получают конкретных закрытых, готовых или открытых уведомлений, приложению может потребоваться проверить состояние процесса, ожидающего выполнения после наступления события.</span><span class="sxs-lookup"><span data-stu-id="dab0f-114">Because event callbacks do not receive specific close, done, or open notifications, an application might have to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="dab0f-115">Возможно, число задач было завершено в момент возвращения объекта [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="dab0f-115">It is possible that a number of tasks could have been completed by the time [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) returns.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dab0f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="dab0f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dab0f-117">Звуковые блоки данных</span><span class="sxs-lookup"><span data-stu-id="dab0f-117">Audio Data Blocks</span></span>](audio-data-blocks.md)
</dt> </dl>

 

 