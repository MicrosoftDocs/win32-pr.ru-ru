---
description: Извлекает данные настройки, связанные с файлом виртуального жесткого диска.
ms.assetid: b82c018e-8d23-4615-99c1-3b622a8f41da
title: Метод Жетвиртуалхарддисксеттингдата класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cf8f19d3bbdac593dabef0a1ff8e9c9b60027301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990936"
---
# <a name="getvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="7ca66-103">Метод Жетвиртуалхарддисксеттингдата \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="7ca66-103">GetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="7ca66-104">Извлекает данные настройки, связанные с файлом виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7ca66-104">Retrieves the setting data associated with a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca66-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ca66-105">Syntax</span></span>


```mof
uint32 GetVirtualHardDiskSettingData(
  [in]  string              Path,
  [out] string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7ca66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ca66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca66-107">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ca66-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca66-108">Полный путь к файлу образа диска.</span><span class="sxs-lookup"><span data-stu-id="7ca66-108">The fully qualified path of the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="7ca66-109">*SettingData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7ca66-109">*SettingData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca66-110">В случае успеха получает встроенный экземпляр класса [**мсвм \_ виртуалхарддисксеттингдата**](msvm-virtualharddisksettingdata.md) , который содержит данные параметров для виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="7ca66-110">If successful, receives an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that contains the setting data for the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="7ca66-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7ca66-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca66-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7ca66-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca66-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ca66-113">Return value</span></span>

<span data-ttu-id="7ca66-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7ca66-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7ca66-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7ca66-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="7ca66-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="7ca66-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="7ca66-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="7ca66-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="7ca66-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="7ca66-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="7ca66-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="7ca66-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="7ca66-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="7ca66-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="7ca66-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="7ca66-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="7ca66-128">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="7ca66-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7ca66-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ca66-129">Remarks</span></span>

<span data-ttu-id="7ca66-130">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7ca66-130">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7ca66-131">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7ca66-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="7ca66-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="7ca66-132">Examples</span></span>

<span data-ttu-id="7ca66-133">В следующем примере C# показано, как вызвать метод [**жетвиртуалхарддискстате**](getvirtualharddiskstate-msvm-imagemanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7ca66-133">The following C# example shows how to call the [**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md) method.</span></span> <span data-ttu-id="7ca66-134">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="7ca66-134">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void GetVirtualHardDiskSettingData(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskSettingData");

    inParams["Path"] = vhdPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskSettingData", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["SettingData"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="7ca66-135">Требования</span><span class="sxs-lookup"><span data-stu-id="7ca66-135">Requirements</span></span>



| <span data-ttu-id="7ca66-136">Требование</span><span class="sxs-lookup"><span data-stu-id="7ca66-136">Requirement</span></span> | <span data-ttu-id="7ca66-137">Значение</span><span class="sxs-lookup"><span data-stu-id="7ca66-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca66-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ca66-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca66-139">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7ca66-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7ca66-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ca66-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca66-141">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7ca66-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ca66-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7ca66-142">Namespace</span></span><br/>                | <span data-ttu-id="7ca66-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7ca66-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7ca66-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7ca66-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ca66-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ca66-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ca66-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7ca66-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ca66-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ca66-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7ca66-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ca66-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca66-149">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="7ca66-149">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

