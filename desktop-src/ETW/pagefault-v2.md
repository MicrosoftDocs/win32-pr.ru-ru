---
description: Этот класс является родительским для событий сбоя страницы. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: Класс PageFault_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984480"
---
# <a name="pagefault_v2-class"></a><span data-ttu-id="6515d-104">\_Класс PageFault v2</span><span class="sxs-lookup"><span data-stu-id="6515d-104">PageFault\_V2 class</span></span>

<span data-ttu-id="6515d-105">Этот класс является родительским для событий сбоя страницы.</span><span class="sxs-lookup"><span data-stu-id="6515d-105">This class is the parent class for page fault events.</span></span>

<span data-ttu-id="6515d-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="6515d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6515d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6515d-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="6515d-108">Участники</span><span class="sxs-lookup"><span data-stu-id="6515d-108">Members</span></span>

<span data-ttu-id="6515d-109">Класс **PageFault \_ v2** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="6515d-109">The **PageFault\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="6515d-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="6515d-110">Remarks</span></span>

<span data-ttu-id="6515d-111">Чтобы включить все события сбоя страниц в сеансе ведения журнала ядра NT, укажите **флаг \_ \_ \_ \_ \_ ошибок страничной памяти флага трассировки событий** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="6515d-111">To enable all page fault events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="6515d-112">Можно также указать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6515d-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="6515d-113">**\_ \_ \_ \_ фиксированные сбои памяти для флага трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="6515d-113">**EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS**</span></span>
-   <span data-ttu-id="6515d-114">**Виртуальный выделенный \_ флаг трассировки событий \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6515d-114">**EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC**</span></span>

<span data-ttu-id="6515d-115">Потребители трассировки событий могут реализовать специальную обработку всех событий сбоя страницы, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**пажефаултгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="6515d-115">Event trace consumers can implement special processing for all page fault events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PageFaultGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="6515d-116">Используйте следующие типы событий для обнаружения фактического события памяти при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="6515d-116">Use the following event types to identify the actual memory event when consuming events.</span></span>



