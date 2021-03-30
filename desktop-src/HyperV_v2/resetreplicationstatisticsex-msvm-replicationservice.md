---
description: Сбрасывает статистику репликации, связанную с указанным отношением репликации указанной виртуальной машины.
ms.assetid: 6E49A7C0-2F60-444E-964E-420470EE1538
title: 'Метод Msvm_ReplicationService:: Ресетрепликатионстатистиксекс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c1acb234660e71636b4a69a697b11385d65cf1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911003"
---
# <a name="msvm_replicationserviceresetreplicationstatisticsex-method"></a><span data-ttu-id="3ba4f-103">Мсвм \_ репликатионсервице:: ресетрепликатионстатистиксекс, метод</span><span class="sxs-lookup"><span data-stu-id="3ba4f-103">Msvm\_ReplicationService::ResetReplicationStatisticsEx method</span></span>

<span data-ttu-id="3ba4f-104">Сбрасывает статистику репликации, связанную с указанным отношением репликации указанной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3ba4f-104">Resets replication statistics that are associated with the specified replication relationship of the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba4f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ba4f-105">Syntax</span></span>


```C++
uint32 ResetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="3ba4f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ba4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ba4f-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ba4f-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba4f-108">Ссылка на экземпляр [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину с поддержкой реплики.</span><span class="sxs-lookup"><span data-stu-id="3ba4f-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the replica-enabled virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="3ba4f-109">*Репликатионрелатионшип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ba4f-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba4f-110">Строковое представление внедренного экземпляра класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , определяющего отношение репликации, для которого сбрасывается статистика репликации.</span><span class="sxs-lookup"><span data-stu-id="3ba4f-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to reset the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="3ba4f-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ba4f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba4f-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ba4f-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="3ba4f-113">Если задача завершена, ссылка может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="3ba4f-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ba4f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ba4f-114">Return value</span></span>

<span data-ttu-id="3ba4f-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3ba4f-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3ba4f-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3ba4f-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="3ba4f-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3ba4f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3ba4f-130">Requirements</span></span>



| <span data-ttu-id="3ba4f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3ba4f-131">Requirement</span></span> | <span data-ttu-id="3ba4f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3ba4f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba4f-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ba4f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba4f-134">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3ba4f-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3ba4f-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ba4f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba4f-136">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ba4f-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3ba4f-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3ba4f-137">Namespace</span></span><br/>                | <span data-ttu-id="3ba4f-138">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3ba4f-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="3ba4f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3ba4f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ba4f-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ba4f-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ba4f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3ba4f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ba4f-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ba4f-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ba4f-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ba4f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba4f-144">**жетрепликатионстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="3ba4f-144">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="3ba4f-145">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="3ba4f-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

