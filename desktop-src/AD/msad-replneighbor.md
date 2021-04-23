---
title: Класс MSAD_ReplNeighbor
description: Представляет \_ \_ структуру соседей DS REPL, которая содержит сведения о состоянии входящей репликации для определенной пары контекста именования (NC) и исходного сервера.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- Класс MSAD_ReplNeighbor Active Directory
- Active Directory класса MSAD_ReplNeighbor, описание
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988699"
---
# <a name="msad_replneighbor-class"></a><span data-ttu-id="61524-105">\_Класс МСАД реплнеигхбор</span><span class="sxs-lookup"><span data-stu-id="61524-105">MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="61524-106">Представляет структуру [**\_ \_ соседей DS REPL**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) , которая содержит сведения о состоянии входящей репликации для определенной пары контекста именования (NC) и исходного сервера, возвращаемые функцией [**дсрепликажетинфо**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .</span><span class="sxs-lookup"><span data-stu-id="61524-106">Represents the [**DS\_REPL\_NEIGHBOR**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) structure, which contains the inbound replication state information for a particular naming context (NC) and source server pair, as returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="61524-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61524-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a><span data-ttu-id="61524-108">Члены</span><span class="sxs-lookup"><span data-stu-id="61524-108">Members</span></span>

<span data-ttu-id="61524-109">Класс **МСАД \_ реплнеигхбор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="61524-109">The **MSAD\_ReplNeighbor** class has these types of members:</span></span>

-   [<span data-ttu-id="61524-110">Методы</span><span class="sxs-lookup"><span data-stu-id="61524-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="61524-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="61524-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="61524-112">Методы</span><span class="sxs-lookup"><span data-stu-id="61524-112">Methods</span></span>

<span data-ttu-id="61524-113">Класс **МСАД \_ реплнеигхбор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="61524-113">The **MSAD\_ReplNeighbor** class has these methods.</span></span>



| <span data-ttu-id="61524-114">Метод</span><span class="sxs-lookup"><span data-stu-id="61524-114">Method</span></span>                                                           | <span data-ttu-id="61524-115">Описание</span><span class="sxs-lookup"><span data-stu-id="61524-115">Description</span></span>                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="61524-116">**синкнамингконтекст**</span><span class="sxs-lookup"><span data-stu-id="61524-116">**SyncNamingContext**</span></span>](syncnamingcontext-msad-replneighbor.md) | <span data-ttu-id="61524-117">Синхронизирует целевой контекст именования с одним из его источников.</span><span class="sxs-lookup"><span data-stu-id="61524-117">Synchronizes a destination naming context with one of its sources.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="61524-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="61524-118">Properties</span></span>

<span data-ttu-id="61524-119">Класс **МСАД \_ реплнеигхбор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="61524-119">The **MSAD\_ReplNeighbor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61524-120">**асинЦинтерситетранспортдн**</span><span class="sxs-lookup"><span data-stu-id="61524-120">**AsyncIntersiteTransportDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-123">Возвращает путь X. 500 объекта [**интерситетранспорт**](/windows/desktop/ADSchema/c-intersitetransport) , который соответствует транспорту, по которому выполняется репликация.</span><span class="sxs-lookup"><span data-stu-id="61524-123">Gets the X.500 path of the [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) object that corresponds to the transport over which replication is performed.</span></span> <span data-ttu-id="61524-124">Задайте для репликации RPC/IP **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="61524-124">Set to **NULL** for RPC/IP replication.</span></span>

</dd> <dt>

