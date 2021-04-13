---
title: Коды ошибок WFP (Winerror.h)
description: (WFP) коды ошибок.
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491727"
---
# <a name="wfp-error-codes"></a><span data-ttu-id="a8b68-103">Коды ошибок WFP</span><span class="sxs-lookup"><span data-stu-id="a8b68-103">WFP Error Codes</span></span>

<span data-ttu-id="a8b68-104">Коды ошибок, характерные для платформы фильтрации Windows (WFP), приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="a8b68-104">Windows Filtering Platform (WFP) specific error codes are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="a8b68-105"><span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**\_ \_ выноска FWP \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="a8b68-105"><span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**FWP\_E\_CALLOUT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-106">0x80320001</span><span class="sxs-lookup"><span data-stu-id="a8b68-106">0x80320001</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-107">Выноска не существует.</span><span class="sxs-lookup"><span data-stu-id="a8b68-107">The callout does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-108"><span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**\_условие FWP \_ E \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="a8b68-108"><span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**FWP\_E\_CONDITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-109">0x80320002</span><span class="sxs-lookup"><span data-stu-id="a8b68-109">0x80320002</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-110">Условие фильтра не существует.</span><span class="sxs-lookup"><span data-stu-id="a8b68-110">The filter condition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-111"><span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_Фильтр FWP \_ E \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="a8b68-111"><span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**FWP\_E\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-112">0x80320003</span><span class="sxs-lookup"><span data-stu-id="a8b68-112">0x80320003</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-113">Фильтр не существует.</span><span class="sxs-lookup"><span data-stu-id="a8b68-113">The filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-114"><span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**\_слой FWP \_ E \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="a8b68-114"><span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**FWP\_E\_LAYER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-115">0x80320004</span><span class="sxs-lookup"><span data-stu-id="a8b68-115">0x80320004</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-116">Слой не существует.</span><span class="sxs-lookup"><span data-stu-id="a8b68-116">The layer does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-117"><span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**\_поставщик FWP \_ E \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="a8b68-117"><span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**FWP\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-118">0x80320005</span><span class="sxs-lookup"><span data-stu-id="a8b68-118">0x80320005</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-119">Поставщик не существует.</span><span class="sxs-lookup"><span data-stu-id="a8b68-119">The provider does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-120"><span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**\_ \_ \_ \_ не \_ найден контекст поставщика FWP E**</span><span class="sxs-lookup"><span data-stu-id="a8b68-120"><span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**FWP\_E\_PROVIDER\_CONTEXT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-121">0x80320006</span><span class="sxs-lookup"><span data-stu-id="a8b68-121">0x80320006</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-122">Контекст поставщика не существует.</span><span class="sxs-lookup"><span data-stu-id="a8b68-122">The provider context does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-123"><span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**подслой FWP \_ E \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="a8b68-123"><span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**FWP\_E\_SUBLAYER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-124">0x80320007</span><span class="sxs-lookup"><span data-stu-id="a8b68-124">0x80320007</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-125">Подуровень не существует.</span><span class="sxs-lookup"><span data-stu-id="a8b68-125">The sub-layer does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-126"><span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP \_ E \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="a8b68-126"><span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-127">0x80320008</span><span class="sxs-lookup"><span data-stu-id="a8b68-127">0x80320008</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-128">Объект не существует.</span><span class="sxs-lookup"><span data-stu-id="a8b68-128">The object does not exist.</span></span>

