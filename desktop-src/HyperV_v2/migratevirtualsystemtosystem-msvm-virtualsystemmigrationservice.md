---
description: Перемещает или переносит виртуальную систему в целевую систему.
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: Метод Мигратевиртуалсистемтосистем класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a346596b094b60456af8e2b63865bec1171d99ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344972"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="39a56-103">Метод Мигратевиртуалсистемтосистем \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="39a56-103">MigrateVirtualSystemToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="39a56-104">Перемещает или переносит виртуальную систему в целевую систему.</span><span class="sxs-lookup"><span data-stu-id="39a56-104">Moves, migrates, or relocates a virtual system to a target system.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a56-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39a56-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="39a56-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a56-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a56-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a56-108">Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий систему виртуального компьютера для переноса.</span><span class="sxs-lookup"><span data-stu-id="39a56-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="39a56-109">*Дестинатионсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a56-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a56-110">Ссылка на экземпляр класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющий систему, в которую необходимо выполнить миграцию.</span><span class="sxs-lookup"><span data-stu-id="39a56-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system to be migrated to.</span></span>

</dd> <dt>

<span data-ttu-id="39a56-111">*Мигратионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a56-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a56-112">Встроенный экземпляр класса [**мсвм \_ виртуалсистеммигратионсеттингдата**](msvm-virtualsystemmigrationsettingdata.md) , представляющий параметры для операции миграции.</span><span class="sxs-lookup"><span data-stu-id="39a56-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="39a56-113">*Невсистемсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a56-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a56-114">Встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющий новые свойства, применимые к виртуальной системе после переноса.</span><span class="sxs-lookup"><span data-stu-id="39a56-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="39a56-115">*Невресаурцесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a56-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a56-116">Массив строк, содержащий встроенный экземпляр класса [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) , который представляет новые свойства, применимые к виртуальным ресурсам виртуальной системы после переноса.</span><span class="sxs-lookup"><span data-stu-id="39a56-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="39a56-117">*Невкомпутерсистем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39a56-117">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39a56-118">Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий новую перенесенную систему.</span><span class="sxs-lookup"><span data-stu-id="39a56-118">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the new migrated system.</span></span>

</dd> <dt>

<span data-ttu-id="39a56-119">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39a56-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39a56-120">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="39a56-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a56-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39a56-121">Return value</span></span>

<span data-ttu-id="39a56-122">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="39a56-122">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="39a56-123">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="39a56-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-124">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="39a56-124">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-125">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="39a56-125">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-126">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="39a56-126">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-127">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="39a56-127">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-128">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="39a56-128">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-129">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="39a56-129">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-130">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="39a56-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-131">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="39a56-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-132">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="39a56-132">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="39a56-133">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="39a56-133">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="39a56-134">Требования</span><span class="sxs-lookup"><span data-stu-id="39a56-134">Requirements</span></span>



| <span data-ttu-id="39a56-135">Требование</span><span class="sxs-lookup"><span data-stu-id="39a56-135">Requirement</span></span> | <span data-ttu-id="39a56-136">Значение</span><span class="sxs-lookup"><span data-stu-id="39a56-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a56-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39a56-137">Minimum supported client</span></span><br/> | <span data-ttu-id="39a56-138">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="39a56-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="39a56-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39a56-139">Minimum supported server</span></span><br/> | <span data-ttu-id="39a56-140">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="39a56-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39a56-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="39a56-141">Namespace</span></span><br/>                | <span data-ttu-id="39a56-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="39a56-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="39a56-143">MOF</span><span class="sxs-lookup"><span data-stu-id="39a56-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39a56-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39a56-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39a56-145">DLL</span><span class="sxs-lookup"><span data-stu-id="39a56-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39a56-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39a56-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39a56-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39a56-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a56-148">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="39a56-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

