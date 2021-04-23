---
description: Этот класс является родительским для событий потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Класс Thread_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: f28b68a2aac5f2d5293f94ed2bab366d238ae662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910743"
---
# <a name="thread_v2-class"></a><span data-ttu-id="ff91b-104">\_Класс Thread v2</span><span class="sxs-lookup"><span data-stu-id="ff91b-104">Thread\_V2 class</span></span>

<span data-ttu-id="ff91b-105">Этот класс является родительским для событий потока.</span><span class="sxs-lookup"><span data-stu-id="ff91b-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="ff91b-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="ff91b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff91b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff91b-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="ff91b-108">Участники</span><span class="sxs-lookup"><span data-stu-id="ff91b-108">Members</span></span>

<span data-ttu-id="ff91b-109">Класс **Thread \_ v2** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="ff91b-109">The **Thread\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff91b-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff91b-110">Remarks</span></span>

<span data-ttu-id="ff91b-111">Чтобы включить события потока в сеансе ведения журнала ядра NT, укажите **флаг \_ \_ \_ потока флага трассировки событий** в **элементе енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="ff91b-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="ff91b-112">Можно также указать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ff91b-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="ff91b-113">**\_ \_ ксвитч флага трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="ff91b-113">**EVENT\_TRACE\_FLAG\_CSWITCH**</span></span>
-   <span data-ttu-id="ff91b-114">**\_ \_ Диспетчер флагов трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="ff91b-114">**EVENT\_TRACE\_FLAG\_DISPATCHER**</span></span>

<span data-ttu-id="ff91b-115">Потребители трассировки событий могут реализовать специальную обработку событий потока, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**среадгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="ff91b-115">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="ff91b-116">Используйте следующие типы событий для обнаружения фактического события потока при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="ff91b-116">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="ff91b-117">Тип события</span><span class="sxs-lookup"><span data-stu-id="ff91b-117">Event type</span></span>                                                      | <span data-ttu-id="ff91b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ff91b-118">Description</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff91b-119">**Событие \_ \_ \_ Конец типа трассировки**(значение типа события — 2)</span><span class="sxs-lookup"><span data-stu-id="ff91b-119">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="ff91b-120">Завершающее событие потока.</span><span class="sxs-lookup"><span data-stu-id="ff91b-120">End thread event.</span></span> <span data-ttu-id="ff91b-121">Класс [**MOF \_ \_ TypeGroup1 в потоке версии 2**](thread-v2-typegroup1.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="ff91b-121">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="ff91b-122">**Событие \_ \_ \_ Начало трассировки типа**(значение типа события равно 1)</span><span class="sxs-lookup"><span data-stu-id="ff91b-122">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="ff91b-123">Событие начала потока.</span><span class="sxs-lookup"><span data-stu-id="ff91b-123">Start thread event.</span></span> <span data-ttu-id="ff91b-124">Класс [**MOF \_ \_ TypeGroup1 в потоке версии 2**](thread-v2-typegroup1.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="ff91b-124">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="ff91b-125">Значение типа события, 3</span><span class="sxs-lookup"><span data-stu-id="ff91b-125">Event type value, 3</span></span>                                             | <span data-ttu-id="ff91b-126">Запуск события потока сбора данных.</span><span class="sxs-lookup"><span data-stu-id="ff91b-126">Start data collection thread event.</span></span> <span data-ttu-id="ff91b-127">Перечисляет потоки, которые выполняются в данный момент во время запуска сеанса ядра.</span><span class="sxs-lookup"><span data-stu-id="ff91b-127">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="ff91b-128">Класс [**MOF \_ \_ TypeGroup1 в потоке версии 2**](thread-v2-typegroup1.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="ff91b-128">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="ff91b-129">Значение типа события, 4</span><span class="sxs-lookup"><span data-stu-id="ff91b-129">Event type value, 4</span></span>                                             | <span data-ttu-id="ff91b-130">Событие потока сбора данных о завершении.</span><span class="sxs-lookup"><span data-stu-id="ff91b-130">End data collection thread event.</span></span> <span data-ttu-id="ff91b-131">Перечисляет потоки, которые выполняются в данный момент в момент завершения сеанса ядра.</span><span class="sxs-lookup"><span data-stu-id="ff91b-131">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="ff91b-132">Класс [**MOF \_ \_ TypeGroup1 в потоке версии 2**](thread-v2-typegroup1.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="ff91b-132">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="ff91b-133">Значение типа события, 36</span><span class="sxs-lookup"><span data-stu-id="ff91b-133">Event type value, 36</span></span>                                            | <span data-ttu-id="ff91b-134">Событие переключения контекста.</span><span class="sxs-lookup"><span data-stu-id="ff91b-134">Context switch event.</span></span> <span data-ttu-id="ff91b-135">Класс MOF [**ксвитч**](cswitch.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="ff91b-135">The [**CSwitch**](cswitch.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="ff91b-136">Значение типа события, 50</span><span class="sxs-lookup"><span data-stu-id="ff91b-136">Event type value, 50</span></span>                                            | <span data-ttu-id="ff91b-137">Готовое событие потока.</span><span class="sxs-lookup"><span data-stu-id="ff91b-137">Ready thread event.</span></span> <span data-ttu-id="ff91b-138">Класс MOF [**реадисреад**](readythread.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="ff91b-138">The [**ReadyThread**](readythread.md) MOF class defines the event data for this event.</span></span>                                                                                                                          |



 

<span data-ttu-id="ff91b-139">События процесса и запуска потока могут регистрироваться в контексте родительского процесса или потока.</span><span class="sxs-lookup"><span data-stu-id="ff91b-139">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="ff91b-140">В результате элементы **ProcessID** и **ThreadID** [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) могут не соответствовать создаваемому процессу и потоку.</span><span class="sxs-lookup"><span data-stu-id="ff91b-140">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="ff91b-141">Именно поэтому эти события содержат идентификаторы процесса и потока в данных события (помимо тех, которые находятся в заголовке события).</span><span class="sxs-lookup"><span data-stu-id="ff91b-141">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff91b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="ff91b-142">Requirements</span></span>



| <span data-ttu-id="ff91b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="ff91b-143">Requirement</span></span> | <span data-ttu-id="ff91b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="ff91b-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff91b-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff91b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ff91b-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff91b-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff91b-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff91b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ff91b-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff91b-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff91b-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff91b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff91b-150">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="ff91b-150">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="ff91b-151">**ксвитч**</span><span class="sxs-lookup"><span data-stu-id="ff91b-151">**CSwitch**</span></span>](cswitch.md)
</dt> <dt>

[<span data-ttu-id="ff91b-152">**Поток**</span><span class="sxs-lookup"><span data-stu-id="ff91b-152">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="ff91b-153">**\_TypeGroup1 потока**</span><span class="sxs-lookup"><span data-stu-id="ff91b-153">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="ff91b-154">**\_V0 потока**</span><span class="sxs-lookup"><span data-stu-id="ff91b-154">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="ff91b-155">**Поток \_ v1**</span><span class="sxs-lookup"><span data-stu-id="ff91b-155">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 
