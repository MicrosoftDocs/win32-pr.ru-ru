---
description: Проверяет конфигурацию запланированной виртуальной машины и преобразует ее в реализованную виртуальную машину.
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: Метод Реализепланнедсистем класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fc69cbc9be9fc72bc7c1184ec30d9e2b58ba2b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272076"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f974d-103">Метод Реализепланнедсистем \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f974d-103">RealizePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f974d-104">Проверяет конфигурацию запланированной виртуальной машины и преобразует ее в реализованную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f974d-104">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span> <span data-ttu-id="f974d-105">Любые файлы среды выполнения или сохраненные состояния, связанные с виртуальной машиной, будут скопированы из каталога импорта в корневой каталог данных виртуальной машины, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="f974d-105">Any runtime or saved state files associated with the virtual machine will be copied from the import directory to the virtual machine's data root, if applicable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f974d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f974d-106">Syntax</span></span>


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f974d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f974d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f974d-108">*Планнедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f974d-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f974d-109">Ссылка на экземпляр [**мсвм \_ планнедкомпутерсистем**](msvm-plannedcomputersystem.md) , который должен быть преобразован в реализованную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f974d-109">A reference to the [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) instance which is to be converted into a realized virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f974d-110">*Ресултингсистем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f974d-110">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f974d-111">Если операция выполняется синхронно, ссылка на объект [**CIM \_ ComputerSystem**](msvm-computersystem.md) , представляющий полученную реализованную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f974d-111">If the operation is completed synchronously, a reference to a [**CIM\_ComputerSystem**](msvm-computersystem.md) object that represents the resulting realized virtual machine.</span></span>

<span data-ttu-id="f974d-112">Тип данных, обновленный из [**мсвм \_ ComputerSystem**](msvm-computersystem.md) в Windows 10, версия 1703.</span><span class="sxs-lookup"><span data-stu-id="f974d-112">Datatype updated from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

</dd> <dt>

<span data-ttu-id="f974d-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f974d-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f974d-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f974d-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f974d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f974d-115">Return value</span></span>

<span data-ttu-id="f974d-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f974d-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f974d-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f974d-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f974d-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f974d-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f974d-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f974d-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f974d-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f974d-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f974d-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f974d-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f974d-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f974d-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f974d-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f974d-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f974d-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="f974d-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="f974d-130">Examples</span></span>

<span data-ttu-id="f974d-131">В следующем примере кода C# метод **реализепланнедсистем** используется для реализации запланированной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f974d-131">The following C# sample uses the **RealizePlannedSystem** method to realize a planned virtual machine.</span></span> <span data-ttu-id="f974d-132">Этот код взят из [примера запланированных виртуальных машин Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="f974d-132">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="f974d-133">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f974d-133">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f974d-134">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="f974d-134">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



## <a name="requirements"></a><span data-ttu-id="f974d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="f974d-135">Requirements</span></span>



| <span data-ttu-id="f974d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="f974d-136">Requirement</span></span> | <span data-ttu-id="f974d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f974d-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f974d-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f974d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f974d-139">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f974d-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f974d-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f974d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f974d-141">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f974d-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f974d-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f974d-142">Namespace</span></span><br/>                | <span data-ttu-id="f974d-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f974d-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f974d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="f974d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f974d-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f974d-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f974d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f974d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f974d-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f974d-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f974d-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f974d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f974d-149">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="f974d-149">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

