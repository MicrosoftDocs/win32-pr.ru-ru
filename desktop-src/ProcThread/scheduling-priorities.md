---
description: Потоки планируются для запуска на основе их приоритета планирования.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Приоритеты планирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673743"
---
# <a name="scheduling-priorities"></a><span data-ttu-id="afe06-103">Приоритеты планирования</span><span class="sxs-lookup"><span data-stu-id="afe06-103">Scheduling Priorities</span></span>

<span data-ttu-id="afe06-104">Потоки планируются для запуска на основе их *приоритета планирования*.</span><span class="sxs-lookup"><span data-stu-id="afe06-104">Threads are scheduled to run based on their *scheduling priority*.</span></span> <span data-ttu-id="afe06-105">Каждому потоку назначается приоритет планирования.</span><span class="sxs-lookup"><span data-stu-id="afe06-105">Each thread is assigned a scheduling priority.</span></span> <span data-ttu-id="afe06-106">Уровни приоритета находятся в диапазоне от нуля (самый низкий приоритет) до 31 (наивысший приоритет).</span><span class="sxs-lookup"><span data-stu-id="afe06-106">The priority levels range from zero (lowest priority) to 31 (highest priority).</span></span> <span data-ttu-id="afe06-107">Только поток нулевой страницы может иметь приоритет, равный нулю.</span><span class="sxs-lookup"><span data-stu-id="afe06-107">Only the zero-page thread can have a priority of zero.</span></span> <span data-ttu-id="afe06-108">(Поток нулевой страницы — это системный поток, ответственный за обнуление свободных страниц при отсутствии других потоков, которые необходимо выполнить.)</span><span class="sxs-lookup"><span data-stu-id="afe06-108">(The zero-page thread is a system thread responsible for zeroing any free pages when there are no other threads that need to run.)</span></span>

<span data-ttu-id="afe06-109">Система рассматривает все потоки с одинаковым приоритетом, равным.</span><span class="sxs-lookup"><span data-stu-id="afe06-109">The system treats all threads with the same priority as equal.</span></span> <span data-ttu-id="afe06-110">Система назначает временные срезы циклическим перебору для всех потоков с наивысшим приоритетом.</span><span class="sxs-lookup"><span data-stu-id="afe06-110">The system assigns time slices in a round-robin fashion to all threads with the highest priority.</span></span> <span data-ttu-id="afe06-111">Если ни один из этих потоков не готов к выполнению, система назначает временные срезы циклическим перебору для всех потоков со следующим высшим приоритетом.</span><span class="sxs-lookup"><span data-stu-id="afe06-111">If none of these threads are ready to run, the system assigns time slices in a round-robin fashion to all threads with the next highest priority.</span></span> <span data-ttu-id="afe06-112">Если поток с более высоким приоритетом станет доступным для выполнения, система прекратит выполнение потока с низким приоритетом (не позволяя ему завершить работу с его временным срезом) и назначает полный временной срез для потока с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="afe06-112">If a higher-priority thread becomes available to run, the system ceases to execute the lower-priority thread (without allowing it to finish using its time slice) and assigns a full time slice to the higher-priority thread.</span></span> <span data-ttu-id="afe06-113">Дополнительные сведения см. в разделе [контекстные переключения](context-switches.md).</span><span class="sxs-lookup"><span data-stu-id="afe06-113">For more information, see [Context Switches](context-switches.md).</span></span>

<span data-ttu-id="afe06-114">Приоритет каждого потока определяется следующими критериями.</span><span class="sxs-lookup"><span data-stu-id="afe06-114">The priority of each thread is determined by the following criteria:</span></span>

-   <span data-ttu-id="afe06-115">Класс приоритета его процесса</span><span class="sxs-lookup"><span data-stu-id="afe06-115">The priority class of its process</span></span>
-   <span data-ttu-id="afe06-116">Уровень приоритета потока в классе приоритета его процесса</span><span class="sxs-lookup"><span data-stu-id="afe06-116">The priority level of the thread within the priority class of its process</span></span>

