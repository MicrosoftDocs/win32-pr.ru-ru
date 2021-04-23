---
title: Средство сопоставления MIDI и Windows
description: Средство сопоставления MIDI и Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- Цифровой интерфейс MIDI, сопоставитель MIDI
- MIDI (цифровой интерфейс музыкального инструмента), сопоставитель MIDI
- Сопоставитель MIDI, архитектура
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069937"
---
# <a name="the-midi-mapper-and-windows"></a><span data-ttu-id="0ebd2-106">Средство сопоставления MIDI и Windows</span><span class="sxs-lookup"><span data-stu-id="0ebd2-106">The MIDI Mapper and Windows</span></span>

<span data-ttu-id="0ebd2-107">Средство сопоставления MIDI входит в состав системного программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-107">The MIDI Mapper is part of the system software.</span></span> <span data-ttu-id="0ebd2-108">На следующем рисунке показано, как средство сопоставления MIDI относится к другим элементам служб аудио.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-108">The following illustration shows how the MIDI Mapper relates to other elements of the audio services.</span></span>

![отношение сопоставителя MIDI к другим элементам образа служб аудио](images/mmap-a01.gif)

<span data-ttu-id="0ebd2-110">С точки зрения приложения средство сопоставления MIDI выглядит как другое устройство вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-110">From the viewpoint of an application, the MIDI Mapper looks like another MIDI output device.</span></span> <span data-ttu-id="0ebd2-111">Средство сопоставления MIDI получает сообщения, отправленные им с помощью функций вывода MIDI нижнего уровня [**мидиаутшортмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) и [**мидиаутлонгмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span><span class="sxs-lookup"><span data-stu-id="0ebd2-111">The MIDI Mapper receives messages sent to it by the low-level MIDI output functions [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) and [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span></span> <span data-ttu-id="0ebd2-112">Средство сопоставления MIDI изменяет эти сообщения и перенаправляет их на устройство вывода MIDI в соответствии с текущей картой установки MIDI.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-112">The MIDI Mapper modifies these messages and redirects them to a MIDI output device according to the current MIDI setup map.</span></span> <span data-ttu-id="0ebd2-113">Текущая схема установки MIDI выбирается пользователем с помощью параметра панели управления MIDI.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-113">The current MIDI setup map is selected by the user by means of the MIDI Control Panel option.</span></span> <span data-ttu-id="0ebd2-114">Только пользователь может выбрать текущую карту установки. приложения не могут изменить текущую схему установки.</span><span class="sxs-lookup"><span data-stu-id="0ebd2-114">Only the user can select the current setup map; applications cannot change the current setup map.</span></span>

 

 