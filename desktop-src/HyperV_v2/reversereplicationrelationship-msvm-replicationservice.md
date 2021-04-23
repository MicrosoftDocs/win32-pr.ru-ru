---
description: Реплицирует отработку отказа виртуальной машины обратно на сервер-источник.
ms.assetid: 21806a66-85b4-4d9e-8a50-52d2b1933b67
title: Метод Реверсерепликатионрелатионшип класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ReverseReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 25ab0c754c5139b0b3419db74162a8ac0495cf1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683380"
---
# <a name="reversereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="96c43-103">Метод Реверсерепликатионрелатионшип \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="96c43-103">ReverseReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="96c43-104">Реплицирует отработку отказа виртуальной машины обратно на сервер-источник.</span><span class="sxs-lookup"><span data-stu-id="96c43-104">Replicates a failed-over virtual machine back to the primary server.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c43-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96c43-105">Syntax</span></span>


```mof
uint32 ReverseReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="96c43-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96c43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c43-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96c43-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96c43-108">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой должна быть отменена репликация.</span><span class="sxs-lookup"><span data-stu-id="96c43-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be reversed.</span></span>

</dd> <dt>

<span data-ttu-id="96c43-109">*Репликатионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96c43-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96c43-110">Строковое представление экземпляра класса [**мсвм \_ репликатионсеттингдата**](msvm-replicationsettingdata.md) , определяющего параметры репликации.</span><span class="sxs-lookup"><span data-stu-id="96c43-110">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="96c43-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="96c43-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96c43-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="96c43-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c43-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96c43-113">Return value</span></span>

<span data-ttu-id="96c43-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="96c43-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="96c43-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="96c43-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="96c43-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="96c43-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="96c43-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="96c43-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="96c43-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="96c43-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="96c43-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="96c43-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="96c43-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="96c43-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="96c43-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="96c43-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="96c43-128">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="96c43-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="96c43-129">Требования</span><span class="sxs-lookup"><span data-stu-id="96c43-129">Requirements</span></span>



| <span data-ttu-id="96c43-130">Требование</span><span class="sxs-lookup"><span data-stu-id="96c43-130">Requirement</span></span> | <span data-ttu-id="96c43-131">Значение</span><span class="sxs-lookup"><span data-stu-id="96c43-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96c43-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96c43-132">Minimum supported client</span></span><br/> | <span data-ttu-id="96c43-133">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="96c43-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="96c43-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96c43-134">Minimum supported server</span></span><br/> | <span data-ttu-id="96c43-135">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="96c43-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96c43-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="96c43-136">Namespace</span></span><br/>                | <span data-ttu-id="96c43-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="96c43-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="96c43-138">MOF</span><span class="sxs-lookup"><span data-stu-id="96c43-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96c43-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96c43-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="96c43-140">DLL</span><span class="sxs-lookup"><span data-stu-id="96c43-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96c43-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="96c43-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="96c43-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96c43-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c43-143">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="96c43-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