<span data-ttu-id="afe06-117">Класс приоритета и уровень приоритета объединяются для формирования *базового приоритета* потока.</span><span class="sxs-lookup"><span data-stu-id="afe06-117">The priority class and priority level are combined to form the *base priority* of a thread.</span></span> <span data-ttu-id="afe06-118">Сведения о динамическом приоритете потока см. в разделе [повышение приоритета](priority-boosts.md).</span><span class="sxs-lookup"><span data-stu-id="afe06-118">For information on the dynamic priority of a thread, see [Priority Boosts](priority-boosts.md).</span></span>

## <a name="priority-class"></a><span data-ttu-id="afe06-119">Класс Priority</span><span class="sxs-lookup"><span data-stu-id="afe06-119">Priority Class</span></span>

<span data-ttu-id="afe06-120">Каждый процесс принадлежит одному из следующих классов приоритета:</span><span class="sxs-lookup"><span data-stu-id="afe06-120">Each process belongs to one of the following priority classes:</span></span><dl> <span data-ttu-id="afe06-121">\_класс приоритета простоя \_</span><span class="sxs-lookup"><span data-stu-id="afe06-121">IDLE\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="afe06-122">НИЖЕ \_ обычного \_ класса приоритета \_</span><span class="sxs-lookup"><span data-stu-id="afe06-122">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="afe06-123">\_класс обычного приоритета \_</span><span class="sxs-lookup"><span data-stu-id="afe06-123">NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="afe06-124">ВЫШЕ \_ класса с нормальным \_ приоритетом \_</span><span class="sxs-lookup"><span data-stu-id="afe06-124">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="afe06-125">класс с высоким \_ приоритетом \_</span><span class="sxs-lookup"><span data-stu-id="afe06-125">HIGH\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="afe06-126">\_класс приоритета в режиме реального времени \_</span><span class="sxs-lookup"><span data-stu-id="afe06-126">REALTIME\_PRIORITY\_CLASS</span></span>  
</dl>

