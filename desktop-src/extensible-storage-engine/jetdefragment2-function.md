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
ms.openlocfilehash: 4bcde8d55032d2e07466668b5a4d96b9a447d843
ms.sourcegitcommit: 35baf9ba19918a38c4ca8714f88c004af0c6f518
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107838808"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="a9dd0-103">Функция JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="a9dd0-103">JetDefragment2 Function</span></span>


<span data-ttu-id="a9dd0-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a9dd0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="a9dd0-105">Функция JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="a9dd0-105">JetDefragment2 Function</span></span>

<span data-ttu-id="a9dd0-106">Функция **JetDefragment2** запускает и останавливает задачи дефрагментации базы данных, которые улучшают организацию данных в базе данных, с параметром обратного вызова, доступным для сообщения о ходе дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="a9dd0-107">Это делается для ограничения роста базы данных за счет более эффективного выделения места на диске в пределах базы данных.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="a9dd0-108">Это также позволяет сократить объем рабочего набора, гарантируя, что данные более тесно упакованы.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="a9dd0-109">Наконец, она может повысить производительность приложения за счет ускорения выполнения общих операций с помощью более эффективной организации данных.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="a9dd0-110">**Windows XP:**  **JetDefragment2** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="a9dd0-111">**JetDefragment2** также содержит параметр функции обратного вызова, который используется для сообщения о ходе процесса дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="a9dd0-112">Дефрагментация базы данных — это оперативная операция, которая не прерывает обычные операции с базой данных, такие как операции запроса или обновления данных.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="a9dd0-113">**JetDefragment2** также не копирует все существующие данные.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="a9dd0-114">Вместо этого он выполняет дефрагментацию базы данных на месте.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="a9dd0-115">Наконец, **JetDefragment2** восстанавливает внутреннее пространство базы данных для повторного использования, но не освобождает лишнее пространство для файловой системы операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="a9dd0-116">Полученный формат данных может быть гораздо более эффективным, но обычно не является оптимальным.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="a9dd0-117">Дефрагментация ограничена освобождением страниц базы данных для повторного использования, содержащих данные, которые уже были логически удалены.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="a9dd0-118">Дефрагментация также делает страницы базы данных доступными для повторного использования в некоторых случаях путем объединения данных из двух страниц, когда они могут поместиться на одной странице.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="a9dd0-119">Эта операция отличается от [жеткомпакт](./jetcompact-function.md) , которая делает копию базы данных, доступную только для чтения, в очень оптимальную форму.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

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

### <a name="parameters"></a><span data-ttu-id="a9dd0-120">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9dd0-120">Parameters</span></span>

<span data-ttu-id="a9dd0-121">*сесид*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-121">*sesid*</span></span>

<span data-ttu-id="a9dd0-122">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-122">The session to use for this call.</span></span>

<span data-ttu-id="a9dd0-123">*DBID*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-123">*dbid*</span></span>

<span data-ttu-id="a9dd0-124">Дефрагментация базы данных.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-124">The database to defragment.</span></span>

<span data-ttu-id="a9dd0-125">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-125">*szTableName*</span></span>

<span data-ttu-id="a9dd0-126">Иногда *сзтабленаме* является обязательным, и иногда она запрещена:</span><span class="sxs-lookup"><span data-stu-id="a9dd0-126">Sometimes *szTableName* is required, and sometimes it is forbidden:</span></span>

| <span data-ttu-id="a9dd0-127">*грбит*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-127">*grbit*</span></span> | <span data-ttu-id="a9dd0-128">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-128">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="a9dd0-129">Этот параметр должен содержать значение `NULL`.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-129">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="a9dd0-130">Указывает имя таблицы или сбалансированного дерева для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-130">Specifies the name of the table/BTree to defragment.</span></span> |
| <span data-ttu-id="a9dd0-131">*иной*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-131">*other*</span></span> | <span data-ttu-id="a9dd0-132">Этот параметр должен содержать значение `NULL`.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-132">Must be `NULL`.</span></span> |
 
<span data-ttu-id="a9dd0-133">Дефрагментация выполняется для всей базы данных, описанной по заданному ИДЕНТИФИКАТОРу базы данных.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-133">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="a9dd0-134">*пкпассес*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-134">*pcPasses*</span></span>

