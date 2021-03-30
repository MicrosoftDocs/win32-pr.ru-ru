---
description: Логический элемент, представляющий выполняемую единицу работы, например скрипт или задание печати. Задание отличается от процесса, так как задание может быть запланировано или поставлено в очередь, а его выполнение не ограничивается одной системой.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: Класс CIM_Job (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999036"
---
# <a name="cim_job-class-hyper-v-management"></a><span data-ttu-id="8985e-104">Класс CIM_Job (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="8985e-104">CIM_Job class (Hyper-V management)</span></span>

<span data-ttu-id="8985e-105">Логический элемент, представляющий выполняемую единицу работы, например скрипт или задание печати.</span><span class="sxs-lookup"><span data-stu-id="8985e-105">A logical element that represents a unit of work to execute, such as a script or a print job.</span></span> <span data-ttu-id="8985e-106">Задание отличается от процесса, так как задание может быть запланировано или поставлено в очередь, а его выполнение не ограничивается одной системой.</span><span class="sxs-lookup"><span data-stu-id="8985e-106">A job is distinct from a process because a job can be scheduled or queued, and its execution is not limited to a single system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8985e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8985e-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a><span data-ttu-id="8985e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8985e-108">Members</span></span>

<span data-ttu-id="8985e-109">Класс **\_ заданий CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8985e-109">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="8985e-110">Методы</span><span class="sxs-lookup"><span data-stu-id="8985e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8985e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="8985e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8985e-112">Методы</span><span class="sxs-lookup"><span data-stu-id="8985e-112">Methods</span></span>

<span data-ttu-id="8985e-113">Класс **\_ заданий CIM** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="8985e-113">The **CIM\_Job** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8985e-114">Метод</span><span class="sxs-lookup"><span data-stu-id="8985e-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8985e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="8985e-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8985e-116"><a href="cim-job-killjob.md"><strong>киллжоб</strong></a></span><span class="sxs-lookup"><span data-stu-id="8985e-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8985e-117">Этот метод является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="8985e-117">This method is deprecated.</span></span> <span data-ttu-id="8985e-118">Вместо этого используйте метод <strong>RequestStateChange</strong> .</span><span class="sxs-lookup"><span data-stu-id="8985e-118">Instead, use the <strong>RequestStateChange</strong> method.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8985e-119">Нерекомендуемое описание: завершает задание.</span><span class="sxs-lookup"><span data-stu-id="8985e-119">Deprecated description: Shuts down a job.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="8985e-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="8985e-120">Properties</span></span>

<span data-ttu-id="8985e-121">Класс **\_ заданий CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8985e-121">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8985e-122">**делетеонкомплетион**</span><span class="sxs-lookup"><span data-stu-id="8985e-122">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-123">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8985e-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8985e-125">**Значение true** , чтобы удалить задание после завершения; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8985e-125">**True** to delete the job upon completion; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="8985e-126">Это свойство не удаляет задания, которые были завершены до того, как это свойство будет установлено в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="8985e-126">This property will not delete jobs that complete before this property is set to **True**.</span></span>

 

</dd> <dt>

<span data-ttu-id="8985e-127">**елапседтиме**</span><span class="sxs-lookup"><span data-stu-id="8985e-127">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-128">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8985e-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8985e-130">Длительность выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-130">The duration for which the job has run.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-131">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8985e-131">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-132">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8985e-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8985e-134">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**ErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="8985e-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-135">Код ошибки, зависящий от поставщика, который фиксирует сведения об обработке повторяющихся заданий.</span><span class="sxs-lookup"><span data-stu-id="8985e-135">A vendor-specific error code that captures processing information for recurring jobs.</span></span> <span data-ttu-id="8985e-136">Если задание завершилось без ошибок, значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8985e-136">The value must be set to zero if the job completed without error.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-137">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8985e-137">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8985e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8985e-140">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="8985e-140">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-141">Строка произвольной формы, содержащая описание соответствующего кода ошибки в свойстве **ErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="8985e-141">A free-form string that contains a description of the corresponding error code in the **ErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-142">**жобрунтимес**</span><span class="sxs-lookup"><span data-stu-id="8985e-142">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8985e-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8985e-145">Количество запусков задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-145">The number of times to run the job.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-146">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="8985e-146">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8985e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8985e-149">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="8985e-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-150">Строка произвольной формы, представляющая состояние задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-150">A free-form string that represents the status of the job.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-151">**локалорутктиме**</span><span class="sxs-lookup"><span data-stu-id="8985e-151">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-152">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8985e-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8985e-154">Указывает, представляют ли значения времени в свойствах **рунстартинтервал** и **унтилтиме** местное время или время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="8985e-154">Indicates whether the times in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

<span data-ttu-id="8985e-155">**Местное время** (1)</span><span class="sxs-lookup"><span data-stu-id="8985e-155">**Local Time** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

<span data-ttu-id="8985e-156">**Время в формате UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="8985e-156">**UTC Time** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8985e-157">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="8985e-157">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8985e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8985e-160">Пользователь, уведомляющий о завершении или сбое задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-160">The user to notify when a job completes or fails.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-161">**осеррековеряктион**</span><span class="sxs-lookup"><span data-stu-id="8985e-161">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8985e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8985e-164">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рековеряктион**")</span><span class="sxs-lookup"><span data-stu-id="8985e-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-165">Строка, описывающая действие восстановления, если свойство **рековеряктион** является **другим** ("1").</span><span class="sxs-lookup"><span data-stu-id="8985e-165">A string that describes the recovery action when the **RecoveryAction** property is **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="8985e-166">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="8985e-166">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8985e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8985e-169">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ овнингжобелемент**](cim-owningjobelement.md).")</span><span class="sxs-lookup"><span data-stu-id="8985e-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OwningJobElement**](cim-owningjobelement.md).")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-170">Пользователь, отправивший задание, или имя службы или метода, запросившего задание.</span><span class="sxs-lookup"><span data-stu-id="8985e-170">The user that submitted the Job, or the service or method name that requested the job.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-171">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="8985e-171">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-172">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8985e-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8985e-174">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("процент"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **Пунит** ("процент")</span><span class="sxs-lookup"><span data-stu-id="8985e-174">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-175">Процент завершенного задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-175">The percentage of the job that is complete.</span></span>

> [!Note]  
> <span data-ttu-id="8985e-176">Значение "101" не определено и будет запрещено в следующей основной редакции спецификации.</span><span class="sxs-lookup"><span data-stu-id="8985e-176">The value "101" is undefined and will be not be allowed in the next major revision of the specification.</span></span>

 

</dd> <dt>

<span data-ttu-id="8985e-177">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="8985e-177">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-178">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8985e-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-179">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8985e-180">Важность задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-180">The importance of the job.</span></span> <span data-ttu-id="8985e-181">Чем меньше число, тем выше приоритет.</span><span class="sxs-lookup"><span data-stu-id="8985e-181">The lower the number, the higher the priority.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-182">**рековеряктион**</span><span class="sxs-lookup"><span data-stu-id="8985e-182">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-183">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8985e-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8985e-185">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Осеррековеряктион**")</span><span class="sxs-lookup"><span data-stu-id="8985e-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**OtherRecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-186">Описывает действие восстановления, выполняемое при сбое выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-186">Describes the recovery action to take when a run job fails.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8985e-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8985e-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8985e-188">Неизвестно, какое действие восстановления будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="8985e-188">It is unknown as to what recovery action to take.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8985e-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="8985e-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8985e-190">Действие восстановления будет указано в свойстве **осеррековеряктион** .</span><span class="sxs-lookup"><span data-stu-id="8985e-190">The recovery action will be specified in the **OtherRecoveryAction** property.</span></span>

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span data-ttu-id="8985e-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Не продолжать** (2)</span><span class="sxs-lookup"><span data-stu-id="8985e-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8985e-192">Останавливает выполнение задания и соответствующим образом обновляет его состояние.</span><span class="sxs-lookup"><span data-stu-id="8985e-192">Stop the execution of the job and appropriately update its status.</span></span>

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span data-ttu-id="8985e-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Перейти к следующему заданию** (3)</span><span class="sxs-lookup"><span data-stu-id="8985e-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8985e-194">Перейти к следующему заданию в очереди.</span><span class="sxs-lookup"><span data-stu-id="8985e-194">Continue with the next job in the queue.</span></span>

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span data-ttu-id="8985e-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Повторно запустить задание** (4)</span><span class="sxs-lookup"><span data-stu-id="8985e-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8985e-196">Задание должно быть запущено повторно.</span><span class="sxs-lookup"><span data-stu-id="8985e-196">The job should be re-run.</span></span>

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span data-ttu-id="8985e-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Запустить задание восстановления** (5)</span><span class="sxs-lookup"><span data-stu-id="8985e-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Run Recovery Job** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8985e-198">Запустите задание, связанное с использованием отношения **рековерижоб** .</span><span class="sxs-lookup"><span data-stu-id="8985e-198">Run the Job associated using the **RecoveryJob** relationship.</span></span> <span data-ttu-id="8985e-199">Обратите внимание, что задание восстановления уже должно находиться в очереди, из которой он будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="8985e-199">Note that the recovery Job must already be in the queue from which it will run.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8985e-200">**рундай**</span><span class="sxs-lookup"><span data-stu-id="8985e-200">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-201">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="8985e-201">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8985e-203">Квалификаторы: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рунмонс**","**\_ Задание CIM**.**Рундайофвик**","**\_ Задание CIM**.**Рунстартинтервал**")</span><span class="sxs-lookup"><span data-stu-id="8985e-203">Qualifiers: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-204">Целое число, используемое в сочетании со свойством **рундайофвик** для указания дня обработки задания. или, если **рундайофвик** имеет значение 0, **рундай** указывает день месяца, когда задание обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="8985e-204">An integer that is used on conjunction with the **RunDayOfWeek** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span> <span data-ttu-id="8985e-205">Если **рундай** является отрицательным целым числом, он указывает день относительно конца месяца или, если **рундай** является положительным целым числом, он указывает день относительно начала месяца.</span><span class="sxs-lookup"><span data-stu-id="8985e-205">If **RunDay** is a negative integer, it specifies a day relative to the end of the month, or if **RunDay** is a positive integer, it specifies a day relative to the beginning of the month.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-206">**рундайофвик**</span><span class="sxs-lookup"><span data-stu-id="8985e-206">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-207">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="8985e-207">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-208">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8985e-209">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рунмонс**","**\_ Задание CIM**.**Рундай**","**\_ Задание CIM**.**Рунстартинтервал**")</span><span class="sxs-lookup"><span data-stu-id="8985e-209">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-210">Целое число, используемое в сочетании со свойством **рундай** для указания дня обработки задания. или, если **рундайофвик** имеет значение 0, **рундай** указывает день месяца, когда задание обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="8985e-210">An integer that is used on conjunction with the **RunDay** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span>

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

