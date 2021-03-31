---
title: I (планировщик задач)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8492f707a171c6811b4702d2a07de47d29482a8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533644"
---
# <a name="i-task-scheduler"></a><span data-ttu-id="679ea-103">I (планировщик задач)</span><span class="sxs-lookup"><span data-stu-id="679ea-103">I (Task Scheduler)</span></span>

<span data-ttu-id="679ea-104">A B C D [E](e.md) F G р. J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="679ea-104">A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="679ea-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**условия простоя**</span><span class="sxs-lookup"><span data-stu-id="679ea-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**idle conditions**</span></span>
</dt> <dd>

<span data-ttu-id="679ea-106">Период времени, в течение которого на компьютере нет вводимых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="679ea-106">A period of time in which there is no user input on the computer.</span></span> <span data-ttu-id="679ea-107">Условия простоя связаны с запланированным временем начала задачи.</span><span class="sxs-lookup"><span data-stu-id="679ea-107">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="679ea-108">Эти условия задаются путем вызова [**исчедуледворкитем:: сетфлагс**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span><span class="sxs-lookup"><span data-stu-id="679ea-108">These conditions are set by calling [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span></span>

</dd> <dt>

<span data-ttu-id="679ea-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**триггеры бездействия**</span><span class="sxs-lookup"><span data-stu-id="679ea-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**idle triggers**</span></span>
</dt> <dd>

<span data-ttu-id="679ea-110">Триггер на основе события, который срабатывает, когда компьютер переходит в состояние бездействия в течение определенного промежутка времени.</span><span class="sxs-lookup"><span data-stu-id="679ea-110">An event-based trigger that is fired when the computer becomes idle for a specific amount of time.</span></span>

<span data-ttu-id="679ea-111">Триггеры простоя создаются путем задания \_ для элемента типа триггера задачи в \_ структуре [**\_ триггера**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) задания \_ \_ триггера события \_ во \_ время бездействия.</span><span class="sxs-lookup"><span data-stu-id="679ea-111">Idle triggers are created by setting the TASK\_TRIGGER\_TYPE member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure to TASK\_EVENT\_TRIGGER\_ON\_IDLE.</span></span>

</dd> <dt>

<span data-ttu-id="679ea-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**время ожидания простоя**</span><span class="sxs-lookup"><span data-stu-id="679ea-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**idle wait time**</span></span>
</dt> <dd>

<span data-ttu-id="679ea-113">Интервал времени (в минутах), используемый триггером простоя или условием простоя.</span><span class="sxs-lookup"><span data-stu-id="679ea-113">The time interval (in minutes) used by an idle trigger or idle condition.</span></span> <span data-ttu-id="679ea-114">Триггеры бездействия — это триггеры на основе событий, которые не связаны с запланированным временем.</span><span class="sxs-lookup"><span data-stu-id="679ea-114">Idle triggers are event-based triggers that are not associated with a scheduled time.</span></span> <span data-ttu-id="679ea-115">Условия простоя связаны с запланированным временем начала задачи.</span><span class="sxs-lookup"><span data-stu-id="679ea-115">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="679ea-116">Время простоя задается вызовом [**исчедуледворкитем:: сетидлеваит**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span><span class="sxs-lookup"><span data-stu-id="679ea-116">The idle time is set by a call to [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span></span>

</dd> </dl>

 

 




