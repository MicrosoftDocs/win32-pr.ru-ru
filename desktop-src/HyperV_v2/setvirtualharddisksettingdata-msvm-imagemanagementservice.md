---
description: Обновляет параметры виртуального жесткого диска.
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Метод Сетвиртуалхарддисксеттингдата класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 969e9019d05b49f2f171f2177e1e74f135e212da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349032"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="034c2-103">Метод Сетвиртуалхарддисксеттингдата \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="034c2-103">SetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="034c2-104">Обновляет параметры виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="034c2-104">Updates the settings for a virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="034c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="034c2-105">Syntax</span></span>


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="034c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="034c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="034c2-107">*Виртуалдисксеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="034c2-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="034c2-108">Строковое представление класса [**мсвм \_ виртуалхарддисксеттингдата**](msvm-virtualharddisksettingdata.md) , которое указывает виртуальный жесткий диск для обновления и содержащий новые данные параметра.</span><span class="sxs-lookup"><span data-stu-id="034c2-108">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the virtual hard disk to update and that contains the new setting data.</span></span> <span data-ttu-id="034c2-109">С помощью этого метода можно обновлять только свойства **парентпас**, **фисикалсекторсизе** или **виртуалдискид** .</span><span class="sxs-lookup"><span data-stu-id="034c2-109">Only the **ParentPath**, **PhysicalSectorSize**, or **VirtualDiskId** properties can be updated with this method.</span></span> <span data-ttu-id="034c2-110">Вы не можете обновить эти свойства с помощью одного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="034c2-110">You can't update these properties with one method call.</span></span> <span data-ttu-id="034c2-111">Обновить одно из этих свойств можно только с помощью одного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="034c2-111">You can only update one of these properties with a single method call.</span></span>

</dd> <dt>

<span data-ttu-id="034c2-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="034c2-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="034c2-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="034c2-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="034c2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="034c2-114">Return value</span></span>

<span data-ttu-id="034c2-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="034c2-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="034c2-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="034c2-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="034c2-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="034c2-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="034c2-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="034c2-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="034c2-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="034c2-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="034c2-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="034c2-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="034c2-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="034c2-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="034c2-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="034c2-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="034c2-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="034c2-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="034c2-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="034c2-130">Remarks</span></span>

<span data-ttu-id="034c2-131">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="034c2-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="034c2-132">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="034c2-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="034c2-133">Требования</span><span class="sxs-lookup"><span data-stu-id="034c2-133">Requirements</span></span>



| <span data-ttu-id="034c2-134">Требование</span><span class="sxs-lookup"><span data-stu-id="034c2-134">Requirement</span></span> | <span data-ttu-id="034c2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="034c2-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="034c2-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="034c2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="034c2-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="034c2-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="034c2-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="034c2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="034c2-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="034c2-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="034c2-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="034c2-140">Namespace</span></span><br/>                | <span data-ttu-id="034c2-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="034c2-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="034c2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="034c2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="034c2-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="034c2-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="034c2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="034c2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="034c2-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="034c2-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="034c2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="034c2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="034c2-147">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="034c2-147">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