<span data-ttu-id="8985e-211">**-Суббота** (-7)</span><span class="sxs-lookup"><span data-stu-id="8985e-211">**-Saturday** (-7)</span></span>


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

<span data-ttu-id="8985e-212">**-Пятница** (-6)</span><span class="sxs-lookup"><span data-stu-id="8985e-212">**-Friday** (-6)</span></span>


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

<span data-ttu-id="8985e-213">**-Четверг** (-5)</span><span class="sxs-lookup"><span data-stu-id="8985e-213">**-Thursday** (-5)</span></span>


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

<span data-ttu-id="8985e-214">**Среда** (-4)</span><span class="sxs-lookup"><span data-stu-id="8985e-214">**-Wednesday** (-4)</span></span>


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

<span data-ttu-id="8985e-215">**-Вторник** (-3)</span><span class="sxs-lookup"><span data-stu-id="8985e-215">**-Tuesday** (-3)</span></span>


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

<span data-ttu-id="8985e-216">**-Понедельник** (-2)</span><span class="sxs-lookup"><span data-stu-id="8985e-216">**-Monday** (-2)</span></span>


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

<span data-ttu-id="8985e-217">**– Воскресенье** (-1)</span><span class="sxs-lookup"><span data-stu-id="8985e-217">**-Sunday** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

