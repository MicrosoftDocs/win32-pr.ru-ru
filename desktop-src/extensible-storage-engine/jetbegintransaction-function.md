---
description: Дополнительные сведения о функции Жетбегинтрансактион
title: Функция JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342665"
---
# <a name="jetbegintransaction-function"></a><span data-ttu-id="d6625-103">Функция JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="d6625-103">JetBeginTransaction Function</span></span>


<span data-ttu-id="d6625-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d6625-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction-function"></a><span data-ttu-id="d6625-105">Функция JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="d6625-105">JetBeginTransaction Function</span></span>

<span data-ttu-id="d6625-106">Функция **жетбегинтрансактион** заставляет сеанс войти в транзакцию и создать новую точку сохранения.</span><span class="sxs-lookup"><span data-stu-id="d6625-106">The **JetBeginTransaction** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="d6625-107">Эту функцию можно вызвать несколько раз в одном сеансе, чтобы создать дополнительные точки сохранения.</span><span class="sxs-lookup"><span data-stu-id="d6625-107">This function can be called more than once on a single session to cause the creation of additional save points.</span></span> <span data-ttu-id="d6625-108">Эти точки сохранения можно использовать для выборочного сохранения или отмены изменений состояния базы данных.</span><span class="sxs-lookup"><span data-stu-id="d6625-108">These save points can be used to selectively keep or discard changes to the state of the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="d6625-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6625-109">Parameters</span></span>

<span data-ttu-id="d6625-110">*сесид*</span><span class="sxs-lookup"><span data-stu-id="d6625-110">*sesid*</span></span>

<span data-ttu-id="d6625-111">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="d6625-111">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="d6625-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6625-112">Return Value</span></span>

<span data-ttu-id="d6625-113">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="d6625-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d6625-114">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d6625-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6625-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d6625-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="d6625-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d6625-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6625-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d6625-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d6625-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d6625-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6625-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d6625-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d6625-120">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="d6625-120">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6625-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d6625-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d6625-122">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="d6625-122">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d6625-123">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="d6625-123">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6625-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d6625-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d6625-125">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="d6625-125">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6625-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d6625-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d6625-127">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="d6625-127">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6625-128">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d6625-128">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d6625-129">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="d6625-129">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="d6625-130">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="d6625-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6625-131">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d6625-131">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d6625-132">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="d6625-132">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6625-133">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="d6625-133">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="d6625-134">Не удается запустить новую транзакцию, так как сеанс уже находится в максимально допустимой глубины точки сохранения в ядре СУБД.</span><span class="sxs-lookup"><span data-stu-id="d6625-134">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6625-135">При успешном выполнении указанный сеанс будет находиться внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="d6625-135">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="d6625-136">Если сеанс был ранее внутри транзакции, будет создана новая точка сохранения.</span><span class="sxs-lookup"><span data-stu-id="d6625-136">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="d6625-137">В случае сбоя состояние транзакции сеанса останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="d6625-137">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="d6625-138">Изменение состояния базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6625-138">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d6625-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6625-139">Remarks</span></span>

<span data-ttu-id="d6625-140">Ядро СУБД предоставляет модель изоляции моментального снимка для своих транзакций.</span><span class="sxs-lookup"><span data-stu-id="d6625-140">The database engine provides a snapshot isolation model for its transactions.</span></span> <span data-ttu-id="d6625-141">Это означает, что при первом входе в транзакционное состояние сеанс будет видеть всю базу данных в момент начала транзакции.</span><span class="sxs-lookup"><span data-stu-id="d6625-141">This means that, when a session first enters into a transactional state, the session will see the entire database frozen in time at the start of the transaction.</span></span> <span data-ttu-id="d6625-142">Сеансу не требуется считывать данные блокировки, так как он всегда может обращаться к соответствующей версии этих данных.</span><span class="sxs-lookup"><span data-stu-id="d6625-142">A session does not need to read lock any data because it can always access the appropriate version of that data.</span></span> <span data-ttu-id="d6625-143">Это означает, что сеанс, который обновляет данные, никогда не будет блокировать считывание этих данных другим сеансом.</span><span class="sxs-lookup"><span data-stu-id="d6625-143">This means that a session that is updating data will never block a different session from reading that data.</span></span>

