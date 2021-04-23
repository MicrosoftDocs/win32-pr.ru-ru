---
description: Удаляет отношение репликации виртуальной машины и действует в отношении первичной репликации виртуальной машины.
ms.assetid: a9a20aa1-378d-4a2a-9ebc-9786ab2dfda7
title: Метод Ремоверепликатионрелатионшип класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb897ff72cd927390362f076114fc8757baa6c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897698"
---
# <a name="removereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="3a152-103">Метод Ремоверепликатионрелатионшип \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="3a152-103">RemoveReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="3a152-104">Удаляет отношение репликации виртуальной машины и действует в отношении первичной репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3a152-104">Removes a virtual machine replication relationship and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="3a152-105">Начиная с Windows 8.1 мы рекомендуем не использовать **ремоверепликатионрелатионшип** для удаления отношения репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3a152-105">Starting with Windows 8.1, we recommend not to use **RemoveReplicationRelationship** anymore to remove a virtual machine replication relationship.</span></span> <span data-ttu-id="3a152-106">Вместо этого используйте [**ремоверепликатионрелатионшипекс**](removereplicationrelationshipex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="3a152-106">Instead, use [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3a152-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a152-107">Syntax</span></span>


```mof
uint32 RemoveReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3a152-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a152-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a152-109">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a152-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a152-110">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой должно быть удалено отношение репликации.</span><span class="sxs-lookup"><span data-stu-id="3a152-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication relationship should be removed.</span></span>

</dd> <dt>

<span data-ttu-id="3a152-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3a152-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a152-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a152-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a152-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a152-113">Return value</span></span>

<span data-ttu-id="3a152-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3a152-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3a152-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="3a152-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="3a152-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="3a152-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="3a152-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="3a152-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="3a152-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="3a152-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="3a152-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="3a152-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="3a152-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="3a152-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="3a152-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="3a152-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3a152-128">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="3a152-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3a152-129">Требования</span><span class="sxs-lookup"><span data-stu-id="3a152-129">Requirements</span></span>



| <span data-ttu-id="3a152-130">Требование</span><span class="sxs-lookup"><span data-stu-id="3a152-130">Requirement</span></span> | <span data-ttu-id="3a152-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3a152-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a152-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a152-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3a152-133">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3a152-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a152-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a152-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3a152-135">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3a152-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a152-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a152-136">Namespace</span></span><br/>                | <span data-ttu-id="3a152-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3a152-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a152-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3a152-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a152-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a152-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a152-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3a152-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a152-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a152-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a152-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a152-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a152-143">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="3a152-143">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="3a152-144">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="3a152-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