<span data-ttu-id="afe06-127">По умолчанию класс приоритета процесса — это класс с НОРМАЛЬным \_ приоритетом \_ .</span><span class="sxs-lookup"><span data-stu-id="afe06-127">By default, the priority class of a process is NORMAL\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="afe06-128">Используйте функцию [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , чтобы указать класс приоритета дочернего процесса при его создании.</span><span class="sxs-lookup"><span data-stu-id="afe06-128">Use the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function to specify the priority class of a child process when you create it.</span></span> <span data-ttu-id="afe06-129">Если вызывающий процесс является \_ классом приоритета простоя \_ или ниже \_ обычного \_ класса приоритета \_ , новый процесс будет наследовать этот класс.</span><span class="sxs-lookup"><span data-stu-id="afe06-129">If the calling process is IDLE\_PRIORITY\_CLASS or BELOW\_NORMAL\_PRIORITY\_CLASS, the new process will inherit this class.</span></span> <span data-ttu-id="afe06-130">Используйте функцию [**жетприоритикласс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) для определения текущего класса приоритета процесса и функции [**сетприоритикласс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) , чтобы изменить класс приоритета процесса.</span><span class="sxs-lookup"><span data-stu-id="afe06-130">Use the [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) function to determine the current priority class of a process and the [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) function to change the priority class of a process.</span></span>

<span data-ttu-id="afe06-131">Процессы, выполняющие мониторинг системы, такие как экранные заставки или приложения, которые периодически обновляют отображение, должны использовать \_ класс приоритета простоя \_ .</span><span class="sxs-lookup"><span data-stu-id="afe06-131">Processes that monitor the system, such as screen savers or applications that periodically update a display, should use IDLE\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="afe06-132">Это препятствует потокам этого процесса, которые не имеют высокого приоритета, от влияния на потоки с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="afe06-132">This prevents the threads of this process, which do not have high priority, from interfering with higher priority threads.</span></span>

<span data-ttu-id="afe06-133">Используйте \_ класс с высоким приоритетом \_ с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="afe06-133">Use HIGH\_PRIORITY\_CLASS with care.</span></span> <span data-ttu-id="afe06-134">Если поток выполняется с наивысшим приоритетом для расширенных периодов, другие потоки в системе не будут получать процессорное время.</span><span class="sxs-lookup"><span data-stu-id="afe06-134">If a thread runs at the highest priority level for extended periods, other threads in the system will not get processor time.</span></span> <span data-ttu-id="afe06-135">Если несколько потоков одновременно устанавливаются с высоким приоритетом, потоки теряют свои эффективность.</span><span class="sxs-lookup"><span data-stu-id="afe06-135">If several threads are set at high priority at the same time, the threads lose their effectiveness.</span></span> <span data-ttu-id="afe06-136">Класс с высоким приоритетом должен быть зарезервирован для потоков, которые должны отвечать на критические по времени события.</span><span class="sxs-lookup"><span data-stu-id="afe06-136">The high-priority class should be reserved for threads that must respond to time-critical events.</span></span> <span data-ttu-id="afe06-137">Если приложение выполняет одну задачу, для которой требуется класс с высоким приоритетом, в то время как остальные задачи имеют нормальный приоритет, используйте [**сетприоритикласс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) , чтобы временно вызвать класс приоритета приложения. затем сократите его после завершения задачи, критичной по времени.</span><span class="sxs-lookup"><span data-stu-id="afe06-137">If your application performs one task that requires the high-priority class while the rest of its tasks are normal priority, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) to raise the priority class of the application temporarily; then reduce it after the time-critical task has been completed.</span></span> <span data-ttu-id="afe06-138">Другая стратегия состоит в том, чтобы создать высокоприоритетный процесс, в большинстве случаев блокирующий все его потоки, выводят потоки только при необходимости выполнения критических задач.</span><span class="sxs-lookup"><span data-stu-id="afe06-138">Another strategy is to create a high-priority process that has all of its threads blocked most of the time, awakening threads only when critical tasks are needed.</span></span> <span data-ttu-id="afe06-139">Важно отметить, что поток с высоким приоритетом должен выполняться в течение короткого промежутка времени и только тогда, когда он имеет критическую для выполнения работу.</span><span class="sxs-lookup"><span data-stu-id="afe06-139">The important point is that a high-priority thread should execute for a brief time, and only when it has time-critical work to perform.</span></span>

<span data-ttu-id="afe06-140">Почти никогда не следует использовать \_ класс приоритета реального времени \_ , так как это прерывает системные потоки, управляющие вводом мыши, вводом с клавиатуры и фоновым сбросом дисков.</span><span class="sxs-lookup"><span data-stu-id="afe06-140">You should almost never use REALTIME\_PRIORITY\_CLASS, because this interrupts system threads that manage mouse input, keyboard input, and background disk flushing.</span></span> <span data-ttu-id="afe06-141">Этот класс может быть пригоден для приложений, которые «говорите» непосредственно на оборудование или выполняют короткие задачи, которые должны иметь ограниченные перерывы.</span><span class="sxs-lookup"><span data-stu-id="afe06-141">This class can be appropriate for applications that "talk" directly to hardware or that perform brief tasks that should have limited interruptions.</span></span>

## <a name="priority-level"></a><span data-ttu-id="afe06-142">Уровень приоритета</span><span class="sxs-lookup"><span data-stu-id="afe06-142">Priority Level</span></span>