<span data-ttu-id="a8b68-129">Функции [ипсексаконтекст \* ](fwp-ipsec-functions.md) возвращают эту ошибку, если идентификатор контекста SA не найден.</span><span class="sxs-lookup"><span data-stu-id="a8b68-129">The [IPsecSaContext\*](fwp-ipsec-functions.md) functions return this error if the SA context ID is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-130"><span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP \_ E \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="a8b68-130"><span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-131">0x80320009</span><span class="sxs-lookup"><span data-stu-id="a8b68-131">0x80320009</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-132">Объект с таким GUID или LUID уже существует.</span><span class="sxs-lookup"><span data-stu-id="a8b68-132">An object with that GUID or LUID already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-133"><span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**\_используется FWP \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-133"><span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP\_E\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-134">0x8032000A</span><span class="sxs-lookup"><span data-stu-id="a8b68-134">0x8032000A</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-135">На объект ссылаются другие объекты, поэтому его нельзя удалить.</span><span class="sxs-lookup"><span data-stu-id="a8b68-135">The object is referenced by other objects, so it cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-136"><span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**\_ \_ \_ выполняется динамический сеанс \_ \_ FWP E**</span><span class="sxs-lookup"><span data-stu-id="a8b68-136"><span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**FWP\_E\_DYNAMIC\_SESSION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-137">0x8032000B</span><span class="sxs-lookup"><span data-stu-id="a8b68-137">0x8032000B</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-138">В динамическом сеансе вызов не разрешен.</span><span class="sxs-lookup"><span data-stu-id="a8b68-138">The call is not allowed from within a dynamic session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-139"><span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP \_ \_ неверного \_ сеанса**</span><span class="sxs-lookup"><span data-stu-id="a8b68-139"><span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP\_E\_WRONG\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-140">0x8032000C</span><span class="sxs-lookup"><span data-stu-id="a8b68-140">0x8032000C</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-141">Вызов был сделан из неверного сеанса, поэтому его невозможно завершить.</span><span class="sxs-lookup"><span data-stu-id="a8b68-141">The call was made from the wrong session, so it cannot be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-142"><span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ е \_ \_ транзакция не \_ \_ выполняется**</span><span class="sxs-lookup"><span data-stu-id="a8b68-142"><span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP\_E\_NO\_TXN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-143">0x8032000D</span><span class="sxs-lookup"><span data-stu-id="a8b68-143">0x8032000D</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-144">Вызов должен быть выполнен в явной транзакции.</span><span class="sxs-lookup"><span data-stu-id="a8b68-144">The call must be made from within an explicit transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-145"><span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**\_выполняется FWP E \_ транзакция \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-145"><span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP\_E\_TXN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-146">0x8032000E</span><span class="sxs-lookup"><span data-stu-id="a8b68-146">0x8032000E</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-147">Вызов не разрешен в явной транзакции.</span><span class="sxs-lookup"><span data-stu-id="a8b68-147">The call is not allowed from within an explicit transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-148"><span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ транзакция \_ прервано**</span><span class="sxs-lookup"><span data-stu-id="a8b68-148"><span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP\_E\_TXN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-149">0x8032000F</span><span class="sxs-lookup"><span data-stu-id="a8b68-149">0x8032000F</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-150">Явная транзакция была принудительно отменена.</span><span class="sxs-lookup"><span data-stu-id="a8b68-150">The explicit transaction has been forcibly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-151"><span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**\_сеанс FWP \_ E \_ прерван**</span><span class="sxs-lookup"><span data-stu-id="a8b68-151"><span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**FWP\_E\_SESSION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-152">0x80320010</span><span class="sxs-lookup"><span data-stu-id="a8b68-152">0x80320010</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-153">Сеанс был отменен.</span><span class="sxs-lookup"><span data-stu-id="a8b68-153">The session has been canceled.</span></span>

