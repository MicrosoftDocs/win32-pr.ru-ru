---
description: Ищет в указанной папке файлы определения моментальных снимков, связанные с указанной запланированной системой компьютера, и создает новый моментальный снимок в запланированной компьютерной системе для каждого связанного файла определения в этом расположении.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Метод Импортснапшотдефинитионс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9ebb36b030786ab88eab899190afcc7f3022286a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898338"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="b5531-103">Метод Импортснапшотдефинитионс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="b5531-103">ImportSnapshotDefinitions method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="b5531-104">Ищет в указанной папке файлы определения моментальных снимков, связанные с указанной запланированной системой компьютера, и создает новый моментальный снимок в запланированной компьютерной системе для каждого связанного файла определения в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="b5531-104">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5531-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5531-105">Syntax</span></span>


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b5531-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5531-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5531-107">*Планнедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5531-107">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-108">Ссылка на объект [**мсвм \_ планнедкомпутерсистем**](msvm-plannedcomputersystem.md) , представляющий запланированную виртуальную машину, которая ссылается на импортируемые моментальные снимки.</span><span class="sxs-lookup"><span data-stu-id="b5531-108">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned virtual machine which references the snapshots to be imported.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-109">*Снапшотфолдер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5531-109">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-110">Полный путь к папке, в которой можно найти конфигурации моментальных снимков для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b5531-110">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-111">*Импортедснапшотс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b5531-111">*ImportedSnapshots* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-112">Если операция завершается синхронно, то массив ссылок на экземпляры [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющие моментальные снимки, которые были успешно импортированы.</span><span class="sxs-lookup"><span data-stu-id="b5531-112">If the operation completes synchronously, an array of references to the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances representing the snapshots which were successfully imported.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b5531-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5531-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5531-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5531-115">Return value</span></span>

<span data-ttu-id="b5531-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b5531-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b5531-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="b5531-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="b5531-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="b5531-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="b5531-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="b5531-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="b5531-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="b5531-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="b5531-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="b5531-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="b5531-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="b5531-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="b5531-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="b5531-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b5531-130">**Используемый файл** (32779)</span><span class="sxs-lookup"><span data-stu-id="b5531-130">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b5531-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b5531-131">Requirements</span></span>



| <span data-ttu-id="b5531-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b5531-132">Requirement</span></span> | <span data-ttu-id="b5531-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b5531-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5531-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5531-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b5531-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b5531-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5531-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5531-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b5531-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b5531-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5531-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b5531-138">Namespace</span></span><br/>                | <span data-ttu-id="b5531-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b5531-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5531-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b5531-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5531-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5531-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5531-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b5531-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5531-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5531-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5531-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5531-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5531-145">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="b5531-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

