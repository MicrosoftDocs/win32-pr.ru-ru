---
description: Этот класс является классом типа события для событий счетчика процесса. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Класс Process_V2_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912324"
---
# <a name="process_v2_typegroup2-class"></a><span data-ttu-id="aa426-104">\_ \_ Класс TypeGroup2 процесса v2</span><span class="sxs-lookup"><span data-stu-id="aa426-104">Process\_V2\_TypeGroup2 class</span></span>

<span data-ttu-id="aa426-105">Этот класс является классом типа события для событий счетчика процесса.</span><span class="sxs-lookup"><span data-stu-id="aa426-105">This class is the event type class for process counter events.</span></span>

<span data-ttu-id="aa426-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="aa426-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa426-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa426-107">Syntax</span></span>

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a><span data-ttu-id="aa426-108">Участники</span><span class="sxs-lookup"><span data-stu-id="aa426-108">Members</span></span>

<span data-ttu-id="aa426-109">Класс **Process \_ v2 \_ TypeGroup2** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="aa426-109">The **Process\_V2\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="aa426-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="aa426-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa426-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="aa426-111">Properties</span></span>

<span data-ttu-id="aa426-112">Класс **Process \_ v2 \_ TypeGroup2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="aa426-112">The **Process\_V2\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa426-113">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="aa426-113">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa426-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-116">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="aa426-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="aa426-117">Число используемых дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="aa426-117">Count of used handles.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-118">**пажефаулткаунт**</span><span class="sxs-lookup"><span data-stu-id="aa426-118">**PageFaultCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa426-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-121">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="aa426-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="aa426-122">Число ошибок страниц.</span><span class="sxs-lookup"><span data-stu-id="aa426-122">Count of page faults.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-123">**пажефилеусаже**</span><span class="sxs-lookup"><span data-stu-id="aa426-123">**PagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-126">Квалификаторы: Вмидатаид (12), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-126">Qualifiers: WmiDataId(12), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-127">Текущее использование файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="aa426-127">Current page file usage.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-128">**пеакпажефилеусаже**</span><span class="sxs-lookup"><span data-stu-id="aa426-128">**PeakPagefileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-129">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-131">Квалификаторы: Вмидатаид (7), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-131">Qualifiers: WmiDataId(7), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-132">Используется самый крупный размер файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="aa426-132">Largest page file size used.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-133">**пеаквиртуалсизе**</span><span class="sxs-lookup"><span data-stu-id="aa426-133">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-134">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-136">Квалификаторы: Вмидатаид (5), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-136">Qualifiers: WmiDataId(5), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-137">Используется самый крупный размер виртуальной страницы.</span><span class="sxs-lookup"><span data-stu-id="aa426-137">Largest virtual page size used.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-138">**пеакворкингсетсизе**</span><span class="sxs-lookup"><span data-stu-id="aa426-138">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-139">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-141">Квалификаторы: Вмидатаид (6), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-141">Qualifiers: WmiDataId(6), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-142">Используется самый крупный размер рабочего набора.</span><span class="sxs-lookup"><span data-stu-id="aa426-142">Largest working set size used.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-143">**приватепажекаунт**</span><span class="sxs-lookup"><span data-stu-id="aa426-143">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-144">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-146">Квалификаторы: Вмидатаид (15), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-146">Qualifiers: WmiDataId(15), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-147">Текущее число частных физических страниц.</span><span class="sxs-lookup"><span data-stu-id="aa426-147">Current private physical page count.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-148">ProcessId</span><span class="sxs-lookup"><span data-stu-id="aa426-148">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa426-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-151">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="aa426-151">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-152">Глобальный идентификатор процесса, который можно использовать для идентификации процесса.</span><span class="sxs-lookup"><span data-stu-id="aa426-152">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="aa426-153">Значение допустимо с момента создания процесса до его завершения.</span><span class="sxs-lookup"><span data-stu-id="aa426-153">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-154">**куотанонпажедпулусаже**</span><span class="sxs-lookup"><span data-stu-id="aa426-154">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-155">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-155">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-157">Квалификаторы: Вмидатаид (14), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-157">Qualifiers: WmiDataId(14), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-158">Текущее зафиксированное использование памяти без страничных операций.</span><span class="sxs-lookup"><span data-stu-id="aa426-158">Current committed non-paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-159">**куотапажедпулусаже**</span><span class="sxs-lookup"><span data-stu-id="aa426-159">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-160">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-160">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-162">Квалификаторы: Вмидатаид (13), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-162">Qualifiers: WmiDataId(13), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-163">Текущее использование выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="aa426-163">Current committed paged memory usage.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-164">**куотапеакнонпажедпулусаже**</span><span class="sxs-lookup"><span data-stu-id="aa426-164">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-165">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-165">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-167">Квалификаторы: Вмидатаид (9), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-167">Qualifiers: WmiDataId(9), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-168">Самая крупная выделенная нестраничная память.</span><span class="sxs-lookup"><span data-stu-id="aa426-168">Largest committed non-paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-169">**куотапеакпажедпулусаже**</span><span class="sxs-lookup"><span data-stu-id="aa426-169">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-170">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-170">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-172">Квалификаторы: Вмидатаид (8), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-172">Qualifiers: WmiDataId(8), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-173">Память с большим объемом выделенной страницы.</span><span class="sxs-lookup"><span data-stu-id="aa426-173">Largest committed paged memory used.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-174">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="aa426-174">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-175">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa426-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-177">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="aa426-177">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="aa426-178">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="aa426-178">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-179">**виртуалсизе**</span><span class="sxs-lookup"><span data-stu-id="aa426-179">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-180">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-180">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-182">Квалификаторы: Вмидатаид (10), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-182">Qualifiers: WmiDataId(10), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-183">Текущий размер виртуальной страницы.</span><span class="sxs-lookup"><span data-stu-id="aa426-183">Current virtual page size.</span></span>

</dd> <dt>

<span data-ttu-id="aa426-184">**воркингсетсизе**</span><span class="sxs-lookup"><span data-stu-id="aa426-184">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa426-185">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="aa426-185">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="aa426-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa426-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa426-187">Квалификаторы: Вмидатаид (11), расширение ("size")</span><span class="sxs-lookup"><span data-stu-id="aa426-187">Qualifiers: WmiDataId(11), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="aa426-188">Текущий размер рабочего набора.</span><span class="sxs-lookup"><span data-stu-id="aa426-188">Current working set size.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa426-189">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa426-189">Remarks</span></span>

<span data-ttu-id="aa426-190">Эти события регистрируются при завершении процесса.</span><span class="sxs-lookup"><span data-stu-id="aa426-190">These events are logged when the process ends.</span></span> <span data-ttu-id="aa426-191">Событие указывает, как процесс обрабатывает использование памяти.</span><span class="sxs-lookup"><span data-stu-id="aa426-191">The event indicates how a process handled memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa426-192">Требования</span><span class="sxs-lookup"><span data-stu-id="aa426-192">Requirements</span></span>



| <span data-ttu-id="aa426-193">Требование</span><span class="sxs-lookup"><span data-stu-id="aa426-193">Requirement</span></span> | <span data-ttu-id="aa426-194">Значение</span><span class="sxs-lookup"><span data-stu-id="aa426-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa426-195">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa426-195">Minimum supported client</span></span><br/> | <span data-ttu-id="aa426-196">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa426-196">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa426-197">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa426-197">Minimum supported server</span></span><br/> | <span data-ttu-id="aa426-198">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa426-198">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa426-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa426-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa426-200">**Процесс \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="aa426-200">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




