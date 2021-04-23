---
description: Этот класс является родительским для событий файлового ввода-вывода. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Класс FileIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985085"
---
# <a name="fileio-class"></a><span data-ttu-id="9a13c-104">Класс FileIo</span><span class="sxs-lookup"><span data-stu-id="9a13c-104">FileIo class</span></span>

<span data-ttu-id="9a13c-105">Этот класс является родительским для событий файлового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9a13c-105">This class is the parent class for file I/O events.</span></span>

<span data-ttu-id="9a13c-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9a13c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a13c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a13c-107">Syntax</span></span>

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="9a13c-108">Участники</span><span class="sxs-lookup"><span data-stu-id="9a13c-108">Members</span></span>

<span data-ttu-id="9a13c-109">Класс **FileIo** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="9a13c-109">The **FileIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a13c-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a13c-110">Remarks</span></span>

<span data-ttu-id="9a13c-111">Чтобы включить события ввода-вывода файлов в сеансе ведения журнала ядра NT, укажите флаг **\_ трассировки \_ \_ \_ \_ операций ввода-вывода для файла диска** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="9a13c-111">To enable the File IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="9a13c-112">Можно также указать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="9a13c-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="9a13c-113">**операция \_ \_ ввода- \_ вывода файла ФЛАГа трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="9a13c-113">**EVENT\_TRACE\_FLAG\_FILE\_IO**</span></span>
-   <span data-ttu-id="9a13c-114">**\_ \_ \_ \_ Инициализация операции ввода-вывода файла флага трассировки событий \_**</span><span class="sxs-lookup"><span data-stu-id="9a13c-114">**EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT**</span></span>

