---
description: Представляет задание, созданное с помощью команды AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Класс Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072377"
---
# <a name="win32_scheduledjob-class"></a><span data-ttu-id="c8311-103">\_Класс Win32 ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="c8311-103">Win32\_ScheduledJob class</span></span>

<span data-ttu-id="c8311-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ ScheduledJob для Win32**   представляет задание, созданное с помощью команды *\*at** .</span><span class="sxs-lookup"><span data-stu-id="c8311-104">The **Win32\_ScheduledJob** [WMI class](../wmisdk/retrieving-a-class.md) represents a job created with the **AT** command.</span></span>

> [!Note]  
> <span data-ttu-id="c8311-105">Класс **Win32 \_ ScheduledJob** не представляет задание, созданное с помощью мастера запланированных заданий, из панели управления.</span><span class="sxs-lookup"><span data-stu-id="c8311-105">The **Win32\_ScheduledJob** class does not represent a job created with the Scheduled Task Wizard from the Control Panel.</span></span> <span data-ttu-id="c8311-106">Задачу, созданную WMI, нельзя изменить в пользовательском интерфейсе запланированных задач.</span><span class="sxs-lookup"><span data-stu-id="c8311-106">You cannot change a task created by WMI in the Scheduled Tasks UI.</span></span> <span data-ttu-id="c8311-107">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="c8311-107">For more information, see the Remarks section.</span></span>

 

<span data-ttu-id="c8311-108">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c8311-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c8311-109">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="c8311-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8311-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8311-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="c8311-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c8311-111">Members</span></span>

<span data-ttu-id="c8311-112">Класс **Win32 \_ ScheduledJob** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c8311-112">The **Win32\_ScheduledJob** class has these types of members:</span></span>

