---
title: Отправка сообщений MIDI с помощью буферов потоков
description: Отправка сообщений MIDI с помощью буферов потоков
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), буферы потоков
- MIDI (цифровой интерфейс музыкального инструмента), буферы потоков
- Воспроизведение файлов MIDI, буферов потоков
- буферы потоков, отправка сообщений MIDI
- Цифровой интерфейс музыкальных инструментов (MIDI), отправка сообщений
- MIDI (цифровой интерфейс музыкального инструмента), отправка сообщений
- Воспроизведение файлов MIDI, отправка сообщений
- Отправка сообщений MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790170"
---
# <a name="sending-midi-messages-with-stream-buffers"></a><span data-ttu-id="ee2a2-111">Отправка сообщений MIDI с помощью буферов потоков</span><span class="sxs-lookup"><span data-stu-id="ee2a2-111">Sending MIDI Messages with Stream Buffers</span></span>

<span data-ttu-id="ee2a2-112">Когда приложение работает с буферами потоков, оно использует функцию [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) для отправки всех (коротких и длинных) сообщений MIDI на устройство.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-112">When your application works with stream buffers, it uses the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function to send all (short and long) MIDI messages to the device.</span></span> <span data-ttu-id="ee2a2-113">Чтобы указать блоки потоковых данных, используйте структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) и [**мидиевент**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="ee2a2-113">To specify stream data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) and [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structures.</span></span> <span data-ttu-id="ee2a2-114">Структура **мидихдр** содержит адрес заблокированного блока данных, длину блока данных и некоторые флаги ассортимента.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-114">The **MIDIHDR** structure contains an address of a locked data block, the data-block length, and some assorted flags.</span></span> <span data-ttu-id="ee2a2-115">Данные хранятся в виде структур **мидиевент** .</span><span class="sxs-lookup"><span data-stu-id="ee2a2-115">The data is stored in the form of **MIDIEVENT** structures.</span></span> <span data-ttu-id="ee2a2-116">Система накладывает ограничение размера 64 КБ на буферы потоков.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-116">The system imposes a size limit of 64K on stream buffers.</span></span>

<span data-ttu-id="ee2a2-117">После использования **мидистреамаут** для отправки буфера потока данных необходимо дождаться завершения работы драйвера устройства с блоком данных перед его освобождением.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-117">After you use **midiStreamOut** to send a stream buffer of data, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="ee2a2-118">При отправке нескольких блоков данных необходимо отслеживать завершение каждого блока данных, чтобы вы могли получить сведения о том, когда отправлять дополнительные блоки.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-118">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="ee2a2-119">Сведения о различных методах мониторинга завершения блоков данных см. в разделе [Управление блоками данных MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="ee2a2-119">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 