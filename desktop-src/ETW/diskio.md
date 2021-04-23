---
description: Этот класс является родительским для событий дискового ввода-вывода. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: Класс Дискио
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990942"
---
# <a name="diskio-class"></a><span data-ttu-id="46127-104">Класс Дискио</span><span class="sxs-lookup"><span data-stu-id="46127-104">DiskIo class</span></span>

<span data-ttu-id="46127-105">Этот класс является родительским для событий дискового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="46127-105">This class is the parent class for disk I/O events.</span></span>

<span data-ttu-id="46127-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="46127-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="46127-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46127-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="46127-108">Участники</span><span class="sxs-lookup"><span data-stu-id="46127-108">Members</span></span>

<span data-ttu-id="46127-109">Класс **дискио** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="46127-109">The **DiskIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="46127-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="46127-110">Remarks</span></span>

<span data-ttu-id="46127-111">Чтобы включить события дискового ввода-вывода в сеансе ведения журнала ядра NT, при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) укажите флаг **отслеживания событий на \_ \_ \_ диске \_** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="46127-111">To enable disk I/0 events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="46127-112">Можно также указать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="46127-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="46127-113">**\_флаг трассировки событий — \_ \_ \_ Инициализация дискового ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="46127-113">**EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT**</span></span>
-   <span data-ttu-id="46127-114">**\_ \_ драйвер флага трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="46127-114">**EVENT\_TRACE\_FLAG\_DRIVER**</span></span>

<span data-ttu-id="46127-115">Потребители трассировки событий могут реализовать специальную обработку событий дискового ввода-вывода, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**дискиогуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="46127-115">Event trace consumers can implement special processing for disk I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**DiskIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="46127-116">Используйте следующие типы событий для обнаружения фактического события дискового ввода-вывода при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="46127-116">Use the following event types to identify the actual disk I/O event when consuming events.</span></span>



