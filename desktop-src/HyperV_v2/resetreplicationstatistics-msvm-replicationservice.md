---
description: Сбрасывает статистику репликации для виртуальной машины и действует в отношении первичной репликации виртуальной машины.
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Метод Ресетрепликатионстатистикс класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8407e20cb38c9aecac26ab0bcee99ce0c8a6be2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683429"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="7efc2-103">Метод Ресетрепликатионстатистикс \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="7efc2-103">ResetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="7efc2-104">Сбрасывает статистику репликации для виртуальной машины и действует в отношении первичной репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7efc2-104">Resets the replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="7efc2-105">Начиная с Windows 8.1 мы рекомендуем не использовать **ресетрепликатионстатистикс** для сброса статистики репликации.</span><span class="sxs-lookup"><span data-stu-id="7efc2-105">Starting with Windows 8.1, we recommend not to use **ResetReplicationStatistics** anymore to reset replication statistics.</span></span> <span data-ttu-id="7efc2-106">Вместо этого используйте [**ресетрепликатионстатистиксекс**](resetreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="7efc2-106">Instead, use [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7efc2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7efc2-107">Syntax</span></span>


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7efc2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7efc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7efc2-109">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7efc2-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7efc2-110">Ссылка на экземпляр класса платформы [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину для сброса статистики репликации.</span><span class="sxs-lookup"><span data-stu-id="7efc2-110">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to reset the replication statistics for.</span></span>

</dd> <dt>

<span data-ttu-id="7efc2-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7efc2-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7efc2-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7efc2-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7efc2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7efc2-113">Return value</span></span>

<span data-ttu-id="7efc2-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7efc2-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7efc2-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7efc2-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="7efc2-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="7efc2-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="7efc2-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="7efc2-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="7efc2-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="7efc2-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="7efc2-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="7efc2-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="7efc2-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="7efc2-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="7efc2-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="7efc2-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="7efc2-128">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="7efc2-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7efc2-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7efc2-129">Requirements</span></span>



| <span data-ttu-id="7efc2-130">Требование</span><span class="sxs-lookup"><span data-stu-id="7efc2-130">Requirement</span></span> | <span data-ttu-id="7efc2-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7efc2-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7efc2-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7efc2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7efc2-133">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7efc2-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7efc2-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7efc2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7efc2-135">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7efc2-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7efc2-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7efc2-136">Namespace</span></span><br/>                | <span data-ttu-id="7efc2-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7efc2-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7efc2-138">MOF</span><span class="sxs-lookup"><span data-stu-id="7efc2-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7efc2-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7efc2-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7efc2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7efc2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7efc2-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7efc2-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7efc2-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7efc2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efc2-143">**жетрепликатионстатистикс**</span><span class="sxs-lookup"><span data-stu-id="7efc2-143">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="7efc2-144">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="7efc2-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

