---
description: Дополнительные сведения о функции JetCommitTransaction2
title: Функция JetCommitTransaction2
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712870"
---
# <a name="jetcommittransaction2-function"></a><span data-ttu-id="e9dfe-103">Функция JetCommitTransaction2</span><span class="sxs-lookup"><span data-stu-id="e9dfe-103">JetCommitTransaction2 Function</span></span>


<span data-ttu-id="e9dfe-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e9dfe-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="e9dfe-105">Функция **JetCommitTransaction2** фиксирует изменения, внесенные в состояние базы данных во время текущей точки сохранения, и переносит их в предыдущую точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-105">The **JetCommitTransaction2** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="e9dfe-106">При фиксации самой внешней точки сохранения изменения, внесенные во время этой точки сохранения, будут зафиксированы в состоянии базы данных, и сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-106">If the outermost save point is committed, the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="e9dfe-107">Функция **JetCommitTransaction2** была введена в операционной системе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-107">The **JetCommitTransaction2** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a><span data-ttu-id="e9dfe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9dfe-108">Parameters</span></span>

<span data-ttu-id="e9dfe-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="e9dfe-109">*sesid*</span></span>

<span data-ttu-id="e9dfe-110">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-110">The session to use for this call.</span></span>

<span data-ttu-id="e9dfe-111">*грбит*</span><span class="sxs-lookup"><span data-stu-id="e9dfe-111">*grbit*</span></span>

<span data-ttu-id="e9dfe-112">Группа битов, задающих ноль или более значений, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-112">A group of bits that specify zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9dfe-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e9dfe-113">Value</span></span></p></th>
<th><p><span data-ttu-id="e9dfe-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e9dfe-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="e9dfe-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-116">Транзакция фиксируется обычным образом, но этот API не ждет сброса транзакции в файл журнала транзакций перед возвратом вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="e9dfe-117">Это радикально сокращает продолжительность операции фиксации за счет устойчивости.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="e9dfe-118">Любая транзакция, которая не записывается в журнал до сбоя, будет автоматически прервана во время восстановления после сбоя во время следующего вызова функции <a href="gg294068(v=exchg.10).md">жетинит</a> .</span><span class="sxs-lookup"><span data-stu-id="e9dfe-118">Any transaction that is not flushed to the log before a crash will automatically be aborted during crash recovery during the next call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function.</span></span></p>
<p><span data-ttu-id="e9dfe-119">Если указаны JET_bitWaitLastLevel0Commit или JET_bitWaitAllLevel0Commit, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="e9dfe-120">Если этот вызов к <strong>JetCommitTransaction2</strong> не соответствует первому вызову функции <a href="gg294083(v=exchg.10).md">жетбегинтрансактион</a> для этого сеанса, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-120">If this call to <strong>JetCommitTransaction2</strong> does not match the first call to the <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> function for this session, this option is ignored.</span></span> <span data-ttu-id="e9dfe-121">Это связано с тем, что последнее действие, выполняемое на самой внешней точке сохранения, является определяющим фактором в том, фиксируется ли вся транзакция на диске.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dfe-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="e9dfe-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-123">Все транзакции, ранее зафиксированные любым сеансом, которые еще не были сброшены в файл журнала транзакций, будут сброшены немедленно.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="e9dfe-124">Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="e9dfe-125">Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="e9dfe-126">Этот параметр нельзя использовать в сочетании с любым другим параметром.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="e9dfe-127">Этот параметр доступен в версиях операционной системы Windows Server, начиная с Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-127">This option is available in versions of the Windows Server operating system starting with Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="e9dfe-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-129">Если в сеансе ранее зафиксированы транзакции и они еще не были записаны в файл журнала транзакций, они должны быть сброшены немедленно.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="e9dfe-130">Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="e9dfe-131">Это полезно, если приложение ранее зафиксировало несколько транзакций с помощью JET_bitCommitLazyFlush и теперь хочет сбросить все эти транзакции на диск.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="e9dfe-132">Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="e9dfe-133">Этот параметр нельзя использовать в сочетании с любым другим параметром.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e9dfe-134">*кмсекдураблекоммит*</span><span class="sxs-lookup"><span data-stu-id="e9dfe-134">*cmsecDurableCommit*</span></span>

<span data-ttu-id="e9dfe-135">Продолжительность фиксации отложенной транзакции.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-135">The duration to commit a lazy transaction.</span></span>

