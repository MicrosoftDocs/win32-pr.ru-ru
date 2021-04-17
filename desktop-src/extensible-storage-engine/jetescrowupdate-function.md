---
description: Дополнительные сведения о функции Жетескровупдате
title: Функция JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702795"
---
# <a name="jetescrowupdate-function"></a><span data-ttu-id="bc519-103">Функция JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="bc519-103">JetEscrowUpdate Function</span></span>


<span data-ttu-id="bc519-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bc519-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetescrowupdate-function"></a><span data-ttu-id="bc519-105">Функция JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="bc519-105">JetEscrowUpdate Function</span></span>

<span data-ttu-id="bc519-106">Функция **жетескровупдате** выполняет атомарную операцию сложения для одного столбца.</span><span class="sxs-lookup"><span data-stu-id="bc519-106">The **JetEscrowUpdate** function performs an atomic addition operation on one column.</span></span> <span data-ttu-id="bc519-107">Эта функция позволяет нескольким сеансам одновременно обновлять одну и ту же запись без конфликтов.</span><span class="sxs-lookup"><span data-stu-id="bc519-107">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="bc519-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc519-108">Parameters</span></span>

<span data-ttu-id="bc519-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="bc519-109">*sesid*</span></span>

<span data-ttu-id="bc519-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="bc519-110">The session to use for this call.</span></span>

<span data-ttu-id="bc519-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="bc519-111">*tableid*</span></span>

<span data-ttu-id="bc519-112">Курсор, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="bc519-112">The cursor to use for this call.</span></span>

<span data-ttu-id="bc519-113">*columnid*</span><span class="sxs-lookup"><span data-stu-id="bc519-113">*columnid*</span></span>

<span data-ttu-id="bc519-114">Значение *columnid* обновляемого столбца.</span><span class="sxs-lookup"><span data-stu-id="bc519-114">The *columnid* of the column to be updated.</span></span>

<span data-ttu-id="bc519-115">*PV*</span><span class="sxs-lookup"><span data-stu-id="bc519-115">*pv*</span></span>

<span data-ttu-id="bc519-116">Указатель на буфер, содержащий слагаемое для столбца.</span><span class="sxs-lookup"><span data-stu-id="bc519-116">A pointer to a buffer containing the addend for the column.</span></span>

<span data-ttu-id="bc519-117">*кбмакс*</span><span class="sxs-lookup"><span data-stu-id="bc519-117">*cbMax*</span></span>

<span data-ttu-id="bc519-118">Размер буфера, содержащего слагаемое.</span><span class="sxs-lookup"><span data-stu-id="bc519-118">The size of the buffer containing the addend.</span></span>

<span data-ttu-id="bc519-119">*пволд*</span><span class="sxs-lookup"><span data-stu-id="bc519-119">*pvOld*</span></span>

<span data-ttu-id="bc519-120">Выходной буфер, получающий текущее значение столбца, хранимое в базе данных (управление версиями игнорируется).</span><span class="sxs-lookup"><span data-stu-id="bc519-120">The output buffer that will receive the current value of the column as stored in the database (versioning is ignored).</span></span>

<span data-ttu-id="bc519-121">*кболдмакс*</span><span class="sxs-lookup"><span data-stu-id="bc519-121">*cbOldMax*</span></span>

<span data-ttu-id="bc519-122">Максимальный размер выходного буфера, который будет принимать текущее значение столбца.</span><span class="sxs-lookup"><span data-stu-id="bc519-122">The maximum size of the output buffer that will receive the current value of the column.</span></span> <span data-ttu-id="bc519-123">В настоящее время поддерживается только JET_coltypLong, поэтому размер буфера должен составлять 4 байт или 0 байт.</span><span class="sxs-lookup"><span data-stu-id="bc519-123">Currently only JET_coltypLong is supported, so the buffer must either be 4 bytes or 0 bytes in length.</span></span> <span data-ttu-id="bc519-124">Если *пволд* имеет значение null, то *кболдмакс* должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="bc519-124">If *pvOld* is NULL then *cbOldMax* should be 0.</span></span>

<span data-ttu-id="bc519-125">*пкболдактуал*</span><span class="sxs-lookup"><span data-stu-id="bc519-125">*pcbOldActual*</span></span>

