---
description: Дополнительные сведения о функции Жеткоммиттрансактион
title: Функция JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999441"
---
# <a name="jetcommittransaction-function"></a><span data-ttu-id="63a40-103">Функция JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="63a40-103">JetCommitTransaction Function</span></span>


<span data-ttu-id="63a40-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="63a40-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcommittransaction-function"></a><span data-ttu-id="63a40-105">Функция JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="63a40-105">JetCommitTransaction Function</span></span>

<span data-ttu-id="63a40-106">Функция **жеткоммиттрансактион** фиксирует изменения, внесенные в состояние базы данных во время текущей точки сохранения, и переносит их в предыдущую точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="63a40-106">The **JetCommitTransaction** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="63a40-107">При фиксации самой внешней точки сохранения изменения, внесенные во время этой точки сохранения, будут зафиксированы в состоянии базы данных, и сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="63a40-107">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="63a40-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="63a40-108">Parameters</span></span>

<span data-ttu-id="63a40-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="63a40-109">*sesid*</span></span>

<span data-ttu-id="63a40-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="63a40-110">The session to use for this call.</span></span>

<span data-ttu-id="63a40-111">*грбит*</span><span class="sxs-lookup"><span data-stu-id="63a40-111">*grbit*</span></span>

<span data-ttu-id="63a40-112">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="63a40-112">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63a40-113">Значение</span><span class="sxs-lookup"><span data-stu-id="63a40-113">Value</span></span></p></th>
<th><p><span data-ttu-id="63a40-114">Значение</span><span class="sxs-lookup"><span data-stu-id="63a40-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63a40-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="63a40-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="63a40-116">Транзакция фиксируется обычным образом, но этот API не ждет сброса транзакции в файл журнала транзакций перед возвратом вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="63a40-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="63a40-117">Это радикально сокращает продолжительность операции фиксации за счет устойчивости.</span><span class="sxs-lookup"><span data-stu-id="63a40-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="63a40-118">Любая транзакция, которая не сброшена в журнал до сбоя, будет автоматически прервана во время восстановления после сбоя во время следующего вызова <a href="gg294068(v=exchg.10).md">жетинит</a>.</span><span class="sxs-lookup"><span data-stu-id="63a40-118">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to <a href="gg294068(v=exchg.10).md">JetInit</a>.</span></span></p>
<p><span data-ttu-id="63a40-119">Если указаны JET_bitWaitLastLevel0Commit или JET_bitWaitAllLevel0Commit, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="63a40-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="63a40-120">Если этот вызов к <strong>жеткоммиттрансактион</strong> не соответствует первому вызову <a href="gg294083(v=exchg.10).md">жетбегинтрансактион</a> для этого сеанса, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="63a40-120">If this call to <strong>JetCommitTransaction</strong> does not match the first call to <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> for this session, this option is ignored.</span></span> <span data-ttu-id="63a40-121">Это связано с тем, что последнее действие, выполняемое на самой внешней точке сохранения, является определяющим фактором в том, фиксируется ли вся транзакция на диске.</span><span class="sxs-lookup"><span data-stu-id="63a40-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63a40-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="63a40-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="63a40-123">Все транзакции, ранее зафиксированные любым сеансом, которые еще не были сброшены в файл журнала транзакций, будут сброшены немедленно.</span><span class="sxs-lookup"><span data-stu-id="63a40-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="63a40-124">Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="63a40-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="63a40-125">Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="63a40-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="63a40-126">Этот параметр нельзя использовать в сочетании с любым другим параметром.</span><span class="sxs-lookup"><span data-stu-id="63a40-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="63a40-127">Этот параметр доступен только в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="63a40-127">This option is only available as of Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63a40-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="63a40-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="63a40-129">Если в сеансе ранее зафиксированы транзакции и они еще не были записаны в файл журнала транзакций, они должны быть сброшены немедленно.</span><span class="sxs-lookup"><span data-stu-id="63a40-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="63a40-130">Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="63a40-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="63a40-131">Это полезно, если приложение ранее зафиксировало несколько транзакций с помощью JET_bitCommitLazyFlush и теперь хочет сбросить все эти транзакции на диск.</span><span class="sxs-lookup"><span data-stu-id="63a40-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="63a40-132">Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="63a40-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="63a40-133">Этот параметр нельзя использовать в сочетании с любым другим параметром.</span><span class="sxs-lookup"><span data-stu-id="63a40-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="63a40-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63a40-134">Return Value</span></span>

