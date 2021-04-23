---
description: Дополнительные сведения о функции Жетдефрагмент
title: Функция Жетдефрагмент
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88495f90e726f8c28128a6456566124f23a17381
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349935"
---
# <a name="jetdefragment-function"></a><span data-ttu-id="473b0-103">Функция Жетдефрагмент</span><span class="sxs-lookup"><span data-stu-id="473b0-103">JetDefragment Function</span></span>


<span data-ttu-id="473b0-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="473b0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment-function"></a><span data-ttu-id="473b0-105">Функция Жетдефрагмент</span><span class="sxs-lookup"><span data-stu-id="473b0-105">JetDefragment Function</span></span>

<span data-ttu-id="473b0-106">Функция **жетдефрагмент** запускает и останавливает задачи дефрагментации базы данных, которые улучшают организацию данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="473b0-106">The **JetDefragment** function starts and stops database defragmentation tasks that improves data organization within a database.</span></span> <span data-ttu-id="473b0-107">Это делается для ограничения роста базы данных за счет более эффективного выделения места на диске в пределах базы данных.</span><span class="sxs-lookup"><span data-stu-id="473b0-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="473b0-108">Это также позволяет сократить объем рабочего набора, гарантируя, что данные более тесно упакованы.</span><span class="sxs-lookup"><span data-stu-id="473b0-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="473b0-109">Наконец, она может повысить производительность приложения за счет ускорения выполнения общих операций с помощью более эффективной организации данных.</span><span class="sxs-lookup"><span data-stu-id="473b0-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="473b0-110">Дефрагментация базы данных — это оперативная операция, которая не прерывает обычные действия с базой данных, например операции запроса или обновления данных.</span><span class="sxs-lookup"><span data-stu-id="473b0-110">Database defragmentation is an online operation and does not interrupt regular database activity, such as query operations or data updates.</span></span> <span data-ttu-id="473b0-111">**Жетдефрагмент** также не копирует все существующие данные.</span><span class="sxs-lookup"><span data-stu-id="473b0-111">**JetDefragment** also does not make a copy of all existing data.</span></span> <span data-ttu-id="473b0-112">Вместо этого он выполняет дефрагментацию базы данных на месте.</span><span class="sxs-lookup"><span data-stu-id="473b0-112">Instead, it defragments a database in place.</span></span> <span data-ttu-id="473b0-113">Наконец, **жетдефрагмент** восстанавливает внутреннее пространство базы данных для повторного использования, но не освобождает лишнее пространство для файловой системы операционной системы.</span><span class="sxs-lookup"><span data-stu-id="473b0-113">Lastly, **JetDefragment** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="473b0-114">Полученный формат данных может быть гораздо более эффективным, но обычно не является оптимальным.</span><span class="sxs-lookup"><span data-stu-id="473b0-114">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="473b0-115">Дефрагментация ограничена освобождением страниц базы данных для повторного использования, содержащих данные, которые уже были логически удалены.</span><span class="sxs-lookup"><span data-stu-id="473b0-115">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="473b0-116">Дефрагментация также делает страницы базы данных доступными для повторного использования в некоторых случаях путем объединения данных из двух страниц, когда они могут поместиться на одной странице.</span><span class="sxs-lookup"><span data-stu-id="473b0-116">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="473b0-117">Эта операция отличается от [жеткомпакт](./jetcompact-function.md) , которая делает копию базы данных, доступную только для чтения, в очень оптимальную форму.</span><span class="sxs-lookup"><span data-stu-id="473b0-117">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="473b0-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="473b0-118">Parameters</span></span>

<span data-ttu-id="473b0-119">*сесид*</span><span class="sxs-lookup"><span data-stu-id="473b0-119">*sesid*</span></span>

<span data-ttu-id="473b0-120">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="473b0-120">The session to use for this call.</span></span>

<span data-ttu-id="473b0-121">*DBID*</span><span class="sxs-lookup"><span data-stu-id="473b0-121">*dbid*</span></span>

<span data-ttu-id="473b0-122">База данных, которая будет дефрагментирована.</span><span class="sxs-lookup"><span data-stu-id="473b0-122">The database that will be defragmented.</span></span>

<span data-ttu-id="473b0-123">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="473b0-123">*szTableName*</span></span>

<span data-ttu-id="473b0-124">Неиспользуемый параметр.</span><span class="sxs-lookup"><span data-stu-id="473b0-124">Unused parameter.</span></span> <span data-ttu-id="473b0-125">Дефрагментация выполняется для всей базы данных, описанной по заданному ИДЕНТИФИКАТОРу базы данных.</span><span class="sxs-lookup"><span data-stu-id="473b0-125">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="473b0-126">*пкпассес*</span><span class="sxs-lookup"><span data-stu-id="473b0-126">*pcPasses*</span></span>

