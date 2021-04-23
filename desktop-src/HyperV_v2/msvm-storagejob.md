---
description: Представляет задание операции с хранилищем, созданным службой управления образами Microsoft Hyper-V.
ms.assetid: a1517c1f-7fb6-4203-a5ec-2ecdfcbc4e8c
title: Класс Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob
- Msvm_StorageJob.KillJob
- Msvm_StorageJob.InstanceID
- Msvm_StorageJob.Caption
- Msvm_StorageJob.Description
- Msvm_StorageJob.ElementName
- Msvm_StorageJob.InstallDate
- Msvm_StorageJob.Name
- Msvm_StorageJob.OperationalStatus
- Msvm_StorageJob.StatusDescriptions
- Msvm_StorageJob.Status
- Msvm_StorageJob.HealthState
- Msvm_StorageJob.CommunicationStatus
- Msvm_StorageJob.DetailedStatus
- Msvm_StorageJob.OperatingStatus
- Msvm_StorageJob.PrimaryStatus
- Msvm_StorageJob.JobStatus
- Msvm_StorageJob.TimeSubmitted
- Msvm_StorageJob.ScheduledStartTime
- Msvm_StorageJob.StartTime
- Msvm_StorageJob.ElapsedTime
- Msvm_StorageJob.JobRunTimes
- Msvm_StorageJob.RunMonth
- Msvm_StorageJob.RunDay
- Msvm_StorageJob.RunDayOfWeek
- Msvm_StorageJob.RunStartInterval
- Msvm_StorageJob.LocalOrUtcTime
- Msvm_StorageJob.UntilTime
- Msvm_StorageJob.Notify
- Msvm_StorageJob.Owner
- Msvm_StorageJob.Priority
- Msvm_StorageJob.PercentComplete
- Msvm_StorageJob.DeleteOnCompletion
- Msvm_StorageJob.ErrorCode
- Msvm_StorageJob.ErrorDescription
- Msvm_StorageJob.ErrorSummaryDescription
- Msvm_StorageJob.RecoveryAction
- Msvm_StorageJob.OtherRecoveryAction
- Msvm_StorageJob.JobState
- Msvm_StorageJob.TimeOfLastStateChange
- Msvm_StorageJob.TimeBeforeRemoval
- Msvm_StorageJob.Cancellable
- Msvm_StorageJob.Child
- Msvm_StorageJob.JobCompletionStatusCode
- Msvm_StorageJob.Parent
- Msvm_StorageJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3014cb9a8201d7baceaf39bb760b17c33844abeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913700"
---
# <a name="msvm_storagejob-class"></a><span data-ttu-id="94933-103">\_Класс мсвм сторажежоб</span><span class="sxs-lookup"><span data-stu-id="94933-103">Msvm\_StorageJob class</span></span>

<span data-ttu-id="94933-104">Представляет задание операции с хранилищем, созданным службой управления образами Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="94933-104">Represents a storage operation job created by the Microsoft Hyper-V Image Management Service.</span></span>

<span data-ttu-id="94933-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="94933-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94933-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94933-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
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
  datetime TimeBeforeRemoval = 00000000000500.000000:000";
  boolean  Cancellable;
  string   Child;
  UINT32   JobCompletionStatusCode;
  string   Parent;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="94933-107">Члены</span><span class="sxs-lookup"><span data-stu-id="94933-107">Members</span></span>

<span data-ttu-id="94933-108">Класс **мсвм \_ сторажежоб** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="94933-108">The **Msvm\_StorageJob** class has these types of members:</span></span>

