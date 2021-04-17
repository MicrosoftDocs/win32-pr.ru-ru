---
description: Дополнительные сведения о функции Жетделете
title: Функция JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647515"
---
# <a name="jetdelete-function"></a><span data-ttu-id="9c412-103">Функция JetDelete</span><span class="sxs-lookup"><span data-stu-id="9c412-103">JetDelete Function</span></span>


<span data-ttu-id="9c412-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9c412-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdelete-function"></a><span data-ttu-id="9c412-105">Функция JetDelete</span><span class="sxs-lookup"><span data-stu-id="9c412-105">JetDelete Function</span></span>

<span data-ttu-id="9c412-106">Функция **жетделете** удаляет текущую запись в таблице базы данных.</span><span class="sxs-lookup"><span data-stu-id="9c412-106">The **JetDelete** function deletes the current record in a database table.</span></span>

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="9c412-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c412-107">Parameters</span></span>

<span data-ttu-id="9c412-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="9c412-108">*sesid*</span></span>

<span data-ttu-id="9c412-109">Контекст сеанса базы данных, который будет использоваться для вызова API.</span><span class="sxs-lookup"><span data-stu-id="9c412-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="9c412-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9c412-110">*tableid*</span></span>

<span data-ttu-id="9c412-111">Курсор в таблице базы данных.</span><span class="sxs-lookup"><span data-stu-id="9c412-111">The cursor on a database table.</span></span> <span data-ttu-id="9c412-112">Текущая строка будет удалена.</span><span class="sxs-lookup"><span data-stu-id="9c412-112">The current row will be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="9c412-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c412-113">Return Value</span></span>

<span data-ttu-id="9c412-114">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="9c412-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9c412-115">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9c412-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c412-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9c412-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="9c412-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9c412-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c412-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9c412-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9c412-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9c412-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c412-120">JET_errCallbackFailed</span><span class="sxs-lookup"><span data-stu-id="9c412-120">JET_errCallbackFailed</span></span></p></td>
<td><p><span data-ttu-id="9c412-121">Ошибка функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="9c412-121">The callback function failed in some manner.</span></span> <span data-ttu-id="9c412-122">Например, нарушения прав доступа в функциях обратного вызова перехватываются и преобразуются в JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="9c412-122">For example, access violations in callback functions are caught and translated into JET_errCallbackFailed.</span></span> <span data-ttu-id="9c412-123">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="9c412-123">This error will only be returned by Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c412-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9c412-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9c412-125">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="9c412-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c412-126">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="9c412-126">JET_errIllegalOperation</span></span></p></td>
<td><p><span data-ttu-id="9c412-127">Курсор, указанный функцией <em>tableid</em> , не поддерживает удаление.</span><span class="sxs-lookup"><span data-stu-id="9c412-127">The cursor specified by <em>tableid</em> does not support deletion.</span></span> <span data-ttu-id="9c412-128">См. раздел «Примечания».</span><span class="sxs-lookup"><span data-stu-id="9c412-128">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c412-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9c412-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9c412-130">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="9c412-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="9c412-131">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="9c412-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c412-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="9c412-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="9c412-133">Курсор, заданный параметром <em>tableid</em> , не находится в записи.</span><span class="sxs-lookup"><span data-stu-id="9c412-133">The cursor specified by <em>tableid</em> is not on a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c412-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9c412-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9c412-135">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="9c412-135">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c412-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9c412-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9c412-137">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="9c412-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c412-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="9c412-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="9c412-139">Ядро СУБД не имеет достаточных разрешений для удаления записи.</span><span class="sxs-lookup"><span data-stu-id="9c412-139">The database engine does not have sufficient permissions to delete the record.</span></span> <span data-ttu-id="9c412-140">Это может произойти, если файл базы данных был открыт с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9c412-140">This may happen if the database file was opened with read-only access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c412-141">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="9c412-141">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="9c412-142">Буфер обновления (см. <a href="gg269339(v=exchg.10).md">жетпрепареупдате</a>) существует, но не все изменения, внесенные в столбцы типа JET_coltypLongText и (или) столбцы типа JET_coltypLongBinary, могут быть отменены.</span><span class="sxs-lookup"><span data-stu-id="9c412-142">An update buffer (see <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) exists, but not all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary could be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c412-143">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9c412-143">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9c412-144">Нельзя одновременно использовать один сеанс из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="9c412-144">It is illegal to use the same session from more than one thread at the same time.</span></span> <span data-ttu-id="9c412-145">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="9c412-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c412-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9c412-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9c412-147">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="9c412-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c412-148">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="9c412-148">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9c412-149">Транзакция является транзакцией только для чтения и не поддерживает удаления.</span><span class="sxs-lookup"><span data-stu-id="9c412-149">The transaction is a read-only transaction, and does not support deletes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c412-150">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="9c412-150">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="9c412-151">Не удалось выполнить операцию, так как недостаточно памяти для удержания транзакционных сведений об обновлении.</span><span class="sxs-lookup"><span data-stu-id="9c412-151">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c412-152">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="9c412-152">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="9c412-153">Другой сеанс ранее заблокировал запись для обновления.</span><span class="sxs-lookup"><span data-stu-id="9c412-153">Another session has previously locked the record for update.</span></span> <span data-ttu-id="9c412-154">Обновление, которое попыталось этот сеанс, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9c412-154">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c412-155">В случае успеха валюта остается непосредственно перед следующей записью.</span><span class="sxs-lookup"><span data-stu-id="9c412-155">On success, the currency is left just before the next record.</span></span> <span data-ttu-id="9c412-156">Если удаленная запись была последней в таблице, то валюта остается в конце таблицы (то есть после новой записи).</span><span class="sxs-lookup"><span data-stu-id="9c412-156">If the deleted record was the last in the table, the currency is left at the end of the table (that is, after the new last record).</span></span> <span data-ttu-id="9c412-157">Если удаленная запись была единственной записью в таблице, то в качестве валюты устанавливается начало.</span><span class="sxs-lookup"><span data-stu-id="9c412-157">If the deleted record was the only record in the table, the currency is set to the beginning.</span></span>

