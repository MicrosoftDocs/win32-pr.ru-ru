---
description: Задает запись авторизации репликации для виртуальной машины.
ms.assetid: 39b6b0c4-5515-4863-9038-4c37421abe65
title: Метод Сетаусоризатионентри класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 03b2c2c37a38e957a1b560e2314845abf204ee01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683374"
---
# <a name="setauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="961cb-103">Метод Сетаусоризатионентри \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="961cb-103">SetAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="961cb-104">Задает запись авторизации репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="961cb-104">Sets the replication authorization entry for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="961cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="961cb-105">Syntax</span></span>


```mof
uint32 SetAuthorizationEntry(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 AuthorizationEntry,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="961cb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="961cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="961cb-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="961cb-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="961cb-108">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой необходимо задать запись авторизации.</span><span class="sxs-lookup"><span data-stu-id="961cb-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to set the authorization entry for.</span></span>

</dd> <dt>

<span data-ttu-id="961cb-109">*Аусоризатионентри* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="961cb-109">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="961cb-110">Строковое представление экземпляра класса [**мсвм \_ репликатионаусоризатионсеттингдата**](msvm-replicationauthorizationsettingdata.md) , определяющего запись авторизации, которая будет использоваться для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="961cb-110">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be used for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="961cb-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="961cb-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="961cb-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="961cb-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="961cb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="961cb-113">Return value</span></span>

<span data-ttu-id="961cb-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="961cb-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="961cb-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="961cb-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="961cb-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="961cb-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="961cb-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="961cb-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="961cb-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="961cb-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="961cb-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="961cb-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="961cb-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="961cb-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="961cb-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="961cb-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="961cb-128">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="961cb-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="961cb-129">Требования</span><span class="sxs-lookup"><span data-stu-id="961cb-129">Requirements</span></span>



| <span data-ttu-id="961cb-130">Требование</span><span class="sxs-lookup"><span data-stu-id="961cb-130">Requirement</span></span> | <span data-ttu-id="961cb-131">Значение</span><span class="sxs-lookup"><span data-stu-id="961cb-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="961cb-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="961cb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="961cb-133">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="961cb-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="961cb-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="961cb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="961cb-135">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="961cb-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="961cb-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="961cb-136">Namespace</span></span><br/>                | <span data-ttu-id="961cb-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="961cb-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="961cb-138">MOF</span><span class="sxs-lookup"><span data-stu-id="961cb-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="961cb-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="961cb-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="961cb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="961cb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="961cb-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="961cb-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="961cb-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="961cb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="961cb-143">**аддаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="961cb-143">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="961cb-144">**модифяусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="961cb-144">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="961cb-145">**ремовеаусоризатионентри**</span><span class="sxs-lookup"><span data-stu-id="961cb-145">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="961cb-146">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="961cb-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