-   [<span data-ttu-id="94933-109">Методы</span><span class="sxs-lookup"><span data-stu-id="94933-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="94933-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="94933-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="94933-111">Методы</span><span class="sxs-lookup"><span data-stu-id="94933-111">Methods</span></span>

<span data-ttu-id="94933-112">Класс **мсвм \_ сторажежоб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="94933-112">The **Msvm\_StorageJob** class has these methods.</span></span>



| <span data-ttu-id="94933-113">Метод</span><span class="sxs-lookup"><span data-stu-id="94933-113">Method</span></span>                                                           | <span data-ttu-id="94933-114">Описание</span><span class="sxs-lookup"><span data-stu-id="94933-114">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94933-115">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="94933-115">**GetError**</span></span>](msvm-storagejob-geterror.md)                     | <span data-ttu-id="94933-116">Извлекает ошибку, описывающую причину сбоя задания.</span><span class="sxs-lookup"><span data-stu-id="94933-116">Retrieves the error that describes the reason why the job failed.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="94933-117">**жетеррорекс**</span><span class="sxs-lookup"><span data-stu-id="94933-117">**GetErrorEx**</span></span>](geterrorex-msvm-storagejob.md)                 | <span data-ttu-id="94933-118">При выполнении или завершении задания без ошибок этот метод не возвращает экземпляр [**\_ ошибки мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="94933-118">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="94933-119">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, возвращается один или несколько экземпляров **мсвм \_ Error** .</span><span class="sxs-lookup"><span data-stu-id="94933-119">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span><br/> |
| <span data-ttu-id="94933-120">**киллжоб**</span><span class="sxs-lookup"><span data-stu-id="94933-120">**KillJob**</span></span>                                                      | <span data-ttu-id="94933-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="94933-121">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="94933-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="94933-122">**RequestStateChange**</span></span>](msvm-storagejob-requeststatechange.md) | <span data-ttu-id="94933-123">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="94933-123">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="94933-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="94933-124">Properties</span></span>

<span data-ttu-id="94933-125">Класс **мсвм \_ сторажежоб** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="94933-125">The **Msvm\_StorageJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94933-126">**Отменяемых**</span><span class="sxs-lookup"><span data-stu-id="94933-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-127">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="94933-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94933-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-129">Указывает, можно ли отменить задание.</span><span class="sxs-lookup"><span data-stu-id="94933-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="94933-130">Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="94933-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="94933-131">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="94933-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-134">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="94933-134">A short description of the object.</span></span> <span data-ttu-id="94933-135">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="94933-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-136">**Дочерний**</span><span class="sxs-lookup"><span data-stu-id="94933-136">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-139">При сбое асинхронной операции это свойство содержит полный путь к дочернему элементу виртуального жесткого диска, затронутого этой операцией.</span><span class="sxs-lookup"><span data-stu-id="94933-139">On failure of the asynchronous operation, this property contains the full path of the child of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="94933-140">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="94933-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-141">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-143">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="94933-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="94933-144">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="94933-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="94933-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="94933-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-146">**делетеонкомплетион**</span><span class="sxs-lookup"><span data-stu-id="94933-146">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-147">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="94933-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94933-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-149">Указывает, следует ли автоматически удалять задание после завершения.</span><span class="sxs-lookup"><span data-stu-id="94933-149">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="94933-150">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-150">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-151">**Описание**</span><span class="sxs-lookup"><span data-stu-id="94933-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-154">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="94933-154">A description of the object.</span></span> <span data-ttu-id="94933-155">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="94933-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="94933-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-157">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-159">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="94933-159">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="94933-160">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="94933-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="94933-161">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="94933-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-162">**елапседтиме**</span><span class="sxs-lookup"><span data-stu-id="94933-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-163">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94933-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94933-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-165">Длительность времени выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="94933-165">The length of time that the job has been executing.</span></span> <span data-ttu-id="94933-166">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="94933-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-170">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="94933-170">A display name for the object.</span></span> <span data-ttu-id="94933-171">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="94933-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="94933-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-173">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-175">Код ошибки, зависящий от поставщика.</span><span class="sxs-lookup"><span data-stu-id="94933-175">A vendor-specific error code.</span></span> <span data-ttu-id="94933-176">Если задание завершилось без ошибок, значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="94933-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="94933-177">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="94933-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-181">Строка, содержащая описание ошибки поставщика.</span><span class="sxs-lookup"><span data-stu-id="94933-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="94933-182">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="94933-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94933-186">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Задание CIM**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="94933-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="94933-187">Сводное описание ошибки, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="94933-187">A summary description of the error, if present.</span></span> <span data-ttu-id="94933-188">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-188">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="94933-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-190">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-192">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="94933-192">The current health of the element.</span></span> <span data-ttu-id="94933-193">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="94933-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="94933-194">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="94933-194">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="94933-195">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="94933-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="94933-196">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="94933-196">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-197">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94933-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94933-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-199">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="94933-199">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="94933-200">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="94933-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-201">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="94933-201">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-204">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="94933-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="94933-205">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="94933-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-206">**жобкомплетионстатускоде**</span><span class="sxs-lookup"><span data-stu-id="94933-206">**JobCompletionStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-207">Тип данных: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="94933-207">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="94933-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-209">Код **HRESULT** , описывающий состояние завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="94933-209">The **HRESULT** code that describes the completion status for the asynchronous operation.</span></span>

