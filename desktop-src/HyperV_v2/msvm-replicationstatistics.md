---
description: Предоставляет статистику репликации для виртуальной машины.
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Класс Msvm_ReplicationStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683685"
---
# <a name="msvm_replicationstatistics-class"></a><span data-ttu-id="080ac-103">\_Класс мсвм репликатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="080ac-103">Msvm\_ReplicationStatistics class</span></span>

<span data-ttu-id="080ac-104">Предоставляет статистику репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="080ac-104">Provides replication statistics for a virtual machine.</span></span> <span data-ttu-id="080ac-105">Эти статистические данные охватывают длительность, заданную свойствами **мониторингстарттиме** и **мониторингинтервал** класса [**мсвм \_ репликатионсервицесеттингдата**](msvm-replicationservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="080ac-105">These statistics cover the duration specified by the **MonitoringStartTime** and **MonitoringInterval** properties of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class.</span></span>

<span data-ttu-id="080ac-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="080ac-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="080ac-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="080ac-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a><span data-ttu-id="080ac-108">Члены</span><span class="sxs-lookup"><span data-stu-id="080ac-108">Members</span></span>

<span data-ttu-id="080ac-109">Класс **мсвм \_ репликатионстатистикс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="080ac-109">The **Msvm\_ReplicationStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="080ac-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="080ac-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="080ac-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="080ac-111">Properties</span></span>

<span data-ttu-id="080ac-112">Класс **мсвм \_ репликатионстатистикс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="080ac-112">The **Msvm\_ReplicationStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="080ac-113">**аппликатионконсистентснапшотфаилурекаунт**</span><span class="sxs-lookup"><span data-stu-id="080ac-113">**ApplicationConsistentSnapshotFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080ac-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-116">Общее число сбоев моментальных снимков VSS.</span><span class="sxs-lookup"><span data-stu-id="080ac-116">The total number of VSS snapshot failures.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="080ac-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="080ac-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-120">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="080ac-120">A short description of the object.</span></span> <span data-ttu-id="080ac-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="080ac-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="080ac-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="080ac-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-125">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="080ac-125">A description of the object.</span></span> <span data-ttu-id="080ac-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="080ac-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="080ac-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="080ac-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-130">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="080ac-130">A display name for the object.</span></span> <span data-ttu-id="080ac-131">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="080ac-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-132">**ендстатистиктиме**</span><span class="sxs-lookup"><span data-stu-id="080ac-132">**EndStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-133">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="080ac-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-135">Время в формате UTC, когда служба реплики Hyper-V остановила сбор данных статистики репликации.</span><span class="sxs-lookup"><span data-stu-id="080ac-135">The time, in UTC, when the Hyper-V Replica service stopped gathering replication statistics data.</span></span> <span data-ttu-id="080ac-136">В настоящее время начинается новый цикл статистики репликации.</span><span class="sxs-lookup"><span data-stu-id="080ac-136">At this time, a new replication statistics cycle starts.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="080ac-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="080ac-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080ac-140">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="080ac-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="080ac-141">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="080ac-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="080ac-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="080ac-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-143">**ласттестфаиловертиме**</span><span class="sxs-lookup"><span data-stu-id="080ac-143">**LastTestFailoverTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-144">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="080ac-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-146">Указывает время последнего создания системы реплики теста для виртуальной машины с поддержкой репликации на сервере восстановления.</span><span class="sxs-lookup"><span data-stu-id="080ac-146">Indicates the last time a test replica system was created for a replication enabled virtual machine on the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-147">**максрепликатионлатенци**</span><span class="sxs-lookup"><span data-stu-id="080ac-147">**MaxReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080ac-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-150">Максимальное количество времени, затраченное на выполнение одного цикла репликации в секундах.</span><span class="sxs-lookup"><span data-stu-id="080ac-150">The maximum amount of time taken to complete a single replication cycle, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-151">**максрепликатионсизе**</span><span class="sxs-lookup"><span data-stu-id="080ac-151">**MaxReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-152">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="080ac-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-154">Максимальное количество данных репликации, передаваемых в систему узла восстановления, в байтах.</span><span class="sxs-lookup"><span data-stu-id="080ac-154">Maximum replication data transferred to the recovery host system, in bytes.</span></span> <span data-ttu-id="080ac-155">Представляет максимальный размер данных репликации, отправляемых за один цикл для этого интервала.</span><span class="sxs-lookup"><span data-stu-id="080ac-155">This represents the maximum size of replication data sent over a single cycle for this interval.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-156">**нетворкфаилурекаунт**</span><span class="sxs-lookup"><span data-stu-id="080ac-156">**NetworkFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080ac-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-159">Общее число сетевых ошибок, обнаруженных для канала репликации с системой узла восстановления.</span><span class="sxs-lookup"><span data-stu-id="080ac-159">The total number of network errors encountered for the replication channel with recovery host system.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-160">**пендингрепликатионсизе**</span><span class="sxs-lookup"><span data-stu-id="080ac-160">**PendingReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-161">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="080ac-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-163">Размер данных для ожидающей репликации в байтах.</span><span class="sxs-lookup"><span data-stu-id="080ac-163">The size of the data for a pending replication, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-164">**репликатионфаилурекаунт**</span><span class="sxs-lookup"><span data-stu-id="080ac-164">**ReplicationFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080ac-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-167">Общее число сбоев репликации.</span><span class="sxs-lookup"><span data-stu-id="080ac-167">The total number of replication failures.</span></span> <span data-ttu-id="080ac-168">Сюда входят ошибки для операции репликации.</span><span class="sxs-lookup"><span data-stu-id="080ac-168">This includes errors for replication operation.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-169">**репликатионхеалс**</span><span class="sxs-lookup"><span data-stu-id="080ac-169">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080ac-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-172">Работоспособность репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="080ac-172">The replication health for the virtual machine.</span></span> <span data-ttu-id="080ac-173">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="080ac-173">This will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="080ac-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (0)</span><span class="sxs-lookup"><span data-stu-id="080ac-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not applicable** (0)</span></span>
</dt> <dt>

<span data-ttu-id="080ac-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="080ac-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok** (1)</span></span>
</dt> <dt>

<span data-ttu-id="080ac-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (2)</span><span class="sxs-lookup"><span data-stu-id="080ac-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (2)</span></span>
</dt> <dt>

<span data-ttu-id="080ac-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Критическая** (3)</span><span class="sxs-lookup"><span data-stu-id="080ac-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critical** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="080ac-178">**ReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="080ac-178">**ReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-179">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080ac-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-181">Общая задержка репликации при передаче данных в систему узла восстановления (в секундах).</span><span class="sxs-lookup"><span data-stu-id="080ac-181">Total replication latency while transferring the data to the recovery host system, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-182">**репликатионмисскаунт**</span><span class="sxs-lookup"><span data-stu-id="080ac-182">**ReplicationMissCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-183">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080ac-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-185">Количество пропущенных циклов репликации.</span><span class="sxs-lookup"><span data-stu-id="080ac-185">The number of missed replication cycles.</span></span> <span data-ttu-id="080ac-186">Это может быть вызвано высокой нагрузкой, сетевыми проблемами или ошибками репликации.</span><span class="sxs-lookup"><span data-stu-id="080ac-186">This can be because of heavy workload, network issues, or replication errors.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-187">**репликатионсизе**</span><span class="sxs-lookup"><span data-stu-id="080ac-187">**ReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-188">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="080ac-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-190">Общий объем данных репликации, передаваемых в систему узла восстановления в байтах.</span><span class="sxs-lookup"><span data-stu-id="080ac-190">The total amount of replication data transferred to the recovery host system, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-191">**репликатионсукцесскаунт**</span><span class="sxs-lookup"><span data-stu-id="080ac-191">**ReplicationSuccessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-192">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080ac-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-194">Общее число успешных репликаций для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="080ac-194">The total number of successful replications for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="080ac-195">**стартстатистиктиме**</span><span class="sxs-lookup"><span data-stu-id="080ac-195">**StartStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080ac-196">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="080ac-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="080ac-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="080ac-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080ac-198">Время в формате UTC, когда служба реплики Hyper-V приступила к сбору данных статистики репликации.</span><span class="sxs-lookup"><span data-stu-id="080ac-198">The time, in UTC, when the Hyper-V Replica service started gathering replication statistics data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="080ac-199">Требования</span><span class="sxs-lookup"><span data-stu-id="080ac-199">Requirements</span></span>



| <span data-ttu-id="080ac-200">Требование</span><span class="sxs-lookup"><span data-stu-id="080ac-200">Requirement</span></span> | <span data-ttu-id="080ac-201">Значение</span><span class="sxs-lookup"><span data-stu-id="080ac-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="080ac-202">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="080ac-202">Minimum supported client</span></span><br/> | <span data-ttu-id="080ac-203">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="080ac-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="080ac-204">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="080ac-204">Minimum supported server</span></span><br/> | <span data-ttu-id="080ac-205">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="080ac-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="080ac-206">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="080ac-206">Namespace</span></span><br/>                | <span data-ttu-id="080ac-207">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="080ac-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="080ac-208">MOF</span><span class="sxs-lookup"><span data-stu-id="080ac-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="080ac-209"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="080ac-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="080ac-210">DLL</span><span class="sxs-lookup"><span data-stu-id="080ac-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="080ac-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="080ac-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

