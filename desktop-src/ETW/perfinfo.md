---
description: Этот класс является родительским классом для событий счетчика производительности. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: Класс Перфинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984513"
---
# <a name="perfinfo-class"></a><span data-ttu-id="7b6b9-104">Класс Перфинфо</span><span class="sxs-lookup"><span data-stu-id="7b6b9-104">PerfInfo class</span></span>

<span data-ttu-id="7b6b9-105">Этот класс является родительским классом для событий счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-105">This class is the parent class for performance counter events.</span></span>

<span data-ttu-id="7b6b9-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6b9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b6b9-107">Syntax</span></span>

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="7b6b9-108">Участники</span><span class="sxs-lookup"><span data-stu-id="7b6b9-108">Members</span></span>

<span data-ttu-id="7b6b9-109">Класс **перфинфо** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-109">The **PerfInfo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b6b9-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b6b9-110">Remarks</span></span>

<span data-ttu-id="7b6b9-111">Чтобы включить события отложенного вызова процедур (DPC) в сеансе ведения журнала ядра NT, при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) укажите флаг **\_ трассировки событий \_ \_ DPC** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="7b6b9-111">To enable deferred procedure call (DPC) events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="7b6b9-112">Можно также указать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="7b6b9-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="7b6b9-113">**\_ \_ прерывание флага трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="7b6b9-113">**EVENT\_TRACE\_FLAG\_INTERRUPT**</span></span>
-   <span data-ttu-id="7b6b9-114">**\_ \_ профиль флага трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="7b6b9-114">**EVENT\_TRACE\_FLAG\_PROFILE**</span></span>
-   <span data-ttu-id="7b6b9-115">**\_ \_ системкалл флага трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="7b6b9-115">**EVENT\_TRACE\_FLAG\_SYSTEMCALL**</span></span>

<span data-ttu-id="7b6b9-116">Потребители трассировки событий могут реализовать специальную обработку событий DPC, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**перфинфогуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="7b6b9-116">Event trace consumers can implement special processing for DPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PerfInfoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="7b6b9-117">Используйте следующие типы событий для обнаружения фактического события при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-117">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="7b6b9-118">Тип события</span><span class="sxs-lookup"><span data-stu-id="7b6b9-118">Event type</span></span>           | <span data-ttu-id="7b6b9-119">Описание</span><span class="sxs-lookup"><span data-stu-id="7b6b9-119">Description</span></span>                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b6b9-120">Значение типа события, 46</span><span class="sxs-lookup"><span data-stu-id="7b6b9-120">Event type value, 46</span></span> | <span data-ttu-id="7b6b9-121">Событие выборки профиля.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-121">Sampled profile event.</span></span> <span data-ttu-id="7b6b9-122">Класс MOF [**сампледпрофиле**](sampledprofile.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-122">The [**SampledProfile**](sampledprofile.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="7b6b9-123">Значение типа события, 51</span><span class="sxs-lookup"><span data-stu-id="7b6b9-123">Event type value, 51</span></span> | <span data-ttu-id="7b6b9-124">Событие ввода системного вызова.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-124">System call enter event.</span></span> <span data-ttu-id="7b6b9-125">Класс MOF [**сискаллентер**](syscallenter.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-125">The [**SysCallEnter**](syscallenter.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="7b6b9-126">Значение типа события, 52</span><span class="sxs-lookup"><span data-stu-id="7b6b9-126">Event type value, 52</span></span> | <span data-ttu-id="7b6b9-127">Событие выхода из системного вызова.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-127">System call exit event.</span></span> <span data-ttu-id="7b6b9-128">Класс MOF [**сискаллексит**](syscallexit.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-128">The [**SysCallExit**](syscallexit.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="7b6b9-129">Значение типа события, 66</span><span class="sxs-lookup"><span data-stu-id="7b6b9-129">Event type value, 66</span></span> | <span data-ttu-id="7b6b9-130">Потоковое событие DPC.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-130">Threaded DPC event.</span></span> <span data-ttu-id="7b6b9-131">Класс [**DPC**](dpc.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-131">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                          |
| <span data-ttu-id="7b6b9-132">Значение типа события, 67</span><span class="sxs-lookup"><span data-stu-id="7b6b9-132">Event type value, 67</span></span> | <span data-ttu-id="7b6b9-133">Событие "процедура службы прерываний" (ISR).</span><span class="sxs-lookup"><span data-stu-id="7b6b9-133">Interrupt service routine (ISR) event.</span></span> <span data-ttu-id="7b6b9-134">Класс MOF [**ISR**](isr.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-134">The [**ISR**](isr.md) MOF class defines the event data for this event.</span></span>       |
| <span data-ttu-id="7b6b9-135">Значение типа события, 68</span><span class="sxs-lookup"><span data-stu-id="7b6b9-135">Event type value, 68</span></span> | <span data-ttu-id="7b6b9-136">Событие DPC.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-136">DPC event.</span></span> <span data-ttu-id="7b6b9-137">Класс [**DPC**](dpc.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-137">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="7b6b9-138">Значение типа события, 69</span><span class="sxs-lookup"><span data-stu-id="7b6b9-138">Event type value, 69</span></span> | <span data-ttu-id="7b6b9-139">Событие таймера DPC.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-139">DPC timer event.</span></span> <span data-ttu-id="7b6b9-140">Класс [**DPC**](dpc.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-140">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="7b6b9-141">Требования</span><span class="sxs-lookup"><span data-stu-id="7b6b9-141">Requirements</span></span>



| <span data-ttu-id="7b6b9-142">Требование</span><span class="sxs-lookup"><span data-stu-id="7b6b9-142">Requirement</span></span> | <span data-ttu-id="7b6b9-143">Значение</span><span class="sxs-lookup"><span data-stu-id="7b6b9-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b6b9-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b6b9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="7b6b9-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b6b9-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b6b9-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b6b9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="7b6b9-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b6b9-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
