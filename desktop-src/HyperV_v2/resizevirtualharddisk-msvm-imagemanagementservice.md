---
description: Изменяет размер существующего виртуального жесткого диска.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Метод Ресизевиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682830"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="d577a-103">Метод Ресизевиртуалхарддиск \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="d577a-103">ResizeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="d577a-104">Изменяет размер существующего виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d577a-104">Resizes an existing virtual hard disk.</span></span> <span data-ttu-id="d577a-105">Виртуальный жесткий диск должен быть вне сети.</span><span class="sxs-lookup"><span data-stu-id="d577a-105">The virtual hard disk must be offline.</span></span> <span data-ttu-id="d577a-106">Ограничения на использование для этого метода см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="d577a-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d577a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d577a-107">Syntax</span></span>


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d577a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d577a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d577a-109">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d577a-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d577a-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="d577a-110">Type: **string**</span></span>

<span data-ttu-id="d577a-111">Полный путь к файлу виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d577a-111">The fully qualified path of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="d577a-112">*Максинтерналсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d577a-112">*MaxInternalSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d577a-113">Тип: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d577a-113">Type: **uint64**</span></span>

<span data-ttu-id="d577a-114">Максимальный размер виртуального жесткого диска, отображаемый виртуальной машиной в байтах.</span><span class="sxs-lookup"><span data-stu-id="d577a-114">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="d577a-115">Минимальное значение *максинтерналсизе* — *DiskSize* + 512 — (*DiskSize* mod 512).</span><span class="sxs-lookup"><span data-stu-id="d577a-115">*MaxInternalSize* minimum value is *DiskSize* + 512 - (*DiskSize* mod 512).</span></span> <span data-ttu-id="d577a-116">*DiskSize* — это размер файла виртуального жесткого диска в байтах.</span><span class="sxs-lookup"><span data-stu-id="d577a-116">*DiskSize* is the size of the virtual hard disk file, in bytes.</span></span> <span data-ttu-id="d577a-117">Если указанное значение *максинтерналсизе* меньше минимального значения, возвращается ошибка инвалидпараметер (32773).</span><span class="sxs-lookup"><span data-stu-id="d577a-117">The InvalidParameter error (32773) is returned if the *MaxInternalSize* value specified is less than the minimum value.</span></span>

</dd> <dt>

<span data-ttu-id="d577a-118">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d577a-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d577a-119">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d577a-119">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="d577a-120">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d577a-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d577a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d577a-121">Return value</span></span>

<span data-ttu-id="d577a-122">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d577a-122">Type: **uint32**</span></span>

<span data-ttu-id="d577a-123">Этот метод может возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d577a-123">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d577a-124">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d577a-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-125">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d577a-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-126">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="d577a-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-127">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="d577a-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-128">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="d577a-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-129">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="d577a-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-130">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="d577a-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-131">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="d577a-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-132">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="d577a-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-133">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="d577a-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-134">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="d577a-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-135">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="d577a-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-136">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="d577a-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d577a-137">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="d577a-137">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d577a-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d577a-138">Remarks</span></span>

<span data-ttu-id="d577a-139">С этим методом можно использовать только следующие типы виртуальных жестких дисков при увеличении размера виртуального жесткого диска:</span><span class="sxs-lookup"><span data-stu-id="d577a-139">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being increased:</span></span>

-   <span data-ttu-id="d577a-140">Фиксированный виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="d577a-140">Fixed VHD</span></span>
-   <span data-ttu-id="d577a-141">Фиксированный VHDX</span><span class="sxs-lookup"><span data-stu-id="d577a-141">Fixed VHDX</span></span>
-   <span data-ttu-id="d577a-142">Динамический виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="d577a-142">Dynamic VHD</span></span>
-   <span data-ttu-id="d577a-143">Динамические VHDX</span><span class="sxs-lookup"><span data-stu-id="d577a-143">Dynamic VHDX</span></span>
-   <span data-ttu-id="d577a-144">Разностные VHDX</span><span class="sxs-lookup"><span data-stu-id="d577a-144">Differencing VHDX</span></span>

<span data-ttu-id="d577a-145">С этим методом можно использовать только следующие типы виртуальных жестких дисков при уменьшении размера виртуального жесткого диска:</span><span class="sxs-lookup"><span data-stu-id="d577a-145">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being decreased:</span></span>

-   <span data-ttu-id="d577a-146">Фиксированный VHDX</span><span class="sxs-lookup"><span data-stu-id="d577a-146">Fixed VHDX</span></span>
-   <span data-ttu-id="d577a-147">Динамические VHDX</span><span class="sxs-lookup"><span data-stu-id="d577a-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="d577a-148">Разностные VHDX</span><span class="sxs-lookup"><span data-stu-id="d577a-148">Differencing VHDX</span></span>

<span data-ttu-id="d577a-149">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d577a-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d577a-150">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d577a-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d577a-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="d577a-151">Examples</span></span>

<span data-ttu-id="d577a-152">В следующем примере кода C# разворачивается файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d577a-152">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="d577a-153">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d577a-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="d577a-154">Требования</span><span class="sxs-lookup"><span data-stu-id="d577a-154">Requirements</span></span>



| <span data-ttu-id="d577a-155">Требование</span><span class="sxs-lookup"><span data-stu-id="d577a-155">Requirement</span></span> | <span data-ttu-id="d577a-156">Значение</span><span class="sxs-lookup"><span data-stu-id="d577a-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d577a-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d577a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d577a-158">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d577a-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d577a-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d577a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d577a-160">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d577a-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d577a-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d577a-161">Namespace</span></span><br/>                | <span data-ttu-id="d577a-162">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d577a-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d577a-163">MOF</span><span class="sxs-lookup"><span data-stu-id="d577a-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d577a-164"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d577a-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d577a-165">DLL</span><span class="sxs-lookup"><span data-stu-id="d577a-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d577a-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d577a-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d577a-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d577a-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="d577a-168">[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d577a-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d577a-169">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="d577a-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

