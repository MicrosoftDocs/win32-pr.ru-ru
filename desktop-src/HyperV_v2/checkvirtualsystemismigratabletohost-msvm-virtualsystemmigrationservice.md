---
description: Определяет, можно ли перенести указанную виртуальную систему на целевой узел, заданный сетевым именем или IP-адресом.
ms.assetid: eacc8448-4683-48df-81b9-8599292944db
title: Метод Чекквиртуалсистемисмигратаблетохост класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b81f6562f892acbaa5bf7ff7f4f3c772574bd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683261"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="81925-103">Метод Чекквиртуалсистемисмигратаблетохост \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="81925-103">CheckVirtualSystemIsMigratableToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="81925-104">Определяет, можно ли перенести указанную виртуальную систему на целевой узел, заданный сетевым именем или IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="81925-104">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="81925-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81925-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  string                  DestinationHost,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="81925-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81925-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81925-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81925-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81925-108">Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий виртуальную машину для проверки возможности миграции.</span><span class="sxs-lookup"><span data-stu-id="81925-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="81925-109">*Дестинатионхост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81925-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81925-110">Имя хостовой системы для миграции.</span><span class="sxs-lookup"><span data-stu-id="81925-110">The name of the host system for the migration.</span></span> <span data-ttu-id="81925-111">Формат этого имени задается свойством **дестинатионхостформатссуппортед** класса [**мсвм \_ виртуалсистеммигратионкапабилитиес**](msvm-virtualsystemmigrationcapabilities.md) , связанного с этим классом.</span><span class="sxs-lookup"><span data-stu-id="81925-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="81925-112">*Мигратионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81925-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81925-113">Встроенный экземпляр класса [**мсвм \_ виртуалсистеммигратионсеттингдата**](msvm-virtualsystemmigrationsettingdata.md) , представляющий параметры для операции миграции.</span><span class="sxs-lookup"><span data-stu-id="81925-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="81925-114">*Невсистемсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81925-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81925-115">Встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющий новые свойства, применимые к виртуальной системе после переноса.</span><span class="sxs-lookup"><span data-stu-id="81925-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="81925-116">*Невресаурцесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81925-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81925-117">Массив строк, содержащий встроенный экземпляр класса [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) , который представляет новые свойства, применимые к виртуальным ресурсам виртуальной системы после переноса.</span><span class="sxs-lookup"><span data-stu-id="81925-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="81925-118">*Переносимость* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81925-118">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81925-119">Получает результат проверки миграции, указывающий, можно ли успешно выполнить миграцию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="81925-119">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81925-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81925-120">Return value</span></span>

<span data-ttu-id="81925-121">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="81925-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="81925-122">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="81925-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81925-123">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="81925-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81925-124">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="81925-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81925-125">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="81925-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81925-126">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="81925-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81925-127">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="81925-127">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81925-128">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="81925-128">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="81925-129">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="81925-129">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81925-130">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="81925-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="81925-131">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="81925-131">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="81925-132">Требования</span><span class="sxs-lookup"><span data-stu-id="81925-132">Requirements</span></span>



| <span data-ttu-id="81925-133">Требование</span><span class="sxs-lookup"><span data-stu-id="81925-133">Requirement</span></span> | <span data-ttu-id="81925-134">Значение</span><span class="sxs-lookup"><span data-stu-id="81925-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81925-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81925-135">Minimum supported client</span></span><br/> | <span data-ttu-id="81925-136">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="81925-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81925-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81925-137">Minimum supported server</span></span><br/> | <span data-ttu-id="81925-138">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="81925-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81925-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="81925-139">Namespace</span></span><br/>                | <span data-ttu-id="81925-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="81925-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81925-141">MOF</span><span class="sxs-lookup"><span data-stu-id="81925-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81925-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81925-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81925-143">DLL</span><span class="sxs-lookup"><span data-stu-id="81925-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81925-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81925-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81925-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81925-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81925-146">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="81925-146">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




