---
description: Извлекает статистику репликации, связанную с указанным отношением репликации виртуальной машины.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: 'Метод Msvm_ReplicationService:: Жетрепликатионстатистиксекс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682792"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a><span data-ttu-id="75b19-103">Мсвм \_ репликатионсервице:: жетрепликатионстатистиксекс, метод</span><span class="sxs-lookup"><span data-stu-id="75b19-103">Msvm\_ReplicationService::GetReplicationStatisticsEx method</span></span>

<span data-ttu-id="75b19-104">Извлекает статистику репликации, связанную с указанным отношением репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="75b19-104">Retrieves the replication statistics that are associated with the specified replication relationship of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b19-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75b19-105">Syntax</span></span>


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="75b19-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75b19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b19-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75b19-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b19-108">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой требуется получить статистику репликации.</span><span class="sxs-lookup"><span data-stu-id="75b19-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="75b19-109">*Репликатионрелатионшип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75b19-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b19-110">Строковое представление внедренного экземпляра класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , определяющего отношение репликации, для которого требуется получить статистику репликации.</span><span class="sxs-lookup"><span data-stu-id="75b19-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="75b19-111">*Репликатионстатистикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75b19-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75b19-112">В случае успеха получает встроенный экземпляр класса [**мсвм \_ репликатионстатистикс**](msvm-replicationstatistics.md) , который содержит статистику репликации для запрошенной связи репликации.</span><span class="sxs-lookup"><span data-stu-id="75b19-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="75b19-113">*Репликатионхеалсиссуес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75b19-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75b19-114">В случае успеха получает массив внедренных экземпляров класса [**\_ ошибок мсвм**](msvm-error.md) , которые указывают на все предупреждения или ошибки репликации для запрошенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="75b19-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="75b19-115">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75b19-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75b19-116">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="75b19-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="75b19-117">Если задача завершена, ссылка может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="75b19-117">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b19-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75b19-118">Return value</span></span>

<span data-ttu-id="75b19-119">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="75b19-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="75b19-120">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="75b19-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="75b19-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-122">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="75b19-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-123">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="75b19-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-124">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="75b19-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-125">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="75b19-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-126">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="75b19-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-127">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="75b19-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-128">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="75b19-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-129">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="75b19-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-130">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="75b19-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-131">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="75b19-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-132">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="75b19-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="75b19-133">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="75b19-133">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="75b19-134">Требования</span><span class="sxs-lookup"><span data-stu-id="75b19-134">Requirements</span></span>



| <span data-ttu-id="75b19-135">Требование</span><span class="sxs-lookup"><span data-stu-id="75b19-135">Requirement</span></span> | <span data-ttu-id="75b19-136">Значение</span><span class="sxs-lookup"><span data-stu-id="75b19-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b19-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75b19-137">Minimum supported client</span></span><br/> | <span data-ttu-id="75b19-138">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="75b19-138">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="75b19-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75b19-139">Minimum supported server</span></span><br/> | <span data-ttu-id="75b19-140">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="75b19-140">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75b19-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="75b19-141">Namespace</span></span><br/>                | <span data-ttu-id="75b19-142">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="75b19-142">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="75b19-143">MOF</span><span class="sxs-lookup"><span data-stu-id="75b19-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75b19-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75b19-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75b19-145">DLL</span><span class="sxs-lookup"><span data-stu-id="75b19-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75b19-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75b19-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75b19-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75b19-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b19-148">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="75b19-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="75b19-149">**ресетрепликатионстатистиксекс**</span><span class="sxs-lookup"><span data-stu-id="75b19-149">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

