---
description: Запускает репликацию виртуальной машины.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Метод StartReplication класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4702b5b73a989e2889bf1da9e4d284afdfe5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343162"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="e1225-103">Метод StartReplication \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="e1225-103">StartReplication method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="e1225-104">Запускает репликацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e1225-104">Starts the replication of a virtual machine.</span></span> <span data-ttu-id="e1225-105">Когда клиент вызывает этот метод для реплики виртуальной машины, он запускает репликацию с помощью расширенной реплики.</span><span class="sxs-lookup"><span data-stu-id="e1225-105">When a client calls this method for a replica virtual machine, it starts the replication with extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1225-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1225-106">Syntax</span></span>


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e1225-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1225-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1225-108">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1225-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1225-109">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой должна быть запущена репликация.</span><span class="sxs-lookup"><span data-stu-id="e1225-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be started.</span></span>

</dd> <dt>

<span data-ttu-id="e1225-110">*Инитиалрепликатионтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1225-110">*InitialReplicationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1225-111">Тип перемещения, используемый для выполнения начальной репликации.</span><span class="sxs-lookup"><span data-stu-id="e1225-111">The type of transfer to be used for performing the initial replication.</span></span>

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span data-ttu-id="e1225-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Сетевая перенаправление** (1)</span><span class="sxs-lookup"><span data-stu-id="e1225-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Network Transfer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e1225-113">Сетевая перенаправление.</span><span class="sxs-lookup"><span data-stu-id="e1225-113">Network transfer.</span></span>

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span data-ttu-id="e1225-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Экспорт** (2)</span><span class="sxs-lookup"><span data-stu-id="e1225-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Export** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e1225-115">Экспорт.</span><span class="sxs-lookup"><span data-stu-id="e1225-115">Export.</span></span>

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span data-ttu-id="e1225-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Начальная сетевая перенаправление** (3)</span><span class="sxs-lookup"><span data-stu-id="e1225-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded Network Transfer** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e1225-117">Начальная сетевая перенаправление.</span><span class="sxs-lookup"><span data-stu-id="e1225-117">Seeded network transfer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e1225-118">*Инитиалрепликатионекспортлокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1225-118">*InitialReplicationExportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1225-119">Если *инитиалрепликатионтипе* имеет значение 2 (экспорт), этот параметр содержит полный путь к каталогу, в который должна быть экспортирована начальная репликация.</span><span class="sxs-lookup"><span data-stu-id="e1225-119">If *InitialReplicationType* is 2 (Export), this parameter contains the fully qualified path of the directory to which the initial replication is to be exported.</span></span> <span data-ttu-id="e1225-120">Этот параметр не используется для других значений *инитиалрепликатионтипе* и может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1225-120">This parameter is not used for other values of *InitialReplicationType*, and can be **Null**.</span></span> <span data-ttu-id="e1225-121">Этот каталог можно использовать повторно для экспорта нескольких репликаций виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e1225-121">This directory can be reused for exporting multiple virtual machine replication.</span></span> <span data-ttu-id="e1225-122">Этот метод размещает каждую репликацию виртуальной машины в отдельном подкаталоге по этому пути.</span><span class="sxs-lookup"><span data-stu-id="e1225-122">This method places each virtual machine replication in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="e1225-123">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1225-123">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1225-124">Запланированное время начала начальной репликации по сетевому подключению к серверу восстановления.</span><span class="sxs-lookup"><span data-stu-id="e1225-124">The scheduled start time for the initial replication over the network connection to recovery server.</span></span> <span data-ttu-id="e1225-125">Этот параметр игнорируется, если *инитиалрепликатионтипе* имеет 2 (экспорт).</span><span class="sxs-lookup"><span data-stu-id="e1225-125">This parameter is ignored when *InitialReplicationType* is 2 (Export).</span></span> <span data-ttu-id="e1225-126">Если этот параметр имеет **значение NULL**, начальная репликация запускается немедленно.</span><span class="sxs-lookup"><span data-stu-id="e1225-126">If this parameter is **Null**, the initial replication starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="e1225-127">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e1225-127">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1225-128">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e1225-128">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1225-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1225-129">Return value</span></span>

<span data-ttu-id="e1225-130">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e1225-130">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e1225-131">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e1225-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-132">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="e1225-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-133">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="e1225-133">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-134">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="e1225-134">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-135">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="e1225-135">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-136">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="e1225-136">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-137">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="e1225-137">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-138">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="e1225-138">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-139">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="e1225-139">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-140">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="e1225-140">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-141">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="e1225-141">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-142">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="e1225-142">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-143">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="e1225-143">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e1225-144">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="e1225-144">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e1225-145">Требования</span><span class="sxs-lookup"><span data-stu-id="e1225-145">Requirements</span></span>



| <span data-ttu-id="e1225-146">Требование</span><span class="sxs-lookup"><span data-stu-id="e1225-146">Requirement</span></span> | <span data-ttu-id="e1225-147">Значение</span><span class="sxs-lookup"><span data-stu-id="e1225-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1225-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1225-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e1225-149">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e1225-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e1225-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1225-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e1225-151">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e1225-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1225-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e1225-152">Namespace</span></span><br/>                | <span data-ttu-id="e1225-153">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e1225-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e1225-154">MOF</span><span class="sxs-lookup"><span data-stu-id="e1225-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1225-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1225-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1225-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e1225-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1225-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1225-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e1225-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1225-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1225-159">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="e1225-159">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