<span data-ttu-id="bc519-126">Получает фактический объем данных необработанных значений, полученных в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="bc519-126">Receives the actual amount of raw value data received in the output buffer.</span></span>

<span data-ttu-id="bc519-127">*грбит*</span><span class="sxs-lookup"><span data-stu-id="bc519-127">*grbit*</span></span>

<span data-ttu-id="bc519-128">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="bc519-128">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc519-129">Значение</span><span class="sxs-lookup"><span data-stu-id="bc519-129">Value</span></span></p></th>
<th><p><span data-ttu-id="bc519-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bc519-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc519-131">JET_bitEscrowNoRollback</span><span class="sxs-lookup"><span data-stu-id="bc519-131">JET_bitEscrowNoRollback</span></span></p></td>
<td><p><span data-ttu-id="bc519-132">Даже если в сеансе, выполняющем Депонированное обновление, выполняется откат транзакций, это обновление не будет отменено.</span><span class="sxs-lookup"><span data-stu-id="bc519-132">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="bc519-133">Обратите внимание, что так как записи журнала не могут быть записаны на диск, последние депонированные обновления, выполненные с помощью этого флага, могут быть утрачены в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="bc519-133">Note that as the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="bc519-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc519-134">Return Value</span></span>

<span data-ttu-id="bc519-135">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="bc519-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bc519-136">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bc519-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc519-137">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bc519-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="bc519-138">Описание</span><span class="sxs-lookup"><span data-stu-id="bc519-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc519-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bc519-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bc519-140">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bc519-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-141">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="bc519-141">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="bc519-142">У курсора есть обновление, подготовленное с помощью <a href="gg269339(v=exchg.10).md">жетпрепареупдате</a>.</span><span class="sxs-lookup"><span data-stu-id="bc519-142">The cursor has an update prepared with <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bc519-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bc519-144">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="bc519-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-145">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bc519-145">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bc519-146">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="bc519-146">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="bc519-147">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="bc519-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-148">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="bc519-148">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="bc519-149">Передан недопустимый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="bc519-149">An invalid buffer size has been passed in.</span></span> <span data-ttu-id="bc519-150">В настоящее время поддерживается только JET_coltypLong, поэтому размер буфера должен составлять 4 байта.</span><span class="sxs-lookup"><span data-stu-id="bc519-150">Currently only JET_coltypLong is supported, so the buffer must be 4 bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="bc519-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="bc519-152">Указан недопустимый столбец.</span><span class="sxs-lookup"><span data-stu-id="bc519-152">An invalid column has been specified.</span></span> <span data-ttu-id="bc519-153">Столбец должен быть создан с указанным JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="bc519-153">The column must be created with JET_bitColumnEscrowUpdate specified.</span></span> <span data-ttu-id="bc519-154">Только фиксированные столбцы JET_coltypLong можно указать как подобновляемые.</span><span class="sxs-lookup"><span data-stu-id="bc519-154">Only fixed columns of JET_coltypLong can be specified as escrow updateable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="bc519-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="bc519-156">Для обновления столбца курсор должен находиться в записи.</span><span class="sxs-lookup"><span data-stu-id="bc519-156">Cursor must be on a record in order to update a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-157">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="bc519-157">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="bc519-158">Депонированные обновления могут выполняться только сеансами транзакции.</span><span class="sxs-lookup"><span data-stu-id="bc519-158">Escrow updates can only be performed by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bc519-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bc519-160">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="bc519-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-161">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="bc519-161">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="bc519-162">Курсор не может быть доступен только для чтения и обновлять запись.</span><span class="sxs-lookup"><span data-stu-id="bc519-162">Cursor cannot be read only and update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-163">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bc519-163">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bc519-164">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="bc519-164">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-165">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bc519-165">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bc519-166">Один и тот же сеанс нельзя использовать одновременно из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="bc519-166">The same session cannot be used from more than one thread at the same time.</span></span> <span data-ttu-id="bc519-167">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="bc519-167">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-168">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bc519-168">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bc519-169">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="bc519-169">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-170">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="bc519-170">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="bc519-171">Для обновления записи сеанс должен иметь разрешения на запись.</span><span class="sxs-lookup"><span data-stu-id="bc519-171">Session must have write permissions to update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-172">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bc519-172">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="bc519-173">Ошибка, возвращенная при запросе конфликтующего обновления.</span><span class="sxs-lookup"><span data-stu-id="bc519-173">The error returned when a conflicting update is requested.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="bc519-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc519-174">Remarks</span></span>

