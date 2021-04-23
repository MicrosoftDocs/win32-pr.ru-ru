---
description: Этот класс является родительским для событий TCP/IP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: Класс TcpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6488ece2fd8df0670455ceea25560835c352b83e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984773"
---
# <a name="tcpip-class"></a><span data-ttu-id="8127a-104">Класс TcpIp</span><span class="sxs-lookup"><span data-stu-id="8127a-104">TcpIp class</span></span>

<span data-ttu-id="8127a-105">Этот класс является родительским для событий TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8127a-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="8127a-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="8127a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8127a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8127a-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="8127a-108">Участники</span><span class="sxs-lookup"><span data-stu-id="8127a-108">Members</span></span>

<span data-ttu-id="8127a-109">Класс **TcpIp** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="8127a-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="8127a-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="8127a-110">Remarks</span></span>

<span data-ttu-id="8127a-111">Чтобы включить события TCP/IP в сеансе ведения журнала ядра NT, укажите **флаг \_ отслеживания \_ событий \_ Network \_ tcpip** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="8127a-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="8127a-112">Потребители трассировки событий могут реализовать специальную обработку событий TCP/IP, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**ткпипгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="8127a-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="8127a-113">Используйте следующие типы событий для обнаружения фактического события сети (TCP/IP) при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="8127a-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="8127a-114">Тип события</span><span class="sxs-lookup"><span data-stu-id="8127a-114">Event type</span></span>                                                            | <span data-ttu-id="8127a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="8127a-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8127a-116">**Событие \_ \_Тип трассировки \_ Accept**(значение типа события — 15)</span><span class="sxs-lookup"><span data-stu-id="8127a-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="8127a-117">Принять событие для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="8127a-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="8127a-118">Класс [**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="8127a-119">**Событие \_ \_Тип трассировки \_ Connect**(значение типа события — 12)</span><span class="sxs-lookup"><span data-stu-id="8127a-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="8127a-120">Событие подключения для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="8127a-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="8127a-121">Класс [**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="8127a-122">**Событие \_ \_ \_ Отключение типа трассировки**(значение типа события равно 13)</span><span class="sxs-lookup"><span data-stu-id="8127a-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="8127a-123">Событие отсоединения для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="8127a-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="8127a-124">Класс [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="8127a-125">**Событие \_ \_ \_ Получение типа трассировки**(значение типа события — 11)</span><span class="sxs-lookup"><span data-stu-id="8127a-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="8127a-126">Событие получения для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="8127a-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="8127a-127">Класс [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="8127a-128">**Событие \_ \_Переподключение \_ типа трассировки**(значение типа события — 16)</span><span class="sxs-lookup"><span data-stu-id="8127a-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="8127a-129">Событие повторного подключения для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="8127a-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="8127a-130">(Попытка подключения не удалась, выполняется другая попытка.) Класс [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="8127a-131">**Событие \_ Повторная \_ \_ передача типа трассировки**(значение типа события — 14)</span><span class="sxs-lookup"><span data-stu-id="8127a-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="8127a-132">Повторно передать событие для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="8127a-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="8127a-133">Класс [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="8127a-134">**Событие \_ ТРАССИРОВКа \_ типа \_ Send**(значение типа события — 10)</span><span class="sxs-lookup"><span data-stu-id="8127a-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="8127a-135">Событие отправки для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="8127a-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="8127a-136">Класс [**TcpIp \_ SendIPV4**](tcpip-sendipv4.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="8127a-137">Значение типа события, 17</span><span class="sxs-lookup"><span data-stu-id="8127a-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="8127a-138">Событие Fail.</span><span class="sxs-lookup"><span data-stu-id="8127a-138">Fail event.</span></span> <span data-ttu-id="8127a-139">Класс [**MOF \_ Failed**](tcpip-fail.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="8127a-140">Значение типа события, 18</span><span class="sxs-lookup"><span data-stu-id="8127a-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="8127a-141">Событие копирования TCP для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="8127a-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="8127a-142">Класс [**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="8127a-143">Значение типа события, 26</span><span class="sxs-lookup"><span data-stu-id="8127a-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="8127a-144">Отправка события для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="8127a-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="8127a-145">Класс [**TcpIp \_ SendIPV6**](tcpip-sendipv6.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="8127a-146">Значение типа события, 27</span><span class="sxs-lookup"><span data-stu-id="8127a-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="8127a-147">Событие получения для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="8127a-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="8127a-148">Класс [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="8127a-149">Значение типа события, 28</span><span class="sxs-lookup"><span data-stu-id="8127a-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="8127a-150">Событие подключения для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="8127a-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="8127a-151">Класс [**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="8127a-152">Значение типа события, 29</span><span class="sxs-lookup"><span data-stu-id="8127a-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="8127a-153">Событие отсоединения для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="8127a-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="8127a-154">Класс [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="8127a-155">Значение типа события, 30</span><span class="sxs-lookup"><span data-stu-id="8127a-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="8127a-156">Повторно передать событие для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="8127a-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="8127a-157">Класс [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="8127a-158">Значение типа события, 31</span><span class="sxs-lookup"><span data-stu-id="8127a-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="8127a-159">Принять событие для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="8127a-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="8127a-160">Класс [**TcpIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="8127a-161">Значение типа события, 32</span><span class="sxs-lookup"><span data-stu-id="8127a-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="8127a-162">Событие повторного подключения для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="8127a-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="8127a-163">(Попытка подключения не удалась, выполняется другая попытка.) Класс [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="8127a-164">Значение типа события, 34</span><span class="sxs-lookup"><span data-stu-id="8127a-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="8127a-165">Событие копирования TCP для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="8127a-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="8127a-166">Класс [**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="8127a-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="8127a-167">Вы можете отслеживать сетевые события в исходном и целевом процессах, используя свойство **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="8127a-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="8127a-168">Так как некоторые сетевые события регистрируются отдельными потоками, вы не сможете использовать члены **ProcessID** и **ThreadID** [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) для выявления процесса или потока, которые были источником сетевых операций.</span><span class="sxs-lookup"><span data-stu-id="8127a-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="8127a-169">Требования</span><span class="sxs-lookup"><span data-stu-id="8127a-169">Requirements</span></span>



| <span data-ttu-id="8127a-170">Требование</span><span class="sxs-lookup"><span data-stu-id="8127a-170">Requirement</span></span> | <span data-ttu-id="8127a-171">Значение</span><span class="sxs-lookup"><span data-stu-id="8127a-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8127a-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8127a-172">Minimum supported client</span></span><br/> | <span data-ttu-id="8127a-173">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8127a-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8127a-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8127a-174">Minimum supported server</span></span><br/> | <span data-ttu-id="8127a-175">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8127a-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8127a-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8127a-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8127a-177">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="8127a-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="8127a-178">**Сбой TCP/IP \_**</span><span class="sxs-lookup"><span data-stu-id="8127a-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="8127a-179">**TCP/IP \_ SendIPV4**</span><span class="sxs-lookup"><span data-stu-id="8127a-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="8127a-180">**TCP/IP \_ SendIPV6**</span><span class="sxs-lookup"><span data-stu-id="8127a-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="8127a-181">**TCP/IP \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="8127a-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="8127a-182">**TCP/IP \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="8127a-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="8127a-183">**TCP/IP \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="8127a-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="8127a-184">**TCP/IP \_ TypeGroup4**</span><span class="sxs-lookup"><span data-stu-id="8127a-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="8127a-185">**TCP/IP \_ v0**</span><span class="sxs-lookup"><span data-stu-id="8127a-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="8127a-186">**TcpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="8127a-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
