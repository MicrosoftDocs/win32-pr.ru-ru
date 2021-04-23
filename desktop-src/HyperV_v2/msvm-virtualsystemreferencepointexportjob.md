---
description: Этот класс представляет задание операции экспорта точки ссылки на виртуальную систему.
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Класс Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547295"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="c5be4-103">\_Класс мсвм виртуалсистемреференцепоинтекспортжоб</span><span class="sxs-lookup"><span data-stu-id="c5be4-103">Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="c5be4-104">Этот класс представляет задание операции экспорта точки ссылки на виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="c5be4-104">This class represents a virtual system reference point export operation job.</span></span>

<span data-ttu-id="c5be4-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c5be4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5be4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5be4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a><span data-ttu-id="c5be4-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c5be4-107">Members</span></span>

<span data-ttu-id="c5be4-108">Класс **мсвм \_ виртуалсистемреференцепоинтекспортжоб** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c5be4-108">The **Msvm\_VirtualSystemReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="c5be4-109">Методы</span><span class="sxs-lookup"><span data-stu-id="c5be4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c5be4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5be4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c5be4-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c5be4-111">Methods</span></span>

<span data-ttu-id="c5be4-112">Класс **мсвм \_ виртуалсистемреференцепоинтекспортжоб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c5be4-112">The **Msvm\_VirtualSystemReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="c5be4-113">Метод</span><span class="sxs-lookup"><span data-stu-id="c5be4-113">Method</span></span>                                                                                     | <span data-ttu-id="c5be4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c5be4-114">Description</span></span>                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="c5be4-115">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="c5be4-115">**GetError**</span></span>](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | <span data-ttu-id="c5be4-116">Извлекает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c5be4-116">Retrieves the error.</span></span><br/>                    |
| [<span data-ttu-id="c5be4-117">**жетеррорекс**</span><span class="sxs-lookup"><span data-stu-id="c5be4-117">**GetErrorEx**</span></span>](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="c5be4-118">Извлекает дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c5be4-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="c5be4-119">**Равен**</span><span class="sxs-lookup"><span data-stu-id="c5be4-119">**RequestStateChange**</span></span>](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="c5be4-120">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="c5be4-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="c5be4-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5be4-121">Properties</span></span>

<span data-ttu-id="c5be4-122">Класс **мсвм \_ виртуалсистемреференцепоинтекспортжоб** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c5be4-122">The **Msvm\_VirtualSystemReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5be4-123">**басереференцепоинтид**</span><span class="sxs-lookup"><span data-stu-id="c5be4-123">**BaseReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5be4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-126">Идентификатор GUID точки ссылки, используемой в качестве базы для операции экспорта.</span><span class="sxs-lookup"><span data-stu-id="c5be4-126">GUID of the reference point which is used as the base in the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="c5be4-127">**Отменяемых**</span><span class="sxs-lookup"><span data-stu-id="c5be4-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c5be4-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-130">Указывает, можно ли отменить задание.</span><span class="sxs-lookup"><span data-stu-id="c5be4-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="c5be4-131">Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="c5be4-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="c5be4-132">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="c5be4-132">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5be4-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-135">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Задание CIM**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="c5be4-135">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-136">Содержит описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="c5be4-136">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="c5be4-137">**експортдиректори**</span><span class="sxs-lookup"><span data-stu-id="c5be4-137">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5be4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-140">Расположение экспорта.</span><span class="sxs-lookup"><span data-stu-id="c5be4-140">The export location.</span></span>

</dd> <dt>

<span data-ttu-id="c5be4-141">**експортедконфигфилепас**</span><span class="sxs-lookup"><span data-stu-id="c5be4-141">**ExportedConfigFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5be4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-144">Путь к экспортированному файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c5be4-144">Path of the exported config file.</span></span>

</dd> <dt>

<span data-ttu-id="c5be4-145">**експортеддискс**</span><span class="sxs-lookup"><span data-stu-id="c5be4-145">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-146">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c5be4-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-148">Идентификаторы экземпляров виртуальных дисков, для которых были экспортированы файлы журналов.</span><span class="sxs-lookup"><span data-stu-id="c5be4-148">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="c5be4-149">**експортедгуестстатефилепас**</span><span class="sxs-lookup"><span data-stu-id="c5be4-149">**ExportedGuestStateFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5be4-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-152">Путь к экспортированному файлу состояния гостя.</span><span class="sxs-lookup"><span data-stu-id="c5be4-152">Path of the exported guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="c5be4-153">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="c5be4-153">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="c5be4-154">**експортедлогфилепасс**</span><span class="sxs-lookup"><span data-stu-id="c5be4-154">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-155">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c5be4-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-157">Пути к файлам журнала, которые были экспортированы.</span><span class="sxs-lookup"><span data-stu-id="c5be4-157">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="c5be4-158">**експортедрунтимефилепас**</span><span class="sxs-lookup"><span data-stu-id="c5be4-158">**ExportedRuntimeFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5be4-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-161">Путь к экспортированному файлу состояния среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="c5be4-161">Path of the exported runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="c5be4-162">**референцепоинтид**</span><span class="sxs-lookup"><span data-stu-id="c5be4-162">**ReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5be4-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-165">Идентификатор GUID экспортируемой точки ссылки.</span><span class="sxs-lookup"><span data-stu-id="c5be4-165">GUID of the reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="c5be4-166">**виртуалмачинеид**</span><span class="sxs-lookup"><span data-stu-id="c5be4-166">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5be4-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5be4-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5be4-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5be4-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5be4-169">Идентификатор GUID виртуальной машины, для которой были экспортированы файлы журналов.</span><span class="sxs-lookup"><span data-stu-id="c5be4-169">GUID of the virtual machine for which log files were exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5be4-170">Требования</span><span class="sxs-lookup"><span data-stu-id="c5be4-170">Requirements</span></span>



| <span data-ttu-id="c5be4-171">Требование</span><span class="sxs-lookup"><span data-stu-id="c5be4-171">Requirement</span></span> | <span data-ttu-id="c5be4-172">Значение</span><span class="sxs-lookup"><span data-stu-id="c5be4-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5be4-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5be4-173">Minimum supported client</span></span><br/> | <span data-ttu-id="c5be4-174">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="c5be4-174">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c5be4-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5be4-175">Minimum supported server</span></span><br/> | <span data-ttu-id="c5be4-176">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c5be4-176">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c5be4-177">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c5be4-177">Namespace</span></span><br/>                | <span data-ttu-id="c5be4-178">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c5be4-178">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c5be4-179">MOF</span><span class="sxs-lookup"><span data-stu-id="c5be4-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5be4-180"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5be4-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5be4-181">DLL</span><span class="sxs-lookup"><span data-stu-id="c5be4-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5be4-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5be4-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5be4-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5be4-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5be4-184">**\_КОНКРЕТЕЖОБ CIM**</span><span class="sxs-lookup"><span data-stu-id="c5be4-184">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