</dd> <dt>

<span data-ttu-id="94933-210">**жобрунтимес**</span><span class="sxs-lookup"><span data-stu-id="94933-210">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-211">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94933-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94933-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-213">Количество запусков задания.</span><span class="sxs-lookup"><span data-stu-id="94933-213">The number of times that the job should be run.</span></span> <span data-ttu-id="94933-214">Значение 1 указывает, что задание не повторяется, а любое ненулевое значение указывает на ограничение на количество повторений задания.</span><span class="sxs-lookup"><span data-stu-id="94933-214">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="94933-215">Ноль указывает, что количество операций, которые может обработать задание, не ограничено, но оно будет завершено либо после достижения **унтилтиме** , либо после того, как задание будет прервано вручную.</span><span class="sxs-lookup"><span data-stu-id="94933-215">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="94933-216">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-216">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-217">**JobState**</span><span class="sxs-lookup"><span data-stu-id="94933-217">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-218">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-220">Рабочее состояние задания.</span><span class="sxs-lookup"><span data-stu-id="94933-220">The operational state of a job.</span></span> <span data-ttu-id="94933-221">Он также может указывать на переходы между этими состояниями, например 6 (завершение работы) и 3 (запуск).</span><span class="sxs-lookup"><span data-stu-id="94933-221">It can also indicate transitions between these states, for example, 6 (Shutting Down) and 3 (Starting).</span></span> <span data-ttu-id="94933-222">Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94933-222">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="94933-223">Значение</span><span class="sxs-lookup"><span data-stu-id="94933-223">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="94933-224">Значение</span><span class="sxs-lookup"><span data-stu-id="94933-224">Meaning</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="94933-225"><dt>**Новое**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="94933-225"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                               | <span data-ttu-id="94933-226">Задание никогда не запускалось.</span><span class="sxs-lookup"><span data-stu-id="94933-226">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="94933-227"><dt>**Начиная**</dt> с <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="94933-227"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                           | <span data-ttu-id="94933-228">Задание переходит с состояния "новое", "приостановлено" или "служба" в состояние "работает".</span><span class="sxs-lookup"><span data-stu-id="94933-228">The job is moving from the "New", "Suspended", or "Service" states into the "Running" state.</span></span><br/>                                                                                                                                            |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="94933-229"><dt>**Выполнение**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="94933-229"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                               | <span data-ttu-id="94933-230">Задание выполняется.</span><span class="sxs-lookup"><span data-stu-id="94933-230">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="94933-231"><dt>**Приостановлено**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="94933-231"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                       | <span data-ttu-id="94933-232">Задание остановлено, но его можно легко перезапустить.</span><span class="sxs-lookup"><span data-stu-id="94933-232">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="94933-233"><dt>**Завершение работы**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="94933-233"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                       | <span data-ttu-id="94933-234">Задание переходит в состояние "завершено", "завершено" или "уничтожено".</span><span class="sxs-lookup"><span data-stu-id="94933-234">The job is moving to a "Completed", "Terminated", or "Killed" state.</span></span><br/>                                                                                                                                                                    |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="94933-235"><dt>**Завершено**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="94933-235"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                       | <span data-ttu-id="94933-236">Задание выполнено нормально.</span><span class="sxs-lookup"><span data-stu-id="94933-236">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="94933-237"><dt>**Завершено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="94933-237"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                                   | <span data-ttu-id="94933-238">Задание остановлено запросом на изменение состояния "завершено".</span><span class="sxs-lookup"><span data-stu-id="94933-238">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="94933-239">Задание и все его базовые процессы завершены и могут быть перезапущены только в качестве нового задания.</span><span class="sxs-lookup"><span data-stu-id="94933-239">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="94933-240">Требование перезапуска задания только в том случае, если задано новое задание.</span><span class="sxs-lookup"><span data-stu-id="94933-240">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="94933-241"><dt>**Уничтожено**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="94933-241"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                                   | <span data-ttu-id="94933-242">Задание остановлено запросом на изменение состояния "Kill".</span><span class="sxs-lookup"><span data-stu-id="94933-242">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="94933-243">Базовые процессы могут по-прежнему выполняться, а для освобождения ресурсов может потребоваться очистка.</span><span class="sxs-lookup"><span data-stu-id="94933-243">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="94933-244"><dt>**Исключение**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="94933-244"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                      | <span data-ttu-id="94933-245">Задание находится в ненормальном состоянии, что может указывать на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="94933-245">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="94933-246">Фактическое состояние задания может быть доступно через объекты конкретного задания.</span><span class="sxs-lookup"><span data-stu-id="94933-246">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="94933-247"><dt>**Служба**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="94933-247"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                              | <span data-ttu-id="94933-248">Задание находится в состоянии, зависящем от поставщика, которое поддерживает обнаружение проблем, разрешение или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="94933-248">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="94933-249"><dt>**Зарезервировано**</dt> <dt>12 32767</dt> в формате DMTF</span><span class="sxs-lookup"><span data-stu-id="94933-249"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>                | <span data-ttu-id="94933-250">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="94933-250">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="94933-251"><dt> **Поставщик зарезервированный**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="94933-251"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="94933-252">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="94933-252">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="94933-253">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="94933-253">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-254">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-256">Строка, представляющая состояние задания.</span><span class="sxs-lookup"><span data-stu-id="94933-256">A string that represents the job status.</span></span> <span data-ttu-id="94933-257">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-257">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-258">**JobType**</span><span class="sxs-lookup"><span data-stu-id="94933-258">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-259">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-261">Тип асинхронной операции, отслеживаемой этим экземпляром **мсвм \_ сторажежоб**.</span><span class="sxs-lookup"><span data-stu-id="94933-261">The type of asynchronous operation being tracked by this instance of **Msvm\_StorageJob**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94933-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="94933-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>

