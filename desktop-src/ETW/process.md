---
description: Класс процесса — этот класс является родительским для событий процесса. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Класс процесса
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
ms.openlocfilehash: 8085bae0d00ebe830efff420744f6b7e9b4bf23c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106272"
---
# <a name="process-class"></a><span data-ttu-id="506c8-104">Класс процесса</span><span class="sxs-lookup"><span data-stu-id="506c8-104">Process class</span></span>

<span data-ttu-id="506c8-105">Этот класс является родительским для событий процесса.</span><span class="sxs-lookup"><span data-stu-id="506c8-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="506c8-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="506c8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="506c8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="506c8-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="506c8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="506c8-108">Members</span></span>

<span data-ttu-id="506c8-109">Класс **Process** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="506c8-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="506c8-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="506c8-110">Remarks</span></span>

<span data-ttu-id="506c8-111">Чтобы включить события обработки в сеансе ведения журнала ядра NT, задайте **флаг \_ \_ \_ процесса трассировки событий** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="506c8-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="506c8-112">Можно также указать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="506c8-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="506c8-113">**\_ \_ \_ счетчики процесса ФЛАГа трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="506c8-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="506c8-114">Потребители трассировки событий могут реализовать специальную обработку событий процесса, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**процессгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="506c8-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="506c8-115">Используйте следующие типы событий для обнаружения фактического события обработки при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="506c8-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="506c8-116">Тип события</span><span class="sxs-lookup"><span data-stu-id="506c8-116">Event type</span></span>                                                      | <span data-ttu-id="506c8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="506c8-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="506c8-118">**Событие \_ \_ \_ Конец типа трассировки**(значение типа события — 2)</span><span class="sxs-lookup"><span data-stu-id="506c8-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="506c8-119">Событие завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="506c8-119">End process event.</span></span> <span data-ttu-id="506c8-120">Класс [**Process \_ TypeGroup1**](process-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="506c8-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="506c8-121">**Событие \_ \_ \_ Начало трассировки типа**(значение типа события равно 1)</span><span class="sxs-lookup"><span data-stu-id="506c8-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="506c8-122">Запуск события обработки.</span><span class="sxs-lookup"><span data-stu-id="506c8-122">Start process event.</span></span> <span data-ttu-id="506c8-123">Класс [**Process \_ TypeGroup1**](process-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="506c8-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="506c8-124">Значение типа события, 3</span><span class="sxs-lookup"><span data-stu-id="506c8-124">Event type value, 3</span></span>                                             | <span data-ttu-id="506c8-125">Запустить событие процесса сбора данных.</span><span class="sxs-lookup"><span data-stu-id="506c8-125">Start data collection process event.</span></span> <span data-ttu-id="506c8-126">Перечисляет процессы, выполняемые в данный момент во время запуска сеанса ядра.</span><span class="sxs-lookup"><span data-stu-id="506c8-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="506c8-127">Класс [**Process \_ TypeGroup1**](process-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="506c8-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="506c8-128">Значение типа события, 4</span><span class="sxs-lookup"><span data-stu-id="506c8-128">Event type value, 4</span></span>                                             | <span data-ttu-id="506c8-129">Событие завершения процесса сбора данных.</span><span class="sxs-lookup"><span data-stu-id="506c8-129">End data collection process event.</span></span> <span data-ttu-id="506c8-130">Перечисляет процессы, выполняемые в данный момент в момент завершения сеанса ядра.</span><span class="sxs-lookup"><span data-stu-id="506c8-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="506c8-131">Класс [**Process \_ TypeGroup1**](process-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="506c8-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="506c8-132">События процесса и запуска потока могут регистрироваться в контексте родительского процесса или потока.</span><span class="sxs-lookup"><span data-stu-id="506c8-132">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="506c8-133">В результате элементы **ProcessID** и **ThreadID** [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) могут не соответствовать создаваемому процессу и потоку.</span><span class="sxs-lookup"><span data-stu-id="506c8-133">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="506c8-134">Именно поэтому эти события содержат идентификаторы процесса и потока в данных события (помимо тех, которые находятся в заголовке события).</span><span class="sxs-lookup"><span data-stu-id="506c8-134">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="506c8-135">Требования</span><span class="sxs-lookup"><span data-stu-id="506c8-135">Requirements</span></span>



| <span data-ttu-id="506c8-136">Требование</span><span class="sxs-lookup"><span data-stu-id="506c8-136">Requirement</span></span> | <span data-ttu-id="506c8-137">Значение</span><span class="sxs-lookup"><span data-stu-id="506c8-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="506c8-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="506c8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="506c8-139">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="506c8-139">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="506c8-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="506c8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="506c8-141">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="506c8-141">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="506c8-142">См. также</span><span class="sxs-lookup"><span data-stu-id="506c8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506c8-143">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="506c8-143">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="506c8-144">**Обработка \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="506c8-144">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="506c8-145">**Обработка \_ v0**</span><span class="sxs-lookup"><span data-stu-id="506c8-145">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="506c8-146">**Процесс \_ v1**</span><span class="sxs-lookup"><span data-stu-id="506c8-146">**Process\_V1**</span></span>](process-v1.md)
</dt> <dt>

[<span data-ttu-id="506c8-147">**Процесс \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="506c8-147">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 
