---
description: Добавляет подсети миграции сети для службы миграции виртуальной системы.
ms.assetid: b0e0f187-beeb-4fdf-a91c-f6c5500f0f6d
title: Метод Адднетворксеттингс класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.AddNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 75d168b1a49d8ac44ab66ba9da13d1e598c647b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663385"
---
# <a name="addnetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="3c79a-103">Метод Адднетворксеттингс \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="3c79a-103">AddNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="3c79a-104">Добавляет подсети миграции сети для службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3c79a-104">Adds migration network subnets for the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c79a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c79a-105">Syntax</span></span>


```mof
uint32 AddNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3c79a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c79a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c79a-107">*Нетворксеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c79a-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c79a-108">Массив внедренных экземпляров класса [**мсвм \_ виртуалсистеммигратионнетворксеттингдата**](msvm-virtualsystemmigrationnetworksettingdata.md) , содержащих параметры сети миграции.</span><span class="sxs-lookup"><span data-stu-id="3c79a-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that contain the migration network settings.</span></span>

</dd> <dt>

<span data-ttu-id="3c79a-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3c79a-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c79a-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c79a-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c79a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c79a-111">Return value</span></span>

<span data-ttu-id="3c79a-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3c79a-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3c79a-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="3c79a-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="3c79a-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="3c79a-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="3c79a-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="3c79a-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="3c79a-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="3c79a-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="3c79a-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="3c79a-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="3c79a-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="3c79a-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="3c79a-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3c79a-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="3c79a-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3c79a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3c79a-126">Requirements</span></span>



| <span data-ttu-id="3c79a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3c79a-127">Requirement</span></span> | <span data-ttu-id="3c79a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3c79a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c79a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c79a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3c79a-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3c79a-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3c79a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c79a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3c79a-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3c79a-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c79a-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3c79a-133">Namespace</span></span><br/>                | <span data-ttu-id="3c79a-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3c79a-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3c79a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="3c79a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c79a-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c79a-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c79a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3c79a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c79a-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c79a-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c79a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c79a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c79a-140">**модифинетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="3c79a-140">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="3c79a-141">**ремовенетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="3c79a-141">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="3c79a-142">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="3c79a-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