<span data-ttu-id="61524-125">**асинЦинтерситетранспортобжгуид**</span><span class="sxs-lookup"><span data-stu-id="61524-125">**AsyncIntersiteTransportObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-126">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-128">Возвращает идентификатор GUID объекта межсайтового транспорта, соответствующего свойству **асинЦинтерситетранспортдн** .</span><span class="sxs-lookup"><span data-stu-id="61524-128">Gets the GUID of the intersite transport object that corresponds to the **AsyncIntersiteTransportDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-129">**компрессчанжес**</span><span class="sxs-lookup"><span data-stu-id="61524-129">**CompressChanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-130">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-132">Возвращает значение, указывающее, задан ли **флаг \_ \_ \_ сжатия \_ Changes НБР redirectory REPL** в свойстве **репликафлагс** .</span><span class="sxs-lookup"><span data-stu-id="61524-132">Gets the value that indicates whether the **DS\_REPL\_NBR\_COMPRESS\_CHANGES** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-133">**дисаблесчедуледсинк**</span><span class="sxs-lookup"><span data-stu-id="61524-133">**DisableScheduledSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-136">Возвращает значение, указывающее, был ли установлен флаг **\_ \_ \_ \_ плановой \_ синхронизации DS REPL НБР Disabled Sync** в свойстве **репликафлагс** .</span><span class="sxs-lookup"><span data-stu-id="61524-136">Gets the value that indicates whether the **DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-137">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="61524-137">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-138">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-140">Возвращает каноническое имя домена реплицированного NC.</span><span class="sxs-lookup"><span data-stu-id="61524-140">Gets the canonical name of the domain of the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="61524-141">**досчедуледсинкс**</span><span class="sxs-lookup"><span data-stu-id="61524-141">**DoScheduledSyncs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-144">Возвращает значение, указывающее, установлен ли флаг **DS \_ REPL \_ НБР \_ Do \_ Schedule \_ syncs** в свойстве **репликафлагс** .</span><span class="sxs-lookup"><span data-stu-id="61524-144">Gets the value that indicates whether the **DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-145">**фуллсинЦинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="61524-145">**FullSyncInProgress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-146">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-148">Возвращает значение, указывающее, установлен ли **флаг \_ \_ \_ \_ \_ \_ выполнения НБР полной синхронизации DS REPL** в свойстве **репликафлагс** .</span><span class="sxs-lookup"><span data-stu-id="61524-148">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-149">**фуллсинкнекстпаккет**</span><span class="sxs-lookup"><span data-stu-id="61524-149">**FullSyncNextPacket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-150">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-152">Возвращает значение, указывающее, установлен ли в свойстве **репликафлагс** флаг **DS \_ REPL для \_ \_ полной \_ синхронизации \_ следующего \_ пакета** .</span><span class="sxs-lookup"><span data-stu-id="61524-152">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-153">**игноречанженотификатионс**</span><span class="sxs-lookup"><span data-stu-id="61524-153">**IgnoreChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-154">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-156">Возвращает значение, указывающее, установлен ли **флаг \_ \_ НБР \_ Ignore \_ \_ извещения об изменении уведомлений DS REPL** в свойстве **репликафлагс** .</span><span class="sxs-lookup"><span data-stu-id="61524-156">Gets the value that indicates whether the **DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-157">**исделетедсаурцедса**</span><span class="sxs-lookup"><span data-stu-id="61524-157">**IsDeletedSourceDsa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-158">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-160">Возвращает значение, указывающее, представляет ли это соединение исходный контроллер домена, который был удален.</span><span class="sxs-lookup"><span data-stu-id="61524-160">Gets the value that indicates whether this connection represents a source DC that has been deleted.</span></span> <span data-ttu-id="61524-161">**Значение true** , если это подключение представляет исходный контроллер домена, который был удален; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="61524-161">**TRUE** if this connection represents a source DC that has been deleted; otherwise, **FALSE**.</span></span> <span data-ttu-id="61524-162">Служба DS будет по-прежнему реплицировать эти подключения на некоторое время после удаления исходного контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="61524-162">By design, the DS will continue to replicate these connections for some time for some time after the source DC is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="61524-163">**ластсинкресулт**</span><span class="sxs-lookup"><span data-stu-id="61524-163">**LastSyncResult**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-164">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61524-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61524-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-166">Возвращает код ошибки **HRESULT** для последней попытки репликации.</span><span class="sxs-lookup"><span data-stu-id="61524-166">Gets the **HRESULT** error code for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="61524-167">**модифиеднумконсекутивесинкфаилурес**</span><span class="sxs-lookup"><span data-stu-id="61524-167">**ModifiedNumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61524-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61524-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-170">Возвращает число последовательных неудачных попыток репликации, не включая ожидаемые подключения.</span><span class="sxs-lookup"><span data-stu-id="61524-170">Gets the number of consecutive failed replication attempts, not including the connections that are expected to fail.</span></span> <span data-ttu-id="61524-171">Например, если свойство **исделетедсаурцедса** имеет значение **true**, ожидается сбой.</span><span class="sxs-lookup"><span data-stu-id="61524-171">For example, if the **IsDeletedSourceDsa** property is set to **TRUE**, it is expected to fail.</span></span>

