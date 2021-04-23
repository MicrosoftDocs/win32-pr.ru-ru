---
description: Сжимает файл виртуального жесткого диска.
ms.assetid: 1E64BD91-6FE6-4658-9EBF-615FC705B920
title: Метод Компактвиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CompactVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e8c148e51105d8c78021b58366e2f2df3913f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683761"
---
# <a name="compactvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="567a6-103">Метод Компактвиртуалхарддиск \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="567a6-103">CompactVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="567a6-104">Сжимает файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="567a6-104">Compacts a virtual hard disk file.</span></span> <span data-ttu-id="567a6-105">Сжатие — это процесс освобождения неиспользуемых частей виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="567a6-105">Compacting is the process of freeing unused portions of the virtual hard disk.</span></span> <span data-ttu-id="567a6-106">Виртуальный жесткий диск не подключен автоматически.</span><span class="sxs-lookup"><span data-stu-id="567a6-106">The virtual hard disk is not automatically mounted.</span></span> <span data-ttu-id="567a6-107">Ограничения на использование для этого метода см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="567a6-107">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="567a6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="567a6-108">Syntax</span></span>


```mof
uint32 CompactVirtualHardDisk(
  [in]  string              Path,
  [in]  uint16              Mode,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="567a6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="567a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="567a6-110">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="567a6-110">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567a6-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="567a6-111">Type: **string**</span></span>

<span data-ttu-id="567a6-112">Полный путь, указывающий расположение файла слияния.</span><span class="sxs-lookup"><span data-stu-id="567a6-112">A fully qualified path that specifies the location of the merging file.</span></span>

</dd> <dt>

<span data-ttu-id="567a6-113">*Режим* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="567a6-113">*Mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567a6-114">Тип: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="567a6-114">Type: **uint16**</span></span>

<span data-ttu-id="567a6-115">Задает режим для операции Compact.</span><span class="sxs-lookup"><span data-stu-id="567a6-115">Specifies the mode for the compact operation.</span></span> <span data-ttu-id="567a6-116">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="567a6-116">This must be one of the following values.</span></span>

<dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="567a6-117">**Full** (0)</span><span class="sxs-lookup"><span data-stu-id="567a6-117">**Full** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Quick"></span><span id="quick"></span><span id="QUICK"></span>

<span data-ttu-id="567a6-118">**Быстрый** (1)</span><span class="sxs-lookup"><span data-stu-id="567a6-118">**Quick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Retrim"></span><span id="retrim"></span><span id="RETRIM"></span>

<span data-ttu-id="567a6-119">Повторно **обрезать** (2)</span><span class="sxs-lookup"><span data-stu-id="567a6-119">**Retrim** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Pretrimmed"></span><span id="pretrimmed"></span><span id="PRETRIMMED"></span>

<span data-ttu-id="567a6-120">**Предобрезанные** (3)</span><span class="sxs-lookup"><span data-stu-id="567a6-120">**Pretrimmed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Prezeroed"></span><span id="prezeroed"></span><span id="PREZEROED"></span>

<span data-ttu-id="567a6-121">**До нуля** (4)</span><span class="sxs-lookup"><span data-stu-id="567a6-121">**Prezeroed** (4)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="567a6-122">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="567a6-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="567a6-123">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="567a6-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="567a6-124">Ссылка на задание (может иметь **значение NULL** , если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="567a6-124">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="567a6-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="567a6-125">Return value</span></span>

<span data-ttu-id="567a6-126">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="567a6-126">Type: **uint32**</span></span>

<span data-ttu-id="567a6-127">Этот метод может возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="567a6-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="567a6-128">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="567a6-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-129">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="567a6-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-130">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="567a6-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-131">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="567a6-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-132">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="567a6-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-133">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="567a6-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-134">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="567a6-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-135">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="567a6-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-136">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="567a6-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-137">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="567a6-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-138">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="567a6-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-139">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="567a6-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-140">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="567a6-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="567a6-141">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="567a6-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="567a6-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="567a6-142">Remarks</span></span>

<span data-ttu-id="567a6-143">С этим методом можно использовать только следующие типы виртуальных жестких дисков:</span><span class="sxs-lookup"><span data-stu-id="567a6-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="567a6-144">Фиксированный VHDX</span><span class="sxs-lookup"><span data-stu-id="567a6-144">Fixed VHDX</span></span>
-   <span data-ttu-id="567a6-145">Динамический виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="567a6-145">Dynamic VHD</span></span>
-   <span data-ttu-id="567a6-146">Динамические VHDX</span><span class="sxs-lookup"><span data-stu-id="567a6-146">Dynamic VHDX</span></span>
-   <span data-ttu-id="567a6-147">Разностный виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="567a6-147">Differencing VHD</span></span>
-   <span data-ttu-id="567a6-148">Разностные VHDX</span><span class="sxs-lookup"><span data-stu-id="567a6-148">Differencing VHDX</span></span>

<span data-ttu-id="567a6-149">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="567a6-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="567a6-150">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="567a6-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="567a6-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="567a6-151">Examples</span></span>

<span data-ttu-id="567a6-152">В следующем примере C# сжимается виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="567a6-152">The following C# example compacts a virtual hard disk.</span></span> <span data-ttu-id="567a6-153">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="567a6-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskCompactMode
{
    Full = 0,
    Quick = 1,
    Retrim = 2,
    Pretrimmed = 3,
    Prezeroed = 4
}

public static void CompactVirtualHardDisk(string vhdPath, VirtualHardDiskCompactMode compactMode)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("CompactVirtualHardDisk");
    inParams["Path"] = vhdPath;
    inParams["Mode"] = compactMode;
    ManagementBaseObject outParams = imageService.InvokeMethod("CompactVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was compacted successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to compact {0}", inParams["Path"]);
        }
    }
    else
    {
        Console.WriteLine("Compact {0} returned error {1}", inParams["Path"], outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="567a6-154">Требования</span><span class="sxs-lookup"><span data-stu-id="567a6-154">Requirements</span></span>



| <span data-ttu-id="567a6-155">Требование</span><span class="sxs-lookup"><span data-stu-id="567a6-155">Requirement</span></span> | <span data-ttu-id="567a6-156">Значение</span><span class="sxs-lookup"><span data-stu-id="567a6-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="567a6-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="567a6-157">Minimum supported client</span></span><br/> | <span data-ttu-id="567a6-158">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="567a6-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="567a6-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="567a6-159">Minimum supported server</span></span><br/> | <span data-ttu-id="567a6-160">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="567a6-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="567a6-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="567a6-161">Namespace</span></span><br/>                | <span data-ttu-id="567a6-162">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="567a6-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="567a6-163">MOF</span><span class="sxs-lookup"><span data-stu-id="567a6-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="567a6-164"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="567a6-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="567a6-165">DLL</span><span class="sxs-lookup"><span data-stu-id="567a6-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="567a6-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="567a6-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="567a6-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="567a6-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="567a6-168">[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="567a6-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="567a6-169">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="567a6-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

