---
description: Дополнительные сведения о функции JetDefragment2
title: Функция JetDefragment2
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105720989"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="a0cb9-103">Функция JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="a0cb9-103">JetDefragment2 Function</span></span>


<span data-ttu-id="a0cb9-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a0cb9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="a0cb9-105">Функция JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="a0cb9-105">JetDefragment2 Function</span></span>

<span data-ttu-id="a0cb9-106">Функция **JetDefragment2** запускает и останавливает задачи дефрагментации базы данных, которые улучшают организацию данных в базе данных, с параметром обратного вызова, доступным для сообщения о ходе дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="a0cb9-107">Это делается для ограничения роста базы данных за счет более эффективного выделения места на диске в пределах базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="a0cb9-108">Это также позволяет сократить объем рабочего набора, гарантируя, что данные более тесно упакованы.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="a0cb9-109">Наконец, она может повысить производительность приложения за счет ускорения выполнения общих операций с помощью более эффективной организации данных.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="a0cb9-110">**Windows XP:**  **JetDefragment2** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="a0cb9-111">**JetDefragment2** также содержит параметр функции обратного вызова, который используется для сообщения о ходе процесса дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="a0cb9-112">Дефрагментация базы данных — это оперативная операция, которая не прерывает обычные операции с базой данных, такие как операции запроса или обновления данных.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="a0cb9-113">**JetDefragment2** также не копирует все существующие данные.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="a0cb9-114">Вместо этого он выполняет дефрагментацию базы данных на месте.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="a0cb9-115">Наконец, **JetDefragment2** восстанавливает внутреннее пространство базы данных для повторного использования, но не освобождает лишнее пространство для файловой системы операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="a0cb9-116">Полученный формат данных может быть гораздо более эффективным, но обычно не является оптимальным.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="a0cb9-117">Дефрагментация ограничена освобождением страниц базы данных для повторного использования, содержащих данные, которые уже были логически удалены.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="a0cb9-118">Дефрагментация также делает страницы базы данных доступными для повторного использования в некоторых случаях путем объединения данных из двух страниц, когда они могут поместиться на одной странице.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="a0cb9-119">Эта операция отличается от [жеткомпакт](./jetcompact-function.md) , которая делает копию базы данных, доступную только для чтения, в очень оптимальную форму.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="a0cb9-120">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0cb9-120">Parameters</span></span>

<span data-ttu-id="a0cb9-121">*сесид*</span><span class="sxs-lookup"><span data-stu-id="a0cb9-121">*sesid*</span></span>

<span data-ttu-id="a0cb9-122">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-122">The session to use for this call.</span></span>

<span data-ttu-id="a0cb9-123">*DBID*</span><span class="sxs-lookup"><span data-stu-id="a0cb9-123">*dbid*</span></span>

<span data-ttu-id="a0cb9-124">Дефрагментация базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-124">The database to defragment.</span></span>

<span data-ttu-id="a0cb9-125">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="a0cb9-125">*szTableName*</span></span>

<span data-ttu-id="a0cb9-126">Неиспользуемый параметр.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-126">Unused parameter.</span></span> <span data-ttu-id="a0cb9-127">Дефрагментация выполняется для всей базы данных, описанной по заданному ИДЕНТИФИКАТОРу базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-127">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="a0cb9-128">*пкпассес*</span><span class="sxs-lookup"><span data-stu-id="a0cb9-128">*pcPasses*</span></span>

<span data-ttu-id="a0cb9-129">При запуске задачи дефрагментации в оперативном режиме этот необязательный входной параметр задает максимальное количество проходов дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-129">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="a0cb9-130">При остановке задачи дефрагментации в оперативном режиме для этого дополнительного выходного буфера задается количество выполненных проходов.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-130">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="a0cb9-131">Если этот параметр имеет значение NULL, число проходов оперативной дефрагментации не ограничено.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-131">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="a0cb9-132">*пксекондс*</span><span class="sxs-lookup"><span data-stu-id="a0cb9-132">*pcSeconds*</span></span>

<span data-ttu-id="a0cb9-133">При запуске задачи дефрагментации в оперативном режиме этот необязательный входной параметр задает максимальное время для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-133">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="a0cb9-134">При остановке задачи дефрагментации в оперативном режиме для этого необязательного выходного буфера задается продолжительность времени, используемого для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-134">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="a0cb9-135">Если для этого параметра задано значение NULL или *пксекондс* указывает на отрицательное значение, максимальное время дефрагментации не ограничено.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-135">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="a0cb9-136">*обратный вызов*</span><span class="sxs-lookup"><span data-stu-id="a0cb9-136">*callback*</span></span>

<span data-ttu-id="a0cb9-137">Функция обратного вызова, которая регулярно вызывает дефрагментацию для отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-137">Callback function that defragmentation calls regularly to report progress.</span></span>

<span data-ttu-id="a0cb9-138">*грбит*</span><span class="sxs-lookup"><span data-stu-id="a0cb9-138">*grbit*</span></span>

