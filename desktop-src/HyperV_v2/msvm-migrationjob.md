---
description: Этот класс представляет задание операции миграции, созданное для миграции хранилища или виртуальной системы с помощью службы миграции виртуальной системы.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Класс Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683174"
---
# <a name="msvm_migrationjob-class"></a><span data-ttu-id="43bbe-103">\_Класс мсвм мигратионжоб</span><span class="sxs-lookup"><span data-stu-id="43bbe-103">Msvm\_MigrationJob class</span></span>

<span data-ttu-id="43bbe-104">Этот класс представляет задание операции миграции, созданное для миграции хранилища или виртуальной системы с помощью службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="43bbe-104">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span>

<span data-ttu-id="43bbe-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="43bbe-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="43bbe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43bbe-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
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
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="43bbe-107">Члены</span><span class="sxs-lookup"><span data-stu-id="43bbe-107">Members</span></span>

<span data-ttu-id="43bbe-108">Класс **мсвм \_ мигратионжоб** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="43bbe-108">The **Msvm\_MigrationJob** class has these types of members:</span></span>

-   [<span data-ttu-id="43bbe-109">Методы</span><span class="sxs-lookup"><span data-stu-id="43bbe-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="43bbe-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="43bbe-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="43bbe-111">Методы</span><span class="sxs-lookup"><span data-stu-id="43bbe-111">Methods</span></span>

<span data-ttu-id="43bbe-112">Класс **мсвм \_ мигратионжоб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="43bbe-112">The **Msvm\_MigrationJob** class has these methods.</span></span>



| <span data-ttu-id="43bbe-113">Метод</span><span class="sxs-lookup"><span data-stu-id="43bbe-113">Method</span></span>                                                             | <span data-ttu-id="43bbe-114">Описание</span><span class="sxs-lookup"><span data-stu-id="43bbe-114">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43bbe-115">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-115">**GetError**</span></span>](geterror-msvm-migrationjob.md)                     | <span data-ttu-id="43bbe-116">Возвращает объект ошибки для задания миграции, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="43bbe-116">Retrieves the error object for the migration job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="43bbe-117">**жетеррорекс**</span><span class="sxs-lookup"><span data-stu-id="43bbe-117">**GetErrorEx**</span></span>](geterrorex-msvm-migrationjob.md)                 | <span data-ttu-id="43bbe-118">Возвращает объекты ошибок для задания миграции, если они существуют.</span><span class="sxs-lookup"><span data-stu-id="43bbe-118">Retrieves the error objects for the migration job, if any exist.</span></span><br/>                |
| <span data-ttu-id="43bbe-119">**киллжоб**</span><span class="sxs-lookup"><span data-stu-id="43bbe-119">**KillJob**</span></span>                                                        | <span data-ttu-id="43bbe-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="43bbe-120">This method is not supported.</span></span><br/>                                                   |
| [<span data-ttu-id="43bbe-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="43bbe-121">**RequestStateChange**</span></span>](requeststatechange-msvm-migrationjob.md) | <span data-ttu-id="43bbe-122">Запрашивает изменение состояния задания миграции на указанное состояние.</span><span class="sxs-lookup"><span data-stu-id="43bbe-122">Requests that the state of the migration job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="43bbe-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="43bbe-123">Properties</span></span>

<span data-ttu-id="43bbe-124">Класс **мсвм \_ мигратионжоб** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="43bbe-124">The **Msvm\_MigrationJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43bbe-125">**Отменяемых**</span><span class="sxs-lookup"><span data-stu-id="43bbe-125">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-126">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="43bbe-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-128">Указывает, можно ли отменить задание.</span><span class="sxs-lookup"><span data-stu-id="43bbe-128">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="43bbe-129">Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="43bbe-129">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-130">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="43bbe-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-133">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="43bbe-133">A short description of the object.</span></span> <span data-ttu-id="43bbe-134">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="43bbe-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-135">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="43bbe-135">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-136">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-138">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="43bbe-138">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="43bbe-139">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="43bbe-139">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="43bbe-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="43bbe-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-141">**делетеонкомплетион**</span><span class="sxs-lookup"><span data-stu-id="43bbe-141">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="43bbe-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-144">Указывает, следует ли автоматически удалять задание после завершения.</span><span class="sxs-lookup"><span data-stu-id="43bbe-144">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="43bbe-145">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-145">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="43bbe-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-149">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="43bbe-149">A description of the object.</span></span> <span data-ttu-id="43bbe-150">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="43bbe-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-151">**дестинатионхост**</span><span class="sxs-lookup"><span data-stu-id="43bbe-151">**DestinationHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-154">Имя узла целевой платформы виртуализации, на которой выполняется миграция виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="43bbe-154">The hostname of the destination virtualization platform that the virtual system is migrating to.</span></span> <span data-ttu-id="43bbe-155">Это значение будет **равно NULL** для миграции хранилища.</span><span class="sxs-lookup"><span data-stu-id="43bbe-155">This will be **Null** for storage migration.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="43bbe-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-157">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-159">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="43bbe-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="43bbe-160">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="43bbe-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="43bbe-161">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="43bbe-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-162">**елапседтиме**</span><span class="sxs-lookup"><span data-stu-id="43bbe-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-163">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-165">Интервал времени, в течение которого выполнялось задание, или общее время выполнения, если задание завершено.</span><span class="sxs-lookup"><span data-stu-id="43bbe-165">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="43bbe-166">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="43bbe-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-170">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="43bbe-170">A display name for the object.</span></span> <span data-ttu-id="43bbe-171">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="43bbe-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="43bbe-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-173">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-175">Код ошибки, зависящий от поставщика.</span><span class="sxs-lookup"><span data-stu-id="43bbe-175">A vendor-specific error code.</span></span> <span data-ttu-id="43bbe-176">Если задание завершилось без ошибок, значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="43bbe-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="43bbe-177">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="43bbe-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-181">Строка, содержащая описание ошибки поставщика.</span><span class="sxs-lookup"><span data-stu-id="43bbe-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="43bbe-182">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="43bbe-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-186">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Задание CIM**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="43bbe-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-187">Сводное описание ошибки, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="43bbe-187">A summary description of the error, if present.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-188">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="43bbe-188">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-189">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-191">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="43bbe-191">The current health of the element.</span></span> <span data-ttu-id="43bbe-192">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="43bbe-192">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="43bbe-193">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="43bbe-193">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="43bbe-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="43bbe-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="43bbe-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-196">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-198">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="43bbe-198">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="43bbe-199">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="43bbe-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-200">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="43bbe-200">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-203">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="43bbe-203">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-204">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="43bbe-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="43bbe-205">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="43bbe-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-206">**жобрунтимес**</span><span class="sxs-lookup"><span data-stu-id="43bbe-206">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-207">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43bbe-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-209">Количество запусков задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-209">The number of times that the job should be run.</span></span> <span data-ttu-id="43bbe-210">Значение 1 указывает, что задание не повторяется, а любое ненулевое значение указывает на ограничение на количество повторений задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-210">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="43bbe-211">Ноль указывает, что количество операций, которые может обработать задание, не ограничено, но оно будет завершено либо после достижения **унтилтиме** , либо после того, как задание будет прервано вручную.</span><span class="sxs-lookup"><span data-stu-id="43bbe-211">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="43bbe-212">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-212">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-213">**JobState**</span><span class="sxs-lookup"><span data-stu-id="43bbe-213">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-214">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-216">**JobState** — это целочисленное перечисление, указывающее операционное состояние задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-216">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="43bbe-217">Он также может указывать на переходы между этими состояниями, например "завершение работы" и "Запуск".</span><span class="sxs-lookup"><span data-stu-id="43bbe-217">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="43bbe-218">Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="43bbe-218">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="43bbe-219">Значение</span><span class="sxs-lookup"><span data-stu-id="43bbe-219">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="43bbe-220">Значение</span><span class="sxs-lookup"><span data-stu-id="43bbe-220">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="43bbe-221"><dt>**Новое**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-221"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="43bbe-222">Задание никогда не запускалось.</span><span class="sxs-lookup"><span data-stu-id="43bbe-222">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="43bbe-223"><dt>**Начиная**</dt> с <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-223"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="43bbe-224">Задание переходит из состояния 2 (новое), 5 (приостановлено) или 11 (служба) в состояние 4 (работает).</span><span class="sxs-lookup"><span data-stu-id="43bbe-224">The job is moving from the 2 (New), 5(Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="43bbe-225"><dt>**Выполнение**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-225"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="43bbe-226">Задание выполняется.</span><span class="sxs-lookup"><span data-stu-id="43bbe-226">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="43bbe-227"><dt>**Приостановлено**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-227"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="43bbe-228">Задание остановлено, но его можно легко перезапустить.</span><span class="sxs-lookup"><span data-stu-id="43bbe-228">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="43bbe-229"><dt>**Завершение работы**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-229"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="43bbe-230">Задание переходит в состояние 7 (завершено), 8 (завершено) или 9 (прервано).</span><span class="sxs-lookup"><span data-stu-id="43bbe-230">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="43bbe-231"><dt>**Завершено**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-231"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="43bbe-232">Задание выполнено нормально.</span><span class="sxs-lookup"><span data-stu-id="43bbe-232">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="43bbe-233"><dt>**Завершено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-233"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="43bbe-234">Задание остановлено запросом на изменение состояния "завершено".</span><span class="sxs-lookup"><span data-stu-id="43bbe-234">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="43bbe-235">Задание и все его базовые процессы завершены и могут быть перезапущены только в качестве нового задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-235">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="43bbe-236">Требование перезапуска задания только в том случае, если задано новое задание.</span><span class="sxs-lookup"><span data-stu-id="43bbe-236">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="43bbe-237"><dt>**Уничтожено**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-237"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="43bbe-238">Задание остановлено запросом на изменение состояния "Kill".</span><span class="sxs-lookup"><span data-stu-id="43bbe-238">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="43bbe-239">Базовые процессы могут по-прежнему выполняться, а для освобождения ресурсов может потребоваться очистка.</span><span class="sxs-lookup"><span data-stu-id="43bbe-239">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="43bbe-240"><dt>**Исключение**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-240"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="43bbe-241">Задание находится в ненормальном состоянии, что может указывать на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="43bbe-241">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="43bbe-242">Фактическое состояние задания может быть доступно через объекты конкретного задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-242">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="43bbe-243"><dt>**Служба**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-243"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="43bbe-244">Задание находится в состоянии, зависящем от поставщика, которое поддерживает обнаружение проблем, разрешение или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="43bbe-244">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="43bbe-245"><dt>**Зарезервировано**</dt> <dt>12 32767</dt> в формате DMTF</span><span class="sxs-lookup"><span data-stu-id="43bbe-245"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="43bbe-246">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="43bbe-246">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="43bbe-247"><dt>**Поставщик Зарезервированный**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-247"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="43bbe-248">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="43bbe-248">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="43bbe-249">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="43bbe-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-250">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-252">Строка, представляющая состояние задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-252">A string that represents the job status.</span></span> <span data-ttu-id="43bbe-253">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-253">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-254">**JobType**</span><span class="sxs-lookup"><span data-stu-id="43bbe-254">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-255">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-257">Указывает тип задания, отслеживаемого этим объектом.</span><span class="sxs-lookup"><span data-stu-id="43bbe-257">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43bbe-258">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="43bbe-258">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="43bbe-259">**Создание удаленной виртуальной машины** (300)</span><span class="sxs-lookup"><span data-stu-id="43bbe-259">**Creating Remote Virtual Machine** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

<span data-ttu-id="43bbe-260">**Проверка совместимости виртуальной машины** (301)</span><span class="sxs-lookup"><span data-stu-id="43bbe-260">**Checking Virtual Machine Compatibility** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="43bbe-261">**Проверка совместимости виртуальной машины и хранилища** (302)</span><span class="sxs-lookup"><span data-stu-id="43bbe-261">**Checking Virtual Machine and Storage Compatibility** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="43bbe-262">**Проверка совместимости хранилища** (303)</span><span class="sxs-lookup"><span data-stu-id="43bbe-262">**Checking Storage Compatibility** (303)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

<span data-ttu-id="43bbe-263">**Проверка миграции хранилища** (304)</span><span class="sxs-lookup"><span data-stu-id="43bbe-263">**Checking Storage Migration** (304)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="43bbe-264">**Перемещение виртуальной машины** (305)</span><span class="sxs-lookup"><span data-stu-id="43bbe-264">**Moving Virtual Machine** (305)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

<span data-ttu-id="43bbe-265">**Перемещение виртуальной машины и хранилища** (306)</span><span class="sxs-lookup"><span data-stu-id="43bbe-265">**Moving Virtual Machine and Storage** (306)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

<span data-ttu-id="43bbe-266">**Перемещение хранилища** (307)</span><span class="sxs-lookup"><span data-stu-id="43bbe-266">**Moving Storage** (307)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43bbe-267">**локалорутктиме**</span><span class="sxs-lookup"><span data-stu-id="43bbe-267">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-268">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-270">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-270">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<span data-ttu-id="43bbe-271">Указывает, представляют ли значения времени, представленные в свойствах **рунстартинтервал** и **унтилтиме** , местное время или время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="43bbe-271">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dl> <dt>

<span data-ttu-id="43bbe-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Местное время** (1)</span><span class="sxs-lookup"><span data-stu-id="43bbe-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Время в формате UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="43bbe-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="43bbe-274">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="43bbe-274">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-275">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-277">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**мсвм \_ виртуалсистеммигратионсеттингдата**](msvm-virtualsystemmigrationsettingdata.md).**Мигратионтипе**")</span><span class="sxs-lookup"><span data-stu-id="43bbe-277">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-278">Тип миграции, представленный этим объектом задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-278">The migration type represented by this job object.</span></span> <span data-ttu-id="43bbe-279">Это будет одно из значений, определенных для свойства **мигратионтипе** класса [**\_ виртуалсистеммигратионсеттингдата мсвм**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="43bbe-279">This will be one of the values defined for the **MigrationType** property of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-280">**Name**</span><span class="sxs-lookup"><span data-stu-id="43bbe-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-281">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-283">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="43bbe-283">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-284">Отображаемое имя для этого экземпляра задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-284">The display name for this instance of a job.</span></span> <span data-ttu-id="43bbe-285">Кроме того, отображаемое имя можно использовать в качестве свойства для поиска или запроса.</span><span class="sxs-lookup"><span data-stu-id="43bbe-285">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="43bbe-286">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="43bbe-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-287">**невресаурцесеттингдата**</span><span class="sxs-lookup"><span data-stu-id="43bbe-287">**NewResourceSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-288">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="43bbe-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-290">Для динамической миграции всегда будет задано **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="43bbe-290">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="43bbe-291">Если для миграции хранилища задано **значение NULL**, то ни один из виртуальных жестких дисков виртуальной машины не будет перемещен.</span><span class="sxs-lookup"><span data-stu-id="43bbe-291">For a storage migration, if this is **Null**, none of the virtual machine's virtual hard disks (VHDs) will be moved.</span></span> <span data-ttu-id="43bbe-292">В противном случае он будет содержать массив внедренных экземпляров класса [**мсвм \_ сторажеаллокатионсеттингдата**](msvm-storageallocationsettingdata.md) , представляющих виртуальные жесткие диски для перемещения.</span><span class="sxs-lookup"><span data-stu-id="43bbe-292">Otherwise, this will contain an array of embedded instances of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class that represent the VHDs to be moved.</span></span> <span data-ttu-id="43bbe-293">В свойстве **Connection** этих экземпляров будет указано целевое расположение виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="43bbe-293">The **Connection** property of these instances will specify the destination location of the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-294">**невсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="43bbe-294">**NewSystemSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-297">Для динамической миграции всегда будет задано **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="43bbe-297">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="43bbe-298">Для миграции хранилища, если это значение равно **null**, корни данных виртуальной машины не перемещаются.</span><span class="sxs-lookup"><span data-stu-id="43bbe-298">For a storage migration, if this is **Null**, the virtual machine's data roots are not moving.</span></span> <span data-ttu-id="43bbe-299">В противном случае он будет содержать встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , где свойства **Екстерналдатарут**, **снапшотдатарут** и **свапфиледатарут** будут указывать новые корни данных.</span><span class="sxs-lookup"><span data-stu-id="43bbe-299">Otherwise, this will contain an embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class, where the **ExternalDataRoot**, **SnapshotDataRoot**, and **SwapFileDataRoot** properties will specify the new data roots.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-300">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="43bbe-300">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-303">Пользователь, который получает уведомление о завершении задания или сбое.</span><span class="sxs-lookup"><span data-stu-id="43bbe-303">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="43bbe-304">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-304">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-305">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="43bbe-305">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-306">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-308">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="43bbe-308">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="43bbe-309">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="43bbe-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="43bbe-310">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="43bbe-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="43bbe-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-312">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="43bbe-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-314">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="43bbe-314">The current statuses of the object.</span></span> <span data-ttu-id="43bbe-315">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="43bbe-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-316">**осеррековеряктион**</span><span class="sxs-lookup"><span data-stu-id="43bbe-316">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-319">Строка, описывающая действие восстановления, если свойство **рековеряктион** экземпляра имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="43bbe-319">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="43bbe-320">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-320">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-321">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="43bbe-321">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-324">Пользователь, отправивший задание.</span><span class="sxs-lookup"><span data-stu-id="43bbe-324">The user who submitted the job.</span></span> <span data-ttu-id="43bbe-325">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-325">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-326">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="43bbe-326">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-327">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-329">Квалификаторы: **MinValue** (0), **MaxValue** (100), **единицы** ("процент")</span><span class="sxs-lookup"><span data-stu-id="43bbe-329">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-330">Процент завершения задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-330">The completion percentage of the job.</span></span> <span data-ttu-id="43bbe-331">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-331">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-332">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="43bbe-332">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-333">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-333">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-335">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="43bbe-335">Provides high level status information.</span></span> <span data-ttu-id="43bbe-336">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="43bbe-336">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="43bbe-337">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="43bbe-337">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="43bbe-338">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="43bbe-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-339">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="43bbe-339">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-340">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43bbe-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-342">Важность выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-342">The importance of a job's execution.</span></span> <span data-ttu-id="43bbe-343">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-343">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-344">**рековеряктион**</span><span class="sxs-lookup"><span data-stu-id="43bbe-344">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-345">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43bbe-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-347">Описывает действие восстановления, которое необходимо выполнить для неуспешного выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-347">Describes the recovery action to be taken for an unsuccessfully run job.</span></span> <span data-ttu-id="43bbe-348">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-348">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="43bbe-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="43bbe-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="43bbe-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Не продолжать** (2)</span><span class="sxs-lookup"><span data-stu-id="43bbe-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Перейти к следующему заданию** (3)</span><span class="sxs-lookup"><span data-stu-id="43bbe-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Повторно запустить задание** (4)</span><span class="sxs-lookup"><span data-stu-id="43bbe-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Запустить задание восстановления** (5)</span><span class="sxs-lookup"><span data-stu-id="43bbe-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="43bbe-355">**рундай**</span><span class="sxs-lookup"><span data-stu-id="43bbe-355">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-356">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="43bbe-356">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-358">Квалификаторы: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="43bbe-358">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-359">День месяца, в который должно быть обработано задание.</span><span class="sxs-lookup"><span data-stu-id="43bbe-359">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="43bbe-360">Для этого свойства существуют различные интерпретации в зависимости от значения **рундайофвик**.</span><span class="sxs-lookup"><span data-stu-id="43bbe-360">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="43bbe-361">Если **рундайофвик** имеет значение 0, а **рундай** является положительным, **рундай** определяет день месяца, в котором обработано задание.</span><span class="sxs-lookup"><span data-stu-id="43bbe-361">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="43bbe-362">Например, если **рундайофвик** имеет значение 0, а **рундай** — 12, задание будет обработано на 12-<sup>й</sup> день месяца.</span><span class="sxs-lookup"><span data-stu-id="43bbe-362">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="43bbe-363">Если **рундайофвик** имеет значение 0, а **рундай** имеет отрицательное значение, **рундай** определяет число дней до последнего дня месяца, в котором обработано задание.</span><span class="sxs-lookup"><span data-stu-id="43bbe-363">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="43bbe-364">1 указывает последний день месяца, 2 — один день до последнего дня месяца и т. д.</span><span class="sxs-lookup"><span data-stu-id="43bbe-364">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="43bbe-365">Например, если **рундайофвик** имеет значение 0, а **рундай** — значение 1, задание будет обрабатываться в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="43bbe-365">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="43bbe-366">Если **рундайофвик** не равен 0, **рундайофвик** — это день недели, в который будет обработано задание, относительно **рундай**.</span><span class="sxs-lookup"><span data-stu-id="43bbe-366">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="43bbe-367">Например, если **рундай** имеет значение 15, а **рундайофвик** — 7 (+ Суббота), задание будет обработано в первую субботу в или после 15-<sup>го</sup> дня месяца.</span><span class="sxs-lookup"><span data-stu-id="43bbe-367">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="43bbe-368">Если **рундай** имеет значение 20, а **рундайофвик** — 7 (Суббота), задание будет обработано в первую субботу в течение или до 20-<sup>го</sup> дня месяца.</span><span class="sxs-lookup"><span data-stu-id="43bbe-368">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="43bbe-369">Если **рундай** имеет значение 1, а **рундайофвик** — 1 (воскресенье), задание будет обработано в последнем воскресенье месяца.</span><span class="sxs-lookup"><span data-stu-id="43bbe-369">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="43bbe-370">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-370">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-371">**рундайофвик**</span><span class="sxs-lookup"><span data-stu-id="43bbe-371">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-372">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="43bbe-372">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-374">Положительное или отрицательное целое число, используемое в сочетании с **рундай** для обозначения дня недели или месяца, в котором обрабатывается задание.</span><span class="sxs-lookup"><span data-stu-id="43bbe-374">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="43bbe-375">Дополнительные сведения см. в описании свойства **рундай** .</span><span class="sxs-lookup"><span data-stu-id="43bbe-375">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="43bbe-376">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-376">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="43bbe-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Суббота** (7)</span><span class="sxs-lookup"><span data-stu-id="43bbe-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Пятница** (6)</span><span class="sxs-lookup"><span data-stu-id="43bbe-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Четверг** (5)</span><span class="sxs-lookup"><span data-stu-id="43bbe-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**Среда** (4)</span><span class="sxs-lookup"><span data-stu-id="43bbe-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Вторник** (3)</span><span class="sxs-lookup"><span data-stu-id="43bbe-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Понедельник** (2)</span><span class="sxs-lookup"><span data-stu-id="43bbe-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**– Воскресенье** (1)</span><span class="sxs-lookup"><span data-stu-id="43bbe-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**Ексактдайофмонс** (0)</span><span class="sxs-lookup"><span data-stu-id="43bbe-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Воскресенье** (1)</span><span class="sxs-lookup"><span data-stu-id="43bbe-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Понедельник** (2)</span><span class="sxs-lookup"><span data-stu-id="43bbe-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Вторник** (3)</span><span class="sxs-lookup"><span data-stu-id="43bbe-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Среда** (4)</span><span class="sxs-lookup"><span data-stu-id="43bbe-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Четверг** (5)</span><span class="sxs-lookup"><span data-stu-id="43bbe-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Пятница** (6)</span><span class="sxs-lookup"><span data-stu-id="43bbe-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Суббота** (7)</span><span class="sxs-lookup"><span data-stu-id="43bbe-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="43bbe-392">**рунмонс**</span><span class="sxs-lookup"><span data-stu-id="43bbe-392">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-393">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="43bbe-393">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-395">Месяц, в течение которого должно быть обработано задание.</span><span class="sxs-lookup"><span data-stu-id="43bbe-395">The month during which the job should be processed.</span></span> <span data-ttu-id="43bbe-396">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-396">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="43bbe-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Январь** (0)</span><span class="sxs-lookup"><span data-stu-id="43bbe-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Февраль** (1)</span><span class="sxs-lookup"><span data-stu-id="43bbe-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Март** (2)</span><span class="sxs-lookup"><span data-stu-id="43bbe-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Апрель** (3)</span><span class="sxs-lookup"><span data-stu-id="43bbe-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Май** (4)</span><span class="sxs-lookup"><span data-stu-id="43bbe-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Июнь** (5)</span><span class="sxs-lookup"><span data-stu-id="43bbe-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Июль** (6)</span><span class="sxs-lookup"><span data-stu-id="43bbe-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Август** (7)</span><span class="sxs-lookup"><span data-stu-id="43bbe-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Сентябрь** (8)</span><span class="sxs-lookup"><span data-stu-id="43bbe-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Октябрь** (9)</span><span class="sxs-lookup"><span data-stu-id="43bbe-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Ноябрь** (10)</span><span class="sxs-lookup"><span data-stu-id="43bbe-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Декабрь** (11)</span><span class="sxs-lookup"><span data-stu-id="43bbe-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="43bbe-409">**рунстартинтервал**</span><span class="sxs-lookup"><span data-stu-id="43bbe-409">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-410">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-412">Интервал времени после полуночи, когда должно быть обработано задание.</span><span class="sxs-lookup"><span data-stu-id="43bbe-412">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="43bbe-413">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-414">**счедуледстарттиме**</span><span class="sxs-lookup"><span data-stu-id="43bbe-414">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-415">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-417">Запланированное время запуска задания (если применимо).</span><span class="sxs-lookup"><span data-stu-id="43bbe-417">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="43bbe-418">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-419">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-419">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-420">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-420">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-422">Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-422">The time that the job began.</span></span> <span data-ttu-id="43bbe-423">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-423">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-424">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="43bbe-424">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-425">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-427">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="43bbe-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-428">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="43bbe-428">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-429">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="43bbe-429">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-431">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="43bbe-431">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="43bbe-432">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="43bbe-432">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-433">**тимебефореремовал**</span><span class="sxs-lookup"><span data-stu-id="43bbe-433">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-434">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-436">Время (в минутах), в течение которого задание сохраняется после завершения выполнения, как успешно, так и в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="43bbe-436">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="43bbe-437">Задание должно оставаться в наличии в течение некоторого периода времени независимо от значения свойства **делетеонкомплетион** .</span><span class="sxs-lookup"><span data-stu-id="43bbe-437">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="43bbe-438">Значение по умолчанию — пять минут.</span><span class="sxs-lookup"><span data-stu-id="43bbe-438">The default is five minutes.</span></span> <span data-ttu-id="43bbe-439">Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))и всегда имеет значение 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="43bbe-439">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-440">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="43bbe-440">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-441">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-443">Дата или время последнего изменения состояния задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-443">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="43bbe-444">Если состояние задания не изменилось и заполнено это свойство, то для него должно быть задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="43bbe-444">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="43bbe-445">Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="43bbe-445">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="43bbe-446">Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="43bbe-446">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-447">**тимесубмиттед**</span><span class="sxs-lookup"><span data-stu-id="43bbe-447">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-448">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-448">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-450">Время отправки задания.</span><span class="sxs-lookup"><span data-stu-id="43bbe-450">The time that the job was submitted.</span></span> <span data-ttu-id="43bbe-451">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-451">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-452">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="43bbe-452">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-453">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43bbe-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-454">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-455">Время, когда задание недопустимо или должно быть остановлено.</span><span class="sxs-lookup"><span data-stu-id="43bbe-455">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="43bbe-456">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="43bbe-456">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="43bbe-457">**виртуалсистемнаме**</span><span class="sxs-lookup"><span data-stu-id="43bbe-457">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43bbe-458">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="43bbe-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43bbe-459">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43bbe-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43bbe-460">Уникальное имя затронутой виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="43bbe-460">The unique name of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43bbe-461">Требования</span><span class="sxs-lookup"><span data-stu-id="43bbe-461">Requirements</span></span>



| <span data-ttu-id="43bbe-462">Требование</span><span class="sxs-lookup"><span data-stu-id="43bbe-462">Requirement</span></span> | <span data-ttu-id="43bbe-463">Значение</span><span class="sxs-lookup"><span data-stu-id="43bbe-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43bbe-464">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43bbe-464">Minimum supported client</span></span><br/> | <span data-ttu-id="43bbe-465">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="43bbe-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="43bbe-466">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43bbe-466">Minimum supported server</span></span><br/> | <span data-ttu-id="43bbe-467">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="43bbe-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43bbe-468">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43bbe-468">Namespace</span></span><br/>                | <span data-ttu-id="43bbe-469">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="43bbe-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="43bbe-470">MOF</span><span class="sxs-lookup"><span data-stu-id="43bbe-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43bbe-471"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43bbe-472">DLL</span><span class="sxs-lookup"><span data-stu-id="43bbe-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43bbe-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43bbe-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

