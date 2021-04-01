---
description: KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии диспетчера транзакций (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Маски доступа диспетчера транзакций (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909184"
---
# <a name="transaction-manager-access-masks"></a><span data-ttu-id="8830f-103">Маски доступа диспетчера транзакций</span><span class="sxs-lookup"><span data-stu-id="8830f-103">Transaction Manager Access Masks</span></span>

<span data-ttu-id="8830f-104">KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии диспетчера транзакций (TM).</span><span class="sxs-lookup"><span data-stu-id="8830f-104">KTM defines the following enlistment access masks to be used when opening a transaction manager (TM).</span></span>

<dl> <dt>

<span data-ttu-id="8830f-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**\_сведения о запросе диспетчером транзакций \_**</span><span class="sxs-lookup"><span data-stu-id="8830f-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**TRANSACTIONMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-106">Номера 0x00001</span><span class="sxs-lookup"><span data-stu-id="8830f-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="8830f-107">Вызывающий объект может запросить сведения об этом TM.</span><span class="sxs-lookup"><span data-stu-id="8830f-107">The caller can query information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8830f-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**\_сведения о задании диспетчеров транзакций \_**</span><span class="sxs-lookup"><span data-stu-id="8830f-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="8830f-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="8830f-110">Вызывающий объект может задать сведения об этом TM.</span><span class="sxs-lookup"><span data-stu-id="8830f-110">The caller can set information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8830f-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**Восстановление ДИСПЕТЧЕРом транзакций \_**</span><span class="sxs-lookup"><span data-stu-id="8830f-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="8830f-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="8830f-113">Вызывающий объект может восстановить этот TM.</span><span class="sxs-lookup"><span data-stu-id="8830f-113">The caller can recover this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8830f-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**Переименование диспетчер транзакций \_**</span><span class="sxs-lookup"><span data-stu-id="8830f-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="8830f-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="8830f-116">Вызывающий объект может переименовать экземпляр TM.</span><span class="sxs-lookup"><span data-stu-id="8830f-116">The caller can rename a TM instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8830f-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**Диспетчер транзакций \_ создает \_ RM**</span><span class="sxs-lookup"><span data-stu-id="8830f-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER\_CREATE\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-118">0x00010</span><span class="sxs-lookup"><span data-stu-id="8830f-118">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="8830f-119">Вызывающий объект может создать диспетчер ресурсов, связанный с этим TM.</span><span class="sxs-lookup"><span data-stu-id="8830f-119">The caller can create a resource manager that is associated with this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8830f-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**\_транзакция привязки \_ транзакции транзакций**</span><span class="sxs-lookup"><span data-stu-id="8830f-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER\_BIND\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-121">0x00020</span><span class="sxs-lookup"><span data-stu-id="8830f-121">0x00020</span></span>
</dt> <dt>



<span data-ttu-id="8830f-122">Это значение зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="8830f-122">This value is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8830f-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**\_универсальное чтение с диспетчером транзакций \_**</span><span class="sxs-lookup"><span data-stu-id="8830f-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**TRANSACTIONMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-124">0x20001</span><span class="sxs-lookup"><span data-stu-id="8830f-124">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="8830f-125">Вызывающий объект имеет следующие привилегии: **стандартные \_ права \_ Чтение** и **Диспетчер транзакций, \_ \_ сведения о запросах**.</span><span class="sxs-lookup"><span data-stu-id="8830f-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **TRANSACTIONMANAGER\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8830f-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**\_Общая \_ запись в диспетчер транзакций**</span><span class="sxs-lookup"><span data-stu-id="8830f-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-127">0x2001E</span><span class="sxs-lookup"><span data-stu-id="8830f-127">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="8830f-128">Вызывающий объект имеет следующие привилегии **: \_ стандартные \_ права записи**, диспетчер транзакций, **\_ \_ сведения о задании**, **\_ Восстановление**, диспетчер **транзакций \_** и **\_ Создание \_ RM**.</span><span class="sxs-lookup"><span data-stu-id="8830f-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTIONMANAGER\_SET\_INFORMATION**, **TRANSACTIONMANAGER\_RECOVER**, **TRANSACTIONMANAGER\_RENAME**, and **TRANSACTIONMANAGER\_CREATE\_RM**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8830f-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**\_универсальное выполнение диспетчером транзакций \_**</span><span class="sxs-lookup"><span data-stu-id="8830f-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-130">0x20000</span><span class="sxs-lookup"><span data-stu-id="8830f-130">0x20000</span></span>
</dt> <dt>



<span data-ttu-id="8830f-131">Вызывающий объект имеет следующие привилегии: **стандартные \_ права \_ выполнения**.</span><span class="sxs-lookup"><span data-stu-id="8830f-131">The caller has the following privilege: **STANDARD\_RIGHTS\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8830f-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**Диспетчер транзакций \_ все \_ доступ**</span><span class="sxs-lookup"><span data-stu-id="8830f-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8830f-133">0xF003F</span><span class="sxs-lookup"><span data-stu-id="8830f-133">0xF003F</span></span>
</dt> <dt>



<span data-ttu-id="8830f-134">Это значение задает все допустимые биты для значения доступа TM.</span><span class="sxs-lookup"><span data-stu-id="8830f-134">This value sets all valid bits for a TM access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8830f-135">Требования</span><span class="sxs-lookup"><span data-stu-id="8830f-135">Requirements</span></span>



| <span data-ttu-id="8830f-136">Требование</span><span class="sxs-lookup"><span data-stu-id="8830f-136">Requirement</span></span> | <span data-ttu-id="8830f-137">Значение</span><span class="sxs-lookup"><span data-stu-id="8830f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8830f-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8830f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8830f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8830f-139">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="8830f-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8830f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8830f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8830f-141">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="8830f-142">Header</span><span class="sxs-lookup"><span data-stu-id="8830f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8830f-143"><dt>Файл WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="8830f-143"><dt>WinNT.h</dt></span></span> </dl> |



 

 




