---
title: О таймерах мультимедиа
description: О таймерах мультимедиа
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Мультимедиа Windows, таймеры
- мультимедиа, таймеры
- входные данные мультимедиа, таймеры
- Таймеры мультимедиа, сведения
- таймеры, сведения
- Таймеры мультимедиа, планирование событий
- таймеры, события планирования
- Планирование событий таймера
- время высокого разрешения
- Функция Сеттимер
- Функция сбой createwaitabletimer
- Сообщения WM_TIMER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069941"
---
# <a name="about-multimedia-timers"></a><span data-ttu-id="d3249-115">О таймерах мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d3249-115">About Multimedia Timers</span></span>

<span data-ttu-id="d3249-116">Службы таймера мультимедиа позволяют приложениям планировать события таймера с наибольшим разрешением (или точностью), возможным для аппаратной платформы.</span><span class="sxs-lookup"><span data-stu-id="d3249-116">Multimedia timer services allow applications to schedule timer events with the greatest resolution (or accuracy) possible for the hardware platform.</span></span> <span data-ttu-id="d3249-117">Эти службы таймера мультимедиа позволяют планировать события таймера с более высоким разрешением, чем другие службы таймера.</span><span class="sxs-lookup"><span data-stu-id="d3249-117">These multimedia timer services allow you to schedule timer events at a higher resolution than other timer services.</span></span>

<span data-ttu-id="d3249-118">Эти службы таймера полезны для приложений, которые требуют времени высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="d3249-118">These timer services are useful for applications that demand high-resolution timing.</span></span> <span data-ttu-id="d3249-119">Например, секвенсору MIDI требуется таймер высокого разрешения, так как он должен поддерживать скорость событий MIDI в рамках разрешения 1 миллисекунды.</span><span class="sxs-lookup"><span data-stu-id="d3249-119">For example, a MIDI sequencer requires a high-resolution timer because it must maintain the pace of MIDI events within a resolution of 1 millisecond.</span></span>

<span data-ttu-id="d3249-120">Приложения, для которых не используется синхронизация с высоким разрешением, должны использовать функцию [сеттимер](/windows/win32/api/winuser/nf-winuser-settimer) вместо служб таймера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d3249-120">Applications that do not use high-resolution timing should use the [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) function instead of multimedia timer services.</span></span> <span data-ttu-id="d3249-121">Службы таймера, предоставляемые **сеттимер** POST WM messages в очередь сообщений, а службы таймера мультимедиа вызывают функцию обратного вызова. [ \_](../winmsg/wm-timer.md)</span><span class="sxs-lookup"><span data-stu-id="d3249-121">The timer services provided by **SetTimer** post [WM\_TIMER](../winmsg/wm-timer.md) messages to a message queue, while the multimedia timer services call a callback function.</span></span> <span data-ttu-id="d3249-122">Приложения, которым требуется таймер ожидания, должны использовать функцию [сбой createwaitabletimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) .</span><span class="sxs-lookup"><span data-stu-id="d3249-122">Applications that want a waitable timer should use the [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) function.</span></span>

 

 