<span data-ttu-id="9c412-158">Соответствующие индексы обновляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="9c412-158">The appropriate indexes are automatically updated.</span></span>

<span data-ttu-id="9c412-159">Если обновление подготовлено (с помощью [жетпрепареупдате](./jetprepareupdate-function.md)), оно будет отменено.</span><span class="sxs-lookup"><span data-stu-id="9c412-159">If an update is prepared (using [JetPrepareUpdate](./jetprepareupdate-function.md)), it will be canceled.</span></span> <span data-ttu-id="9c412-160">Буфер обновления будет сброшен.</span><span class="sxs-lookup"><span data-stu-id="9c412-160">The update buffer will be reset.</span></span>

<span data-ttu-id="9c412-161">В случае сбоя валюта остается неизменной.</span><span class="sxs-lookup"><span data-stu-id="9c412-161">On failure, the currency remains unchanged.</span></span> <span data-ttu-id="9c412-162">Если обновление подготовлено (см. [жетпрепареупдате](./jetprepareupdate-function.md)), буфер обновления может быть сброшен.</span><span class="sxs-lookup"><span data-stu-id="9c412-162">If an update is prepared (see [JetPrepareUpdate](./jetprepareupdate-function.md)), the update buffer may be reset.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9c412-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c412-163">Remarks</span></span>