<span data-ttu-id="94933-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**Создание виртуального жесткого диска** (1)</span><span class="sxs-lookup"><span data-stu-id="94933-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD Creation** (1)</span></span>


</dt> <dd>

<span data-ttu-id="94933-264">Создание образа виртуального жесткого диска (VHD).</span><span class="sxs-lookup"><span data-stu-id="94933-264">Creating a virtual hard disk (VHD) image.</span></span>

</dd> <dt>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>

<span data-ttu-id="94933-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Создание дискеты** (2)</span><span class="sxs-lookup"><span data-stu-id="94933-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Floppy Creation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="94933-266">Создание образа виртуального гибкого диска (VFD).</span><span class="sxs-lookup"><span data-stu-id="94933-266">Creating a virtual floppy disk image (VFD).</span></span>

</dd> <dt>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>

<span data-ttu-id="94933-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Сжатие** (3)</span><span class="sxs-lookup"><span data-stu-id="94933-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compaction** (3)</span></span>


</dt> <dd>

<span data-ttu-id="94933-268">Сжатие размера образа VHD.</span><span class="sxs-lookup"><span data-stu-id="94933-268">Compacting the size of a VHD image.</span></span>

</dd> <dt>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>

<span data-ttu-id="94933-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Расширение** (4)</span><span class="sxs-lookup"><span data-stu-id="94933-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansion** (4)</span></span>


