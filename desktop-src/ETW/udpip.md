---
description: Класс Удпип. Этот класс является родительским для событий UDP/IP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: Класс Удпип
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105392"
---
# <a name="udpip-class"></a><span data-ttu-id="82727-104">Класс Удпип</span><span class="sxs-lookup"><span data-stu-id="82727-104">UdpIp class</span></span>

<span data-ttu-id="82727-105">Этот класс является родительским для событий UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="82727-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="82727-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="82727-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="82727-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82727-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="82727-108">Члены</span><span class="sxs-lookup"><span data-stu-id="82727-108">Members</span></span>

<span data-ttu-id="82727-109">Класс **удпип** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="82727-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="82727-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="82727-110">Remarks</span></span>

<span data-ttu-id="82727-111">Чтобы включить события UDP/IP в сеансе ведения журнала ядра NT, укажите **флаг \_ отслеживания \_ событий \_ Network \_ tcpip** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="82727-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="82727-112">Потребители трассировки событий могут реализовать специальную обработку событий UDP/IP, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**удпипгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="82727-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="82727-113">Используйте следующие типы событий для обнаружения фактического события сети (UDP/IP) при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="82727-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="82727-114">Тип события</span><span class="sxs-lookup"><span data-stu-id="82727-114">Event type</span></span>                                                         | <span data-ttu-id="82727-115">Описание</span><span class="sxs-lookup"><span data-stu-id="82727-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82727-116">**Событие \_ \_ \_ Получение типа трассировки**(значение типа события — 11)</span><span class="sxs-lookup"><span data-stu-id="82727-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="82727-117">Событие получения для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="82727-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="82727-118">Класс [**удпип \_ TypeGroup1**](udpip-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="82727-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="82727-119">**Событие \_ ТРАССИРОВКа \_ типа \_ Send**(значение типа события — 10)</span><span class="sxs-lookup"><span data-stu-id="82727-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="82727-120">Событие отправки для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="82727-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="82727-121">Класс [**удпип \_ TypeGroup1**](udpip-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="82727-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="82727-122">Значение типа события, 17</span><span class="sxs-lookup"><span data-stu-id="82727-122">Event type value, 17</span></span>                                               | <span data-ttu-id="82727-123">Событие Fail.</span><span class="sxs-lookup"><span data-stu-id="82727-123">Fail event.</span></span> <span data-ttu-id="82727-124">Класс [**удпип \_ Failed**](udpip-fail.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="82727-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="82727-125">Значение типа события, 26</span><span class="sxs-lookup"><span data-stu-id="82727-125">Event type value, 26</span></span>                                               | <span data-ttu-id="82727-126">Отправка события для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="82727-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="82727-127">Класс [**удпип \_ TypeGroup2**](udpip-typegroup2.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="82727-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="82727-128">Значение типа события, 27</span><span class="sxs-lookup"><span data-stu-id="82727-128">Event type value, 27</span></span>                                               | <span data-ttu-id="82727-129">Событие получения для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="82727-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="82727-130">Класс [**удпип \_ TypeGroup2**](udpip-typegroup2.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="82727-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="82727-131">Вы можете отслеживать сетевые события в исходном и целевом процессах, используя свойство **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="82727-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="82727-132">Так как некоторые сетевые события регистрируются отдельными потоками, вы не сможете использовать члены **ProcessID** и **ThreadID** [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) для выявления процесса или потока, которые были источником сетевых операций.</span><span class="sxs-lookup"><span data-stu-id="82727-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="82727-133">Требования</span><span class="sxs-lookup"><span data-stu-id="82727-133">Requirements</span></span>



| <span data-ttu-id="82727-134">Требование</span><span class="sxs-lookup"><span data-stu-id="82727-134">Requirement</span></span> | <span data-ttu-id="82727-135">Значение</span><span class="sxs-lookup"><span data-stu-id="82727-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="82727-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82727-136">Minimum supported client</span></span><br/> | <span data-ttu-id="82727-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82727-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="82727-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82727-138">Minimum supported server</span></span><br/> | <span data-ttu-id="82727-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82727-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82727-140">См. также</span><span class="sxs-lookup"><span data-stu-id="82727-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82727-141">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="82727-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="82727-142">**\_Сбой удпип**</span><span class="sxs-lookup"><span data-stu-id="82727-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="82727-143">**Удпип \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="82727-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="82727-144">**Удпип \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="82727-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="82727-145">**Удпип \_ v0**</span><span class="sxs-lookup"><span data-stu-id="82727-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="82727-146">**Удпип \_ v1**</span><span class="sxs-lookup"><span data-stu-id="82727-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