<span data-ttu-id="8985e-218">**Ексактдайофмонс** (0)</span><span class="sxs-lookup"><span data-stu-id="8985e-218">**ExactDayOfMonth** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="8985e-219">**Воскресенье** (1)</span><span class="sxs-lookup"><span data-stu-id="8985e-219">**Sunday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="8985e-220">**Понедельник** (2)</span><span class="sxs-lookup"><span data-stu-id="8985e-220">**Monday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="8985e-221">**Вторник** (3)</span><span class="sxs-lookup"><span data-stu-id="8985e-221">**Tuesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="8985e-222">**Среда** (4)</span><span class="sxs-lookup"><span data-stu-id="8985e-222">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="8985e-223">**Четверг** (5)</span><span class="sxs-lookup"><span data-stu-id="8985e-223">**Thursday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="8985e-224">**Пятница** (6)</span><span class="sxs-lookup"><span data-stu-id="8985e-224">**Friday** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="8985e-225">**Суббота** (7)</span><span class="sxs-lookup"><span data-stu-id="8985e-225">**Saturday** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8985e-226">**рунмонс**</span><span class="sxs-lookup"><span data-stu-id="8985e-226">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-227">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8985e-227">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-228">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8985e-229">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рундай**","**\_ Задание CIM**.**Рундайофвик**","**\_ Задание CIM**.**Рунстартинтервал**")</span><span class="sxs-lookup"><span data-stu-id="8985e-229">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-230">Месяц, когда обработано задание.</span><span class="sxs-lookup"><span data-stu-id="8985e-230">The month when the job is processed.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="8985e-231">**Январь** (0)</span><span class="sxs-lookup"><span data-stu-id="8985e-231">**January** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="8985e-232">**Февраль** (1)</span><span class="sxs-lookup"><span data-stu-id="8985e-232">**February** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="8985e-233">**Март** (2)</span><span class="sxs-lookup"><span data-stu-id="8985e-233">**March** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="8985e-234">**Апрель** (3)</span><span class="sxs-lookup"><span data-stu-id="8985e-234">**April** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="8985e-235">**Май** (4)</span><span class="sxs-lookup"><span data-stu-id="8985e-235">**May** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="8985e-236">**Июнь** (5)</span><span class="sxs-lookup"><span data-stu-id="8985e-236">**June** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="8985e-237">**Июль** (6)</span><span class="sxs-lookup"><span data-stu-id="8985e-237">**July** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="8985e-238">**Август** (7)</span><span class="sxs-lookup"><span data-stu-id="8985e-238">**August** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="8985e-239">**Сентябрь** (8)</span><span class="sxs-lookup"><span data-stu-id="8985e-239">**September** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="8985e-240">**Октябрь** (9)</span><span class="sxs-lookup"><span data-stu-id="8985e-240">**October** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="8985e-241">**Ноябрь** (10)</span><span class="sxs-lookup"><span data-stu-id="8985e-241">**November** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="8985e-242">**Декабрь** (11)</span><span class="sxs-lookup"><span data-stu-id="8985e-242">**December** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8985e-243">**рунстартинтервал**</span><span class="sxs-lookup"><span data-stu-id="8985e-243">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-244">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8985e-244">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-245">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8985e-246">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рунмонс**","**\_ Задание CIM**.**Рундай**","**\_ Задание CIM**.**Рундайофвик**","**\_ Задание CIM**.**Рунстартинтервал**")</span><span class="sxs-lookup"><span data-stu-id="8985e-246">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-247">Интервал времени после полуночи при обработке задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-247">The time interval after midnight when the job is be processed.</span></span> <span data-ttu-id="8985e-248">Например, "00000000020000.000000:000" указывает, что задание выполняется в два или более часов местного времени или в формате UTC (время в формате UTC указано с помощью свойства **локалорутктиме** ).</span><span class="sxs-lookup"><span data-stu-id="8985e-248">For example, "00000000020000.000000:000" indicates that the job is be run on or after two o'clock local time, or UTC time (UTC is specified with the **LocalOrUtcTime** property).</span></span>