<span data-ttu-id="afe06-143">Ниже приведены уровни приоритета в каждом классе приоритета.</span><span class="sxs-lookup"><span data-stu-id="afe06-143">The following are priority levels within each priority class:</span></span><dl> <span data-ttu-id="afe06-144">приоритет потока — \_ \_ бездействие</span><span class="sxs-lookup"><span data-stu-id="afe06-144">THREAD\_PRIORITY\_IDLE</span></span>  
<span data-ttu-id="afe06-145">\_ \_ самый низкий приоритет потока</span><span class="sxs-lookup"><span data-stu-id="afe06-145">THREAD\_PRIORITY\_LOWEST</span></span>  
<span data-ttu-id="afe06-146">\_приоритет потока \_ ниже \_ обычного</span><span class="sxs-lookup"><span data-stu-id="afe06-146">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  
<span data-ttu-id="afe06-147">приоритет потока — \_ \_ нормальный</span><span class="sxs-lookup"><span data-stu-id="afe06-147">THREAD\_PRIORITY\_NORMAL</span></span>  
<span data-ttu-id="afe06-148">\_приоритет потока \_ выше \_ обычного</span><span class="sxs-lookup"><span data-stu-id="afe06-148">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  
<span data-ttu-id="afe06-149">приоритет потока — \_ \_ самый высокий</span><span class="sxs-lookup"><span data-stu-id="afe06-149">THREAD\_PRIORITY\_HIGHEST</span></span>  
<span data-ttu-id="afe06-150">\_ \_ критическое время ПРИОРИТЕТа потока \_</span><span class="sxs-lookup"><span data-stu-id="afe06-150">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span>  
</dl>

<span data-ttu-id="afe06-151">Все потоки создаются с использованием \_ обычного приоритета потока \_ .</span><span class="sxs-lookup"><span data-stu-id="afe06-151">All threads are created using THREAD\_PRIORITY\_NORMAL.</span></span> <span data-ttu-id="afe06-152">Это означает, что приоритет потока аналогичен классу приоритета процесса.</span><span class="sxs-lookup"><span data-stu-id="afe06-152">This means that the thread priority is the same as the process priority class.</span></span> <span data-ttu-id="afe06-153">После создания потока используйте функцию [**сетсреадприорити**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) , чтобы изменить ее приоритет относительно других потоков в процессе.</span><span class="sxs-lookup"><span data-stu-id="afe06-153">After you create a thread, use the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function to adjust its priority relative to other threads in the process.</span></span>

<span data-ttu-id="afe06-154">Типичной стратегией является использование \_ приоритета потока \_ выше \_ обычного или \_ приоритета потока \_ для входного потока процесса, чтобы обеспечить реагирование приложения на запросы пользователя.</span><span class="sxs-lookup"><span data-stu-id="afe06-154">A typical strategy is to use THREAD\_PRIORITY\_ABOVE\_NORMAL or THREAD\_PRIORITY\_HIGHEST for the process's input thread, to ensure that the application is responsive to the user.</span></span> <span data-ttu-id="afe06-155">Фоновым потокам, в частности, которые являются ресурсоемкими, можно задать \_ приоритет потока \_ ниже \_ обычного или \_ приоритета потока \_ , чтобы гарантировать, что при необходимости они могут быть вытеснены.</span><span class="sxs-lookup"><span data-stu-id="afe06-155">Background threads, particularly those that are processor intensive, can be set to THREAD\_PRIORITY\_BELOW\_NORMAL or THREAD\_PRIORITY\_LOWEST, to ensure that they can be preempted when necessary.</span></span> <span data-ttu-id="afe06-156">Однако при наличии потока, ожидающего другого потока с более низким приоритетом для выполнения некоторой задачи, не забудьте заблокировать выполнение ожидающего потока с высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="afe06-156">However, if you have a thread waiting for another thread with a lower priority to complete some task, be sure to block the execution of the waiting high-priority thread.</span></span> <span data-ttu-id="afe06-157">Для этого используйте [функцию Wait](../sync/wait-functions.md), [критическую секцию](../sync/critical-section-objects.md)или функцию [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) , [**слипекс**](/windows/win32/api/synchapi/nf-synchapi-sleepex)или [**свитчтосреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) .</span><span class="sxs-lookup"><span data-stu-id="afe06-157">To do this, use a [wait function](../sync/wait-functions.md), [critical section](../sync/critical-section-objects.md), or the [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function, [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function.</span></span> <span data-ttu-id="afe06-158">Это предпочтительнее, чтобы поток выполнял цикл.</span><span class="sxs-lookup"><span data-stu-id="afe06-158">This is preferable to having the thread execute a loop.</span></span> <span data-ttu-id="afe06-159">В противном случае процесс может привести к взаимоблокировке, так как не запланировано выполнение потока с более низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="afe06-159">Otherwise, the process may become deadlocked, because the thread with lower priority is never scheduled.</span></span>

