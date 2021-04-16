---
description: Слияние дочернего виртуального жесткого диска в цепочке разностного с одним или несколькими родительскими виртуальными жесткими дисками в цепочке.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Метод Мержевиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 347e11d55357a8b3366aeb09badc53c1afad9e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546242"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="37944-103">Метод Мержевиртуалхарддиск \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="37944-103">MergeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="37944-104">Слияние дочернего виртуального жесткого диска в цепочке разностного с одним или несколькими родительскими виртуальными жесткими дисками в цепочке.</span><span class="sxs-lookup"><span data-stu-id="37944-104">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span> <span data-ttu-id="37944-105">Ограничения на использование для этого метода см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="37944-105">See Remarks for usage restrictions for this method.</span></span>

<span data-ttu-id="37944-106">Если пользователь, выполняющий эту функцию, не имеет разрешения на обновление виртуальных машин, то эта функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="37944-106">If the user executing this function does not have permission to update the virtual machines, then this function will fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="37944-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37944-107">Syntax</span></span>


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="37944-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="37944-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37944-109">*Источник* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37944-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37944-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="37944-110">Type: **string**</span></span>

<span data-ttu-id="37944-111">Полный путь, указывающий расположение файла виртуального жесткого диска для слияния.</span><span class="sxs-lookup"><span data-stu-id="37944-111">A fully qualified path that specifies the location of the virtual hard disk file to merge.</span></span>

</dd> <dt>

<span data-ttu-id="37944-112">*DestinationPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37944-112">*DestinationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37944-113">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="37944-113">Type: **string**</span></span>

<span data-ttu-id="37944-114">Полный путь, указывающий расположение файла родительского виртуального жесткого диска, в который должны быть объединены данные.</span><span class="sxs-lookup"><span data-stu-id="37944-114">A fully qualified path that specifies the location of the parent virtual hard disk file into which data is to be merged.</span></span> <span data-ttu-id="37944-115">Это может быть непосредственный родительский виртуальный жесткий диск файла слияния или образа родительского диска, а несколько уровней разностной цепочки.</span><span class="sxs-lookup"><span data-stu-id="37944-115">This could be the immediate parent virtual hard disk of the merging file or the parent disk image a few levels up the differencing chain.</span></span>

</dd> <dt>

<span data-ttu-id="37944-116">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="37944-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37944-117">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="37944-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="37944-118">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="37944-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37944-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37944-119">Return value</span></span>

<span data-ttu-id="37944-120">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37944-120">Type: **uint32**</span></span>

<span data-ttu-id="37944-121">Этот метод может возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="37944-121">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="37944-122">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="37944-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37944-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="37944-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="37944-124">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="37944-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="37944-125">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="37944-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="37944-126">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="37944-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="37944-127">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="37944-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="37944-128">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="37944-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="37944-129">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="37944-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="37944-130">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="37944-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="37944-131">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="37944-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="37944-132">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="37944-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="37944-133">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="37944-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="37944-134">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="37944-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="37944-135">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="37944-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="37944-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37944-136">Remarks</span></span>

<span data-ttu-id="37944-137">Дочерний виртуальный жесткий диск должен быть вне сети.</span><span class="sxs-lookup"><span data-stu-id="37944-137">The child virtual hard disk must be offline.</span></span>

<span data-ttu-id="37944-138">С этим методом можно использовать только следующие типы виртуальных жестких дисков:</span><span class="sxs-lookup"><span data-stu-id="37944-138">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="37944-139">Разностный виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="37944-139">Differencing VHD</span></span>
-   <span data-ttu-id="37944-140">Разностные VHDX</span><span class="sxs-lookup"><span data-stu-id="37944-140">Differencing VHDX</span></span>

<span data-ttu-id="37944-141">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="37944-141">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="37944-142">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="37944-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="37944-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="37944-143">Examples</span></span>

<span data-ttu-id="37944-144">В следующем примере кода C# разворачивается файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="37944-144">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="37944-145">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="37944-145">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="37944-146">Требования</span><span class="sxs-lookup"><span data-stu-id="37944-146">Requirements</span></span>



| <span data-ttu-id="37944-147">Требование</span><span class="sxs-lookup"><span data-stu-id="37944-147">Requirement</span></span> | <span data-ttu-id="37944-148">Значение</span><span class="sxs-lookup"><span data-stu-id="37944-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37944-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37944-149">Minimum supported client</span></span><br/> | <span data-ttu-id="37944-150">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="37944-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="37944-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37944-151">Minimum supported server</span></span><br/> | <span data-ttu-id="37944-152">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="37944-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37944-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="37944-153">Namespace</span></span><br/>                | <span data-ttu-id="37944-154">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="37944-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="37944-155">MOF</span><span class="sxs-lookup"><span data-stu-id="37944-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37944-156"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37944-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37944-157">DLL</span><span class="sxs-lookup"><span data-stu-id="37944-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37944-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37944-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37944-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37944-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="37944-160">[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="37944-160">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="37944-161">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="37944-161">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

