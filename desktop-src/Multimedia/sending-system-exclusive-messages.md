---
title: Отправка сообщений System-Exclusive
description: Отправка сообщений System-Exclusive
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), отправка сообщений
- MIDI (цифровой интерфейс музыкального инструмента), отправка сообщений
- Воспроизведение файлов MIDI, отправка сообщений
- Отправка сообщений MIDI
- Цифровой интерфейс MIDI, сообщения, исключаемые из системы
- MIDI (цифровой интерфейс музыкального инструмента), сообщения, исключаемые из системы
- Воспроизведение файлов MIDI, сообщений, исключаемых из системы
- сообщения, исключающие системы MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890469"
---
# <a name="sending-system-exclusive-messages"></a><span data-ttu-id="d04b1-111">Отправка сообщений System-Exclusive</span><span class="sxs-lookup"><span data-stu-id="d04b1-111">Sending System-Exclusive Messages</span></span>

<span data-ttu-id="d04b1-112">Сообщения, исключающие систему MIDI — это единственные сообщения MIDI, которые не помещаются в одно значение даублеворд.</span><span class="sxs-lookup"><span data-stu-id="d04b1-112">MIDI system-exclusive messages are the only MIDI messages that will not fit into a single doubleword value.</span></span> <span data-ttu-id="d04b1-113">Сообщения, исключающие из системы, могут иметь любую длину.</span><span class="sxs-lookup"><span data-stu-id="d04b1-113">System-exclusive messages can be any length.</span></span> <span data-ttu-id="d04b1-114">Windows предоставляет функцию [**мидиаутлонгмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) для отправки безсистемных сообщений на устройства вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="d04b1-114">Windows provides the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) function for sending system-exclusive messages to MIDI output devices.</span></span> <span data-ttu-id="d04b1-115">Для указания блоков данных, исключающих систему MIDI, используйте структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .</span><span class="sxs-lookup"><span data-stu-id="d04b1-115">To specify MIDI system-exclusive data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

<span data-ttu-id="d04b1-116">После отправки безсистемного блока данных с помощью **мидиаутлонгмсг** необходимо дождаться завершения работы драйвера устройства с блоком данных перед его освобождением.</span><span class="sxs-lookup"><span data-stu-id="d04b1-116">After you send a system-exclusive data block using **midiOutLongMsg**, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="d04b1-117">При отправке нескольких блоков данных необходимо отслеживать завершение каждого блока данных, чтобы вы могли получить сведения о том, когда отправлять дополнительные блоки.</span><span class="sxs-lookup"><span data-stu-id="d04b1-117">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="d04b1-118">Сведения о различных методах мониторинга завершения блоков данных см. в разделе [Управление блоками данных MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="d04b1-118">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

> [!Note]  
> <span data-ttu-id="d04b1-119">Любой байт состояния MIDI, отличный от сообщения системы в режиме реального времени, прерывает системное сообщение.</span><span class="sxs-lookup"><span data-stu-id="d04b1-119">Any MIDI status byte other than a system-real-time message will terminate a system-exclusive message.</span></span> <span data-ttu-id="d04b1-120">При использовании нескольких блоков данных для отправки одного сообщения, эксклюзивного от системы, не отправляйте сообщения MIDI, отличные от системных сообщений в режиме реального времени между блоками данных.</span><span class="sxs-lookup"><span data-stu-id="d04b1-120">If you are using multiple data blocks to send a single system-exclusive message, do not send any MIDI messages other than system-real-time messages between data blocks.</span></span>

 

 

 