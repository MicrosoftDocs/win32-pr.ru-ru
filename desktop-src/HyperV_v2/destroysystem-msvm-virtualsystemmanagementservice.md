---
description: Удаляет ранее определенную виртуальную машину из области управления основной системы.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Метод Дестройсистем класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1caf4e4a590bdbfe2f7543e23d5ca00018300fb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911692"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="d9910-103">Метод Дестройсистем \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="d9910-103">DestroySystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d9910-104">Удаляет ранее определенную виртуальную машину из области управления основной системы.</span><span class="sxs-lookup"><span data-stu-id="d9910-104">Removes the previously defined virtual machine from the management scope of the host system.</span></span> <span data-ttu-id="d9910-105">Все связанные определения ресурсов также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="d9910-105">Any associated resource definitions will also be removed.</span></span> <span data-ttu-id="d9910-106">Перед вызовом этого метода виртуальная машина должна находиться в выключенном или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="d9910-106">The virtual machine must be in the powered off or saved state prior to calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9910-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9910-107">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d9910-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9910-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9910-109">*Аффектедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9910-109">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9910-110">Тип: **CIM \_ ComputerSystem** .</span><span class="sxs-lookup"><span data-stu-id="d9910-110">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="d9910-111">Ссылка на экземпляр платформы CIM, представляющий [**экземпляр \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) виртуальной машины, который необходимо уничтожить.</span><span class="sxs-lookup"><span data-stu-id="d9910-111">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine instance to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="d9910-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d9910-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9910-113">Тип: **CIM \_ конкретежоб**</span><span class="sxs-lookup"><span data-stu-id="d9910-113">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="d9910-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9910-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9910-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9910-115">Return value</span></span>

<span data-ttu-id="d9910-116">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9910-116">Type: **uint32**</span></span>

<span data-ttu-id="d9910-117">Если этот метод выполняется синхронно, он возвращает 0, если он выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9910-117">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="d9910-118">Если этот метод выполняется асинхронно, возвращается 4096, а для отслеживания хода выполнения асинхронной операции можно использовать выходной параметр *задания* .</span><span class="sxs-lookup"><span data-stu-id="d9910-118">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="d9910-119">Любое другое возвращаемое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="d9910-119">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="d9910-120">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d9910-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d9910-121">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="d9910-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d9910-122">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="d9910-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d9910-123">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="d9910-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d9910-124">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="d9910-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d9910-125">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="d9910-125">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d9910-126">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d9910-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d9910-127">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d9910-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d9910-128">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d9910-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d9910-129">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="d9910-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d9910-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9910-130">Remarks</span></span>

<span data-ttu-id="d9910-131">Доступ к классу [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d9910-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d9910-132">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d9910-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d9910-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="d9910-133">Examples</span></span>

<span data-ttu-id="d9910-134">В следующем примере кода C# метод **дестройсистем** используется для удаления запланированной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9910-134">The following C# sample uses the **DestroySystem** method to remove a planned virtual machine.</span></span> <span data-ttu-id="d9910-135">Этот код взят из [примера запланированных виртуальных машин Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="d9910-135">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="d9910-136">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d9910-136">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9910-137">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="d9910-137">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="d9910-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d9910-138">Requirements</span></span>



| <span data-ttu-id="d9910-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d9910-139">Requirement</span></span> | <span data-ttu-id="d9910-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d9910-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9910-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9910-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d9910-142">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d9910-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d9910-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9910-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d9910-144">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d9910-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9910-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d9910-145">Namespace</span></span><br/>                | <span data-ttu-id="d9910-146">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d9910-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d9910-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d9910-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9910-148"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9910-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9910-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d9910-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9910-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d9910-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d9910-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9910-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9910-152">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="d9910-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