-   [<span data-ttu-id="c8311-113">Методы</span><span class="sxs-lookup"><span data-stu-id="c8311-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c8311-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8311-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c8311-115">Методы</span><span class="sxs-lookup"><span data-stu-id="c8311-115">Methods</span></span>

<span data-ttu-id="c8311-116">Класс **Win32 \_ ScheduledJob** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c8311-116">The **Win32\_ScheduledJob** class has these methods.</span></span>



| <span data-ttu-id="c8311-117">Метод</span><span class="sxs-lookup"><span data-stu-id="c8311-117">Method</span></span>                                                      | <span data-ttu-id="c8311-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c8311-118">Description</span></span>                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8311-119">**Создания**</span><span class="sxs-lookup"><span data-stu-id="c8311-119">**Create**</span></span>](create-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="c8311-120">Метод класса, который отправляет задание в операционную систему для выполнения в указанное будущее время и дату.</span><span class="sxs-lookup"><span data-stu-id="c8311-120">Class method that submits a job to the operating system for execution at a specified future time and date.</span></span><br/> |
| [<span data-ttu-id="c8311-121">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="c8311-121">**Delete**</span></span>](delete-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="c8311-122">Метод класса, который удаляет запланированное задание.</span><span class="sxs-lookup"><span data-stu-id="c8311-122">Class method that deletes a scheduled job.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="c8311-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8311-123">Properties</span></span>

<span data-ttu-id="c8311-124">Класс **Win32 \_ ScheduledJob** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c8311-124">The **Win32\_ScheduledJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8311-125">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c8311-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8311-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-128">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c8311-128">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-129">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c8311-129">A short textual description of the object.</span></span>

<span data-ttu-id="c8311-130">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8311-131">**Команда**</span><span class="sxs-lookup"><span data-stu-id="c8311-131">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8311-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-134">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| ")</span><span class="sxs-lookup"><span data-stu-id="c8311-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Command**")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-135">Имя команды, пакетной программы или двоичного файла (и аргументы командной строки), которые служба расписаний использует для вызова задания.</span><span class="sxs-lookup"><span data-stu-id="c8311-135">Name of the command, batch program, or binary file (and command-line arguments) that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="c8311-136">Пример: "**Defrag** **/к/ф**"</span><span class="sxs-lookup"><span data-stu-id="c8311-136">Example: "**defrag** **/q/f**"</span></span>

</dd> <dt>

<span data-ttu-id="c8311-137">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="c8311-137">**DaysOfMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8311-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-140">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетью Win32API \| [**по \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**")</span><span class="sxs-lookup"><span data-stu-id="c8311-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfMonth**")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-141">Дни месяца, в которые запланировано выполнение задания.</span><span class="sxs-lookup"><span data-stu-id="c8311-141">Days of the month when the job is scheduled to run.</span></span> <span data-ttu-id="c8311-142">Если задание планируется запускать в несколько дней месяца, эти значения можно объединить в логическое или.</span><span class="sxs-lookup"><span data-stu-id="c8311-142">If a job is scheduled to run on multiple days of the month, these values can be joined in a logical OR.</span></span> <span data-ttu-id="c8311-143">Например, если задание выполняется в первый и в 16-й день каждого месяца, значение свойства **DaysOfMonth** будет равно 1 или 32768.</span><span class="sxs-lookup"><span data-stu-id="c8311-143">For example, if a job is to run on the 1st and 16th of each month, the value of the **DaysOfMonth** property would be 1 OR 32768.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="c8311-144"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="c8311-144"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-145">-</span><span class="sxs-lookup"><span data-stu-id="c8311-145">1st</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="c8311-146"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="c8311-146"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-147">ое</span><span class="sxs-lookup"><span data-stu-id="c8311-147">2nd</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="c8311-148"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="c8311-148"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-149">3-й</span><span class="sxs-lookup"><span data-stu-id="c8311-149">3rd</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="c8311-150"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="c8311-150"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-151">4-й</span><span class="sxs-lookup"><span data-stu-id="c8311-151">4th</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="c8311-152"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="c8311-152"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-153">го</span><span class="sxs-lookup"><span data-stu-id="c8311-153">5th</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="c8311-154"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="c8311-154"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-155">шестую</span><span class="sxs-lookup"><span data-stu-id="c8311-155">6th</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="c8311-156"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="c8311-156"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-157">7</span><span class="sxs-lookup"><span data-stu-id="c8311-157">7th</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="c8311-158"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="c8311-158"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-159">ВОСЬМ</span><span class="sxs-lookup"><span data-stu-id="c8311-159">8th</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="c8311-160"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="c8311-160"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-161">го</span><span class="sxs-lookup"><span data-stu-id="c8311-161">9th</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="c8311-162"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="c8311-162"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-163">Конференции</span><span class="sxs-lookup"><span data-stu-id="c8311-163">10th</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="c8311-164"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="c8311-164"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-165">11th</span><span class="sxs-lookup"><span data-stu-id="c8311-165">11th</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="c8311-166"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="c8311-166"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-167">12th</span><span class="sxs-lookup"><span data-stu-id="c8311-167">12th</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="c8311-168"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="c8311-168"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-169">13th</span><span class="sxs-lookup"><span data-stu-id="c8311-169">13th</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="c8311-170"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="c8311-170"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-171">14</span><span class="sxs-lookup"><span data-stu-id="c8311-171">14th</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="c8311-172"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="c8311-172"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-173">15</span><span class="sxs-lookup"><span data-stu-id="c8311-173">15th</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="c8311-174"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="c8311-174"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-175">й</span><span class="sxs-lookup"><span data-stu-id="c8311-175">16th</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="c8311-176"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="c8311-176"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-177">17</span><span class="sxs-lookup"><span data-stu-id="c8311-177">17th</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="c8311-178"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="c8311-178"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-179">18</span><span class="sxs-lookup"><span data-stu-id="c8311-179">18th</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="c8311-180"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="c8311-180"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-181">й</span><span class="sxs-lookup"><span data-stu-id="c8311-181">19th</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="c8311-182"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="c8311-182"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-183">заказан</span><span class="sxs-lookup"><span data-stu-id="c8311-183">20th</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="c8311-184"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="c8311-184"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-185">21st</span><span class="sxs-lookup"><span data-stu-id="c8311-185">21st</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="c8311-186"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="c8311-186"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-187">22nd</span><span class="sxs-lookup"><span data-stu-id="c8311-187">22nd</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="c8311-188"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="c8311-188"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-189">23rd</span><span class="sxs-lookup"><span data-stu-id="c8311-189">23rd</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="c8311-190"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="c8311-190"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-191">24</span><span class="sxs-lookup"><span data-stu-id="c8311-191">24th</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="c8311-192"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="c8311-192"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-193">ая</span><span class="sxs-lookup"><span data-stu-id="c8311-193">25th</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="c8311-194"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="c8311-194"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-195">26th</span><span class="sxs-lookup"><span data-stu-id="c8311-195">26th</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="c8311-196"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="c8311-196"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-197">27</span><span class="sxs-lookup"><span data-stu-id="c8311-197">27th</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="c8311-198"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="c8311-198"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-199">28</span><span class="sxs-lookup"><span data-stu-id="c8311-199">28th</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="c8311-200"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="c8311-200"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-201">29</span><span class="sxs-lookup"><span data-stu-id="c8311-201">29th</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="c8311-202"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="c8311-202"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-203">30</span><span class="sxs-lookup"><span data-stu-id="c8311-203">30th</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="c8311-204"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="c8311-204"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="c8311-205">м</span><span class="sxs-lookup"><span data-stu-id="c8311-205">31st</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c8311-206">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="c8311-206">**DaysOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-207">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8311-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-209">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетью Win32API \| [**по \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")</span><span class="sxs-lookup"><span data-stu-id="c8311-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfWeek**")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-210">Дни недели, в которые запланировано выполнение задания.</span><span class="sxs-lookup"><span data-stu-id="c8311-210">Days of the week when a job is scheduled to run.</span></span> <span data-ttu-id="c8311-211">Если задание запланировано на несколько дней недели, значения можно объединить в логическую или.</span><span class="sxs-lookup"><span data-stu-id="c8311-211">If a job is scheduled to run on multiple days of the week, the values can be joined in a logical OR.</span></span> <span data-ttu-id="c8311-212">Например, если задание планируется запускать в понедельниках, по средам и пятницу, значение свойства **DaysOfWeek** будет равно 1 или 4 или 16.</span><span class="sxs-lookup"><span data-stu-id="c8311-212">For example, if a job is scheduled to run on Mondays, Wednesdays, and Fridays the value of the **DaysOfWeek** property would be 1 OR 4 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="c8311-213">**Понедельник** (1)</span><span class="sxs-lookup"><span data-stu-id="c8311-213">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="c8311-214">**Вторник** (2)</span><span class="sxs-lookup"><span data-stu-id="c8311-214">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="c8311-215">**Среда** (4)</span><span class="sxs-lookup"><span data-stu-id="c8311-215">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="c8311-216">**Четверг** (8)</span><span class="sxs-lookup"><span data-stu-id="c8311-216">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="c8311-217">**Пятница** (16)</span><span class="sxs-lookup"><span data-stu-id="c8311-217">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="c8311-218">**Суббота** (32)</span><span class="sxs-lookup"><span data-stu-id="c8311-218">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="c8311-219">**Воскресенье** (64)</span><span class="sxs-lookup"><span data-stu-id="c8311-219">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8311-220">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8311-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8311-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-223">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="c8311-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-224">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c8311-224">A textual description of the object.</span></span>

<span data-ttu-id="c8311-225">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8311-226">**елапседтиме**</span><span class="sxs-lookup"><span data-stu-id="c8311-226">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-227">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8311-227">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8311-229">Время выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="c8311-229">Length of time the job has been executing.</span></span>

<span data-ttu-id="c8311-230">Это свойство наследуется [**от \_ задания CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-230">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8311-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c8311-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-232">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8311-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-234">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="c8311-234">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-235">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="c8311-235">Indicates when the object was installed.</span></span> <span data-ttu-id="c8311-236">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="c8311-236">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c8311-237">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8311-238">**интерактвисдесктоп**</span><span class="sxs-lookup"><span data-stu-id="c8311-238">**InteractWithDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-239">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c8311-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-241">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures On \| [**\_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **flags** \| **Job \_ uninteractive**")</span><span class="sxs-lookup"><span data-stu-id="c8311-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_NONINTERACTIVE**")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-242">Указанное задание является интерактивным. Это означает, что пользователь может предоставить входные данные для запланированного задания во время его выполнения.</span><span class="sxs-lookup"><span data-stu-id="c8311-242">Specified job is interactive, which means that a user can give input to a scheduled job while it is executing.</span></span>

</dd> <dt>

<span data-ttu-id="c8311-243">**JobId**</span><span class="sxs-lookup"><span data-stu-id="c8311-243">**JobId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-244">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8311-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-246">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетью Win32API \| [**в \_ перечислении**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JOBID**")</span><span class="sxs-lookup"><span data-stu-id="c8311-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobId**")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-247">Идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="c8311-247">Identifying number of the job.</span></span> <span data-ttu-id="c8311-248">Он используется методами в качестве маркера для одного задания, запланированного на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="c8311-248">It is used by methods as a handle to one job being scheduled on this computer.</span></span>

</dd> <dt>

<span data-ttu-id="c8311-249">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="c8311-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-250">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8311-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-252">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры управления \| [**при \_ перечислении**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **flags** \| **Job \_ \_ Error**")</span><span class="sxs-lookup"><span data-stu-id="c8311-252">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**Flags**\|**JOB\_EXEC\_ERROR**")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-253">Состояние выполнения при последнем запланированном запуске этого задания.</span><span class="sxs-lookup"><span data-stu-id="c8311-253">Status of execution the last time this job was scheduled to run.</span></span>

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

<span data-ttu-id="c8311-254">**Успешно** ("успешно")</span><span class="sxs-lookup"><span data-stu-id="c8311-254">**Success** ("Success")</span></span>


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

<span data-ttu-id="c8311-255">**Сбой** ("сбой")</span><span class="sxs-lookup"><span data-stu-id="c8311-255">**Failure** ("Failure")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8311-256">**Name**</span><span class="sxs-lookup"><span data-stu-id="c8311-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8311-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-259">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="c8311-259">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-260">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="c8311-260">Label by which the object is known.</span></span> <span data-ttu-id="c8311-261">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="c8311-261">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c8311-262">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8311-263">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="c8311-263">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8311-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8311-266">Пользователь получает уведомление о завершении задания или сбое.</span><span class="sxs-lookup"><span data-stu-id="c8311-266">User is notified upon job completion or failure.</span></span>

<span data-ttu-id="c8311-267">Это свойство наследуется [**от \_ задания CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-267">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8311-268">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="c8311-268">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-269">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8311-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8311-271">Пользователь, отправивший задание.</span><span class="sxs-lookup"><span data-stu-id="c8311-271">User who submitted the job.</span></span>

<span data-ttu-id="c8311-272">Это свойство наследуется [**от \_ задания CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-272">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8311-273">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="c8311-273">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-274">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8311-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8311-276">Важность выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="c8311-276">Importance of a job's execution.</span></span>

<span data-ttu-id="c8311-277">Это свойство наследуется [**от \_ задания CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-277">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8311-278">**рунрепеатедли**</span><span class="sxs-lookup"><span data-stu-id="c8311-278">**RunRepeatedly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-279">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c8311-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-281">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетями Win32API \| [**по \_ сведениям**](/windows/win32/api/lmat/ns-lmat-at_info). \|  \| **Задание \_ выполняется \_ периодически**")</span><span class="sxs-lookup"><span data-stu-id="c8311-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_RUN\_PERIODICALLY**")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-282">Запланированное задание выполняется несколько раз в дни, когда запланировано задание.</span><span class="sxs-lookup"><span data-stu-id="c8311-282">Scheduled job runs repeatedly on the days that the job is scheduled.</span></span> <span data-ttu-id="c8311-283">Если задано **значение false**, задание выполняется один раз.</span><span class="sxs-lookup"><span data-stu-id="c8311-283">If **False**, then the job is run one time.</span></span>

</dd> <dt>

<span data-ttu-id="c8311-284">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="c8311-284">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-285">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8311-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-287">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетью Win32API \| [**в \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **жобтиме**")</span><span class="sxs-lookup"><span data-stu-id="c8311-287">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobTime**")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-288">Время выполнения задания в формате UTC в виде "YYYYMMDDHHMMSS". ММММММ (+-) OOO ", где" ГГГГММДД "должен быть заменен на" \* \* \* \* \* \* \* \* ".</span><span class="sxs-lookup"><span data-stu-id="c8311-288">UTC time to run the job, in the form of "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="c8311-289">Замена необходима, так как служба планирования позволяет настраивать задания только один раз или запускать в день месяца или недели.</span><span class="sxs-lookup"><span data-stu-id="c8311-289">The replacement is necessary because the scheduling service only allows jobs to be configured to run one time, or run on a day of the month or week.</span></span> <span data-ttu-id="c8311-290">Задание не может выполняться в указанную дату.</span><span class="sxs-lookup"><span data-stu-id="c8311-290">A job cannot be run on a specific date.</span></span>

<span data-ttu-id="c8311-291">Раздел "(+-) OOO" в значении свойства **StartTime** является текущим смещением для локального преобразования времени.</span><span class="sxs-lookup"><span data-stu-id="c8311-291">The "(+-)OOO" section of the **StartTime** property value is the current bias for local time translation.</span></span> <span data-ttu-id="c8311-292">Смещение — это разница между временем в формате UTC и местным временем.</span><span class="sxs-lookup"><span data-stu-id="c8311-292">The bias is the difference between the UTC time and local time.</span></span> <span data-ttu-id="c8311-293">Чтобы вычислить смещение для часового пояса, умножьте число часов, в течение которых часовой пояс составляет вперед или выше среднего времени по Гринвичу (GMT) на 60 (Используйте положительное число в часах, если часовой пояс находится впереди GMT и отрицательное число, если часовой пояс находится за GMT).</span><span class="sxs-lookup"><span data-stu-id="c8311-293">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="c8311-294">Добавьте дополнительные 60 к вычислению, если часовой пояс использует летнее время.</span><span class="sxs-lookup"><span data-stu-id="c8311-294">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="c8311-295">Например, тихоокеанское стандартное часовое пояса составляет восемь часов после GMT, поэтому он равен-420 (-8 \* 60 + 60) при использовании летнего времени и-480 (-8 \* 60), если летнее время не используется.</span><span class="sxs-lookup"><span data-stu-id="c8311-295">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="c8311-296">Можно также определить значение смещения, запросив свойство смещения класса [**\_ часового пояса Win32**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="c8311-296">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

<span data-ttu-id="c8311-297">Например: " \* \* \* \* \* \* \* \* 123000.000000-420" указывает 14,30 (2:30 вечера) PST, в котором действует летнее время.</span><span class="sxs-lookup"><span data-stu-id="c8311-297">For example: "\*\*\*\*\*\*\*\*123000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

</dd> <dt>

<span data-ttu-id="c8311-298">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c8311-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-299">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8311-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8311-301">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="c8311-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c8311-302">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c8311-302">String that indicates the current status of the object.</span></span> <span data-ttu-id="c8311-303">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="c8311-303">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c8311-304">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="c8311-304">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c8311-305">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="c8311-305">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c8311-306">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="c8311-306">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c8311-307">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="c8311-307">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c8311-308">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="c8311-308">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c8311-309">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-309">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c8311-310">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c8311-310">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c8311-311">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="c8311-311">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c8311-312">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="c8311-312">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c8311-313">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="c8311-313">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c8311-314">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c8311-314">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c8311-315">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c8311-315">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c8311-316">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c8311-316">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c8311-317">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="c8311-317">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c8311-318">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="c8311-318">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c8311-319">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="c8311-319">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c8311-320">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="c8311-320">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c8311-321">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="c8311-321">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c8311-322">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="c8311-322">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8311-323">**тимесубмиттед**</span><span class="sxs-lookup"><span data-stu-id="c8311-323">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-324">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8311-324">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8311-326">Время отправки задания.</span><span class="sxs-lookup"><span data-stu-id="c8311-326">Time that the job was submitted.</span></span>

<span data-ttu-id="c8311-327">Это свойство наследуется [**от \_ задания CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-327">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8311-328">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="c8311-328">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8311-329">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8311-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8311-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8311-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8311-331">Время, когда задание является недопустимым или должно быть остановлено.</span><span class="sxs-lookup"><span data-stu-id="c8311-331">Time at which the job is invalid or should be stopped.</span></span>

<span data-ttu-id="c8311-332">Это свойство наследуется [**от \_ задания CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-332">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8311-333">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8311-333">Remarks</span></span>

<span data-ttu-id="c8311-334">Каждое задание, запланированное для службы расписания, хранится постоянно (планировщик может запустить задание после перезагрузки) и выполняется в указанное время и день недели или месяца.</span><span class="sxs-lookup"><span data-stu-id="c8311-334">Each job scheduled against the schedule service is stored persistently (the scheduler can start a job after a reboot), and is executed at the specified time and day of the week or month.</span></span> <span data-ttu-id="c8311-335">Если компьютер неактивен или запланированная служба не запущена в указанное время, служба расписаний запускает указанное задание в следующий день в указанное время.</span><span class="sxs-lookup"><span data-stu-id="c8311-335">If the computer is not active, or if the scheduled service is not running at the specified job time, the schedule service runs the specified job on the next day at the specified time.</span></span>

<span data-ttu-id="c8311-336">Задания планируются в соответствии со временем в формате UTC с смещением смещения от среднего времени по Гринвичу (GMT). Это означает, что задание можно указать с помощью любого часового пояса.</span><span class="sxs-lookup"><span data-stu-id="c8311-336">Jobs are scheduled according to Coordinated Universal Time (UTC) with bias offset from Greenwich Mean Time (GMT), which means that a job can be specified using any time zone.</span></span> <span data-ttu-id="c8311-337">Класс **Win32 \_ ScheduledJob** Возвращает местное время со СМЕЩЕНИЕМ в формате UTC при перечислении объекта и преобразует его в местное время при создании заданий.</span><span class="sxs-lookup"><span data-stu-id="c8311-337">The **Win32\_ScheduledJob** class returns the local time with UTC offset when enumerating an object, and converts to local time when creating new jobs.</span></span> <span data-ttu-id="c8311-338">Например, задание, указанное для запуска на компьютере в Бостоне в 10:30 P.M.</span><span class="sxs-lookup"><span data-stu-id="c8311-338">For example, a job specified to run on a computer in Boston at 10:30 P.M.</span></span> <span data-ttu-id="c8311-339">Время работы с графиком в понедельник будет запланировано локально в 1:30 утра.</span><span class="sxs-lookup"><span data-stu-id="c8311-339">Monday PST time will be scheduled to run locally at 1:30 A.M.</span></span> <span data-ttu-id="c8311-340">Вторник, средство EST.</span><span class="sxs-lookup"><span data-stu-id="c8311-340">Tuesday EST.</span></span>

> [!Note]  
> <span data-ttu-id="c8311-341">Клиент должен учитывать, выполняется ли летнее время на локальном компьютере, и, если это так, вычтите смещение в 60 минут от смещения UTC.</span><span class="sxs-lookup"><span data-stu-id="c8311-341">A client must take into account whether or not daylight savings time is in operation on the local computer, and if it is, then subtract a bias of 60 minutes from the UTC offset.</span></span>

 

<span data-ttu-id="c8311-342">Класс **Win32 \_ ScheduledJob** является производным от [**\_ задания CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-342">The **Win32\_ScheduledJob** class is derived from [**CIM\_Job**](cim-job.md).</span></span> <span data-ttu-id="c8311-343">Для создания запланированного задания с помощью этого класса необходимо быть членом группы "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="c8311-343">You must be a member of the administrators group to create a scheduled job using this class.</span></span>

<span data-ttu-id="c8311-344">Класс **Win32 \_ ScheduledJob** внутренне использует протокол AT, который привязан к устаревшим данным, начиная с Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c8311-344">The **Win32\_ScheduledJob** class is internally using the AT protocol, which is bound to deprecation starting with Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="c8311-345">В качестве первого шага по умолчанию протокол AT отключен.</span><span class="sxs-lookup"><span data-stu-id="c8311-345">As a first step the AT protocol is disabled by default.</span></span> <span data-ttu-id="c8311-346">Если протокол отключен, например вызов метода [**CREATE**](create-method-in-class-win32-scheduledjob.md) для объекта **Win32 \_ ScheduledJob** , произойдет сбой с ошибкой 0x8.</span><span class="sxs-lookup"><span data-stu-id="c8311-346">If the protocol is disabled, for example calling the [**Create**](create-method-in-class-win32-scheduledjob.md) method on a **Win32\_ScheduledJob** object will fail with error 0x8.</span></span> <span data-ttu-id="c8311-347">Можно включить по протоколу обратно, добавив следующую запись реестра:</span><span class="sxs-lookup"><span data-stu-id="c8311-347">You can turn the AT protocol back on by adding the following registry entry:</span></span>

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

<span data-ttu-id="c8311-348">Возможно, потребуется перезагрузить компьютер, чтобы сделать этот параметр эффективным.</span><span class="sxs-lookup"><span data-stu-id="c8311-348">You may need to restart the machine to make the setting effective.</span></span>

<span data-ttu-id="c8311-349">Поскольку **Win32 \_ ScheduledJob** основан на API Win32 [**нетсчедулежобжетинфо**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , этот класс нельзя использовать совместно с планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c8311-349">Because **Win32\_ScheduledJob** is based on the [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) Win32 API, you cannot use this class in conjunction with the Task Scheduler.</span></span> <span data-ttu-id="c8311-350">Если вы хотите использовать планировщик задач, используйте API планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c8311-350">If you wish to use Task Scheduler, use the Task Scheduler API.</span></span> <span data-ttu-id="c8311-351">Дополнительные сведения см. в [справочнике по планировщик задач](../taskschd/task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c8311-351">For more information, see the [Task Scheduler Reference](../taskschd/task-scheduler-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c8311-352">Примеры</span><span class="sxs-lookup"><span data-stu-id="c8311-352">Examples</span></span>

<span data-ttu-id="c8311-353">Следующий пример кода на языке VBScript планирует Notepad.exe запускаться в интерактивном режиме в 1:25 на локальном компьютере каждый понедельник.</span><span class="sxs-lookup"><span data-stu-id="c8311-353">The following VBScript code example schedules Notepad.exe to run interactively at 1:25 by the local computer time every Wednesday.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a><span data-ttu-id="c8311-354">Требования</span><span class="sxs-lookup"><span data-stu-id="c8311-354">Requirements</span></span>



| <span data-ttu-id="c8311-355">Требование</span><span class="sxs-lookup"><span data-stu-id="c8311-355">Requirement</span></span> | <span data-ttu-id="c8311-356">Значение</span><span class="sxs-lookup"><span data-stu-id="c8311-356">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8311-357">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8311-357">Minimum supported client</span></span><br/> | <span data-ttu-id="c8311-358">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8311-358">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8311-359">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8311-359">Minimum supported server</span></span><br/> | <span data-ttu-id="c8311-360">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8311-360">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8311-361">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c8311-361">Namespace</span></span><br/>                | <span data-ttu-id="c8311-362">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c8311-362">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8311-363">MOF</span><span class="sxs-lookup"><span data-stu-id="c8311-363">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8311-364"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8311-364"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8311-365">DLL</span><span class="sxs-lookup"><span data-stu-id="c8311-365">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8311-366"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8311-366"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8311-367">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8311-367">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8311-368">**\_Задание CIM**</span><span class="sxs-lookup"><span data-stu-id="c8311-368">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dt>

[<span data-ttu-id="c8311-369">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="c8311-369">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c8311-370">Задачи WMI: запланированные задачи</span><span class="sxs-lookup"><span data-stu-id="c8311-370">WMI Tasks: Scheduled Tasks</span></span>](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