<span data-ttu-id="bc519-175">Как правило, если два сеанса пытаются одновременно обновить запись, второй сеанс получит JET_errWriteConflict ошибку, если только сеансы не будут полностью сериализованы.</span><span class="sxs-lookup"><span data-stu-id="bc519-175">Normally, if two sessions attempt to update a record simultaneously, the second session will receive a JET_errWriteConflict error unless the sessions are completely serialized.</span></span> <span data-ttu-id="bc519-176">Чтобы сериализовать два сеанса, которые обновляют одну и ту же запись, второй сеанс должен начать свою транзакцию после того, как первая транзакция зафиксирует свою транзакцию.</span><span class="sxs-lookup"><span data-stu-id="bc519-176">To serialize two sessions that update the same record, the second session must start its transaction after the first transaction commits its transaction.</span></span> <span data-ttu-id="bc519-177">Дополнительные сведения см. в разделе [жетбегинтрансактион](./jetbegintransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="bc519-177">See [JetBeginTransaction](./jetbegintransaction-function.md) for more information.</span></span>

<span data-ttu-id="bc519-178">Несколько столбцов в одной записи можно условно обновить.</span><span class="sxs-lookup"><span data-stu-id="bc519-178">Multiple columns in the same record can be escrow updated.</span></span> <span data-ttu-id="bc519-179">Обновления не влияют друг на друга.</span><span class="sxs-lookup"><span data-stu-id="bc519-179">The updates do not affect each other.</span></span>

<span data-ttu-id="bc519-180">Только операции **жетескровупдате** совместимы друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bc519-180">Only **JetEscrowUpdate** operations are compatible with each other.</span></span> <span data-ttu-id="bc519-181">Если два разных сеанса пытаются подготовить обновления или удалить одну и ту же запись, будет создан конфликт записи.</span><span class="sxs-lookup"><span data-stu-id="bc519-181">If two different sessions try to prepare updates or delete the same record, a write conflict will be generated.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p><span data-ttu-id="bc519-182">Сеанс б</span><span class="sxs-lookup"><span data-stu-id="bc519-182">Session B</span></span><br /><span data-ttu-id="bc519-183">
<strong>жетескровупдате</strong></span><span class="sxs-lookup"><span data-stu-id="bc519-183">
<strong>JetEscrowUpdate</strong></span></span></p></th>
<th><p><span data-ttu-id="bc519-184"><a href="gg269339(v=exchg.10).md">жетпрепареупдате</a></span><span class="sxs-lookup"><span data-stu-id="bc519-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span></span></p></th>
<th><p><span data-ttu-id="bc519-185"><a href="gg269315(v=exchg.10).md">жетделете</a></span><span class="sxs-lookup"><span data-stu-id="bc519-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="bc519-186"><strong>жетескровупдате</strong></span><span class="sxs-lookup"><span data-stu-id="bc519-186"><strong>JetEscrowUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="bc519-187">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bc519-187">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bc519-188">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bc519-188">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="bc519-189">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bc519-189">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="bc519-190"><a href="gg269288(v=exchg.10).md">жетупдате</a></span><span class="sxs-lookup"><span data-stu-id="bc519-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="bc519-191">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bc519-191">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="bc519-192">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bc519-192">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="bc519-193">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bc519-193">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-194">Сеанс а</span><span class="sxs-lookup"><span data-stu-id="bc519-194">Session A</span></span></p></td>
<td><p><span data-ttu-id="bc519-195"><a href="gg269315(v=exchg.10).md">жетделете</a></span><span class="sxs-lookup"><span data-stu-id="bc519-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></td>
<td><p><span data-ttu-id="bc519-196">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bc519-196">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="bc519-197">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bc519-197">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="bc519-198">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bc519-198">JET_errWriteConflict</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bc519-199">Для депонированных операций используется версия и они отменяются с помощью [жетроллбакк](./jetrollback-function.md) (если не указано JET_bitEscrowNoRollback).</span><span class="sxs-lookup"><span data-stu-id="bc519-199">Escrow operations are versioned and are undone using [JetRollback](./jetrollback-function.md) (unless JET_bitEscrowNoRollback was specified).</span></span> <span data-ttu-id="bc519-200">**Жетескровупдате** возвращает необработанное значение столбца, хранящегося в базе данных, так как приложению может потребоваться выполнить определенное действие при попадании в значение Sentinel.</span><span class="sxs-lookup"><span data-stu-id="bc519-200">**JetEscrowUpdate** returns the raw value of the column stored in the database, because an application may want to perform a special action when a sentinel value is hit.</span></span> <span data-ttu-id="bc519-201">[Жетретриевеколумн](./jetretrievecolumn-function.md) возвращает правильное представление столбца с версиями, игнорируя обновления, сделанные параллельными сеансами.</span><span class="sxs-lookup"><span data-stu-id="bc519-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) returns the correctly versioned view of the column, ignoring updates made by concurrent sessions.</span></span>

<span data-ttu-id="bc519-202">При наличии двух сеансов, работающих в одном столбце одной и той же записи, можно увидеть, как это работает.</span><span class="sxs-lookup"><span data-stu-id="bc519-202">Given two sessions operating on the same column of the same record, we can see how this works.</span></span> <span data-ttu-id="bc519-203">Предположим, что столбец начинается со значения 0.</span><span class="sxs-lookup"><span data-stu-id="bc519-203">Assume the column starts with a value of 0.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc519-204">Сеанс</span><span class="sxs-lookup"><span data-stu-id="bc519-204">Session</span></span></p></th>
<th><p><span data-ttu-id="bc519-205">Операция</span><span class="sxs-lookup"><span data-stu-id="bc519-205">Operation</span></span></p></th>
<th><p><span data-ttu-id="bc519-206">Сохраненное значение</span><span class="sxs-lookup"><span data-stu-id="bc519-206">Stored value</span></span></p></th>
<th><p><span data-ttu-id="bc519-207">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc519-207">Returned value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc519-208">Объект</span><span class="sxs-lookup"><span data-stu-id="bc519-208">A</span></span></p></td>
<td><p><span data-ttu-id="bc519-209"><a href="gg294083(v=exchg.10).md">жетбегинтрансатион</a></span><span class="sxs-lookup"><span data-stu-id="bc519-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-210">Объект</span><span class="sxs-lookup"><span data-stu-id="bc519-210">A</span></span></p></td>
<td><p><span data-ttu-id="bc519-211"><a href="gg294083(v=exchg.10).md">жетбегинтрансатион</a></span><span class="sxs-lookup"><span data-stu-id="bc519-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bc519-212">0</span><span class="sxs-lookup"><span data-stu-id="bc519-212">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-213">Объект</span><span class="sxs-lookup"><span data-stu-id="bc519-213">A</span></span></p></td>
<td><p><span data-ttu-id="bc519-214"><strong>Жетескровупдате</strong> (4)</span><span class="sxs-lookup"><span data-stu-id="bc519-214"><strong>JetEscrowUpdate</strong> (4)</span></span></p></td>
<td><p><span data-ttu-id="bc519-215">4</span><span class="sxs-lookup"><span data-stu-id="bc519-215">4</span></span></p></td>
<td><p><span data-ttu-id="bc519-216">0</span><span class="sxs-lookup"><span data-stu-id="bc519-216">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-217">Объект</span><span class="sxs-lookup"><span data-stu-id="bc519-217">A</span></span></p></td>
<td><p><span data-ttu-id="bc519-218"><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></span><span class="sxs-lookup"><span data-stu-id="bc519-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bc519-219">4</span><span class="sxs-lookup"><span data-stu-id="bc519-219">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-220">B</span><span class="sxs-lookup"><span data-stu-id="bc519-220">B</span></span></p></td>
<td><p><span data-ttu-id="bc519-221"><a href="gg294083(v=exchg.10).md">жетбегинтрансактион</a></span><span class="sxs-lookup"><span data-stu-id="bc519-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-222">B</span><span class="sxs-lookup"><span data-stu-id="bc519-222">B</span></span></p></td>
<td><p><span data-ttu-id="bc519-223"><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></span><span class="sxs-lookup"><span data-stu-id="bc519-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bc519-224">0</span><span class="sxs-lookup"><span data-stu-id="bc519-224">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-225">B</span><span class="sxs-lookup"><span data-stu-id="bc519-225">B</span></span></p></td>
<td><p><span data-ttu-id="bc519-226"><strong>Жетескровупдате</strong> (3)</span><span class="sxs-lookup"><span data-stu-id="bc519-226"><strong>JetEscrowUpdate</strong> (3)</span></span></p></td>
<td><p><span data-ttu-id="bc519-227">7</span><span class="sxs-lookup"><span data-stu-id="bc519-227">7</span></span></p></td>
<td><p><span data-ttu-id="bc519-228">4</span><span class="sxs-lookup"><span data-stu-id="bc519-228">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-229">B</span><span class="sxs-lookup"><span data-stu-id="bc519-229">B</span></span></p></td>
<td><p><span data-ttu-id="bc519-230"><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></span><span class="sxs-lookup"><span data-stu-id="bc519-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bc519-231">3</span><span class="sxs-lookup"><span data-stu-id="bc519-231">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-232">A</span><span class="sxs-lookup"><span data-stu-id="bc519-232">A</span></span></p></td>
<td><p><span data-ttu-id="bc519-233"><strong>Жетескровупдате</strong> (2)</span><span class="sxs-lookup"><span data-stu-id="bc519-233"><strong>JetEscrowUpdate</strong> (2)</span></span></p></td>
<td><p><span data-ttu-id="bc519-234">9</span><span class="sxs-lookup"><span data-stu-id="bc519-234">9</span></span></p></td>
<td><p><span data-ttu-id="bc519-235">7</span><span class="sxs-lookup"><span data-stu-id="bc519-235">7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-236">Объект</span><span class="sxs-lookup"><span data-stu-id="bc519-236">A</span></span></p></td>
<td><p><span data-ttu-id="bc519-237"><strong>Жетескровупдате</strong> (-7)</span><span class="sxs-lookup"><span data-stu-id="bc519-237"><strong>JetEscrowUpdate</strong> (-7)</span></span></p></td>
<td><p><span data-ttu-id="bc519-238">2</span><span class="sxs-lookup"><span data-stu-id="bc519-238">2</span></span></p></td>
<td><p><span data-ttu-id="bc519-239">9</span><span class="sxs-lookup"><span data-stu-id="bc519-239">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-240">B</span><span class="sxs-lookup"><span data-stu-id="bc519-240">B</span></span></p></td>
<td><p><span data-ttu-id="bc519-241"><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></span><span class="sxs-lookup"><span data-stu-id="bc519-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bc519-242">3</span><span class="sxs-lookup"><span data-stu-id="bc519-242">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-243">A</span><span class="sxs-lookup"><span data-stu-id="bc519-243">A</span></span></p></td>
<td><p><span data-ttu-id="bc519-244"><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></span><span class="sxs-lookup"><span data-stu-id="bc519-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bc519-245">-1</span><span class="sxs-lookup"><span data-stu-id="bc519-245">-1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-246">B</span><span class="sxs-lookup"><span data-stu-id="bc519-246">B</span></span></p></td>
<td><p><span data-ttu-id="bc519-247"><a href="gg269273(v=exchg.10).md">жетроллбакк</a></span><span class="sxs-lookup"><span data-stu-id="bc519-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span></span></p></td>
<td><p><span data-ttu-id="bc519-248">-1</span><span class="sxs-lookup"><span data-stu-id="bc519-248">-1</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-249">Объект</span><span class="sxs-lookup"><span data-stu-id="bc519-249">A</span></span></p></td>
<td><p><span data-ttu-id="bc519-250"><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></span><span class="sxs-lookup"><span data-stu-id="bc519-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bc519-251">-1</span><span class="sxs-lookup"><span data-stu-id="bc519-251">-1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bc519-252">Не рекомендуется заменять запись в той же транзакции, которая выполняет депонированные обновления записи.</span><span class="sxs-lookup"><span data-stu-id="bc519-252">Replacing a record in the same transaction that performs escrow updates to a record is not recommended.</span></span> <span data-ttu-id="bc519-253">В частности, если обновление записи подготовлено с помощью одной [JET_TABLEID](./jet-tableid.md) и для депонирования обновления записи используется другая [JET_TABLEID](./jet-tableid.md) , то при вызове [жетупдате](./jetupdate-function.md) будет утрачено значение «условно Обновлено».</span><span class="sxs-lookup"><span data-stu-id="bc519-253">In particular, if an update on a record is prepared with one [JET_TABLEID](./jet-tableid.md) and a different [JET_TABLEID](./jet-tableid.md) is used to escrow update the record then the escrow updated will be lost when [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="bc519-254">Это происходит, даже если во время обновления не был задан депонированный столбец.</span><span class="sxs-lookup"><span data-stu-id="bc519-254">This happens even if the escrow column was not set during the update.</span></span>

<span data-ttu-id="bc519-255">Если столбец с подобновляемым значением имеет нулевое значение, можно запустить специальное поведение.</span><span class="sxs-lookup"><span data-stu-id="bc519-255">When an escrow updateable column has a value of zero, special behavior can be triggered.</span></span> <span data-ttu-id="bc519-256">Такое поведение происходит только в том случае, если операция **жетескровупдате** приводит к тому, что столбец имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="bc519-256">This behavior only happens if a **JetEscrowUpdate** operation causes the column to have a value of zero.</span></span> <span data-ttu-id="bc519-257">Действие не происходит немедленно, но происходит после транзакции, которая привела к тому, что столбец имеет нулевое значение фиксаций.</span><span class="sxs-lookup"><span data-stu-id="bc519-257">The action does not happen immediately, but occurs sometime after the transaction which caused the column to have a value of zero commits.</span></span> <span data-ttu-id="bc519-258">Столбец по-прежнему должен иметь нулевое значение (т. е. Если другие сеансы не изменили столбец).</span><span class="sxs-lookup"><span data-stu-id="bc519-258">The column must still have a value of zero (that is, if no other sessions have modified the column).</span></span> <span data-ttu-id="bc519-259">Если столбец был создан с помощью JET_bitColumnDeleteOnZero, то запись, содержащая столбец, будет удалена.</span><span class="sxs-lookup"><span data-stu-id="bc519-259">If the column was created with JET_bitColumnDeleteOnZero, the record containing the column will be deleted.</span></span> <span data-ttu-id="bc519-260">Если столбец был создан с JET_bitColumnFinalize то будет выдан обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="bc519-260">If the column was created with JET_bitColumnFinalize then a callback will be issued.</span></span> <span data-ttu-id="bc519-261">Сбой может привести к тому, что эти действия не будут выполняться, но оперативное обслуживание (с помощью функции [жетдефрагмент](./jetdefragment-function.md) ) будет правильно повторять действия.</span><span class="sxs-lookup"><span data-stu-id="bc519-261">A crash may cause these actions not to happen, but online maintenance (using the [JetDefragment](./jetdefragment-function.md) function) will correctly redo the actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bc519-262">Требования</span><span class="sxs-lookup"><span data-stu-id="bc519-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc519-263"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="bc519-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bc519-264">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bc519-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-265"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bc519-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bc519-266">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bc519-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-267"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bc519-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bc519-268">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bc519-268">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc519-269"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="bc519-269"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bc519-270">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bc519-270">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc519-271"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="bc519-271"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bc519-272">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bc519-272">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bc519-273">См. также:</span><span class="sxs-lookup"><span data-stu-id="bc519-273">See Also</span></span>

[<span data-ttu-id="bc519-274">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="bc519-274">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="bc519-275">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bc519-275">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bc519-276">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bc519-276">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bc519-277">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bc519-277">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bc519-278">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bc519-278">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bc519-279">жетбегинтрансактион</span><span class="sxs-lookup"><span data-stu-id="bc519-279">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="bc519-280">жетдефрагмент</span><span class="sxs-lookup"><span data-stu-id="bc519-280">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="bc519-281">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="bc519-281">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="bc519-282">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="bc519-282">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="bc519-283">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="bc519-283">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="bc519-284">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="bc519-284">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="bc519-285">жетупдате</span><span class="sxs-lookup"><span data-stu-id="bc519-285">JetUpdate</span></span>](./jetupdate-function.md)
