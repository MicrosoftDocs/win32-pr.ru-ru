---
description: Изменяет отношение расширенной репликации на основное отношение для реплики виртуальной машины. Виртуальная машина реплики должна находиться в состоянии фиксации отработки отказа.
ms.assetid: B593A155-B5E6-44E5-8835-09DEB1FF868E
title: 'Метод Msvm_ReplicationService:: Чанжерепликатионмодетопримари'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ChangeReplicationModeToPrimary
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a18b3c9f1003ff7b263f5c6b7cc89abedccfd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662247"
---
# <a name="msvm_replicationservicechangereplicationmodetoprimary-method"></a><span data-ttu-id="3cce8-104">Мсвм \_ репликатионсервице:: чанжерепликатионмодетопримари, метод</span><span class="sxs-lookup"><span data-stu-id="3cce8-104">Msvm\_ReplicationService::ChangeReplicationModeToPrimary method</span></span>

<span data-ttu-id="3cce8-105">Изменяет отношение расширенной репликации на основное отношение для реплики виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3cce8-105">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="3cce8-106">Виртуальная машина реплики должна находиться в состоянии фиксации отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="3cce8-106">The replica virtual machine must be in a failover committed state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cce8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cce8-107">Syntax</span></span>


```C++
uint32 ChangeReplicationModeToPrimary(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="3cce8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cce8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cce8-109">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3cce8-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cce8-110">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой этот метод изменяет отношение расширенной репликации к первичной связи.</span><span class="sxs-lookup"><span data-stu-id="3cce8-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which this method changes the extended replication relationship to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="3cce8-111">*Репликатионрелатионшип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3cce8-111">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cce8-112">Строковое представление внедренного экземпляра класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , определяющего отношение расширенной репликации, которое этот метод изменяет в основную связь.</span><span class="sxs-lookup"><span data-stu-id="3cce8-112">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the extended replication relationship that this method changes to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="3cce8-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3cce8-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cce8-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3cce8-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="3cce8-115">Если задача завершена, ссылка может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="3cce8-115">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cce8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cce8-116">Return value</span></span>

<span data-ttu-id="3cce8-117">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3cce8-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3cce8-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="3cce8-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="3cce8-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="3cce8-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="3cce8-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="3cce8-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="3cce8-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="3cce8-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="3cce8-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="3cce8-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="3cce8-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="3cce8-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="3cce8-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="3cce8-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3cce8-131">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="3cce8-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3cce8-132">Требования</span><span class="sxs-lookup"><span data-stu-id="3cce8-132">Requirements</span></span>



| <span data-ttu-id="3cce8-133">Требование</span><span class="sxs-lookup"><span data-stu-id="3cce8-133">Requirement</span></span> | <span data-ttu-id="3cce8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3cce8-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cce8-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cce8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3cce8-136">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3cce8-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3cce8-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cce8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3cce8-138">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3cce8-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3cce8-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3cce8-139">Namespace</span></span><br/>                | <span data-ttu-id="3cce8-140">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3cce8-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="3cce8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3cce8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cce8-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cce8-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cce8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3cce8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cce8-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3cce8-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3cce8-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cce8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cce8-146">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="3cce8-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

