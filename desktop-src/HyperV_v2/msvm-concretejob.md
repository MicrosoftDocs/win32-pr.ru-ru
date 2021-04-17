---
description: Представляет единицу работы и используется для отслеживания хода выполнения асинхронных операций.
ms.assetid: 33c13880-92a4-4367-8f0b-ecdf38b2ff8e
title: Класс Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob
- Msvm_ConcreteJob.KillJob
- Msvm_ConcreteJob.InstanceID
- Msvm_ConcreteJob.Caption
- Msvm_ConcreteJob.Description
- Msvm_ConcreteJob.ElementName
- Msvm_ConcreteJob.InstallDate
- Msvm_ConcreteJob.Name
- Msvm_ConcreteJob.OperationalStatus
- Msvm_ConcreteJob.StatusDescriptions
- Msvm_ConcreteJob.Status
- Msvm_ConcreteJob.HealthState
- Msvm_ConcreteJob.CommunicationStatus
- Msvm_ConcreteJob.DetailedStatus
- Msvm_ConcreteJob.OperatingStatus
- Msvm_ConcreteJob.PrimaryStatus
- Msvm_ConcreteJob.JobStatus
- Msvm_ConcreteJob.TimeSubmitted
- Msvm_ConcreteJob.ScheduledStartTime
- Msvm_ConcreteJob.StartTime
- Msvm_ConcreteJob.ElapsedTime
- Msvm_ConcreteJob.JobRunTimes
- Msvm_ConcreteJob.RunMonth
- Msvm_ConcreteJob.RunDay
- Msvm_ConcreteJob.RunDayOfWeek
- Msvm_ConcreteJob.RunStartInterval
- Msvm_ConcreteJob.LocalOrUtcTime
- Msvm_ConcreteJob.UntilTime
- Msvm_ConcreteJob.Notify
- Msvm_ConcreteJob.Owner
- Msvm_ConcreteJob.Priority
- Msvm_ConcreteJob.PercentComplete
- Msvm_ConcreteJob.DeleteOnCompletion
- Msvm_ConcreteJob.ErrorCode
- Msvm_ConcreteJob.ErrorDescription
- Msvm_ConcreteJob.ErrorSummaryDescription
- Msvm_ConcreteJob.RecoveryAction
- Msvm_ConcreteJob.OtherRecoveryAction
- Msvm_ConcreteJob.JobState
- Msvm_ConcreteJob.TimeOfLastStateChange
- Msvm_ConcreteJob.TimeBeforeRemoval
- Msvm_ConcreteJob.Cancellable
- Msvm_ConcreteJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2cff9594bfd39cf365020a1da8ae2f1ec0aea562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663734"
---
# <a name="msvm_concretejob-class"></a><span data-ttu-id="f306e-103">\_Класс мсвм конкретежоб</span><span class="sxs-lookup"><span data-stu-id="f306e-103">Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="f306e-104">Конкретная версия задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-104">A concrete version of job.</span></span> <span data-ttu-id="f306e-105">Этот класс представляет универсальную и экземплярную единицу работы, например пакет или задание печати, и специально используется в Hyper-V для отслеживания хода выполнения асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="f306e-105">This class represents a generic and instantiatable unit of work, such as a batch or a print job, and is specifically used in Hyper-V to track the progress of asynchronous operations.</span></span>

<span data-ttu-id="f306e-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f306e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f306e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f306e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
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
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 
                00000000000500.000000:000
              ;
  boolean  Cancellable;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="f306e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f306e-108">Members</span></span>

<span data-ttu-id="f306e-109">Класс **мсвм \_ конкретежоб** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f306e-109">The **Msvm\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="f306e-110">Методы</span><span class="sxs-lookup"><span data-stu-id="f306e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f306e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f306e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f306e-112">Методы</span><span class="sxs-lookup"><span data-stu-id="f306e-112">Methods</span></span>

