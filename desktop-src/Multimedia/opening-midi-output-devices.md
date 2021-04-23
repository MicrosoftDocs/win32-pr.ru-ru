---
title: Открытие выходных устройств MIDI
description: Открытие выходных устройств MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- Цифровой интерфейс MIDI, выходные устройства
- MIDI (цифровой интерфейс музыкального инструмента), выходные устройства
- Воспроизведение файлов MIDI, выходных устройств
- Устройства вывода MIDI
- Цифровой интерфейс музыкальных инструментов (MIDI), открытие выходных устройств
- MIDI (цифровой интерфейс музыкального инструмента), открытие выходных устройств
- Воспроизведение файлов MIDI, открытие выходных устройств
- Открытие выходных устройств MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487644"
---
# <a name="opening-midi-output-devices"></a><span data-ttu-id="57e90-111">Открытие выходных устройств MIDI</span><span class="sxs-lookup"><span data-stu-id="57e90-111">Opening MIDI Output Devices</span></span>

<span data-ttu-id="57e90-112">Чтобы открыть устройство вывода MIDI для воспроизведения, используйте функцию [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .</span><span class="sxs-lookup"><span data-stu-id="57e90-112">To open a MIDI output device for playback, use the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="57e90-113">Эта функция открывает устройство, связанное с указанным идентификатором устройства, и возвращает маркер открытого устройства путем записи маркера в указанное место в памяти.</span><span class="sxs-lookup"><span data-stu-id="57e90-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="57e90-114">Одним из параметров **мидиаутопен** является значение даублеворд.</span><span class="sxs-lookup"><span data-stu-id="57e90-114">One of the parameters of **midiOutOpen** is a doubleword value.</span></span> <span data-ttu-id="57e90-115">Это значение указывает обработчика окна или потока, обработчик события или адрес функции обратного вызова, который используется для отслеживания хода воспроизведения потока данных, исключающих систему MIDI, и буферов потоков.</span><span class="sxs-lookup"><span data-stu-id="57e90-115">This value specifies a window or thread handle, an event handle, or the address of a callback function that is used to monitor the progress of the playback of MIDI system-exclusive data and stream buffers.</span></span> <span data-ttu-id="57e90-116">Мониторинг позволяет приложению определить, когда отправлять дополнительные блоки данных и когда отправляются свободные блоки данных.</span><span class="sxs-lookup"><span data-stu-id="57e90-116">Monitoring enables the application to determine when to send additional data blocks and when to free data blocks that have been sent.</span></span> <span data-ttu-id="57e90-117">Дополнительные сведения об этих методах см. в разделе [Управление блоками данных MIDI](managing-midi-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="57e90-117">For more information about these methods, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 