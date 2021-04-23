---
description: Определяет, является ли файл виртуального жесткого диска допустимым.
ms.assetid: 5F7C99DB-0C81-46D5-A965-B6D87647ABF6
title: Метод Валидатевиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 50c00dc4336e3e85b7db8ffd334de8868054c997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664325"
---
# <a name="validatevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="2fc84-103">Метод Валидатевиртуалхарддиск \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="2fc84-103">ValidateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="2fc84-104">Определяет, является ли файл виртуального жесткого диска допустимым.</span><span class="sxs-lookup"><span data-stu-id="2fc84-104">Determines whether a virtual hard disk file is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc84-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fc84-105">Syntax</span></span>


```mof
uint32 ValidateVirtualHardDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2fc84-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2fc84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc84-107">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fc84-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc84-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="2fc84-108">Type: **string**</span></span>

<span data-ttu-id="2fc84-109">Полный путь, указывающий расположение файла виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="2fc84-109">A fully qualified path that specifies the location of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="2fc84-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2fc84-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc84-111">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="2fc84-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="2fc84-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2fc84-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc84-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2fc84-113">Return value</span></span>

<span data-ttu-id="2fc84-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fc84-114">Type: **uint32**</span></span>

<span data-ttu-id="2fc84-115">Этот метод может возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2fc84-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2fc84-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="2fc84-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="2fc84-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="2fc84-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="2fc84-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="2fc84-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="2fc84-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="2fc84-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="2fc84-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="2fc84-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="2fc84-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="2fc84-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="2fc84-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="2fc84-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="2fc84-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="2fc84-130">**Обнаружен цикл цепочки разностных виртуальных жестких дисков** (32787)</span><span class="sxs-lookup"><span data-stu-id="2fc84-130">**Vhd differencing chain cycle detected** (32787)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2fc84-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2fc84-131">Remarks</span></span>

<span data-ttu-id="2fc84-132">Если виртуальный жесткий диск является разностным диском, открывается вся цепочка виртуальных дисков.</span><span class="sxs-lookup"><span data-stu-id="2fc84-132">If the virtual hard disk is a differencing disk, the entire virtual disk chain is opened.</span></span> <span data-ttu-id="2fc84-133">Если ссылка разорвана в цепочке дисков, возвращается объект задания с соответствующей инициализированной ошибкой, а дочерний и родительский свойства инициализируются в расположение, в котором связь разорвана.</span><span class="sxs-lookup"><span data-stu-id="2fc84-133">If the link is broken in the disk chain, a job object is returned with the appropriate error initialized and the child and parent properties are initialized to the location where the link is broken.</span></span>

<span data-ttu-id="2fc84-134">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="2fc84-134">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2fc84-135">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2fc84-135">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="2fc84-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="2fc84-136">Examples</span></span>

<span data-ttu-id="2fc84-137">В следующем примере кода C# проверяется образ виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="2fc84-137">The following C# example validates a virtual hard disk image.</span></span> <span data-ttu-id="2fc84-138">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="2fc84-138">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void ValidateVirtualHardDisk(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ValidateVirtualHardDisk");
    inParams["Path"] = vhdPath;
    ManagementBaseObject outParams = imageService.InvokeMethod("ValidateVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} is a valid virtual hard disk.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to validate {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="2fc84-139">Требования</span><span class="sxs-lookup"><span data-stu-id="2fc84-139">Requirements</span></span>



| <span data-ttu-id="2fc84-140">Требование</span><span class="sxs-lookup"><span data-stu-id="2fc84-140">Requirement</span></span> | <span data-ttu-id="2fc84-141">Значение</span><span class="sxs-lookup"><span data-stu-id="2fc84-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc84-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2fc84-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2fc84-143">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2fc84-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2fc84-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2fc84-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2fc84-145">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2fc84-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2fc84-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2fc84-146">Namespace</span></span><br/>                | <span data-ttu-id="2fc84-147">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2fc84-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2fc84-148">MOF</span><span class="sxs-lookup"><span data-stu-id="2fc84-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fc84-149"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fc84-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fc84-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2fc84-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fc84-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2fc84-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2fc84-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2fc84-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc84-153">**Валидатевиртуалхарддиск (v1)**</span><span class="sxs-lookup"><span data-stu-id="2fc84-153">**ValidateVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/validatevirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="2fc84-154">[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2fc84-154">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2fc84-155">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="2fc84-155">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