</dd> <dt>

<span data-ttu-id="61524-172">**намингконтекстдн**</span><span class="sxs-lookup"><span data-stu-id="61524-172">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-173">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61524-175">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61524-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61524-176">Возвращает путь X. 500 для сетевого контроллера, который реплицируется с помощью этого соединения.</span><span class="sxs-lookup"><span data-stu-id="61524-176">Gets the X.500 path for the NC that is replicated by this connection.</span></span>

</dd> <dt>

<span data-ttu-id="61524-177">**намингконтекстобжгуид**</span><span class="sxs-lookup"><span data-stu-id="61524-177">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-178">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-180">Возвращает идентификатор GUID для реплицированного NC.</span><span class="sxs-lookup"><span data-stu-id="61524-180">Gets the GUID for the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="61524-181">**неверсинцед**</span><span class="sxs-lookup"><span data-stu-id="61524-181">**NeverSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-182">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-184">Возвращает значение, указывающее, был ли установлен флаг **DS \_ REPL \_ НБР, \_ не \_ синхронизированный** в свойстве **репликафлагс** .</span><span class="sxs-lookup"><span data-stu-id="61524-184">Gets the value that indicates whether the **DS\_REPL\_NBR\_NEVER\_SYNCED** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-185">**ночанженотификатионс**</span><span class="sxs-lookup"><span data-stu-id="61524-185">**NoChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-186">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-188">Возвращает значение, указывающее, был ли установлен флаг **DS \_ REPL \_ НБР \_ No \_ Change \_ Notifications** в свойстве **репликафлагс** .</span><span class="sxs-lookup"><span data-stu-id="61524-188">Gets the value that indicates whether the **DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-189">**нумконсекутивесинкфаилурес**</span><span class="sxs-lookup"><span data-stu-id="61524-189">**NumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-190">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61524-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61524-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-192">Возвращает число последовательных неудачных попыток репликации.</span><span class="sxs-lookup"><span data-stu-id="61524-192">Gets the number of consecutive failed replication attempts.</span></span>

</dd> <dt>