<span data-ttu-id="473b0-127">При запуске задачи дефрагментации в оперативном режиме этот входной параметр задает максимальное число проходов дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="473b0-127">When starting an online defragmentation task, this input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="473b0-128">При остановке задачи дефрагментации в оперативном режиме для этого буфера вывода задается количество выполненных проходов.</span><span class="sxs-lookup"><span data-stu-id="473b0-128">When stopping an online defragmentation task, this output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="473b0-129">Если этот параметр имеет значение NULL, число проходов оперативной дефрагментации не ограничено.</span><span class="sxs-lookup"><span data-stu-id="473b0-129">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="473b0-130">*пксекондс*</span><span class="sxs-lookup"><span data-stu-id="473b0-130">*pcSeconds*</span></span>

<span data-ttu-id="473b0-131">При запуске задачи дефрагментации в оперативном режиме этот входной параметр задает максимальное время для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="473b0-131">When starting an online defragmentation task, this input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="473b0-132">При остановке задачи дефрагментации в оперативном режиме этот выходной буфер задается в течение времени, используемого для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="473b0-132">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="473b0-133">Если для этого параметра задано значение NULL или *пксекондс* указывает на отрицательное значение, максимальное время дефрагментации не ограничено.</span><span class="sxs-lookup"><span data-stu-id="473b0-133">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="473b0-134">*грбит*</span><span class="sxs-lookup"><span data-stu-id="473b0-134">*grbit*</span></span>

<span data-ttu-id="473b0-135">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="473b0-135">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="473b0-136">Значение</span><span class="sxs-lookup"><span data-stu-id="473b0-136">Value</span></span></p></th>
<th><p><span data-ttu-id="473b0-137">Значение</span><span class="sxs-lookup"><span data-stu-id="473b0-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="473b0-138">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="473b0-138">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="473b0-139">Дефрагментация доступного места в выделенном пространстве базы данных ESE.</span><span class="sxs-lookup"><span data-stu-id="473b0-139">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="473b0-140">Пространство базы данных делится на два типа: пространство и доступное пространство.</span><span class="sxs-lookup"><span data-stu-id="473b0-140">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="473b0-141">Владельцем пространства выделяется таблица или индекс, в то время как доступное место может быть готово к использованию в таблице или индексе соответственно.</span><span class="sxs-lookup"><span data-stu-id="473b0-141">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="473b0-142">Доступное пространство является гораздо более динамичным в поведении и требует дополнительной дефрагментации, что больше, чем принадлежащие пространства или данные таблицы или индекса.</span><span class="sxs-lookup"><span data-stu-id="473b0-142">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-143">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="473b0-143">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="473b0-144">Запускает новую задачу дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="473b0-144">Starts a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473b0-145">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="473b0-145">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="473b0-146">Останавливает задачу дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="473b0-146">Stops a defragmentation task.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="473b0-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="473b0-147">Return Value</span></span>

