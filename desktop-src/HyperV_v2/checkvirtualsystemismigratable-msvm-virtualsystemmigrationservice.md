---
description: Определяет, можно ли перенести указанную виртуальную систему.
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: Метод Чекквиртуалсистемисмигратабле класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1aed843f3f0f4c6c30eb6125cdd5859cdba902d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896846"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="eba0b-103">Метод Чекквиртуалсистемисмигратабле \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="eba0b-103">CheckVirtualSystemIsMigratable method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="eba0b-104">Определяет, можно ли перенести указанную виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="eba0b-104">Determines whether the specified virtual system can be migrated.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba0b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eba0b-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="eba0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eba0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eba0b-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eba0b-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba0b-108">Ссылка на экземпляр класса платформы [**CIM \_**](cim-computersystem.md) , представляющий виртуальную машину для проверки возможности миграции.</span><span class="sxs-lookup"><span data-stu-id="eba0b-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="eba0b-109">*Дестинатионхост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eba0b-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba0b-110">Имя хостовой системы для миграции.</span><span class="sxs-lookup"><span data-stu-id="eba0b-110">The name of the host system for the migration.</span></span> <span data-ttu-id="eba0b-111">Формат этого имени задается свойством **дестинатионхостформатссуппортед** класса [**мсвм \_ виртуалсистеммигратионкапабилитиес**](msvm-virtualsystemmigrationcapabilities.md) , связанного с этим классом.</span><span class="sxs-lookup"><span data-stu-id="eba0b-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="eba0b-112">*Мигратионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eba0b-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba0b-113">Встроенный экземпляр класса [**мсвм \_ виртуалсистеммигратионсеттингдата**](msvm-virtualsystemmigrationsettingdata.md) , представляющий параметры для операции миграции.</span><span class="sxs-lookup"><span data-stu-id="eba0b-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="eba0b-114">*Невсистемсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eba0b-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba0b-115">Встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющий новые свойства, применимые к виртуальной системе после переноса.</span><span class="sxs-lookup"><span data-stu-id="eba0b-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="eba0b-116">*Невресаурцесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eba0b-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba0b-117">Массив строк, содержащий встроенный экземпляр класса [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) , который представляет новые свойства, применимые к виртуальным ресурсам виртуальной системы после переноса.</span><span class="sxs-lookup"><span data-stu-id="eba0b-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="eba0b-118">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eba0b-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eba0b-119">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eba0b-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eba0b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eba0b-120">Return value</span></span>

<span data-ttu-id="eba0b-121">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="eba0b-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="eba0b-122">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="eba0b-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-123">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="eba0b-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-124">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="eba0b-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-125">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="eba0b-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-126">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="eba0b-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-127">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="eba0b-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-128">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="eba0b-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-129">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="eba0b-129">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-130">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="eba0b-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-131">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="eba0b-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-132">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="eba0b-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="eba0b-133">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="eba0b-133">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="eba0b-134">Требования</span><span class="sxs-lookup"><span data-stu-id="eba0b-134">Requirements</span></span>



| <span data-ttu-id="eba0b-135">Требование</span><span class="sxs-lookup"><span data-stu-id="eba0b-135">Requirement</span></span> | <span data-ttu-id="eba0b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="eba0b-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba0b-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eba0b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="eba0b-138">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eba0b-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eba0b-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eba0b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="eba0b-140">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eba0b-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eba0b-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eba0b-141">Namespace</span></span><br/>                | <span data-ttu-id="eba0b-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="eba0b-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eba0b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="eba0b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eba0b-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eba0b-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eba0b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="eba0b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eba0b-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eba0b-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eba0b-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eba0b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba0b-148">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="eba0b-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

