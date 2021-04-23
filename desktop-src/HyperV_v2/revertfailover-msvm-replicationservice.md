---
description: Отменяет текущую отработку отказа для виртуальной машины, удаляя текущий диск отработки отказа.
ms.assetid: 99d3a3d3-49e4-4410-b979-47b62ebc6aa6
title: Метод Ревертфаиловер класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RevertFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: db20abf34fdad2e0eba499fd1b4cc390bf93b754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664679"
---
# <a name="revertfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="f0bb3-103">Метод Ревертфаиловер \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f0bb3-103">RevertFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="f0bb3-104">Отменяет текущую отработку отказа для виртуальной машины, удаляя текущий диск отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="f0bb3-104">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span> <span data-ttu-id="f0bb3-105">После этой операции [**инитиатефаиловер**](initiatefailover-msvm-replicationservice.md) можно вызвать снова.</span><span class="sxs-lookup"><span data-stu-id="f0bb3-105">After this operation, [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) can be called again.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0bb3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0bb3-106">Syntax</span></span>


```mof
uint32 RevertFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f0bb3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0bb3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0bb3-108">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f0bb3-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bb3-109">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой необходимо отменить отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="f0bb3-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to revert the failover.</span></span>

</dd> <dt>

<span data-ttu-id="f0bb3-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f0bb3-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bb3-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0bb3-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0bb3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0bb3-112">Return value</span></span>

<span data-ttu-id="f0bb3-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f0bb3-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f0bb3-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-115">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f0bb3-127">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="f0bb3-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f0bb3-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f0bb3-128">Requirements</span></span>



| <span data-ttu-id="f0bb3-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f0bb3-129">Requirement</span></span> | <span data-ttu-id="f0bb3-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f0bb3-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0bb3-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0bb3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f0bb3-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f0bb3-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f0bb3-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0bb3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f0bb3-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f0bb3-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0bb3-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f0bb3-135">Namespace</span></span><br/>                | <span data-ttu-id="f0bb3-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f0bb3-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0bb3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f0bb3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0bb3-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0bb3-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0bb3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f0bb3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0bb3-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0bb3-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0bb3-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0bb3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bb3-142">**инитиатефаиловер**</span><span class="sxs-lookup"><span data-stu-id="f0bb3-142">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="f0bb3-143">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="f0bb3-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="f0bb3-144">**сетфаиловернетворкадаптерсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f0bb3-144">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

