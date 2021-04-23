---
title: Класс MSAD_ReplPendingOp
description: Представляет \_ \_ структуру Op REPL DS, которая описывает задачу репликации, которая выполняется в данный момент или ожидает выполнения.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- Класс MSAD_ReplPendingOp Active Directory
- Active Directory класса MSAD_ReplPendingOp, описание
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415556"
---
# <a name="msad_replpendingop-class"></a><span data-ttu-id="9576f-105">\_Класс МСАД реплпендингоп</span><span class="sxs-lookup"><span data-stu-id="9576f-105">MSAD\_ReplPendingOp class</span></span>

<span data-ttu-id="9576f-106">Представляет структуру [**\_ \_ Op REPL DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , которая описывает задачу репликации, которая выполняется в данный момент или ожидает выполнения.</span><span class="sxs-lookup"><span data-stu-id="9576f-106">Represents the [**DS\_REPL\_OP**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) structure, which describes a replication task that is currently executing or pending execution.</span></span> <span data-ttu-id="9576f-107">Эта структура возвращается функцией [**дсрепликажетинфо**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .</span><span class="sxs-lookup"><span data-stu-id="9576f-107">This structure is returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9576f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9576f-108">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a><span data-ttu-id="9576f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="9576f-109">Members</span></span>

<span data-ttu-id="9576f-110">Класс **МСАД \_ реплпендингоп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9576f-110">The **MSAD\_ReplPendingOp** class has these types of members:</span></span>

-   [<span data-ttu-id="9576f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9576f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9576f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9576f-112">Properties</span></span>

<span data-ttu-id="9576f-113">Класс **МСАД \_ реплпендингоп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9576f-113">The **MSAD\_ReplPendingOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9576f-114">**дсааддресс**</span><span class="sxs-lookup"><span data-stu-id="9576f-114">**DsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9576f-115">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-117">Возвращает сетевой адрес удаленного сервера, связанного с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="9576f-117">Gets the transport-specific network address of the remote server that is associated with this operation.</span></span> <span data-ttu-id="9576f-118">**Значение NULL** , если отсутствует удаленный сервер, связанный с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="9576f-118">**NULL** if there is no remote server that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-119">**дсадн**</span><span class="sxs-lookup"><span data-stu-id="9576f-119">**DsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9576f-120">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-122">Возвращает путь к DSA X. 500, связанному с удаленным сервером, который соответствует этой операции.</span><span class="sxs-lookup"><span data-stu-id="9576f-122">Gets the X.500 path of the DSA that is associated with the remote server that corresponds to this operation.</span></span> <span data-ttu-id="9576f-123">**Значение NULL** , если ни один удаленный сервер не соответствует этой операции.</span><span class="sxs-lookup"><span data-stu-id="9576f-123">**NULL** if no remote server corresponds to this operation.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-124">**дсаобжгуид**</span><span class="sxs-lookup"><span data-stu-id="9576f-124">**DsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9576f-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-127">Возвращает значение атрибута [**OBJECTGUID**](/windows/desktop/ADSchema/a-objectguid) DSA, идентифицируемого свойством **дсадн** .</span><span class="sxs-lookup"><span data-stu-id="9576f-127">Gets the value of the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the DSA that is identified by the **DsaDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-128">**намингконтекстдн**</span><span class="sxs-lookup"><span data-stu-id="9576f-128">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9576f-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-131">Возвращает путь X. 500 контекста именования (NC), связанного с данной операцией.</span><span class="sxs-lookup"><span data-stu-id="9576f-131">Gets the X.500 path of the naming context (NC) that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-132">**намингконтекстобжгуид**</span><span class="sxs-lookup"><span data-stu-id="9576f-132">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9576f-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-135">Возвращает атрибут [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) сетевого контекста, идентифицируемого свойством **намингконтекстдн** .</span><span class="sxs-lookup"><span data-stu-id="9576f-135">Gets the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the NC that is identified by the **NamingContextDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-136">**опстарттиме**</span><span class="sxs-lookup"><span data-stu-id="9576f-136">**OpStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-137">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9576f-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-139">Возвращает время начала операции.</span><span class="sxs-lookup"><span data-stu-id="9576f-139">Gets the time when the operation was started.</span></span> <span data-ttu-id="9576f-140">**Значение NULL** , если эта операция все еще находится в очереди.</span><span class="sxs-lookup"><span data-stu-id="9576f-140">**NULL** if this operation is still in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-141">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="9576f-141">**Options**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9576f-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-144">Возвращает набор флагов, которые предоставляют дополнительные данные об операции.</span><span class="sxs-lookup"><span data-stu-id="9576f-144">Gets the set of flags that provides additional data about the operation.</span></span> <span data-ttu-id="9576f-145">Содержимое этого элемента определяется значением свойства **OpType** .</span><span class="sxs-lookup"><span data-stu-id="9576f-145">The contents of this member are determined by the value of the **OpType** property.</span></span>

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span data-ttu-id="9576f-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_ \_ \_ Синхронизация типа операции DS \_ REPL**</span><span class="sxs-lookup"><span data-stu-id="9576f-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS\_REPL\_OP\_TYPE\_SYNC**</span></span>


</dt> <dd>

<span data-ttu-id="9576f-147">Содержит ноль или сочетание одного или нескольких значений \**DS \_ \_ \* репсинк* _, как определено для параметра _Options \* в [**дсрепликасинк**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span><span class="sxs-lookup"><span data-stu-id="9576f-147">Contains zero or a combination of one or more of the **DS\_REPSYNC\_\** _ values as defined for the _Options* parameter in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span data-ttu-id="9576f-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**\_ \_ \_ Добавление типа Op в DS REPL \_**</span><span class="sxs-lookup"><span data-stu-id="9576f-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS\_REPL\_OP\_TYPE\_ADD**</span></span>


</dt> <dd>

<span data-ttu-id="9576f-149">Содержит ноль или комбинацию одного или нескольких значений \**DS \_ \_ \* repadd*, определенных для параметра _Options \* в [**дсрепликаадд**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span><span class="sxs-lookup"><span data-stu-id="9576f-149">Contains zero or a combination of one or more of the **DS\_REPADD\_\** _ values as defined for the _Options* parameter in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span data-ttu-id="9576f-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**\_ \_ операция \_ \_ удаления типа операции DS REPL**</span><span class="sxs-lookup"><span data-stu-id="9576f-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS\_REPL\_OP\_TYPE\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="9576f-151">Содержит ноль или сочетание одного или нескольких значений \**DS \_ \_ \* репдел* _, как определено для параметра _Options \* в [**дсрепликадел**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span><span class="sxs-lookup"><span data-stu-id="9576f-151">Contains zero or a combination of one or more of the **DS\_REPDEL\_\** _ values as defined for the _Options* parameter in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span data-ttu-id="9576f-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS \_ REPL \_ , \_ изменение типа Op \_**</span><span class="sxs-lookup"><span data-stu-id="9576f-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS\_REPL\_OP\_TYPE\_MODIFY**</span></span>


</dt> <dd>

<span data-ttu-id="9576f-153">Содержит ноль или сочетание одного или нескольких значений \**DS \_ \_ \* репмод* _, как определено для параметра _Options \* в [**дсрепликамодифи**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span><span class="sxs-lookup"><span data-stu-id="9576f-153">Contains zero or a combination of one or more of the **DS\_REPMOD\_\** _ values as defined for the _Options* parameter in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span data-ttu-id="9576f-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_ссылки для \_ \_ обновления типа \_ \_ операций DS REPL**</span><span class="sxs-lookup"><span data-stu-id="9576f-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS\_REPL\_OP\_TYPE\_UPDATE\_REFS**</span></span>


</dt> <dd>

<span data-ttu-id="9576f-155">Содержит ноль или сочетание одного или нескольких значений \**DS \_ \_ \* репсупд* _, как определено для параметра _Options \* в [**дсрепликаупдатерефс**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span><span class="sxs-lookup"><span data-stu-id="9576f-155">Contains zero or a combination of one or more of the **DS\_REPSUPD\_\** _ values as defined for the _Options* parameter in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9576f-156">**OpType**</span><span class="sxs-lookup"><span data-stu-id="9576f-156">**OpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9576f-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-159">Возвращает значение [**\_ \_ \_ типа Op REPL**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) , которое указывает тип операции, представляемой этим классом.</span><span class="sxs-lookup"><span data-stu-id="9576f-159">Gets the [**DS\_REPL\_OP\_TYPE**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) value that indicates the type of operation that this class represents.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-160">**поситионинк**</span><span class="sxs-lookup"><span data-stu-id="9576f-160">**PositionInQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-161">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9576f-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-163">Возвращает расположение этой операции в очереди.</span><span class="sxs-lookup"><span data-stu-id="9576f-163">Gets the position of this operation in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-164">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="9576f-164">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9576f-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-167">Возвращает приоритет этой операции.</span><span class="sxs-lookup"><span data-stu-id="9576f-167">Gets the priority of this operation.</span></span> <span data-ttu-id="9576f-168">Задачи с более высоким приоритетом выполняются первыми.</span><span class="sxs-lookup"><span data-stu-id="9576f-168">Higher-priority tasks are executed first.</span></span> <span data-ttu-id="9576f-169">Приоритет вычисляется сервером в зависимости от типа операции, представляемой этим классом, и параметров операции.</span><span class="sxs-lookup"><span data-stu-id="9576f-169">The priority is calculated by the server based on the type of operation that this class represents and the parameters of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-170">**Номер**</span><span class="sxs-lookup"><span data-stu-id="9576f-170">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-171">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9576f-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9576f-173">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9576f-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9576f-174">Возвращает идентификатор операции, уникальный для каждого компьютера и для каждой загрузки.</span><span class="sxs-lookup"><span data-stu-id="9576f-174">Gets the ID of the operation, which is unique per-machine and per-boot.</span></span>

</dd> <dt>

<span data-ttu-id="9576f-175">**тиминкуеуед**</span><span class="sxs-lookup"><span data-stu-id="9576f-175">**TimeEnqueued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9576f-176">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9576f-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9576f-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9576f-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9576f-178">Возвращает время, когда эта операция была добавлена в очередь.</span><span class="sxs-lookup"><span data-stu-id="9576f-178">Gets the time at which this operation was added to the queue.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9576f-179">Требования</span><span class="sxs-lookup"><span data-stu-id="9576f-179">Requirements</span></span>



| <span data-ttu-id="9576f-180">Требование</span><span class="sxs-lookup"><span data-stu-id="9576f-180">Requirement</span></span> | <span data-ttu-id="9576f-181">Значение</span><span class="sxs-lookup"><span data-stu-id="9576f-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9576f-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9576f-182">Minimum supported client</span></span><br/> | <span data-ttu-id="9576f-183">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9576f-183">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9576f-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9576f-184">Minimum supported server</span></span><br/> | <span data-ttu-id="9576f-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9576f-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9576f-186">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9576f-186">Namespace</span></span><br/>                | <span data-ttu-id="9576f-187">Корневой \\ микрософтактиведиректори</span><span class="sxs-lookup"><span data-stu-id="9576f-187">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="9576f-188">MOF</span><span class="sxs-lookup"><span data-stu-id="9576f-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9576f-189"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9576f-189"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="9576f-190">DLL</span><span class="sxs-lookup"><span data-stu-id="9576f-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9576f-191"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9576f-191"><dt>Replprov.dll</dt></span></span> </dl> |



 

