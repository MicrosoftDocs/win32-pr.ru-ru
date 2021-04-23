---
description: Подключает файл виртуального жесткого диска в режиме замыкания на себя.
ms.assetid: 54bd8e67-e309-4bf3-94bd-e29bc3300a3d
title: Метод Аттачвиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.AttachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f8a22ac377eb96fdc01fa54877cdc6c12619c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909839"
---
# <a name="attachvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="184c1-103">Метод Аттачвиртуалхарддиск \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="184c1-103">AttachVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="184c1-104">Подключает файл виртуального жесткого диска в режиме замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="184c1-104">Attaches a virtual hard disk file in loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="184c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="184c1-105">Syntax</span></span>


```mof
uint32 AttachVirtualHardDisk(
  [in]  string              Path,
  [in]  boolean             AssignDriveLetter,
  [in]  boolean             ReadOnly,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="184c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="184c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="184c1-107">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="184c1-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184c1-108">Полный путь, указывающий расположение файла виртуального жесткого диска для присоединения.</span><span class="sxs-lookup"><span data-stu-id="184c1-108">A fully qualified path that specifies the location of the virtual hard disk file to attach.</span></span>

</dd> <dt>

<span data-ttu-id="184c1-109">*Ассигндривелеттер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="184c1-109">*AssignDriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184c1-110">Указывает, назначены ли томам диска буквы дисков.</span><span class="sxs-lookup"><span data-stu-id="184c1-110">Indicates if drive letters are assigned to the disk's volumes.</span></span>

</dd> <dt>

<span data-ttu-id="184c1-111">*Только для чтения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="184c1-111">*ReadOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184c1-112">Указывает, должен ли подключенный жесткий диск быть доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="184c1-112">Indicates if the attached hard disk should be read-only.</span></span>

</dd> <dt>

<span data-ttu-id="184c1-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="184c1-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="184c1-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="184c1-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="184c1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="184c1-115">Return value</span></span>

<span data-ttu-id="184c1-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="184c1-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="184c1-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="184c1-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="184c1-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="184c1-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="184c1-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="184c1-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="184c1-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="184c1-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="184c1-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="184c1-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="184c1-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="184c1-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="184c1-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="184c1-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="184c1-130">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="184c1-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="184c1-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="184c1-131">Remarks</span></span>

<span data-ttu-id="184c1-132">Чтобы отсоединить виртуальный жесткий диск, используйте метод [**мсвм \_ Маунтедсторажеимаже. детачвиртуалхарддиск**](detachvirtualharddisk-msvm-mountedstorageimage.md) .</span><span class="sxs-lookup"><span data-stu-id="184c1-132">To detach the virtual hard disk, use the [**Msvm\_MountedStorageImage.DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) method.</span></span>

<span data-ttu-id="184c1-133">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="184c1-133">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="184c1-134">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="184c1-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="184c1-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="184c1-135">Examples</span></span>

<span data-ttu-id="184c1-136">В следующем примере C# показано, как подключить файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="184c1-136">The following C# example shows how to attach a virtual hard disk file.</span></span> <span data-ttu-id="184c1-137">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="184c1-137">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void AttachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("AttachVirtualHardDisk");
    inParams["Path"] = path;
    inParams["AssignDriveLetter"] = true;
    inParams["ReadOnly"] = false;
    ManagementBaseObject outParams = imageService.InvokeMethod("AttachVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was attached successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to attach {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="184c1-138">Требования</span><span class="sxs-lookup"><span data-stu-id="184c1-138">Requirements</span></span>



| <span data-ttu-id="184c1-139">Требование</span><span class="sxs-lookup"><span data-stu-id="184c1-139">Requirement</span></span> | <span data-ttu-id="184c1-140">Значение</span><span class="sxs-lookup"><span data-stu-id="184c1-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="184c1-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="184c1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="184c1-142">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="184c1-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="184c1-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="184c1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="184c1-144">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="184c1-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="184c1-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="184c1-145">Namespace</span></span><br/>                | <span data-ttu-id="184c1-146">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="184c1-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="184c1-147">MOF</span><span class="sxs-lookup"><span data-stu-id="184c1-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="184c1-148"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="184c1-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="184c1-149">DLL</span><span class="sxs-lookup"><span data-stu-id="184c1-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="184c1-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="184c1-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="184c1-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="184c1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184c1-152">**Мсвм \_ маунтедсторажеимаже. детачвиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="184c1-152">**Msvm\_MountedStorageImage.DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md)
</dt> <dt>

[<span data-ttu-id="184c1-153">**Подключение (v1)**</span><span class="sxs-lookup"><span data-stu-id="184c1-153">**Mount (V1)**</span></span>](/previous-versions/windows/desktop/virtual/mount-msvm-imagemanagementservice)
</dt> <dt>

[<span data-ttu-id="184c1-154">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="184c1-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

