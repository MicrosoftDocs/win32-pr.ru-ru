---
title: Операции с событиями таймера
description: Операции с событиями таймера
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- Таймеры мультимедиа, события
- таймеры, события
- Функция Тимесетевент
- Функция Тимекиллевент
- Запуск событий таймера
- события с одним таймером
- периодические события таймера
- Отмена событий таймера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789750"
---
# <a name="timer-event-operations"></a><span data-ttu-id="7d145-111">Операции с событиями таймера</span><span class="sxs-lookup"><span data-stu-id="7d145-111">Timer Event Operations</span></span>

<span data-ttu-id="7d145-112">После установки разрешения таймера приложения можно запустить события таймера с помощью функции [**тимесетевент**](/previous-versions//dd757634(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7d145-112">After you have established your application's timer resolution, you can start timer events by using the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function.</span></span> <span data-ttu-id="7d145-113">Эта функция возвращает идентификатор таймера, который можно использовать для отмены или идентификации событий таймера.</span><span class="sxs-lookup"><span data-stu-id="7d145-113">This function returns a timer identifier that can be used to stop or identify timer events.</span></span> <span data-ttu-id="7d145-114">Одним из параметров функции является адрес функции обратного вызова [**тимепрок**](/previous-versions//dd757631(v=vs.85)) , которая вызывается при выполнении события Timer.</span><span class="sxs-lookup"><span data-stu-id="7d145-114">One of the function's parameters is the address of a [**TimeProc**](/previous-versions//dd757631(v=vs.85)) callback function that is called when the timer event takes place.</span></span>

<span data-ttu-id="7d145-115">Существует два типа событий таймера: *один* и *периодически*.</span><span class="sxs-lookup"><span data-stu-id="7d145-115">There are two types of timer events: *single* and *periodic*.</span></span> <span data-ttu-id="7d145-116">Одно событие таймера происходит один раз после указанного числа миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="7d145-116">A single timer event occurs once, after a specified number of milliseconds.</span></span> <span data-ttu-id="7d145-117">Периодическое событие таймера возникает каждый раз, когда истечет указанное число миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="7d145-117">A periodic timer event occurs every time a specified number of milliseconds elapses.</span></span> <span data-ttu-id="7d145-118">Интервал между периодическими событиями называется *задержкой события*.</span><span class="sxs-lookup"><span data-stu-id="7d145-118">The interval between periodic events is called an *event delay*.</span></span> <span data-ttu-id="7d145-119">Периодические события таймера с задержкой события 10 миллисекунд или менее потребляют значительную часть ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="7d145-119">Periodic timer events with an event delay of 10 milliseconds or less consume a significant portion of CPU resources.</span></span>

<span data-ttu-id="7d145-120">Связь между разрешением события таймера и длительностью задержки события важна в событиях таймера.</span><span class="sxs-lookup"><span data-stu-id="7d145-120">The relationship between the resolution of a timer event and the length of the event delay is important in timer events.</span></span> <span data-ttu-id="7d145-121">Например, если задать разрешение 5 и задержку события 100, службы таймера будут уведомлять функцию обратного вызова через интервал от 95 до 105 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="7d145-121">For example, if you specify a resolution of 5 and an event delay of 100, the timer services notify the callback function after an interval ranging from 95 to 105 milliseconds.</span></span>

<span data-ttu-id="7d145-122">Активное событие таймера можно отменить в любое время с помощью функции [**тимекиллевент**](/previous-versions//dd757630(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7d145-122">You can cancel an active timer event at any time by using the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function.</span></span> <span data-ttu-id="7d145-123">Не забудьте отменить все необработанные таймеры, прежде чем освободить память, содержащую функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7d145-123">Be sure to cancel any outstanding timers before freeing the memory containing the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="7d145-124">Таймер мультимедиа выполняется в собственном потоке.</span><span class="sxs-lookup"><span data-stu-id="7d145-124">The multimedia timer runs in its own thread.</span></span>

 

 

 