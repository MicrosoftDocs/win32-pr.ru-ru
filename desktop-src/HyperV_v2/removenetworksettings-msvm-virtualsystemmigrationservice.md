---
description: Удаляет подсети миграции из службы миграции виртуальной системы.
ms.assetid: 6ae8de07-552b-4525-8806-bfb9da73bd42
title: Метод Ремовенетворксеттингс класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.RemoveNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66b7a9fd1ce29d9dd645242ec7cda346f79a6f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682834"
---
# <a name="removenetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="50794-103">Метод Ремовенетворксеттингс \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="50794-103">RemoveNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="50794-104">Удаляет подсети миграции из службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="50794-104">Removes migration network subnets from the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="50794-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50794-105">Syntax</span></span>


```mof
uint32 RemoveNetworkSettings(
  [in]  Msvm_VirtualSystemMigrationNetworkSettingData REF NetworkSettings[],
  [out] CIM_ConcreteJob                               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="50794-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50794-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50794-107">*Нетворксеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50794-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50794-108">Массив внедренных экземпляров класса [**мсвм \_ виртуалсистеммигратионнетворксеттингдата**](msvm-virtualsystemmigrationnetworksettingdata.md) , представляющих удаляемые сетевые подсети.</span><span class="sxs-lookup"><span data-stu-id="50794-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represent the network subnets to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="50794-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="50794-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50794-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="50794-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50794-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50794-111">Return value</span></span>

<span data-ttu-id="50794-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="50794-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="50794-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="50794-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="50794-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="50794-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="50794-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="50794-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="50794-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="50794-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="50794-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="50794-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="50794-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="50794-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="50794-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="50794-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="50794-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="50794-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="50794-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="50794-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="50794-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="50794-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="50794-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="50794-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="50794-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="50794-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="50794-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="50794-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="50794-126">Требования</span><span class="sxs-lookup"><span data-stu-id="50794-126">Requirements</span></span>



| <span data-ttu-id="50794-127">Требование</span><span class="sxs-lookup"><span data-stu-id="50794-127">Requirement</span></span> | <span data-ttu-id="50794-128">Значение</span><span class="sxs-lookup"><span data-stu-id="50794-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50794-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50794-129">Minimum supported client</span></span><br/> | <span data-ttu-id="50794-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="50794-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="50794-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50794-131">Minimum supported server</span></span><br/> | <span data-ttu-id="50794-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="50794-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50794-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="50794-133">Namespace</span></span><br/>                | <span data-ttu-id="50794-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="50794-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="50794-135">MOF</span><span class="sxs-lookup"><span data-stu-id="50794-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50794-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50794-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50794-137">DLL</span><span class="sxs-lookup"><span data-stu-id="50794-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50794-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50794-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50794-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50794-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50794-140">**адднетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="50794-140">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="50794-141">**модифинетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="50794-141">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="50794-142">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="50794-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

