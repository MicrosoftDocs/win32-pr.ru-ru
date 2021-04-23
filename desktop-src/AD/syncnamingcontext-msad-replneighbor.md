---
title: Метод Синкнамингконтекст класса MSAD_ReplNeighbor
description: Вызывает функцию Дсрепликасинк, которая синхронизирует целевой контекст именования с одним из его источников.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Active Directory метода Синкнамингконтекст
- Active Directory метода Синкнамингконтекст, класс MSAD_ReplNeighbor
- Класс MSAD_ReplNeighbor Active Directory, метод Синкнамингконтекст
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492177"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a><span data-ttu-id="bf194-106">Метод Синкнамингконтекст \_ класса РЕПЛНЕИГХБОР МСАД</span><span class="sxs-lookup"><span data-stu-id="bf194-106">SyncNamingContext method of the MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="bf194-107">Вызывает функцию [**дсрепликасинк**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) , которая синхронизирует целевой контекст именования с одним из его источников.</span><span class="sxs-lookup"><span data-stu-id="bf194-107">Calls the [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) function that synchronizes a destination naming context with one of its sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf194-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf194-108">Syntax</span></span>


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a><span data-ttu-id="bf194-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf194-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf194-110">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf194-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf194-111">Дополнительные данные, определяющие способ обработки запроса методом.</span><span class="sxs-lookup"><span data-stu-id="bf194-111">Additional data that determines how the method processes the request.</span></span> <span data-ttu-id="bf194-112">Этот параметр может быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bf194-112">This parameter can be a combination of the following values.</span></span>

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span data-ttu-id="bf194-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**\_ \_ Добавление ссылки в репсинк DS \_**</span><span class="sxs-lookup"><span data-stu-id="bf194-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS\_REPSYNC\_ADD\_REFERENCE**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-114">Заставляет исходный агент системы каталогов (DSA) проверить наличие локального DSA в списке репликация источника.</span><span class="sxs-lookup"><span data-stu-id="bf194-114">Causes the source directory system agent (DSA) to verify that the local DSA is present in the source replicates-to list.</span></span> <span data-ttu-id="bf194-115">Если локальный DSA отсутствует, он добавляется.</span><span class="sxs-lookup"><span data-stu-id="bf194-115">If the local DSA is not present, it is added.</span></span> <span data-ttu-id="bf194-116">Это гарантирует, что источник отправляет уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="bf194-116">This ensures that the source sends change notifications.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span data-ttu-id="bf194-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ репсинк \_ все \_ источники**</span><span class="sxs-lookup"><span data-stu-id="bf194-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS\_REPSYNC\_ALL\_SOURCES**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-118">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bf194-118">This value is not supported.</span></span>

<span data-ttu-id="bf194-119">**Windows server 2008 R2, Windows server 2008 и Windows server 2003:** Выполняет синхронизацию из всех источников.</span><span class="sxs-lookup"><span data-stu-id="bf194-119">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Synchronizes from all sources.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span data-ttu-id="bf194-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS \_ репсинк, \_ асинхронная \_ операция**</span><span class="sxs-lookup"><span data-stu-id="bf194-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS\_REPSYNC\_ASYNCHRONOUS\_OPERATION**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-121">Выполняет эту операцию асинхронно.</span><span class="sxs-lookup"><span data-stu-id="bf194-121">Performs this operation asynchronously.</span></span>