<span data-ttu-id="a9dd0-135">При запуске задачи дефрагментации в оперативном режиме этот необязательный входной параметр задает максимальное количество проходов дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-135">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="a9dd0-136">При остановке задачи дефрагментации в оперативном режиме для этого дополнительного выходного буфера задается количество выполненных проходов.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-136">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="a9dd0-137">Если этот параметр имеет значение NULL, число проходов оперативной дефрагментации не ограничено.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-137">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="a9dd0-138">*пксекондс*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-138">*pcSeconds*</span></span>

<span data-ttu-id="a9dd0-139">При запуске задачи дефрагментации в оперативном режиме этот необязательный входной параметр задает максимальное время для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-139">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="a9dd0-140">При остановке задачи дефрагментации в оперативном режиме для этого необязательного выходного буфера задается продолжительность времени, используемого для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-140">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="a9dd0-141">Если для этого параметра задано значение NULL или *пксекондс* указывает на отрицательное значение, максимальное время дефрагментации не ограничено.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-141">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="a9dd0-142">*обратный вызов*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-142">*callback*</span></span>

<span data-ttu-id="a9dd0-143">Функция обратного вызова, которая регулярно вызывает дефрагментацию для отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-143">Callback function that defragmentation calls regularly to report progress.</span></span>

| <span data-ttu-id="a9dd0-144">*грбит*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-144">*grbit*</span></span> | <span data-ttu-id="a9dd0-145">*сзтабленаме*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-145">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="a9dd0-146">Этот параметр должен содержать значение `NULL`.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-146">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="a9dd0-147">Этот параметр должен содержать значение `NULL`.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-147">Must be `NULL`.</span></span> |
| <span data-ttu-id="a9dd0-148">*иной*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-148">*other*</span></span> | <span data-ttu-id="a9dd0-149">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-149">Optional.</span></span>


<span data-ttu-id="a9dd0-150">*грбит*</span><span class="sxs-lookup"><span data-stu-id="a9dd0-150">*grbit*</span></span>

<span data-ttu-id="a9dd0-151">Группа битов, задающая ноль или более следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-151">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9dd0-152">Значение</span><span class="sxs-lookup"><span data-stu-id="a9dd0-152">Value</span></span></p></th>
<th><p><span data-ttu-id="a9dd0-153">Значение</span><span class="sxs-lookup"><span data-stu-id="a9dd0-153">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-154">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="a9dd0-154">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-155">Этот параметр используется для дефрагментации свободного места, выделенного для выделения места в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-155">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="a9dd0-156">Пространство базы данных делится на два типа: пространство и доступное пространство.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-156">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="a9dd0-157">Владельцем пространства выделяется таблица или индекс, в то время как доступное место может быть готово к использованию в таблице или индексе соответственно.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-157">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="a9dd0-158">Доступное пространство является гораздо более динамичным поведением и требует оперативной дефрагментации больше, чем присвоено пространство или данные таблицы или индекса.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-158">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-159">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="a9dd0-159">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-160">Этот параметр используется для запуска новой задачи дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-160">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-161">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="a9dd0-161">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-162">Этот параметр используется для отмены существующей запущенной задачи дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-162">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-163">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="a9dd0-163">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-164">Этот параметр используется для дефрагментации сбалансированного дерева, указанного параметром Сзтабленаме.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-164">This option is used to defrag a B-Tree, specified by szTableName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-165">JET_bitDefragmentBTreeBatch</span><span class="sxs-lookup"><span data-stu-id="a9dd0-165">JET_bitDefragmentBTreeBatch</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-166">Этот параметр используется для вызова OLD2 для всей базы данных.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-166">This option is used to call OLD2 on the entire database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a9dd0-167">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9dd0-167">Return Value</span></span>