<span data-ttu-id="f306e-113">Класс **мсвм \_ конкретежоб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f306e-113">The **Msvm\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="f306e-114">Метод</span><span class="sxs-lookup"><span data-stu-id="f306e-114">Method</span></span>                                                            | <span data-ttu-id="f306e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f306e-115">Description</span></span>                                                                      |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="f306e-116">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="f306e-116">**GetError**</span></span>](geterror-msvm-concretejob.md)                     | <span data-ttu-id="f306e-117">Возвращает объект ошибки для задания, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="f306e-117">Retrieves the error object for the job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="f306e-118">**жетеррорекс**</span><span class="sxs-lookup"><span data-stu-id="f306e-118">**GetErrorEx**</span></span>](geterrorex-msvm-concretejob.md)                 | <span data-ttu-id="f306e-119">Возвращает объекты ошибок для задания, если таковые существуют.</span><span class="sxs-lookup"><span data-stu-id="f306e-119">Retrieves the error objects for the job, if any exist.</span></span><br/>                |
| <span data-ttu-id="f306e-120">**киллжоб**</span><span class="sxs-lookup"><span data-stu-id="f306e-120">**KillJob**</span></span>                                                       | <span data-ttu-id="f306e-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f306e-121">This method is not supported.</span></span><br/>                                         |
| [<span data-ttu-id="f306e-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="f306e-122">**RequestStateChange**</span></span>](requeststatechange-msvm-concretejob.md) | <span data-ttu-id="f306e-123">Запрашивает изменение состояния задания на указанное состояние.</span><span class="sxs-lookup"><span data-stu-id="f306e-123">Requests that the state of the job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f306e-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="f306e-124">Properties</span></span>

<span data-ttu-id="f306e-125">Класс **мсвм \_ конкретежоб** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f306e-125">The **Msvm\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f306e-126">**Отменяемых**</span><span class="sxs-lookup"><span data-stu-id="f306e-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-127">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f306e-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-129">Указывает, можно ли отменить задание.</span><span class="sxs-lookup"><span data-stu-id="f306e-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="f306e-130">Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="f306e-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="f306e-131">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f306e-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-134">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f306e-134">A short description of the object.</span></span> <span data-ttu-id="f306e-135">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f306e-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-136">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="f306e-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-137">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-139">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="f306e-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f306e-140">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f306e-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f306e-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f306e-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-142">**делетеонкомплетион**</span><span class="sxs-lookup"><span data-stu-id="f306e-142">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f306e-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-145">Указывает, следует ли автоматически удалять задание после завершения.</span><span class="sxs-lookup"><span data-stu-id="f306e-145">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="f306e-146">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-146">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-147">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f306e-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-150">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f306e-150">A description of the object.</span></span> <span data-ttu-id="f306e-151">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f306e-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-152">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f306e-152">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-153">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-155">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="f306e-155">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f306e-156">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f306e-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f306e-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f306e-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-158">**елапседтиме**</span><span class="sxs-lookup"><span data-stu-id="f306e-158">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-159">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-161">Интервал времени, в течение которого выполнялось задание, или общее время выполнения, если задание завершено.</span><span class="sxs-lookup"><span data-stu-id="f306e-161">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="f306e-162">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-162">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f306e-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-166">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="f306e-166">A display name for the object.</span></span> <span data-ttu-id="f306e-167">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f306e-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-168">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f306e-168">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-169">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-171">Код ошибки, зависящий от поставщика.</span><span class="sxs-lookup"><span data-stu-id="f306e-171">A vendor-specific error code.</span></span> <span data-ttu-id="f306e-172">Если задание завершилось без ошибок, значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f306e-172">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="f306e-173">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-173">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-174">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f306e-174">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-177">Строка, содержащая описание ошибки поставщика.</span><span class="sxs-lookup"><span data-stu-id="f306e-177">A string that contains the vendor error description.</span></span> <span data-ttu-id="f306e-178">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-178">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-179">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="f306e-179">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f306e-182">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Задание CIM**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="f306e-182">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="f306e-183">Сводное описание ошибки, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="f306e-183">A summary description of the error, if present.</span></span> <span data-ttu-id="f306e-184">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-184">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-185">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f306e-185">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-186">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-188">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="f306e-188">The current health of the element.</span></span> <span data-ttu-id="f306e-189">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="f306e-189">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="f306e-190">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="f306e-190">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="f306e-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="f306e-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="f306e-192">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f306e-192">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-193">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-195">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f306e-195">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="f306e-196">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f306e-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f306e-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f306e-200">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="f306e-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f306e-201">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="f306e-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f306e-202">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f306e-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f306e-203">**жобрунтимес**</span><span class="sxs-lookup"><span data-stu-id="f306e-203">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-204">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f306e-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-206">Количество запусков задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-206">The number of times that the job should be run.</span></span> <span data-ttu-id="f306e-207">Значение 1 указывает, что задание не повторяется, а любое ненулевое значение указывает на ограничение на количество повторений задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-207">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="f306e-208">Ноль указывает, что количество операций, которые может обработать задание, не ограничено, но оно будет завершено либо после достижения **унтилтиме** , либо после того, как задание будет прервано вручную.</span><span class="sxs-lookup"><span data-stu-id="f306e-208">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="f306e-209">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-209">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-210">**JobState**</span><span class="sxs-lookup"><span data-stu-id="f306e-210">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-211">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-213">**JobState** — это целочисленное перечисление, указывающее операционное состояние задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-213">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="f306e-214">Он также может указывать на переходы между этими состояниями, например "завершение работы" и "Запуск".</span><span class="sxs-lookup"><span data-stu-id="f306e-214">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="f306e-215">Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f306e-215">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="f306e-216">Значение</span><span class="sxs-lookup"><span data-stu-id="f306e-216">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="f306e-217">Значение</span><span class="sxs-lookup"><span data-stu-id="f306e-217">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="f306e-218"><dt>**Новое**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-218"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="f306e-219">Задание никогда не запускалось.</span><span class="sxs-lookup"><span data-stu-id="f306e-219">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="f306e-220"><dt>**Начиная**</dt> с <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-220"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="f306e-221">Задание переходит из состояния 2 (новое), 5 (приостановлено) или 11 (служба) в состояние 4 (работает).</span><span class="sxs-lookup"><span data-stu-id="f306e-221">The job is moving from the 2 (New), 5 (Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                   |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="f306e-222"><dt>**Выполнение**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-222"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="f306e-223">Задание выполняется.</span><span class="sxs-lookup"><span data-stu-id="f306e-223">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="f306e-224"><dt>**Приостановлено**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-224"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="f306e-225">Задание остановлено, но его можно легко перезапустить.</span><span class="sxs-lookup"><span data-stu-id="f306e-225">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="f306e-226"><dt>**Завершение работы**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-226"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="f306e-227">Задание переходит в состояние 7 (завершено), 8 (завершено) или 9 (прервано).</span><span class="sxs-lookup"><span data-stu-id="f306e-227">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="f306e-228"><dt>**Завершено**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-228"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="f306e-229">Задание выполнено нормально.</span><span class="sxs-lookup"><span data-stu-id="f306e-229">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="f306e-230"><dt>**Завершено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-230"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="f306e-231">Задание остановлено запросом на изменение состояния "завершено".</span><span class="sxs-lookup"><span data-stu-id="f306e-231">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="f306e-232">Задание и все его базовые процессы завершены и могут быть перезапущены только в качестве нового задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-232">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="f306e-233">Требование перезапуска задания только в качестве нового задания зависит от конкретного задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-233">The requirement that the job be restarted only as a new job is job-specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="f306e-234"><dt>**Уничтожено**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-234"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="f306e-235">Задание остановлено запросом на изменение состояния "Kill".</span><span class="sxs-lookup"><span data-stu-id="f306e-235">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="f306e-236">Базовые процессы могут по-прежнему выполняться, а для освобождения ресурсов может потребоваться очистка.</span><span class="sxs-lookup"><span data-stu-id="f306e-236">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="f306e-237"><dt>**Исключение**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-237"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="f306e-238">Задание находится в ненормальном состоянии, что может указывать на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="f306e-238">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="f306e-239">Фактическое состояние задания может быть доступно через объекты конкретного задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-239">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="f306e-240"><dt>**Служба**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-240"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="f306e-241">Задание находится в состоянии, зависящем от поставщика, которое поддерживает обнаружение проблем, разрешение или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="f306e-241">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="f306e-242"><dt>**Зарезервировано**</dt> <dt>12 32767</dt> в формате DMTF</span><span class="sxs-lookup"><span data-stu-id="f306e-242"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="f306e-243">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f306e-243">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="f306e-244"><dt>**Поставщик Зарезервированный**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-244"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="f306e-245">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f306e-245">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="f306e-246">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="f306e-246">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-249">Строка, представляющая состояние задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-249">A string that represents the job status.</span></span> <span data-ttu-id="f306e-250">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-250">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-251">**JobType**</span><span class="sxs-lookup"><span data-stu-id="f306e-251">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-252">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-254">Указывает тип задания, отслеживаемого этим объектом.</span><span class="sxs-lookup"><span data-stu-id="f306e-254">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f306e-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f306e-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Определение виртуальной машины** (1)</span><span class="sxs-lookup"><span data-stu-id="f306e-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Define Virtual Machine** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Изменение виртуальной машины** (2)</span><span class="sxs-lookup"><span data-stu-id="f306e-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modify Virtual Machine** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Уничтожить виртуальную машину** (3)</span><span class="sxs-lookup"><span data-stu-id="f306e-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Destroy Virtual Machine** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>

<span data-ttu-id="f306e-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Изменение параметров службы управления** (4)</span><span class="sxs-lookup"><span data-stu-id="f306e-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modify Management Service Settings** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Инициализация виртуальной машины** (10)</span><span class="sxs-lookup"><span data-stu-id="f306e-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Initialize Virtual Machine** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Ожидание запуска виртуальной машины** (11)</span><span class="sxs-lookup"><span data-stu-id="f306e-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Waiting to Start Virtual Machine** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Запуск виртуальной машины** (12)</span><span class="sxs-lookup"><span data-stu-id="f306e-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Start Virtual Machine** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Выключение виртуальной машины** (13)</span><span class="sxs-lookup"><span data-stu-id="f306e-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Power Off Virtual Machine** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Сохранение виртуальной машины** (14)</span><span class="sxs-lookup"><span data-stu-id="f306e-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Save Virtual Machine** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Восстановление виртуальной машины** (15)</span><span class="sxs-lookup"><span data-stu-id="f306e-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restore Virtual Machine** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Завершение работы виртуальной машины** (16)</span><span class="sxs-lookup"><span data-stu-id="f306e-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Shut Down Virtual Machine** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Приостановить виртуальную машину** (26)</span><span class="sxs-lookup"><span data-stu-id="f306e-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Pause Virtual Machine** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Возобновление работы виртуальной машины** (27)</span><span class="sxs-lookup"><span data-stu-id="f306e-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Resume Virtual Machine** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Сброс виртуальной машины** (28)</span><span class="sxs-lookup"><span data-stu-id="f306e-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Reset Virtual Machine** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Перезагрузить виртуальную машину** (29)</span><span class="sxs-lookup"><span data-stu-id="f306e-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Reboot Virtual Machine** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="f306e-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Добавление ресурсов виртуальной машины** (30)</span><span class="sxs-lookup"><span data-stu-id="f306e-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Add Virtual Machine Resources** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="f306e-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Изменение ресурсов виртуальной машины** (31)</span><span class="sxs-lookup"><span data-stu-id="f306e-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modify Virtual Machine Resources** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="f306e-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Удаление ресурсов виртуальной машины** (32)</span><span class="sxs-lookup"><span data-stu-id="f306e-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Remove Virtual Machine Resources** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>

<span data-ttu-id="f306e-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Запрос начальной памяти виртуальной машины** (40)</span><span class="sxs-lookup"><span data-stu-id="f306e-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Request Initial Virtual Machine Memory** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Добавление памяти в виртуальную машину** (41)</span><span class="sxs-lookup"><span data-stu-id="f306e-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Add Memory to Virtual Machine** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Удаление памяти из виртуальной машины** (42)</span><span class="sxs-lookup"><span data-stu-id="f306e-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Remove Memory from Virtual Machine** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>

<span data-ttu-id="f306e-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Слияние дисков VHD** (50)</span><span class="sxs-lookup"><span data-stu-id="f306e-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Merging VHD Disks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Создание моментального снимка VSS в виртуальной машине** (51)</span><span class="sxs-lookup"><span data-stu-id="f306e-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Create VSS Snapshot inside Virtual Machine** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>

<span data-ttu-id="f306e-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Получение данных параметров импорта** (60)</span><span class="sxs-lookup"><span data-stu-id="f306e-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Get Import Setting Data** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Импорт виртуальной машины** (61)</span><span class="sxs-lookup"><span data-stu-id="f306e-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Import Virtual Machine** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Экспорт виртуальной машины** (62)</span><span class="sxs-lookup"><span data-stu-id="f306e-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Export Virtual Machine** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>

<span data-ttu-id="f306e-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Регистрация конфигурации** (63)</span><span class="sxs-lookup"><span data-stu-id="f306e-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Register Configuration** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>

<span data-ttu-id="f306e-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Отмена регистрации конфигурации** (64)</span><span class="sxs-lookup"><span data-stu-id="f306e-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Unregister Configuration** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Виртуальная машина моментальных снимков** (70)</span><span class="sxs-lookup"><span data-stu-id="f306e-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Snapshot Virtual Machine** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="f306e-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Применение моментального снимка виртуальной машины** (71)</span><span class="sxs-lookup"><span data-stu-id="f306e-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Apply Virtual Machine Snapshot** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="f306e-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Удаление моментального снимка виртуальной машины** (72)</span><span class="sxs-lookup"><span data-stu-id="f306e-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Delete Virtual Machine Snapshot** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>

<span data-ttu-id="f306e-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Очистить состояние моментального снимка виртуальной машины** (73)</span><span class="sxs-lookup"><span data-stu-id="f306e-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Clear Virtual Machine Snapshot State** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>

<span data-ttu-id="f306e-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Добавление ресурсов в пул ресурсов** (80)</span><span class="sxs-lookup"><span data-stu-id="f306e-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Add Resources to Resource Pool** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>

<span data-ttu-id="f306e-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Удаление ресурсов из пула ресурсов** (81)</span><span class="sxs-lookup"><span data-stu-id="f306e-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Remove Resources from Resource Pool** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>

<span data-ttu-id="f306e-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Изменение параметров сервера репликации** (90)</span><span class="sxs-lookup"><span data-stu-id="f306e-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modify Replication Server Settings** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="f306e-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Создание отношения репликации** (91)</span><span class="sxs-lookup"><span data-stu-id="f306e-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Create Replication Relationship** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>

<span data-ttu-id="f306e-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Изменение параметров отношений репликации** (92)</span><span class="sxs-lookup"><span data-stu-id="f306e-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modify Replication Relationship Settings** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="f306e-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Удаление отношения репликации** (93)</span><span class="sxs-lookup"><span data-stu-id="f306e-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Remove Replication Relationship** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>

<span data-ttu-id="f306e-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Запуск нестандартной начальной репликации** (94)</span><span class="sxs-lookup"><span data-stu-id="f306e-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Start Inband Initial Replication** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>

<span data-ttu-id="f306e-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Импорт репликации** (95)</span><span class="sxs-lookup"><span data-stu-id="f306e-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Import Replication** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>

<span data-ttu-id="f306e-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Репликация изменений состояния** (96)</span><span class="sxs-lookup"><span data-stu-id="f306e-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Replicate State Change** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>

<span data-ttu-id="f306e-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Инициация отработки отказа** (97)</span><span class="sxs-lookup"><span data-stu-id="f306e-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Initiate Failover** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>

<span data-ttu-id="f306e-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Отмена отработки отказа** (98)</span><span class="sxs-lookup"><span data-stu-id="f306e-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Revert Failover** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>

<span data-ttu-id="f306e-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Фиксация отработки отказа** (99)</span><span class="sxs-lookup"><span data-stu-id="f306e-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Commit Failover** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>

<span data-ttu-id="f306e-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Инититате синхронизация репликации** (100)</span><span class="sxs-lookup"><span data-stu-id="f306e-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Inititate Synced Replication** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>

<span data-ttu-id="f306e-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Отмена синхронизации репликации** (101)</span><span class="sxs-lookup"><span data-stu-id="f306e-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Cancel Synced Replication** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>

<span data-ttu-id="f306e-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Запуск реплики теста** (102)</span><span class="sxs-lookup"><span data-stu-id="f306e-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Initiate Test Replica** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>

<span data-ttu-id="f306e-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Удаление тестовой реплики** (103)</span><span class="sxs-lookup"><span data-stu-id="f306e-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Remove Test Replica** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>

<span data-ttu-id="f306e-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Обратная репликация** (104)</span><span class="sxs-lookup"><span data-stu-id="f306e-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Reverse Replication** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>

<span data-ttu-id="f306e-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Дельта-передача репликации** (105)</span><span class="sxs-lookup"><span data-stu-id="f306e-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Replication Sending Delta** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>

<span data-ttu-id="f306e-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Получение разностной репликации** (106)</span><span class="sxs-lookup"><span data-stu-id="f306e-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Replication Receiving Delta** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="f306e-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>Повторная **Синхронизация** (107)</span><span class="sxs-lookup"><span data-stu-id="f306e-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>

<span data-ttu-id="f306e-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Применение журнала изменений** (108)</span><span class="sxs-lookup"><span data-stu-id="f306e-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Apply change log** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>

<span data-ttu-id="f306e-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Завершение начальной репликации** (109)</span><span class="sxs-lookup"><span data-stu-id="f306e-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Stop Initial Replication** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>

<span data-ttu-id="f306e-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>Прерывать повторную **синхронизацию** (110)</span><span class="sxs-lookup"><span data-stu-id="f306e-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Stop Resynchronizing** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>

<span data-ttu-id="f306e-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Получение статистики реплики** (111)</span><span class="sxs-lookup"><span data-stu-id="f306e-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Get Replica statistics** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="f306e-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Подготовка к проверке согласованности** (112)</span><span class="sxs-lookup"><span data-stu-id="f306e-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Prepare for Consistency Checker** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>

<span data-ttu-id="f306e-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Средство проверки согласованности** (113)</span><span class="sxs-lookup"><span data-stu-id="f306e-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Consistency Checker** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="f306e-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Прерывать проверку согласованности** (114)</span><span class="sxs-lookup"><span data-stu-id="f306e-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Stop Consistency Checker** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>

<span data-ttu-id="f306e-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Проверка подключения репликации** (115)</span><span class="sxs-lookup"><span data-stu-id="f306e-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Test Replication Connection** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>

<span data-ttu-id="f306e-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Отправка начальной реплики** (116)</span><span class="sxs-lookup"><span data-stu-id="f306e-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Sending Initial Replica** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>

<span data-ttu-id="f306e-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Запуск повторной синхронизации начальной репликации** (117)</span><span class="sxs-lookup"><span data-stu-id="f306e-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Start Resync Initial Replication** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>

<span data-ttu-id="f306e-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Начать экспорт начальной репликации** (118)</span><span class="sxs-lookup"><span data-stu-id="f306e-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Start Export Initial Replication** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>

<span data-ttu-id="f306e-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Сброс статистики реплики** (119)</span><span class="sxs-lookup"><span data-stu-id="f306e-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Reset Replica Statistics** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>

<span data-ttu-id="f306e-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Применить зарегистрированные разности** (120)</span><span class="sxs-lookup"><span data-stu-id="f306e-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Apply Registered Deltas** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>

<span data-ttu-id="f306e-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>Повторная **Синхронизация расширенной репликации** (121)</span><span class="sxs-lookup"><span data-stu-id="f306e-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Resynchronizing Extended Replication** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>

<span data-ttu-id="f306e-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Чтение конфигурации реплики теста** (122)</span><span class="sxs-lookup"><span data-stu-id="f306e-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Reading Test Replica Configuration** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>

<span data-ttu-id="f306e-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Изменение режима репликации на основной** (123)</span><span class="sxs-lookup"><span data-stu-id="f306e-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Change the replication mode to primary** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>

<span data-ttu-id="f306e-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Инициация восстановления размещения** (124)</span><span class="sxs-lookup"><span data-stu-id="f306e-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Initiate Failback** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>

<span data-ttu-id="f306e-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Обновление набора дисков** (125)</span><span class="sxs-lookup"><span data-stu-id="f306e-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Update Disk Set** (125)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-326">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-326">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>

<span data-ttu-id="f306e-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Определение коммутатора Ethernet** (130)</span><span class="sxs-lookup"><span data-stu-id="f306e-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Define Ethernet Switch** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>

<span data-ttu-id="f306e-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Изменение параметров Ethernet-коммутатора** (131)</span><span class="sxs-lookup"><span data-stu-id="f306e-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modify Ethernet Switch Settings** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>

<span data-ttu-id="f306e-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Удаление коммутатора Ethernet** (132)</span><span class="sxs-lookup"><span data-stu-id="f306e-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Destroy Ethernet Switch** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="f306e-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Добавление ресурсов коммутатора Ethernet** (133)</span><span class="sxs-lookup"><span data-stu-id="f306e-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Add Ethernet Switch Resources** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="f306e-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Изменение ресурсов коммутатора Ethernet** (134)</span><span class="sxs-lookup"><span data-stu-id="f306e-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modify Ethernet Switch Resources** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="f306e-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Удаление ресурсов коммутатора Ethernet** (135)</span><span class="sxs-lookup"><span data-stu-id="f306e-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Remove Ethernet Switch Resources** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Проверка запланированной виртуальной машины** (140)</span><span class="sxs-lookup"><span data-stu-id="f306e-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Validate Planned Virtual Machine** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Реализация виртуальной машины** (141)</span><span class="sxs-lookup"><span data-stu-id="f306e-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizing Virtual Machine** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>

<span data-ttu-id="f306e-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Создание пула ресурсов** (150)</span><span class="sxs-lookup"><span data-stu-id="f306e-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Creating a Resource Pool** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="f306e-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Изменение родительских ресурсов пула ресурсов** (151)</span><span class="sxs-lookup"><span data-stu-id="f306e-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Changing the Parent Resources of a Resource Pool** (151)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="f306e-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Изменение параметров, не являющихся аллоктион, для пула ресурсов** (152)</span><span class="sxs-lookup"><span data-stu-id="f306e-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Changing the Non-alloction Settings of a Resource Pool** (152)</span></span>


</dt> <dd></dd> <dt>

<span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>

<span data-ttu-id="f306e-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Удаление пула ресурсов** (153)</span><span class="sxs-lookup"><span data-stu-id="f306e-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Deleting a Resource Pool** (153)</span></span>


</dt> <dd></dd> <dt>

<span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="f306e-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Включить GPU RemoteFx** (160)</span><span class="sxs-lookup"><span data-stu-id="f306e-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Enable RemoteFx GPU** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="f306e-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Отключить GPU RemoteFx** (161)</span><span class="sxs-lookup"><span data-stu-id="f306e-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Disable RemoteFx GPU** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>

<span data-ttu-id="f306e-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Изменение параметров трехмерной службы** (162)</span><span class="sxs-lookup"><span data-stu-id="f306e-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modify 3D Service Settings** (162)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-342">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-342">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>

<span data-ttu-id="f306e-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Резервная копия виртуальной машины** (170)</span><span class="sxs-lookup"><span data-stu-id="f306e-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Backup Virtual Machine** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>

<span data-ttu-id="f306e-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Интерфейс гостевой службы** (180)</span><span class="sxs-lookup"><span data-stu-id="f306e-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Guest Service Interface** (180)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-345">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-345">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>

<span data-ttu-id="f306e-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Запрос сведений о гостевом кластере** (181)</span><span class="sxs-lookup"><span data-stu-id="f306e-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Query Guest Cluster Information** (181)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-347">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-347">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>

<span data-ttu-id="f306e-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Определение коллекции** (190)</span><span class="sxs-lookup"><span data-stu-id="f306e-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Define Collection** (190)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-349">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-349">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>

<span data-ttu-id="f306e-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Уничтожение коллекции** (191)</span><span class="sxs-lookup"><span data-stu-id="f306e-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destroy Collection** (191)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-351">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-351">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>

<span data-ttu-id="f306e-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Переименование коллекции** (192)</span><span class="sxs-lookup"><span data-stu-id="f306e-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Rename Collection** (192)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-353">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-353">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>

<span data-ttu-id="f306e-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Добавление члена в коллекцию** (193)</span><span class="sxs-lookup"><span data-stu-id="f306e-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Add Member to Collection** (193)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-355">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-355">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>

<span data-ttu-id="f306e-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Удаление члена из коллекции** (194)</span><span class="sxs-lookup"><span data-stu-id="f306e-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Remove Member from Collection** (194)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-357">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-357">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>

<span data-ttu-id="f306e-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Добавить параметр в коллекцию** (195)</span><span class="sxs-lookup"><span data-stu-id="f306e-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Add Setting to Collection** (195)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-359">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-359">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>

<span data-ttu-id="f306e-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Удалить параметр из коллекции** (196)</span><span class="sxs-lookup"><span data-stu-id="f306e-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Remove Setting from Collection** (196)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-361">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-361">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>

<span data-ttu-id="f306e-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Изменение параметра в коллекции** (197)</span><span class="sxs-lookup"><span data-stu-id="f306e-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modify Setting on Collection** (197)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-363">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-363">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>

<span data-ttu-id="f306e-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Коллекция моментальных снимков** (198)</span><span class="sxs-lookup"><span data-stu-id="f306e-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Snapshot Collection** (198)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-365">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-365">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>

<span data-ttu-id="f306e-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Преобразовать моментальный снимок в опорную точку** (200)</span><span class="sxs-lookup"><span data-stu-id="f306e-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convert Snapshot to Reference Point** (200)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-367">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-367">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>

<span data-ttu-id="f306e-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Создание опорной точки** (201)</span><span class="sxs-lookup"><span data-stu-id="f306e-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Create Reference Point** (201)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-369">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-369">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>

<span data-ttu-id="f306e-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Удаление опорной точки** (202)</span><span class="sxs-lookup"><span data-stu-id="f306e-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Delete Reference Point** (202)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-371">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-371">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>

<span data-ttu-id="f306e-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Экспорт** контрольной точки (203)</span><span class="sxs-lookup"><span data-stu-id="f306e-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Export Reference Point** (203)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-373">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-373">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>

<span data-ttu-id="f306e-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Удалить связанные данные из** контрольной точки (204)</span><span class="sxs-lookup"><span data-stu-id="f306e-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Remove Associated Data from Reference Point** (204)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-375">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-375">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="f306e-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Создание опорной точки для коллекции** (205)</span><span class="sxs-lookup"><span data-stu-id="f306e-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Create Reference Point on Collection** (205)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-377">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-377">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="f306e-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Экспорт опорной точки в коллекции** (206)</span><span class="sxs-lookup"><span data-stu-id="f306e-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Export Reference Point on Collection** (206)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-379">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-379">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="f306e-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Удалить связанные данные из опорной точки в коллекции** (207)</span><span class="sxs-lookup"><span data-stu-id="f306e-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Remove Associated Data from Reference Point on Collection** (207)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-381">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-381">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="f306e-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Удаление опорной точки в коллекции** (208)</span><span class="sxs-lookup"><span data-stu-id="f306e-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Delete Reference Point on Collection** (208)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-383">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-383">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>

<span data-ttu-id="f306e-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Импорт метаданных опорной точки** (209)</span><span class="sxs-lookup"><span data-stu-id="f306e-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Import Reference Point metadata** (209)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-385">Значение, добавленное в Windows 10 в качестве контрольной **точки очистки**.</span><span class="sxs-lookup"><span data-stu-id="f306e-385">Value added in Windows 10 as **Cleanup Reference Point**.</span></span>

 

</dd> <dt>

<span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>

<span data-ttu-id="f306e-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Подключение или отключение назначаемого устройства** (260)</span><span class="sxs-lookup"><span data-stu-id="f306e-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Mount or Dismount Assignable Device** (260)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="f306e-387">Значение, добавленное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f306e-387">Value added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f306e-388">**локалорутктиме**</span><span class="sxs-lookup"><span data-stu-id="f306e-388">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-389">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-391">Указывает, представляют ли значения времени, представленные в свойствах **рунстартинтервал** и **унтилтиме** , местное время или время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="f306e-391">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="f306e-392">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="f306e-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Местное время** (1)</span><span class="sxs-lookup"><span data-stu-id="f306e-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Время в формате UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="f306e-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f306e-395">**Name**</span><span class="sxs-lookup"><span data-stu-id="f306e-395">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-396">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f306e-398">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f306e-398">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f306e-399">Отображаемое имя для этого экземпляра задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-399">The display name for this instance of a job.</span></span> <span data-ttu-id="f306e-400">Кроме того, отображаемое имя можно использовать в качестве свойства для поиска или запроса.</span><span class="sxs-lookup"><span data-stu-id="f306e-400">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="f306e-401">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f306e-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-402">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="f306e-402">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-405">Пользователь, который получает уведомление о завершении задания или сбое.</span><span class="sxs-lookup"><span data-stu-id="f306e-405">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="f306e-406">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-406">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-407">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="f306e-407">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-408">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-410">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f306e-410">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f306e-411">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f306e-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f306e-412">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f306e-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f306e-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-414">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f306e-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f306e-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-416">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f306e-416">The current statuses of the object.</span></span> <span data-ttu-id="f306e-417">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="f306e-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-418">**осеррековеряктион**</span><span class="sxs-lookup"><span data-stu-id="f306e-418">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-419">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-421">Строка, описывающая действие восстановления, если свойство **рековеряктион** экземпляра имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="f306e-421">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="f306e-422">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-422">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-423">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="f306e-423">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-426">Пользователь, отправивший задание.</span><span class="sxs-lookup"><span data-stu-id="f306e-426">The user who submitted the job.</span></span> <span data-ttu-id="f306e-427">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-427">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-428">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="f306e-428">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-429">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f306e-431">Квалификаторы: **MinValue** (0), **MaxValue** (100), **единицы** ("процент")</span><span class="sxs-lookup"><span data-stu-id="f306e-431">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="f306e-432">Процент завершения задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-432">The completion percentage of the job.</span></span> <span data-ttu-id="f306e-433">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-433">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-434">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="f306e-434">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-435">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-436">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-437">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="f306e-437">Provides high level status information.</span></span> <span data-ttu-id="f306e-438">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="f306e-438">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f306e-439">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f306e-439">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f306e-440">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f306e-440">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-441">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="f306e-441">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-442">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f306e-442">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-444">Важность выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-444">The importance of a job's execution.</span></span> <span data-ttu-id="f306e-445">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-445">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-446">**рековеряктион**</span><span class="sxs-lookup"><span data-stu-id="f306e-446">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-447">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f306e-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-448">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-449">Описывает действие восстановления, выполняемое для задания, которое не выполнялось успешно.</span><span class="sxs-lookup"><span data-stu-id="f306e-449">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="f306e-450">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-450">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="f306e-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f306e-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f306e-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Не продолжать** (2)</span><span class="sxs-lookup"><span data-stu-id="f306e-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Перейти к следующему заданию** (3)</span><span class="sxs-lookup"><span data-stu-id="f306e-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Повторно запустить задание** (4)</span><span class="sxs-lookup"><span data-stu-id="f306e-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Запустить задание восстановления** (5)</span><span class="sxs-lookup"><span data-stu-id="f306e-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f306e-457">**рундай**</span><span class="sxs-lookup"><span data-stu-id="f306e-457">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-458">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f306e-458">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-459">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f306e-460">Квалификаторы: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="f306e-460">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="f306e-461">День месяца, в который должно быть обработано задание.</span><span class="sxs-lookup"><span data-stu-id="f306e-461">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="f306e-462">Для этого свойства существуют различные интерпретации в зависимости от значения **рундайофвик**.</span><span class="sxs-lookup"><span data-stu-id="f306e-462">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="f306e-463">Если **рундайофвик** имеет значение 0, а **рундай** является положительным, **рундай** определяет день месяца, в котором обработано задание.</span><span class="sxs-lookup"><span data-stu-id="f306e-463">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="f306e-464">Например, если **рундайофвик** имеет значение 0, а **рундай** — 12, задание будет обработано на 12-<sup>й</sup> день месяца.</span><span class="sxs-lookup"><span data-stu-id="f306e-464">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="f306e-465">Если **рундайофвик** имеет значение 0, а **рундай** имеет отрицательное значение, **рундай** определяет число дней до последнего дня месяца, в котором обработано задание.</span><span class="sxs-lookup"><span data-stu-id="f306e-465">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="f306e-466">1 указывает последний день месяца, 2 — один день до последнего дня месяца и т. д.</span><span class="sxs-lookup"><span data-stu-id="f306e-466">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="f306e-467">Например, если **рундайофвик** имеет значение 0, а **рундай** — значение 1, задание будет обрабатываться в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="f306e-467">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="f306e-468">Если **рундайофвик** не равен 0, **рундайофвик** — это день недели, в который будет обработано задание, относительно **рундай**.</span><span class="sxs-lookup"><span data-stu-id="f306e-468">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="f306e-469">Например, если **рундай** имеет значение 15, а **рундайофвик** — 7 (+ Суббота), задание будет обработано в первую субботу в или после 15-<sup>го</sup> дня месяца.</span><span class="sxs-lookup"><span data-stu-id="f306e-469">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="f306e-470">Если **рундай** имеет значение 20, а **рундайофвик** — 7 (Суббота), задание будет обработано в первую субботу в течение или до 20-<sup>го</sup> дня месяца.</span><span class="sxs-lookup"><span data-stu-id="f306e-470">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="f306e-471">Если **рундай** имеет значение 1, а **рундайофвик** — 1 (воскресенье), задание будет обработано в последнем воскресенье месяца.</span><span class="sxs-lookup"><span data-stu-id="f306e-471">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="f306e-472">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-472">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-473">**рундайофвик**</span><span class="sxs-lookup"><span data-stu-id="f306e-473">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-474">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f306e-474">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-476">Положительное или отрицательное целое число, используемое в сочетании с **рундай** для обозначения дня недели или месяца, в котором обрабатывается задание.</span><span class="sxs-lookup"><span data-stu-id="f306e-476">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="f306e-477">Дополнительные сведения см. в описании свойства **рундай** .</span><span class="sxs-lookup"><span data-stu-id="f306e-477">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="f306e-478">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-478">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="f306e-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Суббота** (7)</span><span class="sxs-lookup"><span data-stu-id="f306e-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Пятница** (6)</span><span class="sxs-lookup"><span data-stu-id="f306e-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Четверг** (5)</span><span class="sxs-lookup"><span data-stu-id="f306e-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**Среда** (4)</span><span class="sxs-lookup"><span data-stu-id="f306e-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Вторник** (3)</span><span class="sxs-lookup"><span data-stu-id="f306e-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Понедельник** (2)</span><span class="sxs-lookup"><span data-stu-id="f306e-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**– Воскресенье** (1)</span><span class="sxs-lookup"><span data-stu-id="f306e-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**Ексактдайофмонс** (0)</span><span class="sxs-lookup"><span data-stu-id="f306e-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Воскресенье** (1)</span><span class="sxs-lookup"><span data-stu-id="f306e-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Понедельник** (2)</span><span class="sxs-lookup"><span data-stu-id="f306e-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Вторник** (3)</span><span class="sxs-lookup"><span data-stu-id="f306e-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Среда** (4)</span><span class="sxs-lookup"><span data-stu-id="f306e-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Четверг** (5)</span><span class="sxs-lookup"><span data-stu-id="f306e-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Пятница** (6)</span><span class="sxs-lookup"><span data-stu-id="f306e-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Суббота** (7)</span><span class="sxs-lookup"><span data-stu-id="f306e-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f306e-494">**рунмонс**</span><span class="sxs-lookup"><span data-stu-id="f306e-494">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-495">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f306e-495">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-496">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-497">Месяц, в течение которого должно быть обработано задание.</span><span class="sxs-lookup"><span data-stu-id="f306e-497">The month during which the job should be processed.</span></span> <span data-ttu-id="f306e-498">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-498">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="f306e-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Январь** (0)</span><span class="sxs-lookup"><span data-stu-id="f306e-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Февраль** (1)</span><span class="sxs-lookup"><span data-stu-id="f306e-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Март** (2)</span><span class="sxs-lookup"><span data-stu-id="f306e-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Апрель** (3)</span><span class="sxs-lookup"><span data-stu-id="f306e-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Май** (4)</span><span class="sxs-lookup"><span data-stu-id="f306e-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Июнь** (5)</span><span class="sxs-lookup"><span data-stu-id="f306e-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Июль** (6)</span><span class="sxs-lookup"><span data-stu-id="f306e-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Август** (7)</span><span class="sxs-lookup"><span data-stu-id="f306e-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Сентябрь** (8)</span><span class="sxs-lookup"><span data-stu-id="f306e-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Октябрь** (9)</span><span class="sxs-lookup"><span data-stu-id="f306e-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Ноябрь** (10)</span><span class="sxs-lookup"><span data-stu-id="f306e-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f306e-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Декабрь** (11)</span><span class="sxs-lookup"><span data-stu-id="f306e-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f306e-511">**рунстартинтервал**</span><span class="sxs-lookup"><span data-stu-id="f306e-511">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-512">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-512">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-513">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-514">Интервал времени после полуночи, когда должно быть обработано задание.</span><span class="sxs-lookup"><span data-stu-id="f306e-514">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="f306e-515">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-515">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-516">**счедуледстарттиме**</span><span class="sxs-lookup"><span data-stu-id="f306e-516">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-517">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-517">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-518">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-519">Запланированное время запуска задания (если применимо).</span><span class="sxs-lookup"><span data-stu-id="f306e-519">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="f306e-520">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-520">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-521">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-521">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-522">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-522">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-523">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-524">Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-524">The time that the job began.</span></span> <span data-ttu-id="f306e-525">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-525">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-526">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f306e-526">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-527">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f306e-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-528">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-528">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-529">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="f306e-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f306e-530">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="f306e-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-531">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f306e-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f306e-532">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-533">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f306e-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f306e-534">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="f306e-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="f306e-535">**тимебефореремовал**</span><span class="sxs-lookup"><span data-stu-id="f306e-535">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-536">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-536">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-537">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-538">Время (в минутах), в течение которого задание сохраняется после завершения выполнения, как успешно, так и в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="f306e-538">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="f306e-539">Задание должно оставаться в наличии в течение некоторого периода времени независимо от значения свойства **делетеонкомплетион** .</span><span class="sxs-lookup"><span data-stu-id="f306e-539">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="f306e-540">Значение по умолчанию — пять минут.</span><span class="sxs-lookup"><span data-stu-id="f306e-540">The default is five minutes.</span></span> <span data-ttu-id="f306e-541">Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))и всегда имеет значение 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="f306e-541">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="f306e-542">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="f306e-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-543">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-544">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-545">Дата или время последнего изменения состояния задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-545">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="f306e-546">Если состояние задания не изменилось и заполнено это свойство, то для него должно быть задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="f306e-546">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="f306e-547">Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="f306e-547">If a state change was requested but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="f306e-548">Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f306e-548">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-549">**тимесубмиттед**</span><span class="sxs-lookup"><span data-stu-id="f306e-549">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-550">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-550">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-551">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-551">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-552">Время отправки задания.</span><span class="sxs-lookup"><span data-stu-id="f306e-552">The time that the job was submitted.</span></span> <span data-ttu-id="f306e-553">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-553">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f306e-554">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="f306e-554">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f306e-555">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f306e-555">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f306e-556">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f306e-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f306e-557">Время, когда задание недопустимо или должно быть остановлено.</span><span class="sxs-lookup"><span data-stu-id="f306e-557">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="f306e-558">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f306e-558">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f306e-559">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f306e-559">Remarks</span></span>

