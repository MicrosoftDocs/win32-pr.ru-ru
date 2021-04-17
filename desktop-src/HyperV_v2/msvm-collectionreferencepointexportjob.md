---
description: Этот класс представляет задание операции экспорта точки ссылки на коллекцию.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Класс Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d21fab1519664471bdc2bb5d7102d94cbe3dde1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684624"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="6326f-103">\_Класс мсвм коллектионреференцепоинтекспортжоб</span><span class="sxs-lookup"><span data-stu-id="6326f-103">Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="6326f-104">Этот класс представляет задание операции экспорта точки ссылки на коллекцию.</span><span class="sxs-lookup"><span data-stu-id="6326f-104">This class represents a collection reference point export operation job.</span></span>

<span data-ttu-id="6326f-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6326f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6326f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6326f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a><span data-ttu-id="6326f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6326f-107">Members</span></span>

<span data-ttu-id="6326f-108">Класс **мсвм \_ коллектионреференцепоинтекспортжоб** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6326f-108">The **Msvm\_CollectionReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="6326f-109">Методы</span><span class="sxs-lookup"><span data-stu-id="6326f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="6326f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6326f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6326f-111">Методы</span><span class="sxs-lookup"><span data-stu-id="6326f-111">Methods</span></span>

<span data-ttu-id="6326f-112">Класс **мсвм \_ коллектионреференцепоинтекспортжоб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6326f-112">The **Msvm\_CollectionReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="6326f-113">Метод</span><span class="sxs-lookup"><span data-stu-id="6326f-113">Method</span></span>                                                                                  | <span data-ttu-id="6326f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6326f-114">Description</span></span>                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="6326f-115">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="6326f-115">**GetError**</span></span>](msvm-collectionreferencepointexportjob-geterror.md)                     | <span data-ttu-id="6326f-116">Возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6326f-116">Retrieves an error.</span></span><br/>                     |
| [<span data-ttu-id="6326f-117">**жетеррорекс**</span><span class="sxs-lookup"><span data-stu-id="6326f-117">**GetErrorEx**</span></span>](msvm-collectionreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="6326f-118">Извлекает дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6326f-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="6326f-119">**Равен**</span><span class="sxs-lookup"><span data-stu-id="6326f-119">**RequestStateChange**</span></span>](msvm-collectionreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="6326f-120">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="6326f-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="6326f-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="6326f-121">Properties</span></span>

<span data-ttu-id="6326f-122">Класс **мсвм \_ коллектионреференцепоинтекспортжоб** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6326f-122">The **Msvm\_CollectionReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6326f-123">**басереференцепоинтграупид**</span><span class="sxs-lookup"><span data-stu-id="6326f-123">**BaseReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6326f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6326f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-126">Идентификатор GUID точки ссылки коллекции, которая используется в качестве базы в експортоператион.</span><span class="sxs-lookup"><span data-stu-id="6326f-126">GUID of the collection reference point which is used as the base in the exportoperation.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-127">**Отменяемых**</span><span class="sxs-lookup"><span data-stu-id="6326f-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6326f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6326f-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-130">Указывает, можно ли отменить задание.</span><span class="sxs-lookup"><span data-stu-id="6326f-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="6326f-131">Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="6326f-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-132">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="6326f-132">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6326f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6326f-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-135">Идентификатор GUID группы виртуальных машин, для которой верикспортед файлы журналов.</span><span class="sxs-lookup"><span data-stu-id="6326f-135">GUID of the virtual machine group for which log files wereexported.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-136">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="6326f-136">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6326f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6326f-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6326f-139">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Задание CIM**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="6326f-139">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="6326f-140">Содержит описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="6326f-140">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-141">**експортдиректори**</span><span class="sxs-lookup"><span data-stu-id="6326f-141">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6326f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6326f-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-144">Расположение экспорта.</span><span class="sxs-lookup"><span data-stu-id="6326f-144">Export Location.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-145">**експортедконфигфилепасс**</span><span class="sxs-lookup"><span data-stu-id="6326f-145">**ExportedConfigFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-146">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6326f-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6326f-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-148">Путь к экспортированному файлу конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6326f-148">Path of the exported virtual machine config file.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-149">**експортеддискс**</span><span class="sxs-lookup"><span data-stu-id="6326f-149">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-150">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6326f-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6326f-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-152">Идентификаторы экземпляров виртуальных дисков, для которых были экспортированы файлы журналов.</span><span class="sxs-lookup"><span data-stu-id="6326f-152">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-153">**експортедгуестстатефилепасс**</span><span class="sxs-lookup"><span data-stu-id="6326f-153">**ExportedGuestStateFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-154">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6326f-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6326f-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-156">Путь к экспортированному файлу состояния гостя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6326f-156">Path of the exported virtual machine guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="6326f-157">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="6326f-157">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="6326f-158">**експортедлогфилепасс**</span><span class="sxs-lookup"><span data-stu-id="6326f-158">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-159">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6326f-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6326f-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-161">Пути к файлам журнала, которые были экспортированы.</span><span class="sxs-lookup"><span data-stu-id="6326f-161">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-162">**експортедрунтимефилепасс**</span><span class="sxs-lookup"><span data-stu-id="6326f-162">**ExportedRuntimeFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-163">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6326f-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6326f-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-165">Путь к экспортированному файлу состояния среды выполнения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6326f-165">Path of the exported virtual machine runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-166">**референцепоинтграупид**</span><span class="sxs-lookup"><span data-stu-id="6326f-166">**ReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6326f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6326f-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-169">Идентификатор GUID для экспортируемой точки ссылки коллекции.</span><span class="sxs-lookup"><span data-stu-id="6326f-169">GUID of the collection reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="6326f-170">**виртуалмачинеид**</span><span class="sxs-lookup"><span data-stu-id="6326f-170">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6326f-171">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6326f-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6326f-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6326f-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6326f-173">Идентификатор GUID виртуальных машин, для которых была выполнена операция экспорта.</span><span class="sxs-lookup"><span data-stu-id="6326f-173">GUID of the virtual machines for which export operation has been performed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6326f-174">Требования</span><span class="sxs-lookup"><span data-stu-id="6326f-174">Requirements</span></span>



| <span data-ttu-id="6326f-175">Требование</span><span class="sxs-lookup"><span data-stu-id="6326f-175">Requirement</span></span> | <span data-ttu-id="6326f-176">Значение</span><span class="sxs-lookup"><span data-stu-id="6326f-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6326f-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6326f-177">Minimum supported client</span></span><br/> | <span data-ttu-id="6326f-178">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="6326f-178">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6326f-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6326f-179">Minimum supported server</span></span><br/> | <span data-ttu-id="6326f-180">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6326f-180">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6326f-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6326f-181">Namespace</span></span><br/>                | <span data-ttu-id="6326f-182">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6326f-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6326f-183">MOF</span><span class="sxs-lookup"><span data-stu-id="6326f-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6326f-184"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6326f-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6326f-185">DLL</span><span class="sxs-lookup"><span data-stu-id="6326f-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6326f-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6326f-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6326f-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6326f-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6326f-188">**\_КОНКРЕТЕЖОБ CIM**</span><span class="sxs-lookup"><span data-stu-id="6326f-188">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

