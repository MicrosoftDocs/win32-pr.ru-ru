---
description: Этот класс является родительским для событий UDP/IP. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: 5116b5f97a4aa7e3bafa9da1c1208ce7ee9d5794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543074"
---
# <a name="udpip-class"></a><span data-ttu-id="bf36e-104">Класс Удпип</span><span class="sxs-lookup"><span data-stu-id="bf36e-104">UdpIp class</span></span>

<span data-ttu-id="bf36e-105">Этот класс является родительским для событий UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="bf36e-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="bf36e-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="bf36e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf36e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf36e-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="bf36e-108">Участники</span><span class="sxs-lookup"><span data-stu-id="bf36e-108">Members</span></span>

<span data-ttu-id="bf36e-109">Класс **удпип** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="bf36e-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf36e-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf36e-110">Remarks</span></span>

<span data-ttu-id="bf36e-111">Чтобы включить события UDP/IP в сеансе ведения журнала ядра NT, укажите **флаг \_ отслеживания \_ событий \_ Network \_ tcpip** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="bf36e-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="bf36e-112">Потребители трассировки событий могут реализовать специальную обработку событий UDP/IP, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**удпипгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="bf36e-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="bf36e-113">Используйте следующие типы событий для обнаружения фактического события сети (UDP/IP) при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="bf36e-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="bf36e-114">Тип события</span><span class="sxs-lookup"><span data-stu-id="bf36e-114">Event type</span></span>                                                         | <span data-ttu-id="bf36e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bf36e-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf36e-116">**Событие \_ \_ \_ Получение типа трассировки**(значение типа события — 11)</span><span class="sxs-lookup"><span data-stu-id="bf36e-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="bf36e-117">Событие получения для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="bf36e-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="bf36e-118">Класс [**удпип \_ TypeGroup1**](udpip-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="bf36e-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="bf36e-119">**Событие \_ ТРАССИРОВКа \_ типа \_ Send**(значение типа события — 10)</span><span class="sxs-lookup"><span data-stu-id="bf36e-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="bf36e-120">Событие отправки для протокола IPv4.</span><span class="sxs-lookup"><span data-stu-id="bf36e-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="bf36e-121">Класс [**удпип \_ TypeGroup1**](udpip-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="bf36e-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="bf36e-122">Значение типа события, 17</span><span class="sxs-lookup"><span data-stu-id="bf36e-122">Event type value, 17</span></span>                                               | <span data-ttu-id="bf36e-123">Событие Fail.</span><span class="sxs-lookup"><span data-stu-id="bf36e-123">Fail event.</span></span> <span data-ttu-id="bf36e-124">Класс [**удпип \_ Failed**](udpip-fail.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="bf36e-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="bf36e-125">Значение типа события, 26</span><span class="sxs-lookup"><span data-stu-id="bf36e-125">Event type value, 26</span></span>                                               | <span data-ttu-id="bf36e-126">Отправка события для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="bf36e-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="bf36e-127">Класс [**удпип \_ TypeGroup2**](udpip-typegroup2.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="bf36e-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="bf36e-128">Значение типа события, 27</span><span class="sxs-lookup"><span data-stu-id="bf36e-128">Event type value, 27</span></span>                                               | <span data-ttu-id="bf36e-129">Событие получения для протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="bf36e-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="bf36e-130">Класс [**удпип \_ TypeGroup2**](udpip-typegroup2.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="bf36e-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="bf36e-131">Вы можете отслеживать сетевые события в исходном и целевом процессах, используя свойство **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="bf36e-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="bf36e-132">Так как некоторые сетевые события регистрируются отдельными потоками, вы не сможете использовать члены **ProcessID** и **ThreadID** [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) для выявления процесса или потока, которые были источником сетевых операций.</span><span class="sxs-lookup"><span data-stu-id="bf36e-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf36e-133">Требования</span><span class="sxs-lookup"><span data-stu-id="bf36e-133">Requirements</span></span>



| <span data-ttu-id="bf36e-134">Требование</span><span class="sxs-lookup"><span data-stu-id="bf36e-134">Requirement</span></span> | <span data-ttu-id="bf36e-135">Значение</span><span class="sxs-lookup"><span data-stu-id="bf36e-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf36e-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf36e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bf36e-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf36e-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bf36e-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf36e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bf36e-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf36e-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf36e-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf36e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf36e-141">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="bf36e-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="bf36e-142">**\_Сбой удпип**</span><span class="sxs-lookup"><span data-stu-id="bf36e-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="bf36e-143">**Удпип \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="bf36e-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="bf36e-144">**Удпип \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="bf36e-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="bf36e-145">**Удпип \_ v0**</span><span class="sxs-lookup"><span data-stu-id="bf36e-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="bf36e-146">**Удпип \_ v1**</span><span class="sxs-lookup"><span data-stu-id="bf36e-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
