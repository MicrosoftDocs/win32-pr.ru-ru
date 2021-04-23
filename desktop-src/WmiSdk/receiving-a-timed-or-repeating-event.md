---
description: Событие времени или повторяющегося события — это событие, возникающее в определенный момент времени, или несколько раз через регулярные интервалы. Например, событие может произойти в полночь только в 2 декабря 2015 г. или раз в неделю в вторники в 2:31 PM.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Получение события времени или повтора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263822"
---
# <a name="receiving-a-timed-or-repeating-event"></a><span data-ttu-id="10bb2-104">Получение события времени или повтора</span><span class="sxs-lookup"><span data-stu-id="10bb2-104">Receiving a Timed or Repeating Event</span></span>

<span data-ttu-id="10bb2-105">Событие времени или повторяющегося события — это событие, возникающее в определенный момент времени, или несколько раз через регулярные интервалы.</span><span class="sxs-lookup"><span data-stu-id="10bb2-105">A timed or repeating event is an event that occurs at one specific time and date, or repeatedly at regular intervals.</span></span> <span data-ttu-id="10bb2-106">Например, событие может произойти в полночь только в 2 декабря 2015 г. или раз в неделю в вторники в 2:31 PM.</span><span class="sxs-lookup"><span data-stu-id="10bb2-106">For example, an event can occur at midnight on only December 2, 2015, or one time each week on Tuesdays at 2:31 PM.</span></span>

<span data-ttu-id="10bb2-107">В следующей таблице перечислены различные классы, которые используются для создания события с временным или повторяющимся событием.</span><span class="sxs-lookup"><span data-stu-id="10bb2-107">The following table lists the different classes that are used to create a timed or repeating event.</span></span>



| <span data-ttu-id="10bb2-108">Класс</span><span class="sxs-lookup"><span data-stu-id="10bb2-108">Class</span></span>                                                                                            | <span data-ttu-id="10bb2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="10bb2-109">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10bb2-110">[**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) или [ **\_ утктиме Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span><span class="sxs-lookup"><span data-stu-id="10bb2-110">[**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span></span> | <span data-ttu-id="10bb2-111">Стандартная модель событий Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="10bb2-111">Standard Microsoft event model.</span></span><br/> <span data-ttu-id="10bb2-112">Дополнительные сведения см. в разделе [Создание события таймера с помощью Win32 \_ LocalTime или Win32 \_ утктиме](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span><span class="sxs-lookup"><span data-stu-id="10bb2-112">For more information, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span><br/> |
| [<span data-ttu-id="10bb2-113">**\_\_тимеринструктион**</span><span class="sxs-lookup"><span data-stu-id="10bb2-113">**\_\_TimerInstruction**</span></span>](--timerinstruction.md)                                               | <span data-ttu-id="10bb2-114">Устаревший метод.</span><span class="sxs-lookup"><span data-stu-id="10bb2-114">Legacy technique.</span></span><br/> <span data-ttu-id="10bb2-115">Дополнительные сведения см. [в разделе Создание события таймера с помощью \_ тимеринструктион](creating-a-timer-event-with---timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="10bb2-115">For more information, see [Creating a Timer Event with \_TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span></span><br/>                                             |



 

<span data-ttu-id="10bb2-116">Если необходимо запланировать выполнение задачи или задания в определенное время или несколько раз, используйте класс [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) и его методы.</span><span class="sxs-lookup"><span data-stu-id="10bb2-116">If you want to schedule a task or job to occur at a specific time or repeatedly, use the [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) class and its methods.</span></span> <span data-ttu-id="10bb2-117">Этот класс представляет задание, созданное с помощью команды AT в командном окне, из **запуска** и затем **запуска**, а также из **запланированных задач** на **панели управления**.</span><span class="sxs-lookup"><span data-stu-id="10bb2-117">This class represents a job created with the AT command in a command window from **Start** and then **Run**, or from the **Scheduled Tasks** in **Control Panel**.</span></span>

 

