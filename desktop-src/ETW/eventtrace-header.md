---
description: Класс типа события для события заголовка файла журнала. Этот класс содержит сведения о сеансе трассировки событий.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: Класс EventTrace_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: dea803849d6aa15c2a3a14deb850d85ade569116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542511"
---
# <a name="eventtrace_header-class"></a><span data-ttu-id="9c7ce-104">\_Класс заголовка евенттраце</span><span class="sxs-lookup"><span data-stu-id="9c7ce-104">EventTrace\_Header class</span></span>

<span data-ttu-id="9c7ce-105">Класс типа события для события заголовка файла журнала.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-105">The event type class for the log file header event.</span></span> <span data-ttu-id="9c7ce-106">Этот класс содержит сведения о сеансе трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-106">This class contains information about the event tracing session.</span></span>

<span data-ttu-id="9c7ce-107">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c7ce-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c7ce-108">Syntax</span></span>

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a><span data-ttu-id="9c7ce-109">Участники</span><span class="sxs-lookup"><span data-stu-id="9c7ce-109">Members</span></span>

<span data-ttu-id="9c7ce-110">Класс **\_ заголовка евенттраце** содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9c7ce-110">The **EventTrace\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="9c7ce-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c7ce-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c7ce-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c7ce-112">Properties</span></span>

<span data-ttu-id="9c7ce-113">Класс **\_ заголовка евенттраце** содержит следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-113">The **EventTrace\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c7ce-114">**буттиме**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-114">**BootTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-115">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-117">Квалификаторы: **вмидатаид** (17)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-117">Qualifiers: **WmiDataId** (17)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-118">Время запуска системы, в 100-наносекундных интервалах с полуночи 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-118">Time at which the system was started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-119">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-119">**BufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-122">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-122">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-123">Размер буферов сеанса трассировки событий в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-123">Size of the event tracing session's buffers, in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-124">**буфферслост**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-124">**BuffersLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-127">Квалификаторы: **вмидатаид** (21)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-127">Qualifiers: **WmiDataId** (21)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-128">Общее число потерянных буферов.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-128">Total number of buffers lost.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-129">**буфферсвриттен**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-129">**BuffersWritten**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-132">Квалификаторы: **вмидатаид** (9)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-132">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-133">Общее число буферов, записанных сеансом трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-133">Total number of buffers written by the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-134">**кпуспид**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-134">**CPUSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-137">Квалификаторы: **вмидатаид** (13)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-137">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-138">Скорость ЦП в мегагерцах.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-138">CPU speed, in megahertz.</span></span>

<span data-ttu-id="9c7ce-139">**Windows 2000:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-139">**Windows 2000:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-140">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-140">**EndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-141">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-143">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-143">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-144">Время остановки сеанса трассировки событий (в 100-наносекундных интервалах с полуночи 1 января 1601 г.).</span><span class="sxs-lookup"><span data-stu-id="9c7ce-144">Time at which the event tracing session stopped, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span> <span data-ttu-id="9c7ce-145">Это значение может быть равно 0, если вы используете события в режиме реального времени или из файла журнала, в который он по-прежнему ведет журнал событий.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-145">This value may be 0 if you are consuming events in real time or from a log file to which the provide is still logging events.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-146">**евентслост**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-146">**EventsLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-149">Квалификаторы: **вмидатаид** (12)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-150">Число событий, потерянных во время сеанса трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-150">Number of events lost during the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-151">**логфилемоде**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-151">**LogFileMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-154">Квалификаторы: **вмидатаид** (8), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-154">Qualifiers: **WmiDataId** (8), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-155">Текущий режим ведения журнала для сеанса трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-155">Current logging mode for the event tracing session.</span></span> <span data-ttu-id="9c7ce-156">Список значений см. в разделе константы режима ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-156">For a list of values, see Logging Mode Constants.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-157">**LogFileName**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-157">**LogFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-158">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-160">Квалификаторы: **вмидатаид** (15), **pointer**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-160">Qualifiers: **WmiDataId** (15), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-161">Имя файла журнала трассировки событий, содержащего события.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-161">Name of the event tracing log file that contains the events.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-162">**логжернаме**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-162">**LoggerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-163">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-165">Квалификаторы: **вмидатаид** (14), **указатель**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-165">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-166">Имя сеанса трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-166">Name of the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-167">**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-167">**MaxFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-170">Квалификаторы: **вмидатаид** (7)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-170">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-171">Максимальный размер файла журнала в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-171">Maximum size of the log file, in megabytes.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-172">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-172">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-173">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-175">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-175">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-176">Количество процессоров в системе.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-176">Number of processors on the system.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-177">**перффрек**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-177">**PerfFreq**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-178">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-180">Квалификаторы: **вмидатаид** (18)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-180">Qualifiers: **WmiDataId** (18)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-181">Частота счетчика производительности с высоким разрешением, если таковая существует.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-181">Frequency of the high-resolution performance counter, if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-182">**поинтерсизе**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-182">**PointerSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-183">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-185">Квалификаторы: **вмидатаид** (11)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-185">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-186">Размер типа данных указателя в байтах.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-186">Size of a pointer data type, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-187">**провидерверсион**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-187">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-188">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-190">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-190">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-191">Номер сборки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-191">Build number of the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-192">**ресерведфлагс**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-192">**ReservedFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-193">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-195">Квалификаторы: **вмидатаид** (20)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-195">Qualifiers: **WmiDataId** (20)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-196">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-196">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-197">**стартбуфферс**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-197">**StartBuffers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-198">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-200">Квалификаторы: **вмидатаид** (10)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-200">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-201">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-201">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-202">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-202">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-203">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-205">Квалификаторы: **вмидатаид** (19)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-205">Qualifiers: **WmiDataId** (19)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-206">Время начала сеанса трассировки событий, в 100-наносекундных интервалах с полуночи 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-206">Time at which the event tracing session started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-207">**TimerResolution**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-207">**TimerResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-208">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-210">Квалификаторы: **вмидатаид** (6)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-210">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-211">Разрешение аппаратного таймера в единицах 100 наносекунд.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-211">Resolution of the hardware timer, in units of 100 nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-212">**тимезонеинформатион**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-212">**TimeZoneInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-213">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-213">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-215">Квалификаторы: **вмидатаид** (16), **Extension ("OnPrint")**, **Max** (176)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-215">Qualifiers: **WmiDataId** (16), **Extension("NoPrint")**, **Max** (176)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-216">Структура [**\_ \_ сведений о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) , которая содержит часовой пояс для элементов **буттиме**, **EndTime** и **StartTime** .</span><span class="sxs-lookup"><span data-stu-id="9c7ce-216">A [**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) structure that contains the time zone for the **BootTime**, **EndTime** and **StartTime** members.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ce-217">**Версия**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-217">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c7ce-218">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c7ce-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c7ce-220">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="9c7ce-220">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="9c7ce-221">Номер версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-221">Version number of the operating system.</span></span> <span data-ttu-id="9c7ce-222">Начиная с младших байтов, первые два байта содержат основную версию, следующие два байта содержат дополнительную версию, следующие два байта содержат основную версию пакета обновления, а последние два байта содержат дополнительный номер версии пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-222">Starting with the low-order bytes, the first two bytes contain major version, the next two bytes contain minor version, the next two bytes contain service pack major version, and the last two bytes contain service pack minor version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c7ce-223">Примечания</span><span class="sxs-lookup"><span data-stu-id="9c7ce-223">Remarks</span></span>