<span data-ttu-id="f306e-560">Доступ к классу **\_ конкретежоб мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="f306e-560">Access to the **Msvm\_ConcreteJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f306e-561">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f306e-561">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f306e-562">Требования</span><span class="sxs-lookup"><span data-stu-id="f306e-562">Requirements</span></span>



| <span data-ttu-id="f306e-563">Требование</span><span class="sxs-lookup"><span data-stu-id="f306e-563">Requirement</span></span> | <span data-ttu-id="f306e-564">Значение</span><span class="sxs-lookup"><span data-stu-id="f306e-564">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f306e-565">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f306e-565">Minimum supported client</span></span><br/> | <span data-ttu-id="f306e-566">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f306e-566">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f306e-567">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f306e-567">Minimum supported server</span></span><br/> | <span data-ttu-id="f306e-568">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f306e-568">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f306e-569">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f306e-569">Namespace</span></span><br/>                | <span data-ttu-id="f306e-570">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f306e-570">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f306e-571">MOF</span><span class="sxs-lookup"><span data-stu-id="f306e-571">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f306e-572"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-572"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f306e-573">DLL</span><span class="sxs-lookup"><span data-stu-id="f306e-573">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f306e-574"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f306e-574"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f306e-575">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f306e-575">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f306e-576">**\_КОНКРЕТЕЖОБ CIM**</span><span class="sxs-lookup"><span data-stu-id="f306e-576">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="f306e-577">[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f306e-577">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f306e-578">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="f306e-578">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

