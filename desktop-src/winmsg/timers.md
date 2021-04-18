---
description: В этом разделе обсуждаются таймеры. Таймер — это внутренняя подпрограммы, которая многократно измеряет указанный интервал в миллисекундах.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Таймеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703131"
---
# <a name="timers"></a><span data-ttu-id="74615-104">Таймеры</span><span class="sxs-lookup"><span data-stu-id="74615-104">Timers</span></span>

<span data-ttu-id="74615-105">Таймер — это внутренняя подпрограммы, которая многократно измеряет указанный интервал в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="74615-105">A timer is an internal routine that repeatedly measures a specified interval, in milliseconds.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="74615-106">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="74615-106">In This Section</span></span>



| <span data-ttu-id="74615-107">Имя</span><span class="sxs-lookup"><span data-stu-id="74615-107">Name</span></span>                                   | <span data-ttu-id="74615-108">Описание</span><span class="sxs-lookup"><span data-stu-id="74615-108">Description</span></span>                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74615-109">О таймерах</span><span class="sxs-lookup"><span data-stu-id="74615-109">About Timers</span></span>](about-timers.md)       | <span data-ttu-id="74615-110">Описывает создание, определение, установку и удаление таймеров.</span><span class="sxs-lookup"><span data-stu-id="74615-110">Describes how to create, identify, set, and delete timers.</span></span><br/>                                                     |
| [<span data-ttu-id="74615-111">Использование таймеров</span><span class="sxs-lookup"><span data-stu-id="74615-111">Using Timers</span></span>](using-timers.md)       | <span data-ttu-id="74615-112">Описывает создание и удаление таймеров и использование таймера для перехвата входных данных мыши через определенные интервалы.</span><span class="sxs-lookup"><span data-stu-id="74615-112">Discusses how to create and destroy timers, and how to use a timer to trap mouse input at specified intervals.</span></span><br/> |
| [<span data-ttu-id="74615-113">Справочник по таймеру</span><span class="sxs-lookup"><span data-stu-id="74615-113">Timer Reference</span></span>](timer-reference.md) | <span data-ttu-id="74615-114">Содержит справочник по API.</span><span class="sxs-lookup"><span data-stu-id="74615-114">Contains the API reference.</span></span><br/>                                                                                    |



 

### <a name="timer-functions"></a><span data-ttu-id="74615-115">Функции таймера</span><span class="sxs-lookup"><span data-stu-id="74615-115">Timer Functions</span></span>



| <span data-ttu-id="74615-116">Имя</span><span class="sxs-lookup"><span data-stu-id="74615-116">Name</span></span>                           | <span data-ttu-id="74615-117">Описание</span><span class="sxs-lookup"><span data-stu-id="74615-117">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74615-118">**киллтимер**</span><span class="sxs-lookup"><span data-stu-id="74615-118">**KillTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-killtimer) | <span data-ttu-id="74615-119">Уничтожает указанный таймер.</span><span class="sxs-lookup"><span data-stu-id="74615-119">Destroys the specified timer.</span></span> <br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="74615-120">**сеттимер**</span><span class="sxs-lookup"><span data-stu-id="74615-120">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)   | <span data-ttu-id="74615-121">Создает таймер с указанным значением времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="74615-121">Creates a timer with the specified time-out value.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="74615-122">*тимерпрок*</span><span class="sxs-lookup"><span data-stu-id="74615-122">*TimerProc*</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)   | <span data-ttu-id="74615-123">Определяемая приложением функция обратного вызова, которая обрабатывает сообщения [**\_ таймера WM**](wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="74615-123">An application-defined callback function that processes [**WM\_TIMER**](wm-timer.md) messages.</span></span> <span data-ttu-id="74615-124">Тип **тимерпрок** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="74615-124">The **TIMERPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="74615-125">[*Тимерпрок*](/windows/win32/api/winuser/nc-winuser-timerproc) — это заполнитель для имени определяемой приложением функции.</span><span class="sxs-lookup"><span data-stu-id="74615-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) is a placeholder for the application-defined function name.</span></span> <br/> |



 

### <a name="timer-notifications"></a><span data-ttu-id="74615-126">Уведомления таймера</span><span class="sxs-lookup"><span data-stu-id="74615-126">Timer Notifications</span></span>



| <span data-ttu-id="74615-127">Имя</span><span class="sxs-lookup"><span data-stu-id="74615-127">Name</span></span>                          | <span data-ttu-id="74615-128">Описание</span><span class="sxs-lookup"><span data-stu-id="74615-128">Description</span></span>                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74615-129">**\_таймер WM**</span><span class="sxs-lookup"><span data-stu-id="74615-129">**WM\_TIMER**</span></span>](wm-timer.md) | <span data-ttu-id="74615-130">Отправляется в очередь сообщений установки потока по истечении времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="74615-130">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="74615-131">Сообщение отправляется функцией [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . [](/windows/win32/api/winuser/nf-winuser-getmessage)</span><span class="sxs-lookup"><span data-stu-id="74615-131">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <br/> |



 

 

 
