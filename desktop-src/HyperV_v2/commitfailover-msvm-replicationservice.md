---
description: Фиксирует моментальный снимок восстановления, который метод Инитиатефаиловер использовал для отработки отказа.
ms.assetid: 05c27211-adc7-400a-83e2-81792ae7577f
title: Метод Коммитфаиловер класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CommitFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 04687ea29f39645c2407de44faf6bba6ecc75832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683614"
---
# <a name="commitfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="d3c89-103">Метод Коммитфаиловер \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="d3c89-103">CommitFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="d3c89-104">Фиксирует моментальный снимок восстановления, который метод [**инитиатефаиловер**](initiatefailover-msvm-replicationservice.md) использовал для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="d3c89-104">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span>

<span data-ttu-id="d3c89-105">Этот метод выполняет сведение точек восстановления на виртуальной машине восстановления, применяя моментальный снимок восстановления.</span><span class="sxs-lookup"><span data-stu-id="d3c89-105">This method flattens the recovery points on the recovery virtual machine by applying the recovery snapshot.</span></span> <span data-ttu-id="d3c89-106">После этого отменить операцию отработки отказа невозможно.</span><span class="sxs-lookup"><span data-stu-id="d3c89-106">After this is done, the failover operation cannot be canceled.</span></span> <span data-ttu-id="d3c89-107">Пользователи обычно будут выполнять эту команду, когда точка репликации, используемая для отработки отказа, является удовлетворительной, а виртуальная машина восстановления может изменить роль на первичную.</span><span class="sxs-lookup"><span data-stu-id="d3c89-107">Users will typically perform this when the replication point used for failover is satisfactory and the recovery virtual machine can change role to be primary.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c89-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3c89-108">Syntax</span></span>


```mof
uint32 CommitFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d3c89-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3c89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c89-110">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3c89-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c89-111">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой зафиксирована отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="d3c89-111">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to commit the failover.</span></span>

</dd> <dt>

<span data-ttu-id="d3c89-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d3c89-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c89-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3c89-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c89-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3c89-114">Return value</span></span>

<span data-ttu-id="d3c89-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d3c89-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d3c89-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d3c89-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d3c89-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="d3c89-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="d3c89-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="d3c89-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="d3c89-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="d3c89-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="d3c89-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="d3c89-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="d3c89-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="d3c89-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="d3c89-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="d3c89-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d3c89-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="d3c89-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d3c89-130">Требования</span><span class="sxs-lookup"><span data-stu-id="d3c89-130">Requirements</span></span>



| <span data-ttu-id="d3c89-131">Требование</span><span class="sxs-lookup"><span data-stu-id="d3c89-131">Requirement</span></span> | <span data-ttu-id="d3c89-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d3c89-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c89-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3c89-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c89-134">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d3c89-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d3c89-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3c89-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c89-136">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d3c89-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3c89-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d3c89-137">Namespace</span></span><br/>                | <span data-ttu-id="d3c89-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d3c89-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d3c89-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d3c89-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3c89-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3c89-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3c89-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c89-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c89-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3c89-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3c89-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3c89-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c89-144">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="d3c89-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