</dd> <dt>

<span data-ttu-id="8985e-249">**счедуледстарттиме**</span><span class="sxs-lookup"><span data-stu-id="8985e-249">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-250">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8985e-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-251">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-251">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8985e-252">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ Задание CIM**".**Рунмонс**","**\_ Задание CIM**.**Рундай**","**\_ Задание CIM**.**Рундайофвик**","**\_ Задание CIM**.**Рунстартинтервал**")</span><span class="sxs-lookup"><span data-stu-id="8985e-252">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="8985e-253">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8985e-253">This property is deprecated.</span></span> <span data-ttu-id="8985e-254">Вместо этого рекомендуется использовать свойства **рунмонс**, **рундай**, **рундайофвик** и **рунстартинтервал** .</span><span class="sxs-lookup"><span data-stu-id="8985e-254">Instead we recommend that you use the **RunMonth**, **RunDay**, **RunDayOfWeek**, and **RunStartInterval** properties.</span></span>

 

<span data-ttu-id="8985e-255">Время, когда запланировано запуск текущего задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-255">The time when the current job is scheduled to start.</span></span> <span data-ttu-id="8985e-256">Это время может быть представлено в виде даты и времени или интервала относительно времени, когда запрашивается свойство.</span><span class="sxs-lookup"><span data-stu-id="8985e-256">This time can be represented by a date and time, or an interval relative to the time when the property is requested.</span></span> <span data-ttu-id="8985e-257">Значение, равное нулю, указывает, что задание уже исполняется.</span><span class="sxs-lookup"><span data-stu-id="8985e-257">A value of all zeroes indicates that the job is already executing.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-258">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="8985e-258">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-259">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8985e-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8985e-261">Время запуска задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-261">The time when the job started.</span></span> <span data-ttu-id="8985e-262">Это время может быть представлено датой и временем или интервалом относительно времени, когда запрашивается свойство.</span><span class="sxs-lookup"><span data-stu-id="8985e-262">This time can be represented by a date and time, or by an interval relative to the time when the property is requested.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-263">**тимесубмиттед**</span><span class="sxs-lookup"><span data-stu-id="8985e-263">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-264">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8985e-264">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8985e-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8985e-266">Время отправки задания.</span><span class="sxs-lookup"><span data-stu-id="8985e-266">The time when the job was submitted.</span></span> <span data-ttu-id="8985e-267">Значение, равное нулю, указывает, что родительский элемент не может сообщать дату и время.</span><span class="sxs-lookup"><span data-stu-id="8985e-267">A value of all zeroes indicates that the parent element is not capable of reporting a date and time.</span></span>