| <span data-ttu-id="46127-117">Тип события</span><span class="sxs-lookup"><span data-stu-id="46127-117">Event type</span></span>                                                                      | <span data-ttu-id="46127-118">Описание</span><span class="sxs-lookup"><span data-stu-id="46127-118">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46127-119">**Событие \_ \_Тип трассировки \_ \_ Read-IO**(значение типа события — 10)</span><span class="sxs-lookup"><span data-stu-id="46127-119">**EVENT\_TRACE\_TYPE\_IO\_READ**(Event type value is 10)</span></span><br/>             | <span data-ttu-id="46127-120">Чтение события.</span><span class="sxs-lookup"><span data-stu-id="46127-120">Read event.</span></span> <span data-ttu-id="46127-121">Класс [**дискио \_ TypeGroup1**](diskio-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-121">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                              |
| <span data-ttu-id="46127-122">**Событие \_ \_Тип трассировки \_ IO- \_ Write**(значение типа события — 11)</span><span class="sxs-lookup"><span data-stu-id="46127-122">**EVENT\_TRACE\_TYPE\_IO\_WRITE**(Event type value is 11)</span></span><br/>            | <span data-ttu-id="46127-123">Запись события.</span><span class="sxs-lookup"><span data-stu-id="46127-123">Write event.</span></span> <span data-ttu-id="46127-124">Класс [**дискио \_ TypeGroup1**](diskio-typegroup1.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-124">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                             |
| <span data-ttu-id="46127-125">**Событие \_ ТРАССИРОВКа с \_ типом \_ ввода-вывода \_ Read \_ init**(значение типа события — 12)</span><span class="sxs-lookup"><span data-stu-id="46127-125">**EVENT\_TRACE\_TYPE\_IO\_READ\_INIT**(Event type value is 12)</span></span><br/>       | <span data-ttu-id="46127-126">Инициализация события чтения.</span><span class="sxs-lookup"><span data-stu-id="46127-126">Initialize read event.</span></span> <span data-ttu-id="46127-127">Класс [**дискио \_ TypeGroup2**](diskio-typegroup2.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-127">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="46127-128">**Событие \_ Трассировка \_ \_ \_ записи ввода \_ -вывода типа трассировки**(значение типа события 13)</span><span class="sxs-lookup"><span data-stu-id="46127-128">**EVENT\_TRACE\_TYPE\_IO\_WRITE\_INIT**(Event type value is 13)</span></span><br/>      | <span data-ttu-id="46127-129">Инициализация события записи.</span><span class="sxs-lookup"><span data-stu-id="46127-129">Initialize write event.</span></span> <span data-ttu-id="46127-130">Класс [**дискио \_ TypeGroup2**](diskio-typegroup2.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-130">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="46127-131">**Событие \_ \_Тип трассировки \_ i/o \_ flush**(значение типа события — 14)</span><span class="sxs-lookup"><span data-stu-id="46127-131">**EVENT\_TRACE\_TYPE\_IO\_FLUSH**(Event type value is 14)</span></span><br/>            | <span data-ttu-id="46127-132">Инициализация события записи.</span><span class="sxs-lookup"><span data-stu-id="46127-132">Initialize write event.</span></span> <span data-ttu-id="46127-133">Класс [**дискио \_ TypeGroup3**](diskio-typegroup3.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-133">The [**DiskIo\_TypeGroup3**](diskio-typegroup3.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="46127-134">**Событие \_ Трассировка \_ \_ операций ввода-вывода для \_ \_ типа трассировки**(значение типа события — 15)</span><span class="sxs-lookup"><span data-stu-id="46127-134">**EVENT\_TRACE\_TYPE\_IO\_FLUSH\_INIT**(Event type value is 15)</span></span><br/>      | <span data-ttu-id="46127-135">Инициализация события очистки.</span><span class="sxs-lookup"><span data-stu-id="46127-135">Initialize flush event.</span></span> <span data-ttu-id="46127-136">Класс [**дискио \_ TypeGroup2**](diskio-typegroup2.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-136">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="46127-137">**Событие \_ \_ \_ \_ Перенаправленная \_ инициализация типа трассировки IO**(значение типа события — 16)</span><span class="sxs-lookup"><span data-stu-id="46127-137">**EVENT\_TRACE\_TYPE\_IO\_REDIRECTED\_INIT**(Event type value is 16)</span></span><br/> | <span data-ttu-id="46127-138">Инициализация перенаправленного события.</span><span class="sxs-lookup"><span data-stu-id="46127-138">Initialize redirected event.</span></span> <span data-ttu-id="46127-139">Перенаправленные события ввода-вывода используются для преобразования диска IOs в формат Windows Imaging (WIM) в имя файла в WIM.</span><span class="sxs-lookup"><span data-stu-id="46127-139">Redirected IO events are used to map disk IOs to a Windows Imaging Format (WIM) to the filename within the WIM.</span></span>                  |
| <span data-ttu-id="46127-140">Значение типа события — 52</span><span class="sxs-lookup"><span data-stu-id="46127-140">Event type value is 52</span></span><br/>                                               | <span data-ttu-id="46127-141">Событие запроса завершения драйвера.</span><span class="sxs-lookup"><span data-stu-id="46127-141">Driver complete request event.</span></span> <span data-ttu-id="46127-142">Класс MOF [**дриверкомплетерекуест**](drivercompleterequest.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-142">The [**DriverCompleteRequest**](drivercompleterequest.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="46127-143">Значение типа события — 53</span><span class="sxs-lookup"><span data-stu-id="46127-143">Event type value is 53</span></span><br/>                                               | <span data-ttu-id="46127-144">Драйвер завершил запрос на возврат события.</span><span class="sxs-lookup"><span data-stu-id="46127-144">Driver complete request return event.</span></span> <span data-ttu-id="46127-145">Класс MOF [**дриверкомплетерекуестретурн**](drivercompleterequestreturn.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-145">The [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="46127-146">Значение типа события — 37</span><span class="sxs-lookup"><span data-stu-id="46127-146">Event type value is 37</span></span><br/>                                               | <span data-ttu-id="46127-147">Событие процедуры завершения драйвера.</span><span class="sxs-lookup"><span data-stu-id="46127-147">Driver completion routine event.</span></span> <span data-ttu-id="46127-148">Класс MOF [**дриверкомплетионраутине**](drivercompletionroutine.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-148">The [**DriverCompletionRoutine**](drivercompletionroutine.md) MOF class defines the event data for this event.</span></span>              |
| <span data-ttu-id="46127-149">Значение типа события — 34</span><span class="sxs-lookup"><span data-stu-id="46127-149">Event type value is 34</span></span><br/>                                               | <span data-ttu-id="46127-150">Событие вызова основной функции драйвера.</span><span class="sxs-lookup"><span data-stu-id="46127-150">Driver major function call event.</span></span> <span data-ttu-id="46127-151">Класс MOF [**дривермажорфунктионкалл**](drivermajorfunctioncall.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-151">The [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) MOF class defines the event data for this event.</span></span>             |
| <span data-ttu-id="46127-152">Значение типа события — 35</span><span class="sxs-lookup"><span data-stu-id="46127-152">Event type value is 35</span></span><br/>                                               | <span data-ttu-id="46127-153">Событие возврата вызова основной функции драйвера.</span><span class="sxs-lookup"><span data-stu-id="46127-153">Driver major function call return event.</span></span> <span data-ttu-id="46127-154">Класс MOF [**дривермажорфунктионретурн**](drivermajorfunctionreturn.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="46127-154">The [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="46127-155">Поставщик дискового ввода-вывода не может найти файл, который считывается или записывается во время события дискового ввода-вывод.</span><span class="sxs-lookup"><span data-stu-id="46127-155">The disk I/0 provider cannot identify which file is read or written during a disk I/O event.</span></span> <span data-ttu-id="46127-156">Чтобы получить имя файла, связанного с событием дискового ввода-вывода, включите поставщик событий File I/0.</span><span class="sxs-lookup"><span data-stu-id="46127-156">To retrieve the name of the file associated with the disk I/O event, enable the file I/0 event provider.</span></span>

<span data-ttu-id="46127-157">События дискового ввода-вывода записываются в момент завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="46127-157">Disk I/O events are recorded at the I/O completion time.</span></span> <span data-ttu-id="46127-158">Чтобы определить, когда была начата операция ввода-вывода, используйте события инициализации, например, \_ Трассировка событий \_ тип \_ IO \_ Чтение \_ init.</span><span class="sxs-lookup"><span data-stu-id="46127-158">To determine when the I/O operation began, use the initialization events, for example, EVENT\_TRACE\_TYPE\_IO\_READ\_INIT.</span></span>

## <a name="requirements"></a><span data-ttu-id="46127-159">Требования</span><span class="sxs-lookup"><span data-stu-id="46127-159">Requirements</span></span>



| <span data-ttu-id="46127-160">Требование</span><span class="sxs-lookup"><span data-stu-id="46127-160">Requirement</span></span> | <span data-ttu-id="46127-161">Значение</span><span class="sxs-lookup"><span data-stu-id="46127-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46127-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46127-162">Minimum supported client</span></span><br/> | <span data-ttu-id="46127-163">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="46127-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="46127-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46127-164">Minimum supported server</span></span><br/> | <span data-ttu-id="46127-165">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46127-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46127-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46127-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46127-167">**Дискио \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="46127-167">**DiskIo\_TypeGroup1**</span></span>](diskio-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="46127-168">**Дискио \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="46127-168">**DiskIo\_TypeGroup2**</span></span>](diskio-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="46127-169">**Дискио \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="46127-169">**DiskIo\_TypeGroup3**</span></span>](diskio-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="46127-170">**дриверкомплетерекуест**</span><span class="sxs-lookup"><span data-stu-id="46127-170">**DriverCompleteRequest**</span></span>](drivercompleterequest.md)
</dt> <dt>

[<span data-ttu-id="46127-171">**дриверкомплетерекуестретурн**</span><span class="sxs-lookup"><span data-stu-id="46127-171">**DriverCompleteRequestReturn**</span></span>](drivercompleterequestreturn.md)
</dt> <dt>

[<span data-ttu-id="46127-172">**дриверкомплетионраутине**</span><span class="sxs-lookup"><span data-stu-id="46127-172">**DriverCompletionRoutine**</span></span>](drivercompletionroutine.md)
</dt> <dt>

[<span data-ttu-id="46127-173">**дривермажорфунктионкалл**</span><span class="sxs-lookup"><span data-stu-id="46127-173">**DriverMajorFunctionCall**</span></span>](drivermajorfunctioncall.md)
</dt> <dt>

[<span data-ttu-id="46127-174">**дривермажорфунктионретурн**</span><span class="sxs-lookup"><span data-stu-id="46127-174">**DriverMajorFunctionReturn**</span></span>](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