<span data-ttu-id="9c7ce-224">Как правило, необходимо сохранить значения следующих свойств для последующего использования при обработке событий из файла журнала.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-224">Typically, you want to save the values for the following properties for use later when processing events from the log file.</span></span>

-   <span data-ttu-id="9c7ce-225">**Тимерресолутион**— используйте с членами **кернелтиме** и **усертиме** структуры [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) , чтобы определить стоимость ЦП для набора инструкций.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-225">**TimerResolution**—use with the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to determine the CPU cost for a set of instructions.</span></span> <span data-ttu-id="9c7ce-226">Дополнительные сведения см. в разделе "Примечания [**" \_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span><span class="sxs-lookup"><span data-stu-id="9c7ce-226">For details, see the Remarks section of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span></span>
-   <span data-ttu-id="9c7ce-227">**Поинтерсизе**— для свойств, содержащих квалификатор **указателя** , используйте это значение для определения размера указателя.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-227">**PointerSize**—for properties that contain the **Pointer** qualifier, use this value to determine the size of the pointer.</span></span> <span data-ttu-id="9c7ce-228">Обратите внимание, что это значение может быть неточным.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-228">Note that this value may not be accurate.</span></span> <span data-ttu-id="9c7ce-229">Например, на 64-разрядном компьютере 32-разрядное приложение будет регистрировать 4-байтовые указатели; Однако сеанс установит значение **поинтерсизе** равным 8.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-229">For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set **PointerSize** to 8.</span></span>
-   <span data-ttu-id="9c7ce-230">**Логфилемоде**— используйте, чтобы определить, является ли этот сеанс закрытым сеансом ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-230">**LogFileMode**—use to determine if this session is a private logger session.</span></span> <span data-ttu-id="9c7ce-231">Существуют некоторые свойства, которые не содержат данных для сеансов закрытого средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="9c7ce-231">There are some properties that do not contain data for private logger sessions.</span></span> <span data-ttu-id="9c7ce-232">Например, члены **кернелтиме** и **усертиме** структуры [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="9c7ce-232">For example, the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c7ce-233">Требования</span><span class="sxs-lookup"><span data-stu-id="9c7ce-233">Requirements</span></span>



| <span data-ttu-id="9c7ce-234">Требование</span><span class="sxs-lookup"><span data-stu-id="9c7ce-234">Requirement</span></span> | <span data-ttu-id="9c7ce-235">Значение</span><span class="sxs-lookup"><span data-stu-id="9c7ce-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9c7ce-236">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c7ce-236">Minimum supported client</span></span><br/> | <span data-ttu-id="9c7ce-237">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c7ce-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9c7ce-238">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c7ce-238">Minimum supported server</span></span><br/> | <span data-ttu-id="9c7ce-239">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c7ce-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9c7ce-240">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c7ce-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c7ce-241">**евенттрацеевент**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-241">**EventTraceEvent**</span></span>](eventtraceevent.md)
</dt> <dt>

[<span data-ttu-id="9c7ce-242">**\_заголовок файла журнала трассировки \_**</span><span class="sxs-lookup"><span data-stu-id="9c7ce-242">**TRACE\_LOGFILE\_HEADER**</span></span>](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
