---
description: Удаляет запись авторизации с сервера восстановления.
ms.assetid: 1647b35d-1c2f-4fb5-84c0-10b357326abf
title: Метод Ремовеаусоризатионентри класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0bb0d24c9cf4936c6e0187e5091b9fac14ee28c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684456"
---
# <a name="removeauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="7740c-103">Метод Ремовеаусоризатионентри \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="7740c-103">RemoveAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="7740c-104">Удаляет запись авторизации с сервера восстановления.</span><span class="sxs-lookup"><span data-stu-id="7740c-104">Removes an authorization entry from a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7740c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7740c-105">Syntax</span></span>


```mof
uint32 RemoveAuthorizationEntry(
  [in]  string              AllowedPrimaryHostSystem,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7740c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7740c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7740c-107">*Алловедпримарихостсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7740c-107">*AllowedPrimaryHostSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7740c-108">Сервер источника, для которого запись авторизации будет удалена с сервера.</span><span class="sxs-lookup"><span data-stu-id="7740c-108">The primary server for which the authorization entry will be removed from the server.</span></span> <span data-ttu-id="7740c-109">Это то же самое, что и свойство **алловедпримарихостсистем** класса [**\_ репликатионаусоризатионсеттингдата мсвм**](msvm-replicationauthorizationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="7740c-109">This is the same as the **AllowedPrimaryHostSystem** property of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7740c-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7740c-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7740c-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7740c-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7740c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7740c-112">Return value</span></span>

<span data-ttu-id="7740c-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7740c-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7740c-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7740c-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-115">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="7740c-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="7740c-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="7740c-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="7740c-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="7740c-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="7740c-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="7740c-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="7740c-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="7740c-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="7740c-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="7740c-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="7740c-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="7740c-127">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="7740c-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7740c-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7740c-128">Remarks</span></span>

<span data-ttu-id="7740c-129">Удаление записи авторизации приведет к отмене репликации для всех виртуальных машин, авторизованных с этой записью.</span><span class="sxs-lookup"><span data-stu-id="7740c-129">Removing an authorization entry will stop replication for any virtual machines that are authorized with the entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="7740c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7740c-130">Requirements</span></span>



| <span data-ttu-id="7740c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7740c-131">Requirement</span></span> | <span data-ttu-id="7740c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7740c-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7740c-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7740c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7740c-134">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7740c-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7740c-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7740c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7740c-136">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7740c-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7740c-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7740c-137">Namespace</span></span><br/>                | <span data-ttu-id="7740c-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7740c-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7740c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7740c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7740c-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7740c-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7740c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7740c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7740c-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7740c-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7740c-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7740c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7740c-144">**аддаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="7740c-144">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="7740c-145">**модифяусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="7740c-145">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="7740c-146">**сетаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="7740c-146">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="7740c-147">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="7740c-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

