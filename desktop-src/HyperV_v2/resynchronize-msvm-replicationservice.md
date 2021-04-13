---
description: Выполняет операцию повторной синхронизации на указанной виртуальной машине.
ms.assetid: a3d06780-f43b-45c4-a186-a3544f9c7963
title: Повторная синхронизация метода класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.Resynchronize
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dcd4865d110843de27f0a242b31253310439e1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346355"
---
# <a name="resynchronize-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="4780f-103">Метод resynchronize \_ класса мсвм репликатионсервице</span><span class="sxs-lookup"><span data-stu-id="4780f-103">Resynchronize method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="4780f-104">Выполняет операцию повторной синхронизации на указанной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4780f-104">Performs a resynchronization operation on the specified virtual machine.</span></span> <span data-ttu-id="4780f-105">Когда клиент вызывает этот метод для реплики виртуальной машины, он повторно синхронизируется с расширенной репликой.</span><span class="sxs-lookup"><span data-stu-id="4780f-105">When a client calls this method for a replica virtual machine, it resynchronizes with extended replica.</span></span>

<span data-ttu-id="4780f-106">Этот метод сравнивает диски с включенной репликацией на основной виртуальной машине и виртуальными машинами восстановления, а также устраняет все проблемы целостности данных репликации за счет репликации различных блоков из основной реплики в восстановление.</span><span class="sxs-lookup"><span data-stu-id="4780f-106">This methods compares the replication enabled disks on the primary and recovery virtual machines, and fixes any replication data integrity issues by replicating the different blocks from the primary to the recovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="4780f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4780f-107">Syntax</span></span>


```mof
uint32 Resynchronize(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4780f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4780f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4780f-109">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4780f-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4780f-110">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину для повторной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4780f-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to be resynchronized.</span></span>

</dd> <dt>

<span data-ttu-id="4780f-111">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4780f-111">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4780f-112">Запланированное время начала операции повторной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4780f-112">The scheduled start time for the resynchronization operation to begin.</span></span> <span data-ttu-id="4780f-113">Если этот параметр имеет **значение NULL**, операция повторной синхронизации начнется немедленно.</span><span class="sxs-lookup"><span data-stu-id="4780f-113">If this parameter is **Null**, the resynchronization operation starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="4780f-114">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4780f-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4780f-115">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4780f-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4780f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4780f-116">Return value</span></span>

<span data-ttu-id="4780f-117">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4780f-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4780f-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="4780f-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="4780f-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="4780f-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="4780f-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="4780f-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="4780f-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="4780f-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="4780f-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="4780f-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="4780f-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="4780f-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="4780f-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="4780f-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4780f-131">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="4780f-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4780f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="4780f-132">Requirements</span></span>



| <span data-ttu-id="4780f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="4780f-133">Requirement</span></span> | <span data-ttu-id="4780f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4780f-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4780f-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4780f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4780f-136">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4780f-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4780f-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4780f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4780f-138">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4780f-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4780f-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4780f-139">Namespace</span></span><br/>                | <span data-ttu-id="4780f-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4780f-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4780f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4780f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4780f-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4780f-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4780f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4780f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4780f-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4780f-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4780f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4780f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4780f-146">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="4780f-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