<span data-ttu-id="e9dfe-136">*пкоммитид*</span><span class="sxs-lookup"><span data-stu-id="e9dfe-136">*pCommitID*</span></span>

<span data-ttu-id="e9dfe-137">Идентификатор фиксации, связанный с этой записью фиксации.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-137">The Commit-ID associated with this commit record.</span></span>

### <a name="return-value"></a><span data-ttu-id="e9dfe-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9dfe-138">Return value</span></span>

<span data-ttu-id="e9dfe-139">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-139">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="e9dfe-140">Дополнительные сведения о возможных ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e9dfe-140">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9dfe-141">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e9dfe-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="e9dfe-142">Описание</span><span class="sxs-lookup"><span data-stu-id="e9dfe-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e9dfe-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-144">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dfe-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e9dfe-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-146">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова функции <a href="gg269240(v=exchg.10).md">жетстопсервице</a> .</span><span class="sxs-lookup"><span data-stu-id="e9dfe-146">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e9dfe-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-148">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e9dfe-149">Эта ошибка будет возвращена только версиями операционной системы Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-149">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dfe-150">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="e9dfe-150">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-151">Один из запрошенных параметров недопустим или не реализован.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-151">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="e9dfe-152">Эта ошибка будет возвращена функцией <strong>JetCommitTransaction2</strong> , когда происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="e9dfe-152">This error will be returned by the <strong>JetCommitTransaction2</strong> function when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="e9dfe-153">Указан недопустимый <em>грбит</em> .</span><span class="sxs-lookup"><span data-stu-id="e9dfe-153">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="e9dfe-154">JET_bitWaitLastLevel0Commit был указан в сочетании с другой <em>грбит</em>.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-154">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="e9dfe-155">JET_bitWaitAllLevel0Commit был указан в сочетании с другой <em>грбит</em>.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-155">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e9dfe-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-157">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dfe-158">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="e9dfe-158">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-159">Не удалось выполнить операцию, так как данный сеанс не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-159">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e9dfe-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-161">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dfe-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e9dfe-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-163">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-163">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="e9dfe-164">Эта ошибка будет возвращена только версиями операционной системы Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-164">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e9dfe-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e9dfe-166">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e9dfe-167">При успешном выполнении все изменения, внесенные в базу данных во время текущей точки сохранения для данного сеанса, будут зафиксированы, а точка сохранения будет закончена.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-167">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="e9dfe-168">Если последняя точка сохранения сеанса была завершена, транзакция при необходимости будет сброшена в файл журнала транзакций, и сеанс завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-168">If the last save point for the session was ended, the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="e9dfe-169">В случае сбоя состояние транзакции сеанса останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-169">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="e9dfe-170">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-170">No change to the database state will occur.</span></span> <span data-ttu-id="e9dfe-171">Чтобы прервать транзакцию, приложение должно вызвать функцию [жетроллбакк](./jetrollback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e9dfe-171">The application should call the [JetRollback](./jetrollback-function.md) function to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e9dfe-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9dfe-172">Remarks</span></span>

<span data-ttu-id="e9dfe-173">Должен быть один вызов **JetCommitTransaction2** или [жетроллбакк](./jetrollback-function.md) для сопоставления каждого вызова [жетбегинтрансактион](./jetbegintransaction-function.md) для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-173">There must be one call to **JetCommitTransaction2** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e9dfe-174">Требования</span><span class="sxs-lookup"><span data-stu-id="e9dfe-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-175"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="e9dfe-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e9dfe-176">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-176">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dfe-177"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e9dfe-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e9dfe-178">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-178">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-179"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e9dfe-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e9dfe-180">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dfe-181"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="e9dfe-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e9dfe-182">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dfe-183"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="e9dfe-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e9dfe-184">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e9dfe-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e9dfe-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9dfe-185">See also</span></span>

[<span data-ttu-id="e9dfe-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e9dfe-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e9dfe-187">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e9dfe-187">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e9dfe-188">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e9dfe-188">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e9dfe-189">жетбегинтрансактион</span><span class="sxs-lookup"><span data-stu-id="e9dfe-189">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="e9dfe-190">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="e9dfe-190">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="e9dfe-191">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="e9dfe-191">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="e9dfe-192">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="e9dfe-192">JetStopService</span></span>](./jetstopservice-function.md)