<span data-ttu-id="a0cb9-139">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-139">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0cb9-140">Значение</span><span class="sxs-lookup"><span data-stu-id="a0cb9-140">Value</span></span></p></th>
<th><p><span data-ttu-id="a0cb9-141">Значение</span><span class="sxs-lookup"><span data-stu-id="a0cb9-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-142">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="a0cb9-142">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-143">Этот параметр используется для дефрагментации свободного места, выделенного для выделения места в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-143">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="a0cb9-144">Пространство базы данных делится на два типа: пространство и доступное пространство.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-144">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="a0cb9-145">Владельцем пространства выделяется таблица или индекс, в то время как доступное место может быть готово к использованию в таблице или индексе соответственно.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-145">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="a0cb9-146">Доступное пространство является гораздо более динамичным поведением и требует оперативной дефрагментации больше, чем присвоено пространство или данные таблицы или индекса.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-146">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-147">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="a0cb9-147">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-148">Этот параметр используется для запуска новой задачи дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-148">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-149">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="a0cb9-149">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-150">Этот параметр используется для отмены существующей запущенной задачи дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-150">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-151">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="a0cb9-151">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-152">Этот параметр используется для дефрагментации сбалансированного дерева.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-152">This option is used to defrag a B-Tree.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a0cb9-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0cb9-153">Return Value</span></span>

<span data-ttu-id="a0cb9-154">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-154">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a0cb9-155">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a0cb9-155">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0cb9-156">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a0cb9-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="a0cb9-157">Описание</span><span class="sxs-lookup"><span data-stu-id="a0cb9-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a0cb9-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-159">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-159">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-160">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a0cb9-160">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-161">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-161">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-162">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="a0cb9-162">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-163">База данных, выбранная для дефрагментации, доступна только для чтения и не может быть обновлена каким-либо образом, включая дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-163">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="a0cb9-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-165">Данный сеанс находится в состоянии "подготовлено к фиксации" и не может начинать новые обновления до фиксации или отката текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-165">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-166">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a0cb9-166">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-167">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-167">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a0cb9-168">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-169">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="a0cb9-169">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-170">Заданный идентификатор базы данных не соответствует известной базе данных в экземпляре.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-170">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-171">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a0cb9-171">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-172">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-172">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a0cb9-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-174">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-175">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a0cb9-175">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-176">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-176">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="a0cb9-177">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-177">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-178">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a0cb9-178">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-179">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-179">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-180">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="a0cb9-180">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-181">Данный сеанс имеет только права доступа только для чтения и не может запустить задачу, которая может выполнить обновление, включая дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-181">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-182">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a0cb9-182">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-183">Эта ошибка возникает, если настроенный размер хранилища версий недостаточно для хранения всех необработанных обновлений.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-183">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-184">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="a0cb9-184">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-185">Параметр JET_bitDefragmentBatchStart был передан, но задача дефрагментации уже выполняет дефрагментацию данной базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-185">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-186">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="a0cb9-186">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="a0cb9-187">Параметр JET_bitDefragmentBatchStop был передан, но в данный момент задача дефрагментации не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-187">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0cb9-188">При успешном выполнении запрошенное действие либо запуск задачи дефрагментации для заданных параметров с заданными параметрами, либо выполнение действия остановка существующей задачи дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-188">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="a0cb9-189">В случае сбоя запрошенное действие запуска или остановки задания оперативной дефрагментации не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-189">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="a0cb9-190">Другие побочные эффекты не возникают.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-190">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a0cb9-191">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0cb9-191">Remarks</span></span>

<span data-ttu-id="a0cb9-192">Оперативная дефрагментация управляется параметром параметра, а также этим API.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-192">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="a0cb9-193">Значение системного параметра по умолчанию — JET_OnlineDefragAll. Это означает, что дефрагментация включена для всех поддерживаемых структур данных.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-193">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="a0cb9-194">Однако с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md)можно отключить оперативную дефрагментацию или выборочно включить ее только для деревьев пространства базы данных, только для потоковых файлов или любого сочетания этих параметров.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-194">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="a0cb9-195">Если параметр системы для автономной дефрагментации находится в устаревшем параметре, **JetDefragment2** будет рассматривать этот параметр как JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-195">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="a0cb9-196">Для каждой базы данных может выполняться не более одной задачи.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-196">There can at most be one task running for each database.</span></span> <span data-ttu-id="a0cb9-197">Задача выполняется как поток в процессе размещения ESE.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-197">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="a0cb9-198">Сеанс, используемый для запуска задачи дефрагментации в сети, можно впоследствии использовать для операций с базой данных во время выполнения задачи дефрагментации, так как задача дефрагментации выделяет собственный сеанс.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-198">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="a0cb9-199">Данный сеанс используется только для проверки разрешений, связанных с начальным сеансом задачи, и фактически не используется для самих операций дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-199">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a0cb9-200">Требования</span><span class="sxs-lookup"><span data-stu-id="a0cb9-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-201"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a0cb9-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a0cb9-202">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-202">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a0cb9-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a0cb9-204">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-204">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a0cb9-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a0cb9-206">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-207"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="a0cb9-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a0cb9-208">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cb9-209"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="a0cb9-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a0cb9-210">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a0cb9-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cb9-211"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="a0cb9-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a0cb9-212">Реализуется как <strong>JetDefragment2W</strong> (Юникод) и <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a0cb9-212">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a0cb9-213">См. также:</span><span class="sxs-lookup"><span data-stu-id="a0cb9-213">See Also</span></span>

[<span data-ttu-id="a0cb9-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a0cb9-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a0cb9-215">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a0cb9-215">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a0cb9-216">жеткомпакт</span><span class="sxs-lookup"><span data-stu-id="a0cb9-216">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="a0cb9-217">жетдефрагмент</span><span class="sxs-lookup"><span data-stu-id="a0cb9-217">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="a0cb9-218">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="a0cb9-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a0cb9-219">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="a0cb9-219">JetStopService</span></span>](./jetstopservice-function.md)