| <span data-ttu-id="6515d-117">Тип события</span><span class="sxs-lookup"><span data-stu-id="6515d-117">Event type</span></span>                                                     | <span data-ttu-id="6515d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6515d-118">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6515d-119">\_Тип трассировки \_ событий \_ mm \_ Cow (значение типа события — 12)</span><span class="sxs-lookup"><span data-stu-id="6515d-119">EVENT\_TRACE\_TYPE\_MM\_COW(Event type value is 12)</span></span><br/> | <span data-ttu-id="6515d-120">Событие копирования при записи.</span><span class="sxs-lookup"><span data-stu-id="6515d-120">Copy-on-write event.</span></span> <span data-ttu-id="6515d-121">Класс [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-121">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="6515d-122">До выхода Windows Vista класс [**PageFault \_ транситионфаулт**](pagefault-transitionfault.md) MOF определяет событие.</span><span class="sxs-lookup"><span data-stu-id="6515d-122">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>     |
| <span data-ttu-id="6515d-123">\_Тип трассировки \_ событий \_ mm \_ Дзф (значение типа события — 11)</span><span class="sxs-lookup"><span data-stu-id="6515d-123">EVENT\_TRACE\_TYPE\_MM\_DZF(Event type value is 11)</span></span><br/> | <span data-ttu-id="6515d-124">Событие ошибки нулевого требования.</span><span class="sxs-lookup"><span data-stu-id="6515d-124">Demand zero fault event.</span></span> <span data-ttu-id="6515d-125">Класс [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-125">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="6515d-126">До выхода Windows Vista класс [**PageFault \_ транситионфаулт**](pagefault-transitionfault.md) MOF определяет событие.</span><span class="sxs-lookup"><span data-stu-id="6515d-126">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span> |
| <span data-ttu-id="6515d-127">\_Тип трассировки \_ событий \_ mm \_ GPF (значение типа события 13)</span><span class="sxs-lookup"><span data-stu-id="6515d-127">EVENT\_TRACE\_TYPE\_MM\_GPF(Event type value is 13)</span></span><br/> | <span data-ttu-id="6515d-128">Событие ошибки страницы защиты.</span><span class="sxs-lookup"><span data-stu-id="6515d-128">Guard page fault event.</span></span> <span data-ttu-id="6515d-129">Класс [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-129">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="6515d-130">До выхода Windows Vista класс [**PageFault \_ транситионфаулт**](pagefault-transitionfault.md) MOF определяет событие.</span><span class="sxs-lookup"><span data-stu-id="6515d-130">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="6515d-131">\_Тип трассировки \_ событий \_ mm \_ ХПФ (значение типа события — 14)</span><span class="sxs-lookup"><span data-stu-id="6515d-131">EVENT\_TRACE\_TYPE\_MM\_HPF(Event type value is 14)</span></span><br/> | <span data-ttu-id="6515d-132">Событие сбоя страницы.</span><span class="sxs-lookup"><span data-stu-id="6515d-132">Hard page fault event.</span></span> <span data-ttu-id="6515d-133">Класс [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-133">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="6515d-134">До выхода Windows Vista класс [**PageFault \_ транситионфаулт**](pagefault-transitionfault.md) MOF определяет событие.</span><span class="sxs-lookup"><span data-stu-id="6515d-134">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>   |
| <span data-ttu-id="6515d-135">\_Тип трассировки \_ событий \_ \_ , mm, (значение типа события — 10)</span><span class="sxs-lookup"><span data-stu-id="6515d-135">EVENT\_TRACE\_TYPE\_MM\_TF(Event type value is 10)</span></span><br/>  | <span data-ttu-id="6515d-136">Событие сбоя перехода.</span><span class="sxs-lookup"><span data-stu-id="6515d-136">Transition fault event.</span></span> <span data-ttu-id="6515d-137">Класс [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-137">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="6515d-138">До выхода Windows Vista класс [**PageFault \_ транситионфаулт**](pagefault-transitionfault.md) MOF определяет событие.</span><span class="sxs-lookup"><span data-stu-id="6515d-138">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="6515d-139">\_Тип трассировки \_ событий \_ mm \_ AV (значение типа события — 15)</span><span class="sxs-lookup"><span data-stu-id="6515d-139">EVENT\_TRACE\_TYPE\_MM\_AV(Event type value is 15)</span></span><br/>  | <span data-ttu-id="6515d-140">Событие нарушения прав доступа.</span><span class="sxs-lookup"><span data-stu-id="6515d-140">Access violation event.</span></span> <span data-ttu-id="6515d-141">Класс [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-141">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                           |
| <span data-ttu-id="6515d-142">Значение типа события, 32</span><span class="sxs-lookup"><span data-stu-id="6515d-142">Event type value, 32</span></span>                                           | <span data-ttu-id="6515d-143">Событие сбоя страницы. Класс [**PageFault \_ хардфаулт**](pagefault-hardfault.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-143">Hard page fault event.The [**PageFault\_HardFault**](pagefault-hardfault.md) MOF class defines the event data for this event.</span></span>                                                                                                                               |
| <span data-ttu-id="6515d-144">Значение типа события, 105</span><span class="sxs-lookup"><span data-stu-id="6515d-144">Event type value, 105</span></span>                                          | <span data-ttu-id="6515d-145">Событие загрузки изображения в файле подкачки.</span><span class="sxs-lookup"><span data-stu-id="6515d-145">Image load in page file event.</span></span> <span data-ttu-id="6515d-146">Класс [**PageFault \_ имажелоадбаккед**](pagefault-imageloadbacked.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-146">The [**PageFault\_ImageLoadBacked**](pagefault-imageloadbacked.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="6515d-147">Значение типа события, 98</span><span class="sxs-lookup"><span data-stu-id="6515d-147">Event type value, 98</span></span>                                           | <span data-ttu-id="6515d-148">Виртуальное событие выделения.</span><span class="sxs-lookup"><span data-stu-id="6515d-148">Virtual allocation event.</span></span> <span data-ttu-id="6515d-149">Класс [**VirtualAlloc**](pagefault-virtualalloc.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-149">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="6515d-150">Значение типа события, 99</span><span class="sxs-lookup"><span data-stu-id="6515d-150">Event type value, 99</span></span>                                           | <span data-ttu-id="6515d-151">Виртуальное бесплатное событие.</span><span class="sxs-lookup"><span data-stu-id="6515d-151">Virtual free event.</span></span> <span data-ttu-id="6515d-152">Класс [**VirtualAlloc**](pagefault-virtualalloc.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="6515d-152">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                      |



 

<span data-ttu-id="6515d-153">Для выявления неисправного процесса или потока можно использовать члены **ProcessID** и **ThreadID** [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="6515d-153">You can use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the faulting process or thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="6515d-154">Требования</span><span class="sxs-lookup"><span data-stu-id="6515d-154">Requirements</span></span>



| <span data-ttu-id="6515d-155">Требование</span><span class="sxs-lookup"><span data-stu-id="6515d-155">Requirement</span></span> | <span data-ttu-id="6515d-156">Значение</span><span class="sxs-lookup"><span data-stu-id="6515d-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6515d-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6515d-157">Minimum supported client</span></span><br/> | <span data-ttu-id="6515d-158">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6515d-158">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6515d-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6515d-159">Minimum supported server</span></span><br/> | <span data-ttu-id="6515d-160">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6515d-160">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
