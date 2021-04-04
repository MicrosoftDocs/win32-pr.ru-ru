---
title: Идентификаторы доступа (Фвпму. h)
description: Платформа фильтрации Windows (WFP) использует стандартные права доступа Win32, а также набор специальных прав доступа для конкретных платформ, встроенных в платформу фильтрации.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989326"
---
# <a name="access-right-identifiers"></a><span data-ttu-id="7fcf5-103">Идентификаторы прав доступа</span><span class="sxs-lookup"><span data-stu-id="7fcf5-103">Access Right Identifiers</span></span>

<span data-ttu-id="7fcf5-104">Платформа фильтрации Windows (WFP) использует [стандартные права доступа Win32](/windows/desktop/SecAuthZ/standard-access-rights) , а также набор специальных прав доступа для конкретных платформ, встроенных в платформу фильтрации.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-104">Windows Filtering Platform (WFP) uses the [standard Win32 access rights](/windows/desktop/SecAuthZ/standard-access-rights) plus a set of WFP-specific access rights built into the filtering platform.</span></span> <span data-ttu-id="7fcf5-105">Эти права доступа используются для защиты объектов только в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-105">These access rights are used to secure objects in user mode only.</span></span> <span data-ttu-id="7fcf5-106">Вызывающие объекты режима ядра обходят все проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-106">Kernel-mode callers bypass all access checks.</span></span>

