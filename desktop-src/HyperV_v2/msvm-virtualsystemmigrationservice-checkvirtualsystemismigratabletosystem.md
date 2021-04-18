---
description: Определяет, можно ли перенести указанную виртуальную систему в целевую систему.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Метод Чекквиртуалсистемисмигратаблетосистем класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682483"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="e8f53-103">Метод Чекквиртуалсистемисмигратаблетосистем \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="e8f53-103">CheckVirtualSystemIsMigratableToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e8f53-104">Определяет, можно ли перенести указанную виртуальную систему в целевую систему.</span><span class="sxs-lookup"><span data-stu-id="e8f53-104">Determines whether the specified virtual system can be migrated to a destination system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8f53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8f53-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="e8f53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8f53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8f53-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8f53-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f53-108">Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий виртуальную машину для проверки возможности миграции.</span><span class="sxs-lookup"><span data-stu-id="e8f53-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="e8f53-109">*Дестинатионсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8f53-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f53-110">Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий виртуальную машину для проверки возможности миграции.</span><span class="sxs-lookup"><span data-stu-id="e8f53-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability to.</span></span>

</dd> <dt>

<span data-ttu-id="e8f53-111">*Мигратионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8f53-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f53-112">Встроенный экземпляр класса [**мсвм \_ виртуалсистеммигратионсеттингдата**](msvm-virtualsystemmigrationsettingdata.md) , представляющий параметры для операции миграции.</span><span class="sxs-lookup"><span data-stu-id="e8f53-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="e8f53-113">*Невсистемсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8f53-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f53-114">Встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющий новые свойства, применимые к виртуальной системе после переноса.</span><span class="sxs-lookup"><span data-stu-id="e8f53-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e8f53-115">*Невресаурцесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8f53-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f53-116">Массив строк, содержащий встроенный экземпляр класса [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) , который представляет новые свойства, применимые к виртуальным ресурсам виртуальной системы после переноса.</span><span class="sxs-lookup"><span data-stu-id="e8f53-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e8f53-117">*Переносимость* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e8f53-117">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f53-118">Получает результат проверки миграции, указывающий, можно ли успешно выполнить миграцию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e8f53-118">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8f53-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8f53-119">Return value</span></span>

<span data-ttu-id="e8f53-120">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e8f53-120">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e8f53-121">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e8f53-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e8f53-122">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="e8f53-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e8f53-123">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="e8f53-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e8f53-124">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="e8f53-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e8f53-125">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="e8f53-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e8f53-126">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="e8f53-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e8f53-127">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="e8f53-127">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e8f53-128">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e8f53-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e8f53-129">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e8f53-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e8f53-130">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="e8f53-130">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e8f53-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e8f53-131">Requirements</span></span>



| <span data-ttu-id="e8f53-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e8f53-132">Requirement</span></span> | <span data-ttu-id="e8f53-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e8f53-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f53-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8f53-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e8f53-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e8f53-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e8f53-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8f53-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e8f53-137">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="e8f53-137">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8f53-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e8f53-138">Namespace</span></span><br/>                | <span data-ttu-id="e8f53-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e8f53-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e8f53-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e8f53-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8f53-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8f53-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8f53-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e8f53-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8f53-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e8f53-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e8f53-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8f53-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8f53-145">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="e8f53-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