<span data-ttu-id="d6625-144">Еще одним следствием использования изоляции моментального снимка является модель блокировки, используемая для обновлений.</span><span class="sxs-lookup"><span data-stu-id="d6625-144">Another implication of the use of snapshot isolation is the locking model used for updates.</span></span> <span data-ttu-id="d6625-145">Ядро СУБД будет выставлять блокировку записи для определенного фрагмента данных в первый сеанс, запрашивающий его.</span><span class="sxs-lookup"><span data-stu-id="d6625-145">The database engine will award a write lock on a given piece of data to the first session that requests it.</span></span> <span data-ttu-id="d6625-146">Эта блокировка записи освобождается, когда транзакция зафиксирована или прервана полностью, так что сеанс больше не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="d6625-146">This write lock is released when the transaction is either committed or aborted completely such that the session is no longer in a transaction.</span></span> <span data-ttu-id="d6625-147">Пока сеанс удерживает блокировку записи, любой другой сеанс, запрашивающий ту же блокировку записи, не будет блокироваться до тех пор, пока не станет доступной блокировка записи.</span><span class="sxs-lookup"><span data-stu-id="d6625-147">While a session holds a write lock, any other session that requests the same write lock will not block until the write lock is available.</span></span> <span data-ttu-id="d6625-148">Вместо этого второй сеанс немедленно завершится сбоем с JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="d6625-148">Rather, that second session will immediately fail with JET_errWriteConflict.</span></span> <span data-ttu-id="d6625-149">Чтобы устранить этот конфликт, второй сеанс должен полностью прервать (или зафиксировать) его транзакцию, дождаться некоторого небольшого периода времени, в течение которого первый сеанс зафиксирует или прекратит свою транзакцию, а затем снова запустите все снова.</span><span class="sxs-lookup"><span data-stu-id="d6625-149">To resolve this conflict, the second session must abort (or commit) its transaction completely, wait some small period of time for the first session to commit or abort its transaction, and then start all over again.</span></span>

<span data-ttu-id="d6625-150">В поддержку изоляции моментального снимка ядро СУБД сохраняет все версии всех измененных данных в памяти с момента первого запуска самой старой активной транзакции в любом сеансе.</span><span class="sxs-lookup"><span data-stu-id="d6625-150">In support of snapshot isolation, the database engine stores all versions of all modified data in memory since the time when the oldest active transaction on any session was first started.</span></span> <span data-ttu-id="d6625-151">Это имеет важные последствия для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="d6625-151">This has important implications for your application.</span></span> <span data-ttu-id="d6625-152">Любое поведение, которое приводит к созданию большого количества версий в памяти, может привести к исчерпанию максимального размера хранилища версий. Дополнительные сведения см. [JET_paramMaxVerPages](./resource-parameters.md) в разделе " [системные параметры](./extensible-storage-engine-system-parameters.md) ".</span><span class="sxs-lookup"><span data-stu-id="d6625-152">Any behavior that causes a large number of versions to build up in memory may cause the instance to exhaust its maximum version store size (see [JET_paramMaxVerPages](./resource-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md) for more information).</span></span> <span data-ttu-id="d6625-153">Такое поведение включает, но не ограничивается очень большими обновлениями в одной транзакции и очень долго выполняющимися транзакциями.</span><span class="sxs-lookup"><span data-stu-id="d6625-153">Such behavior includes, but is not limited to very large updates in a single transaction and very long running transactions.</span></span> <span data-ttu-id="d6625-154">В результате очень важно правильно настроить размер хранилища версий для ожидаемой транзакционной нагрузки приложения.</span><span class="sxs-lookup"><span data-stu-id="d6625-154">As a result, it is very important to properly configure the version store size for the expected transactional load of the application.</span></span> <span data-ttu-id="d6625-155">Также важно соблюдать осторожность при ограничении количества обновлений, выполняемых в одной транзакции.</span><span class="sxs-lookup"><span data-stu-id="d6625-155">It is also important to take great care to limit the number of updates performed in a single transaction.</span></span> <span data-ttu-id="d6625-156">Более того, очень важно сделать так, чтобы транзакции намерены в условиях высокой нагрузки, как можно более короткие.</span><span class="sxs-lookup"><span data-stu-id="d6625-156">Furthermore, it is important to make transactions as short in duration as possible under high load scenarios.</span></span>

