---
description: Представляет задание операции гостевой файловой службы.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Класс Msvm_CopyFileToGuestJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663729"
---
# <a name="msvm_copyfiletoguestjob-class"></a><span data-ttu-id="b0930-103">\_Класс мсвм копифилетогуестжоб</span><span class="sxs-lookup"><span data-stu-id="b0930-103">Msvm\_CopyFileToGuestJob class</span></span>

<span data-ttu-id="b0930-104">Представляет задание операции гостевой файловой службы.</span><span class="sxs-lookup"><span data-stu-id="b0930-104">Represents a guest file service operation job.</span></span> <span data-ttu-id="b0930-105">Этот класс является производным от [**мсвм \_ гуестфилесервице**](msvm-guestfileservice.md).</span><span class="sxs-lookup"><span data-stu-id="b0930-105">This class derives from [**Msvm\_GuestFileService**](msvm-guestfileservice.md).</span></span>

<span data-ttu-id="b0930-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b0930-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0930-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0930-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a><span data-ttu-id="b0930-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b0930-108">Members</span></span>

<span data-ttu-id="b0930-109">Класс **мсвм \_ копифилетогуестжоб** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b0930-109">The **Msvm\_CopyFileToGuestJob** class has these types of members:</span></span>

-   [<span data-ttu-id="b0930-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b0930-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b0930-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b0930-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b0930-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b0930-112">Methods</span></span>

<span data-ttu-id="b0930-113">Класс **мсвм \_ копифилетогуестжоб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b0930-113">The **Msvm\_CopyFileToGuestJob** class has these methods.</span></span>



| <span data-ttu-id="b0930-114">Метод</span><span class="sxs-lookup"><span data-stu-id="b0930-114">Method</span></span>                                                                   | <span data-ttu-id="b0930-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b0930-115">Description</span></span>                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="b0930-116">**копифилестогуест**</span><span class="sxs-lookup"><span data-stu-id="b0930-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md)       | <span data-ttu-id="b0930-117">Копирует файлы с узла Hyper-V на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b0930-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> |
| [<span data-ttu-id="b0930-118">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="b0930-118">**GetError**</span></span>](geterror-msvm-copyfiletoguestjob.md)                     | <span data-ttu-id="b0930-119">Извлекает объект ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="b0930-119">Retrieves the error object for the job.</span></span><br/>                    |
| [<span data-ttu-id="b0930-120">**жетеррорекс**</span><span class="sxs-lookup"><span data-stu-id="b0930-120">**GetErrorEx**</span></span>](geterrorex-msvm-copyfiletoguestjob.md)                 | <span data-ttu-id="b0930-121">Извлекает объекты ошибок для задания.</span><span class="sxs-lookup"><span data-stu-id="b0930-121">Retrieves the error objects for the job.</span></span><br/>                   |
| [<span data-ttu-id="b0930-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="b0930-122">**RequestStateChange**</span></span>](requeststatechange-msvm-copyfiletoguestjob.md) | <span data-ttu-id="b0930-123">Изменяет состояние задания.</span><span class="sxs-lookup"><span data-stu-id="b0930-123">Changes the state of the job.</span></span><br/>                              |
| <span data-ttu-id="b0930-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="b0930-124">**StartService**</span></span>                                                         | <span data-ttu-id="b0930-125">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b0930-125">This method is not supported.</span></span><br/>                              |
| <span data-ttu-id="b0930-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="b0930-126">**StopService**</span></span>                                                          | <span data-ttu-id="b0930-127">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b0930-127">This method is not supported.</span></span><br/>                              |



 

### <a name="properties"></a><span data-ttu-id="b0930-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="b0930-128">Properties</span></span>

<span data-ttu-id="b0930-129">Класс **мсвм \_ копифилетогуестжоб** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b0930-129">The **Msvm\_CopyFileToGuestJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0930-130">**Отменяемых**</span><span class="sxs-lookup"><span data-stu-id="b0930-130">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-131">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b0930-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-133">Указывает, можно ли отменить задание.</span><span class="sxs-lookup"><span data-stu-id="b0930-133">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="b0930-134">Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="b0930-134">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span> <span data-ttu-id="b0930-135">Если задано **значение true**, задание может быть отменено; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b0930-135">If **TRUE**, the job can be cancelled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b0930-136">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b0930-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-139">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b0930-139">Short textual description of the object.</span></span> <span data-ttu-id="b0930-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0930-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0930-141">**копифилетогуестсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="b0930-141">**CopyFileToGuestSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-142">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="b0930-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0930-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-144">Настройка данных, используемых для копирования файла.</span><span class="sxs-lookup"><span data-stu-id="b0930-144">Setting data that is used to copy a file.</span></span>

</dd> <dt>

<span data-ttu-id="b0930-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b0930-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-148">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b0930-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b0930-149">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b0930-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="b0930-150">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b0930-150">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-153">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b0930-153">Textual description of the object.</span></span> <span data-ttu-id="b0930-154">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0930-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0930-155">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="b0930-155">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0930-158">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Задание CIM**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="b0930-158">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="b0930-159">Сводное описание ошибки, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="b0930-159">A summary description of the error, if present.</span></span> <span data-ttu-id="b0930-160">Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="b0930-160">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="b0930-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b0930-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-162">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b0930-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-164">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b0930-164">Date and time the object was installed.</span></span> <span data-ttu-id="b0930-165">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="b0930-165">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="b0930-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0930-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0930-167">**Name**</span><span class="sxs-lookup"><span data-stu-id="b0930-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-170">Уникальный идентификатор службы, который также содержит сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="b0930-170">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="b0930-171">Дополнительные сведения о функциональных возможностях см. в описании свойства объекта **Description** .</span><span class="sxs-lookup"><span data-stu-id="b0930-171">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="b0930-172">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0930-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0930-173">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="b0930-173">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-174">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b0930-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-176">Если **значение равно true**, служба запущена.</span><span class="sxs-lookup"><span data-stu-id="b0930-176">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="b0930-177">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="b0930-177">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-180">Указывает, запускается ли служба автоматически (например, операционная система) или только после запроса.</span><span class="sxs-lookup"><span data-stu-id="b0930-180">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="b0930-181">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b0930-181">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="b0930-182">**Автоматическое**</span><span class="sxs-lookup"><span data-stu-id="b0930-182">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="b0930-183">**Документации**</span><span class="sxs-lookup"><span data-stu-id="b0930-183">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0930-184">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b0930-184">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-187">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b0930-187">Current status of the object.</span></span> <span data-ttu-id="b0930-188">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b0930-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="b0930-189">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b0930-189">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="b0930-190">**'**</span><span class="sxs-lookup"><span data-stu-id="b0930-190">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="b0930-191">**План**</span><span class="sxs-lookup"><span data-stu-id="b0930-191">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="b0930-192">**Пониженной функциональности**</span><span class="sxs-lookup"><span data-stu-id="b0930-192">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="b0930-193">**Неизвестный**</span><span class="sxs-lookup"><span data-stu-id="b0930-193">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="b0930-194">**"Пред Fail"**</span><span class="sxs-lookup"><span data-stu-id="b0930-194">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="b0930-195">**Start**</span><span class="sxs-lookup"><span data-stu-id="b0930-195">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="b0930-196">**Идет**</span><span class="sxs-lookup"><span data-stu-id="b0930-196">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="b0930-197">**Служеб**</span><span class="sxs-lookup"><span data-stu-id="b0930-197">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="b0930-198">**Груз**</span><span class="sxs-lookup"><span data-stu-id="b0930-198">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="b0930-199">**"Recover"**</span><span class="sxs-lookup"><span data-stu-id="b0930-199">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="b0930-200">**"Нет контакта"**</span><span class="sxs-lookup"><span data-stu-id="b0930-200">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="b0930-201">**"Потеря связи"**</span><span class="sxs-lookup"><span data-stu-id="b0930-201">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0930-202">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b0930-202">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-205">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="b0930-205">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="b0930-206">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b0930-206">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-209">Имя системы, в которой размещена служба.</span><span class="sxs-lookup"><span data-stu-id="b0930-209">Name of the system that hosts the service.</span></span>

</dd> <dt>

<span data-ttu-id="b0930-210">**виртуалсистемнаме**</span><span class="sxs-lookup"><span data-stu-id="b0930-210">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0930-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0930-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0930-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0930-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0930-213">Идентификатор GUID затронутой виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="b0930-213">GUID of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0930-214">Требования</span><span class="sxs-lookup"><span data-stu-id="b0930-214">Requirements</span></span>



| <span data-ttu-id="b0930-215">Требование</span><span class="sxs-lookup"><span data-stu-id="b0930-215">Requirement</span></span> | <span data-ttu-id="b0930-216">Значение</span><span class="sxs-lookup"><span data-stu-id="b0930-216">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0930-217">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0930-217">Minimum supported client</span></span><br/> | <span data-ttu-id="b0930-218">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0930-218">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b0930-219">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0930-219">Minimum supported server</span></span><br/> | <span data-ttu-id="b0930-220">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0930-220">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b0930-221">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b0930-221">Namespace</span></span><br/>                | <span data-ttu-id="b0930-222">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b0930-222">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b0930-223">MOF</span><span class="sxs-lookup"><span data-stu-id="b0930-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0930-224"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0930-224"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0930-225">DLL</span><span class="sxs-lookup"><span data-stu-id="b0930-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0930-226"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0930-226"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b0930-227">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0930-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0930-228">**\_КОНКРЕТЕЖОБ CIM**</span><span class="sxs-lookup"><span data-stu-id="b0930-228">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

[<span data-ttu-id="b0930-229">**Мсвм \_ гуестфилесервице**</span><span class="sxs-lookup"><span data-stu-id="b0930-229">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> <dt>

[<span data-ttu-id="b0930-230">**Мсвм \_ гуестсервице**</span><span class="sxs-lookup"><span data-stu-id="b0930-230">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

