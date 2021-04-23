---
description: Извлекает статистику репликации для виртуальной машины и действует в отношении первичной репликации виртуальной машины.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Метод Жетрепликатионстатистикс класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9dff711830ccdb805c362961671dff28f5bf0b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662456"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="d352a-103">Метод Жетрепликатионстатистикс \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="d352a-103">GetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="d352a-104">Извлекает статистику репликации для виртуальной машины и действует в отношении первичной репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d352a-104">Retrieves replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="d352a-105">Начиная с Windows 8.1 мы рекомендуем не использовать **жетрепликатионстатистикс** для получения статистики репликации.</span><span class="sxs-lookup"><span data-stu-id="d352a-105">Starting with Windows 8.1, we recommend not to use **GetReplicationStatistics** anymore to retrieve replication statistics.</span></span> <span data-ttu-id="d352a-106">Вместо этого используйте [**жетрепликатионстатистиксекс**](getreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="d352a-106">Instead, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d352a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d352a-107">Syntax</span></span>


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d352a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d352a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d352a-109">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d352a-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d352a-110">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой требуется получить статистику репликации.</span><span class="sxs-lookup"><span data-stu-id="d352a-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="d352a-111">*Репликатионстатистикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d352a-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d352a-112">В случае успеха получает встроенный экземпляр класса [**мсвм \_ репликатионстатистикс**](msvm-replicationstatistics.md) , который содержит статистику репликации для запрошенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d352a-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d352a-113">*Репликатионхеалсиссуес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d352a-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d352a-114">В случае успеха получает массив внедренных экземпляров класса [**\_ ошибок мсвм**](msvm-error.md) , которые указывают на все предупреждения или ошибки репликации для запрошенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d352a-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d352a-115">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d352a-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d352a-116">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d352a-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d352a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d352a-117">Return value</span></span>

<span data-ttu-id="d352a-118">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d352a-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d352a-119">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d352a-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-120">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d352a-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-121">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="d352a-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-122">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="d352a-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-123">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="d352a-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-124">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="d352a-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-125">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="d352a-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-126">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="d352a-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-127">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="d352a-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-128">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="d352a-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-129">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="d352a-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-130">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="d352a-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-131">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="d352a-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d352a-132">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="d352a-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d352a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d352a-133">Requirements</span></span>



| <span data-ttu-id="d352a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d352a-134">Requirement</span></span> | <span data-ttu-id="d352a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d352a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d352a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d352a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d352a-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d352a-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d352a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d352a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d352a-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d352a-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d352a-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d352a-140">Namespace</span></span><br/>                | <span data-ttu-id="d352a-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d352a-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d352a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d352a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d352a-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d352a-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d352a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d352a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d352a-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d352a-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d352a-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d352a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d352a-147">**ресетрепликатионстатистикс**</span><span class="sxs-lookup"><span data-stu-id="d352a-147">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d352a-148">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="d352a-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

