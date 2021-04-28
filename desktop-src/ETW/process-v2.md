---
description: Класс Process_V2 — этот класс является родительским для событий процесса. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Класс Process_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: 77d700e7847d0ad19a019985a4e19343ce8f383d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106302"
---
# <a name="process_v2-class"></a><span data-ttu-id="c4308-104">\_Класс Process v2</span><span class="sxs-lookup"><span data-stu-id="c4308-104">Process\_V2 class</span></span>

<span data-ttu-id="c4308-105">Этот класс является родительским для событий процесса.</span><span class="sxs-lookup"><span data-stu-id="c4308-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="c4308-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="c4308-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4308-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4308-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="c4308-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c4308-108">Members</span></span>

<span data-ttu-id="c4308-109">Класс **Process** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="c4308-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4308-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="c4308-110">Remarks</span></span>

<span data-ttu-id="c4308-111">Чтобы включить события обработки в сеансе ведения журнала ядра NT, задайте **флаг \_ \_ \_ процесса трассировки событий** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="c4308-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="c4308-112">Можно также указать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="c4308-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="c4308-113">**\_ \_ \_ счетчики процесса ФЛАГа трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="c4308-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="c4308-114">Потребители трассировки событий могут реализовать специальную обработку событий процесса, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**процессгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="c4308-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="c4308-115">Используйте следующие типы событий для обнаружения фактического события обработки при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="c4308-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="c4308-116">Тип события</span><span class="sxs-lookup"><span data-stu-id="c4308-116">Event type</span></span>                                                      | <span data-ttu-id="c4308-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c4308-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4308-118">**Событие \_ \_ \_ Конец типа трассировки**(значение типа события — 2)</span><span class="sxs-lookup"><span data-stu-id="c4308-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="c4308-119">Событие завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="c4308-119">End process event.</span></span> <span data-ttu-id="c4308-120">Класс [**Process \_ TypeGroup1**](process-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="c4308-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="c4308-121">**Событие \_ \_ \_ Начало трассировки типа**(значение типа события равно 1)</span><span class="sxs-lookup"><span data-stu-id="c4308-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="c4308-122">Запуск события обработки.</span><span class="sxs-lookup"><span data-stu-id="c4308-122">Start process event.</span></span> <span data-ttu-id="c4308-123">Класс [**Process \_ TypeGroup1**](process-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="c4308-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="c4308-124">Значение типа события, 3</span><span class="sxs-lookup"><span data-stu-id="c4308-124">Event type value, 3</span></span>                                             | <span data-ttu-id="c4308-125">Запустить событие процесса сбора данных.</span><span class="sxs-lookup"><span data-stu-id="c4308-125">Start data collection process event.</span></span> <span data-ttu-id="c4308-126">Перечисляет процессы, выполняемые в данный момент во время запуска сеанса ядра.</span><span class="sxs-lookup"><span data-stu-id="c4308-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="c4308-127">Класс [**Process \_ TypeGroup1**](process-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="c4308-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="c4308-128">Значение типа события, 4</span><span class="sxs-lookup"><span data-stu-id="c4308-128">Event type value, 4</span></span>                                             | <span data-ttu-id="c4308-129">Событие завершения процесса сбора данных.</span><span class="sxs-lookup"><span data-stu-id="c4308-129">End data collection process event.</span></span> <span data-ttu-id="c4308-130">Перечисляет процессы, выполняемые в данный момент в момент завершения сеанса ядра.</span><span class="sxs-lookup"><span data-stu-id="c4308-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="c4308-131">Класс [**Process \_ TypeGroup1**](process-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="c4308-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="c4308-132">Значение типа события, 32</span><span class="sxs-lookup"><span data-stu-id="c4308-132">Event type value, 32</span></span>                                            | <span data-ttu-id="c4308-133">Событие счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="c4308-133">Performance counters event.</span></span> <span data-ttu-id="c4308-134">Класс [**MOF \_ \_ TypeGroup2 процесса v2**](process-v2-typegroup2.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="c4308-134">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                                                          |
| <span data-ttu-id="c4308-135">Значение типа события, 33</span><span class="sxs-lookup"><span data-stu-id="c4308-135">Event type value, 33</span></span>                                            | <span data-ttu-id="c4308-136">Очистка счетчиков производительности в начале сеанса.</span><span class="sxs-lookup"><span data-stu-id="c4308-136">Rundown of the performance counters at the start of the session.</span></span> <span data-ttu-id="c4308-137">Класс [**MOF \_ \_ TypeGroup2 процесса v2**](process-v2-typegroup2.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="c4308-137">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                     |
| <span data-ttu-id="c4308-138">Значение типа события, 39</span><span class="sxs-lookup"><span data-stu-id="c4308-138">Event type value, 39</span></span>                                            | <span data-ttu-id="c4308-139">Событие нефункционирующего процесса.</span><span class="sxs-lookup"><span data-stu-id="c4308-139">Defunct process event.</span></span> <span data-ttu-id="c4308-140">Класс [**Process \_ TypeGroup1**](process-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="c4308-140">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |



 

<span data-ttu-id="c4308-141">События процесса и запуска потока могут регистрироваться в контексте родительского процесса или потока.</span><span class="sxs-lookup"><span data-stu-id="c4308-141">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="c4308-142">В результате элементы **ProcessID** и **ThreadID** [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) могут не соответствовать создаваемому процессу и потоку.</span><span class="sxs-lookup"><span data-stu-id="c4308-142">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="c4308-143">Именно поэтому эти события содержат идентификаторы процесса и потока в данных события (помимо тех, которые находятся в заголовке события).</span><span class="sxs-lookup"><span data-stu-id="c4308-143">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4308-144">Требования</span><span class="sxs-lookup"><span data-stu-id="c4308-144">Requirements</span></span>



| <span data-ttu-id="c4308-145">Требование</span><span class="sxs-lookup"><span data-stu-id="c4308-145">Requirement</span></span> | <span data-ttu-id="c4308-146">Значение</span><span class="sxs-lookup"><span data-stu-id="c4308-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="c4308-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4308-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c4308-148">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c4308-148">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="c4308-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4308-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c4308-150">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c4308-150">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4308-151">См. также</span><span class="sxs-lookup"><span data-stu-id="c4308-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4308-152">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="c4308-152">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="c4308-153">**Процесс**</span><span class="sxs-lookup"><span data-stu-id="c4308-153">**Process**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="c4308-154">**Обработка \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="c4308-154">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="c4308-155">**Обработка \_ v0**</span><span class="sxs-lookup"><span data-stu-id="c4308-155">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="c4308-156">**Процесс \_ v1**</span><span class="sxs-lookup"><span data-stu-id="c4308-156">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 