<span data-ttu-id="afe06-160">Чтобы определить текущий уровень приоритета потока, используйте функцию [**жетсреадприорити**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) .</span><span class="sxs-lookup"><span data-stu-id="afe06-160">To determine the current priority level of a thread, use the [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) function.</span></span>

## <a name="base-priority"></a><span data-ttu-id="afe06-161">Базовый приоритет</span><span class="sxs-lookup"><span data-stu-id="afe06-161">Base Priority</span></span>

<span data-ttu-id="afe06-162">Класс приоритета процесса и уровень приоритета потока объединяются для формирования базового приоритета каждого потока.</span><span class="sxs-lookup"><span data-stu-id="afe06-162">The process priority class and thread priority level are combined to form the base priority of each thread.</span></span>

<span data-ttu-id="afe06-163">В следующей таблице показан базовый приоритет для сочетания класса приоритета процесса и значения приоритета потока.</span><span class="sxs-lookup"><span data-stu-id="afe06-163">The following table shows the base priority for combinations of process priority class and thread priority value.</span></span>


<table>
<tr>
<th colspan="2"><span data-ttu-id="afe06-164">Класс приоритета процесса</span><span class="sxs-lookup"><span data-stu-id="afe06-164">Process priority class</span></span></th>
<th><span data-ttu-id="afe06-165">Уровень приоритета потока</span><span class="sxs-lookup"><span data-stu-id="afe06-165">Thread priority level</span></span></th>
<th><span data-ttu-id="afe06-166">Базовый приоритет</span><span class="sxs-lookup"><span data-stu-id="afe06-166">Base priority</span></span></th>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="afe06-167">IDLE_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="afe06-167">IDLE_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="afe06-168">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="afe06-168">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="afe06-169">1</span><span class="sxs-lookup"><span data-stu-id="afe06-169">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-170">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="afe06-170">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="afe06-171">2</span><span class="sxs-lookup"><span data-stu-id="afe06-171">2</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-172">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-172">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-173">3</span><span class="sxs-lookup"><span data-stu-id="afe06-173">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-174">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-174">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-175">4</span><span class="sxs-lookup"><span data-stu-id="afe06-175">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-176">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-176">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-177">5</span><span class="sxs-lookup"><span data-stu-id="afe06-177">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-178">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="afe06-178">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="afe06-179">6</span><span class="sxs-lookup"><span data-stu-id="afe06-179">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-180">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="afe06-180">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="afe06-181">15</span><span class="sxs-lookup"><span data-stu-id="afe06-181">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="afe06-182">BELOW_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="afe06-182">BELOW_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="afe06-183">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="afe06-183">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="afe06-184">1</span><span class="sxs-lookup"><span data-stu-id="afe06-184">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-185">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="afe06-185">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="afe06-186">4</span><span class="sxs-lookup"><span data-stu-id="afe06-186">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-187">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-187">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-188">5</span><span class="sxs-lookup"><span data-stu-id="afe06-188">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-189">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-189">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-190">6</span><span class="sxs-lookup"><span data-stu-id="afe06-190">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-191">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-191">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-192">7</span><span class="sxs-lookup"><span data-stu-id="afe06-192">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-193">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="afe06-193">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="afe06-194">8</span><span class="sxs-lookup"><span data-stu-id="afe06-194">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-195">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="afe06-195">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="afe06-196">15</span><span class="sxs-lookup"><span data-stu-id="afe06-196">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="afe06-197">NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="afe06-197">NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="afe06-198">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="afe06-198">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="afe06-199">1</span><span class="sxs-lookup"><span data-stu-id="afe06-199">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-200">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="afe06-200">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="afe06-201">6</span><span class="sxs-lookup"><span data-stu-id="afe06-201">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-202">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-202">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-203">7</span><span class="sxs-lookup"><span data-stu-id="afe06-203">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-204">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-204">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-205">8</span><span class="sxs-lookup"><span data-stu-id="afe06-205">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-206">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-206">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-207">9</span><span class="sxs-lookup"><span data-stu-id="afe06-207">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-208">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="afe06-208">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="afe06-209">10</span><span class="sxs-lookup"><span data-stu-id="afe06-209">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-210">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="afe06-210">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="afe06-211">15</span><span class="sxs-lookup"><span data-stu-id="afe06-211">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="afe06-212">ABOVE_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="afe06-212">ABOVE_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="afe06-213">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="afe06-213">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="afe06-214">1</span><span class="sxs-lookup"><span data-stu-id="afe06-214">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-215">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="afe06-215">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="afe06-216">8</span><span class="sxs-lookup"><span data-stu-id="afe06-216">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-217">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-217">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-218">9</span><span class="sxs-lookup"><span data-stu-id="afe06-218">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-219">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-219">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-220">10</span><span class="sxs-lookup"><span data-stu-id="afe06-220">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-221">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-221">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-222">11</span><span class="sxs-lookup"><span data-stu-id="afe06-222">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-223">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="afe06-223">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="afe06-224">12</span><span class="sxs-lookup"><span data-stu-id="afe06-224">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-225">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="afe06-225">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="afe06-226">15</span><span class="sxs-lookup"><span data-stu-id="afe06-226">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="afe06-227">HIGH_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="afe06-227">HIGH_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="afe06-228">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="afe06-228">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="afe06-229">1</span><span class="sxs-lookup"><span data-stu-id="afe06-229">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-230">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="afe06-230">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="afe06-231">11</span><span class="sxs-lookup"><span data-stu-id="afe06-231">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-232">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-232">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-233">12</span><span class="sxs-lookup"><span data-stu-id="afe06-233">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-234">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-234">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-235">13</span><span class="sxs-lookup"><span data-stu-id="afe06-235">13</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-236">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-236">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-237">14</span><span class="sxs-lookup"><span data-stu-id="afe06-237">14</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-238">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="afe06-238">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="afe06-239">15</span><span class="sxs-lookup"><span data-stu-id="afe06-239">15</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-240">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="afe06-240">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="afe06-241">15</span><span class="sxs-lookup"><span data-stu-id="afe06-241">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="afe06-242">REALTIME_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="afe06-242">REALTIME_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="afe06-243">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="afe06-243">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="afe06-244">16</span><span class="sxs-lookup"><span data-stu-id="afe06-244">16</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-245">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="afe06-245">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="afe06-246">22</span><span class="sxs-lookup"><span data-stu-id="afe06-246">22</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-247">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-247">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-248">23</span><span class="sxs-lookup"><span data-stu-id="afe06-248">23</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-249">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-249">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-250">24</span><span class="sxs-lookup"><span data-stu-id="afe06-250">24</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-251">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="afe06-251">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="afe06-252">25</span><span class="sxs-lookup"><span data-stu-id="afe06-252">25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-253">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="afe06-253">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="afe06-254">26</span><span class="sxs-lookup"><span data-stu-id="afe06-254">26</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afe06-255">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="afe06-255">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="afe06-256">31</span><span class="sxs-lookup"><span data-stu-id="afe06-256">31</span></span></td>
</tr>
</table>

 

 

 
