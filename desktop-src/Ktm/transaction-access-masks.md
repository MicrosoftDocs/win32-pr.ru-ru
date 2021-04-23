---
description: KTM определяет следующие маски доступа к транзакциям, которые будут использоваться при открытии транзакции.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Маски доступа транзакций (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673601"
---
# <a name="transaction-access-masks"></a><span data-ttu-id="ae2ff-103">Маски доступа транзакций</span><span class="sxs-lookup"><span data-stu-id="ae2ff-103">Transaction Access Masks</span></span>

<span data-ttu-id="ae2ff-104">KTM определяет следующие маски доступа к транзакциям, которые будут использоваться при открытии транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-104">KTM defines the following transaction access masks to be used when opening a transaction.</span></span>

<dl> <dt>

<span data-ttu-id="ae2ff-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_ \_ сведения о запросе транзакции**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**TRANSACTION\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-106">0x000001</span><span class="sxs-lookup"><span data-stu-id="ae2ff-106">0x000001</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-107">Вызывающий объект может запрашивать сведения о транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-107">The caller can query transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_сведения о наборе транзакций \_**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**TRANSACTION\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-109">0x000002</span><span class="sxs-lookup"><span data-stu-id="ae2ff-109">0x000002</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-110">Вызывающий объект может задавать сведения о транзакциях.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-110">The caller can set transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**прикрепление транзакции \_**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-112">0x000004</span><span class="sxs-lookup"><span data-stu-id="ae2ff-112">0x000004</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-113">Вызывающий объект может быть прикреплен в этой транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-113">The caller can enlist in this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**\_фиксация транзакции**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**TRANSACTION\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-115">0x000008</span><span class="sxs-lookup"><span data-stu-id="ae2ff-115">0x000008</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-116">Вызывающий объект может зафиксировать эту транзакцию.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-116">The caller can commit this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**\_откат транзакции**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**TRANSACTION\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-118">0x000010</span><span class="sxs-lookup"><span data-stu-id="ae2ff-118">0x000010</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-119">Вызывающий объект может выполнить откат этой транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-119">The caller can roll back this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**\_распространение транзакции**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**TRANSACTION\_PROPAGATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-121">0x000020</span><span class="sxs-lookup"><span data-stu-id="ae2ff-121">0x000020</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-122">Вызывающий объект может распространить эту транзакцию на старший диспетчер ресурсов, например координатор распределенных транзакций (DTC).</span><span class="sxs-lookup"><span data-stu-id="ae2ff-122">The caller can propagate this transaction to a superior resource manager, such as the Distributed Transaction Coordinator (DTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_Общее \_ Чтение транзакции**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**TRANSACTION\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-124">0x120001</span><span class="sxs-lookup"><span data-stu-id="ae2ff-124">0x120001</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-125">Вызывающий объект имеет следующие привилегии: **стандартные \_ права на \_ Чтение**, **\_ \_ сведения о запросе транзакции** и **синхронизацию**.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ**, **TRANSACTION\_QUERY\_INFORMATION**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_Общая транзакция \_ записи**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**TRANSACTION\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-127">0x12003E</span><span class="sxs-lookup"><span data-stu-id="ae2ff-127">0x12003E</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-128">Вызывающий объект имеет следующие привилегии **: стандартные \_ права на \_ запись**, **\_ \_ сведения о наборе** транзакций, **\_ фиксацию транзакции**, **\_ Прикрепление** транзакций, **\_ откат транзакций**, **\_ Распространение транзакций** и **синхронизацию**.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ENLIST**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**ТРАНЗАКЦИЯ \_ общего \_ выполнения**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-130">0x120018</span><span class="sxs-lookup"><span data-stu-id="ae2ff-130">0x120018</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-131">Вызывающий объект имеет следующие права: **\_ \_ выполнение стандартных прав**, **\_ фиксация транзакции**, **\_ откат транзакции** и **Синхронизация**.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-131">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ROLLBACK**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**ТРАНЗАКЦИЯ \_ все \_ доступ**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-133">0x12003F</span><span class="sxs-lookup"><span data-stu-id="ae2ff-133">0x12003F</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-134">Вызывающий объект имеет следующие привилегии **: \_ \_ требования** уровня "Стандартный", " **транзакция \_ общего \_ чтения**", " **\_ Общая операция \_ записи**" и " **транзакция \_ общего \_ выполнения**".</span><span class="sxs-lookup"><span data-stu-id="ae2ff-134">The caller has the following privilege: **STANDARD\_RIGHTS\_REQUIRED**, **TRANSACTION\_GENERIC\_READ**, **TRANSACTION\_GENERIC\_WRITE**, and **TRANSACTION\_GENERIC\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ae2ff-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**\_ \_ права ДИСПЕТЧЕРА ресурсов \_ транзакций**</span><span class="sxs-lookup"><span data-stu-id="ae2ff-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2ff-136">0x120037</span><span class="sxs-lookup"><span data-stu-id="ae2ff-136">0x120037</span></span>
</dt> <dt>



<span data-ttu-id="ae2ff-137">Вызывающий объект имеет следующие права: **\_ Общее \_ Чтение транзакции**, **\_ \_ запись стандартных прав**, **\_ \_ сведения о наборе** транзакций, **\_ откат транзакции**, **\_ прикрепление транзакции**, **\_ распространение транзакции** и **синхронизацию**.</span><span class="sxs-lookup"><span data-stu-id="ae2ff-137">The caller has the following privileges: **TRANSACTION\_GENERIC\_READ**, **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_ENLIST**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae2ff-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae2ff-138">Remarks</span></span>

<span data-ttu-id="ae2ff-139">При открытии транзакции рекомендуется использовать диспетчеры ресурсов при прикреплении транзакции, а также **указывать \_ \_ \_ права диспетчера ресурсов транзакций** .</span><span class="sxs-lookup"><span data-stu-id="ae2ff-139">It is recommended that resource managers, when enlisting in a transaction, specify **TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS** when opening a transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2ff-140">Требования</span><span class="sxs-lookup"><span data-stu-id="ae2ff-140">Requirements</span></span>



| <span data-ttu-id="ae2ff-141">Требование</span><span class="sxs-lookup"><span data-stu-id="ae2ff-141">Requirement</span></span> | <span data-ttu-id="ae2ff-142">Значение</span><span class="sxs-lookup"><span data-stu-id="ae2ff-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2ff-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae2ff-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2ff-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae2ff-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="ae2ff-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae2ff-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2ff-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae2ff-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="ae2ff-147">Header</span><span class="sxs-lookup"><span data-stu-id="ae2ff-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2ff-148"><dt>Файл WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ff-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