</dd> <dt>

<span data-ttu-id="8985e-268">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="8985e-268">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8985e-269">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8985e-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8985e-270">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8985e-270">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8985e-271">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Локалорутктиме**")</span><span class="sxs-lookup"><span data-stu-id="8985e-271">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**LocalOrUtcTime**")</span></span>
</dt> </dl>

<span data-ttu-id="8985e-272">Время, после которого задание станет недействительным или должно быть остановлено.</span><span class="sxs-lookup"><span data-stu-id="8985e-272">The time after which the job becomes invalid or should be stopped.</span></span> <span data-ttu-id="8985e-273">Время может быть представлено датой и временем или интервалом относительно времени, когда запрашивается это свойство.</span><span class="sxs-lookup"><span data-stu-id="8985e-273">The time can be represented by a date and time, or by an interval relative to the time when this property is requested.</span></span> <span data-ttu-id="8985e-274">Значение всех девяти указывает, что задание может выполняться неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="8985e-274">A value of all nines indicates that the job can run indefinitely.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8985e-275">Требования</span><span class="sxs-lookup"><span data-stu-id="8985e-275">Requirements</span></span>



| <span data-ttu-id="8985e-276">Требование</span><span class="sxs-lookup"><span data-stu-id="8985e-276">Requirement</span></span> | <span data-ttu-id="8985e-277">Значение</span><span class="sxs-lookup"><span data-stu-id="8985e-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8985e-278">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8985e-278">Minimum supported client</span></span><br/> | <span data-ttu-id="8985e-279">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8985e-279">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8985e-280">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8985e-280">Minimum supported server</span></span><br/> | <span data-ttu-id="8985e-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8985e-281">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8985e-282">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8985e-282">Namespace</span></span><br/>                | <span data-ttu-id="8985e-283">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8985e-283">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8985e-284">MOF</span><span class="sxs-lookup"><span data-stu-id="8985e-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8985e-285"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8985e-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8985e-286">DLL</span><span class="sxs-lookup"><span data-stu-id="8985e-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8985e-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8985e-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8985e-288">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8985e-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8985e-289">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="8985e-289">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

