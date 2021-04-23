---
title: Обработка данных MIDI из двух источников MIDI
description: Обработка данных MIDI из двух источников MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Мультимедиа Windows, обработка данных MIDI из двух источников
- мультимедиа, обработка данных MIDI из двух источников
- мультимедийные аудио, обработка данных MIDI из двух источников
- звук, обработка данных MIDI из двух источников
- Цифровой интерфейс MIDI, обработка данных из двух источников
- MIDI (цифровой интерфейс музыкального инструмента), обработка данных из двух источников
- обработка данных MIDI из двух источников
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069938"
---
# <a name="processing-midi-data-from-two-midi-sources"></a><span data-ttu-id="9f0b4-110">Обработка данных MIDI из двух источников MIDI</span><span class="sxs-lookup"><span data-stu-id="9f0b4-110">Processing MIDI Data from Two MIDI Sources</span></span>

<span data-ttu-id="9f0b4-111">Подсистема MIDI может направлять сообщения MIDI из двух источников данных на одно устройство вывода MIDI для одновременного воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-111">The MIDI subsystem can route MIDI messages from two data sources to a single MIDI output device for concurrent playback.</span></span> <span data-ttu-id="9f0b4-112">Например, один источник может представлять собой фоновую музыку или строку басов, которая была предварительно записана и сохранена в файле.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-112">For example, one source can be background music or a bass line that has been pre-recorded and stored in a file.</span></span> <span data-ttu-id="9f0b4-113">Второй источник может быть динамическим источником данных из инструмента MIDI, например клавиатуры или гитаре.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-113">The second source can be live data from a MIDI instrument, such as a keyboard or guitar.</span></span>

<span data-ttu-id="9f0b4-114">Оба источника данных отправляют данные MIDI на одно устройство MIDI, которое определяется одним маркером.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-114">Both data sources send MIDI data to a single MIDI device that is identified with one handle.</span></span> <span data-ttu-id="9f0b4-115">Отправка одного потока данных с помощью функции [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) и одного или нескольких буферов потока.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-115">Send one data stream by using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function and one or more stream buffers.</span></span> <span data-ttu-id="9f0b4-116">Этот поток данных обычно содержит предзаписанные данные, Упакованные в буфер.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-116">This data stream typically contains prerecorded data that is packed into the buffer.</span></span>

<span data-ttu-id="9f0b4-117">Отправляйте второй поток данных (обычно из инструмента MIDI) асинхронно с помощью функции [**мидиаутшортмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) .</span><span class="sxs-lookup"><span data-stu-id="9f0b4-117">Send the second data stream (typically from a MIDI instrument) asynchronously by using the [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) function.</span></span> <span data-ttu-id="9f0b4-118">Асинхронные вызовы, выполняемые вторым потоком данных, не будут влиять на состояние выполнения буфера потока.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-118">The running status of a stream buffer will not be adversely affected by the asynchronous calls made by the second data stream.</span></span>

<span data-ttu-id="9f0b4-119">Каждое короткое сообщение, отправленное с помощью **мидиаутшортмсг** , должно быть полным сообщением MIDI с состоянием Byte и соответствующим числом байтов данных.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-119">Each short message sent with **midiOutShortMsg** must be a complete MIDI message, with a status byte and the appropriate number of data bytes.</span></span> <span data-ttu-id="9f0b4-120">Если байт состояния опущен, **мидиаутшортмсг** возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-120">If the status byte is omitted, **midiOutShortMsg** returns an error.</span></span> <span data-ttu-id="9f0b4-121">(Однако отсутствует состояние выполнения с выходом потока.)</span><span class="sxs-lookup"><span data-stu-id="9f0b4-121">(However, there is no running status with stream output.)</span></span>

 

 