---
description: Возвращает список \_ экземпляров мсвм компатибилитивектор, которые можно использовать для проверки совместимости виртуальной машины с узлом.
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Метод Msvm_VirtualSystemMigrationService:: Жетсистемкомпатибилитивекторс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990937"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a><span data-ttu-id="7f2d3-103">Мсвм \_ виртуалсистеммигратионсервице:: жетсистемкомпатибилитивекторс, метод</span><span class="sxs-lookup"><span data-stu-id="7f2d3-103">Msvm\_VirtualSystemMigrationService::GetSystemCompatibilityVectors method</span></span>

<span data-ttu-id="7f2d3-104">Возвращает список экземпляров [**мсвм \_ компатибилитивектор**](msvm-compatibilityvector.md) , которые можно использовать для проверки совместимости виртуальной машины с узлом.</span><span class="sxs-lookup"><span data-stu-id="7f2d3-104">Gets a list of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that can be used to check for virtual machine (VM) to host compatibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f2d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f2d3-105">Syntax</span></span>


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a><span data-ttu-id="7f2d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f2d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f2d3-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f2d3-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2d3-108">Ссылка на класс [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий виртуальную машину, для которой нужно получить векторы совместимости.</span><span class="sxs-lookup"><span data-stu-id="7f2d3-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the VM to retrieve compatibility vectors for.</span></span> <span data-ttu-id="7f2d3-109">Если этот параметр относится к системе компьютера размещения, данные, возвращаемые в параметре *компатибилитивекторс* , можно использовать, чтобы определить, можно ли быстро перенести любую из виртуальных машин на компьютере, на котором размещен компьютер, в другую систему.</span><span class="sxs-lookup"><span data-stu-id="7f2d3-109">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityVectors* parameter can be used to determine whether any of the VMs on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="7f2d3-110">*Компатибилитивекторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f2d3-110">*CompatibilityVectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2d3-111">Массив экземпляров [**мсвм \_ компатибилитивектор**](msvm-compatibilityvector.md) , содержащих сведения о совместимости для виртуальных машин или системы компьютера размещения.</span><span class="sxs-lookup"><span data-stu-id="7f2d3-111">An array of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that contain the compatibility info for the VMs or hosting computer system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f2d3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f2d3-112">Return value</span></span>

<span data-ttu-id="7f2d3-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7f2d3-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7f2d3-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-115">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7f2d3-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="7f2d3-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7f2d3-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f2d3-127">Remarks</span></span>

<span data-ttu-id="7f2d3-128">**Жетсистемкомпатибилитивекторс** получает сведения о совместимости для виртуальной машины (ВМ) (при запуске на компьютере виртуальной машины) или на узле (при запуске в системе главного компьютера).</span><span class="sxs-lookup"><span data-stu-id="7f2d3-128">**GetSystemCompatibilityVectors** gets compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span> <span data-ttu-id="7f2d3-129">Сведения о совместимости остаются непрозрачными для клиента, а сведения предоставляют способ сравнения сведений о совместимости узла с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="7f2d3-129">The compatibility info remains opaque to the client while the info provides a way to compare the host compatibility info with that of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f2d3-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7f2d3-130">Requirements</span></span>



| <span data-ttu-id="7f2d3-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7f2d3-131">Requirement</span></span> | <span data-ttu-id="7f2d3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7f2d3-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2d3-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f2d3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7f2d3-134">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f2d3-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7f2d3-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f2d3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7f2d3-136">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f2d3-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7f2d3-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7f2d3-137">Namespace</span></span><br/>                | <span data-ttu-id="7f2d3-138">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7f2d3-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="7f2d3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7f2d3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f2d3-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f2d3-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f2d3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7f2d3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f2d3-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7f2d3-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7f2d3-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f2d3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f2d3-144">**Мсвм \_ компатибилитивектор**</span><span class="sxs-lookup"><span data-stu-id="7f2d3-144">**Msvm\_CompatibilityVector**</span></span>](msvm-compatibilityvector.md)
</dt> <dt>

[<span data-ttu-id="7f2d3-145">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="7f2d3-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




