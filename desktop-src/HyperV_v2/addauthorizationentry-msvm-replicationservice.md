---
description: Добавляет запись авторизации на сервер восстановления.
ms.assetid: edc11c5b-b1a1-45e0-a920-2f1f1b0b8779
title: Метод Аддаусоризатионентри класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.AddAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fd4c47bd4468d5804ec7e096d35db271726c92b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683439"
---
# <a name="addauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="d6144-103">Метод Аддаусоризатионентри \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="d6144-103">AddAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="d6144-104">Добавляет запись авторизации на сервер восстановления.</span><span class="sxs-lookup"><span data-stu-id="d6144-104">Adds an authorization entry to a recovery server.</span></span> <span data-ttu-id="d6144-105">Эти записи используются для авторизации подключений к серверу восстановления.</span><span class="sxs-lookup"><span data-stu-id="d6144-105">These entries are used for authorizing connections to the recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6144-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6144-106">Syntax</span></span>


```mof
uint32 AddAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d6144-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6144-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6144-108">*Аусоризатионентри* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6144-108">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6144-109">Строковое представление экземпляра класса [**мсвм \_ репликатионаусоризатионсеттингдата**](msvm-replicationauthorizationsettingdata.md) , определяющего добавляемую запись авторизации.</span><span class="sxs-lookup"><span data-stu-id="d6144-109">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be added.</span></span>

</dd> <dt>

<span data-ttu-id="d6144-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d6144-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6144-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d6144-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6144-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6144-112">Return value</span></span>

<span data-ttu-id="d6144-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d6144-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d6144-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d6144-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-115">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d6144-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="d6144-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="d6144-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="d6144-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="d6144-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="d6144-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="d6144-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="d6144-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="d6144-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="d6144-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="d6144-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="d6144-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d6144-127">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="d6144-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d6144-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d6144-128">Requirements</span></span>



| <span data-ttu-id="d6144-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d6144-129">Requirement</span></span> | <span data-ttu-id="d6144-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d6144-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6144-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6144-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d6144-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d6144-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d6144-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6144-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d6144-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d6144-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6144-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d6144-135">Namespace</span></span><br/>                | <span data-ttu-id="d6144-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d6144-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d6144-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d6144-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6144-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6144-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6144-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d6144-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6144-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d6144-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d6144-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6144-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6144-142">**модифяусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="d6144-142">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d6144-143">**ремовеаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="d6144-143">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d6144-144">**сетаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="d6144-144">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d6144-145">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="d6144-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