<span data-ttu-id="9a13c-115">Потребители трассировки событий могут реализовать специальную обработку событий файлового ввода-вывода, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**филеиогуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="9a13c-115">Event trace consumers can implement special processing for file I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**FileIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="9a13c-116">Используйте следующие типы событий для обнаружения фактического события при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="9a13c-116">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="9a13c-117">Тип события</span><span class="sxs-lookup"><span data-stu-id="9a13c-117">Event type</span></span>             | <span data-ttu-id="9a13c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9a13c-118">Description</span></span>                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a13c-119">Значение типа события равно 0</span><span class="sxs-lookup"><span data-stu-id="9a13c-119">Event type value is 0</span></span>  | <span data-ttu-id="9a13c-120">Событие имени файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-120">File name event.</span></span> <span data-ttu-id="9a13c-121">Класс [**MOF \_ имени FileIo**](fileio-name.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-121">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                               |
| <span data-ttu-id="9a13c-122">Значение типа события — 32</span><span class="sxs-lookup"><span data-stu-id="9a13c-122">Event type value is 32</span></span> | <span data-ttu-id="9a13c-123">Событие создания файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-123">File create event.</span></span> <span data-ttu-id="9a13c-124">Класс [**MOF \_ имени FileIo**](fileio-name.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-124">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="9a13c-125">Значение типа события — 35</span><span class="sxs-lookup"><span data-stu-id="9a13c-125">Event type value is 35</span></span> | <span data-ttu-id="9a13c-126">Событие удаления файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-126">File delete event.</span></span> <span data-ttu-id="9a13c-127">Класс [**MOF \_ имени FileIo**](fileio-name.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-127">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="9a13c-128">Значение типа события — 36</span><span class="sxs-lookup"><span data-stu-id="9a13c-128">Event type value is 36</span></span> | <span data-ttu-id="9a13c-129">Событие очистки файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-129">File rundown event.</span></span> <span data-ttu-id="9a13c-130">Перечисляет все открытые файлы на компьютере в конце сеанса трассировки.</span><span class="sxs-lookup"><span data-stu-id="9a13c-130">Enumerates all open files on the computer at the end of the trace session.</span></span> <span data-ttu-id="9a13c-131">Класс [**MOF \_ имени FileIo**](fileio-name.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-131">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="9a13c-132">Значение типа события — 64</span><span class="sxs-lookup"><span data-stu-id="9a13c-132">Event type value is 64</span></span> | <span data-ttu-id="9a13c-133">Событие создания файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-133">File create event.</span></span> <span data-ttu-id="9a13c-134">Класс [**FileIo \_ CREATE**](fileio-create.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-134">The [**FileIo\_Create**](fileio-create.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="9a13c-135">Значение типа события — 72</span><span class="sxs-lookup"><span data-stu-id="9a13c-135">Event type value is 72</span></span> | <span data-ttu-id="9a13c-136">Событие перечисления каталогов.</span><span class="sxs-lookup"><span data-stu-id="9a13c-136">Directory enumeration event.</span></span> <span data-ttu-id="9a13c-137">Класс [**FileIo \_ диренум**](fileio-direnum.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-137">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                             |
| <span data-ttu-id="9a13c-138">Значение типа события — 77</span><span class="sxs-lookup"><span data-stu-id="9a13c-138">Event type value is 77</span></span> | <span data-ttu-id="9a13c-139">Событие уведомления каталога.</span><span class="sxs-lookup"><span data-stu-id="9a13c-139">Directory notification event.</span></span> <span data-ttu-id="9a13c-140">Класс [**FileIo \_ диренум**](fileio-direnum.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-140">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="9a13c-141">Значение типа события — 69</span><span class="sxs-lookup"><span data-stu-id="9a13c-141">Event type value is 69</span></span> | <span data-ttu-id="9a13c-142">Задать информационное событие.</span><span class="sxs-lookup"><span data-stu-id="9a13c-142">Set information event.</span></span> <span data-ttu-id="9a13c-143">Класс [**MOF \_ info FileIo**](fileio-info.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-143">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="9a13c-144">Значение типа события — 70</span><span class="sxs-lookup"><span data-stu-id="9a13c-144">Event type value is 70</span></span> | <span data-ttu-id="9a13c-145">Событие удаления файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-145">Delete file event.</span></span> <span data-ttu-id="9a13c-146">Класс [**MOF \_ info FileIo**](fileio-info.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-146">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="9a13c-147">Значение типа события — 71</span><span class="sxs-lookup"><span data-stu-id="9a13c-147">Event type value is 71</span></span> | <span data-ttu-id="9a13c-148">Событие переименования файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-148">Rename file event.</span></span> <span data-ttu-id="9a13c-149">Класс [**MOF \_ info FileIo**](fileio-info.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-149">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="9a13c-150">Значение типа события — 74</span><span class="sxs-lookup"><span data-stu-id="9a13c-150">Event type value is 74</span></span> | <span data-ttu-id="9a13c-151">Событие сведений о файле запроса.</span><span class="sxs-lookup"><span data-stu-id="9a13c-151">Query file information event.</span></span> <span data-ttu-id="9a13c-152">Класс [**MOF \_ info FileIo**](fileio-info.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-152">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="9a13c-153">Значение типа события — 75</span><span class="sxs-lookup"><span data-stu-id="9a13c-153">Event type value is 75</span></span> | <span data-ttu-id="9a13c-154">Событие управления файловой системой.</span><span class="sxs-lookup"><span data-stu-id="9a13c-154">File system control event.</span></span> <span data-ttu-id="9a13c-155">Класс [**MOF \_ info FileIo**](fileio-info.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-155">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="9a13c-156">Значение типа события — 76</span><span class="sxs-lookup"><span data-stu-id="9a13c-156">Event type value is 76</span></span> | <span data-ttu-id="9a13c-157">Событие завершения операции.</span><span class="sxs-lookup"><span data-stu-id="9a13c-157">End of operation event.</span></span> <span data-ttu-id="9a13c-158">[**FileIo \_ открытый**](fileio-opend.md) класс MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-158">The [**FileIo\_OpEnd**](fileio-opend.md) MOF class defines the event data for this event.</span></span>                                                                      |
| <span data-ttu-id="9a13c-159">Значение типа события — 67</span><span class="sxs-lookup"><span data-stu-id="9a13c-159">Event type value is 67</span></span> | <span data-ttu-id="9a13c-160">Событие чтения файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-160">File read event.</span></span> <span data-ttu-id="9a13c-161">Класс MOF [**FileIo \_ ReadWrite**](fileio-readwrite.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-161">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="9a13c-162">Значение типа события — 68</span><span class="sxs-lookup"><span data-stu-id="9a13c-162">Event type value is 68</span></span> | <span data-ttu-id="9a13c-163">Событие записи файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-163">File write event.</span></span> <span data-ttu-id="9a13c-164">Класс MOF [**FileIo \_ ReadWrite**](fileio-readwrite.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-164">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                    |
| <span data-ttu-id="9a13c-165">Значение типа события — 65</span><span class="sxs-lookup"><span data-stu-id="9a13c-165">Event type value is 65</span></span> | <span data-ttu-id="9a13c-166">Событие очистки.</span><span class="sxs-lookup"><span data-stu-id="9a13c-166">Clean up event.</span></span> <span data-ttu-id="9a13c-167">Событие создается при освобождении последнего маркера файла.</span><span class="sxs-lookup"><span data-stu-id="9a13c-167">The event is generated when the last handle to the file is released.</span></span> <span data-ttu-id="9a13c-168">Класс [**FileIo \_ симплеоп**](fileio-simpleop.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-168">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="9a13c-169">Значение типа события — 66</span><span class="sxs-lookup"><span data-stu-id="9a13c-169">Event type value is 66</span></span> | <span data-ttu-id="9a13c-170">Событие закрытия.</span><span class="sxs-lookup"><span data-stu-id="9a13c-170">Close event.</span></span> <span data-ttu-id="9a13c-171">Событие создается при освобождении объекта File.</span><span class="sxs-lookup"><span data-stu-id="9a13c-171">The event is generated when the file object is freed.</span></span> <span data-ttu-id="9a13c-172">Класс [**FileIo \_ симплеоп**](fileio-simpleop.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-172">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>                     |
| <span data-ttu-id="9a13c-173">Значение типа события — 73</span><span class="sxs-lookup"><span data-stu-id="9a13c-173">Event type value is 73</span></span> | <span data-ttu-id="9a13c-174">Событие записи на диск.</span><span class="sxs-lookup"><span data-stu-id="9a13c-174">Flush event.</span></span> <span data-ttu-id="9a13c-175">Это событие создается, когда буферы файлов полностью сброшены на диск.</span><span class="sxs-lookup"><span data-stu-id="9a13c-175">This event is generated when the file buffers are fully flushed to disk.</span></span> <span data-ttu-id="9a13c-176">Класс [**FileIo \_ симплеоп**](fileio-simpleop.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9a13c-176">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="9a13c-177">События файлового ввода-вывода регистрируются в начале операции.</span><span class="sxs-lookup"><span data-stu-id="9a13c-177">File IO events are logged at the beginning of the operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a13c-178">Требования</span><span class="sxs-lookup"><span data-stu-id="9a13c-178">Requirements</span></span>



| <span data-ttu-id="9a13c-179">Требование</span><span class="sxs-lookup"><span data-stu-id="9a13c-179">Requirement</span></span> | <span data-ttu-id="9a13c-180">Значение</span><span class="sxs-lookup"><span data-stu-id="9a13c-180">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a13c-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a13c-181">Minimum supported client</span></span><br/> | <span data-ttu-id="9a13c-182">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a13c-182">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9a13c-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a13c-183">Minimum supported server</span></span><br/> | <span data-ttu-id="9a13c-184">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9a13c-184">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a13c-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a13c-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a13c-186">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="9a13c-186">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="9a13c-187">**FileIo \_ v0**</span><span class="sxs-lookup"><span data-stu-id="9a13c-187">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> <dt>

[<span data-ttu-id="9a13c-188">**FileIo \_ v1**</span><span class="sxs-lookup"><span data-stu-id="9a13c-188">**FileIo\_V1**</span></span>](fileio-v1.md)
</dt> </dl>

 

 
