---
description: '\_Класс заданий CIM представляет собой единицу работы для системы, например задание печати. Задание отличается от процесса, так как задание может быть запланировано.'
ms.assetid: a689230e-2a62-4f0d-9961-9bbc055d3c6e
ms.tgt_platform: multiple
title: Класс CIM_Job (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.Caption
- CIM_Job.Description
- CIM_Job.InstallDate
- CIM_Job.Name
- CIM_Job.Status
- CIM_Job.ElapsedTime
- CIM_Job.JobStatus
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.StartTime
- CIM_Job.TimeSubmitted
- CIM_Job.UntilTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd527474309802a4c6d2315d8a9e61b6733e70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141710"
---
# <a name="cim_job-class-cimwin32-wmi-providers"></a><span data-ttu-id="6b857-104">Класс CIM_Job (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="6b857-104">CIM_Job class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="6b857-105">Класс **\_ заданий CIM** представляет собой единицу работы для системы, например задание печати.</span><span class="sxs-lookup"><span data-stu-id="6b857-105">The **CIM\_Job** class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="6b857-106">Задание отличается от процесса, так как задание может быть запланировано.</span><span class="sxs-lookup"><span data-stu-id="6b857-106">A job is distinct from a process because a job can be scheduled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b857-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6b857-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b857-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b857-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6b857-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6b857-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6b857-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6b857-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b857-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b857-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C564-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
};
```

## <a name="members"></a><span data-ttu-id="6b857-112">Члены</span><span class="sxs-lookup"><span data-stu-id="6b857-112">Members</span></span>

<span data-ttu-id="6b857-113">Класс **\_ заданий CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6b857-113">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="6b857-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b857-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b857-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b857-115">Properties</span></span>

<span data-ttu-id="6b857-116">Класс **\_ заданий CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6b857-116">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b857-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6b857-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b857-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b857-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6b857-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6b857-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6b857-121">A short textual description of the object.</span></span>

<span data-ttu-id="6b857-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b857-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b857-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b857-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b857-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b857-126">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="6b857-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6b857-127">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6b857-127">A textual description of the object.</span></span>

<span data-ttu-id="6b857-128">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b857-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b857-129">**елапседтиме**</span><span class="sxs-lookup"><span data-stu-id="6b857-129">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-130">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b857-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b857-132">Время выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="6b857-132">Length of time the job has been executing.</span></span>

</dd> <dt>

<span data-ttu-id="6b857-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6b857-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-134">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b857-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b857-136">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="6b857-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6b857-137">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="6b857-137">Indicates when the object was installed.</span></span> <span data-ttu-id="6b857-138">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="6b857-138">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6b857-139">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b857-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b857-140">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="6b857-140">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b857-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b857-143">Произвольная строка, представляющая состояние задания.</span><span class="sxs-lookup"><span data-stu-id="6b857-143">Free-form string that represents the job status.</span></span>

</dd> <dt>

<span data-ttu-id="6b857-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="6b857-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b857-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b857-147">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="6b857-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6b857-148">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="6b857-148">Label by which the object is known.</span></span> <span data-ttu-id="6b857-149">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="6b857-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6b857-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b857-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b857-151">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="6b857-151">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b857-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b857-154">Пользователь получает уведомление о завершении задания или сбое.</span><span class="sxs-lookup"><span data-stu-id="6b857-154">User is notified upon job completion or failure.</span></span>

</dd> <dt>

<span data-ttu-id="6b857-155">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="6b857-155">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b857-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b857-158">Пользователь, отправивший задание.</span><span class="sxs-lookup"><span data-stu-id="6b857-158">User who submitted the job.</span></span>

</dd> <dt>

<span data-ttu-id="6b857-159">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="6b857-159">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b857-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b857-162">Важность выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="6b857-162">Importance of a job's execution.</span></span>

</dd> <dt>

<span data-ttu-id="6b857-163">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="6b857-163">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-164">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b857-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b857-166">Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="6b857-166">Time that the job began.</span></span>

</dd> <dt>

<span data-ttu-id="6b857-167">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6b857-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b857-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b857-170">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="6b857-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6b857-171">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6b857-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="6b857-172">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="6b857-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6b857-173">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="6b857-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6b857-174">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="6b857-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6b857-175">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="6b857-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6b857-176">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="6b857-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6b857-177">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="6b857-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6b857-178">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b857-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6b857-179">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="6b857-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6b857-180">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="6b857-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6b857-181">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="6b857-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6b857-182">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="6b857-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b857-183">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6b857-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6b857-184">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6b857-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6b857-185">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6b857-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6b857-186">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="6b857-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6b857-187">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="6b857-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6b857-188">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="6b857-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6b857-189">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="6b857-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6b857-190">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="6b857-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6b857-191">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="6b857-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b857-192">**тимесубмиттед**</span><span class="sxs-lookup"><span data-stu-id="6b857-192">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-193">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b857-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b857-195">Время отправки задания.</span><span class="sxs-lookup"><span data-stu-id="6b857-195">Time that the job was submitted.</span></span>

</dd> <dt>

<span data-ttu-id="6b857-196">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="6b857-196">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b857-197">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b857-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b857-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b857-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b857-199">Время, когда задание является недопустимым или должно быть остановлено.</span><span class="sxs-lookup"><span data-stu-id="6b857-199">Time at which the job is invalid or should be stopped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b857-200">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b857-200">Remarks</span></span>

<span data-ttu-id="6b857-201">Класс **\_ задания CIM** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b857-201">The **CIM\_Job** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="6b857-202">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6b857-202">WMI does not implement this class.</span></span> <span data-ttu-id="6b857-203">Классы, производные **от \_ задания CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6b857-203">For classes derived from **CIM\_Job**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6b857-204">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b857-204">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b857-205">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6b857-205">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b857-206">Требования</span><span class="sxs-lookup"><span data-stu-id="6b857-206">Requirements</span></span>



| <span data-ttu-id="6b857-207">Требование</span><span class="sxs-lookup"><span data-stu-id="6b857-207">Requirement</span></span> | <span data-ttu-id="6b857-208">Значение</span><span class="sxs-lookup"><span data-stu-id="6b857-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b857-209">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b857-209">Minimum supported client</span></span><br/> | <span data-ttu-id="6b857-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b857-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b857-211">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b857-211">Minimum supported server</span></span><br/> | <span data-ttu-id="6b857-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b857-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b857-213">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b857-213">Namespace</span></span><br/>                | <span data-ttu-id="6b857-214">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6b857-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b857-215">MOF</span><span class="sxs-lookup"><span data-stu-id="6b857-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b857-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b857-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b857-217">DLL</span><span class="sxs-lookup"><span data-stu-id="6b857-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b857-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b857-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b857-219">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b857-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b857-220">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="6b857-220">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