<span data-ttu-id="a9dd0-168">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-168">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a9dd0-169">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a9dd0-169">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9dd0-170">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a9dd0-170">Return code</span></span></p></th>
<th><p><span data-ttu-id="a9dd0-171">Описание</span><span class="sxs-lookup"><span data-stu-id="a9dd0-171">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-172">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a9dd0-172">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-173">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-173">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-174">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a9dd0-174">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-175">Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-175">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-176">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="a9dd0-176">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-177">База данных, выбранная для дефрагментации, доступна только для чтения и не может быть обновлена каким-либо образом, включая дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-177">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="a9dd0-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-179">Данный сеанс находится в состоянии "подготовлено к фиксации" и не может начинать новые обновления до фиксации или отката текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-179">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-180">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a9dd0-180">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-181">Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-181">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a9dd0-182">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-182">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-183">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="a9dd0-183">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-184">Заданный идентификатор базы данных не соответствует известной базе данных в экземпляре.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-184">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-185">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a9dd0-185">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-186">Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-186">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-187">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a9dd0-187">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-188">Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-188">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-189">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a9dd0-189">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-190">Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-190">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="a9dd0-191">Эта ошибка будет возвращена только Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-191">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-192">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a9dd0-192">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-193">Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-193">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-194">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="a9dd0-194">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-195">Данный сеанс имеет только права доступа только для чтения и не может запустить задачу, которая может выполнить обновление, включая дефрагментацию.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-195">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-196">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a9dd0-196">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-197">Эта ошибка возникает, если настроенный размер хранилища версий недостаточно для хранения всех необработанных обновлений.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-197">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-198">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="a9dd0-198">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-199">Параметр JET_bitDefragmentBatchStart был передан, но задача дефрагментации уже выполняет дефрагментацию данной базы данных.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-199">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-200">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="a9dd0-200">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="a9dd0-201">Параметр JET_bitDefragmentBatchStop был передан, но в данный момент задача дефрагментации не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-201">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9dd0-202">При успешном выполнении запрошенное действие либо запуск задачи дефрагментации для заданных параметров с заданными параметрами, либо выполнение действия остановка существующей задачи дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-202">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="a9dd0-203">В случае сбоя запрошенное действие запуска или остановки задания оперативной дефрагментации не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-203">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="a9dd0-204">Другие побочные эффекты не возникают.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-204">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a9dd0-205">Remarks</span><span class="sxs-lookup"><span data-stu-id="a9dd0-205">Remarks</span></span>

<span data-ttu-id="a9dd0-206">Оперативная дефрагментация управляется параметром параметра, а также этим API.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-206">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="a9dd0-207">Значение системного параметра по умолчанию — JET_OnlineDefragAll. Это означает, что дефрагментация включена для всех поддерживаемых структур данных.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-207">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="a9dd0-208">Однако с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md)можно отключить оперативную дефрагментацию или выборочно включить ее только для деревьев пространства базы данных, только для потоковых файлов или любого сочетания этих параметров.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-208">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="a9dd0-209">Если параметр системы для автономной дефрагментации находится в устаревшем параметре, **JetDefragment2** будет рассматривать этот параметр как JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-209">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="a9dd0-210">Для каждой базы данных может выполняться не более одной задачи.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-210">There can at most be one task running for each database.</span></span> <span data-ttu-id="a9dd0-211">Задача выполняется как поток в процессе размещения ESE.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-211">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="a9dd0-212">Сеанс, используемый для запуска задачи дефрагментации в сети, можно впоследствии использовать для операций с базой данных во время выполнения задачи дефрагментации, так как задача дефрагментации выделяет собственный сеанс.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-212">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="a9dd0-213">Данный сеанс используется только для проверки разрешений, связанных с начальным сеансом задачи, и фактически не используется для самих операций дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-213">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a9dd0-214">Требования</span><span class="sxs-lookup"><span data-stu-id="a9dd0-214">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-215"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a9dd0-215"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a9dd0-216">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-216">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-217"><strong>Сервер</strong></span><span class="sxs-lookup"><span data-stu-id="a9dd0-217"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a9dd0-218">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-218">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-219"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a9dd0-219"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a9dd0-220">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-220">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-221"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="a9dd0-221"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a9dd0-222">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-222">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9dd0-223"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="a9dd0-223"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a9dd0-224">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a9dd0-224">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9dd0-225"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="a9dd0-225"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a9dd0-226">Реализуется как <strong>JetDefragment2W</strong> (Юникод) и <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a9dd0-226">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a9dd0-227">См. также:</span><span class="sxs-lookup"><span data-stu-id="a9dd0-227">See Also</span></span>

[<span data-ttu-id="a9dd0-228">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a9dd0-228">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a9dd0-229">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a9dd0-229">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a9dd0-230">жеткомпакт</span><span class="sxs-lookup"><span data-stu-id="a9dd0-230">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="a9dd0-231">жетдефрагмент</span><span class="sxs-lookup"><span data-stu-id="a9dd0-231">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="a9dd0-232">жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="a9dd0-232">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a9dd0-233">жетстопсервице</span><span class="sxs-lookup"><span data-stu-id="a9dd0-233">JetStopService</span></span>](./jetstopservice-function.md)