<span data-ttu-id="473b0-148">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="473b0-148">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="473b0-149">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="473b0-149">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="473b0-150">Код возврата</span><span class="sxs-lookup"><span data-stu-id="473b0-150">Return code</span></span></p></th>
<th><p><span data-ttu-id="473b0-151">Описание</span><span class="sxs-lookup"><span data-stu-id="473b0-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="473b0-152">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="473b0-152">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="473b0-153">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="473b0-153">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-154">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="473b0-154">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="473b0-155">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="473b0-155">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473b0-156">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="473b0-156">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="473b0-157">База данных, выбранная для дефрагментации, доступна только для чтения и не может быть обновлена каким-либо образом, включая дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="473b0-157">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="473b0-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="473b0-159">Данный сеанс находится в состоянии "подготовлено к фиксации" и не может начинать новые обновления до фиксации или отката текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="473b0-159">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473b0-160">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="473b0-160">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="473b0-161">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="473b0-161">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="473b0-162">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="473b0-162">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-163">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="473b0-163">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="473b0-164">Заданный идентификатор базы данных не соответствует известной базе данных в экземпляре.</span><span class="sxs-lookup"><span data-stu-id="473b0-164">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473b0-165">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="473b0-165">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="473b0-166">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="473b0-166">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="473b0-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="473b0-168">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="473b0-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473b0-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="473b0-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="473b0-170">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="473b0-170">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="473b0-171">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="473b0-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="473b0-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="473b0-173">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="473b0-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473b0-174">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="473b0-174">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="473b0-175">Данный сеанс имеет только права доступа только для чтения и не может запустить задачу, которая может выполнить обновление, включая дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="473b0-175">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-176">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="473b0-176">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="473b0-177">Эта ошибка возникает, если настроенный размер хранилища версий недостаточно для хранения всех необработанных обновлений.</span><span class="sxs-lookup"><span data-stu-id="473b0-177">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473b0-178">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="473b0-178">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="473b0-179">Параметр JET_bitDefragmentBatchStart был передан, но задача дефрагментации уже выполняет дефрагментацию данной базы данных.</span><span class="sxs-lookup"><span data-stu-id="473b0-179">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-180">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="473b0-180">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="473b0-181">Параметр JET_bitDefragmentBatchStop был передан, но в данный момент задача дефрагментации не выполняется.</span><span class="sxs-lookup"><span data-stu-id="473b0-181">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="473b0-182">При успешном выполнении запрошенное действие либо запуск задачи дефрагментации для заданных параметров с заданными параметрами, либо выполнение действия остановка существующей задачи дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="473b0-182">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="473b0-183">В случае сбоя запрошенное действие запуска или остановки задания оперативной дефрагментации не выполняется.</span><span class="sxs-lookup"><span data-stu-id="473b0-183">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="473b0-184">Другие побочные эффекты не возникают.</span><span class="sxs-lookup"><span data-stu-id="473b0-184">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="473b0-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="473b0-185">Remarks</span></span>

<span data-ttu-id="473b0-186">Оперативная дефрагментация управляется параметром параметра, а также этим API.</span><span class="sxs-lookup"><span data-stu-id="473b0-186">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="473b0-187">Значение системного параметра по умолчанию — JET_OnlineDefragAll. Это означает, что дефрагментация включена для всех поддерживаемых структур данных.</span><span class="sxs-lookup"><span data-stu-id="473b0-187">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="473b0-188">Однако с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md)можно отключить оперативную дефрагментацию или выборочно включить ее только для деревьев пространства базы данных, только для потоковых файлов или любого сочетания этих параметров.</span><span class="sxs-lookup"><span data-stu-id="473b0-188">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="473b0-189">Если параметр системы для оперативной дефрагментации имеет значение устаревшей, **жетдефрагмент** будет рассматривать этот параметр как JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="473b0-189">If the system setting for online defragmentation is set to an obsolete setting, **JetDefragment** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="473b0-190">Для каждой базы данных может выполняться не более одной задачи.</span><span class="sxs-lookup"><span data-stu-id="473b0-190">There can at most be one task running for each database.</span></span> <span data-ttu-id="473b0-191">Задача выполняется как поток в процессе размещения ESE.</span><span class="sxs-lookup"><span data-stu-id="473b0-191">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="473b0-192">Сеанс, используемый для запуска задачи дефрагментации в сети, можно впоследствии использовать для операций с базой данных во время выполнения задачи дефрагментации, так как задача дефрагментации выделяет собственный сеанс.</span><span class="sxs-lookup"><span data-stu-id="473b0-192">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="473b0-193">Данный сеанс используется только для проверки разрешений, связанных с начальным сеансом задачи, и фактически не используется для самих операций дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="473b0-193">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="473b0-194">Требования</span><span class="sxs-lookup"><span data-stu-id="473b0-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="473b0-195"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="473b0-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="473b0-196">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="473b0-196">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-197"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="473b0-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="473b0-198">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="473b0-198">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473b0-199"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="473b0-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="473b0-200">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="473b0-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-201"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="473b0-201"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="473b0-202">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="473b0-202">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="473b0-203"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="473b0-203"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="473b0-204">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="473b0-204">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="473b0-205"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="473b0-205"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="473b0-206">Реализуется как <strong>жетдефрагментв</strong> (Юникод) и <strong>жетдефрагмента</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="473b0-206">Implemented as <strong>JetDefragmentW</strong> (Unicode) and <strong>JetDefragmentA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="473b0-207">См. также:</span><span class="sxs-lookup"><span data-stu-id="473b0-207">See Also</span></span>

[<span data-ttu-id="473b0-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="473b0-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="473b0-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="473b0-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="473b0-210">жеткомпакт</span><span class="sxs-lookup"><span data-stu-id="473b0-210">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="473b0-211">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="473b0-211">JetDefragment2</span></span>](./jetdefragment2-function.md)  
[<span data-ttu-id="473b0-212">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="473b0-212">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="473b0-213">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="473b0-213">JetStopService</span></span>](./jetstopservice-function.md)
