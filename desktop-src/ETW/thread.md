---
description: Этот класс является родительским для событий потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread - класс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: c4af87462607b675e46b3459a811925fbefe3ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273125"
---
# <a name="thread-class"></a><span data-ttu-id="a7353-104">Thread - класс</span><span class="sxs-lookup"><span data-stu-id="a7353-104">Thread class</span></span>

<span data-ttu-id="a7353-105">Этот класс является родительским для событий потока.</span><span class="sxs-lookup"><span data-stu-id="a7353-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="a7353-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a7353-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7353-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7353-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="a7353-108">Участники</span><span class="sxs-lookup"><span data-stu-id="a7353-108">Members</span></span>

<span data-ttu-id="a7353-109">Класс **потока** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="a7353-109">The **Thread** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7353-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7353-110">Remarks</span></span>

<span data-ttu-id="a7353-111">Чтобы включить события потока в сеансе ведения журнала ядра NT, укажите **флаг \_ \_ \_ потока флага трассировки событий** в **элементе енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="a7353-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="a7353-112">Потребители трассировки событий могут реализовать специальную обработку событий потока, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**среадгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="a7353-112">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="a7353-113">Используйте следующие типы событий для обнаружения фактического события потока при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="a7353-113">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="a7353-114">Тип события</span><span class="sxs-lookup"><span data-stu-id="a7353-114">Event type</span></span>                                                      | <span data-ttu-id="a7353-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a7353-115">Description</span></span>                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7353-116">**Событие \_ \_ \_ Конец типа трассировки**(значение типа события — 2)</span><span class="sxs-lookup"><span data-stu-id="a7353-116">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="a7353-117">Завершающее событие потока.</span><span class="sxs-lookup"><span data-stu-id="a7353-117">End thread event.</span></span> <span data-ttu-id="a7353-118">Класс [**\_ TypeGroup1 потока**](thread-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="a7353-118">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="a7353-119">**Событие \_ \_ \_ Начало трассировки типа**(значение типа события равно 1)</span><span class="sxs-lookup"><span data-stu-id="a7353-119">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="a7353-120">Событие начала потока.</span><span class="sxs-lookup"><span data-stu-id="a7353-120">Start thread event.</span></span> <span data-ttu-id="a7353-121">Класс [**\_ TypeGroup1 потока**](thread-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="a7353-121">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="a7353-122">Значение типа события, 3</span><span class="sxs-lookup"><span data-stu-id="a7353-122">Event type value, 3</span></span>                                             | <span data-ttu-id="a7353-123">Запуск события потока сбора данных.</span><span class="sxs-lookup"><span data-stu-id="a7353-123">Start data collection thread event.</span></span> <span data-ttu-id="a7353-124">Перечисляет потоки, которые выполняются в данный момент во время запуска сеанса ядра.</span><span class="sxs-lookup"><span data-stu-id="a7353-124">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="a7353-125">Класс [**\_ TypeGroup1 потока**](thread-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="a7353-125">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="a7353-126">Значение типа события, 4</span><span class="sxs-lookup"><span data-stu-id="a7353-126">Event type value, 4</span></span>                                             | <span data-ttu-id="a7353-127">Событие потока сбора данных о завершении.</span><span class="sxs-lookup"><span data-stu-id="a7353-127">End data collection thread event.</span></span> <span data-ttu-id="a7353-128">Перечисляет потоки, которые выполняются в данный момент в момент завершения сеанса ядра.</span><span class="sxs-lookup"><span data-stu-id="a7353-128">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="a7353-129">Класс [**\_ TypeGroup1 потока**](thread-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="a7353-129">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="a7353-130">События процесса и запуска потока могут регистрироваться в контексте родительского процесса или потока.</span><span class="sxs-lookup"><span data-stu-id="a7353-130">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="a7353-131">В результате элементы **ProcessID** и **ThreadID** [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) могут не соответствовать создаваемому процессу и потоку.</span><span class="sxs-lookup"><span data-stu-id="a7353-131">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="a7353-132">Именно поэтому эти события содержат идентификаторы процесса и потока в данных события (помимо тех, которые находятся в заголовке события).</span><span class="sxs-lookup"><span data-stu-id="a7353-132">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7353-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a7353-133">Requirements</span></span>



| <span data-ttu-id="a7353-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a7353-134">Requirement</span></span> | <span data-ttu-id="a7353-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a7353-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7353-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7353-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a7353-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7353-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a7353-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7353-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a7353-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a7353-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7353-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7353-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7353-141">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="a7353-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="a7353-142">**\_TypeGroup1 потока**</span><span class="sxs-lookup"><span data-stu-id="a7353-142">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="a7353-143">**\_V0 потока**</span><span class="sxs-lookup"><span data-stu-id="a7353-143">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="a7353-144">**Поток \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a7353-144">**Thread\_V1**</span></span>](thread-v1.md)
</dt> <dt>

[<span data-ttu-id="a7353-145">**Поток \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="a7353-145">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 
