---
description: Преобразует существующий виртуальный жесткий диск в другой тип или формат.
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: Метод Конвертвиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 766b117b69ecfebd13986d02ca21df3725981bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683760"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="86e48-103">Метод Конвертвиртуалхарддиск \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="86e48-103">ConvertVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="86e48-104">Преобразует существующий виртуальный жесткий диск в другой тип или формат.</span><span class="sxs-lookup"><span data-stu-id="86e48-104">Converts an existing virtual hard disk to a different type or format.</span></span> <span data-ttu-id="86e48-105">Этот метод создает новый виртуальный жесткий диск и не преобразует исходный виртуальный жесткий диск на месте.</span><span class="sxs-lookup"><span data-stu-id="86e48-105">This method creates a new virtual hard disk and does not convert the source virtual hard disk in place.</span></span> <span data-ttu-id="86e48-106">Ограничения на использование для этого метода см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="86e48-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e48-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86e48-107">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="86e48-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="86e48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e48-109">*Источник* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86e48-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e48-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="86e48-110">Type: **string**</span></span>

<span data-ttu-id="86e48-111">Полный путь к файлу исходного виртуального жесткого диска для преобразования.</span><span class="sxs-lookup"><span data-stu-id="86e48-111">The fully qualified path of the source virtual hard disk file to convert.</span></span> <span data-ttu-id="86e48-112">Этот файл не будет изменен в результате этой операции.</span><span class="sxs-lookup"><span data-stu-id="86e48-112">This file will not be modified as a result of this operation.</span></span>

</dd> <dt>

<span data-ttu-id="86e48-113">*Виртуалдисксеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86e48-113">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e48-114">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="86e48-114">Type: **string**</span></span>

<span data-ttu-id="86e48-115">Строковое представление класса [**мсвм \_ виртуалхарддисксеттингдата**](msvm-virtualharddisksettingdata.md) , в котором указаны атрибуты нового виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="86e48-115">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the attributes of the new virtual hard disk.</span></span> <span data-ttu-id="86e48-116">Должны быть заданы свойства **путь**, **Тип**, **Формат**, **парентпас** **, размер и** **логикалсекторсизе** .</span><span class="sxs-lookup"><span data-stu-id="86e48-116">The **Path**, **Type**, **Format**, **ParentPath**, **BlockSize**, and **LogicalSectorSize** properties must be set.</span></span> <span data-ttu-id="86e48-117">Свойство **парентпас** может иметь **значение NULL** , если оно не требуется.</span><span class="sxs-lookup"><span data-stu-id="86e48-117">The **ParentPath** property can be **Null** if it is not needed.</span></span> <span data-ttu-id="86e48-118">Задайте для свойств размерности и **логикалсекторсизе** значение **0, чтобы** использовать значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86e48-118">Set the **BlockSize** and **LogicalSectorSize** properties to 0 to use the default values.</span></span>

<span data-ttu-id="86e48-119">Чтобы указать формат (VHD или VHDX) нового виртуального жесткого диска, задайте для расширения **пути** соответствующее значение (". VHD" или ". VHDX").</span><span class="sxs-lookup"><span data-stu-id="86e48-119">To specify the format (VHD or VHDX) of the new virtual hard disk, set the extension of the **Path** to the appropriate value (".vhd" or ".vhdx").</span></span> <span data-ttu-id="86e48-120">Свойство **Format** должно соответствовать расширению имени файла в **пути**.</span><span class="sxs-lookup"><span data-stu-id="86e48-120">The **Format** property must match the file name extension in the **Path**.</span></span>

<span data-ttu-id="86e48-121">Свойство **логикалсекторсизе** будет пропущено.</span><span class="sxs-lookup"><span data-stu-id="86e48-121">The **LogicalSectorSize** property will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="86e48-122">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="86e48-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86e48-123">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="86e48-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="86e48-124">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="86e48-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e48-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86e48-125">Return value</span></span>

<span data-ttu-id="86e48-126">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86e48-126">Type: **uint32**</span></span>

<span data-ttu-id="86e48-127">Этот метод может возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="86e48-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="86e48-128">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="86e48-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-129">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="86e48-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-130">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="86e48-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-131">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="86e48-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-132">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="86e48-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-133">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="86e48-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-134">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="86e48-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-135">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="86e48-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-136">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="86e48-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-137">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="86e48-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-138">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="86e48-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-139">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="86e48-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-140">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="86e48-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="86e48-141">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="86e48-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="86e48-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86e48-142">Remarks</span></span>

<span data-ttu-id="86e48-143">С этим методом можно использовать только следующие типы виртуальных жестких дисков:</span><span class="sxs-lookup"><span data-stu-id="86e48-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="86e48-144">Фиксированный виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="86e48-144">Fixed VHD</span></span>
-   <span data-ttu-id="86e48-145">Фиксированный VHDX</span><span class="sxs-lookup"><span data-stu-id="86e48-145">Fixed VHDX</span></span>
-   <span data-ttu-id="86e48-146">Динамический виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="86e48-146">Dynamic VHD</span></span>
-   <span data-ttu-id="86e48-147">Динамические VHDX</span><span class="sxs-lookup"><span data-stu-id="86e48-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="86e48-148">Разностный виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="86e48-148">Differencing VHD</span></span>
-   <span data-ttu-id="86e48-149">Разностные VHDX</span><span class="sxs-lookup"><span data-stu-id="86e48-149">Differencing VHDX</span></span>

<span data-ttu-id="86e48-150">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="86e48-150">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="86e48-151">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="86e48-151">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="86e48-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="86e48-152">Examples</span></span>

<span data-ttu-id="86e48-153">Следующий пример на C# Преобразует виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="86e48-153">The following C# example converts a virtual hard disk.</span></span> <span data-ttu-id="86e48-154">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="86e48-154">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="86e48-155">Требования</span><span class="sxs-lookup"><span data-stu-id="86e48-155">Requirements</span></span>



| <span data-ttu-id="86e48-156">Требование</span><span class="sxs-lookup"><span data-stu-id="86e48-156">Requirement</span></span> | <span data-ttu-id="86e48-157">Значение</span><span class="sxs-lookup"><span data-stu-id="86e48-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e48-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86e48-158">Minimum supported client</span></span><br/> | <span data-ttu-id="86e48-159">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="86e48-159">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="86e48-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86e48-160">Minimum supported server</span></span><br/> | <span data-ttu-id="86e48-161">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="86e48-161">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86e48-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="86e48-162">Namespace</span></span><br/>                | <span data-ttu-id="86e48-163">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="86e48-163">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="86e48-164">MOF</span><span class="sxs-lookup"><span data-stu-id="86e48-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86e48-165"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86e48-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="86e48-166">DLL</span><span class="sxs-lookup"><span data-stu-id="86e48-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e48-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="86e48-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="86e48-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86e48-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e48-169">**Конвертвиртуалхарддиск (v1)**</span><span class="sxs-lookup"><span data-stu-id="86e48-169">**ConvertVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="86e48-170">[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86e48-170">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="86e48-171">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="86e48-171">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

