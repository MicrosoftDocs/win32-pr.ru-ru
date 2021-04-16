---
description: Представляет состояние репликации для отношения репликации.
ms.assetid: F11EFF86-5CC9-4310-8254-B310C54B561D
title: Класс Msvm_ReplicationRelationship
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationRelationship
- Msvm_ReplicationRelationship.InstanceID
- Msvm_ReplicationRelationship.ReplicationState
- Msvm_ReplicationRelationship.ReplicationHealth
- Msvm_ReplicationRelationship.FailedOverReplicationType
- Msvm_ReplicationRelationship.LastReplicationType
- Msvm_ReplicationRelationship.LastApplicationConsistentReplicationTime
- Msvm_ReplicationRelationship.LastReplicationTime
- Msvm_ReplicationRelationship.LastApplyTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04665f96f4ec77501ee0b161d816c84943ca2c98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650826"
---
# <a name="msvm_replicationrelationship-class"></a><span data-ttu-id="a5bf2-103">\_Класс мсвм репликатионрелатионшип</span><span class="sxs-lookup"><span data-stu-id="a5bf2-103">Msvm\_ReplicationRelationship class</span></span>

<span data-ttu-id="a5bf2-104">Представляет состояние репликации для отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-104">Represents replication status for a replication relationship.</span></span> <span data-ttu-id="a5bf2-105">Так как у вас может быть несколько репликаций для каждой реплики виртуальной машины, этот класс можно использовать для обнаружения каждого отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-105">Because you can have multiple replications for each replica virtual machine, you can use this class to identify each replication relationship.</span></span>

