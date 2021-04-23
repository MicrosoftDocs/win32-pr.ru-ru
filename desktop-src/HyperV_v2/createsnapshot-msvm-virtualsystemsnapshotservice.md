---
description: Создает моментальный снимок виртуальной машины.
ms.assetid: 2de12fe7-5ec2-49d0-87ff-cd48c34fec46
title: Метод CreateSnapshot класса Msvm_VirtualSystemSnapshotService (Дбдаоинт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c62b4abf60e367da1c4ac4b176e5f5d70f547c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346365"
---
# <a name="createsnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="95805-103">Метод CreateSnapshot \_ класса Виртуалсистемснапшотсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="95805-103">CreateSnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="95805-104">Создает моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95805-104">Creates a snapshot of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="95805-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95805-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="95805-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95805-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95805-107">*Аффектедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95805-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95805-108">Ссылка на класс [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину для создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="95805-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to create a snapshot of.</span></span>

</dd> <dt>

<span data-ttu-id="95805-109">*Снапшотсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95805-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95805-110">Строка, содержащая встроенный экземпляр класса [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) , который содержит настройки параметров для моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="95805-110">A string that contains an embedded instance of a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) class that contains the parameter settings for the snapshot.</span></span> <span data-ttu-id="95805-111">Этот параметр является необязательным и может быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="95805-111">This parameter is optional and may be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="95805-112">*Снапшоттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95805-112">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95805-113">Указывает тип запрошенного моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="95805-113">Specifies the type of snapshot requested.</span></span> <span data-ttu-id="95805-114">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="95805-114">This must be one of the following values.</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="95805-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Полный моментальный снимок** (2)</span><span class="sxs-lookup"><span data-stu-id="95805-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="95805-116">Завершите создание моментального снимка виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95805-116">Complete snapshot of the virtual machine.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="95805-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Моментальный снимок диска** (3)</span><span class="sxs-lookup"><span data-stu-id="95805-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="95805-118">Моментальный снимок дисков виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95805-118">Snapshot of virtual machine disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="95805-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="95805-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="95805-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="95805-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="95805-121">*Ресултингснапшот* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="95805-121">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95805-122">Ссылка на объект [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , представляющий результирующий моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95805-122">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the resulting virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="95805-123">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95805-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95805-124">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="95805-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95805-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95805-125">Return value</span></span>

<span data-ttu-id="95805-126">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="95805-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="95805-127">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="95805-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="95805-128">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="95805-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="95805-129">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="95805-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="95805-130">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="95805-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="95805-131">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="95805-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="95805-132">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="95805-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="95805-133">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="95805-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="95805-134">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="95805-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="95805-135">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="95805-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="95805-136">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="95805-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="95805-137">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="95805-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="95805-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="95805-138">Examples</span></span>

<span data-ttu-id="95805-139">В следующем примере кода C# создается виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="95805-139">The following C# example code creates a virtual machine.</span></span> <span data-ttu-id="95805-140">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="95805-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95805-141">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="95805-141">To function correctly, the following code must be run on the virtual machine host server, and it must be run with Administrator privileges.</span></span>

 


```CSharp
public static void CreateSnapshot(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemSnapshotService");

    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("CreateSnapshot");

    // Set the AffectedSystem property.
    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    if (null == vm)
    {
        throw new ArgumentException(string.Format("The virtual machine \"{0}\" could not be found.", vmName));
    }

    inParams["AffectedSystem"] = vm.Path.Path;

    // Set the SnapshotSettings property.
#if(true)
    inParams["SnapshotSettings"] = "";
#else
    ManagementObject snapshotSettings = Utility.GetServiceObject(scope, "CIM_SettingData"); 
    inParams["SnapshotSettings"] = snapshotSettings.ToString();
#endif       
    // Set the SnapshotType property.
    inParams["SnapshotType"] = 2; // Full snapshot.

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("CreateSnapshot", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Snapshot was created successfully.");

            MiscClass.GetAffectedElement(outParams, scope);
        }
        else
        {
            Console.WriteLine("Failed to create snapshot VM");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Snapshot was created successfully.");
    }
    else
    {
        Console.WriteLine("Create virtual system snapshot failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="95805-142">Требования</span><span class="sxs-lookup"><span data-stu-id="95805-142">Requirements</span></span>



| <span data-ttu-id="95805-143">Требование</span><span class="sxs-lookup"><span data-stu-id="95805-143">Requirement</span></span> | <span data-ttu-id="95805-144">Значение</span><span class="sxs-lookup"><span data-stu-id="95805-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95805-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95805-145">Minimum supported client</span></span><br/> | <span data-ttu-id="95805-146">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="95805-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="95805-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95805-147">Minimum supported server</span></span><br/> | <span data-ttu-id="95805-148">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="95805-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95805-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="95805-149">Namespace</span></span><br/>                | <span data-ttu-id="95805-150">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="95805-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="95805-151">Header</span><span class="sxs-lookup"><span data-stu-id="95805-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="95805-152"><dt>Дбдаоинт. h</dt></span><span class="sxs-lookup"><span data-stu-id="95805-152"><dt>Dbdaoint.h</dt></span></span> </dl>                   |
| <span data-ttu-id="95805-153">MOF</span><span class="sxs-lookup"><span data-stu-id="95805-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95805-154"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95805-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95805-155">DLL</span><span class="sxs-lookup"><span data-stu-id="95805-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95805-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95805-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95805-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95805-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95805-158">**Мсвм \_ виртуалсистемснапшотсервице**</span><span class="sxs-lookup"><span data-stu-id="95805-158">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="95805-159">**Креатевиртуалсистемснапшот (v1)**</span><span class="sxs-lookup"><span data-stu-id="95805-159">**CreateVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/createvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

