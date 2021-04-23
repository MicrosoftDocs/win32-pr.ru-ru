---
description: Представляет коллекцию виртуальных систем.
ms.assetid: acf51beb-1103-43a4-8dc5-1a7f2a0482be
title: Класс Msvm_VirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCollection
- Msvm_VirtualSystemCollection.CollectionID
- Msvm_VirtualSystemCollection.ElementName
- Msvm_VirtualSystemCollection.LastApplyConsistencyLevel
- Msvm_VirtualSystemCollection.LastApplyVirtualMachineIds
- Msvm_VirtualSystemCollection.LastApplyTime
- Msvm_VirtualSystemCollection.FailedOverReplicationType
- Msvm_VirtualSystemCollection.ReplicationMode
- Msvm_VirtualSystemCollection.ReplicationState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a9746356744f2743a8d6656ef4c61044223be113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423690"
---
# <a name="msvm_virtualsystemcollection-class"></a><span data-ttu-id="ec4d0-103">\_Класс мсвм виртуалсистемколлектион</span><span class="sxs-lookup"><span data-stu-id="ec4d0-103">Msvm\_VirtualSystemCollection class</span></span>

<span data-ttu-id="ec4d0-104">Представляет коллекцию виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-104">Represents a collection of virtual systems.</span></span>

