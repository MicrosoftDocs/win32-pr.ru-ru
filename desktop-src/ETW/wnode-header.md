---
description: '\_Структура заголовка вноде является элементом \_ \_ структуры свойств трассировки событий.'
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: Структура WNODE_HEADER (Вмистр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: 6a2ed615d2b67cbd47a817234a14b7cf1221f601
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "104987416"
---
# <a name="wnode_header-structure"></a><span data-ttu-id="0abe1-103">\_Структура заголовка вноде</span><span class="sxs-lookup"><span data-stu-id="0abe1-103">WNODE\_HEADER structure</span></span>

<span data-ttu-id="0abe1-104">Структура **\_ заголовка вноде** является элементом структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="0abe1-104">The **WNODE\_HEADER** structure is a member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0abe1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0abe1-105">Syntax</span></span>


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a><span data-ttu-id="0abe1-106">Участники</span><span class="sxs-lookup"><span data-stu-id="0abe1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0abe1-107">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="0abe1-107">**BufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-108">Общий размер выделенной памяти (в байтах) для свойств сеанса трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="0abe1-108">Total size of memory allocated, in bytes, for the event tracing session properties.</span></span> <span data-ttu-id="0abe1-109">Размер памяти должен включать место для структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , а также строку имени сеанса и имя файла журнала, которые следуют за структурой в памяти.</span><span class="sxs-lookup"><span data-stu-id="0abe1-109">The size of memory must include the room for the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure plus the session name string and log file name string that follow the structure in memory.</span></span>

</dd> <dt>

<span data-ttu-id="0abe1-110">**ProviderId**</span><span class="sxs-lookup"><span data-stu-id="0abe1-110">**ProviderId**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-111">Зарезервировано для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="0abe1-111">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="0abe1-112">**хисторикалконтекст**</span><span class="sxs-lookup"><span data-stu-id="0abe1-112">**HistoricalContext**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-113">На выходе — это обработчик сеанса трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="0abe1-113">On output, the handle to the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="0abe1-114">**Версия**</span><span class="sxs-lookup"><span data-stu-id="0abe1-114">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-115">Зарезервировано для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="0abe1-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="0abe1-116">**Компоновка**</span><span class="sxs-lookup"><span data-stu-id="0abe1-116">**Linkage**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-117">Зарезервировано для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="0abe1-117">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="0abe1-118">**кернелхандле**</span><span class="sxs-lookup"><span data-stu-id="0abe1-118">**KernelHandle**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-119">Зарезервировано для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="0abe1-119">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="0abe1-120">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="0abe1-120">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-121">Время обновления сведений в этой структуре за 100-наносекундных интервалов с полуночи 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="0abe1-121">Time at which the information in this structure was updated, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="0abe1-122">**Устройства**</span><span class="sxs-lookup"><span data-stu-id="0abe1-122">**Guid**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-123">Идентификатор GUID, определенный для сеанса.</span><span class="sxs-lookup"><span data-stu-id="0abe1-123">The GUID that you define for the session.</span></span>

<span data-ttu-id="0abe1-124">Для сеанса ведения журнала ядра NT установите для этого элемента значение **системтрацеконтролгуид**.</span><span class="sxs-lookup"><span data-stu-id="0abe1-124">For an NT Kernel Logger session, set this member to **SystemTraceControlGuid**.</span></span>

<span data-ttu-id="0abe1-125">Если для этого члена задано значение **системтрацеконтролгуид** или **глобаллогжергуид**, средство ведения журнала будет системным журналом.</span><span class="sxs-lookup"><span data-stu-id="0abe1-125">If this member is set to **SystemTraceControlGuid** or **GlobalLoggerGuid**, the logger will be a system logger.</span></span>

<span data-ttu-id="0abe1-126">Для закрытого сеанса ведения журнала задайте для этого элемента идентификатор GUID поставщика, который будет включен для сеанса.</span><span class="sxs-lookup"><span data-stu-id="0abe1-126">For a private logger session, set this member to the provider's GUID that you are going to enable for the session.</span></span>

<span data-ttu-id="0abe1-127">Если вы запускаете сеанс, который не является средством ведения журнала ядра или закрытым сеансом ведения журнала, указывать идентификатор GUID сеанса не требуется.</span><span class="sxs-lookup"><span data-stu-id="0abe1-127">If you start a session that is not a kernel logger or private logger session, you do not have to specify a session GUID.</span></span> <span data-ttu-id="0abe1-128">Если идентификатор GUID не указан, ETW создаст его.</span><span class="sxs-lookup"><span data-stu-id="0abe1-128">If you do not specify a GUID, ETW creates one for you.</span></span> <span data-ttu-id="0abe1-129">Идентификатор GUID сеанса необходимо указывать только в том случае, если необходимо изменить разрешения по умолчанию, связанные с конкретным сеансом.</span><span class="sxs-lookup"><span data-stu-id="0abe1-129">You need to specify a session GUID only if you want to change the default permissions associated with a specific session.</span></span> <span data-ttu-id="0abe1-130">Дополнительные сведения см. в описании функции Евентакцессконтрол.</span><span class="sxs-lookup"><span data-stu-id="0abe1-130">For details, see the EventAccessControl function.</span></span>

<span data-ttu-id="0abe1-131">Нельзя запустить более одного сеанса с одинаковым идентификатором GUID сеанса.</span><span class="sxs-lookup"><span data-stu-id="0abe1-131">You cannot start more than one session with the same session GUID.</span></span>

<span data-ttu-id="0abe1-132">**До Windows Vista:** Можно запустить более одного сеанса с одним идентификатором GUID сеанса.</span><span class="sxs-lookup"><span data-stu-id="0abe1-132">**Prior to Windows Vista:** You can start more than one session with the same session GUID.</span></span>

</dd> <dt>

<span data-ttu-id="0abe1-133">**ClientContext**</span><span class="sxs-lookup"><span data-stu-id="0abe1-133">**ClientContext**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-134">Разрешение часов, используемое при записи метки времени для каждого события.</span><span class="sxs-lookup"><span data-stu-id="0abe1-134">Clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="0abe1-135">Значение по умолчанию — счетчик производительности запросов (QPC).</span><span class="sxs-lookup"><span data-stu-id="0abe1-135">The default is Query performance counter (QPC).</span></span>

<span data-ttu-id="0abe1-136">**До Windows Vista:** По умолчанию используется системное время.</span><span class="sxs-lookup"><span data-stu-id="0abe1-136">**Prior to Windows Vista:** The default is system time.</span></span>

<span data-ttu-id="0abe1-137">**До Windows 10, версия 1703:** Все системные средства ведения журнала могут одновременно использовать не более 2 различных типов часов.</span><span class="sxs-lookup"><span data-stu-id="0abe1-137">**Prior to Windows 10, version 1703:** No more than 2 distinct clock types can be used simultaneously by any system loggers.</span></span>

<span data-ttu-id="0abe1-138">**Начиная с Windows 10, версия 1703:** Ограничение типа "Часы" было удалено.</span><span class="sxs-lookup"><span data-stu-id="0abe1-138">**Starting with Windows 10, version 1703:** The clock type restriction has been removed.</span></span> <span data-ttu-id="0abe1-139">Все три типа часов теперь могут использоваться системными журналами одновременно.</span><span class="sxs-lookup"><span data-stu-id="0abe1-139">All three clock types can now be used simultaneously by system loggers.</span></span>

<span data-ttu-id="0abe1-140">Можно указать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0abe1-140">You can specify one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0abe1-141">Значение</span><span class="sxs-lookup"><span data-stu-id="0abe1-141">Value</span></span></th>
<th><span data-ttu-id="0abe1-142">Значение</span><span class="sxs-lookup"><span data-stu-id="0abe1-142">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="0abe1-143"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="0abe1-143"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="0abe1-144">Счетчик производительности запросов (QPC).</span><span class="sxs-lookup"><span data-stu-id="0abe1-144">Query performance counter (QPC).</span></span> <span data-ttu-id="0abe1-145">Счетчик QPC предоставляет метку времени высокого разрешения, которая не влияет на системные часы.</span><span class="sxs-lookup"><span data-stu-id="0abe1-145">The QPC counter provides a high-resolution time stamp that is not affected by adjustments to the system clock.</span></span> <span data-ttu-id="0abe1-146">Метка времени, хранящаяся в событии, эквивалентна значению, возвращаемому API QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="0abe1-146">The time stamp stored in the event is equivalent to the value returned from the QueryPerformanceCounter API.</span></span> <span data-ttu-id="0abe1-147">Дополнительные сведения о характеристиках этой метки времени см. в разделе <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Получение меток времени с высоким разрешением</a>.</span><span class="sxs-lookup"><span data-stu-id="0abe1-147">For more information on the characteristics of this time stamp, see <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>.</span></span><br/> <span data-ttu-id="0abe1-148">Это разрешение следует использовать при наличии высокой частоты событий или в случае, если потребитель объединяет события из разных буферов.</span><span class="sxs-lookup"><span data-stu-id="0abe1-148">You should use this resolution if you have high event rates or if the consumer merges events from different buffers.</span></span> <span data-ttu-id="0abe1-149">В таких случаях точность и стабильность отметок времени QPC обеспечивают лучшую точность при упорядочении событий из разных буферов.</span><span class="sxs-lookup"><span data-stu-id="0abe1-149">In these cases, the precision and stability of the QPC time stamp allows for better accuracy in ordering the events from different buffers.</span></span> <span data-ttu-id="0abe1-150">Однако отметка времени QPC не отражает обновления системных часов, например, если системные часы настраиваются вперед из-за синхронизации с сервером NTP во время трассировки, то отметки времени QPC в трассировке будут продолжать отражать время, как если бы обновление не происходило.</span><span class="sxs-lookup"><span data-stu-id="0abe1-150">However, the QPC time stamp will not reflect updates to the system clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the QPC time stamps in the trace will continue to reflect time as if no update had occurred.</span></span><br/> <span data-ttu-id="0abe1-151">Чтобы определить разрешение, используйте член <strong>перффрек</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> при использовании события.</span><span class="sxs-lookup"><span data-stu-id="0abe1-151">To determine the resolution, use the <strong>PerfFreq</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="0abe1-152">Чтобы преобразовать отметку времени события в единицы 100-NS, используйте следующую формулу преобразования:</span><span class="sxs-lookup"><span data-stu-id="0abe1-152">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="0abe1-153">Скаледтиместамп = Евентрекорд. Евенсеадер. TimeStamp. Куадпарт \* 10000000,0/Логфилехеадер. Перффрек. Куадпарт</span><span class="sxs-lookup"><span data-stu-id="0abe1-153">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart \* 10000000.0 / logfileHeader.PerfFreq.QuadPart</span></span><br/> <span data-ttu-id="0abe1-154">Обратите внимание, что на старых компьютерах отметка времени может быть неточной, так как счетчик иногда пропускается из-за ошибок оборудования.</span><span class="sxs-lookup"><span data-stu-id="0abe1-154">Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="0abe1-155"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="0abe1-155"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="0abe1-156">Системное время.</span><span class="sxs-lookup"><span data-stu-id="0abe1-156">System time.</span></span> <span data-ttu-id="0abe1-157">Системное время предоставляет отметку времени, которая отслеживает изменения системных часов, например, если системные часы корректируются из-за синхронизации с сервером NTP во время выполнения трассировки, то временные метки времени в трассировке также будут перенаправлены в соответствие с новым значением системных часов.</span><span class="sxs-lookup"><span data-stu-id="0abe1-157">The system time provides a time stamp that tracks changes to the system’s clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the System Time time stamps in the trace will also jump forward to match the new setting of the system clock.</span></span> <br/>
<ul>
<li><span data-ttu-id="0abe1-158">В системах до Windows 10 метка времени, хранящаяся в событии, эквивалентна значению, возвращаемому API GetSystemTimeAsFileTime.</span><span class="sxs-lookup"><span data-stu-id="0abe1-158">On systems prior to Windows 10, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimeAsFileTime API.</span></span></li>
<li><span data-ttu-id="0abe1-159">В Windows 10 или более поздней версии метка времени, хранящаяся в событии, эквивалентна значению, возвращаемому API ЖетсистемтимепреЦисеасфилетиме.</span><span class="sxs-lookup"><span data-stu-id="0abe1-159">On Windows 10 or later, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimePreciseAsFileTime API.</span></span></li>
</ul>
<span data-ttu-id="0abe1-160">До Windows 10 разрешение этой метки времени было разрешением такта системных часов, как указано элементом Тимерресолутион в TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="0abe1-160">Prior to Windows 10, the resolution of this time stamp was the resolution of a system clock tick, as indicated by the TimerResolution member of TRACE_LOGFILE_HEADER.</span></span> <span data-ttu-id="0abe1-161">Начиная с Windows 10, разрешение этой метки времени является разрешением счетчика производительности, как указано элементом Перффрек в TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="0abe1-161">Starting with Windows 10, the resolution of this time stamp is the performance counter resolution, as indicated by the PerfFreq member of TRACE_LOGFILE_HEADER.</span></span><br/> <span data-ttu-id="0abe1-162">Чтобы преобразовать отметку времени события в единицы 100-NS, используйте следующую формулу преобразования:</span><span class="sxs-lookup"><span data-stu-id="0abe1-162">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="0abe1-163">Скаледтиместамп = Евентрекорд. Евенсеадер. TimeStamp. Куадпарт</span><span class="sxs-lookup"><span data-stu-id="0abe1-163">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart</span></span><br/> <span data-ttu-id="0abe1-164">Обратите внимание, что когда события фиксируются в системе под управлением операционной системы до Windows 10, если объем событий высок, разрешение системного времени может быть недостаточно точным для определения последовательности событий.</span><span class="sxs-lookup"><span data-stu-id="0abe1-164">Note that when events are captured on a system running an OS prior to Windows 10, if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events.</span></span> <span data-ttu-id="0abe1-165">В этом случае набор событий будет иметь одинаковую отметку времени, но порядок, в котором трассировки событий Windows доставляет события, может быть неверным.</span><span class="sxs-lookup"><span data-stu-id="0abe1-165">In this case, a set of events will have the same time stamp, but the order in which ETW delivers the events may not be correct.</span></span> <span data-ttu-id="0abe1-166">Начиная с Windows 10, штамп времени записывается с дополнительной точностью, хотя некоторые нестабильность могут возникать в случаях, когда системные часы были скорректированы во время записи трассировки.</span><span class="sxs-lookup"><span data-stu-id="0abe1-166">Starting with Windows 10, the time stamp is captured with additional precision, though some instability may still occur in cases where the system clock was adjusted while the trace was being captured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="0abe1-167"><dt>3-5</dt> </span><span class="sxs-lookup"><span data-stu-id="0abe1-167"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="0abe1-168">Счетчик циклов ЦП.</span><span class="sxs-lookup"><span data-stu-id="0abe1-168">CPU cycle counter.</span></span> <span data-ttu-id="0abe1-169">Счетчик ЦП имеет наивысшую отметку времени разрешения и является наименьшим ресурсоемким ресурсом.</span><span class="sxs-lookup"><span data-stu-id="0abe1-169">The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve.</span></span> <span data-ttu-id="0abe1-170">Однако счетчик ЦП является ненадежным и не должен использоваться в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="0abe1-170">However, the CPU counter is unreliable and should not be used in production.</span></span> <span data-ttu-id="0abe1-171">Например, на некоторых компьютерах таймеры изменяют частоту из-за температурных и энергосберегающих изменений, а также в некоторых состояниях.</span><span class="sxs-lookup"><span data-stu-id="0abe1-171">For example, on some computers, the timers will change frequency due to thermal and power changes, in addition to stopping in some states.</span></span><br/> <span data-ttu-id="0abe1-172">Чтобы определить разрешение, используйте член <strong>кпуспидинмхз</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> при использовании события.</span><span class="sxs-lookup"><span data-stu-id="0abe1-172">To determine the resolution, use the <strong>CpuSpeedInMHz</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="0abe1-173">Если оборудование не поддерживает этот тип часов, ETW использует системное время.</span><span class="sxs-lookup"><span data-stu-id="0abe1-173">If your hardware does not support this clock type, ETW uses system time.</span></span><br/> <span data-ttu-id="0abe1-174"><strong>Windows Server 2003, Windows XP с пакетом обновления 1 (SP1) и Windows XP:</strong> Это значение не поддерживается, оно представлено в Windows Server 2003 с пакетом обновления 1 (SP1) и Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="0abe1-174"><strong>Windows Server 2003, Windows XP with SP1 and Windows XP:</strong> This value is not supported, it was introduced in Windows Server 2003 with SP1 and Windows XP with SP2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0abe1-175">**Windows 2000:** Элемент **ClientContext** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0abe1-175">**Windows 2000:** The **ClientContext** member is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0abe1-176">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="0abe1-176">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="0abe1-177">Должен содержать **флаг вноде с \_ \_ трассировкой \_** , чтобы указать, что структура содержит сведения о трассировке событий.</span><span class="sxs-lookup"><span data-stu-id="0abe1-177">Must contain **WNODE\_FLAG\_TRACED\_GUID** to indicate that the structure contains event tracing information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0abe1-178">Примечания</span><span class="sxs-lookup"><span data-stu-id="0abe1-178">Remarks</span></span>

<span data-ttu-id="0abe1-179">Не забудьте инициализировать память для этой структуры до нуля перед установкой любых элементов.</span><span class="sxs-lookup"><span data-stu-id="0abe1-179">Be sure to initialize the memory for this structure to zero before setting any members.</span></span>

<span data-ttu-id="0abe1-180">Чтобы преобразовать метку времени ETW в FILETIME, выполните следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="0abe1-180">To convert an ETW timestamp into a FILETIME, use the following procedure:</span></span>

<dl> 1. <span data-ttu-id="0abe1-181">Для каждого обрабатываемого сеанса или файла журнала (т. е. для \_ каждого \_ журнала трассировки событий) следует проверить поле файл_журнала. процесстрацемоде, чтобы определить, \_ установлен ли флаг " \_ \_ необработанная \_ Метка времени трассировки процесса".</span><span class="sxs-lookup"><span data-stu-id="0abe1-181">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.ProcessTraceMode field to determine whether the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag is set.</span></span> <span data-ttu-id="0abe1-182">По умолчанию этот флаг не установлен.</span><span class="sxs-lookup"><span data-stu-id="0abe1-182">By default, this flag is not set.</span></span> <span data-ttu-id="0abe1-183">Если этот флаг не установлен, среда выполнения ETW автоматически преобразует метку времени каждой \_ записи события в FILETIME перед отправкой \_ записи события в функцию евентрекордкаллбакк, поэтому дополнительная обработка не требуется.</span><span class="sxs-lookup"><span data-stu-id="0abe1-183">If this flag is not set, the ETW runtime will automatically convert the timestamp of each EVENT\_RECORD into a FILETIME before sending the EVENT\_RECORD to your EventRecordCallback function, so no additional processing is needed.</span></span> <span data-ttu-id="0abe1-184">Следующие шаги следует использовать только в том случае, если трассировка обрабатывается с \_ \_ \_ \_ установленным флагом метки времени необработанного режима трассировки процесса.</span><span class="sxs-lookup"><span data-stu-id="0abe1-184">The following steps should only be used if the trace is being processed with the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag set.</span></span>  
2. <span data-ttu-id="0abe1-185">Для каждого обрабатываемого сеанса или файла журнала (т. е. для \_ каждого \_ журнала трассировки событий) Проверьте поле файл_журнала. Логфилехеадер. ресерведфлагс, чтобы определить шкалу времени для файла журнала.</span><span class="sxs-lookup"><span data-stu-id="0abe1-185">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.LogfileHeader.ReservedFlags field to determine the time stamp scale for the log file.</span></span> <span data-ttu-id="0abe1-186">В зависимости от значения Ресерведфлагс выполните одно из следующих действий, чтобы определить значение, которое будет использоваться для Тиместампскале на оставшихся шагах.</span><span class="sxs-lookup"><span data-stu-id="0abe1-186">Based on the value of ReservedFlags, follow one of these steps to determine the value to use for timeStampScale in the remaining steps:</span></span> <dl> <span data-ttu-id="0abe1-187">a.</span><span class="sxs-lookup"><span data-stu-id="0abe1-187">a.</span></span> <span data-ttu-id="0abe1-188">Если Ресерведфлагс = = 1 (QPC): DOUBLE Тиместампскале = 10000000,0/файл_журнала. Логфилехеадер. Перффрек. Куадпарт;</span><span class="sxs-lookup"><span data-stu-id="0abe1-188">If ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;</span></span>  
<span data-ttu-id="0abe1-189">b.</span><span class="sxs-lookup"><span data-stu-id="0abe1-189">b.</span></span> <span data-ttu-id="0abe1-190">Если Ресерведфлагс = = 2 (системное время): DOUBLE Тиместампскале = 1,0;</span><span class="sxs-lookup"><span data-stu-id="0abe1-190">If ReservedFlags == 2 (System time): DOUBLE timeStampScale = 1.0;</span></span>  
<span data-ttu-id="0abe1-191">Обратите внимание, что оставшиеся шаги не нужны для событий, использующих системное время, так как события уже содержат отметки времени в единицах FILETIME.</span><span class="sxs-lookup"><span data-stu-id="0abe1-191">Note that the remaining steps are unnecessary for events using system time, since the events already provide their time stamps in FILETIME units.</span></span> <span data-ttu-id="0abe1-192">Оставшиеся шаги будут работать, но не нужны, и в них будет представлено небольшое сообщение об ошибке округления.</span><span class="sxs-lookup"><span data-stu-id="0abe1-192">The remaining steps will work but are unnecessary and will introduce a small rounding error.</span></span>  
<span data-ttu-id="0abe1-193">c.</span><span class="sxs-lookup"><span data-stu-id="0abe1-193">c.</span></span> <span data-ttu-id="0abe1-194">Если Ресерведфлагс = = 3 (счетчик циклов ЦП): DOUBLE Тиместампскале = 10,0/файл_журнала. Логфилехеадер. Кпуспидинмхз;</span><span class="sxs-lookup"><span data-stu-id="0abe1-194">If ReservedFlags == 3 (CPU cycle counter): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;</span></span>  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a><span data-ttu-id="0abe1-195">Требования</span><span class="sxs-lookup"><span data-stu-id="0abe1-195">Requirements</span></span>



| <span data-ttu-id="0abe1-196">Требование</span><span class="sxs-lookup"><span data-stu-id="0abe1-196">Requirement</span></span> | <span data-ttu-id="0abe1-197">Значение</span><span class="sxs-lookup"><span data-stu-id="0abe1-197">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0abe1-198">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0abe1-198">Minimum supported client</span></span><br/> | <span data-ttu-id="0abe1-199">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0abe1-199">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                   |
| <span data-ttu-id="0abe1-200">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0abe1-200">Minimum supported server</span></span><br/> | <span data-ttu-id="0abe1-201">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="0abe1-201">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                         |
| <span data-ttu-id="0abe1-202">Header</span><span class="sxs-lookup"><span data-stu-id="0abe1-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="0abe1-203"><dt>Вмистр. h</dt></span><span class="sxs-lookup"><span data-stu-id="0abe1-203"><dt>Wmistr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0abe1-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0abe1-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abe1-205">*контролкаллбакк*</span><span class="sxs-lookup"><span data-stu-id="0abe1-205">*ControlCallback*</span></span>](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[<span data-ttu-id="0abe1-206">**\_Свойства трассировки \_ событий**</span><span class="sxs-lookup"><span data-stu-id="0abe1-206">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="0abe1-207">**жеттрацелогжерхандле**</span><span class="sxs-lookup"><span data-stu-id="0abe1-207">**GetTraceLoggerHandle**</span></span>](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[<span data-ttu-id="0abe1-208">**БОЛЬШОЕ \_ целое число**</span><span class="sxs-lookup"><span data-stu-id="0abe1-208">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