</dt> <dd>

<span data-ttu-id="94933-270">Увеличение размера образа VHD.</span><span class="sxs-lookup"><span data-stu-id="94933-270">Expanding the size of a VHD image.</span></span>

</dd> <dt>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>

<span data-ttu-id="94933-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Слияние** (5)</span><span class="sxs-lookup"><span data-stu-id="94933-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Merging** (5)</span></span>


</dt> <dd>

<span data-ttu-id="94933-272">Объединение нескольких образов VHD в один образ.</span><span class="sxs-lookup"><span data-stu-id="94933-272">Merging multiple VHD images into a single image.</span></span>

</dd> <dt>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>

<span data-ttu-id="94933-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Преобразование** (6)</span><span class="sxs-lookup"><span data-stu-id="94933-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="94933-274">Преобразование типа образа виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="94933-274">Converting the type of a virtual hard disk image.</span></span>

</dd> <dt>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>

<span data-ttu-id="94933-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Подключение с замыканием на себя** (7)</span><span class="sxs-lookup"><span data-stu-id="94933-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Loopback Mount** (7)</span></span>


</dt> <dd>

<span data-ttu-id="94933-276">Подключение виртуального жесткого диска к родительскому разделу</span><span class="sxs-lookup"><span data-stu-id="94933-276">Mounting the virtual hard disk on the parent partition</span></span>

</dd> <dt>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>

<span data-ttu-id="94933-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Получение сведений о VHD** (8)</span><span class="sxs-lookup"><span data-stu-id="94933-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Get VHD Info** (8)</span></span>


</dt> <dd>

<span data-ttu-id="94933-278">Подключение виртуального жесткого диска в операционной системе управления.</span><span class="sxs-lookup"><span data-stu-id="94933-278">Mounting the VHD on the management operating system.</span></span>

</dd> <dt>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>