<span data-ttu-id="bf194-122">**Windows server 2008 R2, Windows server 2008 и Windows server 2003:** Требуется при использовании **DS \_ репсинк \_ все \_ источники**.</span><span class="sxs-lookup"><span data-stu-id="bf194-122">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Required when using **DS\_REPSYNC\_ALL\_SOURCES**.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span data-ttu-id="bf194-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS \_ репсинк \_ Force**</span><span class="sxs-lookup"><span data-stu-id="bf194-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS\_REPSYNC\_FORCE**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-124">Синхронизирует, даже если ссылка в данный момент отключена.</span><span class="sxs-lookup"><span data-stu-id="bf194-124">Synchronizes even if the link is currently disabled.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span data-ttu-id="bf194-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**\_РЕПСИНК DS \_ Full**</span><span class="sxs-lookup"><span data-stu-id="bf194-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS\_REPSYNC\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-126">Синхронизирует, начиная с первого порядкового номера обновления (USN).</span><span class="sxs-lookup"><span data-stu-id="bf194-126">Synchronizes starting from the first Update Sequence Number (USN).</span></span>

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span data-ttu-id="bf194-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**\_Служба DS репсинк \_ межсайтовые \_ сообщения**</span><span class="sxs-lookup"><span data-stu-id="bf194-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS\_REPSYNC\_INTERSITE\_MESSAGING**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-128">Синхронизирует с помощью ISM.</span><span class="sxs-lookup"><span data-stu-id="bf194-128">Synchronizes using an ISM.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span data-ttu-id="bf194-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ репсинк \_ No \_ undiscard**</span><span class="sxs-lookup"><span data-stu-id="bf194-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS\_REPSYNC\_NO\_DISCARD**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-130">Не отменяет этот запрос на синхронизацию даже в случае, если аналогичная синхронизация находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="bf194-130">Does not discard this synchronization request, even if a similar synchronization is pending.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span data-ttu-id="bf194-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ репсинк \_ периодически**</span><span class="sxs-lookup"><span data-stu-id="bf194-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS\_REPSYNC\_PERIODIC**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-132">Указывает, что эта операция является периодическим запросом синхронизации, запланированным администратором.</span><span class="sxs-lookup"><span data-stu-id="bf194-132">Indicates that this operation is a periodic synchronization request that is scheduled by the administrator.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span data-ttu-id="bf194-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**Служба DS \_ репсинк \_ срочно**</span><span class="sxs-lookup"><span data-stu-id="bf194-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS\_REPSYNC\_URGENT**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-134">Указывает, что эта операция является уведомлением об обновлении, которое помечено как срочное.</span><span class="sxs-lookup"><span data-stu-id="bf194-134">Indicates that this operation is a notification of an update that is marked as urgent.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span data-ttu-id="bf194-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**\_РЕПСИНК DS \_ для записи**</span><span class="sxs-lookup"><span data-stu-id="bf194-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS\_REPSYNC\_WRITEABLE**</span></span>


</dt> <dd>

<span data-ttu-id="bf194-136">Указывает, что эта реплика доступна для записи.</span><span class="sxs-lookup"><span data-stu-id="bf194-136">Indicates that this replica is writable.</span></span> <span data-ttu-id="bf194-137">Если этот флаг не установлен, реплика доступна только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf194-137">If this flag is not set, the replica is read-only.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf194-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf194-138">Return value</span></span>

<span data-ttu-id="bf194-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bf194-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf194-140">Требования</span><span class="sxs-lookup"><span data-stu-id="bf194-140">Requirements</span></span>



| <span data-ttu-id="bf194-141">Требование</span><span class="sxs-lookup"><span data-stu-id="bf194-141">Requirement</span></span> | <span data-ttu-id="bf194-142">Значение</span><span class="sxs-lookup"><span data-stu-id="bf194-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf194-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf194-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bf194-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bf194-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="bf194-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf194-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bf194-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf194-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf194-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bf194-147">Namespace</span></span><br/>                | <span data-ttu-id="bf194-148">Корневой \\ микрософтактиведиректори</span><span class="sxs-lookup"><span data-stu-id="bf194-148">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="bf194-149">MOF</span><span class="sxs-lookup"><span data-stu-id="bf194-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf194-150"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf194-150"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf194-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bf194-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf194-152"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf194-152"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf194-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf194-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf194-154">**МСАД \_ реплнеигхбор**</span><span class="sxs-lookup"><span data-stu-id="bf194-154">**MSAD\_ReplNeighbor**</span></span>](msad-replneighbor.md)
</dt> </dl>

 

 





