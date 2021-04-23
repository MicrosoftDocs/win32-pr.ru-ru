---
title: Сброс выходных данных MIDI
description: Сброс выходных данных MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), сброс выходных устройств
- MIDI (цифровой интерфейс музыкального инструмента), сброс выходных устройств
- Воспроизведение файлов MIDI, сброс выходных устройств
- сброс выходных устройств
- Цифровой интерфейс MIDI, выходные устройства
- MIDI (цифровой интерфейс музыкального инструмента), выходные устройства
- Воспроизведение файлов MIDI, выходных устройств
- Устройства вывода MIDI
- ЕОКС (конец монопольного доступа)
- конец монопольного доступа (ЕОКС)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336876"
---
# <a name="resetting-midi-output"></a><span data-ttu-id="cd4aa-113">Сброс выходных данных MIDI</span><span class="sxs-lookup"><span data-stu-id="cd4aa-113">Resetting MIDI Output</span></span>

<span data-ttu-id="cd4aa-114">Функция [**мидиаутресет**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) отключает все заметки на всех каналах MIDI для УКАЗАННОГО устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-114">The [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) function turns off all notes on all MIDI channels for a specified MIDI device.</span></span> <span data-ttu-id="cd4aa-115">Затем функция помечает все ожидающие системные буферы как выполненные и возвращает их приложению.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-115">Then, the function marks any pending system-exclusive buffers as done and returns them to the application.</span></span> <span data-ttu-id="cd4aa-116">Эта функция может быть полезной в приложении, которое использует выходные данные MIDI, чтобы предоставить пользователю возможность сбрасывать выходные данные MIDI.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-116">This function can be useful in an application that uses MIDI output to provide the user with the ability to reset MIDI output.</span></span>

> [!Note]  
> <span data-ttu-id="cd4aa-117">Завершение безсистемного сообщения без отправки ЕОКС (исключающий) байт может привести к проблемам с принимающим устройством.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-117">Terminating a system-exclusive message without sending an EOX (end-of-exclusive) byte can cause problems for the receiving device.</span></span> <span data-ttu-id="cd4aa-118">Функция **мидиаутресет** не ОТПРАВЛЯЕТ байт еокс, когда он завершает сообщение, исключающий систему, потому что приложения отвечают за это.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-118">The **midiOutReset** function does not send an EOX byte when it terminates a system-exclusive message, because applications are responsible for doing this.</span></span>

 

 

 