<span data-ttu-id="94933-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Проверка образа виртуального жесткого диска** (9)</span><span class="sxs-lookup"><span data-stu-id="94933-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Validate VHD Image** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94933-280">**локалорутктиме**</span><span class="sxs-lookup"><span data-stu-id="94933-280">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-281">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-283">Указывает, представляют ли значения времени, представленные в свойствах **рунстартинтервал** и **унтилтиме** , местное время или время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="94933-283">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="94933-284">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-284">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="94933-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Местное время** (1)</span><span class="sxs-lookup"><span data-stu-id="94933-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="94933-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Время в формате UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="94933-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="94933-287">**Name**</span><span class="sxs-lookup"><span data-stu-id="94933-287">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-290">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="94933-290">The label by which the object is known.</span></span> <span data-ttu-id="94933-291">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="94933-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-292">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="94933-292">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-295">Пользователь, который получает уведомление о завершении задания или сбое.</span><span class="sxs-lookup"><span data-stu-id="94933-295">The user who is notified upon job completion or failure.</span></span> <span data-ttu-id="94933-296">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-296">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-297">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="94933-297">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-298">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-300">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="94933-300">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="94933-301">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="94933-301">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="94933-302">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="94933-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-303">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="94933-303">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-304">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="94933-304">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="94933-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-306">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="94933-306">The current statuses of the object.</span></span> <span data-ttu-id="94933-307">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="94933-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-308">**осеррековеряктион**</span><span class="sxs-lookup"><span data-stu-id="94933-308">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-311">Строка, описывающая действие восстановления, если свойство **рековеряктион** экземпляра имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="94933-311">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="94933-312">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-312">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-313">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="94933-313">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-314">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-316">Пользователь, отправивший задание.</span><span class="sxs-lookup"><span data-stu-id="94933-316">The user who submitted the job.</span></span> <span data-ttu-id="94933-317">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-317">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-318">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="94933-318">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-321">При сбое асинхронной операции это свойство содержит путь к родительскому диску виртуального жесткого диска, затронутого этой операцией.</span><span class="sxs-lookup"><span data-stu-id="94933-321">On failure of the asynchronous operation, this property contains the file path to the parent of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="94933-322">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="94933-322">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-323">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94933-325">Квалификаторы: **MinValue** (0), **MaxValue** (100), **единицы** ("процент")</span><span class="sxs-lookup"><span data-stu-id="94933-325">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="94933-326">Процент завершения задания.</span><span class="sxs-lookup"><span data-stu-id="94933-326">The completion percentage of the job.</span></span> <span data-ttu-id="94933-327">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-327">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-328">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="94933-328">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-329">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-329">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-331">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="94933-331">Provides high level status information.</span></span> <span data-ttu-id="94933-332">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="94933-332">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="94933-333">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="94933-333">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="94933-334">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="94933-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-335">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="94933-335">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-336">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94933-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94933-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-338">Важность выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="94933-338">The importance of a job's execution.</span></span> <span data-ttu-id="94933-339">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-339">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-340">**рековеряктион**</span><span class="sxs-lookup"><span data-stu-id="94933-340">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-341">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94933-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94933-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-343">Описывает действие восстановления, выполняемое для задания, которое не выполнялось успешно.</span><span class="sxs-lookup"><span data-stu-id="94933-343">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="94933-344">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-344">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="94933-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="94933-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="94933-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="94933-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="94933-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Не продолжать** (2)</span><span class="sxs-lookup"><span data-stu-id="94933-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="94933-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Перейти к следующему заданию** (3)</span><span class="sxs-lookup"><span data-stu-id="94933-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="94933-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Повторно запустить задание** (4)</span><span class="sxs-lookup"><span data-stu-id="94933-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="94933-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Запустить задание восстановления** (5)</span><span class="sxs-lookup"><span data-stu-id="94933-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="94933-351">**рундай**</span><span class="sxs-lookup"><span data-stu-id="94933-351">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-352">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="94933-352">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="94933-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94933-354">Квалификаторы: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="94933-354">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="94933-355">День месяца, в который должно быть обработано задание.</span><span class="sxs-lookup"><span data-stu-id="94933-355">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="94933-356">Для этого свойства существуют различные интерпретации в зависимости от значения **рундайофвик**.</span><span class="sxs-lookup"><span data-stu-id="94933-356">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="94933-357">Если **рундайофвик** имеет значение 0, а **рундай** является положительным, **рундай** определяет день месяца, в котором обработано задание.</span><span class="sxs-lookup"><span data-stu-id="94933-357">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="94933-358">Например, если **рундайофвик** имеет значение 0, а **рундай** — 12, задание будет обработано на 12-<sup>й</sup> день месяца.</span><span class="sxs-lookup"><span data-stu-id="94933-358">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="94933-359">Если **рундайофвик** имеет значение 0, а **рундай** имеет отрицательное значение, **рундай** определяет число дней до последнего дня месяца, в котором обработано задание.</span><span class="sxs-lookup"><span data-stu-id="94933-359">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="94933-360">1 указывает последний день месяца, 2 — один день до последнего дня месяца и т. д.</span><span class="sxs-lookup"><span data-stu-id="94933-360">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="94933-361">Например, если **рундайофвик** имеет значение 0, а **рундай** — значение 1, задание будет обрабатываться в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="94933-361">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="94933-362">Если **рундайофвик** не равен 0, **рундайофвик** — это день недели, в который будет обработано задание, относительно **рундай**.</span><span class="sxs-lookup"><span data-stu-id="94933-362">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="94933-363">Например, если **рундай** имеет значение 15, а **рундайофвик** — 7 (+ Суббота), задание будет обработано в первую субботу в или после 15-<sup>го</sup> дня месяца.</span><span class="sxs-lookup"><span data-stu-id="94933-363">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="94933-364">Если **рундай** имеет значение 20, а **рундайофвик** — 7 (Суббота), задание будет обработано в первую субботу в течение или до 20-<sup>го</sup> дня месяца.</span><span class="sxs-lookup"><span data-stu-id="94933-364">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="94933-365">Если **рундай** имеет значение 1, а **рундайофвик** — 1 (воскресенье), задание будет обработано в последнем воскресенье месяца.</span><span class="sxs-lookup"><span data-stu-id="94933-365">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="94933-366">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-366">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-367">**рундайофвик**</span><span class="sxs-lookup"><span data-stu-id="94933-367">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-368">Тип данных: **sint8**</span><span class="sxs-lookup"><span data-stu-id="94933-368">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="94933-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-370">Положительное или отрицательное целое число, используемое в сочетании с **рундай** для обозначения дня недели или месяца, в котором обрабатывается задание.</span><span class="sxs-lookup"><span data-stu-id="94933-370">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="94933-371">Дополнительные сведения см. в описании свойства **рундай** .</span><span class="sxs-lookup"><span data-stu-id="94933-371">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="94933-372">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-372">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="94933-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Суббота** (7)</span><span class="sxs-lookup"><span data-stu-id="94933-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="94933-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Пятница** (6)</span><span class="sxs-lookup"><span data-stu-id="94933-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="94933-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Четверг** (5)</span><span class="sxs-lookup"><span data-stu-id="94933-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="94933-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**Среда** (4)</span><span class="sxs-lookup"><span data-stu-id="94933-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="94933-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Вторник** (3)</span><span class="sxs-lookup"><span data-stu-id="94933-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="94933-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Понедельник** (2)</span><span class="sxs-lookup"><span data-stu-id="94933-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="94933-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**– Воскресенье** (1)</span><span class="sxs-lookup"><span data-stu-id="94933-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="94933-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**Ексактдайофмонс** (0)</span><span class="sxs-lookup"><span data-stu-id="94933-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="94933-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Воскресенье** (1)</span><span class="sxs-lookup"><span data-stu-id="94933-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="94933-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Понедельник** (2)</span><span class="sxs-lookup"><span data-stu-id="94933-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="94933-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Вторник** (3)</span><span class="sxs-lookup"><span data-stu-id="94933-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="94933-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Среда** (4)</span><span class="sxs-lookup"><span data-stu-id="94933-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="94933-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Четверг** (5)</span><span class="sxs-lookup"><span data-stu-id="94933-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="94933-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Пятница** (6)</span><span class="sxs-lookup"><span data-stu-id="94933-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="94933-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Суббота** (7)</span><span class="sxs-lookup"><span data-stu-id="94933-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="94933-388">**рунмонс**</span><span class="sxs-lookup"><span data-stu-id="94933-388">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-389">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="94933-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="94933-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-391">Месяц, в течение которого должно быть обработано задание.</span><span class="sxs-lookup"><span data-stu-id="94933-391">The month during which the job should be processed.</span></span> <span data-ttu-id="94933-392">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="94933-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Январь** (0)</span><span class="sxs-lookup"><span data-stu-id="94933-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="94933-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Февраль** (1)</span><span class="sxs-lookup"><span data-stu-id="94933-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="94933-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Март** (2)</span><span class="sxs-lookup"><span data-stu-id="94933-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="94933-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Апрель** (3)</span><span class="sxs-lookup"><span data-stu-id="94933-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="94933-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Май** (4)</span><span class="sxs-lookup"><span data-stu-id="94933-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="94933-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Июнь** (5)</span><span class="sxs-lookup"><span data-stu-id="94933-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="94933-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Июль** (6)</span><span class="sxs-lookup"><span data-stu-id="94933-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="94933-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Август** (7)</span><span class="sxs-lookup"><span data-stu-id="94933-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="94933-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Сентябрь** (8)</span><span class="sxs-lookup"><span data-stu-id="94933-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="94933-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Октябрь** (9)</span><span class="sxs-lookup"><span data-stu-id="94933-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="94933-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Ноябрь** (10)</span><span class="sxs-lookup"><span data-stu-id="94933-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="94933-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Декабрь** (11)</span><span class="sxs-lookup"><span data-stu-id="94933-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="94933-405">**рунстартинтервал**</span><span class="sxs-lookup"><span data-stu-id="94933-405">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-406">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94933-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94933-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-408">Интервал времени после полуночи, когда должно быть обработано задание.</span><span class="sxs-lookup"><span data-stu-id="94933-408">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="94933-409">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-409">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-410">**счедуледстарттиме**</span><span class="sxs-lookup"><span data-stu-id="94933-410">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-411">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94933-411">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94933-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-413">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-414">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="94933-414">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-415">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94933-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94933-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-417">Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="94933-417">The time that the job began.</span></span> <span data-ttu-id="94933-418">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-419">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="94933-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-420">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="94933-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94933-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-422">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="94933-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94933-423">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="94933-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-424">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="94933-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="94933-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-426">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="94933-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="94933-427">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="94933-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="94933-428">**тимебефореремовал**</span><span class="sxs-lookup"><span data-stu-id="94933-428">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-429">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94933-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94933-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-431">Время (в минутах), в течение которого задание сохраняется после завершения выполнения, как успешно, так и в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="94933-431">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="94933-432">Задание должно оставаться в наличии в течение некоторого периода времени независимо от значения свойства **делетеонкомплетион** .</span><span class="sxs-lookup"><span data-stu-id="94933-432">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="94933-433">Значение по умолчанию — пять минут.</span><span class="sxs-lookup"><span data-stu-id="94933-433">The default is five minutes.</span></span> <span data-ttu-id="94933-434">Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))и всегда имеет значение 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="94933-434">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="94933-435">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="94933-435">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-436">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94933-436">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94933-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-438">Время последнего изменения состояния виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="94933-438">The time at which the virtual machine's state was last modified.</span></span> <span data-ttu-id="94933-439">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94933-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94933-440">**тимесубмиттед**</span><span class="sxs-lookup"><span data-stu-id="94933-440">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-441">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94933-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94933-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-443">Время отправки задания.</span><span class="sxs-lookup"><span data-stu-id="94933-443">The time that the job was submitted.</span></span> <span data-ttu-id="94933-444">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-444">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="94933-445">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="94933-445">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94933-446">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94933-446">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94933-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94933-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94933-448">Время, когда задание недопустимо или должно быть остановлено.</span><span class="sxs-lookup"><span data-stu-id="94933-448">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="94933-449">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="94933-449">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94933-450">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94933-450">Remarks</span></span>

