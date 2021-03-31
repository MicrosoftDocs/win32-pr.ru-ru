---
description: Изменяет сетевые подсети миграции для службы миграции виртуальной системы.
ms.assetid: 54ea230a-cda9-4fff-8f79-88f2922b2b15
title: Метод Модифинетворксеттингс класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b57cd3ee594bda704c1bd3b6c344c90eb6a1f7fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999032"
---
# <a name="modifynetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="06cc5-103">Метод Модифинетворксеттингс \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="06cc5-103">ModifyNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="06cc5-104">Изменяет сетевые подсети миграции для службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="06cc5-104">Modifies migration network subnets of the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="06cc5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06cc5-105">Syntax</span></span>


```mof
uint32 ModifyNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="06cc5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06cc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06cc5-107">*Нетворксеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06cc5-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cc5-108">Массив внедренных экземпляров класса [**мсвм \_ виртуалсистеммигратионнетворксеттингдата**](msvm-virtualsystemmigrationnetworksettingdata.md) , содержащих параметры сети миграции.</span><span class="sxs-lookup"><span data-stu-id="06cc5-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that contain the migration network settings.</span></span>

</dd> <dt>

<span data-ttu-id="06cc5-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="06cc5-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06cc5-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="06cc5-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06cc5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06cc5-111">Return value</span></span>

<span data-ttu-id="06cc5-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="06cc5-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="06cc5-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="06cc5-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="06cc5-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="06cc5-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="06cc5-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="06cc5-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="06cc5-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="06cc5-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="06cc5-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="06cc5-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="06cc5-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="06cc5-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="06cc5-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="06cc5-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="06cc5-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="06cc5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="06cc5-126">Requirements</span></span>



| <span data-ttu-id="06cc5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="06cc5-127">Requirement</span></span> | <span data-ttu-id="06cc5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="06cc5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06cc5-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06cc5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="06cc5-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="06cc5-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="06cc5-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06cc5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="06cc5-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="06cc5-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06cc5-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="06cc5-133">Namespace</span></span><br/>                | <span data-ttu-id="06cc5-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="06cc5-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="06cc5-135">MOF</span><span class="sxs-lookup"><span data-stu-id="06cc5-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06cc5-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06cc5-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06cc5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="06cc5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06cc5-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06cc5-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06cc5-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06cc5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06cc5-140">**адднетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="06cc5-140">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="06cc5-141">**ремовенетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="06cc5-141">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="06cc5-142">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="06cc5-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

