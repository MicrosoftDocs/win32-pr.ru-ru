---
description: Проверяет указанную запланированную систему.
ms.assetid: cb969b38-f36d-4c70-b234-590f1c219d22
title: Метод Валидатепланнедсистем класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ValidatePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 96137c3774291e06bfffdea3843658a427e36950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817088"
---
# <a name="validateplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="0e0bb-103">Метод Валидатепланнедсистем \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="0e0bb-103">ValidatePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="0e0bb-104">Проверяет указанную запланированную систему.</span><span class="sxs-lookup"><span data-stu-id="0e0bb-104">Validates the specified planned system.</span></span> <span data-ttu-id="0e0bb-105">Сюда входят проверки конфигурации виртуальной машины, устройств, конфигурации моментальных снимков, устройств моментальных снимков, файлов сохраненных состояний и файлов хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e0bb-105">This involves checks of the virtual machine configuration, devices, snapshot configuration, snapshot devices, saved state files and storage files.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e0bb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e0bb-106">Syntax</span></span>


```mof
uint32 ValidatePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0e0bb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e0bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e0bb-108">*Планнедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e0bb-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e0bb-109">Ссылка на объект [**мсвм \_ планнедкомпутерсистем**](msvm-plannedcomputersystem.md) , представляющий запланированную систему для проверки.</span><span class="sxs-lookup"><span data-stu-id="0e0bb-109">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned system to be validated.</span></span>

</dd> <dt>

<span data-ttu-id="0e0bb-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0e0bb-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e0bb-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e0bb-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e0bb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e0bb-112">Return value</span></span>

<span data-ttu-id="0e0bb-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0e0bb-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0e0bb-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-115">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0e0bb-127">**Используемый файл** (32779)</span><span class="sxs-lookup"><span data-stu-id="0e0bb-127">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="0e0bb-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="0e0bb-128">Examples</span></span>

<span data-ttu-id="0e0bb-129">В следующем примере кода C# метод **валидатепланнедсистем** используется для проверки запланированной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0e0bb-129">The following C# sample uses the **ValidatePlannedSystem** method to validate a planned virtual machine.</span></span> <span data-ttu-id="0e0bb-130">Этот код взят из [примера запланированных виртуальных машин Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="0e0bb-130">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="0e0bb-131">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="0e0bb-131">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e0bb-132">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="0e0bb-132">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and validates it, displaying
/// any warnings produced.
/// </summary>
/// <param name="pvmName">The name of the PVM to be validated.</param>
internal static void
ValidatePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams = 
        managementService.GetMethodParameters("ValidatePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Validating Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams = 
            managementService.InvokeMethod("ValidatePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope))
            {
                using (ManagementObject job = 
                    new ManagementObject((string)outParams["Job"]))
                {
                    WmiUtilities.PrintMsvmErrors(job);
                }
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="0e0bb-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0e0bb-133">Requirements</span></span>



| <span data-ttu-id="0e0bb-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0e0bb-134">Requirement</span></span> | <span data-ttu-id="0e0bb-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0e0bb-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e0bb-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e0bb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0e0bb-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0e0bb-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0e0bb-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e0bb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0e0bb-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0e0bb-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e0bb-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0e0bb-140">Namespace</span></span><br/>                | <span data-ttu-id="0e0bb-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0e0bb-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0e0bb-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0e0bb-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e0bb-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e0bb-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e0bb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0e0bb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e0bb-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e0bb-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e0bb-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e0bb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e0bb-147">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="0e0bb-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