<span data-ttu-id="63a40-135">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="63a40-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="63a40-136">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="63a40-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63a40-137">Код возврата</span><span class="sxs-lookup"><span data-stu-id="63a40-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="63a40-138">Описание</span><span class="sxs-lookup"><span data-stu-id="63a40-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63a40-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="63a40-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="63a40-140">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="63a40-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63a40-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="63a40-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="63a40-142">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="63a40-142">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63a40-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="63a40-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="63a40-144">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="63a40-144">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="63a40-145">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="63a40-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63a40-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="63a40-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="63a40-147">Один из запрошенных параметров недопустим или не реализован.</span><span class="sxs-lookup"><span data-stu-id="63a40-147">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="63a40-148">Эта ошибка будет возвращена <strong>жеткоммиттрансактион</strong> в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="63a40-148">This error will be returned by <strong>JetCommitTransaction</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="63a40-149">Указан недопустимый <em>грбит</em> .</span><span class="sxs-lookup"><span data-stu-id="63a40-149">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="63a40-150">JET_bitWaitLastLevel0Commit был указан в сочетании с другой <em>грбит</em>.</span><span class="sxs-lookup"><span data-stu-id="63a40-150">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="63a40-151">JET_bitWaitAllLevel0Commit был указан в сочетании с другой <em>грбит</em>.</span><span class="sxs-lookup"><span data-stu-id="63a40-151">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63a40-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="63a40-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="63a40-153">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="63a40-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63a40-154">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="63a40-154">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="63a40-155">Не удалось выполнить операцию, так как данный сеанс не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="63a40-155">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63a40-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="63a40-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="63a40-157">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="63a40-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63a40-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="63a40-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="63a40-159">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="63a40-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="63a40-160">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="63a40-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63a40-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="63a40-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="63a40-162">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="63a40-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="63a40-163">При успешном выполнении все изменения, внесенные в базу данных во время текущей точки сохранения для данного сеанса, будут зафиксированы, а точка сохранения будет закончена.</span><span class="sxs-lookup"><span data-stu-id="63a40-163">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="63a40-164">Если последняя точка сохранения сеанса была завершена, транзакция при необходимости будет записана в файл журнала транзакций, и сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="63a40-164">If the last save point for the session was ended then the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="63a40-165">В случае сбоя состояние транзакции сеанса останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="63a40-165">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="63a40-166">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63a40-166">No change to the database state will occur.</span></span> <span data-ttu-id="63a40-167">Чтобы прервать транзакцию, приложение должно вызвать [жетроллбакк](./jetrollback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="63a40-167">The application should call [JetRollback](./jetrollback-function.md) to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63a40-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63a40-168">Remarks</span></span>

<span data-ttu-id="63a40-169">Должен быть один вызов **жеткоммиттрансактион** или [жетроллбакк](./jetrollback-function.md) для сопоставления каждого вызова [жетбегинтрансактион](./jetbegintransaction-function.md) для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="63a40-169">There must be one call to **JetCommitTransaction** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="63a40-170">Требования</span><span class="sxs-lookup"><span data-stu-id="63a40-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63a40-171"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="63a40-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="63a40-172">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="63a40-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63a40-173"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="63a40-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="63a40-174">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="63a40-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63a40-175"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="63a40-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="63a40-176">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="63a40-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63a40-177"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="63a40-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="63a40-178">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="63a40-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63a40-179"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="63a40-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="63a40-180">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="63a40-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="63a40-181">См. также:</span><span class="sxs-lookup"><span data-stu-id="63a40-181">See Also</span></span>

[<span data-ttu-id="63a40-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="63a40-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="63a40-183">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="63a40-183">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="63a40-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="63a40-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="63a40-185">жетбегинтрансактион</span><span class="sxs-lookup"><span data-stu-id="63a40-185">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="63a40-186">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="63a40-186">JetCommitTransaction</span></span>]()  
[<span data-ttu-id="63a40-187">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="63a40-187">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="63a40-188">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="63a40-188">JetStopService</span></span>](./jetstopservice-function.md)