<span data-ttu-id="61524-193">**репликафлагс**</span><span class="sxs-lookup"><span data-stu-id="61524-193">**ReplicaFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-194">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61524-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61524-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-196">Возвращает набор флагов, задающих атрибуты и параметры для данных репликации.</span><span class="sxs-lookup"><span data-stu-id="61524-196">Gets the set of flags that specify attributes and options for the replication data.</span></span> <span data-ttu-id="61524-197">Это свойство может быть равно нулю или быть сочетанием одного или нескольких из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="61524-197">This property can be zero or a combination of one or more of the following flags.</span></span>

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span data-ttu-id="61524-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**Службы каталогов \_ REPL: \_ НБР \_ запись** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="61524-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS\_REPL\_NBR\_WRITEABLE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="61524-199">Локальная копия контекста именования доступна для записи.</span><span class="sxs-lookup"><span data-stu-id="61524-199">The local copy of the naming context is writable.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span data-ttu-id="61524-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**Службы каталогов \_ REPL \_ : \_ Синхронизация НБР \_ при \_ запуске** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="61524-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="61524-201">Репликация этого контекста именования из этого источника предпринимается при загрузке целевого сервера.</span><span class="sxs-lookup"><span data-stu-id="61524-201">Replication of this naming context from this source is attempted when the destination server is booted.</span></span> <span data-ttu-id="61524-202">Этот флаг обычно применяется только к соседям внутри сайта.</span><span class="sxs-lookup"><span data-stu-id="61524-202">This flag usually only applies to intra-site neighbors.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span data-ttu-id="61524-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**Службы каталогов \_ REPL: \_ НБР \_ выполнять \_ запланированные \_ синхронизации** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="61524-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="61524-204">Выполнение репликации по расписанию.</span><span class="sxs-lookup"><span data-stu-id="61524-204">Perform replication on a schedule.</span></span> <span data-ttu-id="61524-205">Этот флаг обычно задается, если только расписание для этого контекста именования или источника не равно «никогда», то есть пустое расписание.</span><span class="sxs-lookup"><span data-stu-id="61524-205">This flag is usually set unless the schedule for this naming context or source is "never", that is, the empty schedule.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span data-ttu-id="61524-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**Службы каталогов \_ REPL: \_ НБР \_ использование \_ асинхронного \_ межсайтового \_ транспорта** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="61524-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="61524-207">Выполнение репликации непрямым путем через службу межсайтовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="61524-207">Perform replication indirectly through the Inter-Site Messaging Service.</span></span> <span data-ttu-id="61524-208">Этот флаг устанавливается только при репликации по протоколу SMTP.</span><span class="sxs-lookup"><span data-stu-id="61524-208">This flag is set only when replicating over SMTP.</span></span> <span data-ttu-id="61524-209">Флаг не устанавливается при репликации по межсайтовому протоколу RPC/IP.</span><span class="sxs-lookup"><span data-stu-id="61524-209">This flag is not set when replicating over inter-site RPC/IP.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span data-ttu-id="61524-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**Службы каталогов \_ \_НБР \_ Синхронизация двух \_ сторон \_ репликации** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="61524-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS\_REPL\_NBR\_TWO\_WAY\_SYNC** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="61524-211">Если задано значение, указывает, что после завершения входящей репликации целевой сервер должен сообщить исходному серверу о необходимости синхронизации в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="61524-211">If set, indicates that when inbound replication is complete, the destination server must tell the source server to synchronize in the reverse direction.</span></span> <span data-ttu-id="61524-212">Данная функция используется в скриптах коммутируемого доступа, когда коммутируемое подключение может инициировать только один из двух серверов.</span><span class="sxs-lookup"><span data-stu-id="61524-212">This feature is used in dial-up scenarios where only one of the two servers can initiate a dial-up connection.</span></span> <span data-ttu-id="61524-213">Например, этот параметр можно использовать в головном офисе организации и филиале, где филиал подключается к корпоративному офису через Интернет через коммутируемое подключение к поставщику услуг Интернета.</span><span class="sxs-lookup"><span data-stu-id="61524-213">For example, this option could be used in a corporate headquarters and branch office, where the branch office connects to the corporate headquarters over the Internet by means of a dial-up ISP connection.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span data-ttu-id="61524-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**Службы каталогов \_ REPL \_ НБР \_ возвращает \_ \_ родительские объекты** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="61524-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS\_REPL\_NBR\_RETURN\_OBJECT\_PARENTS** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="61524-215">Данный сосед находится в состоянии, когда он возвращает родительские объекты перед дочерними.</span><span class="sxs-lookup"><span data-stu-id="61524-215">This neighbor is in a state where it returns parent objects before children objects.</span></span> <span data-ttu-id="61524-216">Он входит в это состоянии после получения дочернего объекта перед его родителем.</span><span class="sxs-lookup"><span data-stu-id="61524-216">It goes into this state after it receives a child object before its parent.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span data-ttu-id="61524-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**Службы каталогов \_ \_ \_ \_ \_ \_ Выполняется полная синхронизация REPL НБР** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="61524-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="61524-218">Сервер назначения выполняет полную синхронизацию с исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="61524-218">The destination server is performing a full synchronization from the source server.</span></span> <span data-ttu-id="61524-219">При полной синхронизации не используются векторы, которые создают обновления (например, [**DS \_ REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) для фильтрации обновлений.</span><span class="sxs-lookup"><span data-stu-id="61524-219">Full synchronizations do not use vectors that create updates (such as [**DS\_REPL\_CURSORS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) for filtering updates.</span></span> <span data-ttu-id="61524-220">Полная синхронизация не используется в качестве части протокола репликации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61524-220">Full synchronizations are not used as a part of the default replication protocol.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span data-ttu-id="61524-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**Службы каталогов \_ \_ \_ \_ \_ Следующий \_ пакет для НБР полной синхронизации REPL** : (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="61524-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="61524-222">Последний пакет из источника указал изменение объекта, который еще не был создан целевым сервером.</span><span class="sxs-lookup"><span data-stu-id="61524-222">The last packet from the source indicated a modification of an object that the destination server has not yet created.</span></span> <span data-ttu-id="61524-223">Следующий запрашиваемый пакет сообщает исходному серверу, что все атрибуты измененного объекта помещаются в пакет.</span><span class="sxs-lookup"><span data-stu-id="61524-223">The next packet to be requested instructs the source server to put all attributes of the modified object into the packet.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span data-ttu-id="61524-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**Службы каталогов \_ REPL: \_ НБР \_ не \_ синхронизировано** (2097152 (0x200000))</span><span class="sxs-lookup"><span data-stu-id="61524-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS\_REPL\_NBR\_NEVER\_SYNCED** (2097152 (0x200000))</span></span>


</dt> <dd>

<span data-ttu-id="61524-225">Синхронизация никогда не была завершена успешно от данного источника.</span><span class="sxs-lookup"><span data-stu-id="61524-225">A synchronization has never been successfully completed from this source.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span data-ttu-id="61524-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**Службы каталогов \_ REPL \_ НБР с \_ вытеснением** (16777216 (0x1000000))</span><span class="sxs-lookup"><span data-stu-id="61524-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS\_REPL\_NBR\_PREEMPTED** (16777216 (0x1000000))</span></span>


</dt> <dd>

<span data-ttu-id="61524-227">Модуль репликации временно прекратил обработку этого соседа для обслуживания другого соседа с более высоким приоритетом, либо для этой секции, либо для другой секции.</span><span class="sxs-lookup"><span data-stu-id="61524-227">The replication engine has temporarily stopped processing this neighbor in order to service another higher-priority neighbor, either for this partition or for another partition.</span></span> <span data-ttu-id="61524-228">Механизм репликации продолжит обработку этого соседа после завершения высокоприоритетной работы.</span><span class="sxs-lookup"><span data-stu-id="61524-228">The replication engine will resume processing this neighbor after the higher-priority work is completed.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span data-ttu-id="61524-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**Службы каталогов \_ \_НБР \_ игнорировать \_ \_ уведомления об изменениях** (67108864 (0x4000000))</span><span class="sxs-lookup"><span data-stu-id="61524-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** (67108864 (0x4000000))</span></span>


</dt> <dd>

<span data-ttu-id="61524-230">Этот сосед имеет значение отключить синхронизацию на основе уведомлений.</span><span class="sxs-lookup"><span data-stu-id="61524-230">This neighbor is set to disable notification-based synchronizations.</span></span> <span data-ttu-id="61524-231">В пределах узла контроллеры домена синхронизируются друг с другом на основе уведомлений, когда происходят изменения.</span><span class="sxs-lookup"><span data-stu-id="61524-231">Within a site, domain controllers synchronize with each other based on notifications when changes occur.</span></span> <span data-ttu-id="61524-232">Этот параметр не разрешает этому соседу выполнять синхронизацию, активируемую уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="61524-232">This setting prevents this neighbor from performing synchronizations that are triggered by notifications.</span></span> <span data-ttu-id="61524-233">Сосед по-прежнему будет выполнять синхронизацию в соответствии с расписанием или в ответ на запрошенные вручную синхронизации.</span><span class="sxs-lookup"><span data-stu-id="61524-233">The neighbor will still do synchronizations based on its schedule, or in response to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span data-ttu-id="61524-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**Службы каталогов \_ REPL \_ НБР \_ Отключить \_ запланированную \_ синхронизацию** (134217728 (0x8000000))</span><span class="sxs-lookup"><span data-stu-id="61524-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** (134217728 (0x8000000))</span></span>


</dt> <dd>

<span data-ttu-id="61524-235">Для этого соседа задано значение не выполнять синхронизацию в соответствии с расписанием.</span><span class="sxs-lookup"><span data-stu-id="61524-235">This neighbor is set to not perform synchronizations based on its schedule.</span></span> <span data-ttu-id="61524-236">Единственный способ, которым этот сосед будет выполнять синхронизацию, — в ответ на уведомления об изменениях или на синхронизацию вручную.</span><span class="sxs-lookup"><span data-stu-id="61524-236">The only way this neighbor will perform synchronizations is in response to change notifications or to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span data-ttu-id="61524-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**Службы каталогов \_ REPL: \_ НБР \_ Сжатие \_ изменений** (268435456 (0x10000000))</span><span class="sxs-lookup"><span data-stu-id="61524-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS\_REPL\_NBR\_COMPRESS\_CHANGES** (268435456 (0x10000000))</span></span>


</dt> <dd>

<span data-ttu-id="61524-238">Изменения, полученные из этого источника, должны быть сжаты.</span><span class="sxs-lookup"><span data-stu-id="61524-238">Changes received from this source are to be compressed.</span></span> <span data-ttu-id="61524-239">Сжатие обычно происходит, только если исходный сервер находится на другом сайте.</span><span class="sxs-lookup"><span data-stu-id="61524-239">Compression usually occurs only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span data-ttu-id="61524-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**Службы каталогов \_ REPL \_ : \_ НБР \_ без \_ уведомлений об изменениях** (536870912 (0x20000000))</span><span class="sxs-lookup"><span data-stu-id="61524-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** (536870912 (0x20000000))</span></span>


</dt> <dd>

<span data-ttu-id="61524-241">От данного источника не следует получать уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="61524-241">No change notifications should be received from this source.</span></span> <span data-ttu-id="61524-242">Обычно задается, только если исходный сервер находится на другом сайте.</span><span class="sxs-lookup"><span data-stu-id="61524-242">Usually set only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span data-ttu-id="61524-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**Службы каталогов \_ REPL \_ НБР \_ частичный \_ \_ набор атрибутов** (1073741824 (0x40000000))</span><span class="sxs-lookup"><span data-stu-id="61524-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS\_REPL\_NBR\_PARTIAL\_ATTRIBUTE\_SET** (1073741824 (0x40000000))</span></span>


</dt> <dd>

<span data-ttu-id="61524-244">Данный сосед находится в состоянии перестроения содержимого данной реплики из-за изменения в частичном наборе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="61524-244">This neighbor is in a state where it is rebuilding the contents of this replica because of a change in the partial attribute set.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="61524-245">**саурцедсааддресс**</span><span class="sxs-lookup"><span data-stu-id="61524-245">**SourceDsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-246">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-248">Возвращает DNS-адрес исходного контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="61524-248">Gets the DNS address of the source DC.</span></span>

> [!Note]  
> <span data-ttu-id="61524-249">Эта строка содержит измененный идентификатор GUID, а не часто используемое каноническое DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="61524-249">This string contains a modified GUID, not the commonly used canonical DNS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="61524-250">**саурцедсакн**</span><span class="sxs-lookup"><span data-stu-id="61524-250">**SourceDsaCN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-251">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-253">Возвращает компонент пути к объекту для DSA, представляющего исходный контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="61524-253">Gets the object path component for the DSA that represents the source DC.</span></span> <span data-ttu-id="61524-254">Эта строка часто похожа на имя компьютера, но не всегда идентична.</span><span class="sxs-lookup"><span data-stu-id="61524-254">This string is often similar to the computer name but is not always identical.</span></span>

</dd> <dt>

<span data-ttu-id="61524-255">**саурцедсадн**</span><span class="sxs-lookup"><span data-stu-id="61524-255">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-256">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-256">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-258">Возвращает путь X. 500 для DSA, представляющего исходный контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="61524-258">Gets the X.500 path for the DSA that represents the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="61524-259">**саурцедсаинвокатионид**</span><span class="sxs-lookup"><span data-stu-id="61524-259">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-260">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-260">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-262">Возвращает идентификатор вызова, который использовался исходным сервером на момент последней репликации.</span><span class="sxs-lookup"><span data-stu-id="61524-262">Gets the invocation ID that was used by the source server as of the last replication.</span></span>

</dd> <dt>

<span data-ttu-id="61524-263">**саурцедсаобжгуид**</span><span class="sxs-lookup"><span data-stu-id="61524-263">**SourceDsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-264">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61524-266">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61524-266">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61524-267">Возвращает идентификатор GUID для агента службы каталогов (DSA), который представляет исходный контроллер домена (DC).</span><span class="sxs-lookup"><span data-stu-id="61524-267">Gets the GUID for the directory service agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="61524-268">**саурцедсасите**</span><span class="sxs-lookup"><span data-stu-id="61524-268">**SourceDsaSite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-269">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="61524-269">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="61524-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-271">Возвращает сайт, содержащий исходный контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="61524-271">Gets the site that contains the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="61524-272">**синконстартуп**</span><span class="sxs-lookup"><span data-stu-id="61524-272">**SyncOnStartup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-273">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-275">Возвращает значение, указывающее, установлен ли в свойстве **репликафлагс** флаг **службы DS \_ REPL \_ НБР \_ Sync \_ On \_ Startup** .</span><span class="sxs-lookup"><span data-stu-id="61524-275">Gets the value that indicates whether the **DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-276">**тимеофластсинкаттемпт**</span><span class="sxs-lookup"><span data-stu-id="61524-276">**TimeOfLastSyncAttempt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-277">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61524-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="61524-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-279">Возвращает метку времени для последней попытки репликации.</span><span class="sxs-lookup"><span data-stu-id="61524-279">Gets the timestamp for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="61524-280">**тимеофластсинксукцесс**</span><span class="sxs-lookup"><span data-stu-id="61524-280">**TimeOfLastSyncSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-281">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61524-281">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="61524-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-283">Возвращает метку времени для последней успешной попытки репликации.</span><span class="sxs-lookup"><span data-stu-id="61524-283">Gets the timestamp for the last successful replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="61524-284">**твовайсинк**</span><span class="sxs-lookup"><span data-stu-id="61524-284">**TwoWaySync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-285">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-287">Возвращает значение, указывающее, установлен ли в свойстве **репликафлагс** флаг **\_ \_ \_ \_ \_ синхронизации DS REPL НБР Two** .</span><span class="sxs-lookup"><span data-stu-id="61524-287">Gets the value that indicates whether the **DS\_REPL\_NBR\_TWO\_WAY\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-288">**усеасинЦинтерситетранспорт**</span><span class="sxs-lookup"><span data-stu-id="61524-288">**UseAsyncIntersiteTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-289">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-291">Возвращает значение, указывающее, установлен ли в свойстве **репликафлагс** флаг **DS \_ REPL \_ НБР \_ USE \_ Async \_ межсайтового \_ транспорта** .</span><span class="sxs-lookup"><span data-stu-id="61524-291">Gets the value that indicates whether the **DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="61524-292">**уснаттрибутефилтер**</span><span class="sxs-lookup"><span data-stu-id="61524-292">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-293">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="61524-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="61524-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-295">Возвращает значение свойства **уснластобжчанжесинцед** в конце последнего успешного завершения цикла репликации.</span><span class="sxs-lookup"><span data-stu-id="61524-295">Gets the **USNLastObjChangeSynced** property value at the end of the last successful completed replication cycle.</span></span> <span data-ttu-id="61524-296">Нуль, если нет успешно завершенных циклов репликации.</span><span class="sxs-lookup"><span data-stu-id="61524-296">Zero if there were no successfully completed replication cycles.</span></span>

</dd> <dt>

<span data-ttu-id="61524-297">**уснластобжчанжесинцед**</span><span class="sxs-lookup"><span data-stu-id="61524-297">**USNLastObjChangeSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-298">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="61524-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="61524-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-300">Возвращает значение [**неизмененного**](/windows/desktop/ADSchema/a-usnchanged) атрибута последнего полученного обновления объекта.</span><span class="sxs-lookup"><span data-stu-id="61524-300">Gets the [**unchanged**](/windows/desktop/ADSchema/a-usnchanged) attribute value of the last object update that was received.</span></span>

</dd> <dt>

<span data-ttu-id="61524-301">**Writeable (Доступно для записи)**</span><span class="sxs-lookup"><span data-stu-id="61524-301">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61524-302">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="61524-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61524-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61524-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61524-304">Возвращает значение, указывающее, установлен ли флаг **DS \_ REPL \_ НБР \_ Write** в свойстве **репликафлагс** .</span><span class="sxs-lookup"><span data-stu-id="61524-304">Gets the value that indicates whether the **DS\_REPL\_NBR\_WRITEABLE** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61524-305">Требования</span><span class="sxs-lookup"><span data-stu-id="61524-305">Requirements</span></span>



| <span data-ttu-id="61524-306">Требование</span><span class="sxs-lookup"><span data-stu-id="61524-306">Requirement</span></span> | <span data-ttu-id="61524-307">Значение</span><span class="sxs-lookup"><span data-stu-id="61524-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61524-308">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61524-308">Minimum supported client</span></span><br/> | <span data-ttu-id="61524-309">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="61524-309">None supported</span></span><br/>                                                               |
| <span data-ttu-id="61524-310">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61524-310">Minimum supported server</span></span><br/> | <span data-ttu-id="61524-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61524-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61524-312">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="61524-312">Namespace</span></span><br/>                | <span data-ttu-id="61524-313">Корневой \\ микрософтактиведиректори</span><span class="sxs-lookup"><span data-stu-id="61524-313">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="61524-314">MOF</span><span class="sxs-lookup"><span data-stu-id="61524-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61524-315"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61524-315"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="61524-316">DLL</span><span class="sxs-lookup"><span data-stu-id="61524-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61524-317"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61524-317"><dt>Replprov.dll</dt></span></span> </dl> |



 