<span data-ttu-id="d6625-157">Настоятельно рекомендуется, чтобы приложение всегда набыло в контексте транзакции при вызове API-интерфейсов ESE, которые извлекают или обновляют данные.</span><span class="sxs-lookup"><span data-stu-id="d6625-157">It is highly recommended that the application always be in the context of a transaction when calling ESE APIs that retrieve or update data.</span></span> <span data-ttu-id="d6625-158">Если это не так, ядро СУБД автоматически заключает каждый вызов API-интерфейса ESE этого типа в транзакцию от имени приложения.</span><span class="sxs-lookup"><span data-stu-id="d6625-158">If this is not done, the database engine will automatically wrap each ESE API call of this type in a transaction on behalf of the application.</span></span> <span data-ttu-id="d6625-159">В некоторых случаях затраты на эти очень короткие транзакции могут быстро сложиться.</span><span class="sxs-lookup"><span data-stu-id="d6625-159">The cost of these very short transactions can add up quickly in some cases.</span></span>

<span data-ttu-id="d6625-160">Поведение обработчика по умолчанию заключается в ограничении использования сеанса тем же потоком с момента выполнения первого вызова **жетбегинтрансактион** до тех пор, пока не будет произведен соответствующий вызов [жеткоммиттрансактион](./jetcommittransaction-function.md) или [жетроллбакк](./jetrollback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="d6625-160">The default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to **JetBeginTransaction** is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="d6625-161">Это поведение можно изменить, чтобы удалить это ограничение, задав пользовательский контекст сеанса с помощью [жетсетсессионконтекст](./jetsetsessioncontext-function.md) и [жетресетсессионконтекст](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="d6625-161">This behavior can be changed to remove this restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

<span data-ttu-id="d6625-162">Ядро СУБД также поддерживает изменения схемы транзакций.</span><span class="sxs-lookup"><span data-stu-id="d6625-162">The database engine also supports transactional schema modifications.</span></span> <span data-ttu-id="d6625-163">Например, можно начать новую транзакцию, создать таблицу, добавить несколько столбцов, создать индекс или две, а затем прервать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="d6625-163">For example, it is possible to begin a new transaction, create a table, add a few columns, create an index or two, and then abort the transaction.</span></span> <span data-ttu-id="d6625-164">Только что добавленные элементы схемы будут удалены из базы данных.</span><span class="sxs-lookup"><span data-stu-id="d6625-164">The schema elements that were just added will be removed from the database.</span></span> <span data-ttu-id="d6625-165">Также можно сочетать изменения схемы и обычные обновления базы данных в одной транзакции.</span><span class="sxs-lookup"><span data-stu-id="d6625-165">It is also possible to mix schema modifications and ordinary database updates in the same transaction.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d6625-166">Требования</span><span class="sxs-lookup"><span data-stu-id="d6625-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6625-167"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="d6625-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d6625-168">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d6625-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6625-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d6625-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d6625-170">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d6625-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6625-171"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d6625-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d6625-172">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d6625-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6625-173"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="d6625-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d6625-174">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d6625-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6625-175"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="d6625-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d6625-176">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d6625-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d6625-177">См. также:</span><span class="sxs-lookup"><span data-stu-id="d6625-177">See Also</span></span>

[<span data-ttu-id="d6625-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d6625-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d6625-179">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d6625-179">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d6625-180">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d6625-180">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d6625-181">жеткоммиттрансактион</span><span class="sxs-lookup"><span data-stu-id="d6625-181">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="d6625-182">жетжетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="d6625-182">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="d6625-183">жетресетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="d6625-183">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="d6625-184">жетроллбакк</span><span class="sxs-lookup"><span data-stu-id="d6625-184">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="d6625-185">жетсетсессионконтекст</span><span class="sxs-lookup"><span data-stu-id="d6625-185">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="d6625-186">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="d6625-186">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="d6625-187">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="d6625-187">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