<span data-ttu-id="94933-451">Доступ к классу **\_ сторажежоб мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="94933-451">Access to the **Msvm\_StorageJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="94933-452">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="94933-452">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="94933-453">Требования</span><span class="sxs-lookup"><span data-stu-id="94933-453">Requirements</span></span>



| <span data-ttu-id="94933-454">Требование</span><span class="sxs-lookup"><span data-stu-id="94933-454">Requirement</span></span> | <span data-ttu-id="94933-455">Значение</span><span class="sxs-lookup"><span data-stu-id="94933-455">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94933-456">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94933-456">Minimum supported client</span></span><br/> | <span data-ttu-id="94933-457">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="94933-457">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94933-458">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94933-458">Minimum supported server</span></span><br/> | <span data-ttu-id="94933-459">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="94933-459">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94933-460">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="94933-460">Namespace</span></span><br/>                | <span data-ttu-id="94933-461">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="94933-461">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="94933-462">MOF</span><span class="sxs-lookup"><span data-stu-id="94933-462">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94933-463"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94933-463"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94933-464">DLL</span><span class="sxs-lookup"><span data-stu-id="94933-464">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94933-465"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94933-465"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94933-466">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94933-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94933-467">**\_КОНКРЕТЕЖОБ CIM**</span><span class="sxs-lookup"><span data-stu-id="94933-467">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="94933-468">[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94933-468">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="94933-469">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="94933-469">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