<span data-ttu-id="a5bf2-106">Следующий синтаксис упрощен из MOF-кода и включает эти наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-106">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5bf2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5bf2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationRelationship : CIM_ManagedSystemElement
{
  string   InstanceID;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  datetime LastApplicationConsistentReplicationTime;
  datetime LastReplicationTime;
  datetime LastApplyTime;
};
```

## <a name="members"></a><span data-ttu-id="a5bf2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a5bf2-108">Members</span></span>

<span data-ttu-id="a5bf2-109">Класс **мсвм \_ репликатионрелатионшип** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a5bf2-109">The **Msvm\_ReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="a5bf2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5bf2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5bf2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5bf2-111">Properties</span></span>

<span data-ttu-id="a5bf2-112">Класс **мсвм \_ репликатионрелатионшип** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-112">The **Msvm\_ReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5bf2-113">**фаиледоверрепликатионтипе**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-113">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bf2-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5bf2-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5bf2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bf2-116">Тип отработки отказа, который был выполнен для отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-116">The type of failover that was performed for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="a5bf2-117">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-117">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="a5bf2-118">**Обычный** (1)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-118">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="a5bf2-119">С **совместимостью приложений** (2)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-119">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="a5bf2-120">**Запланировано** (3)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-120">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5bf2-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bf2-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5bf2-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5bf2-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bf2-124">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="a5bf2-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="a5bf2-125">Определяет отношение репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-125">Identifies replication relationship.</span></span> <span data-ttu-id="a5bf2-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a5bf2-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="a5bf2-127">Это свойство имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="a5bf2-127">This property has this format:</span></span>

<span data-ttu-id="a5bf2-128">**Microsoft: <vmid> \\ HVR \\<0/1>**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-128">**Microsoft:<vmid>\\HVR\\<0/1>**</span></span>

<span data-ttu-id="a5bf2-129">0 указывает на первичный, а 1 — на [расширенную репликацию](#extended-replication).</span><span class="sxs-lookup"><span data-stu-id="a5bf2-129">0 indicates primary and 1 indicates [extended replication](#extended-replication).</span></span>

</dd> <dt>

<span data-ttu-id="a5bf2-130">**ластаппликатионконсистентрепликатионтиме**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-130">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bf2-131">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a5bf2-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5bf2-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bf2-133">Дата и время получения последней репликации, соответствующей приложению, при восстановлении для отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-133">The date and time at which the last application consistent replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="a5bf2-134">**ластапплитиме**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-134">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bf2-135">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a5bf2-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5bf2-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bf2-137">Дата и время, когда последняя репликация применяется к восстановлению для отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-137">The date and time at which the last replication is applied on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="a5bf2-138">**ластрепликатионтиме**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-138">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bf2-139">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a5bf2-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5bf2-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bf2-141">Дата и время получения последней репликации при восстановлении для отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-141">The date and time at which the last replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="a5bf2-142">**ластрепликатионтипе**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-142">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bf2-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5bf2-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5bf2-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bf2-145">Тип последней репликации, полученной для отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-145">The type of the last replication that was received for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="a5bf2-146">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-146">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="a5bf2-147">**Обычный** (1)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-147">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="a5bf2-148">С **совместимостью приложений** (2)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-148">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="a5bf2-149">**Запланировано** (3)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-149">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5bf2-150">**репликатионхеалс**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-150">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bf2-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5bf2-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5bf2-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bf2-153">Работоспособность репликации для отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-153">Replication health for the replication relationship.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a5bf2-154">**Неприменимо** (0)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-154">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="a5bf2-155">**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-155">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a5bf2-156">**Предупреждение** (2)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-156">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a5bf2-157">**Критическая** (3)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-157">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a5bf2-158">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-158">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bf2-159">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5bf2-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5bf2-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5bf2-161">Состояние репликации для отношения репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-161">Replication state for the replication relationship.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a5bf2-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="a5bf2-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Готово к репликации** (1)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="a5bf2-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Ожидание завершения начальной репликации** (2)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="a5bf2-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Репликация** (3)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="a5bf2-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Синхронизированная репликация завершена** (4)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="a5bf2-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Восстановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="a5bf2-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Зафиксировано** (6)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="a5bf2-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (7)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a5bf2-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (8)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="a5bf2-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Ожидание запуска повторной синхронизации** (9)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="a5bf2-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>Повторная **Синхронизация** (10)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="a5bf2-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Повторная синхронизация приостановлена** (11)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="a5bf2-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Выполняется отработка отказа** (12)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="a5bf2-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Выполняется восстановление размещения** (13)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="a5bf2-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Восстановление размещения завершено** (14)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="a5bf2-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Выполняется обновление диска** (15)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5bf2-178">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-178">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="a5bf2-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Критическое обновление диска** (16)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5bf2-180">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a5bf2-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (17)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5bf2-182">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-182">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="a5bf2-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Выполняется перецель репликации** (18)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5bf2-184">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-184">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="a5bf2-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Подготовлено к репликации синхронизации** (19)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5bf2-186">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-186">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="a5bf2-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Подготовлено к групповой отмене репликации** (20)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5bf2-188">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-188">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="a5bf2-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Фиредрилл выполняется** (21)</span><span class="sxs-lookup"><span data-stu-id="a5bf2-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a5bf2-190">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-190">This property was added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5bf2-191">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5bf2-191">Remarks</span></span>

### <a name="extended-replication"></a><span data-ttu-id="a5bf2-192">Расширенная репликация</span><span class="sxs-lookup"><span data-stu-id="a5bf2-192">Extended replication</span></span>

<span data-ttu-id="a5bf2-193">Функция репликации Hyper-V в Windows 8 позволяет эффективно реплицировать виртуальные машины, работающие на сервере Hyper-V на первичном сайте, в другой сервер Hyper-V на вторичном сайте.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-193">The Hyper-V replication feature in Windows 8 allows virtual machines that run on a Hyper-V server at the primary site to be efficiently replicated to another Hyper-V server at the secondary site.</span></span>

<span data-ttu-id="a5bf2-194">Функция репликации Hyper-V в Windows 8.1 позволяет пользователю расширить отношение репликации с вторичного сайта на третий сайт.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-194">The Hyper-V replication feature in Windows 8.1 enables a user to extend the replication relationship from the secondary site onwards to a third site.</span></span> <span data-ttu-id="a5bf2-195">Третий сайт может быть предварительно подготовлен узлом Hyper-V в качестве сервера восстановления или внешнего поставщика репликации.</span><span class="sxs-lookup"><span data-stu-id="a5bf2-195">The third site can be a Hyper-V host pre-provisioned as a recovery server or external replication provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5bf2-196">Требования</span><span class="sxs-lookup"><span data-stu-id="a5bf2-196">Requirements</span></span>



| <span data-ttu-id="a5bf2-197">Требование</span><span class="sxs-lookup"><span data-stu-id="a5bf2-197">Requirement</span></span> | <span data-ttu-id="a5bf2-198">Значение</span><span class="sxs-lookup"><span data-stu-id="a5bf2-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bf2-199">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5bf2-199">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bf2-200">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5bf2-200">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a5bf2-201">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5bf2-201">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bf2-202">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5bf2-202">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a5bf2-203">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5bf2-203">Namespace</span></span><br/>                | <span data-ttu-id="a5bf2-204">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a5bf2-204">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a5bf2-205">MOF</span><span class="sxs-lookup"><span data-stu-id="a5bf2-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5bf2-206"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf2-206"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5bf2-207">DLL</span><span class="sxs-lookup"><span data-stu-id="a5bf2-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5bf2-208"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf2-208"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5bf2-209">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5bf2-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bf2-210">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-210">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="a5bf2-211">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="a5bf2-211">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

