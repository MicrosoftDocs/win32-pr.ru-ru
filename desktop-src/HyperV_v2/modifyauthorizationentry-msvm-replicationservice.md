---
description: Изменяет запись авторизации для сервера восстановления.
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Метод Модифяусоризатионентри класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17f5ff1a0e4e1cca95dc5f7764d2f8e2bf9d2c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683973"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="f7f87-103">Метод Модифяусоризатионентри \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f7f87-103">ModifyAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="f7f87-104">Изменяет запись авторизации для сервера восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7f87-104">Modifies an authorization entry for a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7f87-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7f87-105">Syntax</span></span>


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f7f87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7f87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7f87-107">*Аусоризатионентри* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7f87-107">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7f87-108">Строковое представление экземпляра класса [**мсвм \_ репликатионаусоризатионсеттингдата**](msvm-replicationauthorizationsettingdata.md) , определяющего изменяемую запись авторизации.</span><span class="sxs-lookup"><span data-stu-id="f7f87-108">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="f7f87-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f7f87-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7f87-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f7f87-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7f87-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7f87-111">Return value</span></span>

<span data-ttu-id="f7f87-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f7f87-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f7f87-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f7f87-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f7f87-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f7f87-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f7f87-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f7f87-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f7f87-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f7f87-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f7f87-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f7f87-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f7f87-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f7f87-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f7f87-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f7f87-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f7f87-126">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="f7f87-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f7f87-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f7f87-127">Requirements</span></span>



| <span data-ttu-id="f7f87-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f7f87-128">Requirement</span></span> | <span data-ttu-id="f7f87-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f7f87-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f87-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7f87-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f7f87-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f7f87-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f7f87-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7f87-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f7f87-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f7f87-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7f87-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7f87-134">Namespace</span></span><br/>                | <span data-ttu-id="f7f87-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f7f87-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f7f87-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f7f87-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7f87-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7f87-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7f87-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f7f87-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7f87-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7f87-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f7f87-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7f87-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f87-141">**аддаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="f7f87-141">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="f7f87-142">**ремовеаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="f7f87-142">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="f7f87-143">**сетаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="f7f87-143">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="f7f87-144">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="f7f87-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