<span data-ttu-id="a8b68-154">Необходимо закрыть этот обработчик, вызвав [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), несмотря на то, что он больше не является допустимым; в противном случае состояние на стороне клиента будет утечкой.</span><span class="sxs-lookup"><span data-stu-id="a8b68-154">The session handle needs to be closed by calling [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), even though it is no longer valid; otherwise, the client-side state will be leaked.</span></span> <span data-ttu-id="a8b68-155">Новый сеанс должен быть создан путем вызова [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="a8b68-155">A new session should be created by calling [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-156"><span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP \_ E \_ несовместимый \_ транзакция**</span><span class="sxs-lookup"><span data-stu-id="a8b68-156"><span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP\_E\_INCOMPATIBLE\_TXN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-157">0x80320011</span><span class="sxs-lookup"><span data-stu-id="a8b68-157">0x80320011</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-158">Вызов не разрешен из транзакции, доступной только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a8b68-158">The call is not allowed from within a read-only transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-159"><span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP \_ E \_ timeout**</span><span class="sxs-lookup"><span data-stu-id="a8b68-159"><span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP\_E\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-160">0x80320012</span><span class="sxs-lookup"><span data-stu-id="a8b68-160">0x80320012</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-161">Истекло время ожидания вызова при ожидании получения блокировки транзакции.</span><span class="sxs-lookup"><span data-stu-id="a8b68-161">The call timed out while waiting to acquire the transaction lock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-162"><span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_ \_ \_ Отключенные события FWP E NET \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-162"><span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**FWP\_E\_NET\_EVENTS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-163">0x80320013</span><span class="sxs-lookup"><span data-stu-id="a8b68-163">0x80320013</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-164">Сбор событий диагностики сети отключен.</span><span class="sxs-lookup"><span data-stu-id="a8b68-164">The collection of network diagnostic events is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-165"><span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**\_ \_ несовместимый слой FWP \_ E**</span><span class="sxs-lookup"><span data-stu-id="a8b68-165"><span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**FWP\_E\_INCOMPATIBLE\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-166">0x80320014</span><span class="sxs-lookup"><span data-stu-id="a8b68-166">0x80320014</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-167">Операция не поддерживается указанным слоем.</span><span class="sxs-lookup"><span data-stu-id="a8b68-167">The operation is not supported by the specified layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-168"><span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**\_ \_ \_ только клиенты FWP км \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-168"><span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**FWP\_E\_KM\_CLIENTS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-169">0x80320015</span><span class="sxs-lookup"><span data-stu-id="a8b68-169">0x80320015</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-170">Вызов разрешен только для вызывающих методов режима ядра.</span><span class="sxs-lookup"><span data-stu-id="a8b68-170">The call is allowed for kernel-mode callers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-171"><span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**\_несоответствие \_ времени существования FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-171"><span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**FWP\_E\_LIFETIME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-172">0x80320016</span><span class="sxs-lookup"><span data-stu-id="a8b68-172">0x80320016</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-173">Вызов попытался связать два объекта с несовместимыми временами существования.</span><span class="sxs-lookup"><span data-stu-id="a8b68-173">The call tried to associate two objects with incompatible lifetimes.</span></span>

<span data-ttu-id="a8b68-174">Дополнительные сведения о времени существования объектов и ассоциации объектов см. в разделе [Управление объектами](object-management.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b68-174">See [Object Management](object-management.md) for more information on object lifetime and object association.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-175"><span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**\_ \_ встроенный объект FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-175"><span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**FWP\_E\_BUILTIN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-176">0x80320017</span><span class="sxs-lookup"><span data-stu-id="a8b68-176">0x80320017</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-177">Объект является встроенным, поэтому его нельзя удалить.</span><span class="sxs-lookup"><span data-stu-id="a8b68-177">The object is built-in, so it cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-178"><span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ \_ слишком \_ много \_ выносок**</span><span class="sxs-lookup"><span data-stu-id="a8b68-178"><span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP\_E\_TOO\_MANY\_CALLOUTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-179">0x80320018</span><span class="sxs-lookup"><span data-stu-id="a8b68-179">0x80320018</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-180">Достигнуто максимальное число выносок.</span><span class="sxs-lookup"><span data-stu-id="a8b68-180">The maximum number of callouts has been reached.</span></span>

<span data-ttu-id="a8b68-181">В большинстве случаев 100 000 выноски могут быть зарегистрированы одновременно.</span><span class="sxs-lookup"><span data-stu-id="a8b68-181">At most, 100,000 callouts can be registered at the same time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-182"><span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**FWP \_ \_ уведомления \_ удалено**</span><span class="sxs-lookup"><span data-stu-id="a8b68-182"><span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**FWP\_E\_NOTIFICATION\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-183">0x80320019</span><span class="sxs-lookup"><span data-stu-id="a8b68-183">0x80320019</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-184">Не удалось доставить уведомление, так как достигнута максимальная емкость очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8b68-184">A notification could not be delivered because a message queue is at its maximum capacity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-185"><span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**\_несоответствие \_ трафика FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-185"><span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**FWP\_E\_TRAFFIC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-186">0x8032001A</span><span class="sxs-lookup"><span data-stu-id="a8b68-186">0x8032001A</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-187">Параметры сетевого трафика не соответствуют контексту сопоставления безопасности.</span><span class="sxs-lookup"><span data-stu-id="a8b68-187">The network traffic parameters do not match those for the security association context.</span></span>

<span data-ttu-id="a8b68-188">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) можно вызывать несколько раз, но вызывающий объект должен указать один и тот же [**\_ TRAFFIC0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) каждый раз.</span><span class="sxs-lookup"><span data-stu-id="a8b68-188">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) can be called multiple times, but the caller must specify the same [**IPSEC\_TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) each time.</span></span> <span data-ttu-id="a8b68-189">Эта ошибка возвращается, если последующий вызов предоставляет другой **\_ TRAFFIC0 IPSec**.</span><span class="sxs-lookup"><span data-stu-id="a8b68-189">This error is returned if a subsequent call supplies a different **IPSEC\_TRAFFIC0**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-190"><span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP \_ E \_ несовместимое \_ \_ состояние SA**</span><span class="sxs-lookup"><span data-stu-id="a8b68-190"><span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP\_E\_INCOMPATIBLE\_SA\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-191">0x8032001B</span><span class="sxs-lookup"><span data-stu-id="a8b68-191">0x8032001B</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-192">Вызов не разрешен для текущего состояния сопоставления безопасности (SA).</span><span class="sxs-lookup"><span data-stu-id="a8b68-192">The call is not allowed for the current security association (SA) state.</span></span>

<span data-ttu-id="a8b68-193">Функции контекста SA должны вызываться в определенном порядке:</span><span class="sxs-lookup"><span data-stu-id="a8b68-193">The SA context functions must be called in a specific order:</span></span>

-   [<span data-ttu-id="a8b68-194">**IPsecSaContextCreate0**</span><span class="sxs-lookup"><span data-stu-id="a8b68-194">**IPsecSaContextCreate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [<span data-ttu-id="a8b68-195">**IPsecSaContextGetSpi0**</span><span class="sxs-lookup"><span data-stu-id="a8b68-195">**IPsecSaContextGetSpi0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [<span data-ttu-id="a8b68-196">**IPsecSaContextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="a8b68-196">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [<span data-ttu-id="a8b68-197">**IPsecSaContextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="a8b68-197">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

<span data-ttu-id="a8b68-198">Эта ошибка возвращается, если они вызываются неупорядоченно.</span><span class="sxs-lookup"><span data-stu-id="a8b68-198">This error is returned if they are called out of order.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-199"><span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP \_ \_ указатель null \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-199"><span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP\_E\_NULL\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-200">0x8032001C</span><span class="sxs-lookup"><span data-stu-id="a8b68-200">0x8032001C</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-201">Обязательный указатель имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="a8b68-201">A required pointer is null.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-202"><span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**FWP \_ E \_ Недопустимый \_ перечислитель**</span><span class="sxs-lookup"><span data-stu-id="a8b68-202"><span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**FWP\_E\_INVALID\_ENUMERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-203">0x8032001D</span><span class="sxs-lookup"><span data-stu-id="a8b68-203">0x8032001D</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-204">Значение перечислителя в структуре выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="a8b68-204">An enumerator value in a structure is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-205"><span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FWP \_ E \_ недопустимые \_ Флаги**</span><span class="sxs-lookup"><span data-stu-id="a8b68-205"><span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FWP\_E\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-206">0x8032001E</span><span class="sxs-lookup"><span data-stu-id="a8b68-206">0x8032001E</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-207">Поле flags содержит недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="a8b68-207">The flags field contains an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-208"><span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP \_ E \_ Недопустимая \_ Сетевая \_ Маска**</span><span class="sxs-lookup"><span data-stu-id="a8b68-208"><span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP\_E\_INVALID\_NET\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-209">0x8032001F</span><span class="sxs-lookup"><span data-stu-id="a8b68-209">0x8032001F</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-210">Недопустимая маска сети.</span><span class="sxs-lookup"><span data-stu-id="a8b68-210">A network mask is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-211"><span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP \_ E \_ Недопустимый \_ диапазон**</span><span class="sxs-lookup"><span data-stu-id="a8b68-211"><span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP\_E\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-212">0x80320020</span><span class="sxs-lookup"><span data-stu-id="a8b68-212">0x80320020</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-213">Недопустимая структура [**\_ RANGE0 FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) .</span><span class="sxs-lookup"><span data-stu-id="a8b68-213">An [**FWP\_RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) structure is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-214"><span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP \_ E — \_ Недопустимый \_ интервал**</span><span class="sxs-lookup"><span data-stu-id="a8b68-214"><span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP\_E\_INVALID\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-215">0x80320021</span><span class="sxs-lookup"><span data-stu-id="a8b68-215">0x80320021</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-216">Недопустимый интервал времени.</span><span class="sxs-lookup"><span data-stu-id="a8b68-216">The time interval is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-217"><span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP \_ \_ массив нулевой \_ длины \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-217"><span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP\_E\_ZERO\_LENGTH\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-218">0x80320022</span><span class="sxs-lookup"><span data-stu-id="a8b68-218">0x80320022</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-219">Массив, который должен содержать хотя бы один элемент, имеет нулевую длину.</span><span class="sxs-lookup"><span data-stu-id="a8b68-219">An array that must contain at least one element has zero length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-220"><span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**FWP \_ E \_ , \_ отображаемое \_ имя null**</span><span class="sxs-lookup"><span data-stu-id="a8b68-220"><span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**FWP\_E\_NULL\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-221">0x80320023</span><span class="sxs-lookup"><span data-stu-id="a8b68-221">0x80320023</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-222">Поле **displayData.Name** не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="a8b68-222">The **displayData.name** field cannot be null.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-223"><span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP \_ E \_ Недопустимый \_ \_ тип действия**</span><span class="sxs-lookup"><span data-stu-id="a8b68-223"><span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP\_E\_INVALID\_ACTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-224">0x80320024</span><span class="sxs-lookup"><span data-stu-id="a8b68-224">0x80320024</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-225">Тип действия не является допустимым типом действия для фильтра.</span><span class="sxs-lookup"><span data-stu-id="a8b68-225">The action type is not one of the allowed action types for a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-226"><span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP \_ E \_ Недопустимый \_ вес**</span><span class="sxs-lookup"><span data-stu-id="a8b68-226"><span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP\_E\_INVALID\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-227">0x80320025</span><span class="sxs-lookup"><span data-stu-id="a8b68-227">0x80320025</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-228">Недопустимый вес фильтра.</span><span class="sxs-lookup"><span data-stu-id="a8b68-228">The filter weight is not valid.</span></span>

<span data-ttu-id="a8b68-229">Дополнительные сведения см. в разделе [назначение веса фильтра](filter-weight-assignment.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b68-229">See [Filter Weight Assignment](filter-weight-assignment.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-230"><span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**\_несоответствие \_ типа сопоставления FWP E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-230"><span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**FWP\_E\_MATCH\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-231">0x80320026</span><span class="sxs-lookup"><span data-stu-id="a8b68-231">0x80320026</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-232">Условие фильтра содержит тип соответствия, несовместимый с операндами.</span><span class="sxs-lookup"><span data-stu-id="a8b68-232">A filter condition contains a match type that is not compatible with the operands.</span></span>

<span data-ttu-id="a8b68-233">Дополнительные сведения см. в разделе [**FWP \_ Match \_ Type**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) .</span><span class="sxs-lookup"><span data-stu-id="a8b68-233">See [**FWP\_MATCH\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-234"><span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**\_несоответствие \_ типов FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-234"><span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**FWP\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-235">0x80320027</span><span class="sxs-lookup"><span data-stu-id="a8b68-235">0x80320027</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-236">Структура [**\_ VALUE0 FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) или [**фвпм \_ условие \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) имеет неверный тип.</span><span class="sxs-lookup"><span data-stu-id="a8b68-236">An [**FWP\_VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) structure or an [**FWPM\_CONDITION\_VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) structure is of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-237"><span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ из \_ \_ \_ границ**</span><span class="sxs-lookup"><span data-stu-id="a8b68-237"><span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP\_E\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-238">0x80320028</span><span class="sxs-lookup"><span data-stu-id="a8b68-238">0x80320028</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-239">Целочисленное значение находится за пределами допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="a8b68-239">An integer value is outside the allowed range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-240"><span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ е \_ зарезервировано**</span><span class="sxs-lookup"><span data-stu-id="a8b68-240"><span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP\_E\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-241">0x80320029</span><span class="sxs-lookup"><span data-stu-id="a8b68-241">0x80320029</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-242">Зарезервированное поле не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a8b68-242">A reserved field is nonzero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-243"><span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP \_ , \_ повторяющееся \_ условие**</span><span class="sxs-lookup"><span data-stu-id="a8b68-243"><span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP\_E\_DUPLICATE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-244">0x8032002A</span><span class="sxs-lookup"><span data-stu-id="a8b68-244">0x8032002A</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-245">Фильтр не может содержать несколько условий, работающих с одним полем.</span><span class="sxs-lookup"><span data-stu-id="a8b68-245">A filter cannot contain multiple conditions operating on a single field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-246"><span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP \_ E \_ дубликат \_ кэймод**</span><span class="sxs-lookup"><span data-stu-id="a8b68-246"><span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP\_E\_DUPLICATE\_KEYMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-247">0x8032002B</span><span class="sxs-lookup"><span data-stu-id="a8b68-247">0x8032002B</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-248">Политика не может содержать один и тот же модуль ключа более одного раза.</span><span class="sxs-lookup"><span data-stu-id="a8b68-248">A policy cannot contain the same keying module more than once.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-249"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**FWP \_ \_ действие \_ несовместимо \_ с \_ слоем**</span><span class="sxs-lookup"><span data-stu-id="a8b68-249"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**FWP\_E\_ACTION\_INCOMPATIBLE\_WITH\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-250">0x8032002C</span><span class="sxs-lookup"><span data-stu-id="a8b68-250">0x8032002C</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-251">Тип действия несовместим с уровнем.</span><span class="sxs-lookup"><span data-stu-id="a8b68-251">The action type is not compatible with the layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-252"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**FWP \_ \_ действие \_ несовместимо \_ с \_ подслоем**</span><span class="sxs-lookup"><span data-stu-id="a8b68-252"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**FWP\_E\_ACTION\_INCOMPATIBLE\_WITH\_SUBLAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-253">0x8032002D</span><span class="sxs-lookup"><span data-stu-id="a8b68-253">0x8032002D</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-254">Тип действия несовместим с подслоем.</span><span class="sxs-lookup"><span data-stu-id="a8b68-254">The action type is not compatible with the sub-layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-255"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**\_контекст FWP \_ E \_ несовместим \_ с \_ слоем**</span><span class="sxs-lookup"><span data-stu-id="a8b68-255"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**FWP\_E\_CONTEXT\_INCOMPATIBLE\_WITH\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-256">0x8032002E</span><span class="sxs-lookup"><span data-stu-id="a8b68-256">0x8032002E</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-257">Необработанный контекст или контекст поставщика несовместим с уровнем.</span><span class="sxs-lookup"><span data-stu-id="a8b68-257">The raw context or the provider context is not compatible with the layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-258"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**\_контекст FWP \_ E \_ несовместим \_ с \_ выноской**</span><span class="sxs-lookup"><span data-stu-id="a8b68-258"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**FWP\_E\_CONTEXT\_INCOMPATIBLE\_WITH\_CALLOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-259">0x8032002F</span><span class="sxs-lookup"><span data-stu-id="a8b68-259">0x8032002F</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-260">Необработанный контекст или контекст поставщика несовместим с вызываемым.</span><span class="sxs-lookup"><span data-stu-id="a8b68-260">The raw context or the provider context is not compatible with the callout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-261"><span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP \_ E \_ несовместимый \_ метод проверки подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-261"><span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP\_E\_INCOMPATIBLE\_AUTH\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-262">0x80320030</span><span class="sxs-lookup"><span data-stu-id="a8b68-262">0x80320030</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-263">Метод проверки подлинности несовместим с типом политики.</span><span class="sxs-lookup"><span data-stu-id="a8b68-263">The authentication method is not compatible with the policy type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-264"><span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP \_ E \_ несовместимая \_ Группа Диффи-Хелмана \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-264"><span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP\_E\_INCOMPATIBLE\_DH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-265">0x80320031L</span><span class="sxs-lookup"><span data-stu-id="a8b68-265">0x80320031L</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-266">Группа Diffie-Hellman несовместима с типом политики.</span><span class="sxs-lookup"><span data-stu-id="a8b68-266">The Diffie-Hellman group is not compatible with the policy type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-267"><span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP \_ E \_ EM \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="a8b68-267"><span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP\_E\_EM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-268">0x80320032</span><span class="sxs-lookup"><span data-stu-id="a8b68-268">0x80320032</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-269">Политика IKE не может содержать политику расширенного режима.</span><span class="sxs-lookup"><span data-stu-id="a8b68-269">An IKE policy cannot contain an Extended Mode policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-270"><span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ е \_ никогда не \_ соответствует**</span><span class="sxs-lookup"><span data-stu-id="a8b68-270"><span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP\_E\_NEVER\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-271">0x80320033</span><span class="sxs-lookup"><span data-stu-id="a8b68-271">0x80320033</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-272">Шаблон перечисления или подписка никогда не будут сопоставляться ни с одним из объектов.</span><span class="sxs-lookup"><span data-stu-id="a8b68-272">The enumeration template or subscription will never match any objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-273"><span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**\_несоответствие \_ контекста поставщика FWP E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-273"><span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**FWP\_E\_PROVIDER\_CONTEXT\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-274">0x80320034</span><span class="sxs-lookup"><span data-stu-id="a8b68-274">0x80320034</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-275">Неправильный тип контекста поставщика.</span><span class="sxs-lookup"><span data-stu-id="a8b68-275">The provider context is of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-276"><span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP \_ E \_ Недопустимый \_ параметр**</span><span class="sxs-lookup"><span data-stu-id="a8b68-276"><span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-277">0x80320035</span><span class="sxs-lookup"><span data-stu-id="a8b68-277">0x80320035</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-278">Неправильный параметр".</span><span class="sxs-lookup"><span data-stu-id="a8b68-278">The parameter is incorrect.</span></span>

<span data-ttu-id="a8b68-279">Возможные причины этой ошибки:</span><span class="sxs-lookup"><span data-stu-id="a8b68-279">Possible reasons for this error:</span></span>

-   <span data-ttu-id="a8b68-280">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) был вызван без задания флага **\_ туннеля фвпм \_ \_ в качестве \_ точки \_** и с условиями, отличными от локального или удаленного адреса.</span><span class="sxs-lookup"><span data-stu-id="a8b68-280">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) was called without setting the flag **FWPM\_TUNNEL\_FLAG\_POINT\_TO\_POINT** and with conditions other than local/remote address.</span></span>
-   <span data-ttu-id="a8b68-281">Недопустимая строка в Юникоде или строка в Юникоде, которая содержит непечатаемые символы.</span><span class="sxs-lookup"><span data-stu-id="a8b68-281">An invalid Unicode string, or a Unicode string that contains unprintable characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-282"><span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ , \_ слишком \_ много \_ подуровней**</span><span class="sxs-lookup"><span data-stu-id="a8b68-282"><span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP\_E\_TOO\_MANY\_SUBLAYERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-283">0x80320036</span><span class="sxs-lookup"><span data-stu-id="a8b68-283">0x80320036</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-284">Достигнуто максимальное число подслоев.</span><span class="sxs-lookup"><span data-stu-id="a8b68-284">The maximum number of sublayers has been reached.</span></span>

<span data-ttu-id="a8b68-285">WFP поддерживает не более 2 6 подуровней.</span><span class="sxs-lookup"><span data-stu-id="a8b68-285">WFP supports at most 2 6 sublayers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-286"><span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**\_ \_ \_ не удалось отправить уведомление на выноску FWP \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-286"><span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**FWP\_E\_CALLOUT\_NOTIFICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-287">0x80320037</span><span class="sxs-lookup"><span data-stu-id="a8b68-287">0x80320037</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-288">Функция уведомления для вызова вернула ошибку.</span><span class="sxs-lookup"><span data-stu-id="a8b68-288">The notification function for a callout returned an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-289"><span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP \_ E \_ недопустимое \_ Преобразование проверки подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-289"><span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP\_E\_INVALID\_AUTH\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-290">0x80320038</span><span class="sxs-lookup"><span data-stu-id="a8b68-290">0x80320038</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-291">Недопустимое преобразование проверки подлинности IPsec.</span><span class="sxs-lookup"><span data-stu-id="a8b68-291">The IPsec authentication transform is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b68-292"><span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP \_ E \_ недопустимое \_ преобразование шифра \_**</span><span class="sxs-lookup"><span data-stu-id="a8b68-292"><span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP\_E\_INVALID\_CIPHER\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b68-293">0x80320039</span><span class="sxs-lookup"><span data-stu-id="a8b68-293">0x80320039</span></span>
</dt> <dt>



<span data-ttu-id="a8b68-294">Недопустимое преобразование шифра IPsec.</span><span class="sxs-lookup"><span data-stu-id="a8b68-294">The IPsec cipher transform is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8b68-295">Требования</span><span class="sxs-lookup"><span data-stu-id="a8b68-295">Requirements</span></span>



| <span data-ttu-id="a8b68-296">Требование</span><span class="sxs-lookup"><span data-stu-id="a8b68-296">Requirement</span></span> | <span data-ttu-id="a8b68-297">Значение</span><span class="sxs-lookup"><span data-stu-id="a8b68-297">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b68-298">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8b68-298">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b68-299">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8b68-299">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8b68-300">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8b68-300">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b68-301">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8b68-301">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8b68-302">Header</span><span class="sxs-lookup"><span data-stu-id="a8b68-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b68-303"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b68-303"><dt>Winerror.h</dt></span></span> </dl> |



 

 