<span data-ttu-id="7fcf5-107">Идентификаторы прав доступа, специфические для WFP, приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-107">WFP specific access right identifiers are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="7fcf5-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**\_Добавление фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-109">Добавьте объект в модуль базовой фильтрации (BFE).</span><span class="sxs-lookup"><span data-stu-id="7fcf5-109">Add an object to the Base Filtering Engine (BFE).</span></span> <span data-ttu-id="7fcf5-110">Это право доступа требуется для вызова функций [**\* Add0 фвпм**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .</span><span class="sxs-lookup"><span data-stu-id="7fcf5-110">This access right is needed in order to call [**Fwpm\*Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**ФВПМ \_ актрл \_ Добавить \_ ссылку**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-112">Добавьте объект, на который ссылается ссылка.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-112">Add an object referenced through a link.</span></span> <span data-ttu-id="7fcf5-113">Например, это право доступа требуется для вызовов, на которые ссылаются с помощью идентификаторов GUID.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-113">For example, this access right is needed for callouts referenced through GUIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**ФВПМ \_ актрл \_ Начало \_ чтения \_ транзакция**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-115">Начать транзакцию только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-115">Begin a read-only transaction.</span></span> <span data-ttu-id="7fcf5-116">Это право доступа необходимо для вызова [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span><span class="sxs-lookup"><span data-stu-id="7fcf5-116">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**ФВПМ \_ актрл \_ начать \_ запись \_ транзакция**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-118">Начать транзакцию для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-118">Begin a read/write transaction.</span></span> <span data-ttu-id="7fcf5-119">Это право доступа необходимо для вызова [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) для транзакции чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-119">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) for a read/write transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_классификация фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-121">Классификация удаленного вызова процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="7fcf5-121">Classify Remote Procedure Call (RPC).</span></span> <span data-ttu-id="7fcf5-122">Это право доступа требуется во время выполнения RPC, чтобы применить фильтры RPC.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-122">This access right is needed by the RPC run-time in order to enforce RPC filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**\_перечисление АКТРЛ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-124">Перечислить.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-124">Enumerate.</span></span> <span data-ttu-id="7fcf5-125">Это право доступа требуется для вызова функций [**\* CreateEnumHandle0 фвпм**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) .</span><span class="sxs-lookup"><span data-stu-id="7fcf5-125">This access right is needed in order to call [**Fwpm\*CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) functions.</span></span> <span data-ttu-id="7fcf5-126">Чтобы перечислить объект, вызывающему объекту также требуется ФВПМ \_ актрл \_ доступ для чтения к объекту.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-126">To enumerate an object, the caller also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**ФВПМ \_ актрл \_ Open**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-128">Откройте сеанс с обработчиком фильтров.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-128">Open a session to the filter engine.</span></span> <span data-ttu-id="7fcf5-129">Это право доступа необходимо для вызова [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="7fcf5-129">This access right is needed in order to call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**\_Чтение фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-131">доступ для чтения;</span><span class="sxs-lookup"><span data-stu-id="7fcf5-131">Read.</span></span> <span data-ttu-id="7fcf5-132">Это право доступа требуется для вызова функций [**фвпм \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) и [**фвпм \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .</span><span class="sxs-lookup"><span data-stu-id="7fcf5-132">This access right is needed in order to call [**Fwpm\*GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) and [**Fwpm\*GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_ \_ Статистика чтения фвпм \_ актрл**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-134">Чтение статистики.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-134">Read statistics.</span></span> <span data-ttu-id="7fcf5-135">Это право доступа необходимо для вызова [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) и [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span><span class="sxs-lookup"><span data-stu-id="7fcf5-135">This access right is needed in order to call [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) and [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**\_Подписка фвпм актрл \_**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-137">Оформите подписку.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-137">Subscribe.</span></span> <span data-ttu-id="7fcf5-138">Это право доступа требуется для вызова функций [**\* SubscribeChanges0 фвпм**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) .</span><span class="sxs-lookup"><span data-stu-id="7fcf5-138">This access right is needed in order to call [**Fwpm\*SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) functions.</span></span> <span data-ttu-id="7fcf5-139">Чтобы получить уведомление для объекта, подписчику также требуется ФВПМ \_ актрл \_ доступ для чтения к объекту.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-139">To receive a notification for an object, a subscriber also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**ФВПМ \_ актрл \_ запись**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-141">Параметры модуля записи.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-141">Write engine options.</span></span> <span data-ttu-id="7fcf5-142">Это право доступа необходимо для вызова [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span><span class="sxs-lookup"><span data-stu-id="7fcf5-142">This access right is needed in order to call [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**ФВПМ \_ универсальное \_ чтение**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-144">СТАНДАРТНЫЕ \_ права \_ Чтение \| фвпм \_ актрл \_ Начало \_ чтения \_ транзакция \| фвпм \_ актрл \_ классификация \| фвпм \_ актрл \_ Open \| фвпм \_ актрл \_ Read \| фвпм \_ актрл \_ Read \_ stats</span><span class="sxs-lookup"><span data-stu-id="7fcf5-144">STANDARD\_RIGHTS\_READ \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**ФВПМ \_ универсальное \_ выполнение**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-146">СТАНДАРТНЫЕ \_ права \_ выполнить \| фвпм \_ актрл \_ Enum \| фвпм \_ актрл \_ Subscribe</span><span class="sxs-lookup"><span data-stu-id="7fcf5-146">STANDARD\_RIGHTS\_EXECUTE \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_SUBSCRIBE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**ФВПМ \_ Универсальная \_ запись**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**FWPM\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-148">\_права на \_ запись \| Удаление \| фвпм \_ актрл \_ Добавить \| фвпм \_ актрл \_ Add \_ Link \| фвпм \_ актрл \_ Начало \_ записи \_ транзакция \| фвпм \_ актрл \_ Write</span><span class="sxs-lookup"><span data-stu-id="7fcf5-148">STANDARD\_RIGHTS\_WRITE \| DELETE \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7fcf5-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**ФВПМ \_ Общие \_ все**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM\_GENERIC\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7fcf5-150">для стандартных \_ прав \_ требуются \| фвпм \_ актрл \_ Add \| фвпм \_ актрл \_ Add \_ Link \| фвпм \_ актрл \_ Начало \_ чтения \_ транзакция \| фвпм \_ актрл \_ Begin \_ Write \_ транзакция \| фвпм \_ актрл \_ классифицировать \| фвпм \_ актрл \_ Enum \| фвпм \_ актрл \_ Open \| фвпм \_ актрл \_ Read \| фвпм \_ ACTRL \_ Read \_ stats \| FWPM \_ ACTRL \_ Subscribe \| FWPM \_ ACTRL \_ Write</span><span class="sxs-lookup"><span data-stu-id="7fcf5-150">STANDARD\_RIGHTS\_REQUIRED \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS \| FWPM\_ACTRL\_SUBSCRIBE \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fcf5-151">Требования</span><span class="sxs-lookup"><span data-stu-id="7fcf5-151">Requirements</span></span>



| <span data-ttu-id="7fcf5-152">Требование</span><span class="sxs-lookup"><span data-stu-id="7fcf5-152">Requirement</span></span> | <span data-ttu-id="7fcf5-153">Значение</span><span class="sxs-lookup"><span data-stu-id="7fcf5-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcf5-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fcf5-154">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcf5-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fcf5-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7fcf5-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fcf5-156">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcf5-157">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7fcf5-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7fcf5-158">Header</span><span class="sxs-lookup"><span data-stu-id="7fcf5-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fcf5-159"><dt>Фвпму. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fcf5-159"><dt>Fwpmu.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcf5-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fcf5-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcf5-161">Модель контроля доступа платформы фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="7fcf5-161">Windows Filtering Platform Access Control Model</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="7fcf5-162">Стандартные права доступа</span><span class="sxs-lookup"><span data-stu-id="7fcf5-162">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

