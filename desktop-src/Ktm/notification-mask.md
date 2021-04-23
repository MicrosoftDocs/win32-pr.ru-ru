---
description: Список различных типов уведомлений, которые могут быть получены прикреплением.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (Ктмтипес. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683838"
---
# <a name="notification_mask"></a><span data-ttu-id="456b3-103">\_Маска уведомления</span><span class="sxs-lookup"><span data-stu-id="456b3-103">NOTIFICATION\_MASK</span></span>

<span data-ttu-id="456b3-104">Список различных типов уведомлений, которые могут быть получены прикреплением.</span><span class="sxs-lookup"><span data-stu-id="456b3-104">Lists the different types of notifications that can be received by an enlistment.</span></span>

<dl> <dt>

<span data-ttu-id="456b3-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_Маска уведомления \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="456b3-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**TRANSACTION\_NOTIFY\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-106">0x3FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="456b3-106">0x3FFFFFFF</span></span>
</dt> <dt>



<span data-ttu-id="456b3-107">Маска, которая указывает все допустимые биты для уведомления транзакции.</span><span class="sxs-lookup"><span data-stu-id="456b3-107">A mask that indicates all valid bits for a transaction notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**Предварительная \_ Подготовка уведомлений транзакции \_**</span><span class="sxs-lookup"><span data-stu-id="456b3-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**TRANSACTION\_NOTIFY\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="456b3-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="456b3-110">Это уведомление вызывается после того, как клиент вызывает [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) , а либо диспетчер ресурсов (RM) не поддерживает однофазную фиксацию, либо старший диспетчер транзакций (TM) вызывает [**препрепаринлистмент**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span><span class="sxs-lookup"><span data-stu-id="456b3-110">This notification is called after a client calls [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) and either no resource manager (RM) supports single-phase commit or a superior transaction manager (TM) calls [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span></span> <span data-ttu-id="456b3-111">Это уведомление получает RMs, указывая, что он должен выполнить все действия, которые могут привести к тому, что другие RMs должны присоединиться к транзакции, например очистить свой кэш.</span><span class="sxs-lookup"><span data-stu-id="456b3-111">This notification is received by the RMs indicating that they should complete any work that could cause other RMs to need to enlist in a transaction, such as flushing its cache.</span></span> <span data-ttu-id="456b3-112">После выполнения этих операций RM должен вызвать [**препрепарекомплете**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span><span class="sxs-lookup"><span data-stu-id="456b3-112">After completing these operations the RM must call [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span></span> <span data-ttu-id="456b3-113">Для получения этого уведомления RM также должен поддерживать **\_ \_ фиксацию** **\_ уведомлений транзакции \_ Prepare** и извещения о транзакции.</span><span class="sxs-lookup"><span data-stu-id="456b3-113">To receive this notification the RM must also support **TRANSACTION\_NOTIFY\_PREPARE** and **TRANSACTION\_NOTIFY\_COMMIT**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**\_Подготовка уведомления \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="456b3-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**TRANSACTION\_NOTIFY\_PREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="456b3-115">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="456b3-116">Это уведомление вызывается после завершения обработки предварительной **\_ \_ подготовки уведомления о транзакции** .</span><span class="sxs-lookup"><span data-stu-id="456b3-116">This notification is called after the **TRANSACTION\_NOTIFY\_PREPREPARE** processing is complete.</span></span> <span data-ttu-id="456b3-117">Он сигнализирует диспетчеру ресурсов завершить всю работу, связанную с этим зачислением, чтобы гарантировать успешную операцию фиксации, а также выполнить операцию аварийного завершения.</span><span class="sxs-lookup"><span data-stu-id="456b3-117">It signals the RM to complete all the work that is associated with this enlistment so that it can guarantee that a commit operation could succeed and an abort operation could also succeed.</span></span> <span data-ttu-id="456b3-118">Как правило, основная часть работы для транзакции выполняется на этапе подготовки.</span><span class="sxs-lookup"><span data-stu-id="456b3-118">Typically, the bulk of the work for a transaction is done during the prepare phase.</span></span> <span data-ttu-id="456b3-119">Для устойчивых RMs они должны регистрировать свое состояние до вызова функции [**препарекомплете**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) .</span><span class="sxs-lookup"><span data-stu-id="456b3-119">For durable RMs, they must log their state prior to calling the [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) function.</span></span> <span data-ttu-id="456b3-120">Это последняя вероятность того, что RM запросит, что была произведена откат транзакции.</span><span class="sxs-lookup"><span data-stu-id="456b3-120">This is the last chance for the RM to request that the transaction be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**\_уведомление о \_ ФИКСАЦИи транзакции**</span><span class="sxs-lookup"><span data-stu-id="456b3-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION\_NOTIFY\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="456b3-122">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="456b3-123">Это уведомление сигнализирует диспетчеру ресурсов завершить всю работу, связанную с этим зачислением.</span><span class="sxs-lookup"><span data-stu-id="456b3-123">This notification signals the RM to complete all the work that is associated with this enlistment.</span></span> <span data-ttu-id="456b3-124">Как правило, RM освобождает все блокировки и освобождает все сведения, необходимые для отката транзакции.</span><span class="sxs-lookup"><span data-stu-id="456b3-124">Typically, the RM releases any locks, releases any information necessary to roll back the transaction.</span></span> <span data-ttu-id="456b3-125">RM должен ответить, вызвав функцию [**коммиткомплете**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) , когда она завершит эти операции.</span><span class="sxs-lookup"><span data-stu-id="456b3-125">The RM must respond by calling the [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) function when it has finished these operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**\_откат уведомления \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="456b3-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION\_NOTIFY\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-127">0x00000008</span><span class="sxs-lookup"><span data-stu-id="456b3-127">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="456b3-128">Это уведомление сообщает RM о необходимости отмены всей выполненной работы, связанной с транзакцией.</span><span class="sxs-lookup"><span data-stu-id="456b3-128">This notification signals the RM to undo all the work it has done that is associated with the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**Предварительная \_ Подготовка уведомлений транзакции \_ \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="456b3-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-130">0x00000010</span><span class="sxs-lookup"><span data-stu-id="456b3-130">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="456b3-131">Это уведомление сообщает старший TM, что операция предварительной подготовки успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="456b3-131">This notification signals to the superior TM that a pre-prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**\_Подготовка к уведомлению транзакции \_ \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="456b3-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-133">0x00000020</span><span class="sxs-lookup"><span data-stu-id="456b3-133">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="456b3-134">Это уведомление сообщает старший TM, что операция подготовки успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="456b3-134">This notification signals to the superior TM that a prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**\_уведомление о \_ фиксации транзакции \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="456b3-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION\_NOTIFY\_COMMIT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-136">0x00000040</span><span class="sxs-lookup"><span data-stu-id="456b3-136">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="456b3-137">Это уведомление сообщает старший TM о том, что операция фиксации выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="456b3-137">This notification signals to the superior TM that a commit operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**\_откат уведомления о транзакции \_ \_ завершен**</span><span class="sxs-lookup"><span data-stu-id="456b3-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**TRANSACTION\_NOTIFY\_ROLLBACK\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="456b3-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="456b3-140">Это уведомление сообщает старший TM, что операция отката была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="456b3-140">This notification signals to the superior TM that a rollback operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_Восстановление уведомления \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="456b3-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACTION\_NOTIFY\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="456b3-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="456b3-143">Это уведомление передает службе RMs о том, что они должны восстановить свое состояние, так как результат транзакции должен быть доставлен снова.</span><span class="sxs-lookup"><span data-stu-id="456b3-143">This notification signals to RMs that they should recover their state because a transaction outcome must be redelivered.</span></span> <span data-ttu-id="456b3-144">Например, при восстановлении RM и при наличии транзакций, оставшихся под сомнением.</span><span class="sxs-lookup"><span data-stu-id="456b3-144">For example, when an RM is recovered, and when there are transactions left in-doubt.</span></span> <span data-ttu-id="456b3-145">Это уведомление доставляется после разрешения сомнительного состояния.</span><span class="sxs-lookup"><span data-stu-id="456b3-145">This notification is delivered once the in-doubt state is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**\_ \_ \_ фиксация одной фазы уведомления транзакции \_**</span><span class="sxs-lookup"><span data-stu-id="456b3-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION\_NOTIFY\_SINGLE\_PHASE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-147">0x00000200</span><span class="sxs-lookup"><span data-stu-id="456b3-147">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="456b3-148">Это уведомление сообщает RM о завершении и фиксации транзакции без использования протокола двухфазной фиксации.</span><span class="sxs-lookup"><span data-stu-id="456b3-148">This notification signals the RM to complete and commit the transaction without using a two-phase commit protocol.</span></span> <span data-ttu-id="456b3-149">Если RM хочет использовать двухэтапный процесс, он должен ответить, вызвав функцию [**синглефасережект**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .</span><span class="sxs-lookup"><span data-stu-id="456b3-149">If the RM wants to use a two-phase operation, it must respond by calling the [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_ \_ фиксация делегата уведомления транзакции \_**</span><span class="sxs-lookup"><span data-stu-id="456b3-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION\_NOTIFY\_DELEGATE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-151">0x00000400</span><span class="sxs-lookup"><span data-stu-id="456b3-151">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="456b3-152">KTM сообщает старший TM о выполнении операции фиксации.</span><span class="sxs-lookup"><span data-stu-id="456b3-152">KTM is signaling to the superior TM to perform a commit operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**\_запрос на \_ Восстановление \_ уведомления транзакции**</span><span class="sxs-lookup"><span data-stu-id="456b3-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**TRANSACTION\_NOTIFY\_RECOVER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-154">0x00000800</span><span class="sxs-lookup"><span data-stu-id="456b3-154">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="456b3-155">KTM сообщает старшему TM-запросу о состоянии сомнительной транзакции.</span><span class="sxs-lookup"><span data-stu-id="456b3-155">KTM is signaling to the superior TM to query the status of an in-doubt transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**Предварительная \_ \_ Подготовка прикрепления для уведомления транзакции \_**</span><span class="sxs-lookup"><span data-stu-id="456b3-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION\_NOTIFY\_ENLIST\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-157">0x00001000</span><span class="sxs-lookup"><span data-stu-id="456b3-157">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="456b3-158">Это уведомление сообщает старший TM, что предварительно подготовленные уведомления должны доставляться по указанному зачислению.</span><span class="sxs-lookup"><span data-stu-id="456b3-158">This notification signals to the superior TM that pre-prepare notifications must be delivered on the specified enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ Последнее восстановление транзакции с уведомлением \_**</span><span class="sxs-lookup"><span data-stu-id="456b3-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION\_NOTIFY\_LAST\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="456b3-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="456b3-161">Это уведомление означает, что операция восстановления для этого RM завершена.</span><span class="sxs-lookup"><span data-stu-id="456b3-161">This notification indicates that the recovery operation is complete for this RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**уведомление о неопределенном \_ \_ состоянии транзакции**</span><span class="sxs-lookup"><span data-stu-id="456b3-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**TRANSACTION\_NOTIFY\_INDOUBT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-163">0x00004000</span><span class="sxs-lookup"><span data-stu-id="456b3-163">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="456b3-164">Указанная транзакция находится в состоянии «под сомнением».</span><span class="sxs-lookup"><span data-stu-id="456b3-164">The specified transaction is in an in-doubt state.</span></span> <span data-ttu-id="456b3-165">RM получает это уведомление во время операций восстановления, когда транзакция была подготовлена, но старший диспетчер транзакций (TM) не доступен.</span><span class="sxs-lookup"><span data-stu-id="456b3-165">The RM receives this notification during recovery operations when a transaction has been prepared, but there is no superior transaction manager (TM) available.</span></span> <span data-ttu-id="456b3-166">Например, если транзакция включает в себя удаленный TM и этот узел недоступен, его узел недоступен или локальная служба [координатор распределенных транзакций](/previous-versions/windows/desktop/ms684146(v=vs.85)) недоступна, состояние транзакции считается сомнительным.</span><span class="sxs-lookup"><span data-stu-id="456b3-166">For example, when a transaction involves a remote TM and that node is unavailable, its node is unavailable, or the local [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) service is unavailable, the transaction state is in-doubt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**ТРАНЗАКЦИЯ \_ уведомления \_ TM \_ Online**</span><span class="sxs-lookup"><span data-stu-id="456b3-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACTION\_NOTIFY\_TM\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-168">0x02000000</span><span class="sxs-lookup"><span data-stu-id="456b3-168">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="456b3-169">TM находится в оперативном режиме и принимает запросы.</span><span class="sxs-lookup"><span data-stu-id="456b3-169">The TM is online and accepting requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**\_ \_ результат запроса уведомления \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="456b3-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**TRANSACTION\_NOTIFY\_REQUEST\_OUTCOME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-171">0x20000000</span><span class="sxs-lookup"><span data-stu-id="456b3-171">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="456b3-172">Сообщает RMs о том, что имеются сведения о результатах, и что необходимо сделать запрос на эту информацию.</span><span class="sxs-lookup"><span data-stu-id="456b3-172">Signals to RMs that there is outcome information available, and that a request for that information should be made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="456b3-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_уведомление о \_ ФИКСАЦИи транзакции \_**</span><span class="sxs-lookup"><span data-stu-id="456b3-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION\_NOTIFY\_COMMIT\_FINALIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="456b3-174">0x40000000</span><span class="sxs-lookup"><span data-stu-id="456b3-174">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="456b3-175">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="456b3-175">Reserved.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="456b3-176">Требования</span><span class="sxs-lookup"><span data-stu-id="456b3-176">Requirements</span></span>



| <span data-ttu-id="456b3-177">Требование</span><span class="sxs-lookup"><span data-stu-id="456b3-177">Requirement</span></span> | <span data-ttu-id="456b3-178">Значение</span><span class="sxs-lookup"><span data-stu-id="456b3-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="456b3-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="456b3-179">Minimum supported client</span></span><br/> | <span data-ttu-id="456b3-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="456b3-180">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="456b3-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="456b3-181">Minimum supported server</span></span><br/> | <span data-ttu-id="456b3-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="456b3-182">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="456b3-183">Header</span><span class="sxs-lookup"><span data-stu-id="456b3-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="456b3-184"><dt>Ктмтипес. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="456b3-184"><dt>KtmTypes.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="456b3-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="456b3-185">See also</span></span>

<dl> <dt>

<span data-ttu-id="456b3-186">[Координатор распределенных транзакций](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="456b3-186">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="456b3-187">Константы диспетчера транзакций ядра</span><span class="sxs-lookup"><span data-stu-id="456b3-187">Kernel Transaction Manager Constants</span></span>](kernel-transaction-manager-constants.md)
</dt> <dt>

[<span data-ttu-id="456b3-188">**креатинлистмент**</span><span class="sxs-lookup"><span data-stu-id="456b3-188">**CreateEnlistment**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[<span data-ttu-id="456b3-189">**коммиткомплете**</span><span class="sxs-lookup"><span data-stu-id="456b3-189">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[<span data-ttu-id="456b3-190">**жетнотификатионресаурцеманажер**</span><span class="sxs-lookup"><span data-stu-id="456b3-190">**GetNotificationResourceManager**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[<span data-ttu-id="456b3-191">**жетнотификатионресаурцеманажерасинк**</span><span class="sxs-lookup"><span data-stu-id="456b3-191">**GetNotificationResourceManagerAsync**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[<span data-ttu-id="456b3-192">**препарекомплете**</span><span class="sxs-lookup"><span data-stu-id="456b3-192">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[<span data-ttu-id="456b3-193">**синглефасережект**</span><span class="sxs-lookup"><span data-stu-id="456b3-193">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[<span data-ttu-id="456b3-194">**\_уведомление транзакции**</span><span class="sxs-lookup"><span data-stu-id="456b3-194">**TRANSACTION\_NOTIFICATION**</span></span>](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

