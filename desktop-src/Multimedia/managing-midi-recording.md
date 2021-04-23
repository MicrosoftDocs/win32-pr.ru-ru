---
title: Управление записью MIDI
description: Управление записью MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- Цифровой интерфейс MIDI, запись
- MIDI (цифровой интерфейс музыкального инструмента), запись
- запись аудио MIDI, управление
- Запись MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487549"
---
# <a name="managing-midi-recording"></a><span data-ttu-id="ddb8b-107">Управление записью MIDI</span><span class="sxs-lookup"><span data-stu-id="ddb8b-107">Managing MIDI Recording</span></span>

<span data-ttu-id="ddb8b-108">После открытия устройства MIDI можно начать запись данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-108">After you open a MIDI device, you can begin recording MIDI data.</span></span> <span data-ttu-id="ddb8b-109">Windows предоставляет следующие функции для управления записью MIDI.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-109">Windows provides the following functions for managing MIDI recording.</span></span>



| <span data-ttu-id="ddb8b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ddb8b-110">Value</span></span>                                      | <span data-ttu-id="ddb8b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ddb8b-111">Meaning</span></span>                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddb8b-112">**мидиинаддбуффер**</span><span class="sxs-lookup"><span data-stu-id="ddb8b-112">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | <span data-ttu-id="ddb8b-113">Отправляет буфер драйверу устройства, чтобы его можно было заполнить записанными системой данными MIDI.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-113">Sends a buffer to the device driver so it can be filled with recorded system-exclusive MIDI data.</span></span> |
| [<span data-ttu-id="ddb8b-114">**мидиинресет**</span><span class="sxs-lookup"><span data-stu-id="ddb8b-114">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | <span data-ttu-id="ddb8b-115">Останавливает запись MIDI и помечает все ожидающие буфер как выполненные.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-115">Stops MIDI recording and marks all pending buffers as done.</span></span>                                       |
| [<span data-ttu-id="ddb8b-116">**мидиинстарт**</span><span class="sxs-lookup"><span data-stu-id="ddb8b-116">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | <span data-ttu-id="ddb8b-117">Запускает запись MIDI и сбрасывает отметку времени в ноль.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-117">Starts MIDI recording and resets the time stamp to zero.</span></span>                                          |
| [<span data-ttu-id="ddb8b-118">**мидиинстоп**</span><span class="sxs-lookup"><span data-stu-id="ddb8b-118">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | <span data-ttu-id="ddb8b-119">Останавливает запись MIDI.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-119">Stops MIDI recording.</span></span>                                                                             |



 

<span data-ttu-id="ddb8b-120">Для отправки буферов в драйвер устройства для записи исключающих сообщений используйте [**мидиинаддбуффер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span><span class="sxs-lookup"><span data-stu-id="ddb8b-120">To send buffers to the device driver for recording system-exclusive messages, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span></span> <span data-ttu-id="ddb8b-121">Приложение получает уведомления, так как буферы заполнены регистрируемыми системой данными.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-121">The application is notified as the buffers are filled with system-exclusive recorded data.</span></span> <span data-ttu-id="ddb8b-122">Дополнительные сведения о методах уведомления см. в разделе [Управление блоками данных MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="ddb8b-122">For more information about the notification techniques, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

<span data-ttu-id="ddb8b-123">Функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) начинает процесс записи.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-123">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function begins the recording process.</span></span> <span data-ttu-id="ddb8b-124">При записи исключающих системных сообщений перед началом записи отправьте по крайней мере один буфер в драйвер.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-124">When recording system-exclusive messages, send at least one buffer to the driver before starting recording.</span></span> <span data-ttu-id="ddb8b-125">Чтобы прерывать запись, используйте [**мидиинстоп**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span><span class="sxs-lookup"><span data-stu-id="ddb8b-125">To stop recording, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span></span> <span data-ttu-id="ddb8b-126">Перед закрытием устройства с помощью функции [**мидиинклосе**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) пометьте все ожидающие блоки данных как выполненные путем вызова [**мидиинресет**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span><span class="sxs-lookup"><span data-stu-id="ddb8b-126">Before closing the device by using the [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) function, mark any pending data blocks as being done by calling [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span></span>

<span data-ttu-id="ddb8b-127">Приложения, для которых требуются данные с отметкой времени, используют функцию обратного вызова для получения данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-127">Applications that require time-stamped data use a callback function to receive MIDI data.</span></span> <span data-ttu-id="ddb8b-128">Если ваши требования к времени не ограничиваются, можно использовать обратный вызов окна или потока.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-128">If your timing requirements are not strict, you can use a window or thread callback.</span></span> <span data-ttu-id="ddb8b-129">Однако нельзя использовать обратный вызов события для получения данных MIDI.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-129">However, you cannot use an event callback to receive MIDI data.</span></span>

<span data-ttu-id="ddb8b-130">Для записи безсистемных сообщений с приложениями, которые не используют буферы потоков, необходимо предоставить драйверу устройства буферы.</span><span class="sxs-lookup"><span data-stu-id="ddb8b-130">To record system-exclusive messages with applications that do not use stream buffers, you must supply the device driver with buffers.</span></span> <span data-ttu-id="ddb8b-131">Эти буферы указываются с помощью структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="ddb8b-131">These buffers are specified by using a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddb8b-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ddb8b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddb8b-133">Запись звука MIDI</span><span class="sxs-lookup"><span data-stu-id="ddb8b-133">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 