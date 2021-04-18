---
description: Создает новую запланированную компьютерную систему на основе указанного определения виртуальной машины.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Метод Импортсистемдефинитион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683105"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="3a149-103">Метод Импортсистемдефинитион \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="3a149-103">ImportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3a149-104">Создает новую запланированную компьютерную систему на основе указанного определения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3a149-104">Creates a new planned computer system based on the specified virtual machine definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a149-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a149-105">Syntax</span></span>


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3a149-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a149-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a149-107">*Системдефинитионфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a149-107">*SystemDefinitionFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a149-108">Полный путь к файлу определения системы (XML или exp), представляющему виртуальную машину, которую необходимо импортировать.</span><span class="sxs-lookup"><span data-stu-id="3a149-108">The fully qualified path to the system definition file (.xml or .exp) representing the virtual machine which is to be imported.</span></span> <span data-ttu-id="3a149-109">Файл определения не должен быть уже используется основной системой или платформой виртуализации.</span><span class="sxs-lookup"><span data-stu-id="3a149-109">The definition file must not already be in use by the host system or the virtualization platform.</span></span>

</dd> <dt>

<span data-ttu-id="3a149-110">*Снапшотфолдер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a149-110">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a149-111">Полный путь к папке, в которой можно найти конфигурации моментальных снимков для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3a149-111">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span> <span data-ttu-id="3a149-112">Для поиска моментальных снимков, на которые ссылается определение виртуальной машины, будет выполнен поиск в этой папке.</span><span class="sxs-lookup"><span data-stu-id="3a149-112">This folder will be searched in order to locate any snapshots referenced by the virtual machine definition.</span></span> <span data-ttu-id="3a149-113">Все моментальные снимки, на которые имеются ссылки, не найденные в этом расположении, необходимо удалить с помощью метода [**дестройснапшот**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) или импортировать с помощью метода [**импортснапшотдефинитионс**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) перед реализацией запланированной компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="3a149-113">Any referenced snapshots not found in this location must be deleted using the [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) method, or imported using the [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) method prior to realizing the planned computer system.</span></span>

</dd> <dt>

<span data-ttu-id="3a149-114">*Женератеневсистемидентифиер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a149-114">*GenerateNewSystemIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a149-115">Указывает, следует ли повторно использовать уникальный идентификатор для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3a149-115">Indicates whether to reuse the unique identifier for the virtual machine.</span></span> <span data-ttu-id="3a149-116">Если этот параметр имеет **значение true**, то создается новый идентификатор системы.</span><span class="sxs-lookup"><span data-stu-id="3a149-116">If this parameter is **True**, then a new system identifier is generated.</span></span> <span data-ttu-id="3a149-117">Если этот параметр имеет **значение false**, то используется существующий идентификатор системы.</span><span class="sxs-lookup"><span data-stu-id="3a149-117">If this parameter is **False**, then the existing system identifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="3a149-118">*Импортедсистем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3a149-118">*ImportedSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a149-119">Если операция завершается синхронно, ссылка на объект [**мсвм \_ планнедкомпутерсистем**](msvm-plannedcomputersystem.md) , представляющий импортированную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3a149-119">If the operation completes synchronously, a reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the imported virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="3a149-120">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3a149-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a149-121">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a149-121">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a149-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a149-122">Return value</span></span>

<span data-ttu-id="3a149-123">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3a149-123">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3a149-124">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="3a149-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-125">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="3a149-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-126">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="3a149-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-127">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="3a149-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-128">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="3a149-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-129">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="3a149-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-130">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="3a149-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-131">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="3a149-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-132">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="3a149-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-133">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="3a149-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-134">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="3a149-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-135">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="3a149-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-136">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="3a149-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3a149-137">**Используемый файл** (32779)</span><span class="sxs-lookup"><span data-stu-id="3a149-137">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3a149-138">Требования</span><span class="sxs-lookup"><span data-stu-id="3a149-138">Requirements</span></span>



| <span data-ttu-id="3a149-139">Требование</span><span class="sxs-lookup"><span data-stu-id="3a149-139">Requirement</span></span> | <span data-ttu-id="3a149-140">Значение</span><span class="sxs-lookup"><span data-stu-id="3a149-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a149-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a149-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3a149-142">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3a149-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a149-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a149-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3a149-144">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3a149-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a149-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a149-145">Namespace</span></span><br/>                | <span data-ttu-id="3a149-146">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3a149-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a149-147">MOF</span><span class="sxs-lookup"><span data-stu-id="3a149-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a149-148"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a149-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a149-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3a149-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a149-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a149-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a149-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a149-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a149-152">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="3a149-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

