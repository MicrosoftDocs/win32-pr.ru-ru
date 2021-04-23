---
description: Дополнительные сведения о функции Жетжетлокк
title: Функция Жетжетлокк
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104157279"
---
# <a name="jetgetlock-function"></a><span data-ttu-id="9e4ba-103">Функция Жетжетлокк</span><span class="sxs-lookup"><span data-stu-id="9e4ba-103">JetGetLock Function</span></span>


<span data-ttu-id="9e4ba-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9e4ba-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetlock-function"></a><span data-ttu-id="9e4ba-105">Функция Жетжетлокк</span><span class="sxs-lookup"><span data-stu-id="9e4ba-105">JetGetLock Function</span></span>

<span data-ttu-id="9e4ba-106">Функция **жетжетлокк** предоставляет средства для явного резервирования возможности обновления строки, блокировки записи или явного предотвращения обновления строки любым другим сеансом, блокировки чтения.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-106">The **JetGetLock** function provides a means to explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="9e4ba-107">Обычно блокировки записи строк получаются неявно в результате обновления строк.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-107">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="9e4ba-108">Блокировки чтения обычно не требуются из-за управления версиями записей.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-108">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="9e4ba-109">Однако в некоторых случаях транзакция может потребовать явно заблокировать строку для принудительного применения сериализации или убедиться, что последующая операция будет выполнена успешно, предуверенной в том, что необходимые блокировки уже выполнены.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-109">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed by virtue that required locks have already been taken.</span></span>

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="9e4ba-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e4ba-110">Parameters</span></span>

<span data-ttu-id="9e4ba-111">*сесид*</span><span class="sxs-lookup"><span data-stu-id="9e4ba-111">*sesid*</span></span>

<span data-ttu-id="9e4ba-112">Сеанс, который будет использоваться для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-112">The session that will be used for this call.</span></span>

<span data-ttu-id="9e4ba-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9e4ba-113">*tableid*</span></span>

<span data-ttu-id="9e4ba-114">Курсор, который будет использоваться для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-114">The cursor that will be used for this call.</span></span>

<span data-ttu-id="9e4ba-115">*грбит*</span><span class="sxs-lookup"><span data-stu-id="9e4ba-115">*grbit*</span></span>

<span data-ttu-id="9e4ba-116">Группа битов, содержащая параметры, которые должны использоваться для этого вызова, в том числе ноль или более следующих:</span><span class="sxs-lookup"><span data-stu-id="9e4ba-116">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e4ba-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9e4ba-117">Value</span></span></p></th>
<th><p><span data-ttu-id="9e4ba-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9e4ba-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-119">JET_bitReadLock</span><span class="sxs-lookup"><span data-stu-id="9e4ba-119">JET_bitReadLock</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-120">Этот флаг приводит к получению блокировки чтения для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-120">This flag causes a read lock to be acquired on the current record.</span></span> <span data-ttu-id="9e4ba-121">Блокировки чтения несовместимы с блокировками записи, уже удерживаемыми другими сеансами, но совместимы с блокировками чтения, удерживаемыми другими сеансами.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-121">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4ba-122">JET_bitWriteLock</span><span class="sxs-lookup"><span data-stu-id="9e4ba-122">JET_bitWriteLock</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-123">Этот флаг приводит к получению блокировки записи для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-123">This flag causes a write lock to be acquired on the current record.</span></span> <span data-ttu-id="9e4ba-124">Блокировки записи несовместимы с блокировками записи или чтения, удерживаемыми другими сеансами, но совместимы с блокировками чтения, удерживаемыми в одном сеансе.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-124">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9e4ba-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e4ba-125">Return Value</span></span>

<span data-ttu-id="9e4ba-126">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9e4ba-127">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9e4ba-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e4ba-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9e4ba-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="9e4ba-129">Описание</span><span class="sxs-lookup"><span data-stu-id="9e4ba-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9e4ba-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-131">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4ba-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9e4ba-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-133">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9e4ba-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-135">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="9e4ba-136">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4ba-137">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="9e4ba-137">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-138">Данный <em>грбит</em> не является ни JET_bitReadLock, ни JET_bitWriteLock.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-138">The given <em>grbit</em> is neither JET_bitReadLock or JET_bitWriteLock.</span></span> <span data-ttu-id="9e4ba-139">Это должен быть один из этих двух флагов.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-139">It must be one of these two flags.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-140">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="9e4ba-140">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-141">Для получения блокировки курсор должен находиться в записи.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-141">Cursor must be on a record in order to acquire a lock.</span></span> <span data-ttu-id="9e4ba-142">Блокировки — это записи Always on.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-142">Locks are always on records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4ba-143">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9e4ba-143">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-144">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-144">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-145">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="9e4ba-145">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-146">Блокировки могут быть получены только сеансами транзакции.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-146">Locks can only be acquired by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4ba-147">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="9e4ba-147">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-148">Курсор не может быть доступен только для чтения и получить блокировку записи.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-148">Cursor cannot be read only and acquire a write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9e4ba-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-150">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4ba-151">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9e4ba-151">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-152">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-152">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="9e4ba-153">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-153">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9e4ba-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-155">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4ba-156">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="9e4ba-156">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-157">Сеанс должен иметь разрешения на запись для получения блокировки записи.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-157">Session must have write permissions to acquire write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-158">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="9e4ba-158">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="9e4ba-159">Ошибка, возвращенная при запросе конфликтующей блокировки.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-159">The error returned when a conflicting lock is requested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e4ba-160">При успешном выполнении сеанс получил запрошенную блокировку.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-160">On success, session has acquired requested lock.</span></span>