<span data-ttu-id="ec4d0-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec4d0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec4d0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCollection : CIM_CollectionOfMSEs
{
  string   CollectionID;
  string   ElementName;
  uint16   LastApplyConsistencyLevel;
  String   LastApplyVirtualMachineIds[];
  DateTime LastApplyTime;
  uint16   FailedOverReplicationType;
  uint16   ReplicationMode;
  uint16   ReplicationState;
};
```

## <a name="members"></a><span data-ttu-id="ec4d0-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ec4d0-107">Members</span></span>

<span data-ttu-id="ec4d0-108">Класс **мсвм \_ виртуалсистемколлектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ec4d0-108">The **Msvm\_VirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="ec4d0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec4d0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec4d0-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec4d0-110">Properties</span></span>

<span data-ttu-id="ec4d0-111">Класс **мсвм \_ виртуалсистемколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-111">The **Msvm\_VirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec4d0-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec4d0-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec4d0-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ec4d0-116">Уникальная идентификация объекта коллекции.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="ec4d0-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec4d0-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec4d0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="ec4d0-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="ec4d0-121">Определяемое пользователем имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-121">An user-defined name for the collection.</span></span> <span data-ttu-id="ec4d0-122">Обратите внимание, что это не обязательно должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-122">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="ec4d0-123">**фаиледоверрепликатионтипе**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-123">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec4d0-124">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec4d0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec4d0-126">Тип отработки отказа, который был выполнен для коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-126">Type of failover that was performed for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="ec4d0-127">Добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-127">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ec4d0-128">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-128">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="ec4d0-129">**Обычный** (1)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-129">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="ec4d0-130">**Запланировано** (2)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-130">**Planned** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec4d0-131">**ластаппликонсистенцилевел**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-131">**LastApplyConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec4d0-132">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec4d0-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec4d0-134">Уровень согласованности последнего примененного разностного изменения.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-134">Consistency level of the last applied delta.</span></span>

> [!Note]  
> <span data-ttu-id="ec4d0-135">Добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-135">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ec4d0-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="ec4d0-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>С **совместимостью приложений** (1)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ec4d0-138">Последняя примененная Дельта указывает на момент времени, когда виртуальная система находилась в состоянии совместимости с приложениями.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-138">The last applied delta indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="ec4d0-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Отказоустойчивость (2** )</span><span class="sxs-lookup"><span data-stu-id="ec4d0-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ec4d0-140">Последняя примененная Дельта указывает на момент времени, когда виртуальная система находилась в состоянии отказоустойчивости.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-140">The last applied delta indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span data-ttu-id="ec4d0-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Противоречивое аварийное завершение группы** (3)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Group Crash Consistent** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ec4d0-142">Последняя примененная Дельта указывает на момент времени, когда группа находилась в состоянии сбоя.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-142">The last applied delta indicates a point in time when the group was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec4d0-143">**ластапплитиме**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-143">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec4d0-144">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-144">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec4d0-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec4d0-146">Время, когда последняя репликация применяется к восстановлению для коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-146">The time at which the last replication is applied on recovery for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="ec4d0-147">Добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-147">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ec4d0-148">**ластаппливиртуалмачинеидс**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-148">**LastApplyVirtualMachineIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec4d0-149">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-149">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec4d0-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec4d0-151">Массив идентификаторов виртуальных машин, которые были успешно применены при последнем цикле применения.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-151">Array of Virtual Machine Ids which were successfully applied in last apply cycle.</span></span>

> [!Note]  
> <span data-ttu-id="ec4d0-152">Добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-152">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ec4d0-153">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-153">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec4d0-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec4d0-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec4d0-156">Тип репликации для коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-156">Replication type for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="ec4d0-157">Добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-157">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ec4d0-158">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-158">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="ec4d0-159">**Основной** (1)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-159">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="ec4d0-160">**Реплика** (2)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-160">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="ec4d0-161">**Тестовая реплика** (3)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-161">**Test Replica** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec4d0-162">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-162">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec4d0-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec4d0-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec4d0-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec4d0-165">Состояние репликации для коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-165">Replication state for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="ec4d0-166">Добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="ec4d0-166">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ec4d0-167">**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-167">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="ec4d0-168">**Готово к репликации** (1)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-168">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="ec4d0-169">**Ожидание завершения начальной репликации** (2)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-169">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="ec4d0-170">**Репликация** (3)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-170">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

<span data-ttu-id="ec4d0-171">**Инициирована отработка отказа** (4)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-171">**Failover initiated** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="ec4d0-172">**Восстановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-172">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="ec4d0-173">**Зафиксировано** (6)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-173">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="ec4d0-174">**Приостановлено** (7)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-174">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="ec4d0-175">**Критическая** (8)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-175">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="ec4d0-176">**Ожидание запуска повторной синхронизации** (9)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-176">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="ec4d0-177">Повторная **Синхронизация** (10)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-177">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

<span data-ttu-id="ec4d0-178">**Плановая отработка отказа Инитиатедрепурпосе инитиатедтест отработка отказа включена** (11)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-178">**Planned failover initiatedRepurpose initiatedTest failover initiatedPartially enabled** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

<span data-ttu-id="ec4d0-179">**Частично отключено** (12)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-179">**Partially disabled** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

<span data-ttu-id="ec4d0-180">**Частично восстановлено** (13)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-180">**Partially recovered** (13)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec4d0-181">(14)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-181">(14)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec4d0-182">(15)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-182">(15)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec4d0-183">(16)</span><span class="sxs-lookup"><span data-stu-id="ec4d0-183">(16)</span></span>


<span data-ttu-id="ec4d0-184"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ec4d0-184"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ec4d0-185">Требования</span><span class="sxs-lookup"><span data-stu-id="ec4d0-185">Requirements</span></span>



| <span data-ttu-id="ec4d0-186">Требование</span><span class="sxs-lookup"><span data-stu-id="ec4d0-186">Requirement</span></span> | <span data-ttu-id="ec4d0-187">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4d0-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec4d0-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec4d0-188">Minimum supported client</span></span><br/> | <span data-ttu-id="ec4d0-189">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ec4d0-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ec4d0-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec4d0-190">Minimum supported server</span></span><br/> | <span data-ttu-id="ec4d0-191">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ec4d0-191">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ec4d0-192">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ec4d0-192">Namespace</span></span><br/>                | <span data-ttu-id="ec4d0-193">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ec4d0-193">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ec4d0-194">MOF</span><span class="sxs-lookup"><span data-stu-id="ec4d0-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec4d0-195"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec4d0-195"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec4d0-196">DLL</span><span class="sxs-lookup"><span data-stu-id="ec4d0-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec4d0-197"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec4d0-197"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec4d0-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec4d0-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec4d0-199">**\_КОЛЛЕКТИОНОФМСЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec4d0-199">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