<span data-ttu-id="9c412-164">Не все таблицы поддерживают удаление строк.</span><span class="sxs-lookup"><span data-stu-id="9c412-164">Not all tables support deletion of rows.</span></span> <span data-ttu-id="9c412-165">Как правило, временная таблица не поддерживает удаление строк.</span><span class="sxs-lookup"><span data-stu-id="9c412-165">A temporary table does not normally support deletion of rows.</span></span> <span data-ttu-id="9c412-166">Удаление записей может быть включено во временных таблицах по многим причинам:</span><span class="sxs-lookup"><span data-stu-id="9c412-166">Deletion of records may be enabled on temporary tables for many reasons, some of which are:</span></span>

  - <span data-ttu-id="9c412-167">JET_bitTTUpdatable был указан во время создания.</span><span class="sxs-lookup"><span data-stu-id="9c412-167">JET_bitTTUpdatable was specified during creation.</span></span>

  - <span data-ttu-id="9c412-168">Большие временные таблицы могут поддерживать удаление, если они были созданы с помощью JET_bitTTScrollable или JET_bitTTIndexed.</span><span class="sxs-lookup"><span data-stu-id="9c412-168">Large temporary tables can support deletion if they were created with JET_bitTTScrollable or JET_bitTTIndexed.</span></span> <span data-ttu-id="9c412-169">Пороговое значение, при достижении которого временная таблица становится "большим", в настоящее время составляет 64 килобайт, но может быть изменено в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="9c412-169">The threshold at which a temporary table becomes "large" is currently 64 kilobytes, but it may be changed in future releases.</span></span>

<span data-ttu-id="9c412-170">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="9c412-170">Windows XP and later.</span></span> <span data-ttu-id="9c412-171">Функции обратного вызова могут вызываться **жетделете**, включая JET_cbtypBeforeDelete и JET_cbtypAfterDelete.</span><span class="sxs-lookup"><span data-stu-id="9c412-171">Callback functions can be invoked by **JetDelete**, including JET_cbtypBeforeDelete and JET_cbtypAfterDelete.</span></span>

<span data-ttu-id="9c412-172">Важно понимать влияние выполнения большого количества операций обновления в рамках одной транзакции.</span><span class="sxs-lookup"><span data-stu-id="9c412-172">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="9c412-173">Каждое обновление базы данных должно быть отслеживанием ядра СУБД в хранилище версий.</span><span class="sxs-lookup"><span data-stu-id="9c412-173">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="9c412-174">Хранилище версий содержит активную запись всех различных версий каждой записи или записи индекса в базе данных, которые могут быть видны всем активным транзакциям.</span><span class="sxs-lookup"><span data-stu-id="9c412-174">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="9c412-175">Эти версии используются для поддержки управления параллелизмом с несколькими версиями, используемого ядром СУБД для поддержки транзакций с использованием изоляции моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="9c412-175">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="9c412-176">После того, как ядро СУБД исчерпало ресурсы, используемые для хранения этих версий, оно больше не сможет принять дальнейшие изменения до тех пор, пока некоторые транзакции не разрешают высвободить эти ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9c412-176">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="9c412-177">Если обработчик находится в этом состоянии, все обновления будут завершаться с JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="9c412-177">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="9c412-178">Ресурсы, доступные ядру СУБД для хранения этих версий, можно контролировать с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с *JET_paramMaxVerPages* и *JET_paramGlobalMinVerPages*.</span><span class="sxs-lookup"><span data-stu-id="9c412-178">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxVerPages* and *JET_paramGlobalMinVerPages*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9c412-179">Требования</span><span class="sxs-lookup"><span data-stu-id="9c412-179">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c412-180"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9c412-180"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9c412-181">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9c412-181">Requires Windows Vista, Windows XP or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c412-182"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9c412-182"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9c412-183">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9c412-183">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c412-184"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9c412-184"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9c412-185">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9c412-185">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c412-186"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="9c412-186"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9c412-187">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9c412-187">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c412-188"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="9c412-188"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9c412-189">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9c412-189">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9c412-190">См. также:</span><span class="sxs-lookup"><span data-stu-id="9c412-190">See Also</span></span>

[<span data-ttu-id="9c412-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9c412-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9c412-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9c412-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9c412-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9c412-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9c412-194">жетопентемптабле</span><span class="sxs-lookup"><span data-stu-id="9c412-194">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="9c412-195">жетпрепареупдате</span><span class="sxs-lookup"><span data-stu-id="9c412-195">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="9c412-196">Системные параметры</span><span class="sxs-lookup"><span data-stu-id="9c412-196">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