<span data-ttu-id="9e4ba-161">В случае сбоя сеанс не получил запрошенную блокировку.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-161">On failure, session has not acquired requested lock.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9e4ba-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e4ba-162">Remarks</span></span>

<span data-ttu-id="9e4ba-163">Блокировка записи не может быть получена с сеансами или курсорами, имеющими разрешения только для чтения, даже если сеанс и курсор в конечном итоге не выполняют операции обновления.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-163">Write locks cannot be acquired with sessions or cursors that have read-only permissions, even if the session and cursor ultimately do not perform an update operation.</span></span> <span data-ttu-id="9e4ba-164">Как сеанс, так и курсор должны иметь права записи, чтобы получить блокировку записи.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-164">Both the session and the cursor must have write privileges in order to acquire a write lock.</span></span>

<span data-ttu-id="9e4ba-165">Блокировки чтения и записи являются средством пессимистической блокировки.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-165">Read and write locks are a means of pessimistic locking.</span></span> <span data-ttu-id="9e4ba-166">Пессимистическая блокировка ждет, что несколько параллельных сеансов конфликтуют и заранее запрашивают блокировки, чтобы гарантировать, что их операции завершаются.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-166">Pessimistic locking expects multiple concurrent sessions to conflict and acquire locks in advance to ensure that their operations succeed.</span></span>

<span data-ttu-id="9e4ba-167">Большинство операций будет сериализуемым путем неявного выполнения блокировок.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-167">Most operations will be serializable by virtue of locks implicitly taken.</span></span> <span data-ttu-id="9e4ba-168">Однако некоторые операции не будут.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-168">However, some operations will not.</span></span> <span data-ttu-id="9e4ba-169">Чтобы проиллюстрировать это, рассмотрим две транзакции:</span><span class="sxs-lookup"><span data-stu-id="9e4ba-169">To illustrate this, consider the two transactions,</span></span>

<span data-ttu-id="9e4ba-170">T1: R (A), U (B)</span><span class="sxs-lookup"><span data-stu-id="9e4ba-170">T1 : R(A), U(B)</span></span>

<span data-ttu-id="9e4ba-171">T2: R (B), U (A)</span><span class="sxs-lookup"><span data-stu-id="9e4ba-171">T2 : R(B), U(A)</span></span>

<span data-ttu-id="9e4ba-172">Управление версиями на уровне записей гарантирует, что при одновременном выполнении каждой транзакции будут видны исходные значения A и B. Нет последовательного порядка выполнения, который может получить те же результаты для и B в случае, если результаты зависят от считываемых данных.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-172">Record level versioning will ensure that each transaction when executed concurrently will see the original values for A and B. There is no serial order of execution that could produce the same results for A and B in the case that the results are dependent upon the data read.</span></span> <span data-ttu-id="9e4ba-173">Чтобы приложение мог сделать эту транзакцию сериализуемой, она должна получить явную блокировку чтения для A и B в каждой транзакции при считывании значения.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-173">In order for the application to make this transaction serializable, it should acquire an explicit read lock on A and B in each transaction when the value is read.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9e4ba-174">Требования</span><span class="sxs-lookup"><span data-stu-id="9e4ba-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-175"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9e4ba-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4ba-176">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-176">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4ba-177"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9e4ba-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4ba-178">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-178">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-179"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9e4ba-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4ba-180">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4ba-181"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="9e4ba-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4ba-182">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4ba-183"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="9e4ba-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4ba-184">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9e4ba-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9e4ba-185">См. также:</span><span class="sxs-lookup"><span data-stu-id="9e4ba-185">See Also</span></span>

[<span data-ttu-id="9e4ba-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9e4ba-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9e4ba-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9e4ba-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9e4ba-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9e4ba-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9e4ba-189">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="9e4ba-189">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="9e4ba-190">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="9e4ba-190">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="9e4ba-191">жетупдате</span><span class="sxs-lookup"><span data-stu-id="9e4ba-191">JetUpdate</span></span>](./jetupdate-function.md)
