---
description: Изменяет данные настройки для службы миграции.
ms.assetid: 5162fe88-dd39-4fe0-b8e9-e9b70c2b6a5c
title: Метод Модифисервицесеттингс класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e1e9dc96196752ec4408939adc418e7c43bc0c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663984"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="13019-103">Метод Модифисервицесеттингс \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="13019-103">ModifyServiceSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="13019-104">Изменяет данные настройки для службы миграции.</span><span class="sxs-lookup"><span data-stu-id="13019-104">Modifies the setting data for the migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="13019-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13019-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="13019-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="13019-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13019-107">*Сервицесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13019-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13019-108">Встроенный экземпляр класса [**мсвм \_ виртуалсистемманажементсервицесеттингдата**](msvm-virtualsystemmanagementservicesettingdata.md) , который содержит новые параметры службы.</span><span class="sxs-lookup"><span data-stu-id="13019-108">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the new service settings.</span></span>

</dd> <dt>

<span data-ttu-id="13019-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="13019-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13019-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13019-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13019-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13019-111">Return value</span></span>

<span data-ttu-id="13019-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="13019-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="13019-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="13019-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13019-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="13019-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="13019-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="13019-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="13019-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="13019-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="13019-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="13019-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="13019-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="13019-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="13019-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="13019-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="13019-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="13019-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="13019-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="13019-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="13019-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="13019-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="13019-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="13019-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="13019-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="13019-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="13019-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="13019-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="13019-126">Требования</span><span class="sxs-lookup"><span data-stu-id="13019-126">Requirements</span></span>



| <span data-ttu-id="13019-127">Требование</span><span class="sxs-lookup"><span data-stu-id="13019-127">Requirement</span></span> | <span data-ttu-id="13019-128">Значение</span><span class="sxs-lookup"><span data-stu-id="13019-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13019-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13019-129">Minimum supported client</span></span><br/> | <span data-ttu-id="13019-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="13019-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="13019-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13019-131">Minimum supported server</span></span><br/> | <span data-ttu-id="13019-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="13019-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13019-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="13019-133">Namespace</span></span><br/>                | <span data-ttu-id="13019-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="13019-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="13019-135">MOF</span><span class="sxs-lookup"><span data-stu-id="13019-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13019-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13019-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13019-137">DLL</span><span class="sxs-lookup"><span data-stu-id="13019-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13019-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13019-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13019-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13019-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13019-140">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="13019-140">